---
title: 重新驗證 [!DNL Google Analytics] 資料來源
description: 瞭解如何重新驗證 [!DNL Google Analytics] 資料來源（如果您變更相關密碼或憑證過期）。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# 重新驗證 [!DNL Google Analytics] 資料來源

*僅限代理公司管理員、代理公司帳戶管理員、Adobe帳戶管理員及管理員*

如果您變更用於資料來源的電子郵件帳戶密碼，或 [!DNL OAuth] 帳戶的憑證會過期，然後會關閉與電子郵件帳戶的所有開啟連線，您必須重新驗證身分才能繼續同步資料。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. 選取您要重新驗證的資料來源旁的核取方塊。

1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

1. 編輯 [資料來源設定](data-source-settings.md)：

   1. 在 [!UICONTROL Connect to Google Analytics] 章節，請執行下列動作。

      1. （如有必要）輸入新的電子郵件地址，以使用此資料來源存取資料。 電子郵件地址必須註冊到 [!DNL Google] 帳戶並擁有的「讀取和分析」許可權 [!DNL Google Analytics] 帳戶。 請參閱 [在中指派使用者許可權的說明 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >若要確保僅特定於 [!DNL Google Analytics] Search、Social和Commerce中有屬性和檢視可用，使用只能存取這些屬性和檢視的電子郵件地址登入。
   1. 選取核取方塊以授權Search、Social和Commerce存取帳戶的量度。

   1. 按一下 **[!UICONTROL Re-Authenticate]**.


1. 按一下 **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定的必要條件 [!DNL Google Analytics] 資料來源](data-source-prerequisites.md)
>* [設定 [!DNL Google Analytics] 以資料來源檢視](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停資料來源的同步處理](data-source-pause.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)

