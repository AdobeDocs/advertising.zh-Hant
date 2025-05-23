---
title: ' [!DNL Baidu] 帳戶必要的大量表單資料'
description: 參考 [!DNL Baidu] 帳戶大量表單中必要的標題欄位和資料欄位。
exl-id: 9680cb37-50d4-4b4b-b359-ac54267cd5e6
feature: Search Bulksheets
source-git-commit: 5c750153ff9e4be2d02f572d96b171d7aa293dd9
workflow-type: tm+mt
source-wordcount: '1964'
ht-degree: 0%

---

# 附錄 — [!DNL Baidu]帳戶需要的大量表單資料

若要大量建立和更新[!DNL Baidu]行銷活動資料，您可以使用特別針對[!DNL Baidu]帳戶格式化的搜尋、社交和Commerce大量表單檔案。 您可以a) [以必要的檔案格式](../bulksheet-download.md)產生現有帳戶的批次工作表檔案，或b)手動建立這些檔案（如需支援之檔案格式的一般資訊，請參閱[支援的批次工作表檔案格式](bulksheet-file-formats.md)）。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Budget,Location,Excluded IPs (Baidu), Ad Serving (Baidu),Ad Group Name,Max CPC,Keyword,Match Type,Ad Title,Description Line 1,Description Line 2,Display URL,Base URL,Destination URL,Custom URL Param,Campaign Status,Ad Group Status,Keyword Status,Ad Status,Location Status,[Advertiser-specific Label Classification],Campaign ID,Ad Group ID,Keyword ID,Ad ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用的資料欄位

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>下表為寬表格。 若要擴大檢視區域，您可以按一下左窗格頂端的![隱藏左窗格](/help/dsp/assets/hide-left-pane.png "隱藏左窗格")和右窗格頂端的![隱藏右側窗格](/help/dsp/assets/hide-right-pane.png "隱藏右側窗格")，暫時隱藏目錄和右窗格。 您也可以使用表格底部的卷軸來檢視完整內容。

| 欄位 | Campaign | 廣告群組 | 關鍵字 | 文字廣告 | 位置目標 | 說明 |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Acct Name] | 必要/選用 | R/O | 必要/選用 | 必要/選用 | 必要/選用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 必填 | 必填 | 可識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Campaign Budget] | 必要： Create<br>選用：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的每日支出限制，無論是否包含貨幣符號和標點符號。 此值會覆寫，但不能超過科目預算。 |
| [!UICONTROL Location] | 不適用 | 不適用 | 不適用 | 不適用 | 必填 | 為行銷活動放置廣告的地理位置。 若要排除位置，請在位置前面加上減號(`-`)。 如果您未輸入促銷活動的特定值，則會鎖定所有位置。 |
| [!UICONTROL Excluded IPs (Baidu)] | 可選 | 不適用 | 不適用 | 不適用 | 不適用 | 不應顯示廣告之網站的IP位址。 以逗號分隔多個值。 |
| [!UICONTROL Ad Serving (Baidu)] | 可選 | 不適用 | 不適用 | 不適用 | 不適用 | 在廣告群組中相互關聯地傳遞有效廣告的頻率：<ul><li><i>輪播</i> （新行銷活動的預設值）：您的每個廣告進入廣告拍賣的次數大致相同，可讓Search、Social和Commerce不僅根據點進率，而且也根據轉換為您的廣告評分。</li><li><i>最佳化：</i>廣告網路偏好高點進率與高品質分陣列合的廣告。 這些廣告更常進入廣告拍賣，一段時間過後，系統會偏好使用單一廣告。 此結果可能與您的業務和最佳化目標不一致。</li></ul> |
| [!UICONTROL Ad Group Name] | 不適用 | 必填 | 必填 | 必填 | 不適用 | 可識別廣告群組的唯一名稱。 |
| [!UICONTROL Max CPC] | 不適用 | O | O | 不適用 | 不適用 | 最高每次點按成本(CPC)，這是搜尋網路上廣告點按的最高金額，無論是否包含貨幣符號和標點符號。 您可以設定廣告群組和關鍵字的值。 新關鍵字的預設值繼承自廣告群組層級。 |
| [!UICONTROL Keyword] | 選填/不適用 | 選填/不適用 | 必填 | 不適用 | 不適用 | 關鍵字字串。<br><br>若要在廣告群組或行銷活動層級排除關鍵字，請將[!UICONTROL Match Type]設為[!UICONTROL Negative]。 如果列包含廣告群組名稱，則會為廣告群組排除關鍵字。 如果列不包含廣告群組名稱，則會在整個行銷活動中排除關鍵字。<br><br><b>注意：</b>變更Baidu關鍵字會刪除現有關鍵字，並建立具有新關鍵字識別碼的新關鍵字。 但是，您可以變更相符型別，而不刪除現有關鍵字。 |
| [!UICONTROL Match Type] | 選填/不適用 | 選填/不適用 | 可選：建立<br>必要/可選：編輯或刪除 | 不適用 | 不適用 | 關鍵字的關鍵字比對選項： <i>[!UICONTROL Broad]</i>、<i>[!UICONTROL Exact]</i>、<i>[!UICONTROL Phrase]</i>、<i>[!UICONTROL Negative Broad]</i>或<i>[!UICONTROL Negative Exact]</i>。 在行銷活動層級或廣告群組層級定義負面關鍵字。<br><br>對於新關鍵字，預設值為<i>[!UICONTROL Broad]</i>。 只有在編輯具有多個相符型別的關鍵字時，才需要相符型別或關鍵字ID的值。<br><br><b>注意：</b>您可以變更[!DNL Baidu]關鍵字的相符型別，而不刪除現有的關鍵字。 |
| [!UICONTROL Ad Title] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 廣告的標題。 長度上限為14個雙位元組或28個單位元組字元。<br><br><b>注意：</b>變更廣告復本會刪除現有廣告，並建立具有相同屬性的新廣告。 |
| [!UICONTROL Description Line 1] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 廣告內文的第一行。 最小長度是4個雙位元組或8個單位元組字元，最大長度為20個雙位元組或40個單位元組字元。<br><br><b>注意：</b>變更廣告復本會刪除現有廣告，並建立具有相同屬性的新廣告。 |
| [!UICONTROL Description Line 2] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 廣告本文的第二行。 最小長度是4個雙位元組或8個單位元組字元，最大長度為20個雙位元組或40個單位元組字元。<br><br><b>注意：</b>變更廣告復本會刪除現有廣告，並建立具有相同屬性的新廣告。 |
| [!UICONTROL Display URL] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 廣告中顯示的URL。 長度上限為35個單位元組字元。 |
| [!UICONTROL Base URL] | 不適用 | 不適用 | 可選 | 必填 | 不適用 | 使用者按一下您的廣告時，系統會將使用者帶入的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。關鍵字層級的<br><br>基本/最終URL會覆寫廣告層級及更高層級的URL。 |
| [!UICONTROL Destination URL] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考；未張貼至廣告網路）對於具有目的地URL的帳戶，此值是將廣告連結至廣告商網站上的基礎URL/登陸頁面的URL （有時透過另一個網站來追蹤點選，然後將使用者重新導向到登陸頁面）。 其中包含為「搜尋」、「社交」和「Commerce」行銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，此值會以您帳戶設定和促銷活動設定中的追蹤引數為基礎。 如果您附加廣告網路特定引數，這些引數可能會取代為搜尋、社交和Commerce的同等引數。<br><br>對於具有最終URL的帳戶，此欄會顯示與[!UICONTROL Base URL/Final URL column]相同的值。 |
| [!UICONTROL Custom URL Param] | 不適用 | 不適用 | 可選 | 可選 | 不適用 | 當變數包含在搜尋帳戶或促銷活動設定的追蹤引數中時，用來取代`{custom_code}`動態變數的資料。 若要在追蹤URL中插入自訂值，請使用[!UICONTROL Generate Tracking URLs]選項上傳Bulksheet檔案。 |
| [!UICONTROL Campaign Status] | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有行銷活動）。 新行銷活動的預設值為<i>[!UICONTROL Active]</i>。 若要刪除作用中或暫停的行銷活動，請輸入值&quot;[!UICONTROL Deleted]&quot;。 |
| [!UICONTROL Ad Group Status] | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 不適用 | 廣告群組的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （僅限現有廣告群組）。 新廣告群組的預設值為<i>[!UICONTROL Active]</i>。 若要刪除作用中或暫停的廣告群組，請輸入值&quot;[!UICONTROL Deleted]&quot;。 |
| [!UICONTROL Keyword Status] | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 關鍵字的顯示狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Deleted]</i> （僅限現有關鍵字）、<i>[!UICONTROL Inactive]</i> （無法編輯）、<i>[!UICONTROL Paused]</i> （僅限現有關鍵字）或<i>[!UICONTROL Pending]</i> （無法編輯）。 新關鍵字的預設值為<i>[!UICONTROL Active]</i>。<br><br>若要刪除關鍵字，請輸入值<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Status] | 不適用 | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 廣告的顯示狀態： <i>[!UICONTROL Active]</i> （新廣告的預設）、<i>[!UICONTROL Deleted]</i> （僅限現有廣告）、<i>[!UICONTROL Disapproved]</i> （不可編輯）、<i>[!UICONTROL Inactive]</i> （不可編輯）、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Pending (not editable)]</i>。<br><br>若要刪除廣告，請輸入值<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Location Status] | 不適用 | 不適用 | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 位置目標的狀態： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted] （僅限現有位置）。 新位置的預設值為<i>[!UICONTROL Active]。 若要刪除使用中的位置，請輸入值<i>[!UICONTROL Deleted]。 |
| \[廣告商特定標籤分類\] | 可選 | 可選 | 可選 | 可選 | 不適用 | (以廣告商專屬的標籤分類命名，例如「顏色」（針對稱為「顏色」的標籤分類）與實體相關聯的指定分類值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 最大長度為100個字元，此值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤建立關聯。 <br><br>分類名稱和分類值不區分大小寫。 |
| [!UICONTROL Constraints] | 可選 | 可選 | 可選 | 不適用 | 不適用 | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><br>限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體輸入值。 |
| [!UICONTROL Campaign ID] | 不適用：建立<br>必要/選用：編輯和刪除 | 可選 | 可選 | 可選 | 不適用 | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有當您變更促銷活動名稱時才需要，除非該列包含促銷活動的AMO ID。 |
| [!UICONTROL Ad Group ID] | 不適用 | 不適用：建立<br>必要/選用：編輯和刪除 | 可選 | 可選 | 不適用 | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更廣告群組名稱時才需要，除非該列包含廣告群組的AMO ID。 |
| [!UICONTROL Keyword ID] | 不適用 | 不適用 | 不適用：建立<br>必要/選用：編輯和刪除 | 不適用 | 不適用 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更關鍵字名稱時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) AMO ID。 |
| [!UICONTROL Ad ID] | 不適用 | 不適用 | 不適用 | 不適用：建立<br>必要/選用：編輯和刪除 | 不適用 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更關鍵字名稱時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) AMO ID。 |
| [!UICONTROL AMO ID] | 不適用：建立<br>選用：編輯並刪除 | 不適用：建立<br>選用：編輯並刪除 | 不適用：建立<br>選用：編輯並刪除 | 不適用：建立<br>選用：編輯並刪除 | 不適用：建立<br>選用：編輯並刪除 | （在產生的Bulksheets中）同步實體的[!DNL Adobe]產生的唯一識別碼。 若為回應式搜尋廣告，除非包含[!UICONTROL Ad ID]，否則編輯或刪除廣告需使用AMO ID。 若要編輯具有AMO ID之所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則必須使用AMO ID來編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |
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
