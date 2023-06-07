---
title: 必要的大量表單資料 [!DNL Google Ads] 帳戶
description: 參考Bulksheets中必要的標題欄位和資料欄位 [!DNL Google Ads] 帳戶。
source-git-commit: 05a3424b67d084dbb664321c7a6ada0f99a840b2
workflow-type: tm+mt
source-wordcount: '6628'
ht-degree: 0%

---

# 附錄 — 必要的大量表單資料 [!DNL Google Ads] 帳戶

若要建立和更新 [!DNL Google Ads] 大量行銷活動資料，您可以使用特別格式化的搜尋、社交和商務大量表單檔案 [!DNL Google Ads] 帳戶。 您可以) [產生現有帳號的大量工作表檔案](../bulksheet-download.md) (b)手動建立（請參閱「 」）[支援的Bulksheet檔案格式](bulksheet-file-formats.md)」以取得受支援檔案格式的一般資訊)。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## 所有可用資料欄位

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| 欄位 | 說明 |
| ---- | ---- |
| Platform | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的「AMO ID」，否則為必要。 |
| 帳戶名稱 | 可識別廣告網路帳戶的唯一名稱。 除非每一列包含實體的「AMO ID」，否則為必要。 |
| 行銷活動名稱 | 識別帳戶促銷活動的唯一名稱。 |
| 行銷活動預算 | 行銷活動的每日支出限制，無論是否包含貨幣符號和標點符號。 此值會覆寫但不能超過科目預算。 |
| 傳遞方法 | <p>每天顯示行銷活動廣告的速度如何：</p><ul><li><p><i>標準（分散式）</i> （新行銷活動的預設）：將廣告印象分散在一天當中。</p></li><li><p><i>加速：</i> （2019年10月淘汰）在達到預算前儘可能多地顯示廣告。 因此，您的廣告可能不會在當天稍後出現。</p></li></ul> |
| 頻道型別 | <p>放置廣告的頻道。 指定一或多個選項：</p><ul><li class="p"><p><span style="font-style: italic;"><i>搜尋</i></span> （新行銷活動的預設值）：在Google搜尋網路(包括Google搜尋和Google搜尋合作夥伴網站)上放置廣告，也可選擇在Google顯示網路上放置廣告。 <b>注意：</b> 針對搜尋網路和顯示網路的行銷活動無法新增到產品組合以進行競標最佳化。</p></li><li class="p"><p><span style="font-style: italic;"><i>顯示</i></span>：僅將廣告放置在Google顯示網路上。</p></li><li class="p"><p><span style="font-style: italic;"><i>購物</i></span>：在Google Shopping （位於特定國家/地區）和Google搜尋網路(包括Google搜尋和Google搜尋合作夥伴網站)上放置購物廣告。 若要建立購物廣告，您必須在Google商家中心帳戶中擁有產品，並且 [允許搜尋、社交和商務從帳戶下載資料](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 請參閱「[實作 [!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)」以取得建立購物廣告流程的詳細資訊。</p></li></ul> |
| 網路 | <p>廣告的放置位置。 指定一或多個選項：</p><ul><li class="p"><p><span style="font-style: italic;"><i>Google搜尋</i></span>：僅支援在Google搜尋網路上的搜尋清單。</p></li><li class="p"><p><span style="font-style: italic;"><i>搜尋合作夥伴</i></span>：Google搜尋合作夥伴的贊助搜尋清單。</p></li><li class="p"><p><span style="font-style: italic;"><i>內容</i></span>：對顯示網路清單進行競標。</p></li><li class="p"><p><span style="font-style: italic;"><i>全部</i></span> （新行銷活動的預設值）：目標Google搜尋、搜尋合作夥伴和內容。</p></li></ul> |
| DSA網域名稱 | <p>（僅限搜尋網路；僅適用於擴充的動態搜尋廣告）廣告網路將用來鎖定動態搜尋廣告之內容的網站的根網域(例如example.com)或子網域(例如shoes.example.com)。<br><br><b>附註：</b></p><ul><li><p>展開動態搜尋廣告的目標是網站內容，而非關鍵字。</p></li><li><p>您的網域必須依廣告網路的自然搜尋索引編制索引，才能定位。</p></li><li><p>如果您未指定網域，則需要建立動態搜尋目標，為每個廣告群組鎖定所有網站頁面或其子集。</p></li></ul> |
| DSA網域語言 | （僅限搜尋網路；僅適用於展開的動態搜尋廣告）指定網站網域的語言。 <b>注意：</b> 如果網域包含多種語言的頁面，而您想要鎖定所有頁面，請針對每種語言建立個別的行銷活動。 |
| GDN自訂競標層級 | （僅針對顯示網路的行銷活動）競標方式：依據 <span style="font-style: italic;"><i>廣告群組</i></span> （預設）， <span style="font-style: italic;"><i>關鍵字</i></span>， <span style="font-style: italic;"><i>刊登</i></span> （網站），或 <span style="font-style: italic;"><i>無</i></span> （重設現有值）。 其他維度(<span style="font-style: italic;"><i>年齡</i></span>， <span style="font-style: italic;"><i>性別</i></span>， <span style="font-style: italic;"><i>興趣和清單</i></span>， <span style="font-style: italic;"><i>主題</i></span>、和 <span style="font-style: italic;"><i>垂直</i></span>)可從Google Ads介面取得。 如果您已使用Google Ads介面設定其他維度的競標，則會顯示該值，但您無法在這裡選取或輸入這些維度。</p><p><b>注意：</b></p><ul><li><p>當您依據關鍵字競標時，請在關鍵字層級建立追蹤範本。 同樣地，當您依版位競標時，請在版位層級建立追蹤範本。 針對所有其他維度，在廣告層級建立追蹤範本。</p></li><li><p>如果您以不支援的維度（年齡、性別、興趣和清單或主題）競標，搜尋、社交和商務不會最佳化維度的競標，而所有歸因都會套用至廣告群組。</p></li><li><p>搜尋網路上的廣告一律會使用關鍵字競標。</p></li></ul> |
| 行銷活動優先順序 | <p>（僅限購物行銷活動）當多個行銷活動廣告相同產品時，使用行銷活動的優先順序：  <span style="font-style: italic;"><i>低</i></span> （新行銷活動的預設值）， <span style="font-style: italic;"><i>中</i></span>，或 <span style="font-style: italic;"><i>高</i></span>.</p><p>當相同產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則符合最高競價的行銷活動條件。 |
| 商家ID | （僅限連結至商家摘要的購物行銷活動和對象行銷活動）其產品用於行銷活動的商家帳戶的客戶ID。 |  |
| 銷售國家 | （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動產品銷售的國家/地區。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。 |
| 產品範圍篩選器 | (僅使用Google購物網路的行銷活動)您的Google商家中心帳戶中的產品，可針對行銷活動建立購物廣告。 您可以使用格式dimension=attribute，輸入最多七個產品維度和屬性組合，以篩選產品。 使用「>>」分隔符號分隔多個篩選器。 如需可用產品維度的清單，請參閱&quot;[購物行銷活動產品篩選器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).」</p><p>範例：「CategoryL1=animals>>CategoryL2=pet supplies>>Brand=Acme Pet Supplies」</p><p>若要刪除現有值，請使用值 <span class="Code">[刪除]</span> （包括括弧）。</p> |
| 語言 | <p>（僅限搜尋和顯示網路）行銷活動中廣告的目標語言。</p><p>如果您沒有為此欄位或新促銷活動的「地理定位」欄位輸入值，則為帳戶指定的貨幣將決定預設語言，但具有未對應至特定語言（例如EUR）之貨幣的促銷活動將鎖定至所有語言。 如果您未輸入此欄位的值，但針對新促銷活動，在「地理定位」欄位中輸入值，則此預設值為 <span style="font-style: italic;"><i>全部</i></span>. 如果您將現有行銷活動的此欄位留空，則會保留現有值。</p><p>若要鎖定所有語言，請輸入 <span style="font-style: italic;"><i>全部</i></span>. 若要鎖定特定語言，請使用下列其中一項，輸入以分號分隔的值： <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">Google的語言名稱</a> (例如 <span style="font-style: italic;"><i>英文；日文</i></span>，此資訊會以正確的數值代碼取代)或數值代碼(例如 <span style="font-style: italic;"><i>1000；1005</i></span>)。 值不區分大小寫。</p> |
| 位置 | 為促銷活動放置廣告或排除廣告的地理位置。 如果您未針對新促銷活動在此欄位或「語言」欄位中輸入任何值，則為帳戶指定的貨幣會決定預設地點，但貨幣未對應至特定地點的促銷活動（例如EUR）會鎖定至所有地點。 如果您未輸入此欄位的值，但在 [!UICONTROL Languages] 欄位輸入新的促銷活動，則預設為 <i>全部</i>. 如果您將現有行銷活動的此欄位留空，則會保留現有值。</p><p>若要鎖定特定位置，請使用下列其中一項 [Google的位置名稱](https://developers.google.com/adwords/api/docs/appendix/geotargeting) （以正確數字代碼取代）或地點代碼：</p><ul><li><p>國家/地區：輸入國家/地區名稱(例如 <span style="font-style: italic;"><i>美國；日本</i></span>)或數值代碼(例如 <span style="font-style: italic;"><i>2840；2392</i></span>)。</p></li><li><p>州/省/地區：輸入州/省/地區名稱以及相關國家/地區的縮寫(例如 <span style="font-style: italic;"><i>東京，JP；美國紐約</i></span>)或數值代碼(例如 <span style="font-style: italic;"><i>20636；21167</i></span>)。</p></li><li><p>非美國城市：輸入城市名稱、州/省/地區名稱，以及國家/地區縮寫(例如 <span style="font-style: italic;"><i>安達市、東京、JP；北多市、東京、JP</i></span>)或數值代碼(例如 <span style="font-style: italic;"><i>1028850；1009293</i></span>)</p></li><li><p>US metro areas：輸入城市名稱、州名和國家/地區縮寫(例如 <span style="font-style: italic;"><i>Buffalo NY，美國；New York NY，美國</i></span>)或數值代碼(例如 <span style="font-style: italic;"><i>514；501</i></span>)。</p></li></ul><p>若要排除位置，請在位置名稱或程式碼前面加上減號(-)，例如 <span style="font-style: italic;"><i> — 日本</i></span>.</p><p><b>注意：</b> 值不區分大小寫。</p> |
| 位置型別 | （當您包含位置時） [位置型別](https://developers.google.com/google-ads/api/data/geotargets). |
| 裝置 | 在行銷活動或廣告群組層級進行競標調整的裝置型別： <i>智慧型手機</i>， <i>平板電腦</i>，或 <i>案頭</i>. |
| 競標調整 | <p>（當您包含位置、裝置或RLSA目標時）若要調整特定位置、特定裝置型別或特定對象目標的廣告競標，請執行下列動作：</p><ul><li><p>若要使用關鍵字層級競標（0%差異），請輸入0。 若為新目標，您也可以將此專案留空。</p></li><li><p>若要對此目標使用不同的競標，請輸入增加或減少競標的百分比。</p></li><ul><li><p>對於位置和RLSA目標，有效百分比包括從–90到900。</p></li><li><p>對於裝置競標調整，有效百分比包括：</p></li><ul><li><p>（行銷活動）–100 （不競標裝置型別的廣告）或從–90到900。</p></li><li><p>（廣告群組） -100代表智慧型手機和平板電腦（不針對裝置型別出價），從–90到900代表所有裝置型別。</p></li></ul></ul><li><p>（現有行銷活動和廣告群組）若要使用現有競標調整，請將此項留空。</p></li></ul> |
| Adobe記錄競標調整 | （包含在產生的Bulksheet中以供參考）Adobe建議用於行銷活動層級位置目標或RLSA的唯讀競標調整。 只有當行銷活動位於具有加權收入目標（而不是「最大化點按次數」目標）的產品組合中，且行銷活動包含至少兩個位置目標或過去90天內具有至少五次點按或成本為5美元的RLSA時，才會計算此值。</p><p>如果您想要手動編輯位置目標或RLSA以使用建議值，請在建立位置目標或RLSA後至少等待兩週，以允許足夠的資料收集，並且不要每週變更值超過一次。 |
| 裝置目標 | <p>（僅限舊版促銷活動型別）可顯示廣告的裝置： <span style="font-style: italic;"><i>全部</i></span>， <span style="font-style: italic;"><i>電腦</i></span>， <span style="font-style: italic;"><i>智慧型手機</i></span>，或 <span style="font-style: italic;"><i>平板電腦</i></span>. 若為新行銷活動，預設值為 <span style="font-style: italic;"><i>全部</i></span>.</p> |
| 裝置作業系統目標(Google Adwords) | （僅限舊版促銷活動型別；適用於裝置目標包含「智慧型手機」或「平板電腦」時）廣告可能顯示的作業系統： <span style="font-style: italic;"><i>全部</i></span>， <span style="font-style: italic;"><i>Android</i></span>， <span style="font-style: italic;"><i>iOS</i></span>，或 <span style="font-style: italic;"><i>掌心</i></span>. 若為新行銷活動，預設值為 <span style="font-style: italic;"><i>全部</i></span>.</p> |
| 行動電信業者(Google Adwords) | <p>（僅限舊版促銷活動型別；適用於裝置目標包含「全部」或「智慧型手機」時）智慧型手機可能連線的行動電信業者： <span style="font-style: italic;"><i>全部</i></span>，或一或多個電信業者，由以下專案表示： &lt;c span=&quot;&quot; id=&quot;2&quot; translate=&quot;no&quot; />電信業者代碼</i></span>>，&lt;<span style="font-style: italic;"><i>國家/地區代碼</i></span>> （例如T-Mobile、US）使用 <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">Google Ads的可用電信業者和代碼</a>. <span style="font-style: italic;"><i>以分號分隔多個電信業者（例如T-Mobile、US；T-Mobile、GB）。 若為新行銷活動，預設值為 <span style="font-style: italic;"><i>全部</i></span>.</p> |
| 廣告群組名稱 | <p>識別廣告群組的唯一名稱。 長度上限為255個字元；結尾的空白字元不會儲存（例如「廣告群組1」會儲存為「廣告群組1」）。 此欄位不適用於行銷活動層級的網站連結或行銷活動層級的裝置目標。</p> |
| 廣告群組型別 | <p>廣告群組型別： <span class="Option">探索</span> （僅適用於探索行銷活動）， <span class="Option">顯示</span> （適用於顯示行銷活動）， <span class="Option">搜尋動態</span> （適用於展開的動態搜尋廣告）， <span class="Option">Search Standard</span> （適用於搜尋廣告）、 <span class="Option">購物產品</span> （適用於購物產品廣告）， <span class="Option">購物展示</span> （不支援建立和編輯），或 <span class="Option">未知</span>.</p> |
| 最大CPC | <p>（僅限CPC行銷活動）最高每次點按成本(CPC)，這是在廣告網路上，無論是否有貨幣符號和標點符號，您為廣告點按會支付的最高金額。 您可以設定廣告群組和關鍵字、產品群組及動態搜尋目標的值。 新關鍵字的預設值繼承自廣告群組層級。 對於產品群組，您可以設定最低產品群組層的值；新層的預設值繼承自父層。</p><p>對於最佳化產品組合中的現有產品群組和動態搜尋目標，更新僅在一天內有效，並在下一個最佳化週期中被覆寫。</p><p><b>注意：</b> 對於版位，請使用「最大版位CPC」欄位。</p> |
| 最大內容CPC | <p>（僅限CPC行銷活動）最高內容每次點按成本(CPC)，這是從顯示網路網站支付廣告點按的最高金額，無論是否有貨幣符號和標點符號。 您可以設定和編輯非定位位置之行銷活動中的廣告群組層級值。</p> |
| 對象目標方法 | <p>（僅搜尋網路上的行銷活動，以及顯示網路上的現有唯讀Gmail行銷活動）是否：</p><ul><li><p><span style="font-style: italic;"><i>目標與競標</i></span>：只向與目標對象相關聯且滿足廣告群組任何其他目標的使用者顯示廣告。</p></li><li><p><span style="font-style: italic;"><i>僅限競標</i></span>：只要未與目標對象相關聯的使用者符合其他廣告群組層級目標，即可對他們顯示廣告。</p><p>不過，您可以針對特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。</p></li></ul> |
| 關鍵字 | 關鍵字字串。 長度上限為80個字元且不能超過10個字詞，而且只能包含字母、數字和下列特殊字元：空格 `# $ & _ - " [ ] ' + . / :`</p><p><b>注意：</b></p><ul><li><p>若要在廣告群組或行銷活動層級排除關鍵字，請將「比對型別」設定為 <span style="font-style: italic;"><i>負面</i></span>. 如果列包含廣告群組名稱，則會排除廣告群組的關鍵字。 如果列不包含廣告群組名稱，則會在整個行銷活動中排除關鍵字。</p></li><li><p>變更Google Ads關鍵字或相符型別，會刪除現有關鍵字並建立新關鍵字。</p></li></ul> |
| 位置 | （僅使用相符內容的行銷活動）顯示網路中可顯示廣告的版位。 指定下列其中一項：</p><ul><li class="p"><p>網站：輸入有效的URL。 它可以是頂層網域、第一層子網域或具有單一目錄名稱的網域。 URL不能包含問號(？)。 範例：<span class="Code"><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</span></p></li><li class="p"><p>特定頁面上的廣告位置：使用格式 `<URL> >> <location,sublocation>` (例如 `finance.google.com >> Company pages,Top right`)。</p></li><li class="p"><p>主題類別：使用語法 `<category::<category> > <subcategory>` 等等(例如 `category::Industries > Energy & Utilities > Oil & Gas`)。</p></li></ul><p><b>注意：</b> 若要在廣告群組或行銷活動層級排除版位，請將「比對型別」設定為 <span style="font-style: italic;"><i>負面</i></span>. 如果列包含廣告群組名稱，則會排除廣告群組的版位。 如果列不包含廣告群組名稱，則會排除整個行銷活動的版位。</p> |
| 自動鎖定目標運算式 | <p>（未啟用行銷活動設定「使用我的網站內容鎖定我的廣告」時為必要；否則為選用）廣告群組的動態搜尋目標。</p><p>對於所有目標，請使用星號(*)。</p><p>若要鎖定最多三個動態搜尋條件，請使用格式 `<category>=<target>`，其中 `<category>` 可包含下列任何類別。 使用「\[blank space\]和\[blank space\]」為個別類別聯結多個目標，並使用「」聯結多個類別[空白空間] 和 [空白空間]「。</p><ul><li class="p"><p><span style="font-style: italic;"><i>類別</i></span>：顯示具有特定Google內容類別的索引頁面的展開動態搜尋廣告。</p></li><li class="p"><p><span style="font-style: italic;"><i>URL</i></span>：針對具有特定URL的索引頁面，顯示展開的動態搜尋廣告，其中URL內的任何位置都可能包含值。</p></li><li class="p"><p><span style="font-style: italic;"><i>頁面標題</i></span>：針對在頁面標題中具有特定文字的索引頁面，顯示展開的動態搜尋廣告。</p></li><li class="p"><p><span style="font-style: italic;"><i>頁面內容</i></span>：針對具有特定內容的索引頁面，顯示展開的動態搜尋廣告。</p></li></ul><p>範例： url=shoes.example.com和page title=footwear</p> |
| 父級產品群組 | 任何父級產品群組的階層。<br><br>範例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| 產品群組 | <p>產品群組（例如「brand=acme」或「所有產品」）。</p><p><b>注意：</b></p><ul><li><p>當指定的產品群組不存在於父產品群組階層中時，Search、Social和Commerce會建立階層中所需的任何部分。</p></li><li><p>每當您在Google購物行銷活動中建立廣告群組，且預設競標設為廣告群組預設競標時，「搜尋、Social和商務」都會自動建立「所有產品」群組。 Search、Social和Commerce會在產品群組階層的每個層級，自動建立具有廣告群組預設競標的「其他一切」群組。 您仍然可以明確建立這些預設群組，並排除它們或變更其競標。</p></li><li><p>每個廣告群組最多可包含八層產品群組，包括「所有產品」和其他七層。</p></li></ul> |
| 資料分割型別 | 產品群組的磁碟分割型別： <i>細分</i> （當具有子產品群組時）或 <i>單位</i> （當它沒有子產品群組時）。 |
| 相符型別 | <p>對於動態搜尋目標或產品群組：動態搜尋目標或產品群組的關鍵字比對選項： <i>動態廣告目標</i> （新動態搜尋目標的預設值）、 <i>產品群組</i> （新產品群組的預設值）或 <i>負面產品群組</i> （排除產品群組）。</p><p>關鍵字：關鍵字的關鍵字比對選項： <span style="font-style: italic;"><i>廣泛</i></span>， <span style="font-style: italic;"><i>片語</i></span>， <span style="font-style: italic;"><i>精確</i></span>，或 <span style="font-style: italic;"><i>負面</i></span> （排除顯示網路上的關鍵字或位置）；將用於購物廣告的產品群組具有的相符型別為 <span style="font-style: italic;"><i>產品群組</i></span>. 如果您使用 <span style="font-style: italic;"><i>負面</i></span>，您也必須包含要排除的相符型別（例如「負面片語」）。</p><p>對於新關鍵字，預設值為 <span style="font-style: italic;"><i>廣泛</i></span>. 只有在編輯具有多個相符型別的關鍵字時，才需要相符型別或關鍵字ID的值。</p><p><b>注意：</b></p><ul><li><p>相符型別不適用於未使用關鍵字的展開動態搜尋廣告。</p></li><li><p>變更Google Ads關鍵字的相符型別，會刪除現有關鍵字並建立新關鍵字。</p></li><li><p>若為「廣泛比對修飾元」，請選擇「廣泛」，並在關鍵字中需要封閉變體的任何字詞前插入+ （例如「+紅色+鞋子」需要「紅色」和「鞋子」的封閉變體）。 <b>注意：</b> 廣泛比對修飾詞現在與某些語言的短語比對具有相同的比對行為，並且自2021年7月起，您一直無法建立新的廣泛比對修飾詞關鍵字。 另請參閱 [Google檔案](https://support.google.com/google-ads/answer/7042511) 以取得詳細資訊。</p> |
| 第一頁競標 | （包含在產生的Bulksheet中以供參考）在搜尋結果的第一頁放置廣告所需的競標。 此值未發佈到廣告網路。 |
| 品質分數 | （包含在產生的Bulksheet中以供參考）搜尋引擎已指派給關鍵字的目前品質分數。 此值未發佈到廣告網路。) |
| 創意偏好裝置 | （文字廣告、展開的動態搜尋廣告和增強型網站連結；選用）您偏好顯示廣告的裝置型別： <span style="font-style: italic;"><i>全部</i></span> （預設）或 <i>行動</i>. 時間 <i>行動</i> 指定，網路會嘗試向行動裝置使用者顯示廣告，而非案頭或平板電腦使用者。 否則，網路會在任何裝置型別上顯示廣告。</p><p><b>注意：</b></p><ul><li><p>僅管理員和 [!DNL Adobe] 帳戶管理員使用者可以編輯此設定。</p></li><li><p>網路不保證會在偏好的裝置型別上顯示廣告。</p></li><li><p>新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。</p></li></ul> |
| 廣告標題，廣告標題2-15 | （僅限展開的文字廣告和回應式搜尋廣告）廣告的標題，每個標題以垂直垂直垂直垂直線隔開( | )。 每個廣告標題欄位的長度上限為30個字元或15個雙位元組字元，包括任何動態文字（例如關鍵字和廣告自訂器的值）。</p><p>對於回應式搜尋廣告，廣告標題、廣告標題2和廣告標題3為必填，所有其他廣告標題欄位為選用。 若要刪除非必要欄位的現有值，請使用值 [刪除]</code> （包括括弧）。</p><p>對於回應式搜尋廣告，請使用以下格式插入廣告自訂器：</p><ul><li><p>Google Ads： `{CUSTOMIZER.AdCustomizerName:DefaultText}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft Advertising： `{CUSTOMIZER.Attribute name:default text}`，例如 `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>您無法建立或編輯文字廣告，但可以刪除展開的文字廣告，Google Ads已於2022年6月棄用。 |
| 廣告標題1-15位置 | <p>（僅限回應式搜尋廣告；選用）釘選對應廣告標題的位置： `[null]` （沒有值，因此廣告標題適用於所有職位）、 <i>1</i>， <i>2</i>，或 <i>3</i>. 例如，如果「廣告標題位置」的值為1，則「廣告標題」將僅出現在「位置1」中。 依預設，所有廣告標題均為Null （沒有值）。</p><p>若要刪除現有值，請使用值 [刪除]</code> （包括括弧）。</p><p><b>注意：</b> 您可以將多個廣告標題釘選至相同位置。 廣告網路將使用已釘選至該位置的其中一個廣告標題。 釘選到位置3的標題可能不會與廣告一起顯示。</p> |
| 說明第1-4行 | <p>（僅限延展的動態搜尋廣告、延展的文字廣告和回應式搜尋廣告）廣告內文。 每個說明欄位的長度上限為90個字元或45個雙位元組字元，包括任何動態文字（例如關鍵字和廣告自訂器的值）。</p><p>對於回應式搜尋廣告，請使用以下格式插入廣告自訂器：</p><ul><li><p>Google Ads： `{CUSTOMIZER.AdCustomizerName:DefaultText}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft Advertising： `{CUSTOMIZER.Attribute name:default text}`，例如 `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>對於展開的動態搜尋廣告，請僅使用「說明第1行」和「說明第2行」。 <b>注意：</b> 對於此廣告型別，變更廣告文案會刪除現有廣告並建立新廣告。</p><p>您無法建立或編輯文字廣告，但可以刪除展開的文字廣告，Google Ads已於2022年6月棄用。</p><p>對於回應式搜尋廣告，「說明第1行」與「說明第2行」為必要專案，「說明第3行」與「說明第4行」為選擇性專案。 若要刪除現有值，請使用值 [刪除]</code> （包括括弧）。</p> |
| 說明第1-4行位置 | （僅限回應式搜尋廣告；選用）釘選對應說明的位置： `[null]` （沒有值，因此說明適用於所有職位）、 <i>1</i>， <i>2</i>，或 <i>3</i>. 例如，如果「描述1位置」的值為1，則「描述1」將僅出現在「位置1」中。 依預設，不會將任何說明釘選到位置。</p><p>若要刪除現有值，請使用值 `[delete]` （包括括弧）。</p><p><b>注意：</b> 您可以將多個說明釘選到相同位置。 廣告網路將使用已釘選至位置的其中一個說明。 釘選到位置2的說明可能不會與廣告一起顯示。 |
| 顯示URL | 廣告中包含的URL。<br><br>對於展開的動態搜尋廣告，Google Ads會從網站網域動態產生此值，您不需要輸入值。<br><br>對於回應式搜尋廣告，您不需要輸入值。 系統會自動從最終URL的網域中擷取顯示URL。 您可以選擇使用「路徑1」和「路徑2」欄位自訂URL。<br><br>您無法建立或編輯文字廣告，但可以刪除展開的文字廣告，Google Ads已於2022年6月棄用。<br><br><b>注意：</b> （具有最終URL的帳戶）顯示URL和最終URL中的網域名稱必須相符。</p> |
| 顯示路徑1 | <p>(展開的文字廣告<span> 和回應式搜尋廣告</span> 僅限)</p><p>（選用）新增至顯示URL的文字，會自動從最終URL擷取。 在URL前面有正斜線(/)。 路徑不能包含正斜線(/)或新行(\n)字元。 長度上限為15個字元或7個雙位元組字元。</p><p>若要插入廣告自訂程式，請使用以下格式，其中 `Default text` 是當摘要檔案未包含有效值時要插入的選用值：</p><ul><li><p>Google Ads： `{CUSTOMIZER.AdCustomizerName:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li><li><p>Microsoft Advertising： `{CUSTOMIZER.Attribute name:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li></ul><p>例如，如果顯示路徑1是&quot;deals&quot;，則顯示URL會是&lt;<i>顯示URL</i>>/deals，例如www.example.com/deals。</p><p>您無法建立或編輯文字廣告，但可以刪除展開的文字廣告，Google Ads已於2022年6月棄用。</p> |
| 顯示路徑2 | 附加顯示路徑；請參閱「顯示路徑1」專案。<br><br>範例：如果顯示路徑1是&quot;deals&quot;，而顯示路徑2是&quot;local&quot;，則顯示URL會是&lt;<i>顯示URL</i>>/deals/local，例如www.example.com/deals/local。</p><p>您無法建立或編輯文字廣告，但可以刪除展開的文字廣告，Google Ads已於2022年6月棄用。</p> |
| 促銷行 | (僅適用於Google產品清單廣告)搜尋結果中產品清單所包含的選擇性促銷明細行。 長度上限為45個字元。</p><p>視廣告在頁面上的出現位置而定，促銷明細行可能會出現在與廣告相關的不同位置（例如廣告下方）。 |
| 連結名稱 | <p>網站連結文字。 最多可包含25個字元。</p><p>若是新的網站連結，您必須在網站連結列中包含行銷活動名稱。 對於廣告群組層級網站連結，您還必須包含廣告群組名稱。</p><p><b>注意：</b> 35個字元的現有文字仍會顯示在桌上型電腦和平板電腦的廣告中，但不會顯示在行動裝置上。</p> |
| 行動應用程式平台(Google Adwords) | （僅限現有應用程式安裝廣告）行動應用程式執行所在的作業系統： <i>android</i> 或 <i>ios</i>. |
| 行動應用程式ID (Google Adwords) | （僅限現有應用程式安裝廣告） <p>應用程式ID或封裝名稱。 |
| 行動應用程式名稱(Google Adwords) | （僅限現有應用程式安裝廣告）應用程式的名稱。 |
| 開始日期 | <p>（僅限增強型網站連結）網站連結可能進行競標的第一天（以廣告商的時區及下列格式之一表示）： <span style="font-style: italic;"><i>m/d/yyyy</i></span>， <span style="font-style: italic;"><i>m/d/yy</i></span>， <span style="font-style: italic;"><i>M-d-yyyy</i></span>，或 <span style="font-style: italic;"><i>m-d-yy</i></span>. 新增強型網站連結的預設值為當天。</p><p><b>注意：</b> 新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。</p> |
| 結束日期 | <p>（僅限增強型網站連結）可針對網站連結進行競標的最後日期（以廣告商的時區及下列格式之一顯示）：  <span style="font-style: italic;"><i>m/d/yyyy</i></span>， <span style="font-style: italic;"><i>m/d/yy</i></span>， <span style="font-style: italic;"><i>M-d-yyyy</i></span>，或 <span style="font-style: italic;"><i>m-d-yy</i></span>. 預設值為none （無結束日期）。</p><p><b>注意：</b> 新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。</p> |
| 排除平板電腦(Google Adwords) | （僅限現有應用程式安裝廣告）</p><p>（選用）防止Google廣告向平板電腦使用者顯示廣告。 值可包括 <i>是</i> 和 <i>否</i>. |
| 登陸頁面尾碼 | 要附加至最終URL結尾以追蹤資訊的任何引數。 範例： `param2=value1&param3=value2`<br><br>請參閱「[的點選追蹤格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).」<br><br>較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同的追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用Google Ads編輯器。 |
| 追蹤範本 | 追蹤範本會指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在ValueTrack引數中。 最精細層級的追蹤範本（以關鍵字作為最精細的層級）會覆寫所有較高層級的值。<br><br>針對Adobe廣告轉換追蹤（在行銷活動設定包含「EF重新導向」和「自動上傳」時套用），搜尋、Social和商務會在您儲存記錄時自動附加自己的重新導向和追蹤代碼。<br><br>針對協力廠商重新導向與追蹤，請輸入值。 如需可指出追蹤範本中最終URL的ValueTrack引數清單，請參閱 <a href="https://support.google.com/google-ads/answer/2375447?hl=en" target="_blank">Google Ads檔案</a>.<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| 基本URL/最終URL | 搜尋引擎使用者按一下您的廣告時，系統會將他們帶往的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 關鍵字層級的基礎/最終URL會覆寫廣告層級和更高層級的基礎/最終URL。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| 目的地URL | （包含在已產生的Bulksheet中以供參考；未張貼至搜尋引擎）對於具有目的地URL的帳戶，此URL會將廣告連結至廣告商網站上的基本URL/登陸頁面（有時透過另一個網站來追蹤點選，然後將使用者重新導向到登陸頁面）。 其中包含為Search， Social， &amp; Commerce促銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，這會根據帳戶設定和促銷活動設定中的追蹤引數。 如果您已附加搜尋引擎特定引數，這些引數可能會取代為搜尋、社交和商務的同等引數。<br><br>若為具有最終URL的帳戶，此欄會顯示與「基本URL/最終URL」欄相同的值。 |
| 自訂URL引數 | 要取代的資料 `{custom_code}` 變數納入搜尋帳戶或促銷活動設定的追蹤引數時，使用動態變數。 若要在追蹤URL中插入自訂值，您必須使用「產生追蹤URL」選項上傳大量表單檔案。 |
| 創意型別 | 廣告格式： <i>文字廣告</i>， <i>展開的文字廣告</i>， <i>動態搜尋廣告</i> （已棄用的廣告型別）， <i>展開的動態搜尋廣告</i>， <i>顯示廣告</i>， <i>應用程式安裝廣告</i> （已棄用）， <i>影像</i> <i>產品廣告</i> （購物廣告），或 <i>回應式搜尋廣告</i>. 新廣告的預設為 <i>文字廣告</i>.<br><br>需要建立或編輯產品廣告的狀態。 |
| Param1 | <p>的數值 `{param1}` 廣告引數，可包含在Bulksheet檔案中任何廣告的廣告復本或顯示URL中。 長度上限為25個字元，您可以包括下列非數字字元：</p><ul><li><p>值前面或後面可附加貨幣符號或代碼。 例如， `£2.000,00` 和 `2000GBP` 有效。</p></li><li><p>值可包含逗號(`,`)或句點(`.`)做為分隔符號，並加上選填的句號(`.`)或逗號(`,`)以取得小數值。 例如， `1,000.00` 和 `2.000,10` 有效。</p></li><li><p>值可以加上前置詞或百分比符號(`%`)，加號(`+`)或減號(`- `)。 例如， `20%`， `208+`、和 `-42.32` 有效。</p></li><li><p>兩個數字可內嵌於正斜線中。 例如， `4/1` 和 `0.95/0.45` 有效。</p></li></ul><p>若要刪除現有值，請使用值 `[delete]` （包括括弧）。</p> |
| Param2 | 的數值 `{param2}` 廣告引數，可包含在Bulksheet檔案中任何廣告的廣告復本或顯示URL中。 如需詳細資訊，請參閱Param1專案。 |
| 對象 | 搜尋廣告(RLSA)目標對象的再行銷清單，或行銷活動或廣告群組的已排除對象。 您將在「目標型別」欄位中指定它是目標還是排除專案。 |
| 目標型別 | （指定對象時）指定的對象是否為 <i>包含</i> （目標）或 <i>排除</i>. |
| 行銷活動狀態 | 行銷活動的顯示狀態： <i>作用中</i>， <i>已暫停</i>， <i>已結束</i> （不可編輯），或 <i>已刪除</i> （僅限現有行銷活動）。 新行銷活動的預設為 <i>作用中</i>. 若要刪除作用中或已暫停的行銷活動，請輸入值 <i>已刪除</i>. |
| 廣告群組狀態 | 廣告群組的顯示狀態： <i>作用中</i>， <i>已暫停</i>，或 <i>已刪除</i> （僅限現有廣告群組）。 新廣告群組的預設值為「作用中」。 若要刪除作用中或暫停的廣告群組，請輸入值 `Deleted`. |
| 關鍵字狀態 | 關鍵字的顯示狀態： <i>作用中</i>， <i>已暫停</i>，或 <i>已刪除</i> （僅限現有關鍵字）。 新關鍵字的預設值為「作用中」。 若要刪除作用中或暫停的關鍵字，請輸入值 <i>已刪除</i>. |
| 廣告狀態 | 廣告的顯示狀態： <i>作用中</i>， <i>已刪除</i> （僅限現有廣告）、 <i>未核准</i> （不可編輯），或 <i>已暫停</i>. 新廣告的預設值為「作用中」。 若要刪除作用中或已暫停的廣告，請輸入值 <i>已刪除</i>. |
| 位置狀態 | 網站位置的狀態： <span style="font-style: italic;"><i>作用中</i></span>， <span style="font-style: italic;"><i>已暫停</i></span>，或 <span style="font-style: italic;"><i>已刪除</i></span> （僅限現有廣告）。 新網站的預設值為 <span style="font-style: italic;"><i>作用中。</i></span> 若要刪除作用中或暫停的位置，請輸入值 <span style="font-style: italic;"><i>已刪除</i></span>. |
| 目標狀態 | 動態搜尋目標的狀態： <span style="font-style: italic;"><i>作用中</i></span>， <span style="font-style: italic;"><i>已暫停</i></span>，或 <span style="font-style: italic;"><i>已刪除</i></span> （僅限現有目標）。 新目標的預設值為 <span style="font-style: italic;"><i>作用中。</i></span> 若要刪除作用中或暫停的目標，請輸入值 <span style="font-style: italic;"><i>已刪除</i></span>. |
| 產品群組狀態 | 產品群組的顯示狀態： <span style="font-style: italic;"><i>作用中</i></span> <span>或</span> <span style="font-style: italic;"><i>已刪除</i></span> （僅限現有產品群組）。 新產品群組的預設值為 <span style="font-style: italic;"><i>作用中</i></span>. 若要刪除使用中的產品群組，請輸入值 <span style="font-style: italic;"><i>已刪除</i></span>. |
| 網站連結狀態 | 網站連結的顯示狀態： <span style="font-style: italic;"><i>作用中或已刪除</i></span> （僅限現有網站連結）。 新網站連結的預設值為 <span style="font-style: italic;"><i>作用中</i></span>. 若要刪除作用中的網站連結，請輸入值 <span style="font-style: italic;"><i>已刪除</i></span>. |
| 位置狀態 | 位置目標的狀態： <i>作用中</i> 或 <i>已刪除</i> （僅限現有位置）。 新位置的預設值為「作用中」。 若要刪除作用中的位置，請輸入值 <i>已刪除</i>. |
| RLSA目標狀態 | 行銷活動或廣告群組層級RLSA目標或(僅限Google廣告)排除的狀態： <span style="font-style: italic;"><i>作用中或已刪除</i></span> （僅限現有目標）。 新目標或排除專案的預設值為 <span style="font-style: italic;"><i>作用中</i></span>. 若要刪除作用中目標或排除專案，請輸入值 <span style="font-style: italic;"><i>已刪除</i></span>. |
| 裝置目標狀態 | <p>行銷活動或廣告群組層級裝置目標的狀態： <span class="Option">作用中</span> 或 <span class="Option">已刪除</span>. 對於新的行銷活動和廣告群組，預設值為 <span class="Option">作用中</span>.</p> |
| \[廣告商特定標籤分類\] | （以廣告商特定的標籤分類命名，例如稱為顏色的標籤分類的「顏色」）與實體相關聯的指定分類的值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 長度上限為100個字元，值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤相關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值都不區分大小寫。 |
| 限制 | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><b>>限制由子實體繼承，因此您不需要輸入子實體的值，除非您想要覆寫繼承的值。 |
| 行銷活動ID | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更促銷活動名稱時才需要，除非該列包含促銷活動的「AMO ID」。 |
| 廣告群組識別碼 | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更行銷活動名稱時才需要，除非該列包含廣告群組的「AMO ID」。 |
| 關鍵字ID | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更關鍵字時才需要，除非該列包含a)足夠的屬性欄來識別關鍵字或b)「AMO ID」。 |
| 廣告ID | <p>可識別現有廣告的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 對於回應式搜尋廣告，編輯或刪除廣告資料需要廣告ID或AMO ID。 對於所有其他實體型別，只有在您變更廣告狀態時才需要AMO ID，除非該列包含a)足夠的廣告屬性欄來識別廣告，或b)「AMO ID」。 不過，如果您既不包含廣告ID也不包含AMO ID，而且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。</p><p><b>注意：</b> 如果您編輯a)廣告屬性欄，但現有廣告的「狀態」除外，或b)回應式搜尋廣告的任何資料，且您既未包含廣告ID也未包含AMO ID，則會建立新廣告，且現有廣告不會變更。</p> |
| 刊登ID | 可識別網站位置的唯一ID。 只有在您變更或刪除位置時才需要，除非該列包含a)足夠的屬性欄來識別位置或b)「AMO ID」。 |
| 目標ID | 可識別現有自動目標的唯一ID。 只有在您變更或刪除自動目標時才需要，除非該列包含目標的「AMO ID」。 |
| 產品群組識別碼 | 可識別現有產品群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄來識別產品群組或b)「AMO ID」。 |
| 網站連結ID | 可識別現有網站連結的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄來識別網站連結或b)「AMO ID」。 不過，如果您未包含網站連結廣告ID或AMO ID，而且屬性欄符合多個網站連結，則只有其中一個網站連結的狀態會變更。</p><p><b>注意：</b> 如果您編輯現有網站連結的網站連結屬性欄（「狀態」除外），而且您既不包含網站連結ID也不包含AMO ID，則會建立新的網站連結，且不會變更現有的網站連結。 |
| RLSA目標ID | 可識別現有行銷活動或廣告群組層級RLSA目標或(僅限Google廣告)排除的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除目標或排除專案時才需要，除非列包含目標的「AMO ID」。 |
| 裝置目標ID | <p>可識別現有行銷活動層級或廣告群組層級裝置目標或排除專案的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除目標時才需要，除非列包含目標的「AMO ID」。</p> |
| AMO ID | （在產生的Bulksheets中）同步實體的Adobe產生的唯一識別碼。 對於回應式搜尋廣告，編輯或刪除廣告時需要AMO ID，除非您包含廣告ID。 若要使用AMO ID編輯所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則編輯或刪除資料時需使用AMO ID。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |
| EF錯誤訊息 | （包含在產生的大量表單中以供參考）用來顯示來自廣告網路的錯誤訊息的預留位置，這些訊息與資料列中的資料有關；錯誤訊息包含在EF錯誤檔案中。 此值未發佈到廣告網路。 |
| SE錯誤訊息 | （包含在已產生的Bulksheets中以供參考）用來顯示來自廣告網路的錯誤訊息的預留位置，這些錯誤訊息與資料列中的資料有關；錯誤訊息包含在SE錯誤檔案中。 此值未發佈到廣告網路。 |
| 劐免要求 | （包含在產生的Bulksheet中以供參考）預留位置，可顯示廣告違反的任何Google廣告原則的名稱和文字。 |
| 零售雜湊 | (包含於使用進階Campaign Management產生的大量表單中以供參考)英數字元雜湊代碼(例如f9639f40cdf56524b541e5dacf55a991)，表示專案是使用進階(ACM)檢視產生的。 |

<table style="table-layout:auto">

## 建立、編輯或刪除每個帳戶元件所需的欄位

### 行銷活動欄位

|帳戶名稱 |除非每一列包含實體的「AMO ID」，否則為必要。 | |行銷活動名稱 |必要 |識別帳戶促銷活動的唯一名稱。 | |行銷活動預算 |必要：建立<br><br>>可選：編輯或刪除 |行銷活動的每日支出限制，無論是否包含貨幣符號和標點符號。 此值會覆寫但不能超過科目預算。 | |傳送方法 |必要：建立<br><br>可選：編輯或刪除 | |頻道型別 |必要：建立<br><br>可選：編輯或刪除 | |網路 |必要：建立<br><br>可選：編輯或刪除 | | DSA網域名稱 |必要：建立<br><br>可選：編輯或刪除 | | DSA網域語言 |必要：建立<br><br>可選：編輯或刪除 | |行銷活動優先順序 |必要/選用：建立<br><br>可選/不適用：編輯或刪除 | |商家ID |必要/選用：建立<br><br>可選/不適用：編輯或刪除 | |銷售國家 |必要/選用：建立<br><br>可選/不適用：編輯或刪除 | |產品範圍篩選器 |選擇性 | |語言 |選擇性 | |裝置目標 |選擇性 | |裝置作業系統目標(Google Adwords) |選擇性 | |行動電信業者(Google Adwords) |選擇性 | |對象目標方法 |不適用 | |登陸頁面尾碼 | <p>可選 | |追蹤範本 |選擇性 | |行銷活動狀態 |選用：建立或編輯<br><br>必要：刪除 | | \[廣告商特定標籤分類\] |選擇性 | |限制 |選擇性 | |促銷活動ID |只有在您變更促銷活動名稱時才需要，除非該列包含促銷活動的「AMO ID」。 | | AMO ID | n/a：建立<br><br>必要/選用：編輯或刪除 |

### 廣告群組欄位

| 欄位 | 必填？ |
| ---- | ---- |
| 帳戶名稱 | 除非每一列包含實體的「AMO ID」，否則為必要。 |
| 行銷活動名稱 | 必填 |
| 網路 | 不適用 |
| GDN自訂競標層級 | 可選 |
| 廣告群組名稱 | 必填 |
| 廣告群組型別 | 必填 |
| 最大CPC | 可選 |
| 最大內容CPC | 可選 |
| 對象目標方法 | 必填 |
| 追蹤範本 | 可選 |
| 廣告群組狀態 | 可選：建立或編輯<br><br>必要：刪除 |
| \[廣告商特定標籤分類\] | 可選 |
| 限制 | 可選 |
| 廣告群組識別碼 | 只有在您變更行銷活動名稱時才需要，除非該列包含廣告群組的「AMO ID」。 |
| AMO ID | 編輯或刪除資料需要AMO ID，除非您包含實體ID和父實體ID。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

<!-- 

### Keyword fields

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

| Field | Required? | Description |
| ---- | ---- | ---- |
| Base URL/Final URL |  |

### Placement fields


### Text/Product listing fields

This uses the "[!UICONTROL Creative (except RSA)]" row in the [!UICONTROL Download Bulksheet] dialog.


### Expanded dynamic search ad

This ad type is now called "dynamic search ad" in [!DNL Google Ads].

This uses the "[!UICONTROL Creative (except RSA)]" row in the [!UICONTROL Download Bulksheet] dialog.


### Responsive search ad fields 

This uses the "[!UICONTROL Responsive Search Ad]" row in the [!UICONTROL Download Bulksheet] dialog.


### Dynamic search target (auto target) fields


### Shopping product group fields


### Campaign-level and ad group-level sitelink fields


### Location target fields

| Field | Required? ]
| ---- | ---- |
| Location | Required: Create or edit<br><br>Optional: Delete |
| Location Type | Optional  |

## Campaign-level and ad group-level device target fields

| Field | Required? | Description |
| ---- | ---- | ---- |
| Device Target Status | Optional |
| Device Target ID | Required only when you change or delete the target, unless the row includes an &quot;AMO ID&quot; for the target. |
| AMO ID | The AMO ID is required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |


## Campaign-level and ad group-level RLSA target/exclusion fields

-->

[^1]： [!DNL Excel] 開啟檔案時，會將大型數字轉換為科學記號(例如2.12E+09 for 2115585666)。 若要檢視標準標籤法中的數字，請選取欄中的任何儲存格，然後按一下公式列內的「 」。

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [可在Bulksheets中執行的作業](bulksheet-operations.md)
>* [支援的Bulksheet檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>* [的點選追蹤格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)
