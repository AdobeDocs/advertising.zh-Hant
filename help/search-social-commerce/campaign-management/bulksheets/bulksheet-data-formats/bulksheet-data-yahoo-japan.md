---
title: ' [!DNL Yahoo! Japan] 帳戶的Bulksheet資料'
description: 參考 [!DNL Yahoo! Japan] 帳戶之已下載大量表單中的標題欄位和資料欄位。
exl-id: 78eb41ce-3854-454c-adf2-ba0339e2aef7
feature: Search Bulksheets
source-git-commit: 5c750153ff9e4be2d02f572d96b171d7aa293dd9
workflow-type: tm+mt
source-wordcount: '2672'
ht-degree: 0%

---

# 附錄 — [!DNL Yahoo! Japan]帳戶的Bulksheet資料

您可以大量下載[!DNL Yahoo! Japan]帳戶的資料，但無法上傳或張貼大量工作表到廣告網路。

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Budget,Delivery Method,Mobile Bid Adjustment,Location,Location Type,Ad Group Name,Max CPC,Keyword,Match Type,First Page Bid, Quality Score,Ad Name (Yahoo JP),Creative Preferred Devices,Ad Title,Ad Title2,Description Line 1,Description Line 2,Creative Type,Display URL,Display Path 1,Display Path 2,Base URL/Final URL,Destination URL,Tracking Template,Campaign Status,Ad Group Status,Keyword Status,Ad Status,Location Status,[Advertiser-specific Label Classification],Constraints,Campaign ID,Ad Group ID,Keyword ID,Ad ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用的資料欄位

>[!TIP]
>
>下表為寬表格。 若要擴大檢視區域，您可以按一下左窗格頂端的![隱藏左窗格](/help/dsp/assets/hide-left-pane.png "隱藏左窗格")和右窗格頂端的![隱藏右側窗格](/help/dsp/assets/hide-right-pane.png "隱藏右側窗格")，暫時隱藏目錄和右窗格。 您也可以使用表格底部的卷軸來檢視完整內容。

| 欄位 | Campaign | 廣告群組 | 關鍵字 | 文字廣告 | 行銷活動位置目標 | 說明 |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Acct Name] | 必要/選用 | 必要/選用 | 必要/選用 | 必要/選用 | 必要/選用 | 可識別廣告網路帳戶的唯一名稱。 除非每一列包含實體的&quot;[!UICONTROL AMO ID]&quot;，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 必填 | 必填 | 可識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Campaign Budget] | 必要： Create<br><br>選用：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的每日支出限制，無論是否包含貨幣符號和標點符號。 此值會覆寫，但不能超過科目預算。 |
| [!UICONTROL Delivery Method] | 必要： Create<br><br>選用：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 每天顯示行銷活動廣告的速度如何：<ul><li>*[!UICONTROL Standard (Distributed)]* （新行銷活動的預設值）：將您的廣告印象分散在一天當中。</li><li>*[!UICONTROL Accelerated]：*&#x200B;在達到預算之前，儘可能顯示您的廣告。 因此，您的廣告可能不會在當天稍後出現。</li></ul> |
| [!UICONTROL Mobile Bid Adjustment] | 可選 | 可選 | 不適用 | 不適用 | 不適用 | 無論是在行銷活動層級或廣告群組層級，是否要在行動裝置上競標廣告：<ul><li>若要使用現有的行動競標調整，請將此項留空。</li><li>若要不競標行動裝置上的廣告，請輸入`-100`。</li><li>若要在行動裝置上競標與桌上型電腦和平板電腦裝置上的廣告競標（0%差異），請輸入`0`。 對於新的行銷活動，您也可以將此項留空。</li><li>若要使用不同出價在行動裝置上競標廣告，請輸入增加或減少出價的百分比。 值可以從`-90`到`300`。</li></ul>如果您在行銷活動層級排除裝置，就無法覆寫廣告群組層級的排除。<br><br><b>附註：</b><ul><li>廣告群組會繼承行銷活動層級設定，但您可以覆寫這些設定。</li><li>如果您將行銷活動指派給最佳化的產品組合，則最佳化功能會自動決定基本關鍵字層級的競標，以協助產品組合達成其目標。 接著，廣告網路會依行動廣告的指定方式調整競標。</li><li>如果您將行銷活動或廣告群組指派給最佳化的產品組合：<ul><li>最佳化功能會自動決定基本關鍵字層級的競標，以協助產品組合達成其目標。 搜尋網路接著會根據行動廣告的指定來調整競標。</li><li>如果產品組合設定為「[!UICONTROL Auto-optimize Bid Adjustment Values]」，則最佳化功能會變更廣告群組層級的競標調整，只要其計算的理想值落在產品組合設定中指定的最小值和最大值內，且廣告群組不排除行動廣告的競標。</li></ul></li></ul> |
| [!UICONTROL Location] | 不適用 | 不適用 | 不適用 | 不適用 | 可選 | 為行銷活動放置廣告的地理位置。 若為城市，請使用「&lt;<i>城市</i>>、&lt;</i>縣</i>>」格式（例如安達致、東京）。 若要排除位置，請在位置前面加上減號(`-`)。 如果您未輸入促銷活動的特定值，則會鎖定所有位置。 |
| [!UICONTROL Location Type] | 不適用 | 不適用 | 不適用 | 不適用 | 必要/選用 | （當您鎖定特定位置時為必要）指定的位置是型別[!UICONTROL Prefecture]還是[!UICONTROL City]。 |
| [!UICONTROL Ad Group Name] | 不適用 | 必填 | 必填 | 必填 | 不適用 | 促銷活動中的唯一廣告群組名稱。 長度上限為50個字元。 |
| [!UICONTROL Max CPC] | 不適用 | 可選 | 可選 | 不適用 | 不適用 | 最高每次點按成本(CPC)，這是搜尋網路上廣告點按的最高金額，無論是否包含貨幣符號和標點符號。 您可以設定廣告群組和關鍵字的值。 新關鍵字的預設值繼承自廣告群組層級。 |
| [!UICONTROL Keyword] | 選填/不適用 | 選填/不適用 | 必填 | 不適用 | 不適用 | 關鍵字字串。 [!DNL Yahoo! Japan]關鍵字和相符型別是可變的，這表示您可以編輯它們而不刪除現有的關鍵字。<br><br>若要在廣告群組或行銷活動層級排除關鍵字，請將[!UICONTROL Match Type]設為「負面」。 如果列包含廣告群組名稱，則會為廣告群組排除關鍵字。 如果列不包含廣告群組名稱，則會在整個行銷活動中排除關鍵字。 |
| [!UICONTROL Match Type] | 選填/不適用 | 選填/不適用 | 可選：建立<br><br>必要/可選：編輯或刪除 | 不適用 | 不適用 | 關鍵字的關鍵字比對選項： *[!UICONTROL Broad]* （新關鍵字的預設）、*[!UICONTROL Exact]*、*[!UICONTROL Phrase]*、*[!UICONTROL Negative Broad]或&#x200B;*[!UICONTROL Negative Exact]*。 在行銷活動層級或廣告群組層級定義負面關鍵字。 [!DNL Yahoo! Japan]關鍵字和相符型別是可變的，這表示您可以編輯它們而不刪除現有的關鍵字。<br><br>只有在編輯包含多個相符型別的關鍵字時，才需要相符型別或關鍵字識別碼的值。 |
| [!UICONTROL First Page Bid] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考）在搜尋結果的第一頁上放置廣告所需的競標。 此值未發佈到廣告網路。 |
| [!UICONTROL Quality Score] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考）廣告網路已指派給關鍵字的目前品質分數。 此值未發佈到廣告網路。 |
| [!UICONTROL Ad Name (Yahoo JP)] | 不適用 | 不適用 | 不適用 | 可選：建立<br><br>必要/可選：編輯或刪除 | 不適用 | 在廣告群組中識別廣告影像的唯一名稱。 長度上限為50個字元。 除非您對資料列使用[!UICONTROL AMO ID]或[!UICONTROL Ad ID]，否則為必要。 |
| [!UICONTROL Creative Preferred Devices] | 不適用 | 不適用 | 不適用 | 可選 | 不適用 | 您偏好顯示廣告的裝置型別： *[!UICONTROL All]* （預設）或&#x200B;*[!UICONTROL Mobile]*。 針對[!UICONTROL Mobile]，廣告網路會嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示廣告。 否則，會在任何裝置型別上顯示廣告。<br><br>只有系統管理員和[!DNL Adobe]帳戶管理員使用者可以編輯此設定。 |
| [!UICONTROL Ad Title] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 廣告的標題。 長度上限為30個單位元組或15個雙位元組字元。 變更廣告文案會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Ad Title 2] | 不適用 | 不適用 | 不適用 | 必填/不適用 | 不適用 | （僅限延伸文字廣告）第二個標題。 長度上限為30個字元或15個雙位元組字元。 變更廣告文案會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Description Line 1] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 廣告內文。 延伸文字廣告的長度上限為80個單位元組或40個雙位元組字元。 變更廣告文案會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Description Line 2] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | （僅限標準文字廣告）廣告內文的第二行。 長度上限為38個單位元組或19個雙位元組字元。 變更廣告文案會刪除現有廣告並建立新廣告。 <b>附註：</b> [!DNL Yahoo! Japan Ads]不再允許建立及編輯標準文字廣告。 |
| [!UICONTROL Creative Type] | 不適用 | 不適用 | 不適用 | 可選 | 不適用 | 廣告格式：<ul><li>*[!UICONTROL Text]* （新廣告的預設值）：可能在電腦、平板電腦和智慧型手機上顯示的文字廣告。</li><li>*[!UICONTROL Mobile]：*&#x200B;已棄用。</li></ul> |
| [!UICONTROL Display URL] | 不適用 | 不適用 | 不適用 | 必要/ n/a：建立<br><br>選用/ n/a：編輯或刪除 | 不適用 | （僅限現有標準文字廣告；唯讀）廣告中顯示的URL。 長度上限為255個單位元組或127個雙位元組字元。 此外，顯示URL和登陸頁面URL的網域必須相同。 <b>附註：</b> [!DNL Yahoo! Japan Ads]已取代建立和編輯標準文字和延伸文字廣告。 |
| [!UICONTROL Display Path 1]，[!UICONTROL Display Path 2] | 不適用 | 不適用 | 不適用 | 選填/不適用 | 不適用 | （僅限延伸文字廣告；選用）新增至顯示URL的文字，會自動從最終URL擷取。 在URL前面有正斜線(`/`)。 路徑不能包含正斜線(`/`)或新行(`\n`)字元。 長度上限為15個字元或7個雙位元組字元。<br><br>若要插入廣告自訂程式，請使用下列格式，其中`Default text`是當摘要檔案未包含有效值時要插入的選用值：<ul><li>[!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`</li><li>[!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`</li></ul>例如，如果[!UICONTROL Display Path 1]是「交易」，則顯示URL將是`&lt;display URL&gt;/deals`，例如www.example.com/deals。 |
| [!UICONTROL Base URL/Final URL] | 不適用 | 不適用 | 可選 | 必填 | 不適用 | 使用者按一下您的廣告時，系統會將使用者帶入的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 關鍵字層級的基礎/最終URL會覆寫廣告層級和更高級別的URL。 |
| [!UICONTROL Destination URL] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考；未張貼至廣告網路）對於具有目的地URL的帳戶，此URL是將廣告連結至廣告商網站上的基礎URL/登陸頁面的URL （有時透過另一個網站來追蹤點選，然後將使用者重新導向登陸頁面）。 其中包含為「搜尋」、「社交」和「Commerce」行銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，這會根據您的帳戶設定和促銷活動設定中的追蹤引數。 如果您附加廣告網路特定引數，這些引數可能會取代為搜尋、社交和Commerce的同等引數。<br><br>對於具有最終URL的帳戶，此欄會顯示與基礎URL/最終URL欄相同的值。<br><br>關鍵字或位置層級的目的地URL會覆寫廣告層級的URL。 |
| [!UICONTROL Tracking Template] | 可選 | 可選 | 可選 | 可選 | 可選 | （可選）追蹤範本或追蹤URL，這會指定所有離登陸網域重新導向和追蹤引數，並將最終/登陸頁面URL內嵌在引數中。 使用引數`!{lpurl}`指示登陸頁面URL。 範例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重新導向。<br><br>您可以選擇新增協力廠商重新導向與追蹤。<br><br>若為Adobe Advertising轉換追蹤，此追蹤會在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用，當您儲存記錄時，Search、Social和Commerce會自動為其自己的重新導向和追蹤代碼加上前置詞。<br><br>最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。 |
| [!UICONTROL Campaign Status] | 可選：建立或編輯<br><br>必要：刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的顯示狀態： *[!UICONTROL Active]* （新行銷活動的預設值）、*[!UICONTROL Paused]*、*[!UICONTROL Ended]* （僅限現有行銷活動）或&#x200B;*[!UICONTROL Deleted]* （僅限現有行銷活動）。 |
| [!UICONTROL Ad Group Status] | 不適用 | 可選：建立或編輯<br><br>必要：刪除 | 不適用 | 不適用 | 不適用 | 廣告群組的顯示狀態：  *[!UICONTROL Active]*、*[!UICONTROL Paused]*&#x200B;或&#x200B;*[!UICONTROL Deleted]* （僅限現有廣告群組）。 新廣告群組的預設值為[!UICONTROL Active]。 若要刪除作用中或暫停的廣告群組，請輸入值`Deleted`。 |
| [!UICONTROL Keyword Status] | 不適用 | 不適用 | 可選：建立或編輯<br><br>必要：刪除 | 不適用 | 不適用 | 關鍵字的顯示狀態： *[!UICONTROL Active]*、*[!UICONTROL Deleted]* （僅限現有關鍵字）、*[!UICONTROL Disapproved]* （無法編輯）、*[!UICONTROL Paused]* （僅限現有關鍵字）或&#x200B;*[!UICONTROL Pending]* （無法編輯）。 新關鍵字的預設值為[!UICONTROL Active]。 若要刪除關鍵字，請輸入值`Deleted`。 |
| [!UICONTROL Ad Status] | 不適用 | 不適用 | 不適用 | 可選：建立或編輯<br><br>必要：刪除 | 不適用 | 廣告的顯示狀態： *[!UICONTROL Active]* （新廣告的預設）、*[!UICONTROL Deleted]* （僅限現有廣告）、*[!UICONTROL Disapproved]* （無法編輯）、*[!UICONTROL Paused]*&#x200B;或&#x200B;*[!UICONTROL Pending]* （無法編輯）。 新廣告的預設值為[!UICONTROL Active]。 若要刪除廣告，請輸入值`Deleted`。 |
| [!UICONTROL Location Status] | 不適用 | 不適用 | 不適用 | 不適用 | 可選 | 位置目標的狀態： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Deleted]* （僅限現有位置）。 新位置的預設值為[!UICONTROL Active]。 若要刪除使用中的位置，請輸入值`Deleted`。 |
| \[廣告商特定標籤分類\] | 可選 | 可選 | 可選 | 可選 | 可選 | (以廣告商專屬的標籤分類命名，例如「顏色」（針對稱為「顏色」的標籤分類）與實體相關聯的指定分類值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 最大長度為100個字元，此值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤建立關聯。 <br><br>分類名稱和分類值不區分大小寫。 |
| [!UICONTROL Constraints] | 可選 | 可選 | 可選 | 可選 | 不適用 | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><br>限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體輸入值。 |
| [!UICONTROL Campaign ID] | 不適用：建立<br><br>必要/選用：編輯或刪除 | 可選 | 可選 | 可選 | 不適用 | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它前面必須是單引號(`'`)。[^1]只有當您變更促銷活動名稱時才需要，除非該列包含促銷活動的「[!UICONTROL AMO ID]」。 |
| [!UICONTROL Ad Group ID] | 不適用 | 不適用：建立<br><br>必要/選用：編輯或刪除 | 可選 | 可選 | 不適用 | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它前面必須是單引號(`'`)。[^1]只有在您變更廣告群組名稱時才需要，除非該列包含廣告群組的「[!UICONTROL AMO ID]」。 |
| [!UICONTROL Keyword ID] | 不適用 | 不適用 | 不適用：建立<br><br>必要/選用：編輯<br><br>必要：刪除 | 不適用 | 不適用 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它前面必須是單引號(`'`)。[^1]只有在編輯或刪除關鍵字時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL Ad ID] | 不適用 | 不適用 | 不適用 | 不適用：建立<br><br>必要/選用：編輯或刪除 | 不適用 | 可識別現有廣告的唯一ID。 在CSV和TSV檔案中，它前面必須是單引號(`'`)。[^1]對於回應式搜尋廣告，需要[!UICONTROL Ad ID]或[!UICONTROL AMO ID]才能編輯或刪除廣告資料。 對於所有其他實體型別，只有在您變更廣告狀態時才需要[!UICONTROL AMO ID]，除非該列包含a)足夠的廣告屬性欄以識別廣告或b) &quot;[!UICONTROL AMO ID]&quot;。 不過，如果您既不包含[!UICONTROL Ad ID]也不包含[!UICONTROL AMO ID]，而且廣告屬性欄符合多個廣告，則只有其中一個廣告的狀態會變更。<br><br><b>注意：</b>如果您編輯a)現有廣告的廣告屬性欄（[!UICONTROL Status]除外）或b)回應式搜尋廣告的任何資料，而且您既未包含[!UICONTROL Ad ID]也未包含[!UICONTROL AMO ID]，則會建立新廣告，且現有廣告不會變更。 |
| [!UICONTROL AMO ID] | 不適用：建立<br><br>選用：編輯或刪除 | 不適用：建立<br><br>選用：編輯或刪除 | 不適用：建立<br><br>選用：編輯或刪除 | 不適用：建立<br><br>選用：編輯或刪除 | 不適用 | （在產生的Bulksheets中）同步實體的[!DNL Adobe]產生的唯一識別碼。 針對回應式搜尋廣告，除非您包含[!UICONTROL Ad ID]，否則需要[!UICONTROL AMO ID]才能編輯或刪除廣告。 若要編輯具有[!UICONTROL AMO ID]之所有其他實體型別的資料，必須有[!UICONTROL AMO ID]才能編輯或刪除資料，除非您包含實體ID和父實體ID。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |
| [!UICONTROL EF Error Message] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考）用來顯示來自搜尋、社交和Commerce的錯誤訊息的預留位置，這些錯誤訊息涉及列中的資料；錯誤訊息包含在[!UICONTROL EF Errors]個檔案中。 此值未發佈到廣告網路。 |
| [!UICONTROL SE Error Message] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考）顯示來自廣告網路的錯誤訊息的預留位置，這些訊息與資料列中的資料有關；錯誤訊息包含在[!UICONTROL SE Errors]個檔案中。 此值未發佈到廣告網路。 |

[^1]： Excel在開啟檔案時將大數轉換為科學記號(例如2115585666的2.12E+09)。 若要以標準標籤法檢視數字，請選取欄中的任何儲存格，然後按一下公式列內的「 」。

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [您可以在大量表單中執行的作業](bulksheet-operations.md)
>* [支援的Bulksheet檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)的點選追蹤格式
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)
