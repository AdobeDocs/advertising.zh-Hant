---
title: 關於自訂報表的常見問題集
description: 瞭解效能報告的常見問題解答，包括疑難排解資料問題。
exl-id: 85707666-7c0f-4aa3-8c91-fb73ef6a5061
source-git-commit: 18d7ec2254dda9e5f94270e13476a521006ec686
workflow-type: tm+mt
source-wordcount: '3919'
ht-degree: 0%

---

# 關於自訂報表的常見問題集

## 一般問題

+++如果報表的日期範圍在報表資料可用之前開始，該怎麼辦？
報表隨即產生，但僅包含可用資料的日期資料。 如需每個報表型別何時可使用資料的相關資訊，請參閱&quot;[用於報表的資料](data-used-for-reports.md).」
+++

+++點按日期和交易日期型報表之間有何差異？
當您依交易日期報告轉換時，資料會包含交易日期在指定時段內發生的交易。 此選項是基本報表和進階報表中的預設設定，它會顯示指定時段內賺取的收入。

當您依點按日期報告轉換時，資料包含在指定時段內發生的點按所產生的交易。 當投資組合在點按和交易之間有重大延遲時，此型別的報告會顯示投資組合的每次點按歷史收入，這讓您可以瞭解一段時間內期望的收入行為。

![按點按日期報告與按交易日期報告](/help/search-social-commerce/assets/click-date-vs-txn-date.png "按點按日期報告與按交易日期報告")
+++

+++如果我變更點選回顧期間或曝光回顧期間，會發生什麼事？
（僅限具有廣告畫素式轉換追蹤服務的廣告商）系統會收集較長時間或較短期間內，由初始點選所產生之事件的資料。

廣告商的 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j) 決定付費點按或顯示曝光發生後，事件可歸因於轉換的天數（分別）。 將值變更為較長或較短的期間，對於點按至收入或顯示曝光至收入期間的廣告商可能很重要。

**最佳實務：** 請確定回顧期間長於大多數關鍵字或廣告的點按收入時間和顯示曝光收入時間。 較短時，某些轉換不會與初始點按或曝光建立關聯。
+++

+++我如何知道哪些轉換來自 [!DNL Google Ads] 廣告擴充功能或產品清單？
您可以檢視哪些轉換是由於點按「 」而產生 [!DNL Google Ads] 廣告擴充功能（而非廣告本身）或產品清單(透過產生 [!UICONTROL Transaction Report]. 此 [!UICONTROL Link Type] 欄值顯示所點按連結的型別和標題：

* 產品清單會列為 `pla:<product ID>`，例如 `pla:8525822`.

* 網站連結的清單為 `sl:<Sitelink text>`，例如 `sl:See Current Offers`.

  如果您包含網站連結，也可以識別網站連結。 [!UICONTROL Tracking URL] 欄中找出。 此 [!UICONTROL Tracking URL] （對於sitelink）包含屬性 `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>轉換來源 [!DNL Google Ads] 位置和電話分機會包含在其隨附廣告的資料中。 這些錯誤不會單獨報告。

+++

+++此&quot;[!UICONTROL Keyword]「我的報告中的」欄包含一個值「（廣告群組內容）&lt;*廣告群組名稱*>.」
當列包含啟用內容的搜尋行銷活動、顯示行銷活動或社交行銷活動（不包含關鍵字）的資料時， [!UICONTROL Keyword] 欄則顯示適用的廣告群組名稱。
+++

+++由於季節性或市場變化，我的報表會顯示非典型資料。 一旦條件變更，這是否會影響競標？
最佳化功能會每天為每個競標單位建立收入模型，以確保它能識別並立即回應趨勢，而且模型會整合長期歷史資料，以協助預測季節性績效。 產品組合的收入模式半衰期設定<!-- add link to glossary? --> 也會決定近期收入資料的加權程度。 最佳實務是在非典型績效期間降低半衰期，但在調整收入模型後增加半衰期。 如果您有任何關於是否需要調整半衰期的問題，請聯絡您的Adobe客戶團隊。

如果您不希望該期間的資料影響未來的出價，則可以選擇從模型中排除這些日期。 請聯絡您的Adobe客戶團隊以排除日期。
+++

+++我可以建立特定屬性量度的報表嗎？例如 [!UICONTROL Device] 或 [!UICONTROL Objective Name]？
針對行銷活動實體報表([!UICONTROL Campaign Report]， [!UICONTROL Ad Group Report]， [!UICONTROL Ad Variation Report]， [!UICONTROL Keyword Report]、和 [!UICONTROL Product Group Report])，量度資料會依您包含在報表中的屬性欄動態彙總。 您可以選擇移除報表的索引鍵欄，並只包含您要彙總資料的屬性欄。

例如，如果您產生 [!UICONTROL Keyword Report] 這包括 [!UICONTROL Ad Group] 和  裝置欄，然後，依預設，報告會依廣告群組和裝置型別彙總每個關鍵字的量度。 不過，如果您移除 [!UICONTROL Keyword] 欄，報表會依裝置型別動態產生指定廣告群組的量度。

>[!NOTE]
>
>您無法使用此功能依標籤分類彙總資料。 報表中的任何標籤分類欄都會被忽略。 請改用 [標籤分類報告](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## 一般資料問題

+++使用不同歸因規則產生的報表會顯示不同的總計。
如果您使用相同的報表引數但使用不同的歸因規則來多次產生報表，則資料可能會因為以下任一原因而有所不同：

* 點按基於日期的資料可能落在指定的日期範圍之外。

  如果您使用報表引數»[!UICONTROL Conversions based on click date]，」則指定的日期範圍會套用至點按的日期，而不是交易的日期。 如果報表也使用歸因規則「第一個事件」或「最後一個事件」，則導致轉換的第一個或最後一個事件可能不在指定的日期範圍內。 例如，假設使用者在4月30日按一下Keyword_1，在5月20日按一下Keyword_2，然後在5月21日轉換。 如果報告使用&quot;[!UICONTROL First Event]&quot;歸因規則和5月1日至21日的日期範圍，則第一個事件（4月30日按一下Keyword_1）不會納入報告中。 如果您使用相同的日期範圍但使用&quot;[!UICONTROL Last Event]&quot;歸因規則，則轉換會包含在報表中，因為上次點按是在指定的日期範圍內。

* 產品組合篩選選擇會排除導致轉換的某些事件。

  如果您針對投資組合的子集製作報表，則可能無法包含行銷活動，其中包含根據某一項歸因規則將轉換歸因於的事件。 例如，假設使用者從Portfolio_1按一下Keyword_1，從Portfolio_2按一下Keyword_2，然後轉換。 如果報告使用&quot;[!UICONTROL First Event]&quot;attribution規則，則Portfolio_1必須包含才能將轉換包含在報表中。 不過，如果報表使用「最後事件」歸因規則，則必須包含Portfolio_2。

>[!TIP]
>
>如果您想要比較不同歸因規則下的轉換總計，請使用報表引數»[!UICONTROL Conversions based on transaction date]」並選取所有廣告網路或所有產品組合。 如果您未設定其他篩選器，則轉換總計應相符。

+++

+++雖然總數正確，但個別資料欄位仍不正確。
當量度格式使用整數時，可能會發生這種情況：

* 如果您建立 [自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) 使用格式 *不含小數點的數字* （會將資料顯示為整數），並將其納入使用加權轉換歸因規則的檢視或報表中([!UICONTROL Weight First Event More]， [!UICONTROL Weight Last Event More]，或 [!UICONTROL Even Distribution])，則輸出會以整數顯示，而非小數。 在這種情況下，個別資料欄位可能不正確，儘管總數正確。 例如，如果順序平均分配到三個事件，則一個順序（而不是0.33順序）會歸因於三個事件的每個。 若要解決問題， [變更量度格式](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) 至 *數字至2小數點*.

* 同樣地，如果您的收入量度是以整數傳送，則會發生相同的問題。 （收入格式是由提交資料的轉換標籤所控制。） 若要解決問題， [建立自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) 僅由收入量度和格式組成 *數字至2小數點*，並將其納入檢視和報表中，而非原始量度。
+++

+++當遺失點按或收入資料時，如何防止其影響未來的出價？
搜尋、社交和商務與廣告網路不同步時，會發生點選資料問題。 請連絡您的Adobe帳戶團隊，以手動同步帳戶。 如果整天的點選資料遺失，請要求您的Adobe帳戶團隊將當天排除在成本模型之外。

由於追蹤或摘要檔案問題，可能會發生收入資料問題。 請聯絡您的Adobe客戶團隊以調查此問題。 如果一整天的收入資料都遺失，請要求您的Adobe帳戶團隊將該天從收入模型中排除。
+++

+++貨幣資料以錯誤的格式顯示。
預設情況下，報表中的所有貨幣資料都會以美元的格式顯示（例如1,000.00）。 若要以正確的貨幣格式顯示值（但不含CSV和TSV格式的任何貨幣符號），請新增&quot;[!UICONTROL Currency]」欄放入報表。 如果報表包含使用不同貨幣的帳戶資料，則任何「[!UICONTROL Total]「貨幣值只是欄中所有數字的總和，不考慮貨幣。
+++

+++為什麼我會看到交易屬性的小數值應該是自然數（1、2等等）？
在以下情況下，您可能會看到小數值：

* 如果您使用以外的任何轉換歸因規則引數執行報表 [!UICONTROL Last Event] 或 [!UICONTROL First Event]，則收入可能會在轉換路徑中的多個事件之間分割。

* 在 [!UICONTROL Transaction Report]，若為多個 [競標單位](/help/search-social-commerce/glossary.md#a-b) 不同比對型別具有相同的交易ID時，追蹤ID的收入會根據指定點選日期的點選次數進行分割。
+++

## 標準效能測量結果

+++報表中缺少點按資料。
以下是缺少點按資料的常見原因。

| 原因 | 偵測/分析 | 解決方法 |
|---|---|---|
| 從廣告帳戶擷取點選資料的程式失敗。 | 沒有系統化的方式可偵測此問題，但您可能會注意到，即使廣告帳戶花費了金錢，促銷活動仍不會顯示成本或點選資訊。 | 聯絡客戶支援： &lt;*您的搜尋、社交和商務使用者帳戶*>@support\.efrontier\.com.<!-- Escaped periods and using HTML code for angle brackets --><br><br>如果資料遺失超過24小時，則從成本預測中排除這些日期，直到擷取資料為止。 您的Adobe帳戶團隊可以排除日期。 |
| 廣告商與廣告網路之間的計費問題導致廣告帳戶無法花費。 | 沒有系統化的方式可偵測此問題，但您可能會注意到行銷活動未顯示任何成本或點選資訊。 | 如果您知道廣告帳戶因帳單問題而無法支出，則從成本預測中排除這些日期。 您的Adobe帳戶團隊可以排除日期。 |
+++

+++效能資料與廣告網路編輯器中的資料不同。
當廣告網路傳送更新至先前的資料時（通常是因為他們將點選詐騙歸因於某些點選），Search、Social和Commerce不會更新資料，除非存在超過5%的差異且Adobe帳戶團隊提出了請求。

此外，當您比較跨日期範圍彙總的曝光比重資料時，Search、Social和Commerce報告的資料可能與廣告網路報告的資料不同。 造成差異的原因在於廣告網路API如何報告資料，Search、Social和Commerce會使用此API來提取資料。 例如， [!DNL Google Ads] 資料：

* 對於大多數曝光比重量度， [!DNL Google Ads] 對小於10%或大於90%的值所報告的值上限為低端或高端。 &lt;10%的資料報告為0.0999，>90%的資料報告為0.9001

* 當日期範圍內混用上限和未上限的資料時，Search、Social和Commerce會使用API中傳回的值依現狀彙總曝光分享資料，對小於10%的列使用0.0999，對大於90%的列使用0.9001。 此彙總可能會導致以下專案的差異： [!DNL Google Ads] 預先彙總資料是因為 [!DNL Google Ads] 可以使用實際百分比值，例如7%或97%。
+++

+++報表中的效能資料與中的資料不同 [!DNL Google Analytics].
這兩個系統會測量不同的資料，因此您應該會看到不同的資料。 例如：

* Search、Social和Commerce (以及Google Ads)會追蹤點按，而 [!DNL Google Analytics] 追蹤每30分鐘瀏覽器工作階段的造訪次數。 例如，如果使用者按一下您的廣告一次，按一下「上一步」按鈕，然後再次按一下廣告，則Search、Social和Commerce會記錄兩次點按，但 [!DNL Google Analytics] 記錄一次造訪。

* [!DNL Google Analytics] 顯示所有流量資料，而搜尋、社交和商務(和 [!DNL Google Ads])會篩選無效的點按（例如過多、重複的點按）。

* [!DNL Google Analytics] 包含所有點按的點按和收入資料。 搜尋、Social和Commerce無法追蹤包含不正確或遺失追蹤URL的廣告和關鍵字的點選和收入資料。
+++

## 轉換量度

+++我的報表未顯示轉換資料。
報表中可能不會包含已發生轉換的轉換量度。
+++

+++報表中缺少收入。

**使用Adobe廣告轉換標籤的廣告商**

*可能的原因：*

* 已新增關鍵字或廣告，但未在追蹤範本或目的地URL中加上搜尋、社交和商務點選追蹤首碼，或追蹤首碼不正確。

* 未在所有適用網頁上正確實作轉換追蹤標籤或已編輯。

* Search、Social和Commerce追蹤的交易屬性會從報表中排除，因此不可見。

* 未實作使用者端的收入剖析器。

*可能的解決方案或因應措施：*

1. 確認報表或資料檢視中包含正確的欄。 如果無法新增正確的欄，您或您的Adobe帳戶團隊必須 [讓交易屬性可供報表使用](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. 確認已在所有適用網頁上實作正確的轉換追蹤標籤。 如有必要，請要求您的Adobe帳戶團隊為每個適用的轉換追蹤標籤建立測試交易，並擷取交易的詳細資訊，例如 `transactionid` 和來自Cookie的詳細資訊(例如 `trackingid`， `clickid`、等等)。

1. 如果 [!UICONTROL Auto Upload] 選項已針對行銷活動停用，且您已新增關鍵字或廣告，然後確定您已產生追蹤範本或目的地URL，包括每個的搜尋、社交和商務點選重新導向追蹤。 您的Adobe帳戶團隊可以執行內部報表，以檢視是否有任何點選追蹤URL （追蹤範本或目的地URL）遺失或格式錯誤。

   如有必要，請建立具有正確URL的Bulksheet檔案來產生追蹤，並使用 **產生追蹤URL** 選項。

   目的地URL應該以「http://pixel.everesttech.net」或「https://pixel.everesttech.net」開頭。

1. 如果這些步驟都無法解決問題，則 [聯絡客戶服務](/help/search-social-commerce/get-help.md).

   如果客戶尚未啟動或剛啟動，客戶服務就會驗證是否已設定收入剖析器。 如果剖析器已設定，剖析器會驗證Search、Social和Commerce是否收到任何畫素轉換，並疑難排解問題。

**傳送轉換資料摘要的廣告商**

*可能的原因：*

* 摘要檔案未傳遞、未完全剖析，或摘要包含孤立交易。

* 相關交易屬性會從報表中排除，因此不可見。

>[!NOTE]
>
>通常在收到摘要後2-4小時，資料才會出現在使用者介面中。

*可能的解決方案或因應措施：*

1. 確認報表或資料檢視中包含正確的欄。 如果無法新增正確的欄，您或您的Adobe帳戶團隊必須 [讓交易屬性可供報表使用](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. 執行 [!UICONTROL Portfolio Report]. 如果它是空的，則執行 [!UICONTROL Campaign Report] 和 [!UICONTROL Search Engine Report] 以檢視收入是否出現在這些報表中。 若包含，則行銷活動可能不會指派給適當的投資組合。

1. 確認檔案已傳送至收入伺服器，且檔案遵循與先前檔案相同的格式和檔案命名慣例。

   如果格式或檔案命名慣例變更，則修正檔案並重新傳送它。

1. 如果檔案已傳送，則 [聯絡客戶服務](/help/search-social-commerce/get-help.md).

   客戶服務將檢查檔案是否已接收及剖析。 如果檔案處理時沒有發生錯誤，他們就會檢查是否有孤立的交易。
+++

+++有些進階報表並不包含廣告商摘要提供的轉換資料。
此 [!UICONTROL Geo Distribution Report] 和 [!UICONTROL Domain Referral Report] 使用透過Adobe Advertising轉換追蹤服務擷取的資料，且只能為該服務的廣告商產生。 報表不包含在Adobe Advertising轉換追蹤系統之外追蹤的轉換資料。
+++

+++收入資料與廣告商本身的收入資料不同。

**使用Adobe廣告轉換標籤的廣告商**

*可能的原因：*

* Search、Social和Commerce會在Cookie過期或刪除時忽略收入，但廣告商可能會將其視為有效收入。

* 前往廣告商頁面的流量來自書籤或自然搜尋，而不是來自廣告。

* 未在所有適用網頁上正確實作轉換追蹤標籤或已編輯。

*可能的解決方案或因應措施：*

1. 前往 **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** 並產生 [!UICONTROL Transaction Report]. 將Search、Social和Commerce收到的交易與廣告商的資料進行比較。

1. 如果某些交易不正確或遺失，請確定相關轉換追蹤標籤已在所有適用網頁上實作，且未進行編輯，除非您的Adobe帳戶團隊建議您這麼做。 如果最近更新了網站，標籤可能會遺失或變更。

   搜尋、Social和Commerce預期內的URL格式正確（具有名稱 — 值配對中的引數） `ef_transaction_properties` 變數和 `src` 的元素 `img` 標籤之間。

1. 如果您無法判斷及解決問題，則 [聯絡客戶服務](/help/search-social-commerce/get-help.md).

   客戶服務將嘗試識別缺少的交易，然後檢查是否有孤立的交易和非來自廣告的交易（「不相關的轉換」）。

**具有轉換資料摘要的廣告商，使用 `ef_id` 值**

檢視上述畫素實施的可能原因和解決方案。

**具有使用交易ID的轉換資料摘要的廣告商**

*可能的原因：*

* Search、Social和Commerce會在Cookie過期或被刪除時忽略收入，但廣告商可能會將其視為有效收入。

* 前往廣告商頁面的流量來自書籤或自然搜尋，而不是來自廣告。

* 發生具有相同交易ID的線上交易之前，已報告離線轉換。 線上交易必須先發生。

*可能的解決方案或因應措施：*

1. 前往 **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** 並產生 [!UICONTROL Transaction Report]. 比較Search、Social和Commerce收到的交易與廣告商的摘要資料。

1. 如果報表中缺少摘要檔案中的交易，則請檢查在離線轉換前是否發生了具有相同交易ID的線上交易（透過畫素追蹤）。

1. 如果您無法判斷及解決問題，則 [聯絡客戶服務](/help/search-social-commerce/get-help.md).

   客戶服務將檢查資料剖析錯誤，並且 [孤立交易](/help/search-social-commerce/glossary.md#o-p).

**具有其他轉換資料摘要型別的廣告商**

*可能的原因：*

* Search、Social和Commerce會在Cookie過期或刪除時忽略收入，但廣告商可能會將其視為有效收入。

* 前往廣告商頁面的流量來自書籤或自然搜尋，而不是來自廣告。

* 有 [孤立交易](/help/search-social-commerce/glossary.md#o-p)，因此Search、Social和Commerce不會計算所有應有的收入。

* 廣告商已針對一組與其在摘要中傳送的不同資料驗證「搜尋、社交和商務」報表。

* 交易ID (`ev_transid` 值)、不唯一或不正確。

* 摘要檔案包含重複的追蹤ID。

* 剖析檔案時發生錯誤。

* 廣告商的重複資料刪除邏輯與搜尋、社交和商務邏輯不同。

*可能的解決方案或因應措施：*

1. 前往 **[!UICONTROL Insights]和[!UICONTROL Reports > Reports]** 並產生 [!UICONTROL Transaction Report]. 將Search、Social和Commerce收到的交易與廣告商的資料進行比較。

1. 如果某些交易不正確或遺失，請確定a)摘要檔案包含所有必要的交易ID且沒有重複的追蹤ID，以及b)交易ID是唯一的且正確無誤。

1. 如果您無法判斷及解決問題，則 [聯絡客戶服務](/help/search-social-commerce/get-help.md).

   客戶服務將檢查資料剖析錯誤和孤立交易。
+++

+++收入資料與Adobe Analytics中的資料不同。請參閱 [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## 特定報告

+++如果 [!UICONTROL Portfolio Report] 顯示與 [!UICONTROL Portfolios] 檢視？
此 [!UICONTROL Portfolio Report] 和 [!UICONTROL Portfolios] 當檢視的所有篩選器、報表引數以及檢視和報表的資料欄相同時，檢視會顯示相同的資料。 例如，如果 [!UICONTROL Portfolios] 檢視顯示屬於「」的投資組合[!UICONTROL All but inactive]「日期範圍的」[!UICONTROL Last 7 days]」並只顯示預設資料欄，然後 [!UICONTROL Portfolio Report] 使用預設引數會顯示相同的資料。 如果您變更任何報表引數，或在 [!UICONTROL Portfolios] 檢視，則資料值可能不同。
+++

+++我的中的資料 [!UICONTROL Portfolio Report] 不符合「 」中的資料 [!UICONTROL Search Engine Report] 或 [!UICONTROL Search Engine Account Report].
此 [!UICONTROL Portfolio Report] 僅顯示指派給指定投資組合的行銷活動的資料，但 [!UICONTROL Search Engine Report] 和 [!UICONTROL Search Engine Account Report] 可能也會包含未指派給投資組合之行銷活動的資料。
+++

+++如何 [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] 與投資組合層級不同 [!UICONTROL Model Accuracy Report]？
(僅限代理商帳戶管理員、Adobe帳戶管理員及管理員使用者) [!UICONTROL Forecast Accuracy Report] 提供自 [!UICONTROL Reports] > [!UICONTROL Model Accuracy] 提供與產品組合層級相同的資料 [!UICONTROL Model Accuracy Report] 但您可在多個投資組合中執行它，而且您可以變更歸因規則。 您也可以使用自訂引數執行及排程報表，也可以用它建立試算表摘要。 此外， [!UICONTROL Forecast Accuracy Report] 比舊版產品組合層級報表更準確，因為前者會使用產品組合的歷史目標而非目前目標來評估收入正確性，且更準確地表示適用時區的資料。
+++

+++廣告層級資料不可用於 [!DNL Google Ads] 動態搜尋廣告(DSA)、最高效能、智慧購物和 [!DNL YouTube] 行銷活動。
廣告網路未提供將收入歸因於這些促銷活動的個別廣告所需的識別碼。 因此，廣告層級的成效資料不適用於 [!UICONTROL Ads] 在「 」中檢視或 [!UICONTROL Ad Variation Report]. 預計行銷活動的廣告層級資料總計與行銷活動資料總計之間會不符。
+++

+++在 [!UICONTROL Transaction Report]，如何知道哪個交易屬性來自資料摘要或由Adobe Advertising追蹤畫素追蹤？
在交易報表中，如果您包含自訂欄，您可以分辨是否有Adobe Advertising追蹤畫素追蹤包含的交易屬性」[!UICONTROL Tracking URL].」 以Adobe Advertising追蹤畫素開始追蹤URL`http://pixel.everesttech.net`.」
+++

+++我的中的資料 [!UICONTROL Transaction Report] 不符合「 」中的資料 [!UICONTROL Keyword Report].
當您按投資組合產生這兩個報表時，如果您產生 [!UICONTROL Keyword Report] 使用歷史資料（即根據指定日期內的產品組合設定），而不是使用目前行銷活動的資料。 當您產生 [!UICONTROL Transaction Report] 依產品組合，其中包含產品組合中目前行銷活動的資料。
+++

## 試算表摘要

+++報告輸出包含日期範圍的組合。
如果摘要使用「 」以外的任何資料彙總層級來彙總資料，您可能會看到不同的日期範圍[!UICONTROL Daily].」

若要解決此問題，請更新試算表摘要，以包含每日彙總的資料。 此工作包括更新報告範本、使用範本產生報告、建立自訂 [!DNL Microsoft® Excel] 範本，然後更新摘要設定以包含新的Excel範本。 如需詳細資訊，請參閱「[編輯試算表報表摘要設定](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).」
+++

+++試算表摘要導致內部錯誤。
如果您變更報表範本中的欄，但未更新 [!DNL Microsoft® Excel] 據以建立範本。

若要解決此問題，請更新試算表摘要以包含新欄。 此工作包括更新報告範本、使用範本產生報告、建立自訂 [!DNL Excel] 範本，然後更新摘要設定以包含新的Excel範本。 如需詳細資訊，請參閱「[編輯試算表報表摘要設定](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).」
+++

+++當我嘗試開啟試算表摘要時 [!DNL Excel]， [!DNL Excel] 報告「無法讀取的內容」錯誤，並從復原的內容中移除資料。
當 [!DNL Microsoft® Excel] 範本不會依開始日期遞增順序排序資料，試算表摘要可能會包含空白列。 尤其是， [!DNL Excel] 回報錯誤「Excel在「」中發現無法讀取的內容&lt;*報告名稱*>.xlsx.&#39; 您要復原活頁簿的內容嗎？ 如果您信任此活頁簿的來源，請按一下「是」。 如果按一下「是」，您會收到下列訊息：「已移除記錄：儲存格資訊來自/xl/worksheets/sheet1.xml部分」，且試算表摘要包含空白列。

若要解決問題，請編輯 [!DNL Excel] 與摘要關聯的範本，用於排序資料 [!DNL Start date in Ascending (Oldest to Newest) order]，然後透過試算表摘要設定上傳更新的範本。 如需詳細資訊，請參閱「[編輯試算表報表摘要](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).」
+++
