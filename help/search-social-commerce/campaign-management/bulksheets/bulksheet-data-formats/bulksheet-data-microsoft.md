---
title: 必要的大量表單資料 [!DNL Microsoft Advertising] 帳戶
description: 參考Bulksheets中必要的標題欄位和資料欄位 [!DNL Microsoft Advertising] 帳戶。
source-git-commit: f7ac5c69f96582d7f9a442a05c333baecc2215df
workflow-type: tm+mt
source-wordcount: '5147'
ht-degree: 0%

---

# 附錄 — 必要的大量表單資料 [!DNL Microsoft Advertising] 帳戶

若要建立和更新 [!DNL Microsoft Advertising] 大量行銷活動資料，您可以使用特別格式化的搜尋、社交和商務大量表單檔案 [!DNL Microsoft Advertising] 帳戶。 您可以) [產生現有帳號的大量工作表檔案](../bulksheet-download.md) (b)手動建立（請參閱「 」）[支援的Bulksheet檔案格式](bulksheet-file-formats.md)」以取得受支援檔案格式的一般資訊)。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## 所有可用資料欄位

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| 欄位 | 說明 |
|----|----|
| Platform | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的「AMO ID」，否則為必要。 |
| 帳戶名稱 | 可識別廣告網路帳戶的唯一名稱。 除非每一列包含實體的「AMO ID」，否則為必要。 |
| 行銷活動名稱 | 識別帳戶促銷活動的唯一名稱。 長度上限為128個字元。 |
| 行銷活動預算 | 每日或每月行銷活動預算，無論是否有貨幣符號和標點符號。 不得少於0.05。 |
| 頻道型別 | 行銷活動鎖定的頻道型別： <i>對象</i>， <i>DynamicSearchAds</i>， <i>搜尋</i>，或 <i>購物</i>. |
| 傳遞方法 | （僅具有每日預算的行銷活動）每天顯示行銷活動廣告的速度如何：<ul><li><i>標準（分散式）</i> （新行銷活動的預設）：將廣告印象分散在一天當中。</li><li><i>加速：</i> 在達到預算之前，儘可能多地顯示您的廣告。 因此，您的廣告可能不會在當天稍後出現。</li></ul> |
| 行銷活動優先順序 | （僅限購物行銷活動）當多個行銷活動廣告相同產品時，使用行銷活動的優先順序： <i>低</i> （新行銷活動的預設值）， <i>中</i>，或 <i>高</i>.<br><br>當相同產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則符合最高競價的行銷活動條件。 |
| 商家ID | （僅限連結至商家摘要的購物行銷活動和對象行銷活動）其產品用於行銷活動的商家帳戶的客戶ID。 |
| 銷售國家 | （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動產品銷售的國家/地區。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。 |
| 產品範圍篩選器 | （僅使用購物網路的行銷活動）您的商家帳戶中的產品，可以針對行銷活動建立產品廣告。 您可以使用格式dimension=attribute，輸入最多七個產品維度和屬性組合，以篩選產品。 使用「>>」分隔符號分隔多個篩選器。 如需可用產品維度的清單，請參閱&quot;[購物行銷活動產品篩選器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).」<br><br> 範例：「`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| DSA網域名稱 | （a型別的行銷活動） 」<i>DynamicSearchAds</i>「或b) 」<i>搜尋</i>&quot;當ExperimentId元素未設定時)動態搜尋廣告的目標網站網域名稱。 長度上限為2,048個字元。 如果網域名稱包含 `www`，已裁剪且未使用。<br><br>對於現有行銷活動，您無法編輯網域，但必須包含它以更新其他屬性。 |
| DSA網域語言 | （a型別的行銷活動） 」<i>DynamicSearchAds</i>「或b) 」<i>搜尋</i>&quot;未設定ExperimentId元素時)動態搜尋廣告的目標網站頁面語言。 支援的網域語言為荷蘭文、英文、法文、德文、義大利文、西班牙文和瑞典文。<br><br>對於現有的行銷活動，您無法編輯語言，但必須包含它以更新其他屬性。 |
| 廣告群組名稱 | 識別廣告群組的唯一名稱。 長度上限為128個字元。 結尾的空白字元不會儲存（例如，「廣告群組1」會儲存為「廣告群組1」）。 |
| 廣告群組型別 | （搜尋網路上的行銷活動；現有廣告群組的唯讀）廣告群組型別： <i>對象</i> （僅適用於對象行銷活動）， <i>搜尋動態</i> （僅適用於動態搜尋廣告）和 <i>Search Standard</i> （僅適用於回應式搜尋廣告和現有的擴充文字廣告）。 某些行銷活動型別可包含多種廣告群組型別。 |
| 關鍵字 | （僅限搜尋網路上的促銷活動）關鍵字字串。 長度上限為50個字元。<br><br><b>附註：</b><ul><li>若要在廣告群組或行銷活動層級排除關鍵字，請將「比對型別」設定為 `Negative`. 如果列包含廣告群組名稱，則會排除廣告群組的關鍵字。 如果列不包含廣告群組名稱，則會在整個行銷活動中排除關鍵字。</li><li>變更Microsoft Advertising關鍵字會刪除現有關鍵字，並使用新關鍵字ID建立新關鍵字。 但是，變更相符型別並不會刪除現有關鍵字。</li></ul> |
| 位置 | 已棄用 |
| 對象 | 行銷活動或廣告群組的搜尋廣告(RLSA)目標對象的再行銷清單。 |
| 目標型別 | （僅限RLSA目標）目標型別： <i>包含</i> 或 <i>排除</i>. |
| 自動鎖定目標運算式 | 廣告群組的動態搜尋目標。 針對所有目標，請使用「所有網頁」。<br><br>若要鎖定最多三個動態搜尋條件，請使用格式 `<category>=<target>`，其中 &lt;category> 可包含下列任何類別。 使用「」聯結個別類別的多個目標`[blank space] and [blank space]`」並使用「」聯結多個類別`[blank space] and [blank space]`「。<br><ul><li><i>類別：</i> 若要針對具有特定Google內容類別的索引頁面顯示動態搜尋廣告。</li><li><i>URL：</i> 顯示具有特定URL之索引頁面的動態搜尋廣告，其中值可能包含在URL內的任何位置。</li><li><i>頁面標題：</i> 顯示索引頁面的動態搜尋廣告，並在頁面標題中顯示特定文字。</li><li><i>頁面內容：</i> 顯示具有特定內容之索引頁面的動態搜尋廣告。</li></ul>範例： url=shoes.example.com和page title=footwear<br>範例：所有網頁 |
| 位置 | 為行銷活動或廣告群組放置廣告的地理位置；值不區分大小寫。 如果您未輸入任何促銷活動或廣告群組的值，則會鎖定所有位置。 若要鎖定特定位置，請使用Microsoft Advertising位置代碼格式來輸入位置。 若要下載位置清單，請使用您的Microsoft Advertising帳戶憑證登入Microsoft Advertising開發人員入口網站。 <b>注意：</b> 若要排除位置，請在位置代碼前加上減號(`-`)，例如 `-United States`. |
| 位置型別 | 位置型別，例如「城市」、「國家/地區」、「MetroArea」、「PostalCode」和「State」。 若要下載位置清單，請使用您的Microsoft Advertising帳戶憑證登入Microsoft Advertising開發人員入口網站。 |
| 相符型別 | （僅限搜尋網路上的促銷活動）關鍵字比對選項。 這可能包括動態搜尋目標或產品群組的關鍵字比對選項。 值包括： <i>廣泛</i> （新關鍵字的預設值）， <i>精確</i>， <i>片語</i>， <i>內容</i> （當廣告群組鎖定內容網路時，自動設定關鍵字）， <i>負面</i> （在內容網路上排除關鍵字）， <i>動態廣告目標</i> （新動態搜尋目標的預設值）、 <i>產品群組</i> （新產品群組的預設值），或 <i>負面產品群組</i> （排除產品群組）。  需要相符型別或關鍵字ID的值，才能編輯或刪除具有多個相符型別的關鍵字。<br><br>若為Broad Match修飾詞，請選擇「Broad」並插入 `+` 在必要的關鍵字內的任何字詞之前(例如&quot;`+red +shoes`」以同時要求「紅色」和「鞋子」)。<br><br>變更Microsoft Advertising關鍵字的相符型別不會刪除現有關鍵字。 |
| 最大CPC | （搜尋網路上的行銷活動）最高每次點按成本(CPC)，這是根據關鍵字、產品群組或動態搜尋目標（無論有否貨幣符號和標點符號）支付廣告點按的最高金額。  對於最佳化產品組合中的現有關鍵字和產品群組記錄，更新僅在一天內有效，並在下一個最佳化週期中被覆寫。 <b>注意：</b> 您無法設定負關鍵字的競標。 |
| 最大內容CPC | （唯讀，適用於在內容網路之前建立的CPC行銷活動，但僅於2017年淘汰）最高每次點按內容成本(CPC)，這是從顯示網路網站為廣告點按付費的最高金額，無論有否貨幣符號和標點符號。 |
| 對象目標方法 | （對象廣告群組）是否：<ul><li><i>目標與競標：</i> 只向與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。</li><li><i>僅限競標：</i>即使未與目標對象相關聯的人，只要他們滿足其他廣告群組層級目標，也能顯示廣告。</li></ul> 不過，您可以針對特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。 |
| 父級產品群組 | 任何父級產品群組的階層。<br><br>範例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| 產品群組 | 產品群組（例如「brand=acme」或「所有產品」）。<br><br><b>附註：</b><ul><li>當指定的產品群組不存在於父產品群組階層中時，Search、Social和Commerce會建立階層中所需的任何部分。</li><li>每當您在Google購物行銷活動中建立廣告群組，且預設競標設為廣告群組預設競標時，「搜尋、Social和商務」都會自動建立「所有產品」群組。 Search、Social和Commerce會在產品群組階層的每個層級，自動建立具有廣告群組預設競標的「其他一切」群組。 您仍然可以明確建立這些預設群組，並排除它們或變更其競標。</li><li>每個廣告群組最多可包含八層產品群組，包括「所有產品」和其他七層。</li></ul> |
| 資料分割型別 | 產品群組的磁碟分割型別： <i>細分</i> （當具有子產品群組時）或 <i>單位</i> （當它沒有子產品群組時）。 |
| 廣告標題，廣告標題2-15 | （僅限擴充文字廣告、多媒體廣告、回應式廣告和回應式搜尋廣告）廣告的頭條。 每個廣告標題欄位的長度上限為30個字元或15個雙位元組字元，包括任何動態文字(例如關鍵字的值、 `{Param2}` 和 `{Param3}` 動態替代變數和ad customizers)。<br><br> 對於回應式搜尋廣告，請使用以下格式插入廣告自訂器，其中「預設文字」是當您的摘要檔案未包含有效值時要插入的選用值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>對於展開的文字廣告，「廣告標題」和「廣告標題2」為必填，「廣告標題3」為選用。 Microsoft Advertising已於2022年8月取代擴充文字廣告，您現在只能報告和刪除這些廣告。<br><br>對於多媒體廣告、回應式廣告和回應式搜尋廣告，廣告標題、廣告標題2和廣告標題3為必填，所有其他廣告標題欄位為選用。<br><br>若要刪除非必要欄位的現有值，請使用值 `[delete]` （包括括弧）。<br><br>對於所有廣告型別（展開的文字廣告除外），變更廣告副本會刪除現有廣告，並建立具有相同屬性的新廣告。 |
| 廣告標題1-15位置 | （僅限回應式搜尋廣告；選用）釘選對應廣告標題的位置： `[null]` （無值，因此廣告標題適用於所有職位）、1、2或3。 例如，如果「廣告標題位置」的值為1，則「廣告標題」將僅出現在「位置1」中。 依預設，所有廣告標題均為Null （沒有值）。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。<br><br><b>注意：</b> 您可以將多個廣告標題釘選至相同位置。 廣告網路將使用已釘選至該位置的其中一個廣告標題。 釘選到位置3的標題可能不會與廣告一起顯示。 |
| 說明第1-4行 | （僅限文字廣告、動態搜尋廣告、多媒體廣告、回應式廣告、回應式搜尋廣告，以及增強型促銷活動層級的網站連結）廣告內文或網站連結。<br><br>對於網站連結，可選擇同時使用說明第1行與說明第2行，以包含廣告網路可能顯示在連結文字下方的額外文字。 每個說明欄位最多可包含35個單位元組或17個雙位元組字元。<br><br>對於廣告，每個說明欄位的長度上限為90個字元或45個雙位元組字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。<br><br>對於回應式搜尋廣告，請使用以下格式插入廣告自訂器，其中預設文字是當您的摘要檔案未包含有效值時要插入的可選值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>對於文字廣告和動態搜尋廣告，「說明第1行」為必填，「說明第2行」為選用。<br><br>對於多媒體廣告、回應式廣告和回應式搜尋廣告，「說明第1行」和「說明第2行」為必填，「說明第3行」和「說明第4行」為選用。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。<br><br><b>附註：</b><ul><li>（標準文字廣告）組合的標題和文字必須至少有三個字。</li><li>（展開文字廣告）此欄位可選擇性地包含{Param2}和{Param3}動態替代變數。 如果超過300個單位元組，廣告文字的長度上限為300個單位元組或150個雙位元組字元。 Microsoft Advertising已於2022年8月取代擴充文字廣告，您現在只能報告和刪除這些廣告。</li><li>（動態搜尋廣告）不允許動態替代文字。</li><li>對於所有廣告型別（展開的文字廣告除外），變更廣告副本將會刪除現有廣告並建立新廣告。</li></ul> |
| 說明第1-4行位置 | （僅限回應式搜尋廣告；選用）釘選對應說明的位置： `[null]` （無值，因此說明適用於所有職位）、1、2或3。 例如，如果「描述1位置」的值為1，則「描述1」將僅出現在「位置1」中。 依預設，不會將任何說明釘選到位置。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。<br><br><b>注意：</b> 您可以將多個說明釘選到相同位置。 廣告網路將使用已釘選至位置的其中一個說明。 釘選到位置2的說明可能不會與廣告一起顯示。 |
| 公司名稱 | （僅限多媒體廣告）企業名稱，最多25個字元。 |
| 促銷行 | （僅限產品清單廣告）搜尋結果中產品清單內含的唯一促銷明細行（例如「立即免運費！」）。 長度上限為45個字元。<br><br>視廣告在頁面上的出現位置而定，促銷明細行可能會出現在與廣告相關的不同位置（例如廣告下方）。 |
| 顯示URL | 廣告中包含的URL。<br><br>對於展開的動態搜尋廣告，廣告網路會從網站網域動態產生此值，而您不需要輸入值。<br><br>對於展開的文字廣告和回應式搜尋廣告，您不需要輸入值。 系統會自動從最終URL的網域中擷取顯示URL。 您可以選擇使用「路徑1」和「路徑2」欄位自訂URL。<br><br><b>附註：</b><ul><li>（具有最終URL的帳戶）顯示URL和最終URL中的網域名稱必須相符。</li><li>Microsoft Advertising已於2022年8月取代擴充文字廣告，您現在只能報告和刪除這些廣告。</li></ul> |
| 顯示路徑1 | （僅限展開的文字廣告、動態搜尋廣告和回應式搜尋廣告）新增至顯示URL的文字，會自動從最終URL擷取。 URL中的每個路徑前面都有一個正斜線(/)。 路徑不能包含正斜線(/)或新行(\n)字元。 每個路徑的長度上限為15個字元或7個雙位元組字元。<br><br>若要插入廣告自訂程式，請使用下列格式，其中「預設文字」是當摘要檔案未包含有效值時要插入的選用值： `{CUSTOMIZER.Attribute name:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`<br><br>例如，如果顯示路徑1是&quot;deals&quot;，則顯示URL將是 &lt;display url=&quot;&quot;>/deals，例如www.example.com/deals。<br><br>Microsoft Advertising已於2022年8月取代擴充文字廣告，您現在只能報告和刪除這些廣告。 |
| 顯示路徑1 | （僅限展開的文字廣告、動態搜尋廣告和回應式搜尋廣告）其他顯示路徑；請參閱顯示路徑1的專案。<br><br>範例：如果顯示路徑1是&quot;deals&quot;，而顯示路徑2是&quot;local&quot;，則顯示URL會是&lt;<i>顯示URL</i>>/deals/local，例如www.example.com/deals/local。 |
| 開始日期 | （僅限增強型網站連結）對網站連結發出投標的第一個日期，採用廣告商的時區格式及下列格式之一： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新增強型網站連結的預設值為當天。 <b>注意：</b> 新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。 |
| 結束日期 | 網站連結可以和廣告一起出現的最後日期、以廣告商的時區及以下格式之一顯示：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 如果是新的網站連結，預設值為 `[blank]` （亦即，無結束日期）。 |
| 行動號召 | 要包含在廣告中的行動號召。 請參閱 [API參考以取得可能值的清單](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction)，但請在Bulksheets中輸入多個單字的動作呼叫（例如「Bet Now」而非「BetNow」）。 |
| 行動號召語言 | 行動號召選項的語言。 請參閱 [API參考以取得可能的語言清單](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| 基本URL/最終URL | 搜尋引擎使用者按一下您的廣告時，系統會將他們帶往的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 關鍵字層級的基礎/最終URL會覆寫廣告層級和更高層級的基礎/最終URL。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| 目的地URL | （包含在已產生的Bulksheet中以供參考；未張貼至搜尋引擎）對於具有目的地URL的帳戶，此URL會將廣告連結至廣告商網站上的基本URL/登陸頁面（有時透過另一個網站來追蹤點選，然後將使用者重新導向到登陸頁面）。 其中包含為Search， Social， &amp; Commerce促銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，這會根據帳戶設定和促銷活動設定中的追蹤引數。 如果您已附加搜尋引擎特定引數，這些引數可能會取代為搜尋、社交和商務的同等引數。<br><br>若為具有最終URL的帳戶，此欄會顯示與「基本URL/最終URL」欄相同的值。 |
| 自訂URL引數 | 要取代的資料 `{custom_code}` 變數納入搜尋帳戶或促銷活動設定的追蹤引數時，使用動態變數。 若要在追蹤URL中插入自訂值，您必須使用「產生追蹤URL」選項上傳大量表單檔案。 |
| 創意型別 | 廣告格式： <i>動態搜尋廣告</i>， <i>展開的文字廣告</i>， <i>展開的動態搜尋廣告</i>， <i>多媒體廣告</i>， <i>產品廣告</i> （購物廣告），或 <i>回應式搜尋廣告</i>，或 <i>文字廣告</i>. 新廣告的預設為 <i>文字廣告</i>. |
| 廣告群組開始日期 | 可對廣告群組下標的第一天（在廣告商的時區中及以下格式之一）：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 若為新廣告群組，預設值為目前日期。 |
| 廣告群組結束日期 | 可對廣告群組下標的最後日期（在廣告商的時區中且以下列格式之一）：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 如果是新廣告群組，預設值為 [空白] （亦即，無結束日期）。 |
| 追蹤範本 | （選用）追蹤範本，可指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。 最精細層級的追蹤範本（以關鍵字作為最精細的層級）會覆寫所有較高層級的值。<br><br>針對Adobe廣告轉換追蹤，此追蹤會在行銷活動設定包含「EF重新導向」和「自動上傳」時套用，當您儲存記錄時，Search、Social和Commerce會自動附加重新導向和追蹤代碼。<br><br>針對協力廠商重新導向與追蹤，請輸入值。<br><br>如需可指出追蹤範本中最終URL的引數清單，請參閱Microsoft Advertising檔案。<br><br> 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| 登陸頁面尾碼 | 要附加至最終URL結尾以追蹤資訊的任何引數。 範例： `param2=value1&param3=value2`<br><br>請參閱「[的點選追蹤格式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).」<br><br>較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同的追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用Microsoft Advertising編輯器。 |
| 搜尋網路狀態 | 是否要將廣告群組的廣告放置在「搜尋網路」的各種元素上：<ul><li><i>全部：</i> 在所有Bing搜尋網路和聯合搜尋合作夥伴上刊登廣告。</li><li><i>OwnedAndOperatedOnly：</i>只在Bing和Yahoo！上刊登廣告 網站。</li><li><i>SyndicatedSearchOnly：</i> 只在Bing和Yahoo！上刊登廣告 財團搜尋合作夥伴。</li><li><i>關閉：</i> 僅將廣告放在內容網路（而非搜尋網路）上。</li></ul> 對於新廣告群組，預設值為「開啟」。 |
| 內容網路狀態 | 已棄用 |
| 語言 | 廣告群組中廣告的目標語言：英文、法文、芬蘭文、德文、挪威文、西班牙文或瑞典文。 新行銷活動的預設為英文。<br><br>此設定會決定您的廣告可以顯示的國家和區域。 請務必選擇與行銷活動位置目標相容的語言。 |
| 預算型別 | 預算是否為 <i>每日</i> （預設）或 <i>每月</i>.<br><br>備註：如果您將促銷活動指定至最佳化的投資組合，此值會自動設為「每日」。 |
| 裝置 | 在行銷活動或廣告群組層級進行競標調整的裝置型別： <i>智慧型手機</i>， <i>平板電腦</i>，或 <i>案頭</i>. |
| 競標調整 | 指定目標型別的競標調整。 例如，如果關鍵字層級競標為1美元，而智慧型手機的競標調整為50%，則智慧型手機的競標為1.50美元。 依預設，所有目標都會以關鍵字層級的競標來競標。 有效百分比可包括：<ul><li>智慧型手機和平板電腦： -100 （不針對裝置型別競標）以及從–90到900</li><li>案頭：從0到900</li></ul> |
| 創意偏好裝置 | 您偏好顯示廣告或網站連結的裝置型別： <i>全部</i> （預設）或 <i>行動</i>. 指定「行動」時，網路會嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示廣告或網站連結。 否則，網路會在任何裝置型別上顯示廣告或網站連結。 <b>注意：</b> 網路不保證會在偏好的裝置型別上顯示廣告。 |
| Param2 | 如果關鍵字的基礎URL或廣告的標題、說明或基礎URL包含 `{Param2}` 動態替代字串。 長度上限為70個字元，但請注意，您將使用它的廣告元素長度上限（例如，標題1和標題2的組合可能最多為76個字元）。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| Param3 | 如果關鍵字的基礎URL或廣告的標題、說明或基礎URL包含 `{Param3}` 動態替代字串。 長度上限為70個字元，但請注意，您將使用它的廣告元素長度上限（例如，標題1和標題2的組合可能最多為76個字元）。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| 連結名稱 | 網站連結文字。 在行銷活動中必須是唯一的。 如果您指定「說明1」和「說明2」，則網站連結文字最多可包含25個單位元組或12個雙位元組字元；否則，網站連結文字最多可包含35個單位元組或17個雙位元組字元。<br><br>Microsoft Advertising可能會顯示兩個、四個或六個具有說明的增強型網站連結，或是包含廣告且沒有說明的單一列中有四個或六個網站連結。<br><br>您只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立新的增強型網站連結。 |
| 行銷活動狀態 | 行銷活動的顯示狀態： <i>作用中</i>， <i>已暫停</i>，或 <i>已刪除</i> （僅限現有行銷活動）。 新行銷活動的預設值為「作用中」。 若要刪除作用中或已暫停的行銷活動，請輸入值 `Deleted`. |
| 廣告群組狀態 | 廣告群組的顯示狀態： <i>作用中</i>， <i>已暫停</i>，或 <i>已刪除</i> （僅限現有廣告群組）。 新廣告群組的預設值為「作用中」。 若要刪除作用中或暫停的廣告群組，請輸入值 `Deleted`. |
| 關鍵字狀態 | 關鍵字的顯示狀態： <i>作用中</i>， <i>已暫停</i>，或 <i>已刪除</i> （僅限現有關鍵字）。 新關鍵字的預設值為「作用中」。 若要刪除作用中或暫停的關鍵字，請輸入值 `Deleted`. <b>注意：</b> 如果您為具有多個相符型別的關鍵字建立追蹤URL，則每個相符型別的關鍵字狀態都必須相同。 |
| 位置狀態 | 已棄用 |
| 廣告狀態 | 廣告的顯示狀態： <i>作用中</i>， <i>已刪除</i> （僅限現有廣告）、 <i>未核准</i> （不可編輯），或 <i>已暫停</i>. 新廣告的預設值為「作用中」。 若要刪除作用中或已暫停的廣告，請輸入值 `Deleted`. |
| 目標狀態 | 動態搜尋目標的狀態： <i>作用中</i>， <i>已暫停</i>，或 <i>已刪除</i> （僅限現有目標）。 新目標的預設值為「作用中」。 若要刪除作用中或暫停的目標，請輸入值 `Deleted`. |
| 網站連結狀態 | 網站連結的顯示狀態： <i>作用中</i> 或 <i>已刪除</i> （僅限現有網站連結）。 新網站連結的預設值為「作用中」。 若要刪除作用中的網站連結，請輸入值 `Deleted`. |
| 位置狀態 | 位置目標的狀態： <i>作用中</i> 或 <i>已刪除</i> （僅限現有位置）。 新位置的預設值為「作用中」。 若要刪除作用中的位置，請輸入值 `Deleted`. |
| 產品群組狀態 | 產品群組的顯示狀態： <i>作用中</i> 或 <i>已刪除</i> （僅限現有產品群組）。 新產品群組的預設值為「作用中」。 若要刪除使用中的產品群組，請輸入值 `Deleted`. |
| 裝置目標狀態 | 行銷活動或廣告群組層級裝置目標的狀態： <i>作用中</i> 或 <i>已刪除</i>. 對於新的行銷活動和廣告群組，預設值為「作用中」。 |
| RLSA目標狀態 | 行銷活動或廣告群組層級RLSA目標或(僅限Google廣告)排除的狀態： <i>作用中</i> 或 <i>已刪除</i> （僅限現有目標）。 新目標或排除專案的預設值為「作用中」。 若要刪除作用中目標或排除專案，請輸入值 `Deleted`. |
| \[廣告商特定標籤分類\] | （以廣告商特定的標籤分類命名，例如稱為顏色的標籤分類的「顏色」）與實體相關聯的指定分類的值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 長度上限為100個字元，值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤相關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值都不區分大小寫。 |
| 限制 | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><b>>限制由子實體繼承，因此您不需要輸入子實體的值，除非您想要覆寫繼承的值。 |
| 行銷活動ID | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更促銷活動名稱時才需要，除非該列包含促銷活動的「AMO ID」。 |
| 廣告群組識別碼 | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更行銷活動名稱時才需要，除非該列包含廣告群組的「AMO ID」。 |
| 刊登ID | 已棄用 |
| 關鍵字ID | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更關鍵字時才需要，除非該列包含a)足夠的屬性欄來識別關鍵字或b)「AMO ID」。 |
| 廣告ID | <p>可識別現有廣告的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 對於回應式搜尋廣告，編輯或刪除廣告資料需要廣告ID或AMO ID。 對於所有其他實體型別，只有在您變更廣告狀態時才需要AMO ID，除非該列包含a)足夠的廣告屬性欄來識別廣告，或b)「AMO ID」。 不過，如果您既不包含廣告ID也不包含AMO ID，而且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。</p><p><b>注意：</b> 如果您編輯a)廣告屬性欄，但現有廣告的「狀態」除外，或b)回應式搜尋廣告的任何資料，且您既未包含廣告ID也未包含AMO ID，則會建立新廣告，且現有廣告不會變更。 </p> |
| 網站連結ID | 可識別現有網站連結的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄來識別網站連結或b)「AMO ID」。 不過，如果您未包含網站連結廣告ID或AMO ID，而且屬性欄符合多個網站連結，則只有其中一個網站連結的狀態會變更。</p><p><b>注意：</b> 如果您編輯現有網站連結的網站連結屬性欄（「狀態」除外），而且您既不包含網站連結ID也不包含AMO ID，則會建立新的網站連結，且不會變更現有的網站連結。 |
| 產品群組識別碼 | 可識別現有產品群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄來識別產品群組或b)「AMO ID」。 |
| 位置ID | 位置目標的唯一Microsoft廣告識別碼。 若要下載位置清單，請使用您的Microsoft Advertising帳戶憑證登入Microsoft Advertising開發人員入口網站。 只有在您變更或刪除位置目標時才需要，除非該列包含目標的「AMO ID」。 |
| 目標ID | 可識別現有自動目標的唯一ID。 只有在您變更或刪除自動目標時才需要，除非該列包含目標的「AMO ID」。 |
| RLSA目標ID | 可識別現有行銷活動或廣告群組層級RLSA目標的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除目標或排除專案時才需要，除非列包含目標的「AMO ID」。 |
| AMO ID | （在產生的Bulksheets中）同步實體的Adobe產生的唯一識別碼。 對於回應式搜尋廣告，編輯或刪除廣告時需要AMO ID，除非您包含廣告ID。 若要使用AMO ID編輯所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則編輯或刪除資料時需使用AMO ID。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |
| EF錯誤訊息 | （包含在產生的大量表單中以供參考）用來顯示來自廣告網路的錯誤訊息的預留位置，這些訊息與資料列中的資料有關；錯誤訊息包含在EF錯誤檔案中。 此值未發佈到廣告網路。 |
| SE錯誤訊息 | （包含在已產生的Bulksheets中以供參考）用來顯示來自廣告網路的錯誤訊息的預留位置，這些錯誤訊息與資料列中的資料有關；錯誤訊息包含在SE錯誤檔案中。 此值未發佈到廣告網路。 |
| 劐免要求 | （包含在產生的Bulksheet中以供參考）預留位置，可顯示廣告違反的任何Google廣告原則的名稱和文字。 |
| 零售雜湊 | (包含於使用進階Campaign Management產生的大量表單中以供參考)英數字元雜湊代碼(例如f9639f40cdf56524b541e5dacf55a991)，表示專案是使用進階(ACM)檢視產生的。 |

<table style="table-layout:auto">

<!-- EDIT ALL -- Copied from Google page -->

<!-- 

## Fields required to create, edit, or delete each account component

### Campaign fields

Campaign Name
Campaign Budget
Campaign Status
Delivery Method
Device OS Targets (Google Adwords)
Device Targets
Languages
Mobile Carriers (Google Adwords)
Networks
Tracking Template
Channel Type
Campaign Priority
Merchant ID
Sales Country
Product Scope Filter
Audience Target Method
DSA Domain Name
DSA Domain Language
Landing Page Suffix
Label Classification

### Ad group fields

Campaign Name
Ad Group Name
Ad Group Type
Networks
Ad Group Status
Max CPC
Max Content CPC
Tracking Template
Audience Target Method
Label Classification


## Keyword fields

Campaign Name
Ad Group Name
Keyword Status
Max CPC
Tracking Template
URLs (Base URL/Final URL, Destination URL)
Exemption Request (Google Adwords)
First Page Bid
Keyword
Match Type
Param1
Param2
Quality Score
Custom URL Param
Label Classification


### Text/Product ad fields

Uses "Creative (except RSA)" row in Download Bulksheet dialog

### Dynamic search ad fields

Note: Create support not available

### Multimedia/Responsive ad fields

### Responsive search ad fields

Uses "Responsive Search Ad" row in Download Bulksheet dialog

### Dynamic search target (auto target) fields
Note: Create support not available

### Shopping product group fields

### Campaign-level sitelink fields

### Location Target fields

### Device Target fields

### RLSA Target

-->

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [可在Bulksheets中執行的作業](bulksheet-operations.md)
>* [支援的Bulksheet檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>* [的點選追蹤格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)
