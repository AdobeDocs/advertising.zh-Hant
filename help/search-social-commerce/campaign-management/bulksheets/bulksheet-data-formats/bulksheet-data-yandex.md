---
title: 必要的大量表單資料 [!DNL Yandex] 帳戶
description: 參考Bulksheets中必要的標題欄位和資料欄位 [!DNL Yandex] 帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1857'
ht-degree: 0%

---

# 附錄 — 必要的大量表單資料 [!DNL Yandex] 帳戶

若要建立和更新 [!DNL Yandex] 大量行銷活動資料，您可以使用特別格式化的搜尋、社交和商務大量表單檔案 [!DNL Yandex] 帳戶。 您可以) [產生現有帳號的大量工作表檔案](../bulksheet-download.md) (b)手動建立（請參閱「 」）[支援的Bulksheet檔案格式](bulksheet-file-formats.md)」以取得受支援檔案格式的一般資訊)。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Start Date,Campaign Budget,Delivery Method,Ad Group Name,Ad Title,Ad Description,Base URL,Destination URL,SiteLink Title,SiteLink Base URL,SiteLink Destination URL,Keyword,Max CPC,Match Type,Search Network Status,Content Network Status,Negative Keywords (Yandex),Param1 (Yandex),Param2 (Yandex),Campaign Status,Ad Group Status,Ad Status,Keyword Status,SiteLink Status,Campaign ID,Ad Group ID, Ad ID,Keyword ID,AMO ID, [Advertiser-specific Label Classification],Constraints,EF Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用的資料欄位

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| 欄位 | Campaign | 廣告群組 | 關鍵字 | 文字廣告 | 網站連結 | 說明 |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Acct Name] | 必要/選用 | 必要/選用 | 必要/選用 | 必要/選用 | 必要/選用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 必填 | 必填 | 識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Campaign Start Date] | 必要：建立<br>可選：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 可以以廣告商時區及以下格式之一為單位對促銷活動發出競標的第一個日期： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新行銷活動的預設值為當天。 |
| [!UICONTROL Campaign Budget] | 必要：建立<br>可選：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的終生支出限制，無論是否包含貨幣符號和標點符號。 |
| [!UICONTROL Delivery Method] | 必要：建立<br>可選：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 每天顯示行銷活動廣告的速度如何：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新行銷活動的預設）：將廣告印象分散在一天當中。</li><li><i>[!UICONTROL Accelerated]：</i> 在達到預算之前，儘可能多地顯示您的廣告。 因此，您的廣告可能不會在當天稍後出現。</li></ul> |
| [!UICONTROL Ad Group Name] | 不適用 | 必填 | 必填 | 必填 | 不適用 | 廣告群組。 |
| [!UICONTROL Ad Title] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 橫幅（廣告）的標題。 長度上限為33個字元，單一字元不能超過23個字元。<br><br><b>注意：</b> 變更廣告復本會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Ad Description] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 橫幅（廣告）的正文。 長度上限為75個字元，一個字最多只能有22個字元。<br><br><b>注意：</b> 變更廣告復本會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Base URL] | 不適用 | 不適用 | 可選 | 必填 | 不適用 | 使用者按一下您的廣告時，會前往登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 包括通訊協定在內，長度上限為1024個字元。<br><br>關鍵字層級的基礎/最終URL會覆寫廣告層級和更高級別的URL。 |
| [!UICONTROL Destination URL] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考；未張貼至廣告網路）對於具有目的地URL的帳戶，此值是將廣告連結至廣告商網站上的基本URL/登陸頁面的URL （有時透過另一個追蹤點按的網站，然後將使用者重新導向至登陸頁面）。 其中包含為Search， Social， &amp; Commerce促銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，此值會以您帳戶設定和促銷活動設定中的追蹤引數為基礎。 如果您已附加廣告網路特定引數，這些引數可能會取代為搜尋、社交和商務的同等引數。 |
| [!UICONTROL SiteLink Title] | 不適用 | 不適用 | 不適用 | 不適用 | 必填 | 網站連結文字。 若為新網站連結，請在網站連結列中包含行銷活動名稱。 對於廣告群組層級或廣告層級的網站連結，請分別加入廣告群組名稱或廣告標題與文字。<br><br><b>注意：</b> 您最多可以有四個網站連結。 |
| [!UICONTROL SiteLink Base URL] | 不適用 | 不適用 | 不適用 | 不適用 | 必填 | 網站連結的基礎URL；它必須是橫幅的基礎URL。 請參閱「[!UICONTROL Base URL].」 |
| [!UICONTROL SiteLink Destination URL] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | 網站連結的目標URL；它必須是橫幅的目標URL。 請參閱「[!UICONTROL Destination URL].」 |
| [!UICONTROL Keyword] | 可選/不適用 | 不適用 | 必填 | 不適用 | 不適用 | 片語（關鍵字字串）。 廣告必須至少有一個片語。 每個關鍵字最多可以有7個單字（停用字除外）。<br><br><b>附註：</b><ul><li>若要在行銷活動層級排除片語，請設定 [!UICONTROL Match Type] 至 [!UICONTROL Negative].</li><li>變更片語會刪除現有的片語並建立新的片語。</li><li>變更 [!DNL Yandex] 關鍵字短語或相符型別會刪除現有的關鍵字短語並建立新的關鍵字短語。</li></ul> |
| [!UICONTROL Max CPC] | 不適用 | 必要：建立<br>可選：編輯或刪除 | 可選 | 不適用 | 不適用 | 最高每次點按成本(CPC)，這是搜尋網路上橫幅（廣告）點按的最高金額，無論是否有貨幣符號和標點符號。 您可以設定廣告群組和關鍵字的值。 新關鍵字的預設值繼承自廣告群組層級。 |
| [!UICONTROL Match Type] | 可選/不適用 | 不適用 | 可選：建立<br>必要/選用：編輯或刪除 | 不適用 | 不適用 | 片語的關鍵字比對選項： <i>[!UICONTROL Content]</i> 或 <i>[!UICONTROL Search]</i>. 使用「」定義負面關鍵字[!UICONTROL Negative Keywords]「 」欄。<br><br><b>注意：</b> 變更 [!DNL Yandex] 關鍵字短語或相符型別會刪除現有的關鍵字短語並建立新的關鍵字短語。 |
| [!UICONTROL Search Network Status] | 可選 | 不適用 | 不適用 | 不適用 | 不適用 | 是否要在搜尋網路上放置廣告： <i>[!UICONTROL Yes]</i> （預設）或 <i>[!UICONTROL No]</i>. |
| 內容網路狀態 | 可選 | 不適用 | 不適用 | 不適用 | 不適用 | 是否要將廣告放置在 [!DNL Yandex] advertising (display)網路： <i>[!UICONTROL Yes]</i> （預設）或 <i>[!UICONTROL No]</i>. |
| [!UICONTROL Negative Keywords (Yandex)] | 不適用 | 不適用 | 可選 | 不適用 | 不適用 | 廣告群組中由所有短語共用的負面關鍵字（短語），前面有減號(例如 `-mykeyword`)。 如果否定關鍵字元合片語中的關鍵字，則否定關鍵字不會套用至片語。 |
| [!UICONTROL Param1 (Yandex)] | 不適用 | 不適用 | 可選 | 不適用 | 不適用 | 的值 `{param1}` 替代變數。 它最多可包含255個位元組。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Param2 (Yandex)] | 不適用 | 不適用 | 可選 | 不適用 | 不適用 | 的值  `{param2}` 替代變數。 它最多可包含255個位元組。 若要刪除現有值，請使用值 `[delete]` （包括括弧）。 |
| [!UICONTROL Campaign Status] | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的顯示狀態： <i>[!UICONTROL active]</i>， <i>[!UICONTROL archived]</i>， <i>[!UICONTROL deleted]</i>， <i>[!UICONTROL disapproved]</i>， <i>[!UICONTROL pending]</i>，或 <i>[!UICONTROL stop]</i> （已暫停）。 新行銷活動的預設為 <i>[!UICONTROL active]</i>.<br><br><b>附註：</b><ul></li>如果行銷活動曾經處於作用中狀態，則無法將其刪除。 請改為封存。</li><li>在某些情況下，行銷活動可能會自動封存或移除。</li><li>您不能手動將狀態設定為 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不會變更這些狀態。</li></ul> |
| [!UICONTROL Ad Group Status] | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 不適用 | 廣告群組的顯示狀態： <i>[!UICONTROL active]</i>， <i>[!UICONTROL archived]</i>， <i>[!UICONTROL deleted]</i>， <i>[!UICONTROL disapproved]</i>， <i>[!UICONTROL pending]</i>，或 <i>[!UICONTROL stop]</i> （已暫停）。 新廣告群組的預設為 <i>[!UICONTROL active]</i>.<br><br><b>附註：</b><ul></li>如果廣告群組曾經處於作用中狀態，則您無法將它刪除。 請改為封存。</li><li>您不能手動將狀態設定為 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不會變更這些狀態。</li></ul> |
| [!UICONTROL Ad Status] | 不適用 | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 橫幅（廣告）的顯示狀態： <i>[!UICONTROL active]</i>， <i>[!UICONTROL archived]</i>， <i>[!UICONTROL deleted]</i>， <i>[!UICONTROL disapproved]</i>， <i>[!UICONTROL pending]</i>，或 <i>[!UICONTROL stop]</i> （已暫停）。 新橫幅的預設值為 <i>[!UICONTROL active]</i>.<br><br><b>注意：您不能手動將狀態設定為 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不會變更這些狀態。 |
| [!UICONTROL Keyword Status] | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 片語（關鍵字）的顯示狀態： <i>[!UICONTROL active]</i>. 新片段的預設值為 <i>[!UICONTROL active]</i>.<br><br><b>注意：您不能手動將狀態設定為 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不會變更這些狀態。 |
| [!UICONTROL SiteLink Status] | 不適用 | 不適用 | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 網站連結的顯示狀態： <i>[*UICONTROL作用中]</i> 或 <i>[*UICONTROL已暫停]</i>. 新網站連結的預設值為 <i>[*UICONTROL作用中]</i>. |
| [!UICONTROL Campaign ID] | 不適用：建立<br>必要/選用：編輯<br>可選：刪除 | 可選 | 可選 | 可選 | 可選 | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更促銷活動名稱時才需要，除非該列包含促銷活動的AMO ID。 |
| [!UICONTROL Ad Group ID] | 不適用 | 不適用：建立<br>必要/選用：編輯<br>可選：刪除 | 可選 | 可選 | 不適用 | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更廣告群組名稱時才需要，除非該列包含廣告群組的AMO ID。 |
| [!UICONTROL Ad ID] | 不適用 | 不適用 | 不適用 | 不適用：建立<br>必要/選用：編輯或刪除 | 不適用 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更關鍵字名稱時才需要，除非該列包含a)足以識別關鍵字的屬性欄或b) AMO ID。 |
| [!UICONTROL Keyword ID] | 不適用 | 不適用 | 不適用：建立<br>必要/選用：編輯<br>必要：刪除 | 不適用 | 不適用 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更關鍵字名稱時才需要，除非該列包含a)足以識別關鍵字的屬性欄或b) AMO ID。 |
| [!UICONTROL AMO ID] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （在產生的大量表單中） An [!DNL Adobe] — 為同步的實體產生的唯一識別碼。 對於回應式搜尋廣告，編輯或刪除廣告時需要AMO ID，除非您包含 [!UICONTROL Ad ID]. 若要使用AMO ID編輯所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則編輯或刪除資料時需使用AMO ID。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |
| \[廣告商特定標籤分類\] | 可選 | 可選 | 可選 | 可選 | 不適用 | （以廣告商特定的標籤分類命名，例如稱為顏色的標籤分類的「顏色」）與實體相關聯的指定分類的值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 長度上限為100個字元，值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤相關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值不區分大小寫。 |
| [!UICONTROL Constraints] | 可選 | 可選 | 可選 | 不適用 | 不適用 | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><br>限制由子實體繼承，因此您不需要輸入子實體的值，除非您想要覆寫繼承的值。 |
| [!UICONTROL EF Error Message] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中，以供參考之用）用來顯示來自搜尋、社交和商務中有關列中資料之錯誤訊息的預留位置；錯誤訊息包含在 [!UICONTROL EF Errors] 檔案。 此值未發佈到廣告網路。 |

<table style="table-layout:auto">

[^1]：Excel在開啟檔案時將大型數字轉換為科學記號(例如2.12E+09 for 2115585666)。 若要檢視標準標籤法中的數字，請選取欄中的任何儲存格，然後按一下公式列內的「 」。

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [可在Bulksheets中執行的作業](bulksheet-operations.md)
>* [支援的Bulksheet檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>* [的點選追蹤格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)

