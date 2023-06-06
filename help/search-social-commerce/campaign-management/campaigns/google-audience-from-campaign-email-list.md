---
title: 建立 [!DNL Google Ads] 來自Adobe Campaign電子郵件清單的客戶比對對象
description: 瞭解如何建立 [!DNL Google Ads] 客戶比對現有Adobe Campaign電子郵件清單中的對象。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# 建立 [!DNL Google Ads] 來自Adobe Campaign電子郵件清單的客戶比對對象

*[!DNL Google Ads]僅符合客戶比對資格的帳戶*

您可以建立 [!DNL Google Ads] 透過在Adobe Campaign中設定帳戶連結和工作流程，客戶可比對電子郵件清單中的對象 [!DNL Campaign].

若要這麼做，您需要存取您的 [!DNL Campaign] 例項和包含必要工作流程的XML檔案，您的Adobe帳戶團隊會提供該工作流程。 指示可能會因不同版本而異 [!DNL Campaign]. 如有需要，您的Adobe帳戶團隊可協助您在中設定工作流程 [!DNL Campaign].

1. 取得Advertising Search、Social和Commerce所提供SFTP帳戶的認證。

1. 在 [!DNL Campaign]，設定將電子郵件清單傳送至Advertising Search、Social和Commerce：

   1. 建立 [外部帳戶](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) 若要連結您的搜尋、Social和商務提供的SFTP帳戶：

      1. 從左側選單前往 **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. 按一下 ![建立帳戶](/help/search-social-commerce/assets/campaign-create-account.png "建立帳戶").

      1. 輸入帳戶的標籤，然後選取 **[!UICONTROL SFTP]** 作為帳戶型別。

      1. 輸入URL和連線埠號碼 [!DNL Adobe] SFTP伺服器和廣告商的資料夾名稱、使用者名稱和密碼。

      1. 按一下 **[!UICONTROL Save]**.
   1. 在 [!DNL Campaign Client]，安裝包含傳送電子郵件資料所需工作流程的資料套件：

      1. 從功能表列，前往 **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. 選取 **[!UICONTROL Install a package from a file]**，然後按一下 **[!UICONTROL Next]**.

      1. 找到資料封裝檔案(`AMO_Workflow.xml`)，然後按一下 **[!UICONTROL Next]**.

      1. 按一下 **[!UICONTROL Start]** 並等待安裝工作流程。
   1. 編輯已安裝的工作流程，以選擇性編輯資料查詢的篩選器，並識別新對象名稱和外部SFTP帳戶：

      1. 前往 **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** 並開啟套件。

      1. （選用）編輯資料的任何篩選器：

         * 在工作流程中，連按兩下查詢活動（例如ForkTransition 1）。

         * 編輯篩選運算式。

         * 按一下 **[!UICONTROL Finish]**.
      1. 為區段命名：

         * 在工作流程中，按兩下活動 **[!UICONTROL Data extraction (File)]**.

         * 開啟至 **[!UICONTROL Data extraction (File)]** 標籤，在 **[!UICONTROL File name]** 欄位，輸入副檔名為的區段名稱»`.added`&quot; （例如PaidSubscribers.added）。

            區段名稱不能已存在。 區段名稱區分大小寫，且必須包含ASCII字元，但不能包含底線(`_`)。

            不過，如果您想要將區段新增至特定 [!DNL Google Ad] 科目，然後將區段名稱加底線及 [!UICONTROL User SE Account ID] (搜尋、社交和商務ID [!DNL Google Ads] 帳戶，而非網路的帳戶ID)：

            `_<User SE Account ID>`

            範例： Paid_Subscribers_1234.added

            >[!NOTE]
            >
            >這是檔案名稱中禁止底線的規則的例外。

            否則，區段會新增至全部 [!DNL Google Ads] 正在為廣告商同步搜尋、社交和商務的帳戶。

         * 將選項保留為 **[!UICONTROL Generate an outbound transition]** 已選取。

         * 按一下 **[!UICONTROL Ok]**.
      1. 指定要向其傳送資料的外部帳戶：

         * 在工作流程中，按兩下活動 **[!UICONTROL File Transfer]**.

         * 開啟至 **[!UICONTROL File Transfer]** 標籤，在 **[!UICONTROL Remote server]** 區段，選取選項 **[!UICONTROL Use an external account]**.

         * 在 **[!UICONTROL External account]** 欄位中，選取您在步驟2中建立的外部帳戶標籤。

         * 在 **[!UICONTROL Server folder]** 欄位中，選取 [!UICONTROL Account] 外部帳戶的欄位。

         * （選用）在 **[!UICONTROL Schedule]** 索引標籤中，為檔案傳輸指定不同的排程。

            根據預設，工作流程會在00:00 （午夜）執行，以確保處理所有記錄。 若要將延遲降至最低，請將工作流程排程在18:00之前執行。

         * 按一下 **[!UICONTROL Ok]**.





搜尋、Social和Commerce每30分鐘檢查一次目錄（廣告商時區的NN：30和NN：59），並將找到的任何檔案移動到另一個位置，然後自動從資料建立受眾，並在22:00 （下午10）)將其推送到Google。 搜尋、Social和Commerce會繼續每30分鐘檢查一次電子郵件清單的更新（新增和減項），並更新上的對象 [!DNL Google Ads] 因此，每天22:00。

>[!NOTE]
>
>* 如果您在處理週期之間上傳一個以上的檔案版本，則會使用最新的檔案。
>
>* Search、Social和Commerce不會儲存您用來建立或編輯的電子郵件清單中的任何客戶資料 [!DNL Google Ads] 對象。
>
>* [!DNL Google Ads] 可能需要一些時間來處理對象的更新。
>
>* 另請參閱 [[!DNL Google Ads] 有關customer match如何運作和限制的說明檔案](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [建立 [!DNL Google Ads] 客戶比對對象來自 [!DNL Adobe] 對象](google-audience-from-adobe-audience.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)

