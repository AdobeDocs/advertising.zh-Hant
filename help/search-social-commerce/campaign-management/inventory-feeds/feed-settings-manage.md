---
title: 設定摘要資料設定
description: 瞭解如何進行設定，以控制摘要資料的處理方式。
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# 設定摘要資料設定

*[!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

您可以透過摘要設定，設定如何處理摘要資料檔案中的廣告群組、關鍵字和廣告，以及如何專門處理FTP檔案中的資料。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Settings]**.

1. 指定 [摘要資料設定](#feed-data-settings)：

   1. 在 [!UICONTROL Obsolete Item Auto-Processing] 區段，選取欄位中的資訊。

   1. （廣告商透過FTP或透過直接連結至商戶中心帳戶上傳資料）在 [!UICONTROL FTP/GMC Account Auto-Processing] 區段，選取欄位中的資訊。

   1. 在 [!UICONTROL Miscellaneous Auto-Processing] 區段，選取欄位中的資訊。

1. 按一下 **[!UICONTROL Save]**.

## 摘要資料設定 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]：** 套用所有 [!UICONTROL Obsolete Item Auto-processing] 設定為：

* *[!UICONTROL Ad Groups Only]：* 僅限過時的廣告群組。

* *[!UICONTROL Keywords Only]：* 僅限過時的關鍵字和產品群組。

* *[!UICONTROL Ad Variations Only]* （預設）：僅過時廣告。

* *[!UICONTROL Keywords and Ad Variations]：* 過時關鍵字/產品目標/產品群組和過時廣告。

>[!NOTE]
>
>* 的 [!DNL Google Ads] 則只會影響最低層的產品群組。
>* 的 [!DNL Yandex] 無論此設定為何，一律會對廣告變化執行過時料號自動處理作業。

**[!UICONTROL When the Scheduled End Date is reached]：** （僅限手動張貼的資料）當結束時間到達後，對具有指定結束日期和時間張貼之摘要檔案中的條列專案應如何處理：

* *[!UICONTROL Delete]* （預設）：到達指定的結束時間時，刪除所有相關元件。 您無法還原此操作。

* *[!UICONTROL Pause]：* 到達指定的結束時間時，暫停所有相關元件。 如有需要，您可稍後重新啟用元件。

* *[!UICONTROL None]：* 請勿變更相關元件的狀態。

**[!UICONTROL Missing line items in a manually uploaded feed]：** 如果現有專案未納入手動上傳的新摘要檔案中，或根據範本中的「僅對應」設定，未對應至現有促銷活動或廣告群組，該怎麼辦：

* *[!UICONTROL Delete]：* 刪除現有元件。

* *[!UICONTROL Pause]：* 暫停現有元件。 如果新的摘要檔案包含任何相同的條列專案，則連結會重新啟用，且會保留其歷史記錄和品質分數。 **注意：** 如果遺失父產品群組的所有子產品群組，則會刪除父產品群組，因為您無法暫停產品群組。

* *[!UICONTROL None]* （預設值）：不變更現有元件。

**[!UICONTROL Missing line items in an FTP feed/GMC account]：** 如何處理現有專案，因為1)未包含a)已上傳至FTP目錄的新摘要檔案中，或b)下次搜尋、社交和Commerce會與商家中心帳戶同步，或2)未對應至現有的促銷活動或廣告群組(根據 [!UICONTROL Map Only] 範本中的設定。

* *[!UICONTROL Delete]：* 刪除現有元件。

* *[!UICONTROL Pause]：* 暫停現有元件。 如果新資料包含任何相同的條列專案，且保留其歷史記錄和品質分數，則會重新啟用這些量度。 **注意：** 如果遺失父產品群組的所有子產品群組，則會刪除父產品群組，因為您無法暫停產品群組。

* *[!UICONTROL None]* （預設值）：不變更現有元件。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']：** 當出現下列情況時，如何處理包含庫存層次的行專案：

* （對於在指定欄中具有僅限數值的庫存值的饋送）庫存層次等於或低於指定數量。 預設數量是零(0)。

* （對於在指定欄中有文字值的摘要） [!UICONTROL Availability] 為「[!UICONTROL out of stock]&quot;；值不區分大小寫。 **注意：** **在摘要範本中，使用&quot;[!UICONTROL This column has non-numeric values].」

針對兩種情況選取動作：

* *[!UICONTROL Delete]* （預設）刪除元件。

* *[!UICONTROL Pause]：* 暫停元件。 當更新資料時，如果數值庫存值超過指定數量或 [!UICONTROL Availability] 為「[!UICONTROL in stock]「或」[!UICONTROL preorder]「。 元件會保留其歷史記錄和品質分數。

每個條列專案的庫存量來自摘要檔案中的欄，如&quot;[!UICONTROL Stock Level]每個範本的「 」欄位。

>[!TIP]
>
>* 對於您預期要重新補充庫存或提高可用性的產品或服務，您應暫停廣告群組、關鍵字和廣告，而不是刪除並重新建立它們。 暫停可讓他們保留其品質分數。
>* 如果您為廣告群組啟用過時的自動處理，而新資料包含廣告群組的庫存層次，則只有在指定的庫存層次在類別層次，而不是品牌/專案層次時，才刪除或暫停廣告群組是有意義的。 例如，如果您有廣告群組「可轉換」，則廣告群組的庫存量應為廣告群組中所代表的所有個別可轉換模型的總計。

**[!UICONTROL Propagate feed data through all applicable templates]：** （透過FTP或商戶中心帳戶上傳資料檔案的廣告商）透過適用的範本自動傳播新資料。 依預設，會選取選項。 如果停用選項，您仍可手動傳播任何摘要檔案或帳戶或任何範本的資料。

>[!NOTE]
>
>* 對於FTP檔案，摘要服務每兩小時檢查FTP目錄中的更新（PST時區為偶數小時）。 此選項會處理自上次檢查以來上傳的所有檔案。
>* 對於商家中心帳戶，搜尋、社交和Commerce每天在廣告商時區的約06:00與帳戶同步。 此選項會處理自上次同步後更新的所有資料。
>* 傳播資料可在以下位置使用： [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 標籤，直到資料發佈至廣告網路或 [!UICONTROL Bulksheets] 檢視。

**[!UICONTROL Post to the SE]：** （廣告商透過FTP或商家中心帳戶上傳資料檔案）透過適用的範本傳播新資料後，自動為相關廣告網路以正確格式建立大量表單檔案。 此選項也會將資料從 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 標籤，除非任何子元件發生錯誤。

此選項預設為停用。 若要啟用此選項，請選取核取方塊，然後指定是否將大量表單檔案張貼至廣告網路：

* *[!UICONTROL Immediately]* （預設值）：透過範本傳輸資料後，將大量工作表檔案張貼至相關的廣告網路。 大量工作表檔案仍可在 [!UICONTROL Bulksheets] 檢視30天。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]：**不會將Bulksheet檔案張貼至相關的廣告網路，但會將其列在 [!UICONTROL Bulksheets] 檢視，您稍後可從中張貼內容。 大量工作表檔案仍可在 [!UICONTROL Bulksheets] 檢視30天。 當大量表單檔案超過10 MB但小於2 GB時，檔案會採用ZIP格式；您不需要解壓縮檔案以進行發佈。 **秘訣：** 如果您先前未驗證登入頁面，請使用此選項，以便您可以從以下位置驗證這些頁面： [!UICONTROL Bulksheets] 在您將資料張貼至廣告網路之前檢視。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]：** 排除將超過指定字數的關鍵字短語張貼到廣告網路。 選取此選項時，會傳播字數超過上限的關鍵字詞句，並列在 [!UICONTROL Keywords] 標籤，但當您嘗試張貼資料時，它們不會張貼。

此選項預設為停用，因此會張貼所有關鍵字，無論片語包含多少個字詞。 如果您選取此選項，請選取要張貼的最大字數（從3到10）。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [透過範本傳播摘要資料](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [從摘要產生的行銷活動資料張貼至廣告網路](propagated-data-post.md)
