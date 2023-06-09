---
title: 建立 [!DNL Google Ads] 客戶比對對象來自 [!DNL Adobe] 對象
description: 瞭解如何建立 [!DNL Google Ads] 客戶會比對來自您現有Adobe Analytics和Audience Manager對象的對象。
source-git-commit: 7089f7fe75b551953026ac6cca4ac7aafa06ba7b
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 建立 [!DNL Google Ads] 客戶比對來自Adobe Analytics和Audience Manager受眾的受眾

*[!DNL Google Ads]僅符合客戶比對資格的帳戶*

*僅具有Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics整合的廣告商*

選擇加入的廣告商可以建立 [!DNL Google Ads] 客戶使用來自的使用者ID比對對象) [!DNL Analytics] 與Adobe Experience Cloud共用的區段，以及b)以「搜尋、社交和商務」為目的地的Audience Manager區段，包括 [!DNL Analytics] 發佈至Adobe Experience Cloud的區段，以及使用Adobe Experience Cloud對象庫建立的區段。 搜尋、Social和Commerce會自動推送 [!DNL Google] 追蹤URL回到 [!DNL Analytics] 或Audience Manager區段，以 [!DNL Google] 可以追蹤對象。

每個 [!DNL Adobe] 對象只能使用一個 [!DNL Google] 對象。

每個新 [!DNL Google] 對象與原始對象具有相同名稱 [!DNL Adobe] 對象。 [!DNL Google] 決定要定位的對象必須有多大。

>[!TIP]
>
>如需即時細分，請使用Audience Manager建立的對象。 在中建立的區段 [!DNL Analytics] 同步至Adobe Experience Cloud的瀏覽者數量可能會較少，因為它們只會每天同步；而符合區段資格的瀏覽者，可能直到隔天才會納入區段中。 區段來源 [!DNL Analytics] 擁有「報告套裝 — 」的資料來源。

>[!NOTE]
>
>Search、Social和Commerce不會儲存您網站的任何客戶資料， [!DNL Adobe] 用來建立或編輯的區段 [!DNL Google] 對象。

1. 視需要完成必要條件：

   1. （若要建立使用者ID再行銷清單對象） An [!DNL Adobe] 管理員使用者或帳戶管理員必須選取廣告商層級的設定，以啟用客戶比對受眾。 設定在具有Audience Manager的廣告商和具有 [!DNL Analytics] 僅限。

   1. 實作 [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) 2.0版或更新版本。

   1. 在廣告商的網頁上儘可能部署以下標籤，並從中追蹤對象

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      位置 `Advertising_Cloud_UserID` 是指派給廣告商的不重複使用者ID。 範例：  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （如果尚未完成）授權使用者必須將廣告商帳戶設定為 [在Adobe Experience Cloud中與廣告商的組織帳戶同步](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路和帳戶名稱，然後按一下 **[!UICONTROL Continue]**.

1. 指定對象資訊：

   1. 在 **[!UICONTROL Data Source]** 功能表，選取 **[!UICONTROL Adobe Audience]**.

   1. 選取 [!UICONTROL Adobe Audience] 作為基礎的 [!DNL Google] 對象。

      >[!NOTE]
      >
      >[!DNL Adobe] 已用於其他對象的對象 [!DNL Google] 對象無法使用。

      您可以選擇搜尋包含至少三個字元之特定文字字串的對象。 如需任何相符的對象，請按一下 **[!UICONTROL Include]** 以選取它。

      如果您選取多個 [!DNL Adobe] 受眾，然後為個別受眾 [!DNL Google] 會為每個對象建立對象。

   1. 選取 **[!UICONTROL Audience Type]** 若要建立： **[!UICONTROL Customer List_User ID]**.

      廣告商的 [!DNL Google Ads] 帳戶必須是 [符合自訂比對的資格](https://support.google.com/adspolicy/answer/6299717) 並選擇加入 [使用者ID再行銷](https://support.google.com/google-ads/answer/9199250).

   1. 選取核取方塊以表示您同意 [!DNL Adobe] 和廣告網路隱私權原則。

   1. 指定數量 **[!UICONTROL Membership Days]**，即使用者的Cookie在對象中停留的天數。

      使用您預期廣告與使用者相關的時間長度。 再行銷清單的最長期限為540天。 客戶清單沒有持續時間上限；若要指示Cookie永不過期，請輸入10000。

   1. 按一下 **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] 處理檔案最多可能需要24小時。
>
>* 另請參閱 [[!DNL Google Ads] 有關customer match如何運作和限制的說明檔案](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [建立 [!DNL Google Ads] 來自Adobe Campaign電子郵件清單的客戶比對對象](google-audience-from-campaign-email-list.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)
