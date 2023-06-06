---
title: 使用客戶資料清單管理客戶比對對象
description: 瞭解如何建立和編輯 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 客戶比對客戶資料清單中的對象。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 使用客戶資料清單進行客戶比對對象

您可以建立 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 客戶比對客戶資料清單中的對象。 您也可以更新任何 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 客戶比對對象，但不包括 [!DNL Google Ads] 從以下專案建立的對象： [!DNL Adobe] 對象。

## 從客戶資料清單建立客戶比對對象

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 僅符合客戶比對資格的帳戶*

您可以建立 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 從您從客戶關係管理(CRM)系統產生的資料檔案中取得客戶資料型清單。

對象 [!DNL Microsoft® Advertising] 帳戶，檔案中可包含電子郵件地址。 對象 [!DNL Google Ads] 帳戶，檔案可包含電子郵件地址、郵寄地址或電話號碼、使用者ID或您CRM的行動裝置ID。

>[!NOTE]
>
>Search、Social和Commerce不會儲存您上傳或來自的任何客戶資料 [!DNL Adobe] 用來建立或編輯的區段 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 對象。

1. 以所需格式產生含有客戶資料的檔案。

   名字和姓氏、電子郵件地址和電話號碼必須使用SHA-256演演算法執行雜湊處理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> 對象 [!DNL Google Ads] 對象，請參閱 [!DNL Google Ads] 「」上的檔案[上傳雜湊資料的格式化准則](https://support.google.com/google-ads/answer/7476159)」以取得允許的聯絡資訊欄位和要求清單。 對象 [!DNL Microsoft® Advertising] 對象，請參閱 [!DNL Microsoft® Advertising] 檔案： [準備客戶比對清單](https://help.ads.microsoft.com/#apex/ads/en/56921. 您可以選擇下載 [!DNL Microsoft® Excel] 聯絡資訊的範本。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路和帳戶名稱，然後按一下 **[!UICONTROL Continue]**.

1. 指定對象資訊：

   1. 在 [!UICONTROL Data Source] 功能表，選取 **[!UICONTROL Customer List]**.

   1. 輸入 **[!UICONTROL Audience Name]**.

   1. 上傳檔案：

      1. 選取 [!UICONTROL Data Upload Type]： *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*， *[!UICONTROL User IDs]*，或 *[!UICONTROL Mobile Device IDs]*.

         使用者ID選項僅適用於 [!DNL Google Ads] 美國選擇加入的廣告商 [使用者ID區段](https://support.google.com/google-ads/answer/9199250)

      1. （僅限行動裝置ID清單）選取 **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* 或 *[!UICONTROL iOS]*)，並輸入 **[!UICONTROL App ID]**.

         應用程式ID是行動作業系統用來允許應用程式連線至Google Play或Apple App Store的唯一識別碼：

         * ([!DNL Android™] 應用程式) [!DNL Android™] 中的封裝名稱 [!DNL Google Play]，由「`id=<package_name>`.」

            例如，在https://play.google.com/store/apps/details?id=com.example.game中，套件名稱為com.example.game。

         * ([!DNL iOS] 應用程式)內的應用程式ID [!DNL iTunes App Store]，由「`<idNNNNNNNNN>`」在URL結尾。 此函式也適用於 [!DNL iOS Developer Console].

            例如，在https://itunes.apple.com/us/app/id284882215中，ID為id284882215。
         您的開發團隊可以存取 [!UICONTROL App ID] 相關平台的資訊。

      1. 在 [!UICONTROL Select File] 欄位，按一下 **[!UICONTROL Choose File]** 並選取網路或裝置上的檔案。

      1. 選取核取方塊以表示您同意 [!DNL Adobe] 和廣告網路隱私權原則。

      1. 按一下 **[!UICONTROL Upload File]**.
   1. 指定數量 **[!UICONTROL Membership Days]**，即使用者的Cookie在對象中停留的天數。

   使用您預期廣告與使用者相關的時間長度。 除非您輸入值，否則客戶清單不會過期。

1. 按一下 **[!UICONTROL Post]**.

>[!NOTE]
>
>* 廣告網路最多可能需要24小時來處理檔案。
>* 另請參閱 [[!DNL Google Ads] 有關customer match如何運作和限制的說明檔案](https://support.google.com/displayvideo/answer/9539301).


## 使用客戶資料清單編輯客戶比對對象

您可以更新任何 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 客戶比對對象，但不包括 [!DNL Google Ads] 從以下專案建立的對象： [!DNL Adobe] 對象。 您可以上傳資料，以新增、刪除或取代對象的所有現有資料。

資料型別必須與原始客戶清單的型別相同（電子郵件地址、郵寄地址、電話號碼、使用者ID，或特定行動作業系統上特定應用程式的行動裝置ID）。

1. 針對現有資料型別，以所需格式產生含有客戶資料的檔案。

名字和姓氏、電子郵件地址和電話號碼必須使用SHA-256演演算法執行雜湊處理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> 對象 [!DNL Google Ads] 對象，請參閱 [!DNL Google Ads] 「」上的檔案[上傳雜湊資料的格式化准則](https://support.google.com/google-ads/answer/7476159)」以取得允許的聯絡資訊欄位和要求清單。 對象 [!DNL Microsoft® Advertising] 對象，請參閱 [!DNL Microsoft® Advertising] 檔案： [準備客戶比對清單](https://help.ads.microsoft.com/#apex/ads/en/56921. 您可以選擇下載 [!DNL Microsoft® Excel] 聯絡資訊的範本。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 選取要編輯的對象旁的核取方塊。

1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png).

1. 選取動作： *[!UICONTROL Add]* （將上傳的資料新增至現有資料，除非現有資料已存在）， *[!UICONTROL Delete]* （若要從現有資料刪除已上傳的資料，只要該資料已存在），或 *[!UICONTROL Replace]* （刪除所有現有資料，並以上傳的資料取代）。

1. 上傳檔案：

   1. 在 [!UICONTROL Select File] 欄位，按一下 **[!UICONTROL Choose File]** 並選取網路或裝置上的檔案。

   1. 選取核取方塊以表示您同意 [!DNL Adobe] 和廣告網路隱私權原則。

   1. 按一下 **[!UICONTROL Upload File]**.

1. 按一下 **[!UICONTROL Post]**.

>[!NOTE]
>
>廣告網路可能需要一些時間來處理對象的更新。

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [建立 [!DNL Google Ads] 客戶比對對象來自 [!DNL Adobe] 對象](google-audience-from-adobe-audience.md)
>* [建立 [!DNL Google Ads] 來自Adobe Campaign電子郵件清單的客戶比對對象](google-audience-from-campaign-email-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)

