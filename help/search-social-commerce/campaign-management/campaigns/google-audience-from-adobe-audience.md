---
title: 建立來自 [!DNL Adobe] 受眾的 [!DNL Google Ads] 客戶比對受眾
description: 瞭解如何從您現有的Adobe Analytics和Audience Manager對象建立 [!DNL Google Ads] 客戶比對對象。
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# 從Adobe Analytics和Audience Manager受眾建立[!DNL Google Ads]個客戶比對受眾

*[!DNL Google Ads]個帳戶僅符合客戶相符資格*

*僅具有Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics整合的廣告商*

選擇加入的廣告商可使用下列來源的使用者ID建立[!DNL Google Ads]個客戶相符對象：a) [!DNL Analytics]與Adobe Experience Cloud共用的區段，以及b)以Search、Social和Commerce作為目的地的Audience Manager區段，包括發佈至Adobe Experience Cloud的[!DNL Analytics]區段，以及使用Adobe Experience Cloud對象庫建立的區段。 搜尋、Social和Commerce會自動將[!DNL Google]追蹤URL推送回每個[!DNL Analytics]或Audience Manager區段，讓[!DNL Google]可以追蹤對象。

每個[!DNL Adobe]對象只能用於一個[!DNL Google]對象。

每個新[!DNL Google]對象與原始[!DNL Adobe]對象具有相同名稱。 [!DNL Google]決定要定位的對象必須有多大。

>[!TIP]
>
>如需即時細分，請使用Audience Manager建立的對象。 在[!DNL Analytics]中建立並同步至Adobe Experience Cloud的區段可能會包含較少的母體，因為這些區段只會每天同步；符合區段資格的瀏覽者可能直到隔天才會包含在區段中。 來自[!DNL Analytics]的區段有資料來源「報告套裝 — 」。

>[!NOTE]
>
>搜尋、Social和Commerce不會儲存您用來建立或編輯[!DNL Google]對象之[!DNL Adobe]區段的任何客戶資料。

1. 視需要完成必要條件：

   1. （若要建立使用者ID再行銷清單對象） [!DNL Adobe]管理員使用者或帳戶管理員必須選取廣告商層級的設定，才能啟用客戶比對對象。

   1. 實作[Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) 2.0或更新版本。

   1. 在廣告商的網頁上儘可能部署以下標籤，並從中追蹤對象

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      其中`Advertising_Cloud_UserID`是指派給廣告商的唯一數值使用者ID。

      範例： `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （如果尚未完成）授權的使用者必須將廣告商帳戶設定為[與Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md)中的廣告商組織帳戶同步。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 選取廣告網路和帳戶名稱，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 指定對象資訊：

   1. 在&#x200B;**[!UICONTROL Data Source]**&#x200B;功能表中，選取&#x200B;**[!UICONTROL Adobe Audience]**。

   1. 選取[!DNL Google]對象所依據的[!UICONTROL Adobe Audience]。

      >[!NOTE]
      >
      >已用於其他[!DNL Google]個對象的[!DNL Adobe]個對象無法使用。

      您可以選擇搜尋包含至少三個字元之特定文字字串的對象。 對於任何相符的對象，按一下&#x200B;**[!UICONTROL Include]**&#x200B;以選取它。

      如果您選取多個[!DNL Adobe]對象，則會為每個建立個別的[!DNL Google]對象。

   1. 選取要建立的&#x200B;**[!UICONTROL Audience Type]**： **[!UICONTROL Customer List_User ID]**。

      廣告商的[!DNL Google Ads]帳戶必須符合[自訂相符專案](https://support.google.com/adspolicy/answer/6299717)的資格，並已選擇加入[使用者ID再行銷](https://support.google.com/google-ads/answer/9199250)。

   1. 選取核取方塊以表示您同意[!DNL Adobe]和廣告網路隱私權政策的條款。

   1. 指定&#x200B;**[!UICONTROL Membership Days]**&#x200B;的數量，這是使用者的Cookie在對象中保留的天數。

      使用您預期廣告與使用者相關的時間長度。 再行銷清單的最長期限為540天。 客戶清單沒有持續時間上限；若要指出Cookie永不過期，請輸入10000。

   1. 按一下&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>* [!DNL Google]最多可能需要24小時來處理檔案。
>
>* 請參閱[[!DNL Google Ads] 檔案，瞭解客戶比對的運作方式和限制](https://support.google.com/displayvideo/answer/9539301)。

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [從Adobe Campaign電子郵件清單建立 [!DNL Google Ads] 客戶比對對象](google-audience-from-campaign-email-list.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)
