---
title: ' [!DNL Microsoft Advertising] 帳戶必要的大量表單資料'
description: 參考 [!DNL Microsoft Advertising] 帳戶大量表單中必要的標題欄位和資料欄位。
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# 附錄 — [!DNL Microsoft Advertising]帳戶需要的大量表單資料

若要大量建立和更新[!DNL Microsoft Advertising]行銷活動資料，您可以使用特別針對[!DNL Microsoft Advertising]帳戶格式化的搜尋、社交和Commerce大量表單檔案。 您可以a) [以必要的檔案格式](../bulksheet-download.md)產生現有帳戶的批次工作表檔案，或b)手動建立這些檔案（如需支援之檔案格式的一般資訊，請參閱[支援的批次工作表檔案格式](bulksheet-file-formats.md)）。

每個Bulksheet都必須包含標題欄位，以及您要執行[特定作業](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) （例如建立廣告）所需的對應資料欄位。 當欄位不是必填欄位時，您可以從標題和資料列忽略它。 上傳大量工作表檔案時，會刪除所有自訂欄。

以下表格包含所有可用的資料欄位和其他表格，指出必須新增、編輯或刪除個別實體資料（例如行銷活動和關鍵字）的欄位。

## 所有可用資料欄位 {#bulksheet-fields-all-microsoft}

下表說明所有可用的資料欄位。

有關帳戶實體相關的資料欄位，請參閱&quot;[建立、編輯或刪除每個帳戶元件](#bulksheet-fields-per-component-microsoft)所需的欄位。&quot;

| 欄位 | 說明 |
|----|----|
| [!UICONTROL Platform] | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Acct Name] | 可識別廣告網路帳戶的唯一名稱。 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 可識別帳戶促銷活動的唯一名稱。 長度上限為128個字元。 |
| [!UICONTROL Campaign Budget] | 每日或每月行銷活動預算，含或不含貨幣符號和標點符號。 不得少於0.05。 |
| [!UICONTROL Channel Type] | 行銷活動鎖定的管道型別： <i>[!UICONTROL Audience]</i>、<i>[!UICONTROL DynamicSearchAds]</i>、<i>[!UICONTROL Search]</i>或<i>[!UICONTROL Shopping]</i>。 |
| [!UICONTROL Delivery Method] | （僅含每日預算的行銷活動）每天顯示行銷活動廣告的速度：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新行銷活動的預設值）：將您的廣告印象分散在一天當中。</li><li><i>[!UICONTROL Accelerated]：</i>在達到預算之前，儘可能顯示您的廣告。 因此，您的廣告可能不會在當天稍後出現。</li></ul> |
| [!UICONTROL Campaign Priority] | （僅限購物行銷活動）當多個行銷活動廣告相同產品時，使用行銷活動的優先順序： <i>[!UICONTROL Low]</i> （新行銷活動的預設值）、<i>[!UICONTROL Medium]</i>或<i>[!UICONTROL High]</i>。<br><br>當同一個產品包含在多個行銷活動中時，廣告網路會先使用行銷活動優先順序來判斷哪個行銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。 |
| [!UICONTROL Merchant ID] | （僅限於連結至商家摘要的購物行銷活動和對象行銷活動）其產品用於行銷活動的商家帳戶的客戶ID。 |
| [!UICONTROL Sales Country] | （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動產品銷售的國家/地區。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。 |
| [!UICONTROL Product Scope Filter] | （僅使用購物網路的行銷活動）商家帳戶中的產品，可為行銷活動建立產品廣告。 您可以使用格式dimension=attribute，輸入最多七種產品維度和屬性組合，以篩選產品。 使用「>>」分隔符號分隔多個篩選器。 如需可用產品維度的清單，請參閱&quot;[購物行銷活動產品篩選器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;。<br><br>範例： &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br>若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL DSA Domain Name] | （型別a） &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot;或b) &quot;<i>[!UICONTROL Search]</i>&quot; （未設定[!DNL ExperimentId]元素時）動態搜尋廣告目標網站的網域名稱。 長度上限為2,048個字元。 如果網域名稱包含`www`，則已修剪且未使用。<br><br>對於現有的行銷活動，您無法編輯網域，但必須包含它以更新其他屬性。 |
| [!UICONTROL DSA Domain Language] | （型別a） &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot;或b) &quot;<i>[!UICONTROL Search]</i>&quot; （未設定[!DNL ExperimentId]元素時）動態搜尋廣告目標網站頁面的語言。 支援的網域語言為[!UICONTROL Dutch]、[!UICONTROL English]、[!UICONTROL French]、[!UICONTROL German]、[!UICONTROL Italian]、[!UICONTROL Spanish]和[!UICONTROL Swedish]。<br><br>對於現有的行銷活動，您無法編輯語言，但必須包含它以更新其他屬性。 |
| [!UICONTROL Ad Group Name] | 可識別廣告群組的唯一名稱。 長度上限為128個字元。 結尾的空白字元不會儲存（例如，「廣告群組1」會儲存為「廣告群組1」）。 |
| [!UICONTROL Ad Group Type] | （搜尋網路上的行銷活動；現有廣告群組的唯讀）廣告群組型別： <i>[!UICONTROL Audience]</i> （僅適用於對象行銷活動）、<i>[!UICONTROL Search Dynamic]</i> （僅適用於動態搜尋廣告）及<i>[!UICONTROL Search Standard]</i> （僅適用於回應式搜尋廣告和現有的展開文字廣告）。 有些行銷活動型別可以包含多種廣告群組型別。 |
| [!UICONTROL Keyword] | （僅限搜尋網路上的促銷活動）關鍵字字串。 長度上限為50個字元。<br><br><b>附註：</b><ul><li>若要在廣告群組或行銷活動層級排除關鍵字，請將[!UICONTROL Match Type]設為`Negative`。 如果列包含廣告群組名稱，則會為廣告群組排除關鍵字。 如果列不包含廣告群組名稱，則會在整個行銷活動中排除關鍵字。</li><li>變更[!DNL Microsoft Advertising]關鍵字會刪除現有關鍵字，並建立具有新關鍵字識別碼的新關鍵字。 但是，變更相符型別並不會刪除現有的關鍵字。</li></ul> |
| 位置 | 已棄用 |
| [!UICONTROL Audience] | 搜尋廣告(RLSA)的再行銷清單，目標為行銷活動或廣告群組的對象。 |
| [!UICONTROL Target Type] | （僅限RLSA目標）目標型別： <i>[!UICONTROL Inclusion]</i>或<i>[!UICONTROL Exclusion]</i>。 |
| [!UICONTROL Auto Target Expression] | 廣告群組的動態搜尋目標。 針對所有目標，請使用&quot;[!UICONTROL All Web Pages]&quot;。<br><br>若要鎖定最多三個動態搜尋條件，請使用格式`<category>=<target>`，其中&lt;category>可包含下列任何類別。 使用&quot;`[blank space] and [blank space]`&quot;為個別類別聯結多個目標，並使用&quot;`[blank space] and [blank space]`&quot;。<br>聯結多個類別<ul><li><i>類別：</i>若要針對具有特定Google內容類別的已索引頁面顯示動態搜尋廣告。</li><li><i>URL：</i>若要針對具有特定URL的索引頁面顯示動態搜尋廣告，其中值可能包含在URL內的任何位置。</li><li><i>頁面標題：</i>若要針對在頁面標題中有特定文字的索引頁面顯示動態搜尋廣告。</li><li><i>頁面內容：</i>若要針對具有特定內容的索引頁面顯示動態搜尋廣告。</li></ul>範例： url=shoes.example.com and page title=footwear<br>範例：所有網頁 |
| [!UICONTROL Location] | 為行銷活動或廣告群組放置廣告的地理位置；值不區分大小寫。 如果您沒有為行銷活動或廣告群組輸入任何值，則會鎖定所有位置。 若要鎖定特定位置，請使用[!DNL Microsoft Advertising]位置代碼格式輸入位置。 若要下載位置清單，請使用您的[!DNL Microsoft Advertising]廣告帳戶認證登入[!DNL Microsoft Advertising]開發人員入口網站。 <b>注意：</b>若要排除位置，請在位置代碼前面加上減號(`-`)，例如`-United States`。 |
| [!UICONTROL Location Type] | 位置型別，例如「城市」、「國家」、「都市區」、「郵遞區號」和「州/省」。 若要下載位置清單，請使用您的[!DNL Microsoft Advertising]廣告帳戶認證登入[!DNL Microsoft Advertising]開發人員入口網站。 |
| [!UICONTROL Match Type] | （僅限搜尋網路上的促銷活動）關鍵字比對選項。 這可能包括動態搜尋目標或產品群組的關鍵字比對選項。 值包括： <i>[!UICONTROL Broad]</i> （新關鍵字的預設）、<i>[!UICONTROL Exact]</i>、<i>[!UICONTROL Phrase]</i>、<i>[!UICONTROL Content]</i> （當廣告群組鎖定內容網路時，自動設定關鍵字）、<i>[!UICONTROL Negative]</i> （排除內容網路上的關鍵字）、<i>[!UICONTROL Dynamic Ad Target]</i> （新動態搜尋目標的預設）、<i>[!UICONTROL Product Group]</i> （新產品群組的預設）或<i>[!UICONTROL Negative Product Group]</i> （排除產品群組）。  需要符合型別或關鍵字ID的值，才能編輯或刪除具有多個符合型別的關鍵字。<br><br>若是Broad Match Modifier，請選擇[廣泛]，並在關鍵字中需要的任何字詞前插入`+` （例如，&quot;`+red +shoes`&quot;同時需要[紅色]和[鞋子]）。<br><br>變更[!DNL Microsoft Advertising]關鍵字的相符型別不會刪除現有關鍵字。 |
| [!UICONTROL Max CPC] | （搜尋網路上的行銷活動）最高每次點按成本(CPC)，這是根據關鍵字、產品群組或動態搜尋目標（無論有無）支付廣告點按的最高金額。  對於最佳化產品組合中的現有關鍵字和產品群組記錄，更新僅在一天內有效，並在下一個最佳化週期中被覆寫。 <b>注意：</b>您無法設定負關鍵字的競標。 |
| [!UICONTROL Max Content CPC] | （唯讀，適用於2017年汰除內容網路之前建立的CPC行銷活動）最高每次點按內容成本(CPC)，這是從顯示網路網站為廣告點按付費的最高金額，無論是否包含貨幣符號和標點符號。 |
| [!UICONTROL Audience Target Method] | （對象廣告群組）是否：<ul><li><i>[!UICONTROL Target and Bid]：</i>若要只對與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。</li><li><i>[!UICONTROL Bid Only]：</i>若要顯示廣告，即使是未與目標對象相關聯的使用者，只要他們符合其他廣告群組層級的目標即可。</li></ul> 不過，您可以為特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。 |
| [!UICONTROL Parent Product Groupings] | 任何父級產品群組的階層。<br><br>範例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | 產品群組（例如「brand=acme」或「所有產品」）。<br><br><b>附註：</b><ul><li>當指定的產品群組不存在於父級產品群組階層中時，Search、Social和Commerce會建立階層中所需的任何部分。</li><li>每當您在購物行銷活動中建立廣告群組（預設競標設為廣告群組預設競標）時，搜尋、Social和Commerce會自動建立「[!UICONTROL All Products]」群組。 搜尋、Social和Commerce會在產品群組階層的每個層級，自動建立具有廣告群組預設競標的&quot;[!UICONTROL Everything Else]&quot;群組。 您仍然可以明確建立這些預設群組，並排除它們或變更其競標。</li><li>每個廣告群組最多可包含八層產品群組，包括&quot;[!UICONTROL All Products]&quot;和七個其他階層。</li></ul> |
| [!UICONTROL Partition Type] | 產品群組的資料分割型別： <i>[!UICONTROL subdivision]</i> （當它有子產品群組時）或<i>[!UICONTROL unit]</i> （當它沒有子產品群組時）。 |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | （僅限擴充文字廣告、多媒體廣告、回應式廣告和回應式搜尋廣告）廣告的頭條。 每個廣告標題欄位的長度上限為30個字元或15個雙位元組字元，包括任何動態文字（例如關鍵字、`{Param2}`和`{Param3}`動態替代變數的值，以及廣告自訂程式）。<br><br>如果是回應式搜尋廣告，請使用下列格式插入廣告自訂程式，其中「預設文字」是當摘要檔案未包含有效值時要插入的選用值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>如果是展開文字廣告，則必須使用「廣告標題」和「廣告標題2」，而[!UICONTROL Ad Title 3]是選用值。 [!DNL Microsoft Advertising]個已於2022年8月汰除的擴充文字廣告，您現在只能報告及刪除這些廣告。<br><br>對於多媒體廣告、回應式廣告和回應式搜尋廣告，[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]和[!UICONTROL Ad Title 3]為必要欄位，而所有其他廣告標題欄位為選用欄位。<br><br>若要刪除非必要欄位的現有值，請使用值`[delete]` （包括括弧）。<br><br>對於展開文字廣告以外的所有廣告型別，變更廣告文案將會刪除現有廣告，並建立具有相同屬性的新廣告。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | （僅限回應式搜尋廣告；選用）釘選對應廣告標題的位置： `[null]` （沒有值，因此廣告標題適用於所有位置）、1、2或3。 例如，如果[!UICONTROL Ad Title Position]的值為1，則[!UICONTROL Ad Title]只能出現在位置1。 依預設，所有廣告標題皆為空值（沒有值）。 若要刪除現有值，請使用值`[delete]` （包括括弧）。<br><br><b>注意：</b>您可以將多個廣告標題釘選到相同位置。 廣告網路使用已釘選至該位置的其中一個廣告標題。 釘選到位置3的標題可能無法與廣告一起顯示。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | （僅限文字廣告、動態搜尋廣告、多媒體廣告、回應式廣告、回應式搜尋廣告，以及增強型促銷活動層級的網站連結）廣告內文或網站連結。<br><br>對於網站連結，可選擇同時使用[!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]以包含廣告網路可能顯示在連結文字下的額外文字。 每個說明欄位最多可包含35個單位元組或17個雙位元組字元。<br><br>對於廣告，每個說明欄位的長度上限為90個字元或45個雙位元組字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。<br><br>如果是回應式搜尋廣告，請使用下列格式插入廣告自訂程式，其中預設文字是當摘要檔案未包含有效值時要插入的可選值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>如果是文字廣告和動態搜尋廣告，說明第1行是必要的，而[!UICONTROL Description Line 2]是選用的。<br><br>對於多媒體廣告、回應式廣告和回應式搜尋廣告，[!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]為必要專案，[!UICONTROL Description Line 3]和[!UICONTROL Description Line 4]為選用專案。<br><br>若要刪除現有值，請使用值`[delete]` （包括括弧）。<br><br><b>附註：</b><ul><li>（標準文字廣告）組合的標題和文字必須至少有三個字。</li><li>（展開文字廣告）此欄位可選擇性地包含{Param2}和{Param3}動態替代變數。 如果超過100個，廣告文字的長度上限為300個單位元組或150個雙位元組字元。 [!DNL Microsoft Advertising]個已於2022年8月汰除的擴充文字廣告，您現在只能報告及刪除這些廣告。</li><li>（動態搜尋廣告）不允許動態替代文字。</li><li>對於所有廣告型別（展開的文字廣告除外），變更廣告文案將會刪除現有廣告並建立新廣告。</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （僅限回應式搜尋廣告；選用）釘選對應說明的位置： `[null]` （沒有值，因此說明適用於所有位置）、1、2或3。 例如，如果[!UICONTROL Description 1 Position]的值為1，則說明1隻能出現在位置1中。 依預設，系統不會將任何說明釘選到位置。<br><br>若要刪除現有值，請使用值`[delete]` （包括括弧）。<br><br><b>注意：</b>您可以將多個說明釘選到同一個位置。 廣告網路使用已釘選至位置的其中一個說明。 釘選到位置2的說明可能無法與廣告一起顯示。 |
| [!UICONTROL Business Name] | （僅限多媒體廣告）企業名稱，最多25個字元。 |
| [!UICONTROL Promotion Line] | （僅限產品清單廣告）搜尋結果中產品清單所包含的不重複促銷明細行（例如「立即免運費！」）。 長度上限為45個字元。<br><br>根據廣告在頁面上出現的位置，促銷活動行可能會出現在與廣告相關的不同位置（例如廣告下方）。 |
| [!UICONTROL Display URL] | 廣告中包含的URL。<br><br>對於展開的動態搜尋廣告，廣告網路會從網站網域動態產生此值，而您不需要輸入值。<br><br>對於展開的文字廣告和回應式搜尋廣告，您不需要輸入值。 顯示URL會自動從最終URL的網域中擷取。 您可以選擇使用「路徑1」和「路徑2」欄位自訂URL。<br><br><b>附註：</b><ul><li>（具有最終URL的帳戶）顯示URL和最終URL中的網域名稱必須相符。</li><li>[!DNL Microsoft Advertising]個已於2022年8月汰除的擴充文字廣告，您現在只能報告及刪除這些廣告。</li></ul> |
| [!UICONTROL Display Path 1] | （僅限展開的文字廣告、動態搜尋廣告和回應式搜尋廣告）新增到顯示URL的文字，會自動從最終URL擷取。 URL中的每個路徑前面都會加上正斜線(/)。 路徑不能包含正斜線(/)或新行(\n)字元。 每個路徑的長度上限為15個字元或7個雙位元組字元。<br><br>若要插入廣告自訂程式，請使用下列格式，其中「預設文字」是當摘要檔案未包含有效值時要插入的選用值： `{CUSTOMIZER.Attribute name:Default text}` （例如`{CUSTOMIZER.Discount:10%}`<br><br>）例如，如果[!UICONTROL Display Path 1]是「交易」，則顯示URL會是&lt;顯示URL>/交易，例如www.example.com/deals。<br><br>[!DNL Microsoft Advertising]個已於2022年8月汰除的擴充文字廣告，您現在只能報告及刪除這些廣告。 |
| [!UICONTROL Display Path 1] | （僅限展開的文字廣告、動態搜尋廣告和回應式搜尋廣告）其他顯示路徑；請參閱[!UICONTROL Display Path 1]的專案。<br><br>範例：如果[!UICONTROL Display Path 1]是「deals」，[!UICONTROL Display Path 2]是「local」，則顯示URL將是&lt;<i>顯示URL</i>>/deals/local，例如www.example.com/deals/local。 |
| [!UICONTROL Start Date] | （僅限增強型網站連結）對網站連結發出投標的第一個日期，在廣告商的時區以及下列格式之一中： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新增強型網站連結的預設值為當天。 <b>注意：</b>新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。 |
| [!UICONTROL End Date] | 網站連結可以和廣告一起出現的最後日期，在廣告商的時區中且以下列格式之一顯示：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新網站連結的預設值為`[blank]` （即無結束日期）。 |
| [!UICONTROL Call To Action] | 要包含在廣告中的行動號召。 檢視[API參考以取得可能的值清單](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction)，但在大量表單中輸入多字呼叫動作做為多個字詞（例如「Bet Now」而非「BetNow」）。 |
| [!UICONTROL Call To Action Language] | 行動號召選項的語言。 請參閱[API參考以取得可能的語言清單](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename)。 |
| [!UICONTROL Base URL/Final URL] | 搜尋引擎使用者按一下您的廣告時，系統會將他們帶往的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 關鍵字層級的基礎/最終URL會覆寫廣告層級和更高級別的URL。<br><br>若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Destination URL] | （包含在產生的大量表單中以供參考；未張貼至搜尋引擎）對於具有目的地URL的帳戶，此URL會將廣告連結至廣告商網站上的基礎URL/登陸頁面（有時透過另一個網站來追蹤點選，然後將使用者重新導向登陸頁面）。 其中包含為「搜尋」、「社交」和「Commerce」行銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，這會根據您的帳戶設定和促銷活動設定中的追蹤引數。 如果您附加搜尋引擎的特定引數，這些引數可能會取代為搜尋、社交和Commerce的同等引數。<br><br>對於具有最終URL的帳戶，此欄會顯示與基礎URL/最終URL欄相同的值。 |
| [!UICONTROL Custom URL Param] | 當變數包含在搜尋帳戶或促銷活動設定的追蹤引數中時，用來取代`{custom_code}`動態變數的資料。 若要在追蹤URL中插入自訂值，您必須使用「產生追蹤URL」選項上傳大量表單檔案。 |
| [!UICONTROL Creative Type] | 廣告格式： <i>[!UICONTROL Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Text Ad]</i>、<i>[!UICONTROL Expanded Dynamic Search Ad]</i>、<i>[!UICONTROL Multimedia Ad]</i>、<i>[!UICONTROL Product Ad]</i> （購物廣告）、<i>[!UICONTROL Responsive Search Ad]</i>或<i>[!UICONTROL Text ad]</i>。 新廣告的預設值為<i>[!UICONTROL Text ad]</i>。 |
| [!UICONTROL Ad Group Start Date] | 可以在廣告商的時區中，以下列格式之一對廣告群組提出競標的第一個日期： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 若為新廣告群組，預設值為目前日期。 |
| [!UICONTROL Ad Group End Date] | 可能為廣告群組下標的最後日期，在廣告商的時區及以下格式之一中： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新廣告群組的預設值為[blank] （即無結束日期）。 |
| [!UICONTROL Tracking Template] | （選用）追蹤範本，可指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。 最精細的層級追蹤範本（以關鍵字為最精細）會覆寫所有較高層級的值。<br><br>若為Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動附加重新導向和追蹤程式碼。<br><br>對於協力廠商重新導向與追蹤，請輸入值。<br><br>如需表示追蹤範本中最終URL的引數清單，請參閱[!DNL Microsoft Advertising]檔案。<br><br>若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Landing Page Suffix] | 要附加至最終URL結尾以追蹤資訊的任何引數。 範例： `param2=value1&param3=value2`<br><br>請參閱 [!DNL Microsoft Advertising][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)的點選追蹤格式。<br><br>較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用[!DNL Microsoft Advertising]編輯器。 |
| 搜尋網路狀態 | 是否要將廣告群組的廣告放置在「搜尋網路」的各種元素上：<ul><li><i>全部：</i>若要在所有Bing搜尋網路和聯合發行搜尋合作夥伴上刊登廣告。</li><li><i>OwnedAndOperatedOnly：</i>僅在Bing和Yahoo上刊登廣告！ 網站。</li><li><i>SyndicatedSearchOnly：</i>僅在Bing和Yahoo上刊登廣告！ 財團搜尋合作夥伴。</li><li><i>關閉：</i>只在「內容網路」（非「搜尋網路」）上刊登廣告。</li></ul> 若為新廣告群組，預設值為「開啟」。 |
| [!UICONTROL Content Network Status] | 已棄用 |
| [!UICONTROL Languages] | 廣告群組中廣告的目標語言： [!UICONTROL English]、[!UICONTROL French]、[!UICONTROL Finnish]、[!UICONTROL German]、[!UICONTROL Norwegian]、[!UICONTROL Spanish]或[!UICONTROL Swedish]。 新行銷活動的預設值為[!UICONTROL English]。<br><br>此設定會決定您的廣告可以顯示的國家和地區。 請務必選擇與行銷活動位置目標相容的語言。 |
| [!UICONTROL Budget Type] | 預算為<i>[!UICONTROL Daily]</i> （預設）或<i>[!UICONTROL Monthly]</i>。<br><br>注意：如果您將行銷活動指派給最佳化的投資組合，此值會自動設為[!UICONTROL Daily]。 |
| [!UICONTROL Device] | 在行銷活動或廣告群組層級進行競標調整的裝置型別： <i>[!UICONTROL smartphone]</i>、<i>[!UICONTROL tablet]</i>或<i>[!UICONTROL desktop]</i>。 |
| [!UICONTROL Bid Adjustment] | 指定目標型別的競標調整。 例如，如果關鍵字層級的競標為1美元，而智慧型手機的競標調整為50%，則智慧型手機的競標為1.50美元。 依預設，所有目標都會以關鍵字層級的競標來競標。 有效百分比可包括：<ul><li>智慧型手機和平板電腦： -100 （不針對裝置型別競標）以及從–90到900</li><li>案頭：從0到900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | 您偏好顯示廣告或網站連結的裝置型別： <i>[!UICONTROL All]</i> （預設）或<i>[!UICONTROL Mobile]</i>。 指定「行動」時，網路會嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示廣告或網站連結。 否則，網路會在任何裝置型別上顯示廣告或網站連結。 <b>注意：</b>網路不保證會在偏好的裝置型別上顯示廣告。 |
| [!UICONTROL Param2] | 如果關鍵字的基礎URL或廣告的標題、說明或基礎URL包含`{Param2}`動態替代字串，則用作替代值的字串。 長度上限為70個字元，但請注意，您使用廣告元素的最大長度限制（例如，標題1和標題2的合併長度上限為76個字元）。 若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Param3] | 如果關鍵字的基礎URL或廣告的標題、說明或基礎URL包含`{Param3}`動態替代字串，則用作替代值的字串。 長度上限為70個字元，但請注意，您使用廣告元素的最大長度限制（例如，標題1和標題2的合併長度上限為76個字元）。 若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Link Name] | 網站連結文字。 此名稱在行銷活動中必須是唯一的。 如果您指定「說明1」和「說明2」，則網站連結文字最多可包含25個單位元組或12個雙位元組字元；否則，網站連結文字最多可包含35個單位元組或17個雙位元組字元。<br><br>[!DNL Microsoft Advertising]可能會顯示含有說明的兩個、四個或六個增強型網站連結，或是含有廣告的四個或六個沒有說明的網站連結。<br><br>您只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立新的增強型網站連結。 |
| [!UICONTROL Campaign Status] | 行銷活動的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有行銷活動）。 新行銷活動的預設值為[!UICONTROL Active]。 若要刪除作用中或暫停的行銷活動，請輸入值`Deleted`。 |
| [!UICONTROL Ad Group Status] | 廣告群組的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有廣告群組）。 新廣告群組的預設值為[!UICONTROL Active]。 若要刪除作用中或暫停的廣告群組，請輸入值`Deleted`。 |
| [!UICONTROL Keyword Status] | 關鍵字的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有關鍵字）。 新關鍵字的預設值為[!UICONTROL Active]。 若要刪除作用中或暫停的關鍵字，請輸入值`Deleted`。 <b>注意：</b>如果您為具有多個相符型別的關鍵字建立追蹤URL，則每個相符型別的關鍵字狀態必須相同。 |
| [!UICONTROL Placement Status] | 已棄用 |
| [!UICONTROL Ad Status] | 廣告的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Deleted]</i> （僅限現有廣告）、<i>[!UICONTROL Disapproved]</i> （無法編輯）或<i>[!UICONTROL Paused]</i>。 新廣告的預設值為[!UICONTROL Active]。 若要刪除作用中或暫停的廣告，請輸入值`Deleted`。 |
| [!UICONTROL Target Status] | 動態搜尋目標的狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有目標）。 新目標的預設值為[!UICONTROL Active]。 若要刪除作用中或暫停的目標，請輸入值`Deleted`。 |
| [!UICONTROL Sitelink Status] | 網站連結的顯示狀態： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有的網站連結）。 新網站連結的預設值為[!UICONTROL Active]。 若要刪除作用中的網站連結，請輸入值`Deleted`。 |
| [!UICONTROL Location Status] | 位置目標的狀態： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有位置）。 新位置的預設值為[!UICONTROL Active]。 若要刪除使用中的位置，請輸入值`Deleted`。 |
| [!UICONTROL Product Group Status] | 產品群組的顯示狀態： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有產品群組）。 新產品群組的預設值為[!UICONTROL Active]。 若要刪除使用中的產品群組，請輸入值`Deleted`。 |
| [!UICONTROL Device Target Status] | 行銷活動或廣告群組層級裝置目標的狀態： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i>。 對於新的行銷活動和廣告群組，預設值為[!UICONTROL Active]。 |
| [!UICONTROL RLSA Target Status] | 行銷活動或廣告群組層級RLSA目標或(僅限Google廣告)排除的狀態： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有目標）。 新目標或排除專案的預設值為[!UICONTROL Active]。 若要刪除作用中的目標或排除專案，請輸入值`Deleted`。 |
| \[廣告商特定標籤分類\] | (以廣告商專屬的標籤分類命名，例如「顏色」（針對稱為「顏色」的標籤分類）與實體相關聯的指定分類值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 最大長度為100個字元，此值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤建立關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值都不區分大小寫。 |
| [!UICONTROL Constraints] | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><b>>限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體輸入值。 |
| [!UICONTROL Campaign ID] | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有當您變更促銷活動名稱時才需要，除非該列包含促銷活動的「[!UICONTROL AMO ID]」。 |
| [!UICONTROL Ad Group ID] | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有當您變更行銷活動名稱時才需要，除非該列包含廣告群組的「[!UICONTROL AMO ID]」。 |
| [!UICONTROL Placement ID] | 已棄用 |
| [!UICONTROL Keyword ID] | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更關鍵字時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL Ad ID] | <p>可識別現有廣告的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]若為回應式搜尋廣告，編輯或刪除廣告資料需使用廣告ID或AMO ID。 對於所有其他實體型別，只有在您變更廣告狀態時才需要AMO ID，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID]&quot;。 不過，如果您既不包含[!UICONTROL Ad ID]也不包含[!UICONTROL AMO ID]，而且廣告屬性欄符合多個廣告，則只有一個廣告的狀態會變更。</p><p><b>注意：</b>如果您編輯a)廣告屬性欄，但現有廣告的「狀態」除外，或b)回應式搜尋廣告的任何資料，而且您既不包含[!UICONTROL Ad ID]也不包含[!UICONTROL AMO ID]，則會建立新廣告，且現有廣告不會變更。 </p> |
| [!UICONTROL Sitelink ID] | 可識別現有網站連結的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄以識別網站連結或b) &quot;[!UICONTROL AMO ID]&quot;。 不過，如果您不包含[!UICONTROL Sitelink ID]或[!UICONTROL AMO ID]，而且屬性資料行符合多個網站連結，則只有其中一個網站連結的狀態會變更。</p><p><b>注意：</b>如果您編輯現有網站連結的Status以外的Sitelink屬性資料行，而且您既不包含[!UICONTROL Sitelink ID]也不包含[!UICONTROL AMO ID]，則會建立新的Sitelink，且不會變更現有的網站連結。 |
| [!UICONTROL Product Group ID] | 可識別現有產品群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有當您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄以識別產品群組或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| 位置ID | 位置目標的唯一[!DNL Microsoft Advertising]識別碼。 若要下載位置清單，請使用您的[!DNL Microsoft Advertising]廣告帳戶認證登入[!DNL Microsoft Advertising]開發人員入口網站。 只有在您變更或刪除位置目標時才需要，除非資料列包含目標的&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL Target ID] | 可識別現有自動目標的唯一ID。 只有在您變更或刪除自動目標時才需要，除非資料列包含目標的&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL RLSA Target ID] | 可識別現有行銷活動或廣告群組層級RLSA目標的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更或刪除目標或排除專案時才需要，除非資料列包含目標的&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | （在產生的大量表單中）同步實體的Adobe產生的唯一識別碼。 對於回應式搜尋廣告，除非您包含廣告ID，否則編輯或刪除廣告時需要AMO ID。 若要編輯具有AMO ID之所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則必須使用AMO ID來編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |
| [!UICONTROL EF Error Message] | （包含在產生的大量表單中以供參考）顯示來自廣告網路的錯誤訊息的預留位置，這些訊息與資料列中的資料有關；錯誤訊息包含在[!UICONTROL EF Errors]個檔案中。 此值未發佈到廣告網路。 |
| [!UICONTROL SE Error Message] | （包含在產生的大量表單中以供參考）顯示來自廣告網路的錯誤訊息的預留位置，這些訊息與資料列中的資料有關；錯誤訊息包含在[!UICONTROL SE Errors]個檔案中。 此值未發佈到廣告網路。 |
| [!UICONTROL Exemption Request] | （包含於產生的大量表單中，以供參考）顯示廣告違反的任何Google廣告原則的名稱和文字的預留位置。 |
| [!UICONTROL Retail Hash] | (包含於使用進階Campaign Management產生的大量表單中以供參考)英數字元雜湊代碼(例如f9639f40cdf56524b541e5dacf55a991)，表示專案是使用進階(ACM)檢視產生的。 |

[^1]： [!DNL Excel]在開啟檔案時將大數轉換為科學記號(例如2115585666的2.12E+09)。 若要以標準標籤法檢視數字，請選取欄中的任何儲存格，然後按一下公式列內的「 」。

## 建立、編輯或刪除每個帳戶元件所需的欄位 {#bulksheet-fields-per-component-microsoft}

以下小節包括與特定帳戶實體相關的欄位。

>[!NOTE]
>
>當欄位不適用於動作時，在欄位中輸入的任何值都會被忽略。

### 行銷活動欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 | 可識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Campaign Budget] | 建立行銷活動所需。 | 行銷活動的每日支出限制，無論是否包含貨幣符號和標點符號。 此值會覆寫，但不能超過科目預算。 |
| [!UICONTROL Channel Type] | 建立行銷活動所需。 |
| [!UICONTROL Delivery Method] | 可選 |
| [!UICONTROL Campaign Priority] | 建立購物行銷活動所需。 |
| [!UICONTROL Merchant ID] | 建立購物行銷活動所需。 |
| [!UICONTROL Sales Country] | 建立購物行銷活動所需。 |
| [!UICONTROL Product Scope Filter] | （購物行銷活動）選填 |
| [!UICONTROL DSA Domain Name] | 未設定[!DNL ExperimentId]元素時，必須建立a) &quot;[!UICONTROL DynamicSearchAds]&quot;或b) &quot;[!UICONTROL Search]&quot;型別的行銷活動 |
| [!UICONTROL DSA Domain Language] | 未設定[!DNL ExperimentId]元素時，必須建立a) &quot;[!UICONTROL DynamicSearchAds]&quot;或b) &quot;[!UICONTROL Search]&quot;型別的行銷活動 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Landing Page Suffix] | <p>可選 |
| [!UICONTROL Budget Type] | 建立行銷活動所需。 |
| [!UICONTROL Device] | 可選 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Campaign Status] | 僅刪除行銷活動時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 只有在您變更行銷活動名稱時才需要，除非該列包含行銷活動的&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 廣告群組欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Group Type] | 建立廣告群組所需。 |
| [!UICONTROL Audience Target Method] | 僅建立對象廣告群組時需要。 |
| [!UICONTROL Ad Group Start Date] | 可選 |
| [!UICONTROL Ad Group End Date] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Search Network Status] | （僅限搜尋網路上的行銷活動）選擇性 |
| [!UICONTROL Languages] | 可選 |
| [!UICONTROL Device] | 可選 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Ad Group Status] | 僅刪除廣告群組時需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Ad Group ID] | 只有在您變更廣告群組名稱時才需要，除非該列包含廣告群組的&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 關鍵字欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Keyword] | 必填 |
| [!UICONTROL Match Type] | 需要符合型別或關鍵字ID的值，才能編輯或刪除具有多個符合型別的關鍵字。 |
| [!UICONTROL Max CPC] | 可選 |
| [!UICONTROL Base URL/Final URL] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Param1] | 可選 |
| [!UICONTROL Param2] | 可選 |
| [!UICONTROL Keyword Status] | 僅刪除關鍵字時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Keyword ID] | 只有在編輯或刪除關鍵字時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 動態搜尋廣告欄位

>[!NOTE]
>
>無法使用建立支援。

對於此廣告型別，請使用[!UICONTROL Download Bulksheet]對話方塊中的&quot;[!UICONTROL Creative (except RSA)]&quot;列。

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2]需要編輯說明。 <b>注意：</b>對於此廣告型別，變更廣告復本會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Display Path 1] | 編輯欄位時需要。 |
| [!UICONTROL Display Path 2] | 編輯欄位時需要。 |
| [!UICONTROL Creative Type] | 需要建立或編輯產品廣告的狀態。 |
| [!UICONTROL Creative Preferred Devices] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告的必要專案。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID]&quot;。 不過，如果您既不包含[!UICONTROL Ad ID]也不包含[!UICONTROL AMO ID]，而且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 產品（購物）廣告欄位

如需建立購物廣告的詳細資訊，請參閱&quot;[實作 [!DNL Microsoft Advertising] 購物行銷活動](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html)&quot;。

對於此廣告型別，請使用[!UICONTROL Download Bulksheet]對話方塊中的&quot;[!UICONTROL Creative (except RSA)]&quot;列。

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Promotion Line] | 可選 |
| [!UICONTROL Base URL/Final URL] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Creative Type] | 需要建立或編輯產品廣告的狀態。 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告的必要專案。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID]&quot;。 不過，如果您既不包含[!UICONTROL Ad ID]也不包含[!UICONTROL AMO ID]，而且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 回應式（多媒體）廣告欄位

對於此廣告型別，請使用[!UICONTROL Download Bulksheet]對話方塊中的&quot;[!UICONTROL Creative (except RSA)]&quot;列。

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | 對於回應式廣告，[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]和[!UICONTROL Ad Title 3]是建立廣告的必要欄位，而所有其他廣告標題欄位是選用欄位。 若要刪除非必要欄位的現有值，請使用值`[delete]` （包括括弧）。 <b>注意：</b>對於此廣告型別，變更廣告復本會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | 必須有[!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]才能建立廣告，而[!UICONTROL Description Line 3]和[!UICONTROL Description Line 4]是選用專案。 <b>注意：</b>對於此廣告型別，變更廣告復本會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Business Name] | 建立或刪除廣告的必要專案。 |
| [!UICONTROL Call To Action] | 建立廣告的必要專案。 |
| [!UICONTROL Call To Action Language] | 建立廣告的必要專案。 |
| [!UICONTROL Base URL/Final URL] | 建立廣告的必要專案。 |
| [!UICONTROL Creative Type] | 選填。 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告的必要專案。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID]&quot;。 不過，如果您既不包含[!UICONTROL Ad ID]也不包含[!UICONTROL AMO ID]，而且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 回應式搜尋廣告欄位

對於此廣告型別，請使用[!UICONTROL Download Bulksheet]對話方塊中的&quot;[!UICONTROL Responsive Search Ad]&quot;列。

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 | |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | 對於回應式搜尋廣告，[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]和[!UICONTROL Ad Title 3]是建立廣告的必要欄位，而所有其他廣告標題欄位是選用欄位。 若要刪除非必要欄位的現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | 可選 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | 對於回應式搜尋廣告，[!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]是建立廣告的必要專案，[!UICONTROL Description Line 3]和[!UICONTROL Description Line 4]是選用專案。 若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | 可選 |
| [!UICONTROL Display Path 1] | 可選 |
| [!UICONTROL Display Path 2] | 可選 |
| [!UICONTROL Base URL/Final URL] | 建立廣告的必要專案。 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Creative Type] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告的必要專案。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 必須編輯或刪除廣告，除非該列包含&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非您包含廣告ID，否則必須編輯或刪除廣告。 |

### 文字廣告欄位

對於此廣告型別，請使用[!UICONTROL Download Bulksheet]對話方塊中的&quot;[!UICONTROL Creative (except RSA)]&quot;列。

>[!NOTE]
>
>已棄用展開的文字廣告。 您只能刪除現有的文字廣告。

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | 唯讀 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2]唯讀 |
| [!UICONTROL Display URL] | 唯讀 |
| [!UICONTROL Display Path 1] | 唯讀 |
| [!UICONTROL Display Path 2] | 唯讀 |
| [!UICONTROL Base URL/Final URL] | 唯讀 |
| [!UICONTROL Custom URL Param] | 唯讀 |
| [!UICONTROL Creative Type] | 可選 |
| [!UICONTROL Tracking Template] | 唯讀 |
| [!UICONTROL Creative Preferred Devices] | 唯讀 |
| [!UICONTROL Ad Status] | 必填 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非您包含廣告ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 動態搜尋目標（自動鎖定目標）欄位

>[!NOTE]
>
>無法使用建立支援。

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Auto Target Expression] | 必填。 |
| [!UICONTROL Match Type] | 可選 |
| [!UICONTROL Max CPC] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Target Status] | 刪除目標所需 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Target ID] | 只有在您變更或刪除自動目標時才需要，除非資料列包含目標的&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 購物產品群組欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Match Type] | 建立產品群組時需要。 |
| [!UICONTROL Max CPC] | 建立產品群組時需要。 |
| [!UICONTROL Parent Product Groupings] | 必填 |
| [!UICONTROL Product Grouping] | 必填 |
| [!UICONTROL Partition Type] | 建立產品群組時需要。 |
| [!UICONTROL Base URL/Final URL] | 必填 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Product Group Status] | 僅刪除產品群組時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Product Group ID] | 只有在您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄以識別產品群組或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 行銷活動層級網站連結欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| 說明第1行 | 可選 |
| [!UICONTROL Description Line 2] | 可選 |
| [!UICONTROL Start Date] | 可選 |
| [!UICONTROL End Date] | 可選 |
| [!UICONTROL Base URL/Final URL] | 必填 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Creative Preferred Devices] | 可選 |
| [!UICONTROL Link Name] | 必填 |
| [!UICONTROL Sitelink Status] | 只有在刪除網站連結時才需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Sitelink ID] | 只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄以識別網站連結或b) &quot;[!UICONTROL AMO ID]&quot;。 不過，如果您不包含[!UICONTROL Sitelink ID]或[!UICONTROL AMO ID]，而且屬性資料行符合多個網站連結，則只有其中一個網站連結的狀態會變更。<br><br><b>注意：</b>如果您編輯網站連結屬性資料行，但現有Sitelink的Status除外，而且您沒有包含[!UICONTROL Sitelink ID]或[!UICONTROL AMO ID]，則會建立新的Sitelink，且現有的Sitelink不會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 位置目標欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Location] | 必填 |
| [!UICONTROL Location Type] | 建立目標所需 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Location Status] | 僅刪除位置目標時需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL AMO ID] | 除非您包含行銷活動ID，否則需要編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 行銷活動層級和廣告群組層級裝置目標欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Device] | 刪除裝置目標時需要。 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Ad Group Name] | 廣告群組層級裝置目標的必要專案。 不適用於行銷活動層級的裝置目標。 |
| [!UICONTROL Device Target Status] | 僅刪除裝置目標時才需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 選用；僅適用於廣告群組層級裝置目標。 |
| [!UICONTROL AMO ID] | 除非您包含裝置目標ID，否則必須編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

### 行銷活動層級和廣告群組層級RLSA目標欄位

如需每個資料欄位的說明，請參閱[所有可用的資料欄位](#bulksheet-fields-all-microsoft)。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 廣告群組層級目標的必要專案。 不適用於行銷活動層級目標。 |
| [!UICONTROL Audience] | 建立新目標時需要。 |
| [!UICONTROL Target Type] | 可選 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL RLSA Target Status] | 刪除目標時需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 選用；僅適用於廣告群組層級目標。 |
| [!UICONTROL RLSA Target ID] | 只有在您變更或刪除目標時才需要，除非資料列包含目標的&quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 除非包含RLSA目標ID，否則必須編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [您可以在大量表單中執行的作業](bulksheet-operations.md)
>* [支援的Bulksheet檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)的點選追蹤格式
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)
