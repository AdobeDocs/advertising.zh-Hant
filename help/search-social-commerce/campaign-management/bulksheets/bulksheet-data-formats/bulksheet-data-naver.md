---
title: 必要的大量表單資料 [!DNL Naver] 帳戶
description: 參考Bulksheets中必要的標題欄位和資料欄位 [!DNL Naver] 帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 0%

---

# 附錄 — 必要的大量表單資料 [!DNL Naver] 帳戶

填入您的 [!DNL Naver] Search， Social， &amp; Commerce中的帳戶，方法是在中產生Bulksheet檔案 [!DNL Naver]，然後將其上傳至Search、Social和Commerce。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用的資料欄位

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| 欄位 | Campaign | 廣告群組 | 關鍵字 | 說明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考）廣告平台。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Acct Name] | 必要/選用 | 必要/選用 | 必要/選用 | 可識別廣告網路帳戶的唯一名稱。 除非每一列包含實體的AMO ID，否則為必要。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 識別帳戶促銷活動的唯一名稱。 |
| [!UICONTROL Ad Group Name] | 不適用 | 必填 | 必填 | 識別廣告群組的唯一名稱。 |
| [!UICONTROL Keyword] | 不適用 | 不適用 | 必填 | 關鍵字字串。 |
| [!UICONTROL Base URL] | 不適用 | 不適用 | 可選 | 使用者按一下您的廣告時，會前往登陸頁面URL，包括針對促銷活動或帳戶設定的任何附加引數。<br><br>關鍵字層級的基礎/最終URL會覆寫廣告層級和更高級別的URL。 |
| [!UICONTROL Destination URL] | 不適用 | 不適用 | 不適用 | （包含在產生的Bulksheet中以供參考；未張貼至廣告網路）對於具有目的地URL的帳戶，此值是將廣告連結至廣告商網站上的基本URL/登陸頁面的URL （有時透過另一個追蹤點按的網站，然後將使用者重新導向至登陸頁面）。 其中包含為Search， Social， &amp; Commerce促銷活動或帳戶設定的任何附加引數。 如果您產生追蹤URL，此值會以您帳戶設定和促銷活動設定中的追蹤引數為基礎。 如果您已附加廣告網路特定引數，這些引數可能會取代為搜尋、社交和商務的同等引數。<br><br>對於具有最終URL的帳戶，此欄會顯示與 [!UICONTROL Base URL/Final URL column]. |
| \[廣告商特定標籤分類\] | 可選 | 可選 | 可選 | （以廣告商特定的標籤分類命名，例如稱為顏色的標籤分類的「顏色」）與實體相關聯的指定分類的值。 每個實體的每個分類只能包含一個值（例如促銷活動A的「顏色」標籤分類為「紅色」）。 長度上限為100個字元，值可包含ASCII和非ASCII字元。<br><br>標籤分類及其標籤值會套用至所有子元件；稍後新增的新元件會自動與標籤相關聯。 產品群組的標籤分類會套用至單位（最精細）層級。<br><br>分類名稱和分類值不區分大小寫。 |
| [!UICONTROL Constraints] | 可選 | 可選 | 可選 | 指定給圖元的限制。 每個圖元只能指定一個限制。<br><br>限制由子實體繼承，因此您不需要輸入子實體的值，除非您想要覆寫繼承的值。 |
| [!UICONTROL Campaign Status] | 可選：建立或編輯<br>必要：刪除 | 不適用 | 不適用 | 行銷活動的顯示狀態：*[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有行銷活動）。 新行銷活動的預設為 <i>[!UICONTROL Active]</i>. 若要刪除作用中或已暫停的行銷活動，請輸入值»[!UICONTROL Deleted]「。 |
| [!UICONTROL Ad Group Status] | 不適用 | 可選：建立或編輯<br>必要：刪除 | 不適用 | 廣告群組的顯示狀態： *[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有廣告群組）。 新廣告群組的預設為 <i>[!UICONTROL Active]</i>. 若要刪除作用中或暫停的廣告群組，請輸入值»[!UICONTROL Deleted]「。 |
| [!UICONTROL Keyword Status] | 不適用 | 不適用 | 可選：建立或編輯<br>必要：刪除 | 關鍵字的顯示狀態： *[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （僅限現有關鍵字）。 新關鍵字的預設值為 <i>[!UICONTROL Active]</i>. 若要刪除作用中或暫停的關鍵字，請輸入值&quot;[!UICONTROL Deleted]「。 |
| [!UICONTROL Campaign ID] | 不適用：建立<br>必要/選用：編輯或刪除 | 可選 | 可選 | 可識別現有行銷活動的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更促銷活動名稱時才需要，除非該列包含促銷活動的AMO ID。 |
| [!UICONTROL Ad Group ID] | 不適用 | 不適用：建立<br>必要/選用：編輯或刪除 | 可選 | 可識別現有廣告群組的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更廣告群組名稱時才需要，除非該列包含廣告群組的AMO ID。 |
| [!UICONTROL Keyword ID] | 不適用 | 不適用 | 不適用：建立<br>必要/選用：編輯<br>必要：刪除 | 可識別現有關鍵字的唯一ID。 在CSV和TSV檔案中，它的前面必須是單引號(&#39;)。[^1] 只有在您變更關鍵字名稱時才需要，除非該列包含a)足以識別關鍵字的屬性欄或b) AMO ID。 |
| [!UICONTROL AMO ID] | 不適用：建立<br>可選：編輯或刪除 | 不適用：建立<br>可選：編輯或刪除 | 不適用：建立<br>可選：編輯或刪除 | （在產生的大量表單中） An [!DNL Adobe] — 為同步的實體產生的唯一識別碼。 對於回應式搜尋廣告，編輯或刪除廣告時需要AMO ID，除非您包含 [!UICONTROL Ad ID]. 若要使用AMO ID編輯所有其他實體型別的資料，除非您包含實體ID和父實體ID，否則編輯或刪除資料時需使用AMO ID。<br><br>Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將ID發佈至廣告網路。 |
| [!UICONTROL EF Error Message] | 不適用 | 不適用 | 不適用 | （包含在產生的大量表單中，以供參考之用）用來顯示來自搜尋、社交和商務中有關列中資料之錯誤訊息的預留位置；錯誤訊息包含在 [!UICONTROL EF Errors] 檔案。 此值未發佈到廣告網路。 |
| [!UICONTROL SE Error Message] | 不適用 | 不適用 | 不適用 | （包含在已產生的Bulksheets中以供參考）用來顯示來自廣告網路的錯誤訊息（關於列中的資料）的預留位置；錯誤訊息包含在 [!UICONTROL SE Errors] 檔案。 此值未發佈到廣告網路。 |

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
>* [實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
