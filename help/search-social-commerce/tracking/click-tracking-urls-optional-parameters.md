---
title: 點選追蹤URL的選用追蹤引數
description: 瞭解選用的搜尋、社交和Commerce追蹤引數，以及可新增至點選追蹤URL的廣告網路特定追蹤引數。
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: f633f2af545f034b08b378653b4b967710402a03
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# 點選追蹤URL的選用追蹤引數

僅&#x200B;*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan]和[!DNL Yandex]帳戶*

您可以新增更多引數來追蹤廣告網路帳戶的特定資料，而不是只使用最終URL或目的地URL的標準追蹤引數。 您可以在帳戶設定或行銷活動設定中新增以下引數的任意組合：

* 您可以將任何靜態文字字串附加為帳戶/促銷活動基礎URL中的引數。

* 您可以在帳戶/促銷活動的基礎URL中附加Adobe Advertising和廣告網路特定引數，以追蹤更多資料：

   * Adobe Advertising引數是半靜態的。 Adobe Advertising將基礎URL上傳至廣告網路時，會插入資料值。 例如，當您將`campaign={ef_campaign}`附加至基底URL時，Adobe Advertising在上傳URL時會將`{ef_campaign}`取代為實際的促銷活動名稱（例如「回到學校促銷活動」）。

     **注意：**&#x200B;一旦插入值，就會維持靜態。 如果您將關鍵字或廣告移至其他廣告群組，或將廣告群組移至其他促銷活動，則{ef_adgroup}或{ef_campaign}引數不會自動更新，因此您必須手動產生新的目的地URL或基本（最終） URL。

   * 廣告網路專屬引數為動態引數，且搜尋引擎會在使用者點按廣告時插入資料值。 例如，當您將`{param1}`附加至基底URL時，一般使用者按一下廣告時，廣告網路會以實際{param1}值取代。

>[!NOTE]
>
>* 請使用逗號或&amp;符號(`&`)分隔多個引數。
>* 下列引數不區分大小寫。
>* 在產生的目的地URL或基礎（最終） URL中，附加引數中的特殊字元會以下列方式取代：
>  * `=`已由`%3D`取代
>  * `?`已由`%26`取代
>  * 空白空間已由`%2B`取代
>  例如，當您將引數`campaign={ef_campaign}`附加至關鍵字的基本URL http://www.example.com時，該關鍵字的基本URL會產生為`http://www.example.com/campaign%3D{ef_campaign}`。

## 搜尋、社交和Commerce靜態追蹤引數

您可以對任何廣告網路上的帳戶使用下列引數，並視需要將其與特定廣告網路的引數結合。 當帳戶的追蹤方法為&quot;[!UICONTROL EF Direct]&quot;時，有些引數會復製為特定廣告網路自動新增的引數。

下列所有引數都必須指定為機碼 — 值組；您可以為一個值組包含多個引數。 例如，若要插入行銷活動名稱，請使用`<your_parameter_name>={ef_campaign}`，例如`campaign={ef_campaign}`。 若要使用指定的比對型別名稱插入比對型別，請使用`<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`，例如`matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`。 不適用的相符型別不會出現在產生的URL中。

| 引數 | 說明 |
| ---- | ---- |
| <code>{custom_code}</code> | 若要將上傳大量表單檔案中「自訂URL引數」欄的資料插入追蹤URL。 {custom_code}只能在追蹤URL中一或多個機碼值組的值結尾使用。 範例： <code>a={custom_code}</code>； <code>a={ef_campaignid}{custom_code}</code>； <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>注意：</b>若要將自訂值從Bulksheet檔案插入追蹤URL，請使用[產生追蹤URL]選項上傳Bulksheet檔案。 如需關於使用Bulksheet檔案的詳細資訊，請參閱[關於使用Bulksheets管理促銷活動資料](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。 |
| <code>{ef_uniqueid}</code> | 插入由Adobe Advertising建立的唯一ID。 當追蹤方法為「EF重新導向」時自動新增。 |
| <code>{ef_userid}</code> | 插入Adobe Advertising指派給廣告商的不重複使用者ID。 |
| <code>{ef_sid}</code> | 若要插入Search、Social和Commerce指派給廣告網路的數值ID： [!DNL Google Ads]的<i>[!UICONTROL 3]</i>、[!DNL Microsoft Advertising]的<i>[!UICONTROL 10]</i>、[!DNL Meta]的<i>[!UICONTROL 45]</i>、[!DNL Yahoo! Display Network]的<i>[!UICONTROL 86]</i>、[!DNL Naver]的<i>[!UICONTROL 87]</i>、[!DNL Baidu]的<i>[!UICONTROL 88]</i>、[!DNL Yandex]的<i>[!UICONTROL 90]</i>、[!DNL Yahoo! Japan Ads]的<i>[!UICONTROL 94]</i>、[!DNL Yahoo Native]的<i>[!UICONTROL 105]</i> （已棄用）或[!DNL Pinterest]的<i>[!UICONTROL 106]</i> （已棄用）。 |
| <code>{ef_searchengine}</code> | 插入廣告網路名稱。 |
| <code>{ef_campaign}</code> | 插入行銷活動名稱。 |
| <code>{ef_campaignid}</code> | 插入促銷活動ID。 <b>注意：</b>新行銷活動的ID必須等到行銷活動發佈至廣告網路後才會建立。 如果帳戶使用&quot;[!UICONTROL EF Redirect]&quot;和&quot;AutoUpload&quot;選項，則Adobe Advertising會在隔天自動將促銷活動ID插入相關的目的地URL或最終URL。 如果帳戶未使用&quot;[!UICONTROL EF Redirect]&quot;和[!UICONTROL Auto Upload]&quot;選項，而您想要在相關目的地URL或最終URL中插入行銷活動ID，您必須建立行銷活動；使用「產生追蹤URL」選項下載新行銷活動的Bulksheet檔案，然後將檔案張貼至廣告網路。 |
| <code>{ef_adgroup}</code> | 插入廣告群組名稱。 |
| <code>{ef_adgroupid}</code> | 插入廣告群組ID。 <b>注意：</b>新廣告群組的ID要等到廣告群組發佈至廣告網路後才會建立。 如果帳戶使用&quot;[!UICONTROL EF Redirect]&quot;和&quot;AutoUpload&quot;選項，Adobe Advertising會在隔天自動將廣告群組ID插入相關的目的地URL或最終URL。 如果帳戶未使用[!UICONTROL EF Redirect]和[!UICONTROL Auto Upload]選項，而您想要在相關的目的地URL或最終URL中插入廣告群組ID，則必須建立廣告群組；使用「產生追蹤URL」選項下載新廣告群組的大量表單檔案；然後將檔案張貼至廣告網路。 |
| <code>{ef_keyword}</code> | 插入關鍵字。 |
| <code>{ef_keywordid}</code> | 插入關鍵字ID。 <b>注意：</b>新關鍵字的ID要等到關鍵字張貼到廣告網路後才會建立。 如果帳戶使用&quot;[!UICONTROL EF Redirect]&quot;和[!UICONTROL Auto Upload]&quot;選項，則Adobe Advertising會在隔天自動將關鍵字ID插入相關的目的地URL或最終URL中。 如果帳戶未使用&quot;[!UICONTROL EF Redirect]&quot;和[!UICONTROL Auto Upload]&quot;選項，而您想要在相關目的地URL或最終URL中插入關鍵字ID，則必須建立關鍵字；使用「產生追蹤URL」選項下載新關鍵字的大量表單檔案，然後將檔案張貼至廣告網路。 |
| <code>{ef_matchtype}</code> | 將關鍵字比對型別插入為「廣泛」、「精確」或「片語」。 已使用&quot;[!UICONTROL EF Redirect]&quot;追蹤方法自動納入[!DNL Google Ads]和[!DNL Microsoft Advertising]。 |
| <code>{ef_adid}</code> | 插入廣告ID。 <b>注意：</b>新廣告的識別碼要等到廣告發佈到廣告網路後才會建立。 如果帳戶使用&quot;[!UICONTROL EF Redirect]&quot;和[!UICONTROL Auto Upload]&quot;選項，則Adobe Advertising會在隔天自動將廣告ID插入相關的目的地URL或最終URL。 如果帳戶未使用&quot;[!UICONTROL EF Redirect]&quot;和[!UICONTROL Auto Upload]&quot;選項，而您想要在相關目的地URL或最終URL中插入廣告ID，則必須建立廣告；使用「產生追蹤URL」選項下載新廣告的Bulksheet檔案；然後將檔案張貼至廣告網路。 |

## [!DNL Google Ads]個動態追蹤引數

請參閱[https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447)。

## [!DNL Microsoft Advertising]個動態追蹤引數

請參閱[https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2)。

## Yahoo！ 日本廣告動態追蹤引數

請參閱[https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US)。

## [!DNL Yandex]個動態追蹤引數

請參閱[https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html)。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤服務的點選追蹤URL格式](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
