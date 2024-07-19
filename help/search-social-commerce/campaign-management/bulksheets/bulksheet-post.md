---
title: 張貼大量工作表或已修正的錯誤檔案
description: 瞭解如何將大量表單檔案張貼至您的廣告網路。
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# 張貼大量工作表或已修正的錯誤檔案

您可以將現有的Bulksheet檔案或已修正的錯誤檔案張貼到[支援的廣告網路](bulksheet-about.md#bulksheet-functionality-by-network)的相關帳戶。 如果檔案為ZIP格式，您不需要先解壓縮。

Bulksheet檔案和錯誤檔案會在上傳或產生30天後自動刪除。

>[!NOTE]
>上傳檔案時，您也可以張貼大量表單檔案或錯誤檔案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**。

1. 選取每個要張貼的檔案旁的核取方塊。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Post]**。

1. 在對話方塊中，在[[!UICONTROL Post Bulksheet]設定](#bulksheet-post-settings)中輸入或選取資訊，然後按一下&#x200B;**[!UICONTROL Post]**。

   相同的設定會套用至您張貼的所有檔案。

當工作開始時，[!UICONTROL Bulksheets]檢視中資料列的狀態和排程的張貼日期會變更。 發佈檔案時，會傳送包含檔案連結的電子郵件通知。 根據編譯的資料量，電子郵件通知可能需要幾分鐘或更長時間。 但是，如果無法張貼任何資料，則會在[!UICONTROL Bulksheets]檢視上列出錯誤檔案，並傳送電子郵件通知，其中包含錯誤檔案的連結。

>[!NOTE]
>
>* 大量資料需要更長的時間才能發佈。 您可以在[!UICONTROL Bulksheets]檢視的[!UICONTROL Progress]資料行中追蹤檔案進度。
>* 所有張貼的資料都受限於網路的編輯程式。
* 在張貼Bulksheet檔案之前，您可以取消張貼。

## 張貼大量工作表和已更正錯誤檔案的設定 {#bulksheet-post-settings}

| 引數 | 說明 |
|----|----|
| [!UICONTROL Account (Search Engine)] | 張貼資料的廣告網路帳戶。 如果您同時張貼多個檔案，或一個檔案套用至多個帳戶，則值為<i>已選取多個帳戶</i>。<br><br>廣告網路名稱的第一個字母位於帳戶名稱后的括弧中(例如[!DNL Google Ads]帳戶的「Acme Realty (G)」)。 |
| [!UICONTROL Scheduling] | 何時將檔案張貼至指定的廣告網路：<ul><li><i>[!UICONTROL Post to ad network now]</i> （預設值）：立即開始張貼資料。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]：</i>在指定的日期和時間開始張貼資料；預設為明天02:00 （凌晨2點）。 若要變更日期，請以DD/MM/YYYY或D/M/YYYY格式輸入日期，或按一下![行事曆](/help/search-social-commerce/assets/calendar.png "行事曆")開啟行事曆，然後[選取日期](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md)。 若要變更時間，請以HH/MM或H/M格式輸入時間，或從清單中選取時間（以15分鐘為間隔）。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 若要在含有追蹤範本的帳戶中包含追蹤範本和登入頁面尾碼（適用於適用的廣告網路），或是在含有目的地URL的帳戶中包含內嵌追蹤程式碼的目的地URL，則發佈的所有關鍵字、廣告、位置、網站連結和[!DNL Google Ads]產品群組皆須包含： <i>[!UICONTROL Yes]</i> （預設）或<i>[!UICONTROL No]</i>。 不管競標單位是否在產品組合中。<br><br>如果您選取<i>[!UICONTROL Yes]</i>，則會根據相關帳戶設定或行銷活動設定的[!UICONTROL Tracking Methods]區段中的引數產生URL。 根據預設，如果追蹤URL存在，則不會重新產生，除非需要新專案（例如如果關鍵字元合型別、廣告文字或相關帳戶的追蹤引數已變更）。<br><br>若您選取<i>[!UICONTROL No]</i>，稍後仍可手動張貼上傳的檔案來產生追蹤URL。<br><br><b>注意：</b>如果廣告商使用Adobe Advertising轉換追蹤，且基礎URL已變更，您必須產生新的追蹤URL，除非將帳戶設定為自動產生及上傳追蹤URL。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允許根據發佈的資料對最佳化產品組合中的行銷活動進行預算變更。 依預設，不會選取此選項。 如果您選取此選項，則任何指定的行銷活動預算變更都適用，直到最佳化功能決定應重新分配預算（通常是在下一個競標週期）為止。<br><br><b>注意：</b>針對非最佳化產品組合中的行銷活動發佈的資料所造成的任何預算變更，會在檔案發佈時發生。 變更會在隔天的行銷活動管理檢視中顯示。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 當最佳化產品組合中包含的行銷活動元件時，此功能會覆寫最佳化策略，並允許根據大量表單中的資料變更競標，直到指定的結束日期為止。 如果您選取此選項，請在&#x200B;**[!UICONTROL Hold bulksheet bids until]**&#x200B;欄位中指定介於1-7天之間的結束日期。 |

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](bulksheet-about.md)
>* [下載/建立Bulksheet檔案](bulksheet-download.md)
>* [上傳大量工作表或已修正的錯誤檔案](bulksheet-upload.md)
>* [驗證Bulksheet檔案中的登入頁面](bulksheet-validate-landing-pages.md)
>* [匯出已產生或已上傳的大量工作表檔案](bulksheet-export.md)
