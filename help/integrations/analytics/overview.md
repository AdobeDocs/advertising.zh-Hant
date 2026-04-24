---
title: ' [!DNL Analytics for Advertising]的概觀'
description: ' [!DNL Analytics for Advertising]的概觀'
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
TQID: https://experienceleague.adobe.com/OHxJO1mtbzOtt5oGDJF26xSuVLG-HnRDdIGDrUH2pzk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1306
ht-degree: 0%

---

# [!DNL Analytics for Advertising]的概觀

*使用Advertising Creative、Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*&#x200B;的廣告商

[!DNL Analytics for Advertising]整合Adobe Analytics和Adobe Advertising以擴充和增強每個產品的功能。

此整合可讓廣告商追蹤其[!DNL Analytics]執行個體中的點進和檢視網站互動，讓品牌瞭解其廣告支出如何帶來網站參與度和關鍵業務目標。

此外，Adobe Advertising可以存取使用網站上已有的[!DNL Analytics]標籤由[!DNL Analytics]收集而來的龐大第一方資料。 這可讓歷程管理、第一方再行銷和付費媒體網站報告功能更加健全。 Adobe Advertising可進一步使用[!DNL Analytics]資料來最佳化支出和競標。

若正確使用，[!DNL Analytics for Advertising]會模糊兩個傳統角色之間的界限：廣告歷程管理（透過廣告將使用者送往網站的動作）和透過網站分析瞭解該網站的參與。

主要優點：

* 將[!DNL Analytics]區段直接傳送至Adobe Advertising，以供第一方網站再行銷。
* 使用[!DNL Analytics]個自訂和標準事件作為轉換訊號，以最佳化付費媒體廣告。
* 利用[!DNL Analytics] Analysis Workspace來更瞭解網站進入點和造訪行為。
* 讓網頁分析人員與付費媒體團隊更緊密地共同作業。
* 在[!DNL Analytics]內使用永續性Adobe Advertising檢視和點進ID來瞭解網站參與情形。
* 將資料或畫素匯出至廣告伺服器或其他DSP時，無法在Analysis Workspace中使用自訂量度、自訂維度和網站活動來增強傳統付費媒體報表。
* 善用網站上已有的[!DNL Analytics]程式碼，以便在Adobe Advertising中追蹤和最佳化。

>[!TIP]
>
> 觀看[介紹 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics)的影片。

## 使用Analytics製作付費媒體報表

[!DNL Analytics for Advertising]允許您：

* 在[!DNL Analytics]內使用永續性Adobe Advertising檢視和點進ID來瞭解網站參與情形。
* 利用Analysis Workspace深入瞭解網站登入點和造訪行為。 您可以存取付費媒體維度和事件資料，其中包括Adobe Advertising行銷活動實體名稱（包括版位和廣告）及其相關量度，例如點按數、曝光數和成本。

若要使用[!DNL Analytics]作為您的付費媒體報告工具，您的組織需要Adobe CX Enterprise （前身為Adobe Experience Cloud）登入才能存取Analysis Workspace。 您的Adobe Advertising團隊將協助您將您的Adobe Advertising資料對應至Analysis Workspace中的個別報表套裝。 您可以將Adobe Advertising資料傳送至任何報表套裝，但您應留意已對應至Adobe Advertising的報表套裝以及尚未對應的報表套裝。 依報表套裝而定，這可能會變更報告的資料。

 [!DNL Analytics]](ids.md)內的[Adobe Advertising ID與其他[!DNL eVars]一樣運作，具有自訂、永久的有效期。 在Adobe Advertising實作期間，歸因回顧期間預設為60天。 若要變更此設定，請與您的Adobe帳戶團隊合作。

Adobe Advertising維度會附加尾碼「(AMO ID)」(例如「廣告型別(AMO ID)」)。 如需可用維度的清單，請參閱&quot;[Analysis Workspace中的Adobe Advertising量度](advertising-metrics-in-analytics.md)&quot;。

>[!NOTE]
>
> 在[!DNL Analytics]中檢視Adobe Advertising資料（或任何資料集）時，請注意，量度和報表是根據[!DNL Analytics]中設定的規則。 資料可能不同於您在其他報告系統中看到的資料，例如廣告伺服器報告、[!DNL DSP]報告或搜尋引擎報告。 若要瞭解[!DNL Analytics]中的資料差異，您必須知道[!DNL eVar]資料何時過期、什麼定義了造訪、什麼被視為上次接觸歸因與總持續歸因，以及其他因素。 如需詳細資訊，請參閱[ [!DNL Analytics] 與Adobe Advertising](data-variances.md)之間的預期資料差異。

## 使用Analytics來推動Adobe Advertising行銷活動和產品組合

[!DNL Analytics for Advertising]不需要任何額外的畫素，即可將兩個主要訊號傳送至Adobe Advertising，讓最佳化更好，對象分割更容易：

* 要當作競標訊號使用的轉換量度：
   * 標準量度，例如[!UICONTROL Revenue]和[!UICONTROL Cart Views]。
   * 網站參與量度，例如頁面檢視和造訪量度。
   * 自訂收入量度。
   * reserved revenue metrics.
* Segments created in [!DNL Analytics] and published to CX Enterprise.

  You can use [!DNL Analytics] segments for first-party site retargeting in [!DNL DSP], [!DNL Creative], and paid search advertisements.

  ([!DNL Search, Social, & Commerce] only) Advertisers with [!DNL Analytics] but not Audience Manager can also create Google website tag-based audiences (remarketing lists) and customer match audiences (customer lists) from [!DNL Analytics] segments that are shared with CX Enterprise.

### Site conversion metrics as bid signals

You can use your standard events and custom events from [!DNL Analytics] to build weighted objectives in Adobe Advertising. Objectives inform bidding decisions for your [!DNL DSP] packages and Search, Social, &amp; Commerce portfolios.

For [!DNL Google Ads] and [!DNL Google Microsoft Advertising] campaigns in Search, Social, &amp; Commerce hybrid portfolios, you can optionally upload the objectives — including any [!DNL Analytics] events in the objectives — directly to the ad networks, where they become available as conversion actions for account-level and campaign-level custom conversion goals.

>[!NOTE]
>
> You can&#39;t map calculated metrics from [!DNL Analytics] into Adobe Advertising.

Your Adobe Advertising team will help you to identify and map the events that are applicable to paid media performance into Adobe Advertising.

See &quot;[Analytics Metrics in Adobe Advertising](analytics-data-in-advertising.md)&quot; for a list of available metrics.

### Analytics segments for site retargeting

Adobe Advertising can ingest [!DNL Analytics] segments for remarketing purposes for [!DNL Creative], [!DNL DSP], and [!DNL Search, Social, & Commerce] ads using the native CX Enterprise Audiences integration between [!DNL Analytics] and CX Enterprise.

To access the [!DNL Analytics] segments, an advertiser account must enable the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). When the ID Service is enabled, all CX Enterprise segments become available within Adobe Advertising as soon as they are processed. CX Enterprise segments include segments created in [!DNL Analytics] and published to CX Enterprise, segments created in Adobe Audience Manager, segments created in CX Enterprise using the [!DNL People core service], and segments created in Adobe Experience Platform and sent to Adobe Advertising via Audience Manager.

[!DNL Analytics] segments are available within 24 hours and are updated daily.

For more information about the CX Enterprise Audiences service, see [CX Enterprise Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Examples of how to use the integration {#integration-examples}

### Using Adobe Advertising data in Analysis Workspace

To learn how you can use your Adobe Advertising data to create visual reports in Analysis Workspace, see the video &quot;[Introduction to Workspace and Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Using connected TV view-through conversions in reports

*Advertising DSP users only*

You can measure the full-funnel effectiveness of your connected TV (CTV) campaigns by linking ad exposure on CTV devices to on-site conversions. The new [!UICONTROL Landing Type] filter &quot;[!UICONTROL View-through (CTV)]&quot; splits conversions into separate rows for [!UICONTROL Click Through], [!UICONTROL View Through], and [!UICONTROL View Through (CTV)] values.

若要檢視您的CTV觀看轉換量度，請使用Analysis Workspace中的「位置」檢視或「行銷管道」檢視。

使用「位置」檢視：

1. 在報表檢視中包含CTV花費位置。

1. 包括所需的量度，例如「曝光數」、「點按數」等。

1. 套用下列篩選器：

   廣告平台： `Advertising Cloud DSP`

   登陸頁面： `View-Through (CTV)`

使用行銷管道檢視：

1. 包含維度`Marketing Channel`。

1. 包括所需的量度，例如「曝光數」、「點按數」等。

1. 套用下列篩選器：

   廣告平台： `Advertising Cloud DSP`

   登陸頁面： `View-Through (CTV)`

### 建立Adobe Advertising控制面板

若要瞭解如何根據Analysis Workspace中的目標追蹤Adobe Advertising資料，請參閱影片「使用Adobe Analytics建立Adobe Advertising儀表板](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)」。[

### 使用Adobe Advertising ID進行網站專案分析

若要瞭解如何建立Adobe Advertising網站專案報告，以監視一週中的某天、一天中的某一時間、瀏覽器和地理影響，請參閱影片「[建立Adobe Advertising網站專案報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)」。

## 如何起始[!DNL Analytics for Advertising]實作

請聯絡您的Adobe客戶團隊，他們將會完成開始所需的初始設定，並將幫助您根據組織的需求規劃實施與資料使用。

>[!MORELIKETHIS]
>
>* [影片： [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)簡介
>* [實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]](prerequisites.md)
>* Analytics使用的[Adobe Advertising ID](ids.md)
>* 適用於Advertising的Analytics的[JavaScript程式碼](/help/integrations/analytics/javascript.md)
>* [ [!DNL Analytics] 與Adobe Advertising](data-variances.md)之間的預期資料差異
>* Analysis Workspace中的[Adobe Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
