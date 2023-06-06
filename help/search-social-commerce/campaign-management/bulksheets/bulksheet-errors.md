---
title: 大量表單錯誤
description: 請參考每個大量表單錯誤的潛在原因。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 0%

---

# 大量表單錯誤

Search、Social和Commerce會在Bulksheet作業期間產生兩種型別的錯誤檔案：

* **SE錯誤：** 當已張貼檔案但廣告網路不接受所有資料時，出現名為的錯誤檔案 `<uploaded file name>_se_errors.<extension used for the bulksheet>` 「 」已建立。 當接受部分而非所有列時，錯誤檔案會顯示未發佈的列以及每個錯誤的說明，以便您進行更正。 錯誤包含在&quot;[!UICONTROL SE Error Message]「 」欄。

>[!NOTE]
>
>如果您張貼任何 [!DNL Google Ads] 違反廣告網路廣告政策，但可能符合劐免資格的廣告，這些廣告就會自動以劐免請求重新上傳。 如果劐免請求失敗，則有關違規的資訊會包含在錯誤檔案中。

* **EF錯誤：** 當大量工作表作業無法上傳或處理檔案或檔案中的個別列時，會建立名為的錯誤檔案 `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. 如果問題是個別列的問題，則會包含這些列，並附上每個錯誤的說明，以便您進行更正。 錯誤包含在&quot;[!UICONTROL EF Error Message]「 」欄。

## [!UICONTROL SE Error] 訊息

中的錯誤 [!UICONTROL SE Error] 欄直接來自廣告網路。

## [!UICONTROL EF Error] 訊息

下列錯誤可能包含在 [!UICONTROL EF Error] EF錯誤檔案中的欄。

### 下載/建立錯誤

| 類別 | 訊息 | 說明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 作業完全失敗，因為發生未分類或未處理的錯誤。 如果問題仍然存在，請聯絡您的Adobe客戶團隊以調查原因。 |
|  | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 搜尋、Social和Commerce在建立大量表單之前無法與廣告網路同步，因此未建立大量表單。 如果問題仍然存在，請聯絡您的Adobe客戶團隊。 |

### 上傳錯誤

| 類別 | 訊息 | 說明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | 作業完全失敗。 如果問題仍然存在，請聯絡您的Adobe客戶團隊。 |
| 所有實體 | [!UICONTROL Invalid Fields.] \[無效的欄位和錯誤\] | 指定的資料遺失或無效。 |
|  | [!UICONTROL Invalid Reference Given] | 實體在廣告網路上的ID，或上層實體的ID （例如帳戶ID），未對應至「搜尋、社交和商務」中的實體。 當您在大量表單中編輯ID時，可能會發生這種情況。 |
|  | [!UICONTROL <Entity> is deleted or expired] | 實體已過期或已刪除，您無法變更其屬性。 當有人手動編輯狀態時，實體可能會被刪除。 |
|  | [!UICONTROL <Entity> status should be Active or Paused] | （新實體）新實體只能是「作用中」或「已暫停」。 |
|  | [!UICONTROL Duplicate Entries are present] | 同一圖元包含多個列，每個列有不同的屬性。 將變更合併為一列。 |
|  | [!UICONTROL Invalid AMO ID given] | 該列的AMO ID不存在。 如果您在大量表單中編輯ID，就可能發生這種情況。 |
|  | [!UICONTROL Invalid row given] | 列包含的資訊不足，無法判斷實體型別。 編輯該列以包含實體型別的所有必填欄位。 |
| 帳戶 | [!UICONTROL Provide Valid Account Details] | （多個帳戶的批次工作表）帳戶識別碼並未包含在所有列中。 為每一列的下列任一欄組合輸入值：a) &quot;[!UICONTROL AMO ID]「或b) 」[!UICONTROL Account Name]「和」[!UICONTROL Platform].」 |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search、Social和Commerce無權存取廣告網路帳戶，因此您無法建立或編輯行銷活動資料。 請確定搜尋帳戶的認證正確，且帳戶已啟用。 |
| Campaign | [!UICONTROL Invalid Shopping Country specified] | （購物行銷活動） &quot;[!UICONTROL Sales Country]「欄位無效。 檢視有效國家/地區的清單 [的 [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) 和 [的 [!DNL Microsoft® Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| 所有行銷活動元件 | [!UICONTROL Campaign creation failed] | 父級行銷活動未建立，因此未建立此實體。 請確定所有父實體都包含所有必要欄位。 |
| 廣告群組 | [!UICONTROL Campaign Row missing] | 指定的父級行銷活動不存在，因此未建立廣告群組。 在新列中建立上層行銷活動。 |
|  | [!UICONTROL New adgroup has both keywords and placement] | 廣告群組可以包含關鍵字或版位，但不能同時包含兩者。 為關鍵字和版位建立個別的廣告群組。 |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex])未建立廣告群組，因為它未包含至少一個關鍵字。 |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex])未建立廣告群組，因為它不包含至少一個廣告。 |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex])未建立廣告群組，因為它不包含至少一個廣告。 |
| 所有廣告群組元件 | [!UICONTROL Adgroup creation failed] | 父級廣告群組未建立，因此無法建立此實體。 這可能是因為廣告群組欄位中發生錯誤或父級行銷活動失敗。 請確定所有父實體都包含所有必要欄位。 |
|  | [!UICONTROL Adgroup Row Missing] | 指定的父廣告群組不存在，因此無法建立實體。 在新列中建立父級廣告群組。 |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | 「[!UICONTROL Tracking Template]「欄位僅適用於使用最終/進階URL的帳戶。 移除值，直到移轉帳戶使用最終/進階URL為止。 |
| 廣告 | [!UICONTROL Cannot modify attributes other than status code and url for <ad type>] | （文字、展開文字、產品、應用程式安裝和動態搜尋以外的廣告型別）您只能編輯此廣告型別的狀態和URL。 |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | 每個廣告群組最多可包含50個廣告，而此Bulksheet包含超過50個。 減少廣告數量。 |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | 廣告位於已過期或已刪除的父實體中，因此您無法進行編輯。 |
| 關鍵字 | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父級行銷活動或廣告群組已刪除或過期，因此您無法變更實體。 |
| 位置 | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父級行銷活動或廣告群組已刪除或過期，因此您無法變更實體。 |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google廣告)您只能在搜尋網路上的促銷活動或內容網路上的刊登版位競標，但不能對同時以搜尋和內容網路為目標的促銷活動競標。 |
| 購物產品群組 | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | 產品群組的每個層級都必須包含&quot;[!UICONTROL Everything Else]「群組。 您無法手動刪除&quot;[!UICONTROL Everything Else]&quot;群組；當您刪除相同層級的所有其他產品群組時，系統會自動刪除該群組。 |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父級行銷活動或廣告群組已刪除或過期，因此您無法變更實體。 |
| 網站連結 | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] 僅限)訊息不準確；每個行銷活動最多可包含四個（非10個）網站連結，而此Bulksheet包含四個以上。 移除部分網站連結。 |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | 上層行銷活動已到期或遭刪除，因此您無法編輯網站連結。 |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex])無法建立網站連結，因為未建立廣告。 |
| 位置目標 | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | 父級行銷活動或廣告群組已刪除或已過期，因此您無法編輯位置目標。 |
| 排除專案 | [!UICONTROL Other than status is modified] | 您只能編輯排除的狀態(&quot;[!UICONTROL Active]「或」[!UICONTROL Deleted]「)。 |
| Google再行銷清單目標/對象 | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] 僅行銷活動) RLSA目標未對應至現有RLSA （對象）。 更正「」中的值[!UICONTROL Audience]「和」[!UICONTROL RLSA Target]&quot;欄。 |

### 張貼錯誤

下列錯誤只會在EF錯誤檔案中發生。 大多數張貼錯誤來自廣告網路，並包含在SE錯誤檔案中。

| 類別 | 訊息 | 說明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | 作業完全失敗。 如果問題仍然存在，請聯絡您的Adobe客戶團隊。 |
| 所有實體 | [!UICONTROL Entity] 已張貼至廣告網路 | 實體已發佈至廣告網路，但未同時同步至「搜尋、社交和商務」，因此實體資料無法立即用於「搜尋、社交和商務」。 同步程式現在會自動觸發。<br><br>當大量資料同步時，資料可能無法在Search、Social和Commerce中使用數小時以上。 |
|  | [!UICONTROL Skipping <ENTITY> creation since <PARENT ENTITY> creation failed.] | 無法建立父實體，因此未建立此子實體。 |

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](bulksheet-about.md)
>* [下載/建立Bulksheet檔案](bulksheet-download.md)
>* [驗證大量表單檔案中的登入頁面](bulksheet-validate-landing-pages.md)
>* [上傳大量表單檔案或已修正的錯誤檔案](bulksheet-upload.md)
>* [張貼大量工作表或已修正的錯誤檔案](bulksheet-post.md)

