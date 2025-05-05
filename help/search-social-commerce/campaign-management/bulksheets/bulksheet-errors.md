---
title: 大量表單錯誤
description: 請參考每個大量表單錯誤的潛在原因。
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# 大量表單錯誤

在大量表單作業期間，搜尋、社交和Commerce會產生兩種型別的錯誤檔案：

* **SE錯誤：**&#x200B;當已張貼檔案但廣告網路不接受所有資料時，會建立名為`<uploaded file name>_se_errors.<extension used for the bulksheet>`的錯誤檔案。 接受部分而非全部列時，錯誤檔案會顯示未發佈的列以及每個錯誤的說明，以便您進行更正。 錯誤包含在&quot;[!UICONTROL SE Error Message]&quot;欄中。

>[!NOTE]
>
>如果您張貼任何[!DNL Google Ads]個違反廣告網路的廣告政策，但可能有資格獲得劐免的廣告，則這些廣告會自動以劐免請求重新張貼。 如果劐免請求失敗，則錯誤檔案中會包含違規的相關資訊。

* **EF錯誤：**&#x200B;當Bulksheet作業無法上傳或處理檔案或檔案中的個別資料列時，會建立名為`<uploaded file name>_ef_errors.<extension used for the bulksheet>`的錯誤檔案。 如果問題與個別列有關，則會包含這些列，
並提供每個錯誤的說明，以便您進行更正。 錯誤包含在&quot;[!UICONTROL EF Error Message]&quot;欄中。

## [!UICONTROL SE Error]則訊息

[!UICONTROL SE Error]欄中的錯誤直接來自廣告網路。

## [!UICONTROL EF Error]則訊息

下列錯誤可能包含在[!UICONTROL EF Errors]檔案的[!UICONTROL EF Error]資料行中。

### 下載/建立錯誤

| 類別 | 訊息 | 說明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 作業完全失敗，因為發生未分類或未處理的錯誤。 如果問題仍然存在，請聯絡您的Adobe客戶團隊以調查原因。 |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 搜尋、社交和Commerce在建立大量表單前無法與廣告網路同步，因此未建立大量表單。 如果問題仍然存在，請聯絡您的Adobe客戶團隊。 |

### 上傳錯誤

| 類別 | 訊息 | 說明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | 作業完全失敗。 如果問題仍然存在，請聯絡您的Adobe客戶團隊。 |
| 所有實體 | [!UICONTROL Invalid Fields.] \[無效的欄位和錯誤\] | 指定的資料遺失或無效。 |
|  | [!UICONTROL Invalid Reference Given] | 該實體在廣告網路上的ID，或上層實體的ID （例如帳戶ID），不會對應至搜尋、社交和Commerce中的實體。 當您在大量表單中編輯ID時，可能會發生這種情況。 |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | 實體已過期或已刪除，您無法變更其屬性。 當有人手動編輯狀態時，實體可能會被刪除。 |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | （新實體）新實體只能是「作用中」或「已暫停」。 |
|  | [!UICONTROL Duplicate Entries are present] | 同一實體包含多個列，每一列都有不同的屬性。 將變更合併為一列。 |
|  | [!UICONTROL Invalid AMO ID given] | 該列的AMO ID不存在。 如果您在大量表單中編輯ID，便可能發生這種情況。 |
|  | [!UICONTROL Invalid row given] | 列包含的資訊不足，無法判斷實體型別。 編輯該列以包含實體型別的所有必填欄位。 |
| 帳戶 | [!UICONTROL Provide Valid Account Details] | （多個帳戶的批次工作表）帳戶識別碼未包含在所有列中。 為每列輸入下列任一資料行組合的值： a) &quot;[!UICONTROL AMO ID]&quot;或b) &quot;[!UICONTROL Account Name]&quot;和&quot;[!UICONTROL Platform]&quot;。 |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | 搜尋、Social和Commerce無法存取廣告網路帳戶，因此您無法建立或編輯行銷活動資料。 請確定搜尋帳戶的認證正確且帳戶已啟用。 |
| Campaign | [!UICONTROL Invalid Shopping Country specified] | （購物行銷活動） &quot;[!UICONTROL Sales Country]&quot;欄位中的值無效。 檢視 [!DNL Google Ads][&#128279;](https://support.google.com/merchants/answer/160637#countrytable)的有效國家[和 [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083)的有效國家/地區清單。 |
| 所有行銷活動元件 | [!UICONTROL Campaign creation failed] | 父級行銷活動未建立，因此未建立此實體。 請確定所有父系實體都包含所有必要欄位。 |
| 廣告群組 | [!UICONTROL Campaign Row missing] | 指定的父級行銷活動不存在，因此未建立廣告群組。 在新列中建立父行銷活動。 |
|  | [!UICONTROL New adgroup has both keywords and placement] | 廣告群組可以包含關鍵字或版位，但不能同時包含兩者。 為關鍵字和版位建立個別的廣告群組。 |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex])未建立廣告群組，因為它未包含至少一個關鍵字。 |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex])未建立廣告群組，因為它未包含至少一個廣告。 |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex])未建立廣告群組，因為它未包含至少一個廣告。 |
| 所有廣告群組元件 | [!UICONTROL Adgroup creation failed] | 未建立父級廣告群組，因此無法建立此實體。 這可能是由於廣告群組欄位中發生錯誤或父級行銷活動失敗所致。 請確定所有父系實體都包含所有必要欄位。 |
|  | [!UICONTROL Adgroup Row Missing] | 指定的父廣告群組不存在，因此無法建立實體。 在新列中建立上層廣告群組。 |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | 「[!UICONTROL Tracking Template]」欄位僅適用於使用最終/進階URL的帳戶。 移除值，直到移轉帳戶使用最終/進階URL為止。 |
| 廣告 | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | （文字、展開文字、產品、應用程式安裝和動態搜尋以外的廣告型別）您只能編輯此廣告型別的狀態和URL。 |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | 每個廣告群組最多可包含50個廣告，而此Bulksheet包含超過50個。 減少廣告數量。 |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | 廣告位於已過期或已刪除的父實體中，因此您無法進行編輯。 |
| 關鍵字 | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父級行銷活動或廣告群組已刪除或過期，因此您無法變更實體。 |
| 位置 | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父級行銷活動或廣告群組已刪除或過期，因此您無法變更實體。 |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google廣告)您只能在搜尋網路上的行銷活動中或僅在內容網路上的刊登版位競標，但不得在目標搜尋和內容網路上的行銷活動中競標。 |
| 購物產品群組 | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | 每個產品群組層級都必須包含&quot;[!UICONTROL Everything Else]&quot;群組。 您無法手動刪除&quot;[!UICONTROL Everything Else]&quot;群組；當您刪除相同層級的所有其他產品群組時，會自動刪除該群組。 |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父級行銷活動或廣告群組已刪除或過期，因此您無法變更實體。 |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | （[!DNL Yandex]僅限）訊息不準確；每個行銷活動最多可包含四個（非10個）網站連結，而此大量表單包含四個以上。 移除部分網站連結。 |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | 上層行銷活動已過期或刪除，因此您無法編輯網站連結。 |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex])無法建立網站連結，因為未建立廣告。 |
| 位置目標 | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | 父級行銷活動或廣告群組已刪除或過期，因此您無法編輯位置目標。 |
| 排除 | [!UICONTROL Other than status is modified] | 您只能編輯排除專案的狀態（&quot;[!UICONTROL Active]&quot;或&quot;[!UICONTROL Deleted]&quot;）。 |
| Google再行銷清單目標/對象 | [!UICONTROL Invalid Audience given] | （僅限[!DNL Google Ads]個行銷活動） RLSA目標未對應至現有的RLSA （對象）。 更正&quot;[!UICONTROL Audience]&quot;及&quot;[!UICONTROL RLSA Target]&quot;欄中的值。 |

### 張貼錯誤

僅在[!UICONTROL EF Errors]個檔案中發生下列錯誤。 大多數張貼錯誤來自廣告網路，並包含在SE錯誤檔案中。

| 類別 | 訊息 | 說明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | 作業完全失敗。 如果問題仍然存在，請聯絡您的Adobe客戶團隊。 |
| 所有實體 | [!UICONTROL Entity]已張貼至廣告網路 | 實體已發佈至廣告網路，但未同時同步至Search、Social和Commerce，因此實體資料無法立即用於Search、Social和Commerce。 同步程式現在會自動觸發。<br><br>當大量資料同步時，搜尋、社交和Commerce中可能會有數小時或更長時間無法使用資料。 |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | 無法建立父實體，因此未建立此子實體。 |

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](bulksheet-about.md)
>* [下載/建立Bulksheet檔案](bulksheet-download.md)
>* [驗證Bulksheet檔案中的登入頁面](bulksheet-validate-landing-pages.md)
>* [上傳大量表單檔案或已修正的錯誤檔案](bulksheet-upload.md)
>* [張貼大量工作表或已修正的錯誤檔案](bulksheet-post.md)
