---
title: 設定摘要資料設定
description: 瞭解如何進行設定，以控制摘要資料的處理方式。
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# 設定摘要資料設定

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

您可以透過摘要設定，設定如何處理摘要資料檔案中的廣告群組、關鍵字和廣告，以及如何專門處理FTP檔案中的資料。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Settings]**。

1. 指定[摘要資料設定](#feed-data-settings)：

   1. 在[!UICONTROL Obsolete Item Auto-Processing]區段中，選取欄位中的資訊。

   1. （廣告商透過FTP或透過直接連結至商戶中心帳戶上傳資料）在[!UICONTROL FTP/GMC Account Auto-Processing]區段中，選取欄位中的資訊。

   1. 在[!UICONTROL Miscellaneous Auto-Processing]區段中，選取欄位中的資訊。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 摘要資料設定 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]：**&#x200B;套用所有[!UICONTROL Obsolete Item Auto-processing]設定至：

* *[!UICONTROL Ad Groups Only]：*&#x200B;僅限過時的廣告群組。

* *[!UICONTROL Keywords Only]：*&#x200B;僅過時關鍵字與產品群組。

* *[!UICONTROL Ad Variations Only]* （預設）：僅過時廣告。

* *[!UICONTROL Keywords and Ad Variations]：*&#x200B;過時關鍵字/產品目標/產品群組和過時廣告。

>[!NOTE]
>
>* 針對[!DNL Google Ads]個購物廣告，只有最低層級的產品群組會受到影響。
>* 對於[!DNL Yandex]帳戶，無論此設定為何，一律會對廣告變化執行過時專案自動處理任務。

**[!UICONTROL When the Scheduled End Date is reached]：** （僅手動張貼資料）結束時間到達後，對已張貼指定結束日期與時間的摘要檔案中的明細專案應如何處理：

* *[!UICONTROL Delete]* （預設值）：當指定的結束時間到達時，刪除所有相關元件。 您無法還原此操作。

* *[!UICONTROL Pause]：*&#x200B;當指定的結束時間到達時，暫停所有相關元件。 如有需要，您可稍後重新啟用元件。

* *[!UICONTROL None]：*&#x200B;不要變更相關元件的狀態。

**[!UICONTROL Missing line items in a manually uploaded feed]：**&#x200B;如果現有專案未包含在手動上傳的新摘要檔案中，或是未依照範本中的「僅對應」設定對應至現有行銷活動或廣告群組，該如何處理現有專案：

* *[!UICONTROL Delete]：*&#x200B;刪除現有元件。

* *[!UICONTROL Pause]：*&#x200B;暫停現有元件。 如果新的摘要檔案包含任何相同的條列專案，則連結會重新啟用，且會保留其歷史記錄和品質分數。 **注意：**&#x200B;如果遺失父產品群組的所有子產品群組，則會刪除父產品群組，因為您無法暫停產品群組。

* *[!UICONTROL None]* （預設）：請勿變更現有元件。

**[!UICONTROL Missing line items in an FTP feed/GMC account]：**&#x200B;如何處理現有專案，如果1)未包含a)已上傳至FTP目錄的新摘要檔案中，或b)下次搜尋、社交和Commerce與其同步時商業中心帳戶中，或2)未根據範本中的[!UICONTROL Map Only]設定對應至現有促銷活動或廣告群組時。

* *[!UICONTROL Delete]：*&#x200B;刪除現有元件。

* *[!UICONTROL Pause]：*&#x200B;暫停現有元件。 如果新資料包含任何相同的條列專案，且保留其歷史記錄和品質分數，則會重新啟用這些量度。 **注意：**&#x200B;如果遺失父產品群組的所有子產品群組，則會刪除父產品群組，因為您無法暫停產品群組。

* *[!UICONTROL None]* （預設）：請勿變更現有元件。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']：**&#x200B;在下列情況下，如何處理包含庫存等級的明細專案：

* （對於在指定欄中具有僅限數值的庫存值的饋送）庫存層次等於或低於指定數量。 預設數量是零(0)。

* （對於在指定資料行中有文字值的摘要） [!UICONTROL Availability]的值為&quot;[!UICONTROL out of stock]&quot;；值不區分大小寫。 **注意：** **在摘要範本中，使用&quot;[!UICONTROL This column has non-numeric values]&quot;的核取方塊表示文字型庫存層級欄。

針對兩種情況選取動作：

* *[!UICONTROL Delete]* （預設）刪除元件。

* *[!UICONTROL Pause]：*&#x200B;暫停元件。 當資料更新時，如果數字型檔存值超過指定的數量，或者[!UICONTROL Availability]為&quot;[!UICONTROL in stock]&quot;或&quot;[!UICONTROL preorder]&quot;，則會重新啟用元件。 元件會保留其歷史記錄和品質分數。

每個條列專案的庫存量來自摘要檔案中的欄，如每個範本的&quot;[!UICONTROL Stock Level]&quot;欄位中所指定。

>[!TIP]
>
>* 對於您預期要重新補充庫存或提高可用性的產品或服務，您應暫停廣告群組、關鍵字和廣告，而不是刪除並重新建立它們。 暫停可讓他們保留其品質分數。
>* 如果您為廣告群組啟用過時的自動處理，而新資料包含廣告群組的庫存層次，則只有在指定的庫存層次在類別層次，而不是品牌/專案層次時，才刪除或暫停廣告群組是有意義的。 例如，如果您有廣告群組「可轉換」，則廣告群組的庫存量應為廣告群組中所代表的所有個別可轉換模型的總計。

**[!UICONTROL Propagate feed data through all applicable templates]：** （廣告商透過FTP或商戶中心帳戶上傳資料檔案）自動透過適用的範本傳播新資料。 依預設，會選取選項。 如果停用選項，您仍可手動傳播任何摘要檔案或帳戶或任何範本的資料。

>[!NOTE]
>
>* 對於FTP檔案，摘要服務每兩小時檢查FTP目錄中的更新（PST時區為偶數小時）。 此選項會處理自上次檢查以來上傳的所有檔案。
>* 對於商家中心帳戶，搜尋、社交和Commerce每天在廣告商時區的約06:00與帳戶同步。 此選項會處理自上次同步後更新的所有資料。
>* 從[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤可以使用已傳播的資料，直到資料張貼到廣告網路或[!UICONTROL Bulksheets]檢視為止。

**[!UICONTROL Post to the SE]：** （廣告商透過FTP或商戶中心帳戶上傳資料檔案）透過適用的範本傳播新資料後，自動以正確格式建立相關廣告網路的Bulksheet檔案。 此選項也會從[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤移除資料，除非任何子元件發生錯誤。

此選項預設為停用。 若要啟用此選項，請選取核取方塊，然後指定是否將大量表單檔案張貼至廣告網路：

* *[!UICONTROL Immediately]* （預設值）：透過範本傳播資料後，將大量工作表檔案張貼到相關的廣告網路。 大量工作表檔案在[!UICONTROL Bulksheets]檢視中保持可用30天。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]：**不會將Bulksheet檔案張貼至相關的廣告網路，但會將其列在[!UICONTROL Bulksheets]檢視中，以便您稍後再張貼。 大量工作表檔案在[!UICONTROL Bulksheets]檢視中保持可用30天。 當大量表單檔案超過10 MB但小於2 GB時，檔案會採用ZIP格式；您不需要解壓縮檔案以進行發佈。 **秘訣：**&#x200B;如果您先前未驗證登入頁面，請使用此選項，這樣就能在將資料張貼至廣告網路之前，從[!UICONTROL Bulksheets]檢視驗證頁面。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]：**&#x200B;排除將超過指定字數的關鍵字短語張貼到廣告網路。 選取此選項時，會傳播超過字數上限的關鍵字片語並列在[!UICONTROL Keywords]索引標籤上，但當您嘗試張貼資料時不會張貼。

此選項預設為停用，因此會張貼所有關鍵字，無論片語包含多少個字詞。 如果您選取此選項，請選取要張貼的最大字數（從3到10）。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [透過範本傳播摘要資料](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [從摘要產生的貼文行銷活動資料到廣告網路](propagated-data-post.md)
