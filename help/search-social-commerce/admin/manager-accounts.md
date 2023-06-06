---
title: 管理廣告網路管理員帳戶的認證
description: 瞭解如何為提供認證 [!DNL Google Ads] 經理帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# 管理廣告網路管理員帳戶的認證

*Beta功能*

*[!DNL Google Ads]僅限帳戶*

提供您的憑證給 [!DNL Google Ads] 您希望Search、Social和Commerce將跨帳戶轉換上傳到的經理帳戶。 如果您想要)上傳，請使用此功能 [!DNL Adobe] — 追蹤、跨帳戶轉換量度至 [!DNL Google Ads] 經理帳戶或b)上傳包含跨帳戶轉換的產品組合目標至 [!DNL Google Ads] 混合最佳化。

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

您可以為新管理員帳戶記錄新增認證，或重新驗證現有的管理員帳戶。

新增管理員帳戶的認證後，帳戶設定會將關聯的管理員帳戶ID顯示為唯讀。 此外，選購的&quot;[!UICONTROL Manager Account for Cross-Account Conversions]「 」欄，在 [!UICONTROL Campaigns] > [!UICONTROL Accounts] 檢視會顯示每個子帳號的管理員帳號ID，並在未驗證管理員帳號時指出錯誤。 [!UICONTROL Notification Center] 包含遺失管理員帳戶認證時的通知([此 [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md))或manager帳戶驗證Token過期時([此 [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md))。

## 若要為新的管理員帳戶新增認證

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 選取 **[!UICONTROL Create new manager account]**.

1. 輸入管理員帳戶的登入認證。

   此 **[!UICONTROL Manager Account ID]** 和 **[!UICONTROL Login Email]** 為必填欄位。 搜尋、Social和Commerce會自動擷取並儲存用於驗證的帳戶Token。

   您可以選擇加入 **[!UICONTROL MCC Account Name]** 用於在Search、Social和Commerce及帳戶中識別 **[!UICONTROL Password]**. 當您想要加密並儲存密碼時，請輸入密碼，以便帳戶管理員視需要重新整理Token。

1. 按一下 **[!UICONTROL Authenticate]**.

1. 按一下 **[!UICONTROL Save]**.

## 若要重新驗證現有的管理員帳戶

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 選取 **[!UICONTROL Reauthenticate existing manager account]**.

1. 選取經理帳戶。

1. 輸入管理員帳戶的登入認證。

   此 **[!UICONTROL Manager Account ID]** 和 **登入電子郵件** 為必填欄位。 搜尋、Social和Commerce會自動擷取並儲存用於驗證的帳戶Token。

   您可以選擇加入 **[!UICONTROL MCC Account Name]** 用於在Search、Social和Commerce及帳戶中識別 **[!UICONTROL Password]**. 當您想要加密並儲存密碼時，請輸入密碼，以便帳戶管理員視需要重新整理Token。

1. 按一下 **[!UICONTROL Authenticate]**.

1. 按一下 **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [啟用上傳目標至廣告網路](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [上傳轉換量度至 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [編輯您的通知設定](/help/search-social-commerce/notifications/notification-edit.md)

