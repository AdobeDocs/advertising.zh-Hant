---
title: ' [!DNL Analytics for Advertising]的概觀'
description: ' [!DNL Analytics for Advertising]的概觀'
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 8911f6ea16878bede96151f004e6de2717484140
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# [!DNL Analytics for Advertising]的概觀

*使用Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*&#x200B;的廣告商

[!DNL Analytics for Advertising]整合Adobe Analytics和Adobe Advertising以擴充和增強每個產品的功能。

此整合可讓廣告商追蹤其[!DNL Analytics]執行個體中的點進和檢視網站互動，讓品牌瞭解其廣告支出如何帶來網站參與度和關鍵業務目標。

此外，Adobe Advertising可以存取使用網站上已有的[!DNL Analytics]標籤的[!DNL Analytics]所收集的大量第一方資料。 這可讓歷程管理、第一方再行銷和付費媒體網站報告功能更加健全。 Adobe Advertising可進一步使用[!DNL Analytics]資料進行支出和競標最佳化。

若正確使用，[!DNL Analytics for Advertising]會模糊兩個傳統角色之間的界限：廣告歷程管理（透過廣告將使用者送往網站的動作）和透過網站分析瞭解該網站的參與。

主要優點：

* 將[!DNL Analytics]個區段直接傳送給Adobe Advertising，以供第一方網站再行銷之用。
* 使用[!DNL Analytics]個自訂和標準事件作為轉換訊號，以最佳化付費媒體廣告。
* 利用[!DNL Analytics] Analysis Workspace來更瞭解網站進入點和造訪行為。
* 讓網頁分析人員與付費媒體團隊更緊密地共同作業。
* 在[!DNL Analytics]內使用永久Adobe Advertising檢視和點進ID來瞭解網站參與。
* 將資料或畫素匯出至廣告伺服器或其他DSP時，無法透過自訂量度、自訂維度和網站活動來增強Analysis Workspace中的傳統付費媒體報表。
* 利用您網站上的[!DNL Analytics]程式碼在Adobe Advertising中追蹤和最佳化。

>[!TIP]
>
> 觀看[介紹 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics)的影片。

## 使用Analytics製作付費媒體報表

[!DNL Analytics for Advertising]允許您：

* 在[!DNL Analytics]內使用永久Adobe Advertising檢視和點進ID來瞭解網站參與。
* 利用Analysis Workspace深入瞭解網站登入點和造訪行為。 您可以存取付費媒體維度和事件資料，其中包括Adobe Advertising促銷活動實體名稱（包括版位和廣告）及其相關量度，例如點按數、曝光數和成本。

若要使用[!DNL Analytics]作為您的付費媒體報告工具，您的組織需要Experience Cloud登入才能存取Analysis Workspace。 您的Adobe Advertising團隊將協助您將您的Adobe Advertising資料對應至Analysis Workspace中的個別報表套裝。 您可以將Adobe Advertising資料傳送至任何報表套裝，但您應留意已對應至Adobe Advertising的報表套裝與未對應的報表套裝。依報表套裝而定，這可能會變更報告的資料。

 [!DNL Analytics][&#128279;](ids.md)內的個Adobe AdvertisingID與其他[!DNL eVars]一樣運作，具有自訂、持續的有效期。 在Adobe Advertising實施期間，歸因回顧期間預設為60天。 若要變更此設定，請與您的Adobe帳戶團隊合作。

Adobe Advertising維度會附加尾碼「(AMO ID)」(例如「廣告型別(AMO ID)」)。 如需可用維度的清單，請參閱&quot;[Analysis Workspace中的Adobe Advertising量度](advertising-metrics-in-analytics.md)&quot;。

>[!NOTE]
>
> 當您在[!DNL Analytics]內檢視Adobe Advertising資料（或任何資料集）時，請注意，量度和報表是根據[!DNL Analytics]內設定的規則。 資料可能不同於您在其他報告系統中看到的資料，例如廣告伺服器報告、[!DNL DSP]報告或搜尋引擎報告。 若要瞭解[!DNL Analytics]中的資料差異，您必須知道[!DNL eVar]資料何時過期、什麼定義了造訪、什麼被視為上次接觸歸因與總持續歸因，以及其他因素。 如需詳細資訊，請參閱[在 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之間的預期資料差異。

## 使用Analytics支援Adobe Advertising促銷活動和Portfolio

[!DNL Analytics for Advertising]不需要任何額外的畫素，即可傳送兩個主要訊號給Adobe Advertising，讓最佳化更佳，對象分割更容易：

* 要當作競標訊號使用的轉換量度：
   * 標準量度，例如[!UICONTROL Revenue]和[!UICONTROL Cart Views]。
   * 網站參與量度，例如頁面檢視和造訪量度。
   * 自訂收入量度。
   * 保留的收入量度。
* 在[!DNL Analytics]中建立並發佈至Experience Cloud的區段。

  您可以在[!DNL DSP]和付費搜尋廣告中使用[!DNL Analytics]區段進行第一方網站重新目標定位。

  （僅限[!DNL Search, Social, & Commerce]）具有[!DNL Analytics]但不具有Audience Manager的廣告商也可以從與Experience Cloud共用的[!DNL Analytics]區段中，建立Google網站標籤型對象（再行銷清單）和客戶比對對象（客戶清單）。

### 網站轉換量度做為競標訊號

您可以使用來自[!DNL Analytics]的標準事件和自訂事件，在Adobe Advertising中建置加權目標。 目標為您的[!DNL DSP]套件和搜尋、社交和Commerce產品組合的競標決定提供資訊。

對於搜尋、Social和Commerce混合專案組合中的[!DNL Google Ads]和[!DNL Google Microsoft Advertising]行銷活動，您可以選擇將目標（包括目標中的任何[!DNL Analytics]事件）直接上傳到廣告網路，以便作為帳戶層級和行銷活動層級自訂轉換目標的轉換動作使用。

>[!NOTE]
>
> 您無法從[!DNL Analytics]將計算量度對應至Adobe Advertising。

您的Adobe Advertising團隊將協助您識別適用於付費媒體效能的事件，並將其對應至Adobe Advertising，這些事件列於[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions]中。

如需可用量度的清單，請參閱&quot;[Adobe Advertising](analytics-data-in-advertising.md)中的Analytics量度&quot;。

### 網站重新目標定位的Analytics區段

Adobe Advertising可使用[!DNL Analytics]與Experience Cloud之間的原生Experience Cloud受眾整合，擷取[!DNL Analytics]個區段以用於Advertising DSP和[!DNL Search, Social, & Commerce]個廣告的再行銷用途。

若要存取[!DNL Analytics]區段，廣告商帳戶必須啟用[Experience Cloud識別碼服務](https://experienceleague.adobe.com/docs/id-service/using/home.html)。 ID服務啟用後，所有Experience Cloud區段(包括在[!DNL Analytics]中建立並發佈至Experience Cloud的區段、在Adobe Audience Manager中建立的區段、使用[!DNL People core service]在Experience Cloud中建立的區段，以及在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe Advertising)一經處理即可在Adobe Advertising中使用。

[!DNL Analytics]區段可在24小時內提供並每日更新。

如需Experience Cloud對象服務的詳細資訊，請參閱[Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)。

## 如何使用整合的範例 {#integration-examples}

### 在Analysis Workspace中使用Adobe Advertising資料

若要瞭解如何使用Adobe Advertising資料在Analysis Workspace中建立視覺化報表，請參閱影片「[Workspace和報表簡介](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)」。

#### 在報表中使用連線電視檢視轉換

*僅限Advertising DSP使用者*

您可以將CTV裝置上的廣告曝光度連結至站上轉換，藉此衡量連線電視(CTV)促銷活動的完整漏鬥成效。 新的[!UICONTROL Landing Type]篩選器&quot;[!UICONTROL View-through (CTV)]&quot;會針對[!UICONTROL Click Through]、[!UICONTROL View Through]和[!UICONTROL View Through (CTV)]值將轉換分割為個別的列。

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

### 建立Adobe Advertising儀表板

若要瞭解如何根據Analysis Workspace中的目標追蹤您的Adobe Advertising資料，請參閱影片「使用Adobe Analytics建立Adobe Advertising儀表板[&#128279;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)」。

### 使用Adobe AdvertisingID進行網站專案分析

若要瞭解如何建立Adobe Advertising網站專案報告，以監視一週中的某天、一天中的某一時間、瀏覽器和地理影響，請參閱影片「[建立Adobe Advertising網站專案報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)」。

## 如何啟動[!DNL Analytics for Advertising]實作

請聯絡您的Adobe客戶團隊，他們將會完成開始所需的初始設定，並將幫助您根據組織的需求規劃實施與資料使用。

>[!MORELIKETHIS]
>
>* [影片： [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)簡介
>* [實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]](prerequisites.md)
>* Analytics使用的[Adobe AdvertisingID](ids.md)
>* 適用於Advertising的Analytics的[JavaScript程式碼](/help/integrations/analytics/javascript.md)
>* [預期資料差異介於 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之間
>* 在Analysis Workspace中[Adobe Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)
