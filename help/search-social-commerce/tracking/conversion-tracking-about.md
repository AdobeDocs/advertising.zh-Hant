---
title: 搜尋、社交和Commerce的轉換追蹤選項
description: 瞭解搜尋、社交和Commerce的轉換追蹤選項。
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# 搜尋、社交和Commerce的轉換追蹤選項

搜尋、社交和Commerce可使用轉換資料，並透過下列方式進行追蹤：

* **Adobe Advertising追蹤的轉換：**&#x200B;廣告商會在每個轉換頁面上插入Adobe Advertising轉換追蹤標籤。 標籤會將轉換資料傳送至追蹤伺服器。 您可以使用舊版協力廠商畫素或更新的第一方畫素。 請參閱&quot;[每個轉換追蹤方法](#conversion-tracking-comparison)的比較。&quot;

* **Adobe Analytics轉換：**&#x200B;廣告商對所有轉換都使用Adobe Analytics追蹤。 此選項需要Adobe Advertising-Adobe Analytics整合。 如需詳細資訊，請參閱&quot;[Adobe Analytics轉換追蹤](conversion-tracking-analytics.md)&quot;。

* **[!DNL Google Analytics]轉換：**&#x200B;廣告商使用[!DNL Google Analytics]標籤來追蹤所有轉換。 如需自動同步之轉換的詳細資訊，請參閱「搜尋、社交和Commerce中的[[!DNL Google Ads] 轉換資料](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」。

* **追蹤廣告商的轉換：** (僅限Search、Social和Commerce使用者端)廣告商提供Search、Social和Commerce摘要檔案，其中包含任何線上和離線轉換資料的組合。 請參閱[使用EF ID摘要](feed-efid.md)的轉換追蹤[使用交易ID摘要](feed-transaction-id.md)的轉換追蹤。

## 每種轉換追蹤方法的比較 {#conversion-tracking-comparison}

隨著瀏覽器Cookie政策日益嚴格，瞭解您目前的追蹤功能，並找出您的最佳長期選項變得十分重要。

| 追蹤方法 | 說明 | 限制 | 優點 | 建議使用？ |
|----|----|----|----|----|
| Adobe Analytics | 使用Advertising適用的[Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的廣告商會自動匯入其[!DNL Analytics]個標準和自訂事件以Adobe Advertising報告和最佳化。 | <ul><li>[!DNL Safari]只允許七天的轉換回顧，這會在回顧期間重複造訪網站時重設。</li><li> 預期2024年[!DNL Chrome]會有類似的限制。</li></ul> | <ul><li>與[!DNL Analytics]緊密整合</li> <li>檢視[!DNL Analytics] Analysis Workspace中的付費搜尋資料</li><li>付費搜尋以外的好處</li></ul> | 是 |
| 舊版Adobe Advertising畫素 | 廣告商會將舊版Adobe Advertising影像或JavaScript畫素新增至其轉換頁面。 當使用者點按廣告到達頁面時，就會觸發畫素。 此方法需仰賴第三方Cookie。 | <ul><li>[!DNL Safari]封鎖使用此方法的所有轉換追蹤。</li><li>預期2024年[!DNL Chrome]會有類似的限制。</li></ul> | 已實作畫素。 不過，您仍必須[實作額外的ITP對應標籤](itp-conversion-mapping-tag.md)。<br><br>建議：切換至第一方畫素。 | 否 |
| Adobe Advertising第一方畫素 | 廣告商執行下列動作： <ul><li>在整個網站上實作[Adobe Experience Cloud ID (ECID)服務](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html)的JavaScript資料庫。</li><li>將具有ITP對應之Adobe Advertising[JavaScript標籤](itp-conversion-mapping-tag.md)新增至搜尋點按後可能為登陸頁面的任何頁面（理想情況下，在所有頁面上，因為登陸頁面可能會隨著時間而變更）。 標籤可讓Adobe Advertising追蹤將大量數字轉換為登入頁面科學記號的頁面上發生的轉換事件。</li><li>將Adobe Advertising[JavaScript轉換追蹤標籤v3](format-conversion-tag-jsv3.md)新增至轉換頁面。</li></ul> | <ul><li>[!DNL Safari]只允許七天的轉換回顧，這會在回顧期間重複造訪網站時重設。</li><li>預期2022年[!DNL Chrome]會有類似的限制。</li></ul> | [!DNL Safari]會在七天回顧期間追蹤轉換。 由於回顧期間在重複網站造訪時重設回顧，因此該限制不會影響所有[!DNL Safari]使用者。 | 否 |
| EFID摘要 | 廣告商的搜尋帳戶已設定為產生Adobe Advertising唯一ID （權杖）的目的地URL/最終URL。 當使用者按一下廣告時，Adobe Advertising會建立唯一識別碼(`EFID`)，並在最終URL的結尾顯示。 廣告商的使用者端系統擷取EFID作為點按所產生轉換的唯一識別碼，並傳送給收入摘要中的Adobe Advertising，其中包括EFID、交易日期和轉換量度。 Adobe Advertising接著會使用EFID來比對轉換與原始點按。 | <ul><li>廣告商必須有能力擷取EFID，並每天傳送自動化摘要給Adobe Advertising。</li><li>最多可追蹤180天的轉換(每個Adobe Advertising)或根據廣告商系統的限制。</li></ul> | <ul><li>此方法使用第一方轉換資料，因此不受第三方Cookie限制影響。</li><li>線上和離線轉換可在一個摘要中傳送。</li><li>網站不需要變更程式碼或標籤。</li></ul> | 是 |
| 交易ID摘要[組合摘要] | 廣告商會將包含唯一交易ID (`ev_transid=&lt;transid&gt;`)引數的Adobe Advertising畫素新增至其網頁，而Adobe Advertising會擷取畫素引發時建立的唯一交易ID。 廣告商的使用者端系統也會擷取[!UICONTROL Transaction ID]，並傳送Adobe Advertising具有相符[!UICONTROL Transaction ID]值的離線轉換收入摘要 | <ul><li>如果廣告商正在使用舊版畫素（會阻隔引發[!DNL Safari]個畫素），則不會擷取該ID以用於離線資料。</li><li>摘要未自動化。</li></ul> | <ul><li>如果您實作第一方畫素，則會在[!DNL Safari]中擷取[!UICONTROL Transaction ID]。</li><li>提供離線/已核准轉換事件的追蹤功能。</li></ul> | 否 |
| [!DNL Google]個轉換 | 透過API連線將使用[!DNL Google Analytics]標籤追蹤的轉換自動匯入至Adobe Advertising。 每個轉換名稱都有`&quot;GGL_&quot;`首碼。 | <ul><li>[!DNL Google]通常不會追蹤離線資料。</li><li>未包含[!DNL Microsoft Advertising]個轉換。</li></ul> | [!DNL Google]使用機器學習來外推&quot;[模型化轉換](https://support.google.com/google-ads/answer/10081327)&quot;。 | 否 |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics轉換追蹤](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [使用EF ID摘要的轉換追蹤](/help/search-social-commerce/tracking/feed-efid.md)
>* [使用交易ID摘要的轉換追蹤](/help/search-social-commerce/tracking/feed-transaction-id.md)
