---
title: 重新驗證 [!DNL Google Analytics] 資料來源
description: 瞭解如何在變更相關密碼或憑證過期時，重新驗證 [!DNL Google Analytics] 資料來源。
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# 重新驗證[!DNL Google Analytics]資料來源

*僅限代理管理員、代理帳戶管理員、Adobe帳戶管理員和管理員*

如果您變更用於資料來源的電子郵件帳戶密碼，或帳戶的[!DNL OAuth]憑證過期，則會關閉與電子郵件帳戶的所有開啟連線，您必須重新驗證以繼續同步資料。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**。

1. 選取您要重新驗證的資料來源旁的核取方塊。

1. 在資料表上方的工具列中，按一下![編輯](/help/search-social-commerce/assets/edit.png "編輯")。

1. 編輯[資料來源設定](data-source-settings.md)：

   1. 在[!UICONTROL Connect to Google Analytics]區段中，執行下列動作。

      1. （如有必要）輸入新的電子郵件地址，以使用此資料來源的資料進行存取。 電子郵件地址必須註冊到[!DNL Google]帳戶，並且擁有[!DNL Google Analytics]帳戶的「讀取和分析」許可權。 請參閱 [!DNL Google Analytics][&#128279;](https://support.google.com/analytics/answer/9305587)中指派使用者許可權的指示。

         >[!TIP]
         >
         >為確保搜尋、社交和Commerce中只有特定的[!DNL Google Analytics]屬性和檢視可用，請使用只能存取這些屬性和檢視的電子郵件地址登入。

   1. 選取核取方塊以授權搜尋、社交和Commerce存取帳戶的量度。

   1. 按一下&#x200B;**[!UICONTROL Re-Authenticate]**。

1. 按一下&#x200B;**[!UICONTROL Post]**。

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定a [!DNL Google Analytics] 資料來源的先決條件](data-source-prerequisites.md)
>* [將 [!DNL Google Analytics] 檢視設定為資料來源](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停同步處理資料來源](data-source-pause.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
