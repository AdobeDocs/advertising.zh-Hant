---
title: 點選追蹤URL的選用追蹤引數
description: 瞭解可選的搜尋、社交和商務追蹤引數，以及可新增至點選追蹤URL的廣告網路特定追蹤引數。
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 0%

---

# 點選追蹤URL的選用追蹤引數

*Google Ads、Microsoft Advertising和Yahoo！ 僅限日本帳戶*

您可以新增更多引數來追蹤廣告網路帳戶的特定資料，而不必只使用最終URL或目的地URL的標準追蹤引數。 您可以在帳戶設定或行銷活動設定中新增以下引數的任意組合：

* 您可以將任何靜態文字字串附加為帳戶/促銷活動之基礎URL中的引數。

* 您可以在帳戶/促銷活動的基本URL中附加Adobe廣告和廣告網路特定的引數，以追蹤更多資料：

   * Adobe廣告引數是半靜態的。 Adobe廣告在上傳基本URL至廣告網路時插入資料值。 例如，當您附加 `campaign={ef_campaign}` 至基本URL，Adobe廣告會取代 `{ef_campaign}` 實際促銷活動名稱（例如「返回學校促銷活動」）。

     **注意：** 插入值後，值會維持靜態。 如果您將關鍵字或廣告移至其他廣告群組，或將廣告群組移至其他促銷活動，則  {ef_adgroup} 或 {ef_campaign} 引數不會自動更新，因此您必須手動產生新的目的地URL或基本（最終） URL。

   * 廣告網路特定的引數為動態引數，而搜尋引擎會在使用者點按廣告時插入資料值。 例如，當您附加 `{param1}` 至基本URL，廣告網路會將其取代為實際 {param1} 值。

>[!NOTE]
>
>* 請使用逗號或&amp;符號分隔多個引數(`&`)。
>* 下列引數不區分大小寫。
>* 附加引數中的特殊字元會在產生的目的地URL或基礎（最終） URL中取代如下：
>  * `=` 替換為 `%3D`
>  * `?` 替換為 `%26`
>  * 空白空間將替換為 `%2B`
>  例如，當您附加引數時 `campaign={ef_campaign}` 至關鍵字的基礎URL http://www.example.com ，則該關鍵字的基礎URL產生為 `http://www.example.com/campaign%3D{ef_campaign}`.

## 搜尋、社交和商務靜態追蹤引數

您可以對任何廣告網路上的帳戶使用下列引數，並視需要將其與特定廣告網路的引數結合。 當帳戶的追蹤方法為「」時，其中一些引數會復製為特定廣告網路自動新增的引數[!UICONTROL EF Direct].」

下列所有引數都必須指定為機碼 — 值組；您可以為一個值組包含多個引數。 例如，若要插入行銷活動名稱，請使用 `<your_parameter_name>={ef_campaign}`，例如 `campaign={ef_campaign}`. 若要使用指定的相符型別名稱插入相符型別，請使用 `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`，例如 `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. 不適用的相符型別不會出現在產生的URL中。

| 引數 | 說明 |
| ---- | ---- |
| <code>{custom_code}</code> | 若要將上傳大量表單檔案中「自訂URL引數」欄的資料插入追蹤URL。 {custom_code} 只能在追蹤URL中一或多個索引鍵值組的值結尾使用。 範例：  <code>a={custom_code}</code>； <code>a={ef_campaignid}{custom_code}</code>； <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>注意：</b> 若要將Bulksheet檔案中的自訂值插入追蹤URL，請使用「產生追蹤URL」選項上傳Bulksheet檔案。 如需有關使用Bulksheet檔案的詳細資訊，請參閱「[關於使用大量表單管理行銷活動資料](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).」 |
| <code>{ef_uniqueid}</code> | 插入Adobe廣告建立的唯一ID。 當追蹤方法為「EF重新導向」時自動新增。 |
| <code>{ef_userid}</code> | 插入Adobe廣告指派給廣告商的不重複使用者ID。 |
| <code>{ef_sid}</code> | 若要插入Search、Social和Commerce指派給廣告網路的數值ID： <i>[!UICONTROL 3]</i> 的 [!DNL Google Ads]， <i>[!UICONTROL 10]</i> 的 [!DNL Microsoft® Advertising]， <i>[!UICONTROL 45]</i> 的 [!DNL Meta]， <i>[!UICONTROL 86]</i> 的 [!DNL Yahoo! Display Network]， <i>[!UICONTROL 87]</i> 的 [!DNL Naver]， <i>[!UICONTROL 88]</i> 的 [!DNL Baidu]， <i>[!UICONTROL 90]</i> 的 [!DNL Yandex]， <i>[!UICONTROL 94]</i> 的 [!DNL Yahoo! Japan Ads]， <i>[!UICONTROL 105]</i> 的 [!DNL Yahoo Native] （已棄用），或 <i>[!UICONTROL 106]</i> 的 [!DNL Pinterest] （已棄用）。 |
| <code>{ef_searchengine}</code> | 插入廣告網路名稱。 |
| <code>{ef_campaign}</code> | 插入行銷活動名稱。 |
| <code>{ef_campaignid}</code> | 插入行銷活動ID。 <b>注意：</b> 新行銷活動的ID要等到行銷活動發佈到廣告網路後才會建立。 如果帳戶使用「EF重新導向」和「自動上傳」選項，則Adobe廣告會在隔天自動將促銷活動ID插入相關目的地URL或最終URL。 如果帳戶未使用「EF重新導向」和「自動上傳」選項，且您想在相關目的地URL或最終URL中插入行銷活動ID，則必須建立行銷活動；使用「產生追蹤URL」選項下載新行銷活動的Bulksheet檔案；然後將檔案張貼至廣告網路。 |
| <code>{ef_adgroup}</code> | 插入廣告群組名稱。 |
| <code>{ef_adgroupid}</code> | 插入廣告群組ID。 <b>注意：</b> 新廣告群組的ID要等到廣告群組發佈至廣告網路後才會建立。 如果帳戶使用「EF重新導向」和「自動上傳」選項，則Adobe廣告會在隔天自動將廣告群組ID插入相關的目的地URL或最終URL。 如果帳戶未使用「EF重新導向」和「自動上傳」選項，且您想在相關目的地URL或最終URL中插入廣告群組ID，則必須建立廣告群組；使用「產生追蹤URL」選項下載新廣告群組的Bulksheet檔案；然後將檔案發佈至廣告網路。 |
| <code>{ef_keyword}</code> | 插入關鍵字。 |
| <code>{ef_keywordid}</code> | 插入關鍵字ID。 <b>注意：</b> 只有在關鍵字發佈至廣告網路後，才會建立新關鍵字的ID。 如果帳戶使用「EF重新導向」和「自動上傳」選項，則Adobe廣告會在隔天自動將關鍵字ID插入相關目的地URL或最終URL。 如果帳戶未使用「EF重新導向」和「自動上傳」選項，且您想要將關鍵字ID插入相關目的地URL或最終URL中，則必須建立關鍵字；使用「產生追蹤URL」選項下載新關鍵字的Bulksheet檔案；然後將檔案張貼至廣告網路。 |
| <code>{ef_matchtype}</code> | 將關鍵字比對型別插入為「廣泛」、「精確」或「片語」。 已透過「EF重新導向」追蹤方法自動納入Google Ads和Microsoft Advertising。 |
| <code>{ef_adid}</code> | 插入廣告ID。 <b>注意：</b> 新廣告ID要等到廣告發佈到廣告網路後才會建立。 如果帳戶使用「EF重新導向」和「自動上傳」選項，則Adobe廣告會在隔天自動將廣告ID插入相關目的地URL或最終URL。 如果帳戶未使用「EF重新導向」和「自動上傳」選項，且您想在相關目的地URL或最終URL中插入廣告ID，則必須建立廣告；使用「產生追蹤URL」選項下載新廣告的Bulksheet檔案；然後將檔案張貼至廣告網路。 |

## Google Ads動態追蹤引數

另請參閱 [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Microsoft Advertising動態追蹤引數

另請參閱 [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo Native動態追蹤引數

另請參閱 [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## Yahoo！ Japan Ad動態追蹤引數

另請參閱 [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## Yandex動態追蹤引數

另請參閱 [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [關於Adobe廣告轉換追蹤服務的點選追蹤URL格式](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
