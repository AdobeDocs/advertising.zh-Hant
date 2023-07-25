---
title: 必要的大量表單資料 [!DNL Microsoft Advertising] 帳戶
description: 參考Bulksheets中必要的標題欄位和資料欄位 [!DNL Microsoft Advertising] 帳戶。
exl-id: a3090962-49df-46b0-89f8-98b633c3ea7a
source-git-commit: 1f27e2616d706c56ef1e6a62cf081d83e6f807c1
workflow-type: tm+mt
source-wordcount: '6900'
ht-degree: 0%

---

# 附錄 — 必要的大量表單資料 [!DNL Microsoft Advertising] 帳戶

若要建立和更新 [!DNL Microsoft Advertising] 大量行銷活動資料，您可以使用特別格式化的搜尋、社交和商務大量表單檔案 [!DNL Microsoft Advertising] 帳戶。 您可以) [產生現有帳號的大量工作表檔案](../bulksheet-download.md) (b)手動建立（請參閱「 」）[支援的Bulksheet檔案格式](bulksheet-file-formats.md)」以取得受支援檔案格式的一般資訊)。

每個大量表單都必須包含標題欄位和所需的對應資料欄位 [您要執行的特定作業](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) （例如建立廣告）。 當欄位不是必要欄位時，您可以從標題和資料列忽略它。 上傳大量工作表檔案時，所有自訂欄都會被刪除。

以下表格包含所有可用的資料欄位，以及其他表格，指出個別實體（例如行銷活動和關鍵字）需要新增、編輯或刪除資料的欄位。

## 所有可用資料欄位 {#bulksheet-fields-all-microsoft}

下表說明所有可用的資料欄位。

有關帳戶實體相關的資料欄位，請參閱&quot;[建立、編輯或刪除每個帳戶元件所需的欄位](#bulksheet-fields-per-component-microsoft).」

| 欄位 | 說明 |
|----|----|
| [!UICONTROL Platform] | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Acct Name] | 可識別廣告網路帳戶的唯一名稱。 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 識別帳戶促銷活動的唯一名稱。 長度上限為128個字元。 |
| [!UICONTROL Campaign Budget] | 每日或每月行銷活動預算，無論是否有貨幣符號和標點符號。 不得少於0.05。 |
| [!UICONTROL Channel Type] | 行銷活動鎖定的頻道型別： <i>[!UICONTROL Audience]</i>， <i>[!UICONTROL DynamicSearchAds]</i>， <i>[!UICONTROL Search]</i>，或 <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | （僅具有每日預算的行銷活動）每天顯示行銷活動廣告的速度如何：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新行銷活動的預設）：將廣告印象分散在一天當中。</li><li><i>[!UICONTROL Accelerated]：</i> 在達到預算之前，儘可能多地顯示您的廣告。 因此，您的廣告可能不會在當天稍後出現。</li></ul> |
| [!UICONTROL Campaign Priority] | （僅限購物行銷活動）當多個行銷活動廣告相同產品時，使用行銷活動的優先順序： <i>[!UICONTROL Low]</i> （新行銷活動的預設值）， <i>[!UICONTROL Medium]</i>，或 <i>[!UICONTROL High]</i>.<br><br>當相同產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則符合最高競價的行銷活動條件。 |
| [!UICONTROL Merchant ID] | （僅限連結至商家摘要的購物行銷活動和對象行銷活動）其產品用於行銷活動的商家帳戶的客戶ID。 |
| [!UICONTROL Sales Country] | （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動產品銷售的國家/地區。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。 |
| [!UICONTROL Product Scope Filter] | （僅使用購物網路的行銷活動）您的商家帳戶中的產品，可以針對行銷活動建立產品廣告。 您可以使用格式dimension=attribute，輸入最多七個產品維度和屬性組合，以篩選產品。 使用「>>」分隔符號分隔多個篩選器。 如需可用產品維度的清單，請參閱&quot;[購物行銷活動產品篩選器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).」<br><br> 範例：「`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL DSA Domain Name] | （a型別的行銷活動） 」<i>[!UICONTROL DynamicSearchAds]</i>「或b) 」<i>[!UICONTROL Search]</i>&quot;，當 [!DNL ExperimentId] 元素)動態搜尋廣告的目標網站網域名稱。 長度上限為2,048個字元。 如果網域名稱包含 `www`，已裁剪且未使用。<br><br>對於現有行銷活動，您無法編輯網域，但必須包含它以更新其他屬性。 |
| [!UICONTROL DSA Domain Language] | （a型別的行銷活動） 」<i>[!UICONTROL DynamicSearchAds]</i>「或b) 」<i>[!UICONTROL Search]</i>&quot;，當 [!DNL ExperimentId] 元素未設定)動態搜尋廣告的目標網站頁面語言。 支援的網域語言為 [!UICONTROL Dutch]， [!UICONTROL English]， [!UICONTROL French]， [!UICONTROL German]， [!UICONTROL Italian]， [!UICONTROL Spanish]、和 [!UICONTROL Swedish].<br><br>對於現有的行銷活動，您無法編輯語言，但必須包含它以更新其他屬性。 |
| [!UICONTROL Ad Group Name] | 識別廣告群組的唯一名稱。 長度上限為128個字元。 結尾的空白字元不會儲存（例如，「廣告群組1」會儲存為「廣告群組1」）。 |
| [!UICONTROL Ad Group Type] | （搜尋網路上的行銷活動；現有廣告群組的唯讀）廣告群組型別： <i>[!UICONTROL Audience]</i> （僅適用於對象行銷活動）， <i>[!UICONTROL Search Dynamic]</i> （僅適用於動態搜尋廣告）和 <i>[!UICONTROL Search Standard]</i> （僅適用於回應式搜尋廣告和現有的擴充文字廣告）。 某些行銷活動型別可包含多種廣告群組型別。 |
| [!UICONTROL Keyword] | （僅限搜尋網路上的促銷活動）關鍵字字串。 長度上限為50個字元。<br><br><b>附註：</b><ul><li>若要在廣告群組或行銷活動層級排除關鍵字，請設定 [!UICONTROL Match Type] 至 `Negative`. 如果列包含廣告群組名稱，則會排除廣告群組的關鍵字。 如果列不包含廣告群組名稱，則會在整個行銷活動中排除關鍵字。</li><li>變更 [!DNL Microsoft Advertising] 關鍵字會刪除現有關鍵字，並使用新關鍵字ID建立新關鍵字。 但是，變更相符型別並不會刪除現有關鍵字。</li></ul> |
| 位置 | 已棄用 |
| [!UICONTROL Audience] | 行銷活動或廣告群組的搜尋廣告(RLSA)目標對象的再行銷清單。 |
| [!UICONTROL Target Type] | （僅限RLSA目標）目標型別： <i>[!UICONTROL Inclusion]</i> 或 <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | 廣告群組的動態搜尋目標。 針對所有目標，請使用「[!UICONTROL All Web Pages].」<br><br>若要鎖定最多三個動態搜尋條件，請使用格式 `<category>=<target>`，其中 &lt;category> 可包含下列任何類別。 使用「」聯結個別類別的多個目標`[blank space] and [blank space]`」並使用「」聯結多個類別`[blank space] and [blank space]`「。<br><ul><li><i>類別：</i> 若要針對具有特定Google內容類別的索引頁面顯示動態搜尋廣告。</li><li><i>URL：</i> 顯示具有特定URL之索引頁面的動態搜尋廣告，其中值可能包含在URL內的任何位置。</li><li><i>頁面標題：</i> 顯示索引頁面的動態搜尋廣告，並在頁面標題中顯示特定文字。</li><li><i>頁面內容：</i> 顯示具有特定內容之索引頁面的動態搜尋廣告。</li></ul>範例： url=shoes.example.com和page title=footwear<br>範例：所有網頁 |
| [!UICONTROL Location] | 為行銷活動或廣告群組放置廣告的地理位置；值不區分大小寫。 如果您未輸入任何促銷活動或廣告群組的值，則會鎖定所有位置。 若要鎖定特定位置，請使用 [!DNL Microsoft Advertising] 位置代碼格式。 若要下載位置清單，請登入 [!DNL Microsoft Advertising] 開發人員入口網站，使用您的 [!DNL Microsoft Advertising] advertising帳戶認證。 <b>注意：</b> 若要排除位置，請在位置代碼前加上減號(`-`)，例如 `-United States`. |
| [!UICONTROL Location Type] | 位置型別，例如「城市」、「國家/地區」、「MetroArea」、「PostalCode」和「State」。 若要下載位置清單，請登入 [!DNL Microsoft Advertising] 開發人員入口網站，使用您的 [!DNL Microsoft Advertising] advertising帳戶認證。 |
| [!UICONTROL Match Type] | （僅限搜尋網路上的促銷活動）關鍵字比對選項。 這可能包括動態搜尋目標或產品群組的關鍵字比對選項。 值包括： <i>[!UICONTROL Broad]</i> （新關鍵字的預設值）， <i>[!UICONTROL Exact]</i>， <i>[!UICONTROL Phrase]</i>， <i>[!UICONTROL Content]</i> （當廣告群組鎖定內容網路時，自動設定關鍵字）， <i>[!UICONTROL Negative]</i> （在內容網路上排除關鍵字）， <i>[!UICONTROL Dynamic Ad Target]</i> （新動態搜尋目標的預設值）、 <i>[!UICONTROL Product Group]</i> （新產品群組的預設值），或 <i>[!UICONTROL Negative Product Group]</i> （排除產品群組）。  需要相符型別或關鍵字ID的值，才能編輯或刪除具有多個相符型別的關鍵字。<br><br>若為Broad Match修飾詞，請選擇「Broad」並插入 `+` 在必要的關鍵字內的任何字詞之前(例如&quot;`+red +shoes`」以同時要求「紅色」和「鞋子」)。<br><br>變更的相符型別 [!DNL Microsoft Advertising] 關鍵字不會刪除現有關鍵字。 |
| [!UICONTROL Max CPC] | （搜尋網路上的行銷活動）最高每次點按成本(CPC)，這是根據關鍵字、產品群組或動態搜尋目標（無論有否貨幣符號和標點符號）支付廣告點按的最高金額。  對於最佳化產品組合中的現有關鍵字和產品群組記錄，更新僅在一天內有效，並在下一個最佳化週期中被覆寫。 <b>注意：</b> 您無法設定負關鍵字的競標。 |
| [!UICONTROL Max Content CPC] | （唯讀，適用於在內容網路之前建立的CPC行銷活動，但僅於2017年淘汰）最高每次點按內容成本(CPC)，這是從顯示網路網站為廣告點按付費的最高金額，無論有否貨幣符號和標點符號。 |
| [!UICONTROL Audience Target Method] | （對象廣告群組）是否：<ul><li><i>[!UICONTROL Target and Bid]：</i> 只向與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。</li><li><i>[!UICONTROL Bid Only]：</i>即使未與目標對象相關聯的人，只要他們滿足其他廣告群組層級目標，也能顯示廣告。</li></ul> 不過，您可以針對特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。 |
| [!UICONTROL Parent Product Groupings] | 任何父級產品群組的階層。<br><br>範例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | 產品群組（例如「brand=acme」或「所有產品」）。<br><br><b>附註：</b><ul><li>當指定的產品群組不存在於父產品群組階層中時，Search、Social和Commerce會建立階層中所需的任何部分。</li><li>Search、Social和Commerce會自動建立「」[!UICONTROL All Products]「群組」適用於您在購物行銷活動中建立廣告群組時，且預設競標設為廣告群組預設競標。 Search、Social和Commerce會自動建立「」[!UICONTROL Everything Else]「產品群組階層的每個層級具有廣告群組預設競價的群組。 您仍然可以明確建立這些預設群組，並排除它們或變更其競標。</li><li>每個廣告群組最多可包含八層產品群組，包括「[!UICONTROL All Products]」和其他七個階層。</li></ul> |
| [!UICONTROL Partition Type] | 產品群組的磁碟分割型別： <i>[!UICONTROL subdivision]</i> （當具有子產品群組時）或 <i>[!UICONTROL unit]</i> （當它沒有子產品群組時）。 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | （僅限擴充文字廣告、多媒體廣告、回應式廣告和回應式搜尋廣告）廣告的頭條。 每個廣告標題欄位的長度上限為30個字元或15個雙位元組字元，包括任何動態文字(例如關鍵字的值、 `{Param2}` 和 `{Param3}` 動態替代變數和ad customizers)。<br><br> 對於回應式搜尋廣告，請使用以下格式插入廣告自訂器，其中「預設文字」是當您的摘要檔案未包含有效值時要插入的選用值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>對於展開的文字廣告，需要廣告標題和廣告標題2，並且 [!UICONTROL Ad Title 3] 是選用專案。 [!DNL Microsoft Advertising] 已於2022年8月汰除的擴充文字廣告，您現在只能報告和刪除這些廣告。<br><br>對於多媒體廣告、回應式廣告和回應式搜尋廣告， [!UICONTROL Ad Title]， [!UICONTROL Ad Title 2]、和 [!UICONTROL Ad Title 3] 為必填欄位，而所有其他廣告標題欄位均為選用欄位。<br><br>若要刪除非必要欄位的現有值，請使用值 `[delete]` （包括括弧）。<br><br>對於所有廣告型別（展開的文字廣告除外），變更廣告副本會刪除現有廣告，並建立具有相同屬性的新廣告。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | （僅限回應式搜尋廣告；選用）釘選對應廣告標題的位置： `[null]` （無值，因此廣告標題適用於所有職位）、1、2或3。 例如，如果 [!UICONTROL Ad Title Position] 的值為1，則 [!UICONTROL Ad Title] 只會出現在位置1。 依預設，所有廣告標題均為Null （沒有值）。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。<br><br><b>注意：</b> 您可以將多個廣告標題釘選至相同位置。 廣告網路將使用已釘選至該位置的其中一個廣告標題。 釘選到位置3的標題可能不會與廣告一起顯示。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | （僅限文字廣告、動態搜尋廣告、多媒體廣告、回應式廣告、回應式搜尋廣告，以及增強型促銷活動層級的網站連結）廣告內文或網站連結。<br><br>若為網站連結，可選擇同時使用兩者 [!UICONTROL Description Line 1] 和 [!UICONTROL Description Line 2] 以包含廣告網路可能顯示在連結文字下方的額外文字。 每個說明欄位最多可包含35個單位元組或17個雙位元組字元。<br><br>對於廣告，每個說明欄位的長度上限為90個字元或45個雙位元組字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。<br><br>對於回應式搜尋廣告，請使用以下格式插入廣告自訂器，其中預設文字是當您的摘要檔案未包含有效值時要插入的可選值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>文字廣告和動態搜尋廣告需要說明第1行，而且 [!UICONTROL Description Line 2] 是選用專案。<br><br>對於多媒體廣告、回應式廣告和回應式搜尋廣告， [!UICONTROL Description Line 1] 和 [!UICONTROL Description Line 2] 為必填，且 [!UICONTROL Description Line 3] 和 [!UICONTROL Description Line 4] 是選用專案。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。<br><br><b>附註：</b><ul><li>（標準文字廣告）組合的標題和文字必須至少有三個字。</li><li>（展開文字廣告）此欄位可選擇包含 {Param2} 和 {Param3} 動態替代變數。 如果超過300個單位元組，廣告文字的長度上限為300個單位元組或150個雙位元組字元。 [!DNL Microsoft Advertising] 已於2022年8月汰除的擴充文字廣告，您現在只能報告和刪除這些廣告。</li><li>（動態搜尋廣告）不允許動態替代文字。</li><li>對於所有廣告型別（展開的文字廣告除外），變更廣告副本將會刪除現有廣告並建立新廣告。</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （僅限回應式搜尋廣告；選用）釘選對應說明的位置： `[null]` （無值，因此說明適用於所有職位）、1、2或3。 例如，如果 [!UICONTROL Description 1 Position] 值為1，則「說明1」將僅顯示在「位置1」中。 依預設，不會將任何說明釘選到位置。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。<br><br><b>注意：</b> 您可以將多個說明釘選到相同位置。 廣告網路將使用已釘選至位置的其中一個說明。 釘選到位置2的說明可能不會與廣告一起顯示。 |
| [!UICONTROL Business Name] | （僅限多媒體廣告）企業名稱，最多25個字元。 |
| [!UICONTROL Promotion Line] | （僅限產品清單廣告）搜尋結果中產品清單內含的唯一促銷明細行（例如「立即免運費！」）。 長度上限為45個字元。<br><br>視廣告在頁面上的出現位置而定，促銷明細行可能會出現在與廣告相關的不同位置（例如廣告下方）。 |
| [!UICONTROL Display URL] | 廣告中包含的URL。<br><br>對於展開的動態搜尋廣告，廣告網路會從網站網域動態產生此值，而您不需要輸入值。<br><br>對於展開的文字廣告和回應式搜尋廣告，您不需要輸入值。 系統會自動從最終URL的網域中擷取顯示URL。 您可以選擇使用「路徑1」和「路徑2」欄位自訂URL。<br><br><b>附註：</b><ul><li>（具有最終URL的帳戶）顯示URL和最終URL中的網域名稱必須相符。</li><li>[!DNL Microsoft Advertising] 已於2022年8月汰除的擴充文字廣告，您現在只能報告和刪除這些廣告。</li></ul> |
| [!UICONTROL Display Path 1] | （僅限展開的文字廣告、動態搜尋廣告和回應式搜尋廣告）新增至顯示URL的文字，會自動從最終URL擷取。 URL中的每個路徑前面都有一個正斜線(/)。 路徑不能包含正斜線(/)或新行(\n)字元。 每個路徑的長度上限為15個字元或7個雙位元組字元。<br><br>若要插入廣告自訂程式，請使用下列格式，其中「預設文字」是當摘要檔案未包含有效值時要插入的選用值： `{CUSTOMIZER.Attribute name:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`<br><br>例如，如果 [!UICONTROL Display Path 1] 為「deals」，則顯示URL會是 &lt;display url=&quot;&quot;>/deals，例如www.example.com/deals。<br><br>[!DNL Microsoft Advertising] 已於2022年8月汰除的擴充文字廣告，您現在只能報告和刪除這些廣告。 |
| [!UICONTROL Display Path 1] | （僅限展開的文字廣告、動態搜尋廣告和回應式搜尋廣告）其他顯示路徑；請參閱專案，瞭解 [!UICONTROL Display Path 1].<br><br>範例： If [!UICONTROL Display Path 1] 是「交易」和 [!UICONTROL Display Path 2] 為「local」，則顯示URL會是&lt;<i>顯示URL</i>>/deals/local，例如www.example.com/deals/local。 |
| [!UICONTROL Start Date] | （僅限增強型網站連結）對網站連結發出投標的第一個日期，採用廣告商的時區格式及下列格式之一： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新增強型網站連結的預設值為當天。 <b>注意：</b> 新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。 |
| [!UICONTROL End Date] | 網站連結可以和廣告一起出現的最後日期、以廣告商的時區及以下格式之一顯示：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 如果是新的網站連結，預設值為 `[blank]` （亦即，無結束日期）。 |
| [!UICONTROL Call To Action] | 要包含在廣告中的行動號召。 請參閱 [API參考以取得可能值的清單](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction)，但請在Bulksheets中輸入多個單字的動作呼叫（例如「Bet Now」而非「BetNow」）。 |
| [!UICONTROL Call To Action Language] | 行動號召選項的語言。 請參閱 [API參考以取得可能的語言清單](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | 搜尋引擎使用者按一下您的廣告時，系統會將他們帶往的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 關鍵字層級的基礎/最終URL會覆寫廣告層級和更高層級的基礎/最終URL。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Destination URL] | （包含在已產生的Bulksheet中以供參考；未張貼至搜尋引擎）對於具有目的地URL的帳戶，此URL會將廣告連結至廣告商網站上的基本URL/登陸頁面（有時透過另一個網站來追蹤點選，然後將使用者重新導向到登陸頁面）。 其中包含為Search， Social， &amp; Commerce促銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，這會根據帳戶設定和促銷活動設定中的追蹤引數。 如果您已附加搜尋引擎特定引數，這些引數可能會取代為搜尋、社交和商務的同等引數。<br><br>若為具有最終URL的帳戶，此欄會顯示與「基本URL/最終URL」欄相同的值。 |
| [!UICONTROL Custom URL Param] | 要取代的資料 `{custom_code}` 變數納入搜尋帳戶或促銷活動設定的追蹤引數時，使用動態變數。 若要在追蹤URL中插入自訂值，您必須使用「產生追蹤URL」選項上傳大量表單檔案。 |
| [!UICONTROL Creative Type] | 廣告格式： <i>[!UICONTROL Dynamic Search Ad]</i>， <i>[!UICONTROL Expanded Text Ad]</i>， <i>[!UICONTROL Expanded Dynamic Search Ad]</i>， <i>[!UICONTROL Multimedia Ad]</i>， <i>[!UICONTROL Product Ad]</i> （購物廣告），或 <i>[!UICONTROL Responsive Search Ad]</i>，或 <i>[!UICONTROL Text ad]</i>. 新廣告的預設為 <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | 可對廣告群組下標的第一天（在廣告商的時區中及以下格式之一）：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 若為新廣告群組，預設值為目前日期。 |
| [!UICONTROL Ad Group End Date] | 可對廣告群組下標的最後日期（在廣告商的時區中且以下列格式之一）：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 如果是新廣告群組，預設值為 [空白] （亦即，無結束日期）。 |
| [!UICONTROL Tracking Template] | （選用）追蹤範本，可指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。 最精細層級的追蹤範本（以關鍵字作為最精細的層級）會覆寫所有較高層級的值。<br><br>針對Adobe廣告轉換追蹤，此追蹤會在行銷活動設定包含時套用&quot;[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search、Social和Commerce會自動附加重新導向和追蹤程式碼。<br><br>針對協力廠商重新導向與追蹤，請輸入值。<br><br>如需指出追蹤範本中最終URL的引數清單，請參閱 [!DNL Microsoft Advertising] 說明檔案。<br><br> 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Landing Page Suffix] | 要附加至最終URL結尾以追蹤資訊的任何引數。 範例： `param2=value1&param3=value2`<br><br>請參閱「[的點選追蹤格式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).」<br><br>較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同的追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用 [!DNL Microsoft Advertising] 編輯者。 |
| 搜尋網路狀態 | 是否要將廣告群組的廣告放置在「搜尋網路」的各種元素上：<ul><li><i>全部：</i> 在所有Bing搜尋網路和聯合搜尋合作夥伴上刊登廣告。</li><li><i>OwnedAndOperatedOnly：</i>只在Bing和Yahoo！上刊登廣告 網站。</li><li><i>SyndicatedSearchOnly：</i> 只在Bing和Yahoo！上刊登廣告 財團搜尋合作夥伴。</li><li><i>關閉：</i> 僅將廣告放在內容網路（而非搜尋網路）上。</li></ul> 對於新廣告群組，預設值為「開啟」。 |
| [!UICONTROL Content Network Status] | 已棄用 |
| [!UICONTROL Languages] | 廣告群組中廣告的目標語言： [!UICONTROL English]， [!UICONTROL French]， [!UICONTROL Finnish]， [!UICONTROL German]， [!UICONTROL Norwegian]， [!UICONTROL Spanish]，或 [!UICONTROL Swedish]. 新行銷活動的預設為 [!UICONTROL English].<br><br>此設定會決定您的廣告可以顯示的國家和區域。 請務必選擇與行銷活動位置目標相容的語言。 |
| [!UICONTROL Budget Type] | 預算是否為 <i>[!UICONTROL Daily]</i> （預設）或 <i>[!UICONTROL Monthly]</i>.<br><br>備註：如果您將促銷活動指定至最佳化的投資組合，此值會自動設為 [!UICONTROL Daily]. |
| [!UICONTROL Device] | 在行銷活動或廣告群組層級進行競標調整的裝置型別： <i>[!UICONTROL smartphone]</i>， <i>[!UICONTROL tablet]</i>，或 <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | 指定目標型別的競標調整。 例如，如果關鍵字層級競標為1美元，而智慧型手機的競標調整為50%，則智慧型手機的競標為1.50美元。 依預設，所有目標都會以關鍵字層級的競標來競標。 有效百分比可包括：<ul><li>智慧型手機和平板電腦： -100 （不針對裝置型別競標）以及從–90到900</li><li>案頭：從0到900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | 您偏好顯示廣告或網站連結的裝置型別： <i>[!UICONTROL All]</i> （預設）或 <i>[!UICONTROL Mobile]</i>. 指定「行動」時，網路會嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示廣告或網站連結。 否則，網路會在任何裝置型別上顯示廣告或網站連結。 <b>注意：</b> 網路不保證會在偏好的裝置型別上顯示廣告。 |
| [!UICONTROL Param2] | 如果關鍵字的基礎URL或廣告的標題、說明或基礎URL包含 `{Param2}` 動態替代字串。 長度上限為70個字元，但請注意，您將使用它的廣告元素長度上限（例如，標題1和標題2的組合可能最多為76個字元）。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Param3] | 如果關鍵字的基礎URL或廣告的標題、說明或基礎URL包含 `{Param3}` 動態替代字串。 長度上限為70個字元，但請注意，您將使用它的廣告元素長度上限（例如，標題1和標題2的組合可能最多為76個字元）。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Link Name] | 網站連結文字。 在行銷活動中必須是唯一的。 如果您指定「說明1」和「說明2」，則網站連結文字最多可包含25個單位元組或12個雙位元組字元；否則，網站連結文字最多可包含35個單位元組或17個雙位元組字元。<br><br>[!DNL Microsoft Advertising] 可能會顯示含有說明的2、4或6個增強型網站連結，或是含有廣告的4或6個網站連結以單一列顯示，而不含說明。<br><br>您只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立新的增強型網站連結。 |
| [!UICONTROL Campaign Status] | 行銷活動的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有行銷活動）。 新行銷活動的預設為 [!UICONTROL Active]. 若要刪除作用中或已暫停的行銷活動，請輸入值 `Deleted`. |
| [!UICONTROL Ad Group Status] | 廣告群組的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有廣告群組）。 新廣告群組的預設為 [!UICONTROL Active]. 若要刪除作用中或暫停的廣告群組，請輸入值 `Deleted`. |
| [!UICONTROL Keyword Status] | 關鍵字的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有關鍵字）。 新關鍵字的預設值為 [!UICONTROL Active]. 若要刪除作用中或暫停的關鍵字，請輸入值 `Deleted`. <b>注意：</b> 如果您為具有多個相符型別的關鍵字建立追蹤URL，則每個相符型別的關鍵字狀態都必須相同。 |
| [!UICONTROL Placement Status] | 已棄用 |
| [!UICONTROL Ad Status] | 廣告的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Deleted]</i> （僅限現有廣告）、 <i>[!UICONTROL Disapproved]</i> （不可編輯），或 <i>[!UICONTROL Paused]</i>. 新廣告的預設為 [!UICONTROL Active]. 若要刪除作用中或已暫停的廣告，請輸入值 `Deleted`. |
| [!UICONTROL Target Status] | 動態搜尋目標的狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有目標）。 新目標的預設值為 [!UICONTROL Active]. 若要刪除作用中或暫停的目標，請輸入值 `Deleted`. |
| [!UICONTROL Sitelink Status] | 網站連結的顯示狀態： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted]</i> （僅限現有網站連結）。 新網站連結的預設值為 [!UICONTROL Active]. 若要刪除作用中的網站連結，請輸入值 `Deleted`. |
| [!UICONTROL Location Status] | 位置目標的狀態： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted]</i> （僅限現有位置）。 新位置的預設值為 [!UICONTROL Active]. 若要刪除作用中的位置，請輸入值 `Deleted`. |
| [!UICONTROL Product Group Status] | 產品群組的顯示狀態： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted]</i> （僅限現有產品群組）。 新產品群組的預設值為 [!UICONTROL Active]. 若要刪除使用中的產品群組，請輸入值 `Deleted`. |
| [!UICONTROL Device Target Status] | 行銷活動或廣告群組層級裝置目標的狀態： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted]</i>. 對於新的行銷活動和廣告群組，預設值為 [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | 行銷活動或廣告群組層級RLSA目標或(僅限Google廣告)排除的狀態： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted]</i> （僅限現有目標）。 新目標或排除專案的預設值為 [!UICONTROL Active]. 若要刪除作用中目標或排除專案，請輸入值 `Deleted`. |
| \[廣告商特定標籤分類\] | （以廣告商特定的標籤分類命名，例如稱為顏色的標籤分類的「顏色」）與實體相關聯的指定分類的值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 長度上限為100個字元，值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤相關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值都不區分大小寫。 |
| [!UICONTROL Constraints] | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><b>>限制由子實體繼承，因此您不需要輸入子實體的值，除非您想要覆寫繼承的值。 |
| [!UICONTROL Campaign ID] | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更行銷活動名稱時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」以代表促銷活動。 |
| [!UICONTROL Ad Group ID] | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更行銷活動名稱時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」作為廣告群組。 |
| [!UICONTROL Placement ID] | 已棄用 |
| [!UICONTROL Keyword ID] | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更關鍵字時才需要，除非該列包含a)足以識別關鍵字的屬性欄或b) &quot;[!UICONTROL AMO ID]「。」 |
| [!UICONTROL Ad ID] | <p>可識別現有廣告的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 對於回應式搜尋廣告，編輯或刪除廣告資料需要廣告ID或AMO ID。 對於所有其他實體型別，只有在您變更廣告狀態時才需要AMO ID，除非該列包含a)足夠的廣告屬性欄來識別廣告或b) &quot;[!UICONTROL AMO ID]「。」 不過，如果您不包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。</p><p><b>注意：</b> 如果您編輯a)廣告屬性欄，但現有廣告的「狀態」除外，或b)回應式搜尋廣告的任何資料，並且您既不包括 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，則會建立新廣告，且現有廣告不會變更。 </p> |
| [!UICONTROL Sitelink ID] | 可識別現有網站連結的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄來識別網站連結或b) &quot;[!UICONTROL AMO ID]「。」 不過，如果您同時包含兩項 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]，且屬性欄符合多個網站連結，則只有其中一個網站連結的狀態會變更。</p><p><b>注意：</b> 如果您編輯網站連結屬性欄，但現有網站連結的狀態除外，而且您既不包括 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]，則會建立新的網站連結，而現有的網站連結不會變更。 |
| [!UICONTROL Product Group ID] | 可識別現有產品群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄來識別產品群組或b) &quot;[!UICONTROL AMO ID]「。」 |
| 位置ID | 唯一 [!DNL Microsoft Advertising] 位置目標的識別碼。 若要下載位置清單，請登入 [!DNL Microsoft Advertising] 開發人員入口網站，使用您的 [!DNL Microsoft Advertising] advertising帳戶認證。 只有在您變更或刪除位置目標時才為必要，除非該列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL Target ID] | 可識別現有自動目標的唯一ID。 只有在您變更或刪除自動目標時才為必要，除非該列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL RLSA Target ID] | 可識別現有行銷活動或廣告群組層級RLSA目標的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除目標或排除專案時才需要，除非列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL AMO ID] | （在產生的Bulksheets中）同步實體的Adobe產生的唯一識別碼。 對於回應式搜尋廣告，編輯或刪除廣告時需要AMO ID，除非您包含廣告ID。 若要使用AMO ID編輯所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則編輯或刪除資料時需使用AMO ID。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |
| [!UICONTROL EF Error Message] | （包含在已產生的Bulksheets中以供參考）用來顯示來自廣告網路的錯誤訊息（關於列中的資料）的預留位置；錯誤訊息包含在 [!UICONTROL EF Errors] 檔案。 此值未發佈到廣告網路。 |
| [!UICONTROL SE Error Message] | （包含在已產生的Bulksheets中以供參考）用來顯示來自廣告網路的錯誤訊息（關於列中的資料）的預留位置；錯誤訊息包含在 [!UICONTROL SE Errors] 檔案。 此值未發佈到廣告網路。 |
| [!UICONTROL Exemption Request] | （包含在產生的Bulksheet中以供參考）預留位置，可顯示廣告違反的任何Google廣告原則的名稱和文字。 |
| [!UICONTROL Retail Hash] | (包含於使用進階Campaign Management產生的大量表單中以供參考)英數字元雜湊代碼(例如f9639f40cdf56524b541e5dacf55a991)，表示專案是使用進階(ACM)檢視產生的。 |

<table style="table-layout:auto">

[^1]： [!DNL Excel] 開啟檔案時，會將大型數字轉換為科學記號(例如2.12E+09 for 2115585666)。 若要檢視標準標籤法中的數字，請選取欄中的任何儲存格，然後按一下公式列內的「 」。

## 建立、編輯或刪除每個帳戶元件所需的欄位 {#bulksheet-fields-per-component-microsoft}

以下小節包含與特定帳戶實體相關的欄位。

>[!NOTE]
>
>當欄位不適用於動作時，在欄位中輸入的任何值都會被忽略。

### 行銷活動欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 | 識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Campaign Budget] | 建立行銷活動所需。 | 行銷活動的每日支出限制，無論是否包含貨幣符號和標點符號。 此值會覆寫但不能超過科目預算。 |
| [!UICONTROL Channel Type] | 建立行銷活動所需。 |
| [!UICONTROL Delivery Method] | 可選 |
| [!UICONTROL Campaign Priority] | 建立購物行銷活動所需。 |
| [!UICONTROL Merchant ID] | 建立購物行銷活動所需。 |
| [!UICONTROL Sales Country] | 建立購物行銷活動所需。 |
| [!UICONTROL Product Scope Filter] | （購物行銷活動）選擇性 |
| [!UICONTROL DSA Domain Name] | 建立a) &quot;[!UICONTROL DynamicSearchAds]「或b) 」[!UICONTROL Search]&quot;，當 [!DNL ExperimentId] 元素未設定) |
| [!UICONTROL DSA Domain Language] | 建立a) &quot;[!UICONTROL DynamicSearchAds]「或b) 」[!UICONTROL Search]&quot;，當 [!DNL ExperimentId] 元素未設定) |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Landing Page Suffix] | <p>可選 |
| [!UICONTROL Budget Type] | 建立行銷活動所需。 |
| [!UICONTROL Device] | 可選 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Campaign Status] | 只有在刪除行銷活動時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 只有在您變更行銷活動名稱時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」以代表促銷活動。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 廣告群組欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Group Type] | 建立廣告群組所需。 |
| [!UICONTROL Audience Target Method] | 只有建立對象廣告群組時才需要。 |
| [!UICONTROL Ad Group Start Date] | 可選 |
| [!UICONTROL Ad Group End Date] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Search Network Status] | （僅限搜尋網路上的行銷活動）選擇性 |
| [!UICONTROL Languages] | 可選 |
| [!UICONTROL Device] | 可選 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Ad Group Status] | 只有在刪除廣告群組時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Ad Group ID] | 只有在您變更廣告群組名稱時才為必要，除非該列包含&quot;[!UICONTROL AMO ID]」作為廣告群組。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 關鍵字欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Keyword] | 必填 |
| [!UICONTROL Match Type] | 需要相符型別或關鍵字ID的值，才能編輯或刪除具有多個相符型別的關鍵字。 |
| [!UICONTROL Max CPC] | 可選 |
| [!UICONTROL Base URL/Final URL] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Param1] | 可選 |
| [!UICONTROL Param2] | 可選 |
| [!UICONTROL Keyword Status] | 只有在刪除關鍵字時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Keyword ID] | 只有在編輯或刪除關鍵字時才需要，除非該列包含a)足以識別關鍵字的屬性欄或b) &quot;[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 動態搜尋廣告欄位

>[!NOTE]
>
>建立支援無法使用。

對於此廣告型別，請使用「[!UICONTROL Creative (except RSA)]「」列於 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] 編輯說明時需要。 <b>注意：</b> 對於此廣告型別，變更廣告文案會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Display Path 1] | 編輯欄位時需要。 |
| [!UICONTROL Display Path 2] | 編輯欄位時需要。 |
| [!UICONTROL Creative Type] | 需要建立或編輯產品廣告的狀態。 |
| [!UICONTROL Creative Preferred Devices] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告所需。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄來識別廣告或b) &quot;[!UICONTROL AMO ID].」 不過，如果您不包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 產品（購物）廣告欄位

如需建立購物廣告的詳細資訊，請參閱&quot;[實作 [!DNL Microsoft Advertising] 購物行銷活動](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).」

對於此廣告型別，請使用「[!UICONTROL Creative (except RSA)]「」列於 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Promotion Line] | 可選 |
| [!UICONTROL Base URL/Final URL] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Creative Type] | 需要建立或編輯產品廣告的狀態。 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告所需。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄來識別廣告或b) &quot;[!UICONTROL AMO ID].」 不過，如果您不包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 回應式（多媒體）廣告欄位

對於此廣告型別，請使用「[!UICONTROL Creative (except RSA)]「」列於 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | 對於回應式廣告， [!UICONTROL Ad Title]， [!UICONTROL Ad Title 2]、和 [!UICONTROL Ad Title 3] 是建立廣告的必要欄位，而所有其他廣告標題欄位則是選用欄位。 若要刪除非必要欄位的現有值，請使用值 `[delete]` （包括括弧）。 <b>注意：</b> 對於此廣告型別，變更廣告文案會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] 和 [!UICONTROL Description Line 2] 建立廣告所需，以及 [!UICONTROL Description Line 3] 和 [!UICONTROL Description Line 4] 是選用專案。 <b>注意：</b> 對於此廣告型別，變更廣告文案會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Business Name] | 建立或刪除廣告的必要條件。 |
| [!UICONTROL Call To Action] | 建立廣告所需。 |
| [!UICONTROL Call To Action Language] | 建立廣告所需。 |
| [!UICONTROL Base URL/Final URL] | 建立廣告所需。 |
| [!UICONTROL Creative Type] | 選填。 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告所需。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄來識別廣告或b) &quot;[!UICONTROL AMO ID].」 不過，如果您不包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 回應式搜尋廣告欄位

對於此廣告型別，請使用「[!UICONTROL Responsive Search Ad]「」列於 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | 對於回應式搜尋廣告， [!UICONTROL Ad Title]， [!UICONTROL Ad Title 2]、和 [!UICONTROL Ad Title 3] 是建立廣告的必要欄位，而所有其他廣告標題欄位則是選用欄位。 若要刪除非必要欄位的現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | 可選 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | 對於回應式搜尋廣告， [!UICONTROL Description Line 1] 和 [!UICONTROL Description Line 2] 建立廣告所必需，以及 [!UICONTROL Description Line 3] 和 [!UICONTROL Description Line 4] 是選用專案。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | 可選 |
| [!UICONTROL Display Path 1] | 可選 |
| [!UICONTROL Display Path 2] | 可選 |
| [!UICONTROL Base URL/Final URL] | 建立廣告所需。 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Creative Type] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告所需。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 編輯或刪除廣告的必要條件，除非該列包含&quot;[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非您包含廣告ID，否則編輯或刪除廣告的必要專案。 |

### 文字廣告欄位

對於此廣告型別，請使用「[!UICONTROL Creative (except RSA)]「」列於 [!UICONTROL Download Bulksheet] 對話方塊。

>[!NOTE]
>
>已棄用展開的文字廣告。 您只能刪除現有的文字廣告。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | 唯讀 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] 唯讀 |
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
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才為必要，除非該列包含&quot;[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非您包含廣告ID，否則需要編輯或刪除資料。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 動態搜尋目標（自動鎖定目標）欄位

>[!NOTE]
>
>建立支援無法使用。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
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
| [!UICONTROL Target ID] | 只有在您變更或刪除自動目標時才為必要，除非該列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 購物產品群組欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Match Type] | 建立產品群組時需要。 |
| [!UICONTROL Max CPC] | 建立產品群組時需要。 |
| [!UICONTROL Parent Product Groupings] | 必填 |
| [!UICONTROL Product Grouping] | 必填 |
| [!UICONTROL Partition Type] | 建立產品群組時需要。 |
| [!UICONTROL Base URL/Final URL] | 必填 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Product Group Status] | 只有在刪除產品群組時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Product Group ID] | 只有在您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄來識別產品群組或b) &quot;[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 行銷活動層級網站連結欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
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
| [!UICONTROL Sitelink ID] | 只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄來識別網站連結或b) &quot;[!UICONTROL AMO ID].」 不過，如果您同時包含兩項 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]  且屬性欄符合多個網站連結，則只有其中一個網站連結的狀態會變更。<br><br><b>注意：</b> 如果您編輯網站連結屬性欄，但現有網站連結的狀態除外，而且您未包含 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]，則會建立新的網站連結，而現有的網站連結不會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父實體ID，否則編輯或刪除資料時需要。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 位置目標欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Location] | 必填 |
| [!UICONTROL Location Type] | 建立目標所需 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Location Status] | 只有在刪除位置目標時才需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL AMO ID] | 除非包含行銷活動ID，否則需要編輯或刪除資料。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 行銷活動層級和廣告群組層級裝置目標欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Device] | 刪除裝置目標時需要。 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Ad Group Name] | 廣告群組層級裝置目標的必要專案。 不適用於行銷活動層級的裝置目標。 |
| [!UICONTROL Device Target Status] | 只有在刪除裝置目標時才需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 選用；僅適用於廣告群組層級裝置目標。 |
| [!UICONTROL AMO ID] | 除非您包含裝置目標ID，否則必須編輯或刪除資料。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 行銷活動層級和廣告群組層級RLSA目標欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-microsoft).」

| 欄位 | 必填？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含「」，否則為必要[!UICONTROL AMO ID]」代表實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 廣告群組層級目標的必要專案。 不適用於行銷活動層級目標。 |
| [!UICONTROL Audience] | 建立新目標時需要。 |
| [!UICONTROL Target Type] | 可選 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL RLSA Target Status] | 刪除目標時需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 選用；僅適用於廣告群組層級目標。 |
| [!UICONTROL RLSA Target ID] | 只有在您變更或刪除目標時才為必要，除非該列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL AMO ID] | 除非包含RLSA目標ID，否則必須編輯或刪除資料。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [可在Bulksheets中執行的作業](bulksheet-operations.md)
>* [支援的Bulksheet檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>* [的點選追蹤格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)
