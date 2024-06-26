---
title: 概觀 [!DNL Analytics for Advertising]
description: 概觀 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: a0a3bb1e74ffc687118d0336a03dcc6164b67226
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# 概觀 [!DNL Analytics for Advertising]

*使用Advertising DSP和的廣告商[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] 整合Adobe Analytics和Adobe Advertising，以擴充和增強每個產品的功能。

此整合可讓廣告商追蹤其網站中的點進和檢視互動 [!DNL Analytics] 例項，讓品牌瞭解其廣告支出如何帶來網站參與度和關鍵業務目標。

此外，Adobe Advertising可存取大量第一方資料，而且 [!DNL Analytics] 收集使用 [!DNL Analytics] 標籤已存在於網站上。 這可讓歷程管理、第一方再行銷和付費媒體網站報告功能更加健全。 Adobe Advertising可進一步使用 [!DNL Analytics] 支出和競標最佳化的資料。

若僱用得當， [!DNL Analytics for Advertising] 模糊兩個傳統角色之間的界限：廣告歷程管理（透過廣告將使用者送往網站的行為）和透過網站分析瞭解網站參與。

主要優點：

* 傳送 [!DNL Analytics] 直接區段至Adobe Advertising，以供第一方網站再行銷。
* 使用 [!DNL Analytics] 自訂和標準事件作為最佳化付費媒體廣告的轉換訊號。
* 充分運用 [!DNL Analytics] Analysis Workspace ，以更加瞭解網站登入點和造訪行為。
* 讓網頁分析人員與付費媒體團隊更緊密地共同作業。
* 在內使用永久Adobe Advertising瀏覽和點進ID [!DNL Analytics] 以瞭解網站參與度。
* 將資料或畫素匯出至廣告伺服器或其他DSP時，無法透過自訂量度、自訂維度和網站活動來增強Analysis Workspace中的傳統付費媒體報表。
* 充分運用 [!DNL Analytics] 程式碼已存在於您的網站上，以在Adobe Advertising中追蹤和最佳化。

>[!TIP]
>
> 觀看 [簡介影片 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## 使用Analytics製作付費媒體報表

[!DNL Analytics for Advertising] 允許您：

* 在內使用永久Adobe Advertising瀏覽和點進ID [!DNL Analytics] 以瞭解網站參與度。
* 利用Analysis Workspace深入瞭解網站登入點和造訪行為。 您可以存取付費媒體維度和事件資料，其中包括Adobe Advertising促銷活動實體名稱（包括版位和廣告）及其相關量度，例如點按數、曝光數和成本。

使用 [!DNL Analytics] 由於您的付費媒體報告工具需要Experience Cloud登入才能存取Analysis Workspace。 您的Adobe Advertising團隊將協助您將您的Adobe Advertising資料對應至Analysis Workspace中的個別報表套裝。 您可以將Adobe Advertising資料傳送至任何報表套裝，但您應留意已對應至Adobe Advertising的報表套裝與未對應的報表套裝。依報表套裝而定，這可能會變更報告的資料。

[內的Adobe AdvertisingID [!DNL Analytics]](ids.md) 像其他一樣工作 [!DNL eVars]，具有自訂、持續的有效期。 在Adobe Advertising實施期間，歸因回顧期間預設為60天。 若要變更此設定，請與您的Adobe帳戶團隊合作。

Adobe Advertising維度會附加尾碼「(AMO ID)」(例如「廣告型別(AMO ID)」)。 請參閱&quot;[Analysis Workspace中的Adobe Advertising量度](advertising-metrics-in-analytics.md)」以取得可用維度的清單。

>[!NOTE]
>
> 當您在中檢視Adobe Advertising資料（或任何資料集）時 [!DNL Analytics]，請注意，量度和報表是根據在中設定的規則 [!DNL Analytics]. 資料可能會與您在其他報表系統中看到的不同，例如廣告伺服器報表、 [!DNL DSP] 報表或搜尋引擎報表。 若要瞭解中的資料差異 [!DNL Analytics]，您必須知道何時 [!DNL eVar] 資料過期、造訪的定義、被視為上次接觸歸因與總持續歸因的專案，以及其他因素。 如需詳細資訊，請參閱 [預期資料差異： [!DNL Analytics] 和Adobe Advertising](data-variances.md).

## 使用Analytics支援Adobe Advertising促銷活動和Portfolio

不需要任何額外的畫素， [!DNL Analytics for Advertising] 透過傳送兩個主要訊號至Adobe Advertising，實現更好的最佳化及更輕鬆的受眾細分：

* 要當作競標訊號使用的轉換量度：
   * 標準量度，例如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views].
   * 網站參與量度，例如頁面檢視和造訪量度。
   * 自訂收入量度。
   * 保留的收入量度。
* 在中建立的區段 [!DNL Analytics] 並發佈至Experience Cloud。

  您可以使用 [!DNL Analytics] 中第一方網站重新目標定位的區段 [!DNL DSP] 和付費搜尋廣告。

  ([!DNL Search, Social, & Commerce] 僅限)廣告商使用 [!DNL Analytics] 但不Audience Manager也可以從建立Google網站標籤型對象（再行銷清單）和客戶比對對象（客戶清單） [!DNL Analytics] 與Experience Cloud共用的區段。

### 網站轉換量度做為競標訊號

您可以從以下位置使用標準事件和自訂事件： [!DNL Analytics] 在Adobe Advertising中建立加權目標。 目標為下列專案的競標決策提供資訊： [!DNL DSP] 套件和搜尋產品組合。

>[!NOTE]
>
> 您無法從對應計算量度 [!DNL Analytics] Adobe Advertising中。

您的Adobe Advertising團隊將協助您識別適用於付費媒體效能的事件，並將其對應至Adobe Advertising，這些事件會列於 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

請參閱&quot;[Adobe Advertising中的Analytics度量](analytics-data-in-advertising.md)」以取得可用量度的清單。

### 網站重新目標定位的Analytics區段

Adobe Advertising可以內嵌 [!DNL Analytics] Advertising DSP和再行銷用途的區段 [!DNL Search, Social, & Commerce] 使用原生Experience Cloud的廣告受眾整合，介於 [!DNL Analytics] 和Experience Cloud。

若要存取 [!DNL Analytics] 區段，廣告商帳戶必須啟用 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html). ID服務啟用時，所有Experience Cloud區段(包括在 [!DNL Analytics] 並發佈至Experience Cloud、在Adobe Audience Manager中建立的區段，以及使用在Experience Cloud中建立的區段 [!DNL People core service]和，在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe Advertising的區段)一經處理即可在Adobe Advertising中使用。

[!DNL Analytics] 區段可在24小時內提供，並每日更新。

如需「Experience Cloud對象」服務的詳細資訊，請參閱 [Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 如何使用整合的範例 {#integration-examples}

### 在Analysis Workspace中使用Adobe Advertising資料

若要瞭解如何使用Adobe Advertising資料在Analysis Workspace中建立視覺報表，請參閱影片」[Workspace和報表的簡介](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).」

#### 在報表中使用連線電視檢視轉換

*僅限Advertising DSP使用者*

您可以將CTV裝置上的廣告曝光度連結至站上轉換，藉此衡量連線電視(CTV)促銷活動的完整漏鬥成效。 新的 [!UICONTROL Landing Type] 篩選器&quot;[!UICONTROL View-through (CTV)]&quot;會將轉換分割為單獨的列， [!UICONTROL Click Through]， [!UICONTROL View Through]、和 [!UICONTROL View Through (CTV)] 值。

若要檢視您的CTV觀看轉換量度，請使用Analysis Workspace中的「位置」檢視或「行銷管道」檢視。

使用「位置」檢視：

1. 在報表檢視中包含CTV花費位置。

1. 包括所需的量度，例如「曝光數」、「點按數」等。

1. 套用下列篩選器：

   廣告平台： `Advertising Cloud DSP`

   登陸頁面： `View-Through (CTV)`

使用行銷管道檢視：

1. 包含維度 `Marketing Channel`.

1. 包括所需的量度，例如「曝光數」、「點按數」等。

1. 套用下列篩選器：

   廣告平台： `Advertising Cloud DSP`

   登陸頁面： `View-Through (CTV)`

### 建立Adobe Advertising儀表板

若要瞭解如何根據Analysis Workspace中的目標追蹤Adobe Advertising資料，請參閱影片」[使用Adobe Analytics建立Adobe Advertising儀表板](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).」

### 使用Adobe AdvertisingID進行網站專案分析

若要瞭解如何建立Adobe Advertising網站專案報表，以監控一週中的某天、一天中的某一時間、瀏覽器和地理影響，請參閱影片」[建立Adobe Advertising網站專案報表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).」

## 如何啟動 [!DNL Analytics for Advertising] 實施

請聯絡您的Adobe客戶團隊，他們將會完成開始所需的初始設定，並將幫助您根據組織的需求規劃實施與資料使用。

>[!MORELIKETHIS]
>
>* [影片：簡介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [實作的必要條件和重要資訊 [!DNL Analytics for Advertising]](prerequisites.md)
>* [Analytics使用的Adobe AdvertisingID](ids.md)
>* [Analytics for Advertising的JavaScript程式碼](/help/integrations/analytics/javascript.md)
>* [預期資料差異： [!DNL Analytics] 和Adobe Advertising](data-variances.md)
>* [Analysis Workspace中的Adobe Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)
