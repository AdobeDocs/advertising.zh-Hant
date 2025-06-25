---
title: 管理廣告網路管理員帳戶的認證
description: 瞭解如何為您的 [!DNL Google Ads] 管理員帳戶提供認證。
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# 管理廣告網路管理員帳戶的認證

僅&#x200B;*[!DNL Google Ads]個帳戶*

提供您的[!DNL Google Ads]管理員帳戶的認證，以便Search、Social和Commerce將跨帳戶轉換上傳到該帳戶。 如果您想要a)將[!DNL Adobe]追蹤的跨帳戶轉換量度上傳至[!DNL Google Ads]管理員帳戶，或b)將包含跨帳戶轉換的產品組合目標上傳至[!DNL Google Ads]以進行混合最佳化，請使用此功能。

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

您可以為新的管理員帳戶記錄新增認證，或重新驗證現有的管理員帳戶。

新增管理員帳戶的認證後，帳戶設定會將關聯的管理員帳戶ID顯示為唯讀。 此外，[!UICONTROL Campaigns] > [!UICONTROL Accounts]檢視中的選用&quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot;欄會顯示每個子帳戶的管理員帳戶ID，並在管理員帳戶未驗證時指出錯誤。 [!UICONTROL Notification Center]包含遺失管理員帳戶認證（[該[!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)）或管理員帳戶驗證Token過期時（[該[!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)）的通知。

## 若要為新的管理員帳戶新增認證

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**。

1. 選取&#x200B;**[!UICONTROL Create new manager account]**。

1. 輸入管理員帳戶的登入認證。

   需要&#x200B;**[!UICONTROL Manager Account ID]**&#x200B;和&#x200B;**[!UICONTROL Login Email]**。 搜尋、Social和Commerce會自動擷取並儲存用於驗證的帳戶權杖。

   您可以選擇在Search、Social和Commerce以及帳戶&#x200B;**[!UICONTROL Password]**&#x200B;中加入&#x200B;**[!UICONTROL MCC Account Name]**&#x200B;以識別。 當您想要加密並儲存密碼時，請輸入密碼，以便帳戶管理員視需要重新整理權杖。

1. 按一下&#x200B;**[!UICONTROL Authenticate]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 若要重新驗證現有的管理員帳戶

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**。

1. 選取&#x200B;**[!UICONTROL Reauthenticate existing manager account]**。

1. 選取管理員帳戶。

1. 輸入管理員帳戶的登入認證。

   需要&#x200B;**[!UICONTROL Manager Account ID]**&#x200B;和&#x200B;**登入電子郵件**。 搜尋、Social和Commerce會自動擷取並儲存用於驗證的帳戶權杖。

   您可以選擇在Search、Social和Commerce以及帳戶&#x200B;**[!UICONTROL Password]**&#x200B;中加入&#x200B;**[!UICONTROL MCC Account Name]**&#x200B;以識別。 當您想要加密並儲存密碼時，請輸入密碼，以便帳戶管理員視需要重新整理權杖。

1. 按一下&#x200B;**[!UICONTROL Authenticate]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [啟用上傳目標至廣告網路](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [將搜尋、社交和Commerce追蹤的轉換量度上傳至 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [編輯您的通知設定](/help/search-social-commerce/notifications/notification-edit.md)
