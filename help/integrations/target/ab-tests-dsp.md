---
title: 在Adobe Target中設定Adobe Advertising DSP廣告的A/B測試
description: 瞭解如何在中設定A/B測試 [!DNL Target] 用於您的DSP廣告。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 7ffa5d3e9f1aae0f9d66d87c74807e491e818daa
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# 在Adobe Target中設定Advertising DSP Ads的A/B測試

*僅使用Advertising DSP的廣告商*

Adobe Advertising和Adobe Target可讓行銷人員更輕鬆地透過付費媒體和站上訊息提供個人化和連線的體驗。 透過在產品之間共用訊號，您可以：

* 將客戶在DSP促銷活動中的廣告曝光度連結至其站上體驗，以降低網站流失率。

* 透過使用Adobe Audience Manager曝光資料和點選摘要來映象廣告訊息的站上體驗，以建立A/B測試 [!DNL Target] 對象。

* 透過Adobe Analytics中的簡單視覺效果，測量整合通訊對網站上的目標提升度的影響，用於 [!DNL Target].

如需必要條件和指示，請參閱下列章節：設定點進和檢視追蹤，以及在DSP和之間實作訊號共用 [!DNL Target] 和設定A/B測試活動，以及設定 [!DNL Analytics] Analysis Workspace以檢視測試資料。

如果您有其他問題，請聯絡adcloud_support@adobe.com。

## 必要條件

此使用案例需要下列產品和整合：

* [!DNL Target]

* [[!DNL Analytics] 適用於廣告](/help/integrations/analytics/overview.md) 整合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 的 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 整合

* Audience Manager（僅對於閱覽測試為必要）

## 步驟1：設定點進架構 {#click-through-framework}

![點進框架](/help/integrations/assets/target-ct-framework.png)

當您將DSP巨集新增至點進URL （使用者點按廣告並到達登陸頁面時顯示的URL）時，DSP會透過以下方式自動擷取位置索引鍵： `${TM_PLACEMENT_ID}` 點進URL中的。 此巨集會擷取英數字元版位索引鍵，而非數值版位ID。

![附加至登陸頁面URL的點進URL](/help/integrations/assets/target-ct-url.jpg)

### (僅限DSP)將DSP巨集新增至您的點進URL

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在Flash交談或Google Campaign Manager 360中，手動更新每個廣告的點進URL，以包含擷取AMO ID變數所需的巨集。 AMO ID變數可用來將點按資料傳送至Adobe Analytics和共用放置索引鍵以進行A/B測試。 如需指示，請參閱下列頁面：

* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)

* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

請聯絡您的Adobe客戶團隊和Advertising Solutions Group (aac-advertising-solutions-group@adobe.com)，以擷取所需的位置索引鍵並完成設定，同時確保每個點進URL都填入位置索引鍵。

## 步驟2：使用Audience Manager設定閱覽架構 {#view-through-framework}

![檢視框架](/help/integrations/assets/targetr-vt-framework.png)

您可以在廣告標籤和位置設定中新增Audience Manager曝光事件畫素，藉此建立測試區段以提供其他閱覽測試機會。

1. 在廣告標籤和DSP版位設定中實作Audience Manager曝光事件畫素。

   如需指示，請參閱&quot;[從Advertising DSP Campaigns收集媒體曝光資料](/help/integrations/audience-manager/media-data-integration/collect.md).」

   請務必新增 [DSP巨集](/help/dsp/campaign-management/macros.md) 擷取您想要曝光事件畫素傳回的所有資料，包括 `${TM_PLACEMENT_ID_NUM}` 以取得數值位置ID。

   >[!NOTE]
   >
   >點選追蹤URL包括 `${TM_PLACEMENT_ID}` 英數字元放置鍵的巨集，而非 `${TM_PLACEMENT_ID_NUM}` 以取得數值位置ID。

1. 從DSP曝光資料設定Audience Manager區段：

   1. 確認區段資料可供使用：

      1. [搜尋訊號](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) 針對 [機碼值組](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) 可決定區段使用者分組的層級。

         使用 [支援的金鑰](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) 其值與新增至Audience Manager曝光事件畫素的巨集相對應。

         例如，若要針對特定位置將使用者分組，請使用 `d_placement` 機碼。 對於值，請使用DSP巨集擷取的實際數值位置ID (例如2501853) `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         如果搜尋結果顯示索引鍵/值組的使用者計數（這表示畫素已正確放置且資料正在流動），則繼續下一個步驟。

   1. [建立規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 用於在Audience Manager中建立區段。

      * 為特徵命名，使其在測試活動中易於識別。 將特徵儲存在您偏好的任何資料夾中。

      * 選取 `Ad Cloud` 作為 **[!UICONTROL Data Source]**.

      * 對於特徵運算式，使用 `d_event` 作為 **[!UICONTROL Key]** 和 `imp` 作為 **[!UICONTROL Value]**.

   1. [設定測試區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) 針對Audience Manager中的新特徵，選取 `Ad Cloud` 作為 **[!UICONTROL Data Source]**.

      Audience Manager會自動將區段分割成控制組，用於接收標準登陸頁面體驗，並分割成測試組，用於接收個人化現場體驗。

## 步驟3：在中設定A/B測試活動 [!DNL Target] 適用於DSP

下列指示會強調與DSP使用案例相關的資訊。

1. [登入Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [建立A/B測試](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在 **[!UICONTROL Enter Activity URL]** 欄位，輸入測試的登入頁面URL。

      >[!NOTE]
      >
      >您可以使用多個URL來測試閱覽網站專案。 如需詳細資訊，請參閱&quot;[多頁活動](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).」 您可以透過建立頁面URL輕鬆識別熱門專案 [網站專案報表](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) Analytics中的。

   1. 在 **[!UICONTROL Goal]** 欄位，輸入測試的成功量度。

      >[!NOTE]
      >
      >請確定 [!DNL Analytics] 在中啟用為資料來源 [!DNL Target]，且已選取正確的報表套裝。

   1. 設定 **[!UICONTROL Priority]** 至 `High` 或 `999` 以避免測試區段中的使用者收到錯誤的站上體驗時發生衝突。

   1. 範圍 **[!UICONTROL Reporting Settings]**，選取 **[!UICONTROL Company Name]** 和 **[!UICONTROL Report Suite]** 已連線至您的DSP帳戶。

      如需其他報表秘訣，請參閱「[報告最佳實務及疑難排解](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).」

   1. 在 **[!UICONTROL Date Range]** 欄位，輸入適當的測試開始與結束日期。

   1. 將對象新增至活動：

      1. 選擇 [您先前在Audience Manager中建立的區段，用於測試閱覽對象](#view-through-framework).

      1. 選取 **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**，然後輸入DSP放置索引鍵，在 **[!UICONTROL Value]** 欄位，用以使用點進對象的Target查詢字串引數。

   1. 對於 **[!UICONTROL Traffic Allocation Method]**，選取 **[!UICONTROL Manual (Default)]** 並以50/50比例分割對象。

   1. 儲存活動。

1. 使用 [Target視覺化體驗撰寫器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 以變更A/B測試登入頁面範本的設計。

   * 體驗A：請勿編輯，因為這是沒有個人化的預設/控制登陸頁面體驗。

   * 體驗B：使用 [!DNL Target] 使用者介面，用來根據測試中包含的資產自訂登入頁面範本（例如標題、復本、按鈕位置和創意）。

   >[!NOTE]
   >
   >例如創意測試使用案例，請聯絡您的Adobe客戶團隊。

## 步驟4：設定您的 [!DNL Analytics for Target] Analysis Workspace於 [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是跨解決方案的整合，可讓廣告商建立 [!DNL Target] 活動依據 [!DNL Analytics] 轉換量度和受眾區段，然後使用測量結果 [!DNL Analytics] 作為報表來源。 該活動的所有報表和區段都根據 [!DNL Analytics] 資料彙集。

有關詳細資訊 [!DNL Analytics for Target]，包括實作指示的連結，請參閱&quot;[Adobe Analytics作為Adobe Target (A4T)的報表來源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)「。

### 設定 [!DNL Analytics for Target] 面板

在Analysis Workspace中，設定 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活動和體驗。 請牢記以下與報表相關的重要指標與資訊。

#### 量度

* 在工作區中建立面板，專用於執行測試的Adobe Advertising促銷活動、套件或位置。 使用摘要視覺效果顯示與相同報表中的Adobe Advertising量度 [!DNL Target] 測試效能。

* 優先使用站上量度（例如造訪和轉換）來測量效能。

* 瞭解Adobe Advertising的彙總媒體量度（例如曝光數、點按數和成本）無法與比對 [!DNL Target] 量度。

#### Dimension

下列維度與 [!DNL Analytics for Target]：

* **[!UICONTROL Target Activities]**： A/B測試的名稱

* **[!UICONTROL Target Experiences]**：活動內使用的登入頁面體驗名稱

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**：同一列中的活動名稱和體驗名稱

### 疑難排解Analytics for [!DNL Target] 資料

在Analysis Workspace中，如果您發現活動和體驗資料很少或未填入，則請執行以下操作：

* 確認相同 [!UICONTROL Supplemental Data ID] (SDID)會用於兩者 [!DNL Target] 和 [!DNL Analytics]. 您可以使用驗證SDID值 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 在行銷活動將使用者引導至的登陸頁面上。

[Adobe Debugger中的補充資料ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在相同登陸頁面上，確認a) [!UICONTROL Hostname] 顯示在Adobe Debugger底下 [!UICONTROL Solutions] > [!UICONTROL Target] 比對b) [!UICONTROL Tracking Server] 顯示於 [!DNL Target] 針對活動(在 [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings])。

  [!DNL Analytics For Target] 需要 [!DNL Analytics] 要以呼叫傳送的追蹤伺服器 [!DNL Target] 至 [!DNL Modstats] Analytics的資料收集伺服器。<!-- just "to Analytics?"-->

[Adobe Debugger的主機名稱值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的追蹤伺服器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 進一步閱讀

* [將Target與Analytics整合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)  — 說明如何設定 [!DNL Target] Analysis Workspace中的報告。
* [A/B測試概覽](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 說明可搭配DSP廣告使用的A/B測試活動。
* [體驗與選件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html)  — 說明 [!DNL Target] 用於判斷DSP測試使用者會接觸到哪些站上內容的工具。
* [訊號、特徵和區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html)  — 定義有助於進行DSP閱覽測試的一些Audience Manager工具。
* [Analytics for Advertising概述](/help/integrations/analytics/overview.md)  — 引進Analytics for Advertising，可讓您追蹤Analytics例項中的點進和檢視網站互動。

>[!MORELIKETHIS]
>
>* [在Adobe Target中設定廣告搜尋、社交和商務廣告的A/B測試](ab-tests-search.md)
