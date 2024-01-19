---
title: 在Adobe Target中設定Adobe Advertising搜尋、社交和商務廣告的A/B測試
description: 瞭解如何在中設定A/B測試 [!DNL Target] 針對您的 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 搜尋、社交和商務中的廣告。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# 在Adobe Target中設定廣告搜尋、社交和商務廣告的A/B測試

*僅含廣告搜尋、社交和商務的廣告商*

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 僅限帳戶*

Adobe Advertising和Adobe Target可讓您輕鬆設定數位廣告流量的登陸頁面體驗A/B測試 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 至：

* 改善轉換率(CVR)和贏取效率測量（例如CPA、CPL和CAC）。

* 提供與廣告相關的更個人化的登陸頁面體驗（例如，比對登陸頁面的影像/影片創意、復本、關鍵字或其他廣告訊號）。

您也可以合併原生 [[!DNL Analytics] 適用於廣告](/help/integrations/analytics/overview.md) 和 [[!DNL Analytics] 的 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 整合報表維度已整合至Adobe Analytics，可透過測量並視覺化您的測試資料 [!DNL Analytics] 量度和成功事件。

請參閱下列章節，瞭解中的先決條件，以及設定A/B測試的指示 [!DNL Target] 以取得來自Search、Social和Commerce中廣告的點進流量，以及有關如何在中衡量和視覺化您的測試的秘訣 [!DNL Analytics].

## 必要條件

### 必要產品

* 搜尋、社交和商務
* [!DNL Target]

### 建議的產品和整合

* [!DNL Analytics]

* [[!DNL Analytics] 適用於廣告](/help/integrations/analytics/overview.md) 整合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 的 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 整合

## 步驟1：在中建立A/B測試活動 [!DNL Target] 用於搜尋、社交和商務

下列指示會強調與搜尋、社交和商務使用案例相關的資訊。

1. [登入Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [建立A/B測試](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在 **[!UICONTROL Enter Activity URL]** 欄位，輸入測試的登入頁面URL。

   1. 在 **[!UICONTROL Goal]** 欄位，輸入測試的成功量度。

      >[!NOTE]
      >
      >請確定 [!DNL Analytics] 在中啟用為資料來源 [!DNL Target]，且已選取正確的報表套裝。

   1. 設定 **[!UICONTROL Priority]** 至 `High` 或 `999` 以避免測試區段中的使用者收到錯誤的站上體驗時發生衝突。


   1. 範圍 **[!UICONTROL Reporting Settings]**，選取 **[!UICONTROL Company Name]** 和 **[!UICONTROL Report Suite]** 已連線至您的搜尋、社交和商務帳戶。

      如需其他報表秘訣，請參閱「[報告最佳實務及疑難排解](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).」

   1. 在 **[!UICONTROL Date Range]** 欄位，輸入適當的測試開始與結束日期。

   1. 選取 **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. 在 **[!UICONTROL Value]** 欄位，輸入 [!UICONTROL Network Account ID]， [!UICONTROL Network Campaign ID]， [!UICONTROL Network Adgroup ID]，或 [!UICONTROL Network Ad ID] 搜尋、社交和商務中相關廣告網路實體的資訊。 這可讓您使用 [!DNL Target] 實體的點進對象適用的查詢字串引數。

      您可透過以下方式找到ID [將相關ID欄新增至實體檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] 中的欄 [!UICONTROL Accounts] 檢視](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] 中的欄 [!UICONTROL Accounts] 檢視")

      如果您需要協助，請與您的Adobe客戶團隊合作。

   1. 對於 **[!UICONTROL Traffic Allocation Method]**，選取 **[!UICONTROL Manual (Default)]** 並以50/50比例分割對象。

   1. 儲存活動。

1. 使用 [Target視覺化體驗撰寫器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 以變更A/B測試登入頁面範本的設計。

   * 體驗A：請勿編輯，因為這是沒有個人化的預設/控制登陸頁面體驗。

   * 體驗B：使用 [!DNL Target] 使用者介面，用來根據測試中包含的資產自訂登入頁面範本（例如標題、復本、按鈕位置和創意）。

   >[!NOTE]
   >
   >例如創意測試使用案例，請聯絡您的Adobe客戶團隊。

## 步驟2：設定您的 [!DNL Analytics for Target] Analysis Workspace於 [!DNL Analytics]

[!DNL Analytics for Target] (A4T)是跨解決方案的整合，可讓廣告商建立 [!DNL Target] 活動依據 [!DNL Analytics] 轉換量度和受眾區段，然後使用測量結果 [!DNL Analytics] 作為報表來源。 該活動的所有報表和區段都根據 [!DNL Analytics] 資料彙集。

有關詳細資訊 [!DNL Analytics for Target]，包括實作指示的連結，請參閱&quot;[Adobe Analytics作為Adobe Target (A4T)的報表來源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)「。

### 設定 [!DNL Analytics for Target] 面板

在Analysis Workspace中，設定 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活動和體驗。 請牢記以下與報表相關的重要指標與資訊。

#### 量度

* 在工作區中建立Adobe Advertising帳戶、行銷活動或廣告群組專用的面板<!-- only applicable entities? --> 執行測試的對象。 使用摘要視覺效果顯示與相同報表中的Adobe Advertising量度 [!DNL Target] 測試效能。

* 優先使用站上量度（例如造訪和轉換）來測量效能。

* 瞭解Adobe Advertising的彙總媒體量度（例如曝光數、點按數和成本）無法與比對 [!DNL Target] 量度。

#### Dimension

下列維度與 [!DNL Analytics for Target]：

* **目標活動**： A/B測試的名稱

* **Target體驗**：活動內使用的登入頁面體驗名稱

* **Target活動** > **體驗**：同一列中的活動名稱和體驗名稱

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
* [A/B測試概覽](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 說明A/B測試活動，您可將其用於搜尋、社交和商務廣告。
* [Analytics for Advertising概述](/help/integrations/analytics/overview.md)  — 引進Analytics for Advertising，可讓您追蹤Analytics例項中的點進和檢視網站互動。

>[!MORELIKETHIS]
>
>* [在Adobe Target中設定Advertising DSP Ads的A/B測試](ab-tests-dsp.md)
