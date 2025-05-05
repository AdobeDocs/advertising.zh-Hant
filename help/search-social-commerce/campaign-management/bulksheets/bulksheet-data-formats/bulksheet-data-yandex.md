---
title: ' [!DNL Yandex] 帳戶必要的大量表單資料'
description: 參考 [!DNL Yandex] 帳戶大量表單中必要的標題欄位和資料欄位。
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
source-git-commit: 5c750153ff9e4be2d02f572d96b171d7aa293dd9
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---

# 附錄 — [!DNL Yandex]帳戶需要的大量表單資料

若要大量建立和更新[!DNL Yandex]行銷活動資料，您可以使用特別針對[!DNL Yandex]帳戶格式化的搜尋、社交和Commerce大量表單檔案。 您可以a) [以必要的檔案格式](../bulksheet-download.md)產生現有帳戶的批次工作表檔案，或b)手動建立這些檔案（如需支援之檔案格式的一般資訊，請參閱[支援的批次工作表檔案格式](bulksheet-file-formats.md)）。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Start Date,Campaign Budget,Delivery Method,Ad Group Name,Ad Title,Ad Description,Base URL,Destination URL,SiteLink Title,SiteLink Base URL,SiteLink Destination URL,Keyword,Max CPC,Match Type,Search Network Status,Content Network Status,Negative Keywords (Yandex),Param1 (Yandex),Param2 (Yandex),Campaign Status,Ad Group Status,Ad Status,Keyword Status,SiteLink Status,Campaign ID,Ad Group ID, Ad ID,Keyword ID,AMO ID, [Advertiser-specific Label Classification],Constraints,EF Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用的資料欄位

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>下表為寬表格。 若要擴大檢視區域，您可以按一下左窗格頂端的![隱藏左窗格](/help/dsp/assets/hide-left-pane.png "隱藏左窗格")和右窗格頂端的![隱藏右側窗格](/help/dsp/assets/hide-right-pane.png "隱藏右側窗格")，暫時隱藏目錄和右窗格。 您也可以使用表格底部的卷軸來檢視完整內容。

| 欄位 | Campaign | 廣告群組 | 關鍵字 | 文字廣告 | Sitelink | 說明 |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Acct Name] | 必要/選用 | 必要/選用 | 必要/選用 | 必要/選用 | 必要/選用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 必填 | 必填 | 可識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Campaign Start Date] | 必要： Create<br>選用：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 可能為行銷活動提出競標的第一個日期，在廣告商的時區中且採用以下格式之一： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新行銷活動的預設為當天。 |
| [!UICONTROL Campaign Budget] | 必要： Create<br>選用：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的期限支出限制，無論是否包含貨幣符號和標點符號。 |
| [!UICONTROL Delivery Method] | 必要： Create<br>選用：編輯或刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 每天顯示行銷活動廣告的速度如何：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新行銷活動的預設值）：將您的廣告印象分散在一天當中。</li><li><i>[!UICONTROL Accelerated]：</i>在達到預算之前，儘可能顯示您的廣告。 因此，您的廣告可能不會在當天稍後出現。</li></ul> |
| [!UICONTROL Ad Group Name] | 不適用 | 必填 | 必填 | 必填 | 不適用 | 廣告群組。 |
| [!UICONTROL Ad Title] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 橫幅（廣告）的標題。 長度上限為33個字元，單一字元不能超過23個字元。<br><br><b>注意：</b>變更廣告復本會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Ad Description] | 不適用 | 不適用 | 不適用 | 必填 | 不適用 | 橫幅（廣告）的正文。 長度上限為75個字元，單一字元不得超過22個字元。<br><br><b>注意：</b>變更廣告復本會刪除現有廣告並建立新廣告。 |
| [!UICONTROL Base URL] | 不適用 | 不適用 | 可選 | 必填 | 不適用 | 使用者按一下您的廣告時，系統會將使用者帶入的登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。 最大長度為1024個字元，包括通訊協定。關鍵字層級的<br><br>基本/最終URL會覆寫廣告層級及更高層級的URL。 |
| [!UICONTROL Destination URL] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考；未張貼至廣告網路）對於具有目的地URL的帳戶，此值是將廣告連結至廣告商網站上的基礎URL/登陸頁面的URL （有時透過另一個網站來追蹤點選，然後將使用者重新導向到登陸頁面）。 其中包含為「搜尋」、「社交」和「Commerce」行銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，此值會以您帳戶設定和促銷活動設定中的追蹤引數為基礎。 如果您附加廣告網路特定引數，這些引數可能會取代為搜尋、社交和Commerce的同等引數。 |
| [!UICONTROL SiteLink Title] | 不適用 | 不適用 | 不適用 | 不適用 | 必填 | 網站連結文字。 若為新網站連結，請在網站連結列中包含行銷活動名稱。 對於廣告群組層級或廣告層級網站連結，請分別加入廣告群組名稱或廣告標題與文字。<br><br><b>注意：</b>您最多可以有四個網站連結。 |
| [!UICONTROL SiteLink Base URL] | 不適用 | 不適用 | 不適用 | 不適用 | 必填 | 網站連結的基本URL；它必須是橫幅的基本URL。 請參閱&quot;[!UICONTROL Base URL]&quot;。 |
| [!UICONTROL SiteLink Destination URL] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | 網站連結的目的地URL；它必須是橫幅的目的地URL。 請參閱&quot;[!UICONTROL Destination URL]&quot;。 |
| [!UICONTROL Keyword] | 選填/不適用 | 不適用 | 必填 | 不適用 | 不適用 | 片語（關鍵字字串）。 廣告必須至少包含一個片語。 每個關鍵字最多可以有七個單字，不包括停用詞。<br><br><b>附註：</b><ul><li>若要在行銷活動層級排除片語，請將[!UICONTROL Match Type]設為[!UICONTROL Negative]。</li><li>變更片語會刪除現有的片語並建立新的片語。</li><li>變更[!DNL Yandex]關鍵字短語或相符型別會刪除現有的關鍵字短語並建立新的關鍵字短語。</li></ul> |
| [!UICONTROL Max CPC] | 不適用 | 必要： Create<br>選用：編輯或刪除 | 可選 | 不適用 | 不適用 | 最高每次點按成本(CPC)，這是搜尋網路上橫幅（廣告）點按的最高金額，無論是否有貨幣符號和標點符號。 您可以設定廣告群組和關鍵字的值。 新關鍵字的預設值繼承自廣告群組層級。 |
| [!UICONTROL Match Type] | 選填/不適用 | 不適用 | 可選：建立<br>必要/可選：編輯或刪除 | 不適用 | 不適用 | 字詞的關鍵字比對選項： <i>[!UICONTROL Content]</i>或<i>[!UICONTROL Search]</i>。 使用&quot;[!UICONTROL Negative Keywords]&quot;欄定義負關鍵字。<br><br><b>注意：</b>變更[!DNL Yandex]關鍵字短語或相符型別會刪除現有的關鍵字短語並建立新短語。 |
| [!UICONTROL Search Network Status] | 可選 | 不適用 | 不適用 | 不適用 | 不適用 | 是否要在搜尋網路上刊登廣告： <i>[!UICONTROL Yes]</i> （預設）或<i>[!UICONTROL No]</i>。 |
| 內容網路狀態 | 可選 | 不適用 | 不適用 | 不適用 | 不適用 | 要在[!DNL Yandex]廣告（顯示）網路上刊登廣告： <i>[!UICONTROL Yes]</i> （預設）或<i>[!UICONTROL No]</i>。 |
| [!UICONTROL Negative Keywords (Yandex)] | 不適用 | 不適用 | 可選 | 不適用 | 不適用 | 由廣告群組中的所有短語共用的負面關鍵字（短語），前面有減號（例如`-mykeyword`）。 如果負面關鍵字元合片語中的關鍵字，則負面關鍵字不會套用至片語。 |
| [!UICONTROL Param1 (Yandex)] | 不適用 | 不適用 | 可選 | 不適用 | 不適用 | `{param1}`替代變數的值。 它最多可包含255個位元組。 若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Param2 (Yandex)] | 不適用 | 不適用 | 可選 | 不適用 | 不適用 | `{param2}`替代變數的值。 它最多可包含255個位元組。 若要刪除現有值，請使用值`[delete]` （包括括弧）。 |
| [!UICONTROL Campaign Status] | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 不適用 | 不適用 | 行銷活動的顯示狀態： <i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>或<i>[!UICONTROL stop]</i> （已暫停）。 新行銷活動的預設值為<i>[!UICONTROL active]</i>。<br><br><b>附註：</b><ul></li>如果行銷活動曾經處於作用中狀態，您無法將之刪除。 請改為封存。</li><li>在某些情況下，行銷活動可能會自動封存或移除。</li><li>您不能手動將狀態設定為<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也不能變更這些狀態。</li></ul> |
| [!UICONTROL Ad Group Status] | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 不適用 | 廣告群組的顯示狀態： <i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>或<i>[!UICONTROL stop]</i> （已暫停）。 新廣告群組的預設值為<i>[!UICONTROL active]</i>。<br><br><b>附註：</b><ul></li>如果廣告群組曾經是作用中，您無法將它刪除。 請改為封存。</li><li>您不能手動將狀態設定為<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也不能變更這些狀態。</li></ul> |
| [!UICONTROL Ad Status] | 不適用 | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 橫幅（廣告）的顯示狀態： <i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>或<i>[!UICONTROL stop]</i> （已暫停）。 新橫幅的預設值為<i>[!UICONTROL active]</i>。<br><br><b>注意：您無法手動將狀態設定為<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也無法變更這些狀態。 |
| [!UICONTROL Keyword Status] | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 片語（關鍵字）的顯示狀態： <i>[!UICONTROL active]</i>。 新片段的預設值為<i>[!UICONTROL active]</i>。<br><br><b>注意：您無法手動將狀態設定為<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也無法變更這些狀態。 |
| [!UICONTROL SiteLink Status] | 不適用 | 不適用 | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 網站連結的顯示狀態： <i>[!UICONTROL * Active]</i>或<i>[!UICONTROL *已暫停]</i>。 新網站連結的預設值為<i>[!UICONTROL * Active]</i>。 |
| [!UICONTROL Campaign ID] | 不適用：建立<br>必要/選用：編輯<br>選用：刪除 | 可選 | 可選 | 可選 | 可選 | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有當您變更促銷活動名稱時才需要，除非該列包含促銷活動的AMO ID。 |
| [!UICONTROL Ad Group ID] | 不適用 | 不適用：建立<br>必要/選用：編輯<br>選用：刪除 | 可選 | 可選 | 不適用 | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更廣告群組名稱時才需要，除非該列包含廣告群組的AMO ID。 |
| [!UICONTROL Ad ID] | 不適用 | 不適用 | 不適用 | 不適用：建立<br>必要/選用：編輯或刪除 | 不適用 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更關鍵字名稱時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) AMO ID。 |
| [!UICONTROL Keyword ID] | 不適用 | 不適用 | 不適用：建立<br>必要/選用：編輯<br>必要：刪除 | 不適用 | 不適用 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1]只有在您變更關鍵字名稱時才需要，除非該列包含a)足夠的屬性欄以識別關鍵字或b) AMO ID。 |
| [!UICONTROL AMO ID] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （在產生的Bulksheets中）同步實體的[!DNL Adobe]產生的唯一識別碼。 若為回應式搜尋廣告，除非包含[!UICONTROL Ad ID]，否則編輯或刪除廣告需使用AMO ID。 若要編輯具有AMO ID之所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則必須使用AMO ID來編輯或刪除資料。<br><br>搜尋、社交和Commerce會使用值來決定要編輯的正確身分，但不會將識別碼張貼至廣告網路。 |
| \[廣告商特定標籤分類\] | 可選 | 可選 | 可選 | 可選 | 不適用 | (以廣告商專屬的標籤分類命名，例如「顏色」（針對稱為「顏色」的標籤分類）與實體相關聯的指定分類值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 最大長度為100個字元，此值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤建立關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值不區分大小寫。 |
| [!UICONTROL Constraints] | 可選 | 可選 | 可選 | 不適用 | 不適用 | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><br>限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體輸入值。 |
| [!UICONTROL EF Error Message] | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中以供參考）用來顯示來自搜尋、社交和Commerce的錯誤訊息的預留位置，這些錯誤訊息涉及列中的資料；錯誤訊息包含在[!UICONTROL EF Errors]個檔案中。 此值未發佈到廣告網路。 |

[^1]： Excel在開啟檔案時將大數轉換為科學記號(例如2115585666的2.12E+09)。 若要以標準標籤法檢視數字，請選取欄中的任何儲存格，然後按一下公式列內的「 」。

>[!MORELIKETHIS]
>
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [您可以在大量表單中執行的作業](bulksheet-operations.md)
>* [支援的Bulksheet檔案格式](bulksheet-file-formats.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)的點選追蹤格式
>* [上傳大量表單檔案或已修正的錯誤檔案](../bulksheet-upload.md)
