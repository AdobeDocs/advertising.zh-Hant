---
title: 上傳大量表單或已修正的錯誤檔案
description: 瞭解如何手動上傳大量表單檔案或已修正的登陸頁面驗證錯誤檔案。
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: f68b2eb267391972eed94e4fec3ea386fbf206c6
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# 上傳大量表單或已修正的錯誤檔案

您可以從您的裝置或網路上傳大量表單檔案、修正的登陸頁面驗證錯誤檔案，以及其他修正的錯誤檔案，以用於 [支援的廣告網路](bulksheet-about.md#bulksheet-functionality-by-network). 上傳檔案時，檔案中的任何自訂欄都會被刪除。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Upload Bulksheet]**.

1. 輸入或選取資訊於 [[!UICONTROL Upload Bulksheet] 設定](#bulksheet-upload-settings).

1. 按一下 **[!UICONTROL Apply]**.

當工作開始時，檔案會列在 [!UICONTROL Bulksheets] 檢視。 檔案完成時，會傳送包含檔案連結的電子郵件通知。 根據編譯的資料量，電子郵件通知可能需要幾分鐘或更長時間。 但是，如果檔案產生失敗，則會在 [!UICONTROL Bulksheets] 檢視，並傳送包含錯誤檔案連結的電子郵件通知。

>[!NOTE]
>
>如果您將Bulksheet資料張貼至廣告網路，您可以依照中的檔案進度進行 [!UICONTROL Progress] 中的欄 [!UICONTROL Bulksheets] 檢視。 大量資料需要更長的時間才能發佈。

## 上傳大量工作表和已更正錯誤檔案的設定 {#bulksheet-upload-settings}

| 引數 | 說明 |
|----|----|
| [!UICONTROL File to Upload] | 要上傳的檔案。 輸入完整路徑和檔案名稱，或按一下 <b>[!UICONTROL Browse]</b> 在您的裝置或網路上尋找檔案。<br><br>Bulksheet檔案最大可達2.5 GB （約250萬列），且必須具備下列其中一種副檔名： <i>[!UICONTROL .tsv]</i> （以定位點分隔的值）， <i>[!UICONTROL .txt]</i> （適用於符合Unicode規範的ASCII文字）， <i>[!UICONTROL .csv]</i> （適用於逗號分隔的值），或 <i>[!UICONTROL .zip]</i> （適用於壓縮的ZIP格式，會解壓縮成TSV檔案）。 檔案名稱不能包含下列字元： `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>秘訣：</b> 若資料包含國際字元，請使用TSV或TXT格式的檔案。 |
| [!UICONTROL Single Account] | 檔案是否套用至一個帳戶： <i>[!UICONTROL Yes]</i> （針對一個帳戶）或 <i>[!UICONTROL No]</i>（適用於多個帳戶）。 |
| [!UICONTROL Account (Search Engine)] | （檔案套用至單一帳戶時）要上傳資料的帳戶。 |
| [!UICONTROL Search Engine] | （檔案套用至多個帳戶時）要上傳資料的廣告網路。 |
| [!UICONTROL Scheduling] | 何時或是否將檔案張貼至指定的廣告網路：<ul><li><i>[!UICONTROL Post to ad network now]</i> （預設值）：立即開始發佈資料。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]：</i> 在指定的日期和時間開始張貼資料；預設值為明天02:00 （上午2點）。 若要變更日期，請以DD/MM/YYYY或D/M/YYYY格式輸入日期，或按一下 ![行事曆](/advertising.en/help/search-social-commerce/campaign-management/bulksheets/assets/calendar.png "行事曆") 以開啟行事曆及 [選取日期](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). 若要變更時間，請以HH/MM或H/M格式輸入時間，或從清單中選取時間（以15分鐘為間隔）。</li><li><i>[!UICONTROL Preview only]：</i> 若要上傳檔案至Search， Social， &amp; Commerce而不將資料張貼至廣告網路，您稍後仍可張貼檔案。 當大量表單檔案超過10 MB但小於2 GB時，檔案會採用ZIP格式；您不需要解壓縮檔案以進行發佈。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 是否包含追蹤範本和登入頁面尾碼（適用於適用的廣告網路）在含有追蹤範本的帳戶中，或是包含內嵌追蹤程式碼的目標URL (針對所有關鍵字、廣告、位置、網站連結和 [!DNL Google Ads] 發佈中的產品群組： <i>[!UICONTROL Yes]</i> （預設）或 <i>[!UICONTROL No]</i>. 不管競標單位是否在產品組合中。<br><br>如果您選取 <i>[!UICONTROL Yes]</i>，則系統會根據 [!UICONTROL Tracking Methods] 區段設定或促銷活動設定。 根據預設，如果追蹤URL存在，則不會重新產生，除非需要新專案（例如如果關鍵字元合型別、廣告文字或相關帳戶的追蹤引數已變更）。<br><br>如果您選取 <i>[!UICONTROL No]</i>，您之後仍可手動上傳檔案，以產生追蹤URL。<br><br><b>注意：</b> 如果廣告商使用Adobe Advertising轉換追蹤，且基礎URL已變更，您必須產生新的追蹤URL，除非將帳戶設定為自動產生和上傳追蹤URL。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允許根據發佈的資料對最佳化產品組合中的行銷活動進行預算變更。 依預設，不會選取此選項。 如果您選取此選項，則任何指定的行銷活動預算變更都適用，直到最佳化功能決定應重新分配預算（通常是在下一個競標週期）為止。<br><br><b>注意：</b> 針對非最佳化產品組合中的行銷活動發佈的資料所導致的任何預算變更，會在檔案發佈時發生。 變更會在隔天的行銷活動管理檢視中顯示。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 當最佳化產品組合中包含的行銷活動元件時，此功能會覆寫最佳化策略，並允許根據大量表單中的資料變更競標，直到指定的結束日期為止。 如果您選取此選項，請在「 」中指定1-7天以外的結束日期 **[!UICONTROL Hold bulksheet bids until]** 欄位。 |

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](bulksheet-about.md)
>* [下載/建立Bulksheet檔案](bulksheet-download.md)
>* [張貼大量工作表或已修正的錯誤檔案](bulksheet-post.md)
>* [驗證Bulksheet檔案中的登入頁面](bulksheet-validate-landing-pages.md)
>* [匯出產生或上傳的大量表單檔案](bulksheet-export.md)
