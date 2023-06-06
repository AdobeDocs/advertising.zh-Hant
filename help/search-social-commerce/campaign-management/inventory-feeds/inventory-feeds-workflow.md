---
title: 關於使用庫存摘要自動化廣告管理
description: 瞭解根據產品或服務詳細目錄相關資料自動管理帳戶結構和投放動態廣告的工作流程。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 使用詳細目錄摘要管理行銷活動資料的工作流程

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

最初，請至少測試一個摘要檔案或帳戶，然後您可以完全自動化此程式，或繼續在每個步驟控制此程式：

1. （可選）請聯絡您的Adobe帳戶團隊，以設定用於存放資料檔案的FTP目錄。

   如果您使用FTP目錄，則摘要服務會每兩小時檢查一次新檔案。

   否則，您可以手動上傳中的檔案 [!UICONTROL Advanced (ACM)] 檢視。

1. 設定 [用於處理摘要資料的引數](feed-settings-manage.md#feed-data-settings).

   如果您使用FTP，一開始請勿自動將資料張貼至廣告網路。 驗證第一個檔案的輸出並對結果滿意後，您可以變更設定。

1. 將資料檔案上傳至FTP目錄， [手動上傳資料檔案](feed-files-manage.md) 在 [!UICONTROL Advanced (ACM) view]，或 [啟用Google或Microsoft®商家中心帳戶的存取權](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

若要手動上傳檔案，您可以等到您建立使用該資料檔案的範本時再上傳。

1. （可選）建立群組 [修飾元](modifiers-manage.md) 在摘要資料範本的各種資料欄位中作為變數使用。

1. [建立一或多個範本](ad-templates/ad-template-manage.md) 資料欄來建立特定廣告網路帳戶的行銷活動、廣告群組、關鍵字和/或廣告復本。

1. [透過範本傳播摘要資料](feed-data-propagate.md)，以檔案或帳戶中的資料取代範本中的欄名稱。 根據範本選項，Search、Social和Commerce會使用預設設定為廣告建立新的帳戶結構（促銷活動、廣告群組、關鍵字），或將廣告對應至現有的帳戶結構。

1. （可選） [預覽輸出](propagated-data-view.md) 在 [!UICONTROL Advanced (ACM)] 檢視，並可選擇檢視上資料變更的摘要 [!UICONTROL Propagations] 標籤。

1. [張貼資料](propagated-data-post.md) 至相關的廣告網路帳戶。

1. （如果您使用FTP或商戶中心帳戶來上傳資料；選用）驗證第一個摘要檔案的輸出後， [編輯引數](feed-settings-manage.md#feed-data-settings) 以透過相關範本自動傳播後續資料，並將其張貼至相關廣告網路。

1. （當您有新資料檔案時）視需要上傳新檔案、透過範本傳播資料，然後將資料發佈到相關廣告網路。 您可以選擇在一個步驟中傳播和發佈資料。

>[!MORELIKETHIS]
>
>* [關於使用庫存摘要自動化廣告管理](inventory-feeds-about.md)
>* [清查摘要何時建立或刪除帳戶元件？](when-are-components-created-deleted.md)

