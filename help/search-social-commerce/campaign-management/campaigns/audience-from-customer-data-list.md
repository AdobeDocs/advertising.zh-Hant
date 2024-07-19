---
title: 使用客戶資料清單管理客戶比對受眾
description: 瞭解如何從您的客戶資料清單建立和編輯 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 客戶比對對象。
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 使用客戶資料清單管理[!DNL Google Ads]和[!DNL Microsoft Advertising]客戶比對對象

您可以從您的客戶資料清單中建立[!DNL Google Ads]和[!DNL Microsoft Advertising]個客戶比對對象。 您也可以更新任何[!DNL Google Ads]或[!DNL Microsoft Advertising]客戶比對對象，但從[!DNL Adobe]對象建立的[!DNL Google Ads]對象除外。

## 從客戶資料清單建立客戶比對對象

*[!DNL Google Ads]與[!DNL Microsoft Advertising]帳戶僅符合客戶相符的條件*

您可以從自客戶關係管理(CRM)系統產生的資料檔案建立[!DNL Google Ads]或[!DNL Microsoft Advertising]以客戶資料為基礎的清單。

對於[!DNL Microsoft Advertising]帳戶，檔案可以包含電子郵件地址。 若為[!DNL Google Ads]帳戶，檔案可包含電子郵件地址、郵寄地址或電話號碼；使用者ID；或來自您CRM的行動裝置ID。

>[!NOTE]
>
>搜尋、Social和Commerce不會儲存您上傳或用來建立或編輯[!DNL Google Ads]或[!DNL Microsoft Advertising]對象之[!DNL Adobe]區段的任何客戶資料。

1. 以所需格式產生含有客戶資料的檔案。

   名字和姓氏、電子郵件地址和電話號碼必須使用SHA-256演演算法進行雜湊處理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. -->若為[!DNL Google Ads]個對象，請參閱有關「[上傳雜湊資料格式化指南](https://support.google.com/google-ads/answer/7476159)」的[!DNL Google Ads]檔案，以取得允許的連絡資訊欄位和需求清單。 若為[!DNL Microsoft Advertising]個對象，請參閱[準備客戶比對清單](https://help.ads.microsoft.com/#apex/ads/en/56921)上的[!DNL Microsoft Advertising]檔案。 您可以選擇下載[!DNL Microsoft Excel]範本以取得連絡資訊。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 選取廣告網路和帳戶名稱，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 指定對象資訊：

   1. 在[!UICONTROL Data Source]功能表中，選取&#x200B;**[!UICONTROL Customer List]**。

   1. 輸入&#x200B;**[!UICONTROL Audience Name]**。

   1. 上傳檔案：

      1. 選取[!UICONTROL Data Upload Type]： *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*、*[!UICONTROL User IDs]*&#x200B;或&#x200B;*[!UICONTROL Mobile Device IDs]*。

         使用者ID選項僅供選擇加入[使用者ID區段](https://support.google.com/google-ads/answer/9199250)的美國[!DNL Google Ads]廣告商使用

      1. （僅限行動裝置識別碼清單）選取&#x200B;**[!UICONTROL OS Type]** （*[!UICONTROL Android™]*&#x200B;或&#x200B;*[!UICONTROL iOS]*），然後輸入&#x200B;**[!UICONTROL App ID]**。

         應用程式ID是行動作業系統使用的唯一識別碼，可讓您的應用程式連線至Google Play或Apple App Store：

         * （[!DNL Android™]個應用程式）[!DNL Google Play]內的[!DNL Android™]封裝名稱，由「`id=<package_name>`」識別。

           例如，在https://play.google.com/store/apps/details?id=com.example.game中，封裝名稱為com.example.game。

         * （[!DNL iOS]個應用程式） [!DNL iTunes App Store]內的應用程式ID，由URL結尾的&quot;`<idNNNNNNNNN>`&quot;識別。 [!DNL iOS Developer Console]中也有提供。

           例如，在https://itunes.apple.com/us/app/id284882215中，ID為id284882215。

         您的開發團隊擁有相關平台[!UICONTROL App ID]的存取權。

      1. 在[!UICONTROL Select File]欄位中，按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;並在您的網路或裝置上選取檔案。

      1. 選取核取方塊以表示您同意[!DNL Adobe]和廣告網路隱私權政策的條款。

      1. (建立在歐洲經濟區(EEA)或英國(UK)做生意的[!DNL Google Ads]受眾的廣告商；選擇性)如果您已向EEA和英國使用者收集同意，可上傳其資料作廣告用途，請選取&#x200B;**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;旁的核取方塊

      [!DNL Google Ads]會以未指定的同意狀態忽略EEA和英國使用者的任何資料。 這可能會導致資料差異和效能問題。

      1. 按一下&#x200B;**[!UICONTROL Upload File]**。

   1. 指定&#x200B;**[!UICONTROL Membership Days]**&#x200B;的數量，這是使用者的Cookie在對象中保留的天數。

   使用您預期廣告與使用者相關的時間長度。 除非您輸入值，否則客戶清單不會過期。

1. 按一下&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>* 廣告網路最多可能需要24小時的時間來處理檔案。
>* 請參閱[[!DNL Google Ads] 檔案，瞭解客戶比對的運作方式和限制](https://support.google.com/displayvideo/answer/9539301)。

## 使用客戶資料清單編輯客戶比對對象

您可以更新任何[!DNL Google Ads]或[!DNL Microsoft Advertising]客戶比對對象，但從[!DNL Adobe]對象建立的[!DNL Google Ads]對象除外。 您可以上傳資料，以新增、刪除或取代對象的所有現有資料。

資料型別必須與原始客戶清單的型別相同（電子郵件地址、郵寄地址、電話號碼、使用者ID，或特定行動作業系統上特定應用程式的行動裝置ID）。

1. 針對現有資料型別，以所需格式產生含有客戶資料的檔案。

名字和姓氏、電子郵件地址和電話號碼必須使用SHA-256演演算法進行雜湊處理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. -->若為[!DNL Google Ads]個對象，請參閱有關「[上傳雜湊資料格式化指南](https://support.google.com/google-ads/answer/7476159)」的[!DNL Google Ads]檔案，以取得允許的連絡資訊欄位和需求清單。 若為[!DNL Microsoft Advertising]個對象，請參閱[準備客戶比對清單](https://help.ads.microsoft.com/#apex/ads/en/56921)上的[!DNL Microsoft Advertising]檔案。 您可以選擇下載[!DNL Microsoft Excel]範本以取得連絡資訊。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 選取要編輯的對象旁的核取方塊。

1. 在資料表上方的工具列中，按一下![編輯](/help/search-social-commerce/assets/edit.png)。

1. 選取動作： *[!UICONTROL Add]* （將上傳的資料新增至現有資料，除非已經存在）、*[!UICONTROL Delete]* (從現有資料中刪除上傳的資料（當已經存在時），或&#x200B;*[!UICONTROL Replace]* （刪除所有現有資料並以上傳的資料取代）。

1. 上傳檔案：

   1. 在[!UICONTROL Select File]欄位中，按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;並在您的網路或裝置上選取檔案。

   1. 選取核取方塊以表示您同意[!DNL Adobe]和廣告網路隱私權政策的條款。

   1. 按一下&#x200B;**[!UICONTROL Upload File]**。

1. 按一下&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>廣告網路可能需要一些時間來處理對象的更新。

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [建立 [!DNL Google Ads] 來自 [!DNL Adobe] 受眾的客戶比對受眾](google-audience-from-adobe-audience.md)
>* [從Adobe Campaign電子郵件清單建立 [!DNL Google Ads] 客戶比對對象](google-audience-from-campaign-email-list.md)
>* [管理動態再行銷對象](audience-dynamic-remarketing-manage.md)
