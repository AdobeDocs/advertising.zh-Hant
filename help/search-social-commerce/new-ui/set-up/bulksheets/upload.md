---
title: （新UI）上傳大量表單或已修正的錯誤檔案
description: 瞭解如何在新的Search、Social和Commerce UI中手動上傳大量表單檔案或已修正登陸頁面驗證錯誤檔案。
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 38fd7ff63b177f13bdfb19b980fb1d1e14edcf56
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# （新UI）上傳大量表單或已修正的錯誤檔案

您可以從您的裝置或網路為[支援的廣告網路](about.md#bulksheet-functionality-by-network)上傳大量表單檔案、修正的登陸頁面驗證錯誤檔案及其他修正的錯誤檔案。 上傳檔案時，檔案中的任何自訂欄都會被刪除。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**。

1. 在工具列中按一下&#x200B;**[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**。

1. 在[[!UICONTROL Upload Bulksheet]設定](#bulksheet-upload-settings)中輸入或選取資訊。

1. 按一下&#x200B;**[!UICONTROL Upload]**。

當工作開始時，檔案會列在[!UICONTROL Bulksheets]檢視中。 在[!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md)中[啟用Bulksheets的電子郵件通知時，當工作完成時，會傳送包含檔案連結的電子郵件通知。 根據編譯的資料量，電子郵件通知可能需要幾分鐘或更長時間。 如果檔案產生失敗，則會在[!UICONTROL Bulksheets]檢視中列出錯誤檔案，並傳送包含錯誤檔案連結的電子郵件通知。

>[!NOTE]
>
>如果您將Bulksheet資料張貼到廣告網路，您可以在[!UICONTROL Bulksheets]檢視中的[!UICONTROL Progress]欄追蹤檔案進度。 大量資料需要更長的時間才能發佈。

## 上傳大量工作表和已更正錯誤檔案的設定 {#bulksheet-upload-settings}

| 引數 | 說明 |
|----|----|
| [!UICONTROL File to Upload] | 要上傳的檔案。 按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;在裝置或網路上尋找檔案，以指定檔案。<br><br>大量工作表檔案最大可達2.5GB （約250萬列），且必須具備下列其中一個副檔名： *[!UICONTROL .tsv]* （適用於定位鍵分隔的值）、*[!UICONTROL .txt]* （適用於符合Unicode的ASCII文字）、*[!UICONTROL .csv]* （適用於逗號分隔的值）或&#x200B;*[!UICONTROL .zip]* （適用於壓縮的ZIP格式，會解壓縮成TSV檔案）。 檔案名稱不能包含下列字元： `# % & * \| \ : " < > . ? /`<br><br>**提示：**&#x200B;對於包含國際字元的資料，請使用TSV或TXT格式的檔案。 |
| [!UICONTROL Single Account] | 檔案套用至一個帳戶： *[!UICONTROL Yes]* （適用於一個帳戶）或&#x200B;*[!UICONTROL No]* （適用於多個帳戶）。 |
| [!UICONTROL Account (Search Engine)] | （檔案套用至單一帳戶時）要上傳資料的帳戶。 |
| [!UICONTROL Search Engine] | （當檔案套用至多個帳戶時）要上傳資料的廣告網路。<br><br>**注意：**&#x200B;多帳戶大量表單不支援最佳化產品組合中關鍵字的競標變更。 |
| [!UICONTROL Scheduling] | 何時或是否將檔案張貼至指定的廣告網路：<ul><li>*[!UICONTROL Post to search engine now]* （預設值）：立即開始張貼資料。</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]：*&#x200B;在指定的日期和時間開始張貼資料；預設值為明天02:00 （上午2點）。 若要變更日期，請以DD/MM/YYYY格式輸入日期，或按一下行事曆圖示開啟行事曆並選取日期。 若要變更時間，請從清單中選取時間（以15分鐘為間隔）。</li><li>*[!UICONTROL Preview only]：*&#x200B;將檔案上傳至Search、Social和Commerce，而不將資料張貼至廣告網路；您稍後仍可張貼檔案。 當大量表單檔案超過10 MB但小於2 GB時，檔案會採用ZIP格式；您不需要解壓縮檔案以進行發佈。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 若要在含有追蹤範本的帳戶中包含追蹤範本和登入頁面尾碼（適用於適用的廣告網路），或是在含有目的地URL的帳戶中包含內嵌追蹤程式碼的目的地URL，則發佈的所有關鍵字、廣告、位置、網站連結和[!DNL Google Ads]產品群組皆須包含： *[!UICONTROL Yes]* （預設）或&#x200B;*[!UICONTROL No]*。 不管競標單位是否在產品組合中。<br><br>如果您選取&#x200B;*[!UICONTROL Yes]*，則會根據相關帳戶設定或行銷活動設定的[!UICONTROL Tracking Methods]區段中的引數產生URL。 根據預設，如果追蹤URL存在，則除非需要新專案（例如關鍵字元合型別、廣告文字或相關帳戶的追蹤引數已變更），否則不會重新產生追蹤URL。<br><br>如果您選取&#x200B;*[!UICONTROL No]*，稍後仍可手動張貼上傳的檔案來產生追蹤URL。<br><br>**注意：**&#x200B;如果廣告商使用Adobe Advertising轉換追蹤，且基本URL已變更，您必須產生新的追蹤URL，除非將帳戶設定為自動產生及上傳追蹤URL。 |
| [!UICONTROL Replace Media Optimizer Tracking] | （當[!UICONTROL Generate Tracking URLs]為&#x200B;*[!UICONTROL Yes]*&#x200B;時可用）以新產生的追蹤取代上傳檔案URL中的任何現有Adobe Advertising追蹤。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允許根據發佈的資料對最佳化產品組合中的行銷活動進行預算變更。 依預設，不會選取此選項。 如果您選取此選項，則在最佳化功能決定應該重新分配預算之前（通常是在下一個競標週期），任何指定的行銷活動預算變更都適用。<br><br>**注意：**&#x200B;當檔案過帳時，非最佳化產品組合中行銷活動的已過帳資料所產生的任何預算變更都會發生。 變更會在隔天的行銷活動管理檢視中顯示。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 當最佳化產品組合中包含的行銷活動元件時，此功能會覆寫最佳化策略，並允許根據大量表單中的資料變更競標，直到指定的結束日期為止。 如果您選取此選項，請在&#x200B;**[!UICONTROL Hold bulksheet bids until]**&#x200B;欄位中指定介於1-7天之間的結束日期。 |

>[!MORELIKETHIS]
>
>* [（新UI）關於使用大量表單管理行銷活動資料](about.md)
>* [ （新UI）下載/建立Bulksheet檔案](download.md)
>* [ （新UI）張貼大量表單或已修正的錯誤檔案](post.md)
>* [（新UI）驗證Bulksheet檔案中的登入頁面](validate-landing-pages.md)
