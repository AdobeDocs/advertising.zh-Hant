---
title: 搜尋、社交和商務的轉換追蹤選項
description: 瞭解搜尋、社交和商務的轉換追蹤選項。
exl-id: 098efaf8-6ffb-4811-8b20-41c7c85df812
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# 搜尋、社交和商務的轉換追蹤選項

搜尋、Social和Commerce可以使用轉換資料，並透過以下方式追蹤：

* **Adobe Advertising追蹤的轉換：** 廣告商會在每個轉換頁面上插入Adobe Advertising轉換追蹤標籤。 標籤會將轉換資料傳送至追蹤伺服器。 您可以使用舊版協力廠商畫素或更新的第一方畫素。 請參閱&quot;[每種轉換追蹤方法的比較](#conversion-tracking-comparison).」

* **Adobe Analytics轉換：** 廣告商針對所有轉換使用Adobe Analytics追蹤功能。 此選項需要Adobe Advertising-Adobe Analytics整合。 請參閱&quot;[Adobe Analytics轉換追蹤](conversion-tracking-analytics.md)」以取得詳細資訊。

* **[!DNL Google Analytics]轉換：** 廣告商使用 [!DNL Google Analytics] 標籤以追蹤所有轉換。 請參閱&quot;[[!DNL Google Ads] 搜尋、社交和商務中的轉換資料](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」以取得自動同步之轉換的詳細資訊。

* **廣告商追蹤的轉換：** （僅限搜尋、社交和商務客戶）廣告商提供搜尋、社交和商務摘要檔案，內含線上和離線轉換資料的任意組合。 請參閱&quot;[使用EF ID摘要的轉換追蹤](feed-efid.md)「和」[使用交易ID摘要的轉換追蹤](feed-transaction-id.md).」

## 每種轉換追蹤方法的比較 {#conversion-tracking-comparison}

隨著瀏覽器Cookie政策日益嚴格，瞭解您目前的追蹤功能，並找出您的最佳長期選項變得十分重要。

| 追蹤方法 | 說明 | 限制 | 優點 | 建議使用？ |
|----|----|----|----|----|
| Adobe Analytics | 廣告商使用 [適用於廣告的Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) 自動匯入其 [!DNL Analytics] 標準和自訂事件，以Adobe Advertising報表和最佳化。 | <ul><li>[!DNL Safari] 只允許七天的轉換回顧，這會在回顧期間重複網站造訪時重設。</li><li> 預期有類似的限制 [!DNL Chrome] （2024年）。</li></ul> | <ul><li>與緊密整合 [!DNL Analytics]</li> <li>請參閱中的付費搜尋資料 [!DNL Analytics] Analysis Workspace</li><li>付費搜尋以外的好處</li></ul> | 是 |
| 舊版Adobe Advertising畫素 | 廣告商會將舊版Adobe Advertising影像或JavaScript畫素新增至其轉換頁面。 當使用者點按廣告到達頁面時，就會觸發畫素。 此方法需仰賴第三方Cookie。 | <ul><li>[!DNL Safari] 會封鎖使用此方法的所有轉換追蹤。</li><li>預期有類似的限制 [!DNL Chrome] （2024年）。</li></ul> | 已實作畫素。 不過，您仍必須 [實作其他ITP對應標籤](itp-conversion-mapping-tag.md).<br><br>建議：切換至第一方畫素。 | 否 |
| Adobe Advertising第一方畫素 | 廣告商執行下列動作： <ul><li>為實作JavaScript資料庫 [Adobe Experience Cloud ID (ECID)服務](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 橫跨整個網站。</li><li>新增Adobe Advertising [具有ITP對應的JavaScript標籤](itp-conversion-mapping-tag.md) 搜尋點選後移至登陸頁面的任何頁面（理想情況下，在所有頁面上，因為登陸頁面可能會隨著時間變更）。 標籤可讓Adobe Advertising追蹤將大量數字轉換為登入頁面科學記號的頁面上發生的轉換事件。</li><li>新增Adobe Advertising [JavaScript轉換追蹤標籤v3](format-conversion-tag-jsv3.md) 至轉換頁面。</li></ul> | <ul><li>[!DNL Safari] 只允許七天的轉換回顧，這會在回顧期間重複網站造訪時重設。</li><li>預期有類似的限制 [!DNL Chrome] （2022年）。</li></ul> | [!DNL Safari] 在七天回顧期間追蹤轉換。 由於回顧期間會在重複網站造訪時重設，因此該限制不會影響所有 [!DNL Safari] 使用者。 | 否 |
| EFID摘要 | 廣告商的搜尋帳戶已設定為產生Adobe Advertising唯一ID （權杖）的目的地URL/最終URL。 當使用者按一下廣告時，Adobe Advertising會建立唯一ID (`EFID`)，並在最終URL的結尾顯示。 廣告商的使用者端系統會擷取EFID，作為點按所產生轉換的唯一識別碼，並傳送給Adobe Advertising的收入摘要，包含EFID、交易日期和轉換屬性。 Adobe Advertising接著會使用EFID來比對轉換與原始點按。 | <ul><li>廣告商必須有能力擷取EFID，並每天傳送自動化摘要給Adobe Advertising。</li><li>最多可追蹤180天的轉換(每個Adobe Advertising)或根據廣告商系統的限制。</li></ul> | <ul><li>此方法使用第一方轉換資料，因此不受第三方Cookie限制影響。</li><li>線上和離線轉換可在一個摘要中傳送。</li><li>網站不需要變更程式碼或標籤。</li></ul> | 是 |
| 交易識別碼摘要 [組合摘要] | 廣告商新增包含唯一交易ID引數的Adobe Advertising畫素(`ev_transid=&lt;transid&gt;`)，而Adobe Advertising會擷取畫素引發時建立的不重複交易ID。 廣告商的使用者端系統也會擷取 [!UICONTROL Transaction ID] 和會傳送Adobe Advertising收入資訊源給具有相符條件的離線轉換 [!UICONTROL Transaction ID] 值 | <ul><li>如果廣告商正在使用舊版畫素，而 [!DNL Safari] 封鎖觸發，則不會擷取ID以用於離線資料。</li><li>摘要未自動化。</li></ul> | <ul><li>如果您實作第一方畫素，則 [!UICONTROL Transaction ID] 在中擷取 [!DNL Safari].</li><li>提供離線/已核准轉換事件的追蹤功能。</li></ul> | 否 |
| Google轉換 | 使用追蹤的轉換 [!DNL Google Analytics] 標籤會透過API連線自動匯入至Adobe Advertising。 每個轉換名稱都有 `&quot;GGL_&quot;` 前置詞。 | <ul><li>Google通常不會追蹤離線資料。</li><li>不包括Microsoft® Advertising轉換。</li></ul> | Google使用機器學習來外推&quot;[模型化轉換](https://support.google.com/google-ads/answer/10081327).」 | 否 |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics轉換追蹤](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [使用EF ID摘要的轉換追蹤](/help/search-social-commerce/tracking/feed-efid.md)
>* [使用交易ID摘要的轉換追蹤](/help/search-social-commerce/tracking/feed-transaction-id.md)
