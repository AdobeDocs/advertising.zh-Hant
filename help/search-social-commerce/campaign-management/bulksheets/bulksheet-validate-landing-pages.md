---
title: 驗證Bulksheet檔案中的登入頁面
description: 瞭解如何驗證單一帳戶大量表單檔案中的目的地URL。
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# 驗證Bulksheet檔案中的登入頁面

*只包含目的地URL的帳戶*

您可以在單一帳戶大量表單檔案中，驗證所有目的地URL的登入頁面。 您可以指定指出無效頁面的任何短語和URL，並可選擇將登入頁面重新導向回報為錯誤。 搜尋、社交和Commerce會檢查您指定的條件和遺失的登陸頁面（這會導致HTTP 404或「找不到」錯誤）。

當發現錯誤時，搜尋、Social和Commerce會建立大量表單錯誤檔案，其中包含原始大量表單中的所有列，以及登陸頁面無效的所有列的錯誤訊息。 已在[!UICONTROL EF Errors]欄中記錄錯誤。 檔案名稱慣例是`<bulksheet name>__lpv_errors.<extension used for the bulksheet>`。

您稍後可以下載檔案、更正錯誤並上傳已更正的檔案，然後將已更正的檔案張貼至廣告網路帳戶。

>[!NOTE]
>
>* 此功能不會驗證基礎URL/最終URL欄中的值。
>* 您可以在驗證Bulksheet檔案時張貼這些檔案，即使發現錯誤也是如此。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**。

1. 選取每個要驗證的檔案旁的核取方塊。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Validate URLs]**。

1. 在對話方塊的欄位中輸入資訊，然後按一下&#x200B;**[!UICONTROL Apply]**：

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]：**&#x200B;登入頁面內文中的文字，指出頁面無效。 若要指定多個值，請在個別行上輸入。

   **[!UICONTROL Enter invalid landing pages(one per line):]**&#x200B;無效作為登入頁面的頁面URL。 若要指定多個值，請在個別行上輸入。

   **[!UICONTROL User Agent:]**&#x200B;如何識別登入頁面驗證代理程式給登入頁面所在的網頁伺服器。 預設為預設值，它會將代理程式的檢視歸因於匿名[!DNL Mozilla Firefox]使用者。 如果網頁伺服器封鎖匿名[!DNL Mozilla Firefox]使用者的要求，請輸入其他代理程式的名稱。 例如，對於[!DNL Googlebot]，輸入`Googlebot/2.1;+http://www.google.com/bot.html`。

   **[!UICONTROL Report redirects as errors]：**&#x200B;當登入頁面重新導向至其他頁面時（例如，如果登入頁面遺失且網站顯示替代頁面），登入頁面錯誤檔案中的[!UICONTROL ER Errors]欄會指出登入頁面重新導向的URL。

當工作開始時，會在[!UICONTROL Bulksheets view]中新增一列。 建立檔案時，會傳送包含檔案連結的電子郵件通知。 根據編譯的資料量，電子郵件通知可能需要幾分鐘或更長時間。 您可以下載檔案進行編輯，然後重新上傳以進行張貼，或者您可以依原樣張貼檔案。 但是，如果檔案產生失敗，則會在[!UICONTROL Bulksheet Management]頁面上列出錯誤檔案，並傳送包含錯誤檔案連結的電子郵件通知。

>[!NOTE]
>
>* 大型檔案需要更長的時間來驗證。
>* 多個行銷活動的Bulksheet檔案最多可包含500,000個資料列。 如果您產生多個行銷活動的資料，且合併的資料包含超過500,000列，則行銷活動會將資料分割成兩個或多個名為`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv`等檔案。

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](bulksheet-about.md)
>* [刪除已上傳的大量工作表和錯誤檔案](bulksheet-delete.md)
>* [張貼大量工作表或已修正的錯誤檔案](bulksheet-post.md)
>* [停止進行中的大量表單工作](bulksheet-stop-job.md)
>* [上傳大量表單或已修正的錯誤檔案](bulksheet-upload.md)
>* [匯出已產生或已上傳的大量工作表檔案](bulksheet-export.md)
