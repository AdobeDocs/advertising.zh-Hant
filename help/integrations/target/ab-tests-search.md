---
title: 在Adobe Target中設定Adobe Advertising搜尋、社交和Commerce廣告的A/B測試
description: 瞭解如何在 [!DNL Target] 中為搜尋、社交和Commerce中的 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 廣告設定A/B測試。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# 在Adobe Target中為Advertising搜尋、社交和Commerce廣告設定A/B測試

*僅使用Advertising Search、Social和Commerce的廣告商*

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶*

Adobe Advertising和Adobe Target可讓您輕鬆為數位廣告流量[!DNL Google Ads]和[!DNL Microsoft Advertising]設定登陸頁面體驗A/B測試，以：

* 改善轉換率(CVR)和贏取效率測量（例如CPA、CPL和CAC）。

* 提供與廣告相關的更個人化的登陸頁面體驗（例如，比對登陸頁面的影像/影片創意、復本、關鍵字或其他廣告訊號）。

您也可以結合Advertising](/help/integrations/analytics/overview.md)的原生[[!DNL Analytics] 與整合至Adobe Analytics的 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)整合報表維度的[[!DNL Analytics] ，以透過[!DNL Analytics]量度和成功事件測量及視覺化您的測試資料。

請參閱下列各節以瞭解先決條件、在[!DNL Target]中設定A/B測試的指示(來自Search、Social和Commerce中的廣告點進流量)，以及如何在[!DNL Analytics]中測量和視覺化測試的秘訣。

## 必要條件

### 必要產品

* 搜尋、社交和Commerce
* [!DNL Target]

### 建議的產品和整合

* [!DNL Analytics]

* 用於Advertising](/help/integrations/analytics/overview.md)整合的[[!DNL Analytics] <!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 用於 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)整合

## 步驟1：在[!DNL Target]中建立A/B測試活動，以搜尋、社交和Commerce

下列指示會醒目顯示與搜尋、社交和Commerce使用案例相關的資訊。

1. [登入Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)。

1. [建立A/B測試](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在&#x200B;**[!UICONTROL Enter Activity URL]**&#x200B;欄位中，輸入測試的登陸頁面URL。

   1. 在&#x200B;**[!UICONTROL Goal]**&#x200B;欄位中輸入測試的成功量度。

      >[!NOTE]
      >
      >請確定[!DNL Analytics]已在[!DNL Target]內啟用為資料來源，且已選取正確的報表套裝。

   1. 將&#x200B;**[!UICONTROL Priority]**&#x200B;設為`High`或`999`，以防止測試區段中的使用者收到錯誤的站台體驗時發生衝突。


   1. 在&#x200B;**[!UICONTROL Reporting Settings]**&#x200B;內，選取連線至您搜尋、社交和Commerce帳戶的&#x200B;**[!UICONTROL Company Name]**&#x200B;和&#x200B;**[!UICONTROL Report Suite]**。

      如需其他報告秘訣，請參閱「[報告最佳實務和疑難排解](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)」。

   1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;欄位中，輸入適當的測試開始與結束日期。

   1. 選取&#x200B;**[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**。 在&#x200B;**[!UICONTROL Value]**&#x200B;欄位中，針對「搜尋」、「社交」和「Commerce」的相關廣告網路實體，輸入[!UICONTROL Network Account ID]、[!UICONTROL Network Campaign ID]、[!UICONTROL Network Adgroup ID]或[!UICONTROL Network Ad ID]。 這可讓您針對實體的點進對象使用[!DNL Target]查詢字串引數。

      您可以[將相關的識別碼資料行新增至實體檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)來尋找識別碼。

      在[!UICONTROL Accounts]檢視")的[!UICONTROL Accounts]檢視](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID]資料行中的![[!UICONTROL Network Account ID]資料行

      如果您需要協助，請與您的Adobe客戶團隊合作。

   1. 針對&#x200B;**[!UICONTROL Traffic Allocation Method]**，選取&#x200B;**[!UICONTROL Manual (Default)]**&#x200B;並以50/50分割對象。

   1. 儲存活動。

1. 使用[Target視覺化體驗撰寫器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)，對A/B測試登入頁面範本進行設計變更。

   * 體驗A：請勿編輯，因為這是沒有個人化的預設/控制登陸頁面體驗。

   * 體驗B：使用[!DNL Target]使用者介面，根據測試中包含的資產自訂登入頁面範本（例如標題、復本、按鈕位置和創意）。

   >[!NOTE]
   >
   >例如創意測試使用案例，請聯絡您的Adobe客戶團隊。

## 步驟2：在[!DNL Analytics]中設定您的[!DNL Analytics for Target] Analysis Workspace

[!DNL Analytics for Target] (A4T)是跨解決方案的整合，可讓廣告商根據[!DNL Analytics]轉換量度和受眾區段來建立[!DNL Target]個活動，然後使用[!DNL Analytics]做為報表來源來測量結果。 該活動的所有報表和區段都以[!DNL Analytics]資料收集為基礎。

如需[!DNL Analytics for Target]的詳細資訊，包括實作指示的連結，請參閱&quot;[Adobe Analytics作為Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)的報告來源&quot;。

### 設定[!DNL Analytics for Target]面板

在Analysis Workspace中，設定[!DNL Analytics for Target panel]以分析您的[!DNL Target]活動和體驗。 請牢記以下與報表相關的重要指標與資訊。

#### 量度

* 在工作區中建立專屬於執行測試之Adobe Advertising帳戶、行銷活動或廣告群組<!-- only applicable entities? -->的面板。 使用摘要視覺效果顯示同一報表中的Adobe Advertising度量作為[!DNL Target]測試效能。

* 優先使用站上量度（例如造訪和轉換）來測量效能。

* 瞭解Adobe Advertising的彙總媒體量度（例如曝光數、點按數和成本）無法與[!DNL Target]量度比對。

#### Dimension

下列維度與[!DNL Analytics for Target]有關：

* **目標活動**： A/B測試的名稱

* **目標體驗**：活動中使用的登陸頁面體驗名稱

* **Target活動** > **體驗**：活動名稱和體驗名稱在同一列

### 疑難排解[!DNL Target]資料的Analytics

在Analysis Workspace中，如果您發現活動和體驗資料很少或未填入，則請執行以下操作：

* 確認相同的[!UICONTROL Supplemental Data ID] (SDID)同時用於[!DNL Target]和[!DNL Analytics]。 您可以在行銷活動驅動使用者的登陸頁面上使用[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)，以驗證SDID值。

[Adobe Debugger中的補充資料ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在相同登入頁面上，確認a) [!UICONTROL Solutions] > [!UICONTROL Target]底下之Adobe Debugger中顯示的[!UICONTROL Hostname]符合b)活動（[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]底下） [!DNL Target]中顯示的[!UICONTROL Tracking Server]。

  [!DNL Analytics For Target]需要從[!DNL Target]傳送追蹤伺服器至Analytics之[!DNL Modstats]資料收集伺服器的呼叫中的[!DNL Analytics]追蹤伺服器。<!-- just "to Analytics?"-->

[Adobe Debugger的主機名稱值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的追蹤伺服器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 進一步閱讀

* [將Target與Analytics整合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 說明如何在Analysis Workspace中設定[!DNL Target]報告。
* [A/B測試概覽](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) — 說明A/B測試活動，您可以將其用於搜尋、社交和Commerce廣告。
* [Advertising適用的Analytics概觀](/help/integrations/analytics/overview.md) — 介紹Advertising適用的Analytics，其可讓您追蹤Analytics執行個體中的點進和檢視網站互動。

>[!MORELIKETHIS]
>
>* [在Adobe Target中設定Advertising DSP Ads的A/B測試](ab-tests-dsp.md)
