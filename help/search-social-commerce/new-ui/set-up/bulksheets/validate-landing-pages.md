---
title: （新UI）驗證Bulksheet檔案中的登入頁面
description: 瞭解如何在新的Search、Social和Commerce UI中，驗證單一帳戶大量表單檔案中的目的地URL。
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
source-git-commit: f22a0f3f1884066faca71c6e8bb760253366b30e
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# （新UI）驗證Bulksheet檔案中的登入頁面

*只包含目的地URL的帳戶*

您可以在單一帳戶大量表單檔案中，驗證所有目的地URL的登入頁面。 您可以指定指出無效頁面的任何短語和URL，並可選擇將登入頁面重新導向回報為錯誤。 搜尋、社交和Commerce會檢查您指定的條件和遺失的登陸頁面（這會導致HTTP 404或「找不到」錯誤）。

當發現錯誤時，搜尋、Social和Commerce會建立大量表單錯誤檔案，其中包含原始大量表單中的所有列，以及具有無效登陸頁面之所有列的錯誤訊息。 已在[!UICONTROL EF Errors]欄中記錄錯誤。 檔案名稱慣例是`<bulksheet name>__lpv_errors.<extension used for the bulksheet>`。

您稍後可以下載檔案、更正錯誤並上傳已更正的檔案，然後將已更正的檔案張貼至廣告網路帳戶。

>[!NOTE]
>
>* 此功能不會驗證基礎URL/最終URL欄中的值。
>* 您可以在驗證Bulksheet檔案時張貼這些檔案，即使發現錯誤也是如此。

>[!IMPORTANT]
>
>已暫時停止支援登陸頁面驗證中的非ASCII字元。 如果您的登陸頁面URL包含非ASCII字元，請聯絡技術支援以尋求協助。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**。

1. 選取每個要驗證的檔案旁的核取方塊。

   >[!NOTE]
   >
   >您只能驗證目前未處理的單一帳戶EF大量表單。 如果您選取多帳戶大量表單或目前正在處理的大量表單，則會排除這些檔案。

1. 在動作列中按一下&#x200B;**[!UICONTROL Validate URLs]**。

1. 在對話方塊的欄位中輸入資訊，然後按一下&#x200B;**[!UICONTROL Apply]**：

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]**&#x200B;登入頁面內文中的文字，指出頁面無效。 若要指定多個值，請在個別行上輸入。

   **[!UICONTROL Enter invalid landing pages (one per line):]**&#x200B;無效作為登入頁面的頁面URL。 若要指定多個值，請在個別行上輸入。

   **[!UICONTROL User Agent:]**&#x200B;如何識別登入頁面驗證代理程式給登入頁面所在的網頁伺服器。 預設值為`default`，它會將代理程式的檢視歸因於匿名[!DNL Mozilla Firefox]使用者。 如果網頁伺服器封鎖匿名[!DNL Mozilla Firefox]使用者的要求，請輸入其他代理程式的名稱。 例如，對於[!DNL Googlebot]，輸入`Googlebot/2.1;+http://www.google.com/bot.html`。

   **[!UICONTROL Report redirects as errors]：**&#x200B;當登入頁面重新導向至其他頁面時（例如，如果登入頁面遺失且網站顯示替代頁面），登入頁面錯誤檔案中的[!UICONTROL EF Errors]欄會指出登入頁面重新導向的URL。

工作開始時，新資料列會新增至[!UICONTROL Bulksheets]檢視。 在[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/new-ui/notifications-manage.md)中啟用Bulksheets的電子郵件通知時，會在建立檔案時傳送內含檔案連結的電子郵件通知。 根據編譯的資料量，電子郵件通知可能需要幾分鐘或更長時間。 您可以下載檔案進行編輯，然後重新上傳以進行張貼，或者您可以依原樣張貼檔案。

>[!NOTE]
>
>* 大型檔案需要更長的時間來驗證。
>* 多個行銷活動的Bulksheet檔案最多可包含500,000個資料列。 如果您產生多個行銷活動的資料，且合併的資料包含超過500,000列，則行銷活動會將資料分割成兩個或多個名為`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv`等檔案。

>[!MORELIKETHIS]
>
>* [（新UI）關於使用大量表單管理行銷活動資料](about.md)
>* [（新使用者介面）上傳大量表單或已修正的錯誤檔案](upload.md)
>* [&#x200B; （新UI）張貼大量表單或已修正的錯誤檔案](post.md)
>* [（新UI）刪除已上傳的大量工作表和錯誤檔案](delete.md)
>* [（新UI）停止進行中的大量表單工作](stop-job.md)
