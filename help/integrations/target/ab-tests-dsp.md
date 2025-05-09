---
title: 在Adobe Target中設定Adobe Advertising DSP Ads的A/B測試
description: 瞭解如何在 [!DNL Target] 中為您的DSP廣告設定A/B測試。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# 在Adobe Target中為Advertising DSP廣告設定A/B測試

*僅使用Advertising DSP的廣告商*

Adobe Advertising和Adobe Target可讓行銷人員更輕鬆地透過付費媒體和站上訊息提供個人化和連線的體驗。 透過在產品之間共用訊號，您可以：

* 將客戶在DSP行銷活動中的廣告曝光度連結至其站上體驗，以降低網站流失率。

* 透過使用Adobe Audience Manager曝光資料和點按摘要[!DNL Target]對象來映象廣告訊息的站上體驗，以建立A/B測試。

* 透過Adobe Analytics中針對[!DNL Target]的簡單視覺效果，測量整合通訊對站上目標提升的影響。

請參閱下列章節，瞭解先決條件，以及設定點進和檢視追蹤、實作DSP與[!DNL Target]之間的訊號共用、設定A/B測試活動，以及設定[!DNL Analytics] Analysis Workspace以檢視測試資料的指示。

如果您有其他問題，請聯絡adcloud_support@adobe.com。

## 先決條件

此使用案例需要下列產品和整合：

* [!DNL Target]

* 用於Advertising](/help/integrations/analytics/overview.md)整合的[[!DNL Analytics] <!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 用於 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)整合

* Audience Manager （僅針對閱覽測試需要）

## 步驟1：設定點進架構 {#click-through-framework}

![點進架構](/help/integrations/assets/target-ct-framework.png)

當您將DSP巨集新增至點進URL （使用者點按廣告並到達登陸頁面時顯示的URL）時，DSP會在點進URL中加入`${TM_PLACEMENT_ID}`，自動擷取位置索引鍵。 此巨集會擷取英數字元版位索引鍵，而非數值版位ID。

![點進URL已附加至登陸頁面URL](/help/integrations/assets/target-ct-url.jpg)

### (僅限DSP)將DSP巨集新增至您的點進URL

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在[!DNL Flashtalking]或Google Campaign Manager 360中，手動更新每個廣告的點進URL，以包含擷取AMO ID變數所需的巨集。 AMO ID變數可用來將點按資料傳送至Adobe Analytics和共用放置索引鍵以進行A/B測試。 如需指示，請參閱下列頁面：

* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)。 **注意：**&#x200B;如果您的組織與[!DNL Flashtalking]有直接的合作關係，而且您根據[!DNL Flashtalking]支援檔案(位於[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros))中的`s_kwcid`與`ef_id`追蹤引數，則不需要執行此程式。

* [將 [!DNL Analytics for Advertising] 巨集附加至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

請聯絡您的Adobe客戶團隊和Advertising解決方案群組(aac-advertising-solutions-group@adobe.com)，以擷取所需的位置索引鍵並完成設定，同時確保每個點進URL皆填入位置索引鍵。

## 步驟2：使用Audience Manager設定閱覽架構 {#view-through-framework}

![檢視框架](/help/integrations/assets/targetr-vt-framework.png)

您可以在廣告標籤和版位設定中新增Audience Manager曝光事件畫素，藉此建立測試區段以提供其他閱覽測試機會。

1. 在廣告標籤和DSP版位設定中實作Audience Manager曝光事件畫素。

   如需指示，請參閱「[從Advertising DSP Campaigns](/help/integrations/audience-manager/media-data-integration/collect.md)收集媒體曝光資料」。

   請務必新增[DSP巨集](/help/dsp/campaign-management/macros.md)以擷取您要讓曝光事件畫素傳回的所有資料，包括數值位置ID的`${TM_PLACEMENT_ID_NUM}`。

   >[!NOTE]
   >
   >點選追蹤URL包含英數字元版位索引鍵的`${TM_PLACEMENT_ID}`巨集，而非數值版位ID的`${TM_PLACEMENT_ID_NUM}`。

1. 從DSP曝光資料設定Audience Manager區段：

   1. 確認區段資料可供使用：

      1. [搜尋[索引鍵值配對](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html)的訊號](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html)，以決定區段使用者在哪個層級分組。

         使用具有對應至您新增至Audience Manager曝光事件畫素之巨集值的[支援索引鍵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html)。

         例如，若要針對特定位置將使用者分組，請使用`d_placement`索引鍵。 對於值，請使用DSP巨集`${TM_PLACEMENT_ID_NUM}`擷取的實際數值位置ID (例如2501853)。<!-- Explain where to find the placement ID, other than in a custom report. -->

         如果搜尋結果顯示索引鍵/值組的使用者計數（這表示畫素已正確放置且資料正在流動），則繼續下一個步驟。

   1. [在Audience Manager中建立規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html)，以建立區段。

      * 為特徵命名，使其在測試活動中易於識別。 將特徵儲存在您偏好的任何資料夾中。

      * 選取`Ad Cloud`做為&#x200B;**[!UICONTROL Data Source]**。

      * 對於特徵運算式，使用`d_event`作為&#x200B;**[!UICONTROL Key]**，使用`imp`作為&#x200B;**[!UICONTROL Value]**。

   1. [在Audience Manager中設定新特徵的測試區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html)，選取`Ad Cloud`做為&#x200B;**[!UICONTROL Data Source]**。

      Audience Manager會自動將區段分割成控制組，用於接收標準登陸頁面體驗，並分割成測試組，用於接收個人化現場體驗。

## 步驟3：在[!DNL Target]中為DSP設定A/B測試活動

下列指示會強調與DSP使用案例相關的資訊。

1. [登入Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)。

1. [建立A/B測試](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在&#x200B;**[!UICONTROL Enter Activity URL]**&#x200B;欄位中，輸入測試的登陸頁面URL。

      >[!NOTE]
      >
      >您可以使用多個URL來測試閱覽網站專案。 如需詳細資訊，請參閱[多頁活動](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)。 您可以在Analytics中建立[網站專案報告](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports)，依頁面URL輕鬆識別熱門專案。

   1. 在&#x200B;**[!UICONTROL Goal]**&#x200B;欄位中輸入測試的成功量度。

      >[!NOTE]
      >
      >請確定[!DNL Analytics]已在[!DNL Target]內啟用為資料來源，且已選取正確的報表套裝。

   1. 將&#x200B;**[!UICONTROL Priority]**&#x200B;設為`High`或`999`，以防止測試區段中的使用者收到錯誤的站台體驗時發生衝突。

   1. 在&#x200B;**[!UICONTROL Reporting Settings]**&#x200B;內，選取連線至您DSP帳戶的&#x200B;**[!UICONTROL Company Name]**&#x200B;和&#x200B;**[!UICONTROL Report Suite]**。

      如需其他報告秘訣，請參閱「[報告最佳實務和疑難排解](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)」。

   1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;欄位中，輸入適當的測試開始與結束日期。

   1. 將對象新增至活動：

      1. 選擇您先前在Audience Manager中建立的[區段，以測試閱覽對象](#view-through-framework)。

      1. 選取「**[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**」，然後在「**[!UICONTROL Value]**」欄位中輸入DSP位置索引鍵，以使用點進對象的Target查詢字串引數。

   1. 針對&#x200B;**[!UICONTROL Traffic Allocation Method]**，選取&#x200B;**[!UICONTROL Manual (Default)]**&#x200B;並以50/50分割對象。

   1. 儲存活動。

1. 使用[Target視覺化體驗撰寫器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)，對A/B測試登入頁面範本進行設計變更。

   * 體驗A：請勿編輯，因為這是沒有個人化的預設/控制登陸頁面體驗。

   * 體驗B：使用[!DNL Target]使用者介面，根據測試中包含的資產自訂登入頁面範本（例如標題、復本、按鈕位置和創意）。

   >[!NOTE]
   >
   >例如創意測試使用案例，請聯絡您的Adobe客戶團隊。

## 步驟4：在[!DNL Analytics]中設定您的[!DNL Analytics for Target] Analysis Workspace

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是跨解決方案的整合，可讓廣告商根據[!DNL Analytics]轉換量度和受眾區段來建立[!DNL Target]個活動，然後使用[!DNL Analytics]做為報表來源來測量結果。 該活動的所有報表和區段都以[!DNL Analytics]資料收集為基礎。

如需[!DNL Analytics for Target]的詳細資訊，包括實作指示的連結，請參閱&quot;[Adobe Analytics作為Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)的報告來源&quot;。

### 設定[!DNL Analytics for Target]面板

在Analysis Workspace中，設定[!DNL Analytics for Target panel]以分析您的[!DNL Target]活動和體驗。 請牢記以下與報表相關的重要指標與資訊。

#### 量度

* 在工作區中建立面板，專用於執行測試的Adobe Advertising行銷活動、套件或位置。 使用摘要視覺效果，在與[!DNL Target]測試效能相同的報表中顯示Adobe Advertising量度。

* 優先使用站上量度（例如造訪和轉換）來測量效能。

* 瞭解Adobe Advertising的彙總媒體量度（例如曝光數、點按數和成本）無法與[!DNL Target]量度比對。

#### 維度

下列維度與[!DNL Analytics for Target]有關：

* **[!UICONTROL Target Activities]**： A/B測試的名稱

* **[!UICONTROL Target Experiences]**：活動中使用的登入頁面體驗名稱

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**：活動名稱和體驗名稱在同一列

### 疑難排解[!DNL Target]資料的Analytics

在Analysis Workspace中，如果您發現活動和體驗資料很少或未填入，則請執行以下操作：

* 確認相同的[!UICONTROL Supplemental Data ID] (SDID)同時用於[!DNL Target]和[!DNL Analytics]。 您可以在行銷活動驅動使用者的登陸頁面上使用[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)，以驗證SDID值。

[Adobe Debugger中的補充資料ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在相同登入頁面上，確認a) [!UICONTROL Solutions] > [!UICONTROL Target]底下之Adobe Debugger中顯示的[!UICONTROL Hostname]符合b)活動（[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]底下） [!DNL Target]中顯示的[!UICONTROL Tracking Server]。

  [!DNL Analytics For Target]需要從[!DNL Target]傳送追蹤伺服器至Analytics之[!DNL Modstats]資料收集伺服器的呼叫中的[!DNL Analytics]追蹤伺服器。<!-- just "to Analytics?"-->

[Adobe Debugger中的主機名稱值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的追蹤伺服器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 進一步閱讀

* [將Target與Analytics整合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 說明如何在Analysis Workspace中設定[!DNL Target]報告。
* [A/B測試總覽](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) — 說明可搭配DSP廣告使用的A/B測試活動。
* [體驗與選件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) — 說明[!DNL Target]用來判斷DSP測試使用者公開之站上內容的工具。
* [訊號、特徵和區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) — 定義有助於進行DSP閱覽測試的一些Audience Manager工具。
* [Advertising適用的Analytics概觀](/help/integrations/analytics/overview.md) — 介紹Advertising適用的Analytics，其可讓您追蹤Analytics執行個體中的點進和檢視網站互動。

>[!MORELIKETHIS]
>
>* [在Adobe Target中設定Advertising Search、Social和Commerce Ads的A/B測試](ab-tests-search.md)
