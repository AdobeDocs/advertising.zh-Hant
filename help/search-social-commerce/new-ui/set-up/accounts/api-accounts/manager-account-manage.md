---
title: （新UI）管理Google Ads管理員帳戶的認證
description: 瞭解如何在新的UI中設定和管理Google Ads管理員帳戶的認證。
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# （新UI）管理[!DNL Google Ads]管理員帳戶的認證

*Beta功能*

僅&#x200B;*[!DNL Google Ads]個帳戶*

提供您的[!DNL Google Ads]管理員帳戶的認證，以便Search、Social和Commerce將跨帳戶轉換上傳到該帳戶。 如果您想要a)將[!DNL Adobe]追蹤的跨帳戶轉換量度上傳至[!DNL Google Ads]管理員帳戶，或b)將包含跨帳戶轉換的產品組合目標上傳至[!DNL Google Ads]以進行混合最佳化，請使用此功能。

您可以為新的管理員帳戶記錄新增認證，或重新驗證現有的管理員帳戶。

新增管理員帳戶的認證後，帳戶設定會將關聯的管理員帳戶ID顯示為唯讀。 [!UICONTROL Notification Center]包含管理員帳戶的認證遺失([!UICONTROL Manager Account Missing Error])或管理員帳戶的驗證權杖過期([!UICONTROL Manager Account Auth Error])時的[通知](/help/search-social-commerce/new-ui/notifications-manage.md)。

## 為新的管理員帳戶新增認證 {#create-manager-account}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**。

1. 按一下&#x200B;**[!UICONTROL +]**。

1. 選取廣告網路，然後按一下&#x200B;**[!UICONTROL Next]**。

1. 指定[管理員帳戶設定](#manager-account-settings)。

1. 按一下&#x200B;**[!UICONTROL Authenticate]**&#x200B;並使用管理員帳戶認證登入。

   搜尋、Social和Commerce會自動擷取並儲存驗證Token。

1. 在「搜尋」、「社交」和「Commerce」中，按一下&#x200B;**[!UICONTROL Save]**。

## 編輯管理員帳戶詳細資料 {#edit-manager-account}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**。

1. 以下列任一方式選取該帳戶：

   * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

   * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下（/help/search-social-commerce/assets/edit-new.png「編輯」）。

1. 編輯[管理員帳戶設定](#manager-account-settings)。

1. 按一下&#x200B;**[!UICONTROL Re-Authenticate]**&#x200B;並使用管理員帳戶認證登入。

   搜尋、Social和Commerce會自動擷取並儲存驗證Token。

1. 在「搜尋」、「社交」和「Commerce」中，按一下&#x200B;**[!UICONTROL Save]**。

## 重新驗證管理員帳戶 {#reauthenticate-manager-account}

當OAuth權杖過期或失效時，重新驗證管理員帳戶。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**。

1. 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Reauthenticate]**。

1. 使用管理員帳戶認證登入。

   搜尋、Social和Commerce會自動擷取並儲存新的驗證Token。

## 管理員帳戶設定 {#manager-account-settings}

**[!UICONTROL Manager Account ID]：**&#x200B;廣告網路上管理員帳戶的唯一帳戶識別碼。

**[!UICONTROL Mnaager Account Name]：**&#x200B;要在Search、Social和Commerce中為經理帳戶顯示的名稱。

**[!UICONTROL Login Email]：**&#x200B;與管理員帳戶登入相關聯的電子郵件地址。 驗證所需。

**[!UICONTROL Password]：** （選擇性）帳戶的密碼。 當您想要加密並儲存密碼時，請輸入密碼，以便帳戶管理員視需要重新整理權杖。

>[!MORELIKETHIS]
>
>* [啟用上傳目標至廣告網路](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [管理通知](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
