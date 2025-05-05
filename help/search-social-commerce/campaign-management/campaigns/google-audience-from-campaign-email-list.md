---
title: 從Adobe Campaign電子郵件清單建立 [!DNL Google Ads] 客戶比對對象
description: 瞭解如何從現有的Adobe Campaign電子郵件清單建立 [!DNL Google Ads] 客戶比對對象。
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# 從Adobe Campaign電子郵件清單建立[!DNL Google Ads]個客戶比對對象

*[!DNL Google Ads]個帳戶僅符合客戶相符資格*

您可以在[!DNL Campaign]中設定帳戶連結和工作流程，以從Adobe Campaign內的電子郵件清單建立[!DNL Google Ads]客戶比對對象。

若要這麼做，您需要存取您的[!DNL Campaign]執行個體以及包含所需工作流程的XML檔案，您的Adobe帳戶團隊會提供您這些工作流程。 指示可能會因不同版本的[!DNL Campaign]而有所不同。 如有需要，您的Adobe帳戶團隊可以協助您在[!DNL Campaign]中設定工作流程。

1. 取得Advertising Search、Social和Commerce所提供SFTP帳戶的認證。

1. 在[!DNL Campaign]中，設定將電子郵件清單傳送至Advertising Search、Social和Commerce：

   1. 建立[外部帳戶](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html?lang=zh-Hant)以連結您的搜尋、社交和Commerce提供的SFTP帳戶：

      1. 從左側功能表，前往&#x200B;**\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**。

      1. 按一下![建立帳戶](/help/search-social-commerce/assets/campaign-create-account.png "建立帳戶")。

      1. 輸入帳戶的標籤，並選取&#x200B;**[!UICONTROL SFTP]**&#x200B;作為帳戶型別。

      1. 輸入[!DNL Adobe] SFTP伺服器的URL和連線埠號碼，以及廣告商的資料夾名稱、使用者名稱和密碼。

      1. 按一下&#x200B;**[!UICONTROL Save]**。

   1. 在[!DNL Campaign Client]中，安裝包含傳送電子郵件資料所需的工作流程的資料套件：

      1. 從功能表列移至&#x200B;**[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**。

      1. 選取&#x200B;**[!UICONTROL Install a package from a file]**，然後按一下&#x200B;**[!UICONTROL Next]**。

      1. 在裝置或網路上找到資料封裝檔案(`AMO_Workflow.xml`)，然後按一下&#x200B;**[!UICONTROL Next]**。

      1. 按一下&#x200B;**[!UICONTROL Start]**&#x200B;並等待工作流程安裝。

   1. 編輯已安裝的工作流程，以選擇性編輯資料查詢的篩選器，並識別新對象名稱和外部SFTP帳戶：

      1. 前往「**[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]**」並開啟封裝。

      1. （選用）編輯資料的任何篩選器：

         * 在工作流程中，連按兩下查詢活動（例如ForkTransition 1）。

         * 編輯篩選運算式。

         * 按一下&#x200B;**[!UICONTROL Finish]**。

      1. 為區段命名：

         * 在工作流程中，按兩下活動&#x200B;**[!UICONTROL Data extraction (File)]**。

         * 在&#x200B;**[!UICONTROL Data extraction (File)]**&#x200B;索引標籤的&#x200B;**[!UICONTROL File name]**&#x200B;欄位中，輸入副檔名為&quot;`.added`&quot;的區段名稱（例如PaidSubscribers.added）。

           區段名稱不得已存在。 區段名稱區分大小寫，且必須包含ASCII字元，但不能包含底線(`_`)。

           不過，如果您想要將區段新增至特定[!DNL Google Ad]帳戶，則請在區段名稱后加上底線和[!UICONTROL User SE Account ID] (搜尋、社交和Commerce的ID以取得[!DNL Google Ads]帳戶，而非網路的帳戶ID)：

           `_<User SE Account ID>`

           範例： Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >這是禁止在檔案名稱中使用底線的規則的例外。

           否則，區段會新增至搜尋、社交和Commerce正在為廣告商同步的所有[!DNL Google Ads]帳戶。

         * 保留選取的選項&#x200B;**[!UICONTROL Generate an outbound transition]**。

         * 按一下&#x200B;**[!UICONTROL Ok]**。

      1. 指定要將資料傳送到的外部帳戶：

         * 在工作流程中，按兩下活動&#x200B;**[!UICONTROL File Transfer]**。

         * 在&#x200B;**[!UICONTROL File Transfer]**&#x200B;索引標籤的&#x200B;**[!UICONTROL Remote server]**&#x200B;區段中，選取&#x200B;**[!UICONTROL Use an external account]**&#x200B;的選項。

         * 在&#x200B;**[!UICONTROL External account]**&#x200B;欄位中，選取您在步驟2建立的外部帳戶標籤。

         * 在&#x200B;**[!UICONTROL Server folder]**&#x200B;欄位中，為外部帳戶選取[!UICONTROL Account]欄位的值。

         * （選擇性）在&#x200B;**[!UICONTROL Schedule]**&#x200B;索引標籤上，指定不同的檔案傳輸排程。

           根據預設，工作流程會在00:00 （午夜）執行，以確保處理所有記錄。 若要將延遲降至最低，請將工作流程排程在18:00之前執行。

         * 按一下&#x200B;**[!UICONTROL Ok]**。

搜尋、Social和Commerce每隔30分鐘檢查一次目錄（廣告商時區的NN：30和NN：59），並將找到的任何檔案移至另一個位置，然後於22:00 （下午10），自動從資料建立對象並推送至Google。 搜尋、Social和Commerce會繼續每隔30分鐘檢查電子郵件清單的更新（新增和減少），並在每日22:00相應地更新[!DNL Google Ads]上的對象。

>[!NOTE]
>
>* 如果在處理週期之間上傳檔案的多個版本，則會使用最新的檔案。
>
>* 搜尋、Social和Commerce不會儲存您用來建立或編輯[!DNL Google Ads]對象的電子郵件清單中的任何客戶資料。
>
>* [!DNL Google Ads]可能需要一些時間來處理對象的更新。
>
>* 請參閱[[!DNL Google Ads] 檔案，瞭解客戶比對的運作方式和限制](https://support.google.com/displayvideo/answer/9539301)。

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [建立 [!DNL Google Ads] 來自 [!DNL Adobe] 受眾的客戶比對受眾](google-audience-from-adobe-audience.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)
