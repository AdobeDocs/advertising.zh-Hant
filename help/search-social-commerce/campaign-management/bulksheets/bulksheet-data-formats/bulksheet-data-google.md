---
title: 以下專案的必要大量表單資料： [!DNL Google Ads] 帳戶
description: 請參考大量表單中必要的標題欄位和資料欄位， [!DNL Google Ads] 帳戶。
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '7855'
ht-degree: 0%

---

# 附錄 — 必要的大量表單資料 [!DNL Google Ads] 帳戶

若要建立和更新 [!DNL Google Ads] 大量行銷活動資料時，您可以使用特別格式化的搜尋、社交和Commerce大量表單檔案 [!DNL Google Ads] 帳戶。 您可以) [產生現有帳戶的批次處理工作表檔案](../bulksheet-download.md) （或b）手動建立(請參閱&quot;[支援的Bulksheet檔案格式](bulksheet-file-formats.md)&quot;，以取得支援的檔案格式的一般資訊)。

每個大量表單都必須包含標題欄位和所需的對應資料欄位 [您要執行的特定作業](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) （例如建立廣告）。 當欄位不是必填欄位時，您可以從標題和資料列忽略它。 上傳大量工作表檔案時，會刪除所有自訂欄。

以下表格包含所有可用的資料欄位和其他表格，指出必須新增、編輯或刪除個別實體資料（例如行銷活動和關鍵字）的欄位。

## 所有可用資料欄位 {#bulksheet-fields-all-google}

下表說明所有可用的資料欄位。

有關帳戶實體相關的資料欄位，請參閱&quot;[建立、編輯或刪除每個帳戶元件所需的欄位](#bulksheet-fields-per-component-google).」

>[!NOTE]
>
>* 所有文字欄中的值都區分大小寫。
>* 當您建立新記錄並且不包含所有必要資料欄位的值時，這些欄位中的某些會被指派指定的預設值。
>* 對於未在下方指定的欄位，會使用廣告網路的預設值。
>* 如需中可用大量表單列的清單， [!UICONTROL Download Bulksheet] 對話方塊，請參閱&quot;[依廣告網路大量表單列](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network).」

| 欄位 | 說明 |
| ---- | ---- |
| [!UICONTROL Platform] | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Acct Name] | 可識別廣告網路帳戶的唯一名稱。 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 可識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Campaign Budget] | 行銷活動的每日支出限制，無論是否包含貨幣符號和標點符號。 此值會覆寫，但不能超過科目預算。 |
| [!UICONTROL Delivery Method] | <p>每天顯示行銷活動廣告的速度如何：</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> （新行銷活動的預設）：將廣告印象分散在一天當中。</p></li><li><p><i>[!UICONTROL Accelerated]：</i> （2019年10月淘汰）在達到預算前儘可能顯示您的廣告。 因此，您的廣告可能不會在當天稍後出現。</p></li></ul> |
| [!UICONTROL Channel Type] | <p>要放置廣告的管道。 指定一或多個選項：</p><ul><li><p><i>[!UICONTROL Search]</i> （新行銷活動的預設）：將廣告放置在 [!DNL Google Ads] 搜尋網路(包括 [!DNL Google Ads] 搜尋和搜尋合作夥伴網站)，並可選擇在 [!DNL Google Ads] 顯示網路。 <b>注意：</b> 同時以搜尋網路和顯示網路為目標的行銷活動，無法新增至競標最佳化的產品組合。</p></li><li><p><i>[!UICONTROL Display]</i>：僅將廣告置於 [!DNL Google Ads] 顯示網路。</p></li><li><p><i>[!UICONTROL Shopping]</i>：若要刊登購物廣告，請執行下列步驟： [!DNL Google Ads] 購物網路（位於特定國家/地區）及 [!DNL Google Ads] 搜尋網路(包括 [!DNL Google Ads] 搜尋及搜尋合作夥伴網站)。 若要建立購物廣告，您必須在 [!DNL Google Merchant Center] 帳戶和 [允許搜尋、社交和Commerce從帳戶下載資料](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 請參閱&quot;[實作 [!DNL Google Ads] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)」以取得建立購物廣告流程的詳細資訊。</p></li></ul> |
| [!UICONTROL Networks] | <p>廣告的放置位置。 指定一或多個選項：</p><ul><li><p><i>[!UICONTROL Google Search]</i>：僅限Google搜尋網路上的贊助搜尋清單。</p></li><li><p><i>[!UICONTROL Search Partners]</i>：Google搜尋合作夥伴的贊助搜尋清單。</p></li><li><p><i>[!UICONTROL Content]</i>：對顯示網路清單進行競標。</p></li><li><p><i>[!UICONTROL All]</i> （新行銷活動的預設值）：鎖定Google搜尋、搜尋合作夥伴和內容。</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>（僅限搜尋網路；僅適用於展開的動態搜尋廣告）廣告網路用來鎖定動態搜尋廣告之內容的網站根網域(例如example.com)或子網域(例如shoes.example.com)。<br><br><b>附註：</b></p><ul><li><p>展開的動態搜尋廣告會以網站內容為目標，而非關鍵字。</p></li><li><p>您的網域必須依廣告網路的有機搜尋索引編制索引，才能定位。</p></li><li><p>如果您未指定網域，則必須建立動態搜尋目標，將目標設為每個廣告群組的所有網站頁面或其子集。</p></li></ul> |
| [!UICONTROL DSA Domain Language] | （僅限搜尋網路；僅適用於擴充的動態搜尋廣告）指定網站網域的語言。 <b>注意：</b> 如果網域包含多種語言的頁面，而您想要鎖定所有頁面，請針對每種語言建立個別的行銷活動。 |
| [!UICONTROL GDN Custom Bid Level] | （僅針對顯示網路的行銷活動）競標方式：依據 <i>[!UICONTROL Ad Group]</i> （預設）， <i>[!UICONTROL Keyword]</i>， <i>[!UICONTROL Placement]</i> （網站），或 <i>[!UICONTROL None]</i> （重設現有值）。 其他維度(<i>年齡</i>， <i>性別</i>， <i>興趣和清單</i>， <i>主題</i>、和 <i>垂直</i>)可從取得。 [!DNL Google Ads] 介面。 如果您已使用 [!DNL Google Ads] 介面可依其他維度設定競標，會顯示該值，但您無法在此處選取或輸入這些維度。</p><p><b>注意：</b></p><ul><li><p>當您依據關鍵字競標時，請在關鍵字層級建立追蹤範本。 同樣地，當您依版位競標時，請在版位層級建立追蹤範本。 針對所有其他維度，在廣告層級建立追蹤範本。</p></li><li><p>如果您以不支援的維度（年齡、性別、興趣和清單或主題）競標，搜尋、社交和Commerce不會最佳化維度的競標，而所有歸因都會套用至廣告群組。</p></li><li><p>搜尋網路上的廣告一律會使用關鍵字競標。</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>（僅適用於購物行銷活動）當多個行銷活動廣告相同產品時，使用行銷活動的優先順序：  <i>[!UICONTROL Low]</i> （新行銷活動的預設值）， <i>[!UICONTROL Medium]</i>，或 <i>[!UICONTROL High]</i>.</p><p>當同一個產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）適用於廣告拍賣。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。 |
| [!UICONTROL Merchant ID] | （僅限於連結至商家摘要的購物行銷活動和對象行銷活動）其產品用於行銷活動的商家帳戶的客戶ID。 |  |
| [!UICONTROL Sales Country] | （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動產品銷售的國家/地區。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。 |
| [!UICONTROL Product Scope Filter] | (使用下列專案的行銷活動： [!DNL Google Ads] 僅限購物網路)您電腦中的產品 [!DNL Google Merchant Center] 可為其建立行銷活動之購物廣告的帳戶。 您可以使用格式dimension=attribute，輸入最多七種產品維度和屬性組合，以篩選產品。 使用「>>」分隔符號分隔多個篩選器。 如需可用產品維度的清單，請參閱&quot;[購物行銷活動產品篩選器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).」</p><p>範例：「CategoryL1=animals>>CategoryL2=pet supplies>>Brand=Acme Pet Supplies」</p><p>若要刪除現有值，請使用值 <code>[刪除]</code> （包括括弧）。</p> |
| [!UICONTROL Languages] | <p>（僅限搜尋和顯示網路）行銷活動中廣告的目標語言。</p><p>如果您沒有為此欄位或 [!UICONTROL Geo Targeting] 欄位若為新行銷活動，為帳戶指定的貨幣會決定預設語言，但貨幣未對應至特定語言的行銷活動（例如EUR）會鎖定至所有語言。 如果您未輸入此欄位的值，但在 [!UICONTROL Geo Targeting] 欄位進行新的行銷活動，此預設為 <i>[!UICONTROL All]</i>. 如果您將現有行銷活動的此欄位留空，則會保留現有值。</p><p>若要鎖定所有語言，請輸入 <span style="font-style: italic;">&lt;i span=&quot;&quot; id=&quot;1&quot; translate=&quot;no&quot; />. [!UICONTROL >All]</i></span>若要鎖定特定語言，請使用下列其中一項，輸入以分號分隔的值： <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] 語言名稱</a> (例如 <i>英文；日文</i>，以正確的數值代碼取代)或數值代碼(例如 <i>1000；1005</i>)。 值不區分大小寫。</p> |
| [!UICONTROL Location] | 為促銷活動放置廣告或排除廣告的地理位置。 如果您未針對新促銷活動在此欄位或「語言」欄位中輸入任何值，則為帳戶指定的貨幣會決定預設地點，除非其貨幣未對應至特定地點的促銷活動（例如EUR）會鎖定至所有地點。 如果您未輸入此欄位的值，但在 [!UICONTROL Languages] 欄位輸入新的促銷活動，則預設為 <i>[!UICONTROL All]</i>. 如果您將現有行銷活動的此欄位留空，則會保留現有值。</p><p>若要鎖定特定位置，請使用下列其中一項 [[!DNL Google Ads] 位置名稱](https://developers.google.com/adwords/api/docs/appendix/geotargeting) （以正確數值代碼取代）或地點代碼：</p><ul><li><p>國家/地區：輸入國家/地區名稱(例如 <i>美國；日本</i>)或數值代碼(例如 <i>2840；2392</i>)。</p></li><li><p>州/省/地區：輸入州/省/地區名稱以及相關國家/地區的縮寫(例如 <i>東京，JP；紐約，美國</i>)或數值代碼(例如 <i>20636；21167</i>)。</p></li><li><p>非美國城市：輸入城市名稱、州/省/地區名稱，以及國家/地區縮寫(例如 <i>安達謙、東京、JP；北極、東京、JP</i>)或數值代碼(例如 <i>1028850；1009293</i>)</p></li><li><p>US metro area：輸入城市名稱、州名和國家/地區縮寫(例如 <i>美國布法羅紐約；美國紐約</i>)或數值代碼(例如 <i>514；501</i>)。</p></li></ul><p>若要排除位置，請在位置名稱或程式碼前面加上減號(`-`)，例如 <i> — 日本</i>.</p><p><b>注意：</b> 值不區分大小寫。</p> |
| [!UICONTROL Location Type] | （當您包含位置時） [位置型別](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | 在行銷活動或廣告群組層級進行競標調整的裝置型別： <i>[!UICONTROL smartphone]</i>， <i>[!UICONTROL tablet]</i>，或 <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(當您包含 [!UICONTROL Location]， [!UICONTROL Device]，或 [!UICONTROL RLSA] target)是否調整特定位置、特定裝置型別或特定對象目標中廣告的競標：</p><ul><li><p>若要使用關鍵字層級的競標（0%差異），請輸入0。 若為新目標，您也可以將此專案留空。</p></li><li><p>若要對此目標使用不同的競標，請輸入增加或減少競標的百分比。</p></li><ul><li><p>對於位置和RLSA目標，有效百分比包括從–90到900。</p></li><li><p>針對裝置競標調整，有效百分比包括：</p></li><ul><li><p>（行銷活動）–100 （不對裝置型別上的廣告投標）或從–90到900。</p></li><li><p>（廣告群組） -100適用於智慧型手機和平板電腦（不得競標裝置型別），以及從–90到900適用於所有裝置型別。</p></li></ul></ul><li><p>（現有行銷活動和廣告群組）若要使用現有競標調整，請將此項留空。</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | （包含在產生的大量表單中以供參考） Adobe建議用於行銷活動層級位置目標或RLSA的唯讀競標調整。 只有當行銷活動位於目標為使用加權轉換量度的產品組合中時，才會計算 [!UICONTROL Maximize Clicks] 目標)，且促銷活動包含至少兩個位置目標或過去九十天內至少點按五次或成本為5美元的零售值。</p><p>如果您想要手動編輯位置目標或RLSA以使用建議值，請在建立位置目標或RLSA後至少等待兩週，以允許足夠的資料收集，並且不要每週變更值超過一次。 |
| [!UICONTROL Device Targets] | <p>（僅限舊版促銷活動型別）廣告可能會顯示的裝置： <i>[!UICONTROL All]</i>， <i>[!UICONTROL Computers]</i>， <i>[!UICONTROL Smartphones]</i>，或 <i>[!UICONTROL Tablets]</i>. 若為新行銷活動，預設值為 <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | （僅限舊版促銷活動型別；適用於裝置目標包含「智慧型手機」或「平板電腦」時）可顯示廣告的作業系統： <i>[!UICONTROL All]</i>， <i>[!UICONTROL Android]</i>， <i>[!UICONTROL iOS]</i>，或 <i>[!UICONTROL Palm]</i>. 若為新行銷活動，預設值為 <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(僅限舊版促銷活動型別；適用於 [!UICONTROL Device Targets] include &quot;[!UICONTROL All]「或」[!UICONTROL Smartphones]&quot;)智慧型手機可能連線的行動電信業者： <i>[!UICONTROL All]</i>，或一或多個電信業者，指示為 &lt;c span=&quot;&quot; id=&quot;4&quot; translate=&quot;no&quot; />電信業者代碼</i>>，&lt;<i>國家/地區代碼</i>> （例如T-Mobile、US）使用 <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">可用的電信業者和代碼 [!DNL Google Ads]</a>. <i>以分號分隔多個電信業者（例如T-Mobile、US；T-Mobile、GB）。 若為新行銷活動，預設值為 <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>可識別廣告群組的唯一名稱。 長度上限為255個字元；不會儲存結尾的空白字元（例如，「廣告群組1」會儲存為「廣告群組1」）。 此欄位不適用於行銷活動層級的網站連結或行銷活動層級的裝置目標。</p> |
| [!UICONTROL Ad Group Type] | <p>廣告群組型別： <i>[!UICONTROL Discovery]</i> （僅適用於探索行銷活動）， <i>[!UICONTROL Display]</i> （適用於顯示行銷活動）， <i>[!UICONTROL Search Dynamic]</i> （適用於延展的動態搜尋廣告）， <i>[!UICONTROL Search Standard]</i> （適用於搜尋廣告）、 <i>[!UICONTROL Shopping Product]</i> （適用於購物產品廣告）， <i>[!UICONTROL Shopping Showcase]</i> （不支援建立和編輯），或 <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>（僅適用於CPC行銷活動）最高每次點按成本(CPC)，這是廣告網路上的廣告點按最高金額，無論是否包含貨幣符號和標點符號。 您可以設定廣告群組和關鍵字、產品群組及動態搜尋目標的值。 新關鍵字的預設值繼承自廣告群組層級。 對於產品群組，您可以設定最低產品群組層的值；新層的預設值繼承自父層。</p><p>對於最佳化產品組合中的現有產品群組和動態搜尋目標，更新僅在一天內有效，並在下一個最佳化週期中被覆寫。</p> |
| [!UICONTROL Max Content CPC] | <p>（僅限CPC行銷活動）最高內容每次點按成本(CPC)，這是顯示網路網站中，無論是否包含貨幣符號和標點符號，針對廣告點按而支付的最高金額。 您可以設定和編輯行銷活動中非位置鎖定目標的廣告群組層級的值。</p> |
| [!UICONTROL Audience Target Method] | <p>(僅限搜尋網路上的行銷活動，且現有為唯讀 [!DNL Gmail] 行銷活動)是否：</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>：只對與目標對象相關聯且滿足廣告群組任何其他目標的使用者顯示廣告。</p></li><li><p><i>[!UICONTROL Bid Only]</i>：只要「未與目標對象建立關聯」的使用者符合其他廣告群組層級目標，即可向他們顯示廣告。</p><p>不過，您可以為特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。</p></li></ul> |
| [!UICONTROL Keyword] | 關鍵字字串。 長度上限為80個字元，不超過10個字詞，而且只能包含字母、數字和下列特殊字元：空格 `# $ & _ - " [ ] ' + . / :`</p><p><b>注意：</b></p><ul><li><p>若要在廣告群組或行銷活動層級排除關鍵字，請設定 [!UICONTROL Match Type] 至 <i>[!UICONTROL Negative]</i>. 如果列包含廣告群組名稱，則會為廣告群組排除關鍵字。 如果列不包含廣告群組名稱，則會在整個行銷活動中排除關鍵字。</p></li><li><p>變更 [!DNL Google Ads] keyword或match type會刪除現有的關鍵字，並建立新的關鍵字。</p></li></ul> |
| [!UICONTROL Placement] | （僅使用內容比對的行銷活動）顯示網路中可顯示您廣告的版位。 指定下列其中一項：</p><ul><li><p>網站：輸入有效的URL。 它可以是頂層網域、第一層子網域或具有單一目錄名稱的網域。 URL不能包含問號(？)。 範例：<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>特定頁面上的廣告位置：使用格式 `<URL> >> <location,sublocation>` (例如 `finance.google.com >> Company pages,Top right`)。</p></li><li><p>主題類別：使用語法 `<category::<category> > <subcategory>` 等等(例如 `category::Industries > Energy & Utilities > Oil & Gas`)。</p></li></ul><p><b>注意：</b> 若要在廣告群組或行銷活動層級排除版位，請設定 [!UICONTROL Match Type] 至 <i>[!UICONTROL Negative]</i>. 如果列包含廣告群組名稱，則會針對廣告群組排除該位置。 如果列不包含廣告群組名稱，則會為整個行銷活動排除該位置。</p> |
| [!UICONTROL Auto Target Expression] | <p>(行銷活動設為&quot;時為必要[!UICONTROL Use my website contents to target my ads]「」未啟用；否則為選用)廣告群組的動態搜尋目標。</p><p>對於所有目標，請使用星號(*)。</p><p>若要鎖定最多三個動態搜尋條件，請使用格式 `<category>=<target>`，其中 `<category>` 可包含下列任何類別。 使用「\[blank space\]和\[blank space\]」為個別類別聯結多個目標，並使用「」聯結多個類別[空白] 和 [空白]「。</p><ul><li><p><i>[!UICONTROL Category]</i>：針對具有特定索引的頁面，顯示展開的動態搜尋廣告 [!DNL Google Ads] 內容類別。</p></li><li><p><i>[!UICONTROL URL]</i>：針對具有特定URL的索引頁面，顯示其展開的動態搜尋廣告，其中URL中的任何位置都可能包含值。</p></li><li><p><i>[!UICONTROL Page Title]</i>：針對在頁面標題中有特定文字的索引頁面，顯示展開的動態搜尋廣告。</p></li><li><p><i>[!UICONTROL Page Content]</i>：針對具有特定內容的索引頁面，顯示展開的動態搜尋廣告。</p></li></ul><p>範例： url=shoes.example.com和page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | 任何父級產品群組的階層。<br><br>範例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>產品群組（例如「brand=acme」或「所有產品」）。</p><p><b>注意：</b></p><ul><li><p>當指定的產品群組不存在於 [!UICONTROL Parent Product Groupings] 階層、搜尋、Social和Commerce會建立階層中所需的任何部分。</p></li><li><p>搜尋、社交和Commerce會自動建立&quot;[!UICONTROL All Products]&quot;群組（當您在中建立廣告群組時） [!DNL Google Ads] 預設競標設為廣告群組預設競標的購物行銷活動。 搜尋、社交和Commerce會自動建立&quot;[!UICONTROL Everything Else]「產品群組階層的每個層級具有廣告群組預設競標的群組。 您仍然可以明確建立這些預設群組，並排除它們或變更其競標。</p></li><li><p>每個廣告群組最多可包含八層產品群組，包括「[!UICONTROL All Products]」和其他7個階層。</p></li></ul> |
| [!UICONTROL Partition Type] | 產品群組的資料分割型別： <i>細分</i> （當具有子產品群組時）或 <i>單位</i> （沒有子產品群組時）。 |
| [!UICONTROL Match Type] | <p>對於動態搜尋目標或產品群組：動態搜尋目標或產品群組的關鍵字比對選項： <i>[!UICONTROL Dynamic Ad Target]</i> （新動態搜尋目標的預設值）、 <i>[!UICONTROL Product Group]</i> （新產品群組的預設值）或 <i>[!UICONTROL Negative Product Group]</i> （排除產品群組）。</p><p>關鍵字：關鍵字的關鍵字比對選項： <i>[!UICONTROL Broad]</i>， <i>[!UICONTROL Phrase]</i>， <i>[!UICONTROL Exact]</i>，或 <i>[!UICONTROL Negative]</i> （排除顯示網路上的關鍵字或位置）；搭配購物廣告使用的產品群組具有符合型別 <i>[!UICONTROL Product Group]</i>. 如果您使用 <i>[!UICONTROL Negative]</i>，您也必須包含要排除的相符型別（例如「負面片語」）。</p><p>對於新關鍵字，預設值為 <i>[!UICONTROL Broad]</i>. 只有在編輯具有多個相符型別的關鍵字時，才需要相符型別或關鍵字ID的值。</p><p><b>注意：</b></p><ul><li><p>相符型別不適用於不使用關鍵字的展開動態搜尋廣告。</p></li><li><p>變更的相符型別 [!DNL Google Ads] 關鍵字會刪除現有關鍵字並建立新關鍵字。</p></li><li><p>若為「廣泛比對修飾元」，請選擇「廣泛」，並在需要封閉變體的關鍵字中的任何字詞前插入+ （例如「+紅色+鞋子」需要「紅色」和「鞋子」的封閉變體）。 <b>注意：</b> 廣泛比對修飾詞現在與某些語言的短語比對有相同的比對行為，並且自2021年7月起，您再也無法建立新的廣泛比對修飾詞關鍵字。 另請參閱 [[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/7042511) 以取得詳細資訊。</p> |
| [!UICONTROL First Page Bid] | （包含在產生的Bulksheet中以供參考）在搜尋結果的第一頁上放置廣告所需的競標。 此值未發佈到廣告網路。 |
| [!UICONTROL Quality Score] | （包含在產生的大量表單中以供參考）搜尋引擎已指派給關鍵字的目前品質分數。 此值未發佈到廣告網路。) |
| [!UICONTROL Creative Preferred Devices] | （文字廣告、展開的動態搜尋廣告和增強型網站連結；選用）您偏好顯示廣告的裝置型別： <i>[!UICONTROL All]</i> （預設）或 <i>[!UICONTROL Mobile]</i>. 時間 <i>[!UICONTROL Mobile]</i> 指定，網路會嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示廣告。 否則，網路會在任何裝置型別上顯示廣告。</p><p><b>注意：</b></p><ul><li><p>僅限管理員和 [!DNL Adobe] 帳戶管理員使用者可以編輯此設定。</p></li><li><p>網路不保證會在偏好的裝置型別上顯示廣告。</p></li><li><p>新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。</p></li></ul> |
| [!UICONTROL Ad Title]， [!UICONTROL Ad Title 2]-15 | （僅限展開的文字廣告和回應式搜尋廣告）廣告的頭條，每個標題由垂直垂直垂直線條(&amp;vert；)分隔。 每個廣告標題欄位的長度上限為30個字元或15個雙位元組字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。</p><p>對於回應式搜尋廣告， [!UICONTROL Ad Title]， [!UICONTROL Ad Title 2]、和 [!UICONTROL Ad Title 3] 為必填欄位，而所有其他廣告標題欄位均為選用欄位。 若要刪除非必要欄位的現有值，請使用值 <code>[刪除]</code> （包括括弧）。</p><p>對於回應式搜尋廣告，請使用以下格式插入廣告自訂器： <code>{CUSTOMIZER.AdCustomizerName：DefaultText}</code>，例如 <code>{CUSTOMIZER.Discount：10%}</code></p><p>您無法建立或編輯文字廣告，但可以刪除 [!DNL Google Ads] 2022年6月淘汰。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>（僅限回應式搜尋廣告；選用）釘選對應廣告標題的位置： `[null]` （沒有值，因此廣告標題適用於所有職位）、 <i>1</i>， <i>2</i>，或 <i>3</i>. 例如，如果 [!UICONTROL Ad Title Position] 值為1，則「廣告標題」僅會出現在位置1中。 依預設，所有廣告標題皆為空值（沒有值）。</p><p>若要刪除現有值，請使用值 <code>[刪除]</code> （包括括弧）。</p><p><b>注意：</b> 您可以將多個廣告標題釘選至相同位置。 廣告網路使用已釘選至該位置的其中一個廣告標題。 釘選到位置3的標題可能無法與廣告一起顯示。</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>（僅限延展的動態搜尋廣告、延展的文字廣告和回應式搜尋廣告）廣告內文。 每個說明欄位的長度上限為90個字元或45個雙位元組字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。</p><p>對於回應式搜尋廣告，請使用以下格式插入廣告自訂器： `{CUSTOMIZER.AdCustomizerName:DefaultText}`，例如 `{CUSTOMIZER.Discount:10%}`</p><p>若為展開的動態搜尋廣告，請使用 [!UICONTROL Description Line 1] 和 [!UICONTROL Description Line 2] 僅限。 <b>注意：</b> 對於此廣告型別，變更廣告文案會刪除現有廣告並建立新廣告。</p><p>您無法建立或編輯文字廣告，但可以刪除 [!DNL Google Ads] 2022年6月淘汰。</p><p>對於回應式搜尋廣告， [!UICONTROL Description Line 1] 和 [!UICONTROL Description Line 2] 為必要項，且 [!UICONTROL Description Line 3] 和 [!UICONTROL Description Line 4] 是選用專案。 若要刪除現有值，請使用值 <code>[刪除]</code> （包括括弧）。</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （僅限回應式搜尋廣告；選用）釘選對應說明的位置： `[null]` （沒有值，因此說明適用於所有職位）、 <i>1</i>， <i>2</i>，或 <i>3</i>. 例如，如果 [!UICONTROL Description 1 Position] 的值為1，則 [!UICONTROL Description 1] 只出現在位置1。 依預設，系統不會將任何說明釘選到位置。</p><p>若要刪除現有值，請使用值 `[delete]` （包括括弧）。</p><p><b>注意：</b> 您可以將多個說明釘選到相同位置。 廣告網路使用已釘選至位置的其中一個說明。 釘選到位置2的說明可能無法與廣告一起顯示。 |
| [!UICONTROL Display URL] | 廣告中包含的URL。<br><br>對於展開的動態搜尋廣告， [!DNL Google Ads] 會從網站網域動態產生此值，因此您不需要輸入值。<br><br>針對回應式搜尋廣告，您不需要輸入值。 顯示URL會自動從最終URL的網域中擷取。 您可以選擇使用「路徑1」和「路徑2」欄位自訂URL。<br><br>您無法建立或編輯文字廣告，但可以刪除 [!DNL Google Ads] 2022年6月淘汰。<br><br><b>注意：</b> （具有最終URL的帳戶）顯示URL和最終URL中的網域名稱必須相符。</p> |
| [!UICONTROL Display Path 1] | <p>(展開的文字廣告<span> 和回應式搜尋廣告</span> 僅限)</p><p>（選用）新增至顯示URL的文字，會自動從最終URL擷取。 在URL前面有正斜線(/)。 路徑不能包含正斜線(/)或新行(\n)字元。 長度上限為15個字元或7個雙位元組字元。</p><p>若要插入廣告自訂程式，請使用以下格式，其中 `Default text` 是選填值，可在摘要檔案未包含有效值時插入：&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`</p><p>例如，如果 [!UICONTROL Display Path 1] 為「deals」，則顯示URL為&lt;<i>顯示URL</i>>/deals，例如www.example.com/deals。</p><p>您無法建立或編輯文字廣告，但可以刪除 [!DNL Google Ads] 2022年6月淘汰。</p> |
| [!UICONTROL Display Path 2] | 第二個顯示路徑；請參閱專案 [!UICONTROL Display Path 1].<br><br>範例：如果 [!UICONTROL Display Path 1] 是「交易」和 [!UICONTROL Display Path 2] 為「local」，則顯示URL為&lt;<i>顯示URL</i>>/deals/local，例如www.example.com/deals/local。</p><p>您無法建立或編輯文字廣告，但可以刪除 [!DNL Google Ads] 2022年6月淘汰。</p> |
| [!UICONTROL Promotion Line] | （僅限產品清單廣告）搜尋結果中產品清單所包含的選擇性促銷明細行。 長度上限為45個字元。</p><p>促銷明細行可能會出現在與廣告相關的不同位置（例如廣告下方），視廣告在頁面上出現的位置而定。 |
| [!UICONTROL Link Name] | <p>網站連結文字。 最多可包含25個字元。</p><p>若是新的網站連結，您必須在網站連結列中包含行銷活動名稱。 針對廣告群組層級網站連結，您也必須包含廣告群組名稱。</p><p><b>注意：</b> 35個字元的現有文字仍會顯示在桌上型電腦和平板電腦的廣告中，但不會顯示在行動裝置上。</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | （僅限現有應用程式安裝廣告）行動應用程式執行的作業系統： <i>Android™</i> 或 <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | （僅限現有應用程式安裝廣告） <p>應用程式ID或封裝名稱。 |
| [!UICONTROL Mobile App Name (Google Adwords)] | （僅限現有應用程式安裝廣告）應用程式的名稱。 |
| [!UICONTROL Start Date] | <p>（僅限增強型網站連結）在廣告商的時區及以下其中一種格式中，對網站連結發出投標的第一個日期： <i>m/d/yyyy</i>， <i>m/d/yy</i>， <i>yyyy年m月d日</i>，或 <i>m-d-yy</i>. 新增強型網站連結的預設值為當天。</p><p><b>注意：</b> 新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。</p> |
| [!UICONTROL End Date] | <p>（僅限增強型網站連結）在廣告商的時區及下列其中一種格式中，對網站連結發出競標的最後日期：  <i>m/d/yyyy</i>， <i>m/d/yy</i>， <i>yyyy年m月d日</i>，或 <i>m-d-yy</i>. 預設值為無（無結束日期）。</p><p><b>注意：</b> 新的增強型網站連結只能在具有現有增強型網站連結或沒有網站連結的行銷活動中建立。</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | （僅限現有應用程式安裝廣告）</p><p>（選擇性）防止 [!DNL Google Ads] 向平板電腦使用者顯示廣告。 值可包括 <i>是</i> 和 <i>否</i>. |
| [!UICONTROL Landing Page Suffix] | 要附加至最終URL結尾以追蹤資訊的任何引數。 範例： `param2=value1&param3=value2`<br><br>請參閱&quot;[的點選追蹤格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).」<br><br>較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用 [!DNL Google Ads] 編輯者。 |
| [!UICONTROL Tracking Template] | 追蹤範本會指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在 [!DNL ValueTrack] 引數。 最精細的層級追蹤範本（以關鍵字為最精細）會覆寫所有較高層級的值。<br><br>針對Adobe Advertising轉換追蹤，此專案會在行銷活動設定包含時套用」[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，搜尋、社交和Commerce會自動附加自己的重新導向和追蹤程式碼。<br><br>對於協力廠商重新導向和追蹤，請輸入值。 針對清單 [!DNL ValueTrack] 若要在追蹤範本中指出最終URL，請參閱「可用」一節中的「僅限追蹤範本」引數 [!DNL ValueTrack] 中的引數」 [[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/2375447).<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Base URL/Final URL] | 搜尋引擎使用者按一下您的廣告時，系統會將他們帶往的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 關鍵字層級的基礎/最終URL會覆寫廣告層級和更高級別的URL。<br><br>若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Destination URL] | （包含在產生的大量表單中以供參考；未張貼至搜尋引擎）對於具有目的地URL的帳戶，此URL會將廣告連結至廣告商網站上的基礎URL/登陸頁面（有時透過另一個網站來追蹤點選，然後將使用者重新導向登陸頁面）。 其中包含為「搜尋」、「社交」和「Commerce」行銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，這會根據您的帳戶設定和促銷活動設定中的追蹤引數。 如果您附加搜尋引擎的特定引數，這些引數可能會取代為搜尋、社交和Commerce的同等引數。<br><br>若為具有最終URL的帳戶，此欄會顯示與「基本URL/最終URL」欄相同的值。 |
| [!UICONTROL Custom URL Param] | 要取代的資料 `{custom_code}` 當變數納入搜尋帳戶或促銷活動設定的追蹤引數中時的動態變數。 若要在追蹤URL中插入自訂值，您必須使用「產生追蹤URL」選項上傳大量表單檔案。 |
| [!UICONTROL Creative Type] | 廣告格式： <i>[!UICONTROL Text ad]</i>， <i>[!UICONTROL Expanded text ad]</i>， <i>[!UICONTROL Dynamic search ad]</i> （已棄用的廣告型別）， <i>[!UICONTROL Expanded Dynamic Search ad]</i>， &lt;[!UICONTROL i>Display ad]</i>， <i>[!UICONTROL App Install ad]</i> （已棄用）， <i>[!UICONTROL Image]</i>， <i>[!UICONTROL Product ad<]/i> （購物廣告），或 <i>[!UICONTROL Responsive search ad]</i>. 新廣告的預設為 <i>[!UICONTROL Text ad]</i>.<br><br>需要建立或編輯產品廣告的狀態。 |
| [!UICONTROL Param1] | <p>的數值 `{param1}` 廣告引數，可包含在Bulksheet檔案中任何廣告的廣告復本或顯示URL中。 長度上限為25個字元，您可以包括下列非數字字元：</p><ul><li><p>值前面或後面可附加貨幣符號或代碼。 例如， `£2.000,00` 和 `2000GBP` 有效。</p></li><li><p>值可包含逗號(`,`)或句點(`.`)做為分隔符號，並加上選填的句號(`.`)或逗號(`,`)以取得分數值。 例如， `1,000.00` 和 `2.000,10` 有效。</p></li><li><p>值可以加上前置詞或百分比符號(`%`)，加號(`+`)或減號(`- `)。 例如， `20%`， `208+`、和 `-42.32` 有效。</p></li><li><p>兩個數字可以用正斜線內嵌。 例如， `4/1` 和 `0.95/0.45` 有效。</p></li></ul><p>若要刪除現有值，請使用值 `[delete]` （包括括弧）。</p> |
| [!UICONTROL Param2] | 的數值 `{param2}` 廣告引數，可包含在Bulksheet檔案中任何廣告的廣告復本或顯示URL中。 如需詳細資訊，請參閱Param1的專案。 |
| [!UICONTROL Audience] | 搜尋廣告(RLSA)目標對象的再行銷清單，或促銷活動或廣告群組的已排除對象。 在「目標型別」欄位中指定其為目標或排除專案。 |
| [!UICONTROL Target Type] | （指定對象時）指定的對象是否為 <i>包含</i> （目標）或 <i>排除</i>. |
| [!UICONTROL Campaign Status] | 行銷活動的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>， <i>[!UICONTROL Ended]</i> （無法編輯），或 <i>[!UICONTROL Deleted]</i> （僅限現有行銷活動）。 新行銷活動的預設為 <i>[!UICONTROL Active]</i>. 若要刪除作用中或已暫停的行銷活動，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | 廣告群組的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有廣告群組）。 新廣告群組的預設為 [!UICONTROL Active]. 若要刪除作用中或暫停的廣告群組，請輸入值 `Deleted`. |
| [!UICONTROL Keyword Status] | 關鍵字的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有關鍵字）。 新關鍵字的預設值為 [!UICONTROL Active]. 若要刪除作用中或暫停的關鍵字，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | 廣告的顯示狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Deleted]</i> （僅限現有廣告）， <i>[!UICONTROL Disapproved]</i> （無法編輯），或 <i>[!UICONTROL Paused]</i>. 新廣告的預設為 [!UICONTROL Active]. 若要刪除作用中或暫停的廣告，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | 網站位置的狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有廣告）。 新網站的預設為 <i>作用中。</i> 若要刪除作用中或暫停的位置，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | 動態搜尋目標的狀態： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有目標）。 新目標的預設值為 <i>作用中。</i> 若要刪除作用中或暫停的目標，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | 產品群組的顯示狀態： <i>[!UICONTROL Active]</i> <span>或</span> <i>[!UICONTROL Deleted]</i> （僅限現有產品群組）。 新產品群組的預設值為 <i>[!UICONTROL Active]</i>. 若要刪除使用中的產品群組，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | 網站連結的顯示狀態： <i>作用中或已刪除</i> （僅限現有網站連結）。 新網站連結的預設值為 <i>[!UICONTROL Active]</i>. 若要刪除作用中的網站連結，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | 位置目標的狀態： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted]</i> （僅限現有位置）。 新位置的預設值為 [!UICONTROL Active]. 若要刪除使用中的位置，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | 行銷活動或廣告群組層級RLSA目標或排除的狀態： <i>[!UICONTROL Active]</i> 或 [!UICONTROL Deleted]</i> （僅限現有目標）。 新目標或排除專案的預設值為 <i>[!UICONTROL Active]</i>. 若要刪除作用中目標或排除專案，請輸入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>行銷活動或廣告群組層級裝置目標的狀態： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted]</i>. 對於新的行銷活動和廣告群組，預設值為 <i>[!UICONTROL Active]</i>.</p> |
| \[廣告商特定標籤分類\] | (以廣告商專屬的標籤分類命名，例如「顏色」（針對稱為「顏色」的標籤分類）與實體相關聯的指定分類值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 最大長度為100個字元，此值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤相關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值都不會區分大小寫。 |
| [!UICONTROL Constraints] | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><b>>限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體輸入值。 |
| [!UICONTROL Campaign ID] | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更行銷活動名稱時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」作為促銷活動。 |
| [!UICONTROL Ad Group ID] | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更行銷活動名稱時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」作為廣告群組。 |
| [!UICONTROL Keyword ID] | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更關鍵字時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) &quot;[!UICONTROL AMO ID]「。」 |
| [!UICONTROL Ad ID] | <p>可識別現有廣告的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 對於回應式搜尋廣告，編輯或刪除廣告資料需使用廣告ID或AMO ID。 對於所有其他實體型別，只有在您變更廣告狀態時才需要廣告ID，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID]「。」 不過，如果您未包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。</p><p><b>注意：</b> 如果您編輯a)現有廣告的廣告屬性欄（「狀態」除外）或b)回應式搜尋廣告的任何資料，並且您既不包括 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，則會建立新廣告，且現有廣告不會變更。</p> |
| [!UICONTROL Placement ID] | 可識別網站位置的唯一ID。 只有在您變更或刪除位置時才需要，除非該列包含a)足夠的屬性欄以識別位置或b) &quot;[!UICONTROL AMO ID]「。」 |
| [!UICONTROL Target ID] | 可識別現有自動目標的唯一ID。 只有在您變更或刪除自動鎖定目標時才為必要，除非該列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL Product Group ID] | 可識別現有產品群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄以識別產品群組或b) &quot;[!UICONTROL AMO ID]「。」 |
| [!UICONTROL Sitelink ID] | 可識別現有網站連結的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄以識別網站連結或b) &quot;[!UICONTROL AMO ID]「。」 不過，如果您未包含 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]，且屬性欄符合多個網站連結，則只有其中一個網站連結的狀態會變更。</p><p><b>注意：</b> 如果您編輯網站連結屬性欄，但現有網站連結的狀態除外，而且您既不包括 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]，則會建立新的網站連結，且不會變更現有的網站連結。 |
| [!UICONTROL RLSA Target ID] | 可識別現有行銷活動或廣告群組層級RLSA目標或排除的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除目標或排除專案時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL Device Target ID] | <p>可識別現有行銷活動層級或廣告群組層級裝置目標或排除的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更或刪除目標時才需要，除非列包含&quot;[!UICONTROL AMO ID]」作為目標。</p> |
| [!UICONTROL AMO ID] | （在產生的大量表單中）同步實體的Adobe產生的唯一識別碼。 對於回應式搜尋廣告，除非您包含廣告ID，否則編輯或刪除廣告時需要AMO ID。 若要編輯具有AMO ID之所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則必須使用AMO ID來編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |
| [!UICONTROL EF Error Message] | （包含在產生的大量表單中，以供參考）顯示來自廣告網路的錯誤訊息（關於列中的資料）預留位置；錯誤訊息包含在 [!UICONTROL EF Errors] 檔案。 此值未發佈到廣告網路。 |
| [!UICONTROL SE Error Message] | （包含在產生的大量表單中，以供參考）顯示來自廣告網路的錯誤訊息（關於列中的資料）預留位置；錯誤訊息包含在 [!UICONTROL SE Errors] 檔案。 此值未發佈到廣告網路。 |
| [!UICONTROL Exemption Request] | （包含在產生的大量表單中以供參考）顯示任何專案名稱和文字的預留位置 [!DNL Google Ads] 廣告違反的廣告原則。 |
| [!UICONTROL Retail Hash] | (包含於使用進階Campaign Management產生的大量表單中以供參考)英數字元雜湊代碼(例如f9639f40cdf56524b541e5dacf55a991)，表示專案是使用進階(ACM)檢視產生的。 |

[^1]： [!DNL Excel] 開啟檔案時，會將大數字轉換為科學記號(例如2.12E+09用於2115585666)。 若要以標準標籤法檢視數字，請選取欄中的任何儲存格，然後按一下公式列內的「 」。

## 建立、編輯或刪除每個帳戶元件所需的欄位 {#bulksheet-fields-per-component-google}

以下小節包括與特定帳戶實體相關的欄位。

>[!NOTE]
>
>當欄位不適用於動作時，在欄位中輸入的任何值都會被忽略。

### 行銷活動欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Campaign Budget] | 建立行銷活動所需。 |
| [!UICONTROL Delivery Method] | 建立行銷活動所需。 |
| [!UICONTROL Channel Type] | 建立行銷活動所需。 |
| [!UICONTROL Networks] | 建立行銷活動所需。 |
| [!UICONTROL DSA Domain Name] | 在搜尋網路上建立具有動態搜尋廣告的行銷活動所需。 |
| [!UICONTROL DSA Domain Language] | 在搜尋網路上建立具有動態搜尋廣告的行銷活動所需。 |
| [!UICONTROL Campaign Priority] | 建立購物行銷活動所需。 |
| [!UICONTROL Merchant ID] | 建立購物行銷活動所需。 |
| [!UICONTROL Sales Country] | 建立購物行銷活動所需。 |
| [!UICONTROL Product Scope Filter] | （購物行銷活動）選填 |
| [!UICONTROL Languages] | 可選 |
| [!UICONTROL Device Targets] | 可選 |
| [!UICONTROL Device Targets (Google Adwords)] | 可選 |
| [!UICONTROL Mobile Carriers (Google Adwords)] | 可選 |
| [!UICONTROL Audience Target Method] | 不適用 |
| [!UICONTROL Landing Page Suffix] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Campaign Status] | 僅刪除行銷活動時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 只有在您變更行銷活動名稱時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」作為促銷活動。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 廣告群組欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Networks] | 不適用 |
| [!UICONTROL GDN Custom Bid Level] | 可選 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Group Type] | 建立廣告群組所需。 |
| [!UICONTROL Max CPC] | 可選 |
| [!UICONTROL Max Content CPC] | 可選 |
| [!UICONTROL Audience Target Method] | 必填 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Ad Group Status] | 僅刪除廣告群組時需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Ad Group ID] | 只有在您變更廣告群組名稱時才需要，除非該列包含&quot;[!UICONTROL AMO ID]」作為廣告群組。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 關鍵字欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Max CPC] | 可選 |
| [!UICONTROL Keyword] | 必填 |
| [!UICONTROL Match Type] | 需要符合型別或關鍵字ID的值，才能編輯或刪除具有多個符合型別的關鍵字。 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Base URL/Final URL] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Param1] | 可選 |
| [!UICONTROL Param2] | 可選 |
| [!UICONTROL Keyword Status] | 僅刪除關鍵字時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Keyword ID] | 只有在編輯或刪除關鍵字時才需要，除非列包含a)足夠的屬性欄以識別關鍵字或b) &quot;[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 位置欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Max Placement CPC (Google Adwords)] | 可選 |
| [!UICONTROL Max Placement CPM (Google Adwords)] | 可選 |
| [!UICONTROL Placement] | 必填 |
| [!UICONTROL Match Type] | 必填 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Base URL/Final URL] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Placement Status] | 只有在刪除位置時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Placement ID] | 只有在編輯或刪除位置時才需要，除非該列包含a)足夠的屬性欄來識別位置或b) &quot;[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 已展開的動態搜尋廣告

此廣告型別現在稱為「動態搜尋廣告」，位於 [!DNL Google Ads]. 如需建立動態搜尋廣告的詳細資訊，請參閱&quot;[實作 [!DNL Google Ads] 動態搜尋廣告](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html).」

對於此廣告型別，請使用「[!UICONTROL Creative (except RSA)]「」列在 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Creative Preferred Devices] | 可選 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 需要建立廣告或編輯說明。 <b>注意：</b> 對於此廣告型別，變更廣告文案會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Display URL] | 必填 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Creative Type] | 需要建立或編輯產品廣告的狀態。 |
| [!UICONTROL Ad Status] | 刪除廣告的必要專案。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID].」 不過，如果您未包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 產品清單/購物廣告欄位

如需建立購物廣告的詳細資訊，請參閱&quot;[實作 [!DNL Google Ads] 購物宣傳](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html).」

對於此廣告型別，請使用「[!UICONTROL Creative (except RSA)]「」列在 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Promotion Line] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Base URL/Final URL] | 可選 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Creative Type] | 需要建立或編輯產品廣告的狀態。 |
| [!UICONTROL Ad Status] | 刪除廣告的必要專案。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID].」 不過，如果您未包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 回應式搜尋廣告欄位

對於此廣告型別，請使用「[!UICONTROL Responsive Search Ad]「」列在 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 | |
| [!UICONTROL Ad Title]， [!UICONTROL Ad Title 2]-15 | 對於回應式搜尋廣告， [!UICONTROL Ad Title]， [!UICONTROL Ad Title 2]、和 [!UICONTROL Ad Title 3] 是建立廣告的必要欄位，而所有其他廣告標題欄位均為選用欄位。 若要刪除非必要欄位的現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | 可選 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | 對於回應式搜尋廣告， [!UICONTROL Description Line 1] 和 [!UICONTROL Description Line 2] 建立廣告所需，以及 [!UICONTROL Description Line 3] 和 [!UICONTROL Description Line 4] 是選用專案。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | 可選 |
| [!UICONTROL Display Path 1] | 可選 |
| [!UICONTROL Display Path 2] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Base URL/Final URL] | 建立廣告的必要專案。 |
| [!UICONTROL Custom URL Param] | 可選 |
| [!UICONTROL Creative Type] | 可選 |
| [!UICONTROL Ad Status] | 刪除廣告的必要專案。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 除非列包含&quot;，否則必須編輯或刪除廣告[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非您包含廣告ID，否則必須編輯或刪除廣告。 |

### 文字廣告欄位

對於此廣告型別，請使用「[!UICONTROL Creative (except RSA)]「」列在 [!UICONTROL Download Bulksheet] 對話方塊。

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

>[!NOTE]
>
>展開的文字廣告已於2022年6月淘汰。 您只能刪除現有的文字廣告。

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Creative Preferred Devices] | 唯讀 |
| [!UICONTROL Ad Title]，廣告標題2-3 | 唯讀 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] 唯讀 |
| [!UICONTROL Display URL] | 唯讀 |
| [!UICONTROL Display Path 1] | 唯讀 |
| [!UICONTROL Display Path 2] | 唯讀 |
| [!UICONTROL Tracking Template] | 唯讀 |
| [!UICONTROL Base URL/Final URL] | 唯讀 |
| [!UICONTROL Custom URL Param] | 唯讀 |
| [!UICONTROL Creative Type] | 可選 |
| [!UICONTROL Ad Status] | 必填 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Ad ID] | 只有在您變更廣告狀態時才需要，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID].」 不過，如果您未包含 [!UICONTROL Ad ID] 也不 [!UICONTROL AMO ID]，且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 動態搜尋目標（自動鎖定目標）欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Max CPC] | 可選 |
| [!UICONTROL Auto Target Expression] | 只有在行銷活動設定為&quot;時才需要[!UICONTROL Use my website contents to target my ads]「」未啟用。 |
| [!UICONTROL Match Type] | 可選 |
| [!UICONTROL Target Status] | 刪除目標所需 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Target ID] | 只有在您變更或刪除自動鎖定目標時才為必要，除非該列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 購物產品群組欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Max CPC] | 建立產品群組時需要。 |
| [!UICONTROL Parent Product Groupings] | 必填 |
| [!UICONTROL Product Grouping] | 必填 |
| [!UICONTROL Partition Type] | 建立產品群組時需要。 |
| [!UICONTROL Match Type] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Base URL/Final URL] | 必填 |
| [!UICONTROL Product Group Status] | 僅刪除產品群組時才需要。 |
| \[廣告商特定標籤分類\] | 可選 |
| [!UICONTROL Constraints] | 可選 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Product Group ID] | 只有在您變更或刪除產品群組時才需要，除非該列包含a)足夠的屬性欄以識別產品群組或b) &quot;[!UICONTROL AMO ID].」 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 行銷活動層級和廣告群組層級網站連結欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 廣告群組層級網站連結的必要專案。 不適用於行銷活動層級的網站連結。 |
| [!UICONTROL Creative Preferred Devices] | 可選 |
| [!UICONTROL Link Name] | 必填 |
| [!UICONTROL Start Date] | 可選 |
| [!UICONTROL End Date] | 可選 |
| [!UICONTROL Tracking Template] | 可選 |
| [!UICONTROL Base URL/Final URL] | 必填 |
| [!UICONTROL Sitelink Status] | 只有在刪除網站連結時才需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 可選 |
| [!UICONTROL Sitelink ID] | 只有在您變更或刪除網站連結時才需要，除非該列包含a)足夠的屬性欄以識別網站連結或b) &quot;[!UICONTROL AMO ID].」 不過，如果您未包含 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]  且屬性欄與多個網站連結相符，則只有其中一個網站連結的狀態會變更。<br><br><b>注意：</b> 如果您編輯網站連結屬性欄，但 [!UICONTROL Status] 若為現有sitelink，則不會包含 [!UICONTROL Sitelink ID] 也不 [!UICONTROL AMO ID]，則會建立新的網站連結，且不會變更現有的網站連結。 |
| [!UICONTROL AMO ID] | 除非包含實體ID和父項實體ID，否則需要編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 位置目標

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Location] | 必填 |
| [!UICONTROL Location Type] | 可選 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Location Status] | 僅刪除位置目標時需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL AMO ID] | 編輯或刪除資料所需，除非您將 [!UICONTROL Campaign ID].<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 行銷活動層級和廣告群組層級裝置目標欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Device] | 需要建立或編輯裝置目標。 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Ad Group Name] | 廣告群組層級裝置目標的必要專案。 不適用於行銷活動層級的裝置目標。 |
| [!UICONTROL Device Target Status] | 僅刪除裝置目標時才需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 選用；僅適用於廣告群組層級裝置目標。 |
| [!UICONTROL Device Target ID] | 只有在您變更或刪除目標時才需要，除非列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL AMO ID] | 除非您包含裝置目標ID，否則必須編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

### 行銷活動等級和廣告群組等級RLSA目標/排除欄位

如需每個資料欄位的說明，請參閱&quot;[所有可用資料欄位](#bulksheet-fields-all-google).」

| 欄位 | 必填？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每一列包含&quot;，否則為必要[!UICONTROL AMO ID]」作為實體。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Bid Adjustment] | 可選 |
| [!UICONTROL Ad Group Name] | 廣告群組層級目標和排除專案需要此專案。 不適用於行銷活動層級的目標和排除。 |
| [!UICONTROL Audience] | 建立新目標或排除專案時需要。 |
| [!UICONTROL Target Type] | 建立新目標或排除專案時需要。 |
| [!UICONTROL RLSA Target Status] | 只有在刪除目標或排除專案時才需要。 |
| [!UICONTROL Campaign ID] | 可選 |
| [!UICONTROL Ad Group ID] | 選用；僅適用於廣告群組層級目標和排除專案。 |
| [!UICONTROL RLSA Target ID] | 只有在您變更或刪除目標時才需要，除非列包含&quot;[!UICONTROL AMO ID]」作為目標。 |
| [!UICONTROL AMO ID] | 除非包含RLSA目標ID，否則必須編輯或刪除資料。<br><br>搜尋、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [可在大量表單中執行的作業](bulksheet-operations.md)
>* [支援的大量表單檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>* [的點選追蹤格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)
