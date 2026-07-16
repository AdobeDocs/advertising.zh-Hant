---
title: （新UI）張貼大量表單或已修正的錯誤檔案
description: 瞭解如何在新的搜尋、社交和Commerce UI中將Bulksheet檔案發佈至您的廣告網路。
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# （新UI）張貼大量表單或已修正的錯誤檔案

您可以將現有的Bulksheet檔案或已修正的錯誤檔案張貼到[支援的廣告網路](about.md#bulksheet-functionality-by-network)的相關帳戶。 如果檔案為ZIP格式，您不需要先解壓縮。

Bulksheet檔案和錯誤檔案會在上傳或產生30天後自動刪除。

>[!NOTE]
>
>上傳檔案時，您也可以張貼大量表單檔案或錯誤檔案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**。

1. 選取每個要張貼的檔案旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Post]**。

1. 在[[!UICONTROL Post Bulksheet]設定](#bulksheet-post-settings)中輸入或選取資訊，然後按一下&#x200B;**[!UICONTROL Post]**。

   相同的設定會套用至您張貼的所有檔案。

工作開始時，[!UICONTROL Bulksheets]檢視中會更新資料列的狀態和排程的張貼日期。 在[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/new-ui/notifications-manage.md)中啟用Bulksheets的電子郵件通知時，便會在張貼檔案時傳送內含檔案連結的電子郵件通知。 根據編譯的資料量，電子郵件通知可能需要幾分鐘或更長時間。 如果無法張貼任何資料，則會在[!UICONTROL Bulksheets]檢視中列出錯誤檔案，並傳送包含錯誤檔案連結的電子郵件通知。

>[!NOTE]
>
>* 大量資料需要更長的時間才能發佈。 您可以在[!UICONTROL Bulksheets]檢視的[!UICONTROL Progress]資料行中追蹤檔案進度。
>* 所有張貼的資料都受限於網路的編輯程式。
>* 在張貼Bulksheet檔案之前，您可以取消張貼。

## 張貼大量工作表和已更正錯誤檔案的設定 {#bulksheet-post-settings}

| 引數 | 說明 |
|----|----|
| [!UICONTROL Account (Search Engine)] | 張貼資料的廣告網路帳戶。 如果您同時張貼多個檔案，或一個檔案套用至多個帳戶，則值為&#x200B;*已選取多個帳戶*。<br><br>廣告網路名稱的第一個字母在帳戶名稱后方的括弧中(例如[!DNL Google Ads]帳戶的「Acme Realty (G)」)。 |
| [!UICONTROL Scheduling] | 何時將檔案張貼至指定的廣告網路：<ul><li>*[!UICONTROL Post to ad network now]* （預設值）：立即開始張貼資料。</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]：*&#x200B;在指定的日期和時間開始張貼資料；預設值為明天02:00 （上午2點）。 若要變更日期，請以DD/MM/YYYY格式輸入日期，或按一下行事曆圖示開啟行事曆並選取日期。 若要變更時間，請從清單中選取時間（以15分鐘為間隔）。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 若要在含有追蹤範本的帳戶中包含追蹤範本和登入頁面尾碼（適用於適用的廣告網路），或是在含有目的地URL的帳戶中包含內嵌追蹤程式碼的目的地URL，則發佈的所有關鍵字、廣告、位置、網站連結和[!DNL Google Ads]產品群組皆須包含： *[!UICONTROL Yes]* （預設）或&#x200B;*[!UICONTROL No]*。 不管競標單位是否在產品組合中。<br><br>如果您選取&#x200B;*[!UICONTROL Yes]*，則會根據相關帳戶設定或行銷活動設定的[!UICONTROL Tracking Methods]區段中的引數產生URL。 根據預設，如果追蹤URL存在，則除非需要新專案（例如關鍵字元合型別、廣告文字或相關帳戶的追蹤引數已變更），否則不會重新產生追蹤URL。<br><br>如果您選取&#x200B;*[!UICONTROL No]*，稍後仍可手動張貼上傳的檔案來產生追蹤URL。<br><br>**注意：**&#x200B;如果廣告商使用Adobe Advertising轉換追蹤，且基本URL已變更，您必須產生新的追蹤URL，除非將帳戶設定為自動產生及上傳追蹤URL。 |
| [!UICONTROL Replace Media Optimizer Tracking] | （當[!UICONTROL Generate Tracking URLs]為&#x200B;*[!UICONTROL Yes]*&#x200B;時可用）以新產生的追蹤取代上傳檔案URL中的任何現有Adobe Advertising追蹤。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允許根據發佈的資料對最佳化產品組合中的行銷活動進行預算變更。 依預設，不會選取此選項。 如果您選取此選項，則在最佳化功能決定應該重新分配預算之前（通常是在下一個競標週期），任何指定的行銷活動預算變更都適用。<br><br>**注意：**&#x200B;當檔案過帳時，非最佳化產品組合中行銷活動的已過帳資料所產生的任何預算變更都會發生。 變更會在隔天的行銷活動管理檢視中顯示。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 當最佳化產品組合中包含的行銷活動元件時，此功能會覆寫最佳化策略，並允許根據大量表單中的資料變更競標，直到指定的結束日期為止。 如果您選取此選項，請在&#x200B;**[!UICONTROL Hold bulksheet bids until]**&#x200B;欄位中指定介於1-7天之間的結束日期。 |

>[!MORELIKETHIS]
>
>* [（新UI）關於使用大量表單管理行銷活動資料](about.md)
>* [&#x200B; （新UI）下載/建立Bulksheet檔案](download.md)
>* [（新使用者介面）上傳大量表單或已修正的錯誤檔案](upload.md)
>* [（新UI）驗證Bulksheet檔案中的登入頁面](validate-landing-pages.md)
>* [（新UI）刪除已上傳的大量工作表和錯誤檔案](delete.md)
