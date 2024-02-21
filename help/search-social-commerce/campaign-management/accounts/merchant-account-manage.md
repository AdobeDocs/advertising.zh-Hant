---
title: 管理商家帳戶
description: 瞭解如何設定及管理商戶中心帳戶的帳戶詳細資料。
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: 35a27d075d5de7c3526cd6522376671954b608db
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# 管理商家帳戶

*僅限代理商帳戶管理員、Adobe帳戶管理員及管理員使用者角色*

搜尋、Social和Commerce可每天下載並顯示廣告商的Google商家中心或Microsoft商家中心帳戶的產品資料。 此外，搜尋、Social和Commerce可以根據商家帳戶的內容自動建立廣告。若要直接在Search、Social和Commerce中使用產品資料，您必須建立包含帳戶存取憑證和存取權的對應帳戶記錄 *已啟用*.

>[!NOTE]
>
>您無法移除商家帳戶記錄。 您可以將帳戶型別變更為，以停用帳戶的存取權 *已停用*.

## 建立商家帳戶詳細資料 {#create-merchant-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員及管理員使用者角色*

若要檢視產品資料並為商家帳戶產生追蹤範本，以及根據資料建立廣告，您必須建立包含帳戶存取認證且有權存取帳戶的對應帳戶記錄 *已啟用*.

>[!NOTE]
>
>若要在商家網路上建立實際帳戶，請前往該網路的網站。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**，隨即開啟以 [!UICONTROL Accounts] 標籤。

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Create Account]**.

1. 指定 [商家帳戶設定](#merchant-account-settings)：

   1. 在 [!UICONTROL Product Source] 功能表，選取商家中心。

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (下列專案需要： [!DNL Google Ads] 帳戶；選擇性的 [!DNL Microsoft Advertising] 帳戶)允許搜尋、社交和商務使用存取帳戶 [[!DNL OAuth] 授權通訊協定](https://oauth.net/2/)：

      1. ([!DNL Microsoft Advertising] 僅限帳戶)選取 **[!UICONTROL oAuth]**.

      1. 按一下 **[!UICONTROL Enable Connection]**.

      1. （如果您未登入廣告商的帳戶）登入廣告商的帳戶。 最佳實務是使用認證來存取商家中心帳戶的內容API。

      1. 在存取權/許可權要求畫面中，按一下按鈕以確認許可權。

      1. 在開啟的快顯視窗中複製驗證字串，並將該字串貼到 **[!UICONTROL oAuth Token]** 欄位。

      1. 指定其他帳戶設定。

1. 按一下 **[!UICONTROL Save]**.

   下一次每日同步程式後，可在Search、Social和Commerce中使用帳戶中所有產品的屬性資料（大約使用者當地時區的06:00）。 然後，您可以使用產品資料，使用詳細目錄摘要來自動化廣告建立。

## 編輯商家帳戶詳細資料 {#edit-merchant-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員及管理員使用者角色*

如果帳戶認證變更，或您想要停止擷取和使用商家帳戶的資料，請編輯帳戶詳細資料。

>[!NOTE]
>
>若要編輯商家網路上的實際帳戶，請前往該網路的網站。

1. 在主功能表中，按一下 **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**，隨即開啟以 [!UICONTROL Accounts] 標籤。

1. 在帳戶名稱旁邊，按一下 ![檢視/編輯設定](/help/search-social-commerce/assets/settings.png "檢視/編輯設定").

1. 編輯 [商家帳戶設定](#merchant-account-settings).

1. 按一下 **[!UICONTROL Save]**.

>[!NOTE]
>
>搜尋、Social和Commerce必須將新帳戶資料與商家網路上的資料同步。 這會在使用者的當地時區中每天大約06:00自動發生一次。

## 停用對商家帳戶的存取權 {#disable-merchant-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員及管理員使用者角色*

當您停用商家帳戶時，Search、Social和Commerce不會登入帳戶，因此不會擷取更新的產品資料。 帳戶啟用時收集的資料仍會儲存，且使用產品資料建立的現有廣告不會根據摘要範本和摘要資料設定進行更新、暫停或刪除。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** ，隨即開啟以 [!UICONTROL Accounts] 標籤。

1. 在帳戶名稱旁邊，按一下 ![檢視/編輯設定](/help/search-social-commerce/assets/settings.png "檢視/編輯設定").

1. 變更 [!UICONTROL EF Account Type] 至 **[!UICONTROL Disabled]**.

1. 按一下 **[!UICONTROL Save]**.

## 商家帳戶設定 {#merchant-account-settings}

>[!NOTE]
>
>僅限代理客戶經理， [!DNL Adobe] 帳戶管理員和管理員使用者角色可以設定商家帳戶設定。

**[!UICONTROL Product Source]：** 商家網路。 您無法變更現有帳戶的值。

**[!UICONTROL OAuth Token]：** ([!DNL Google Merchant Center] 僅限帳戶)帳戶的Token，可授權使用 [[!DNL OAuth] 授權通訊協定](https://oauth.net/2/).

**[!UICONTROL Auth Type]：** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] 僅限)是否授權使用登入帳戶：

* *[!UICONTROL Client login]：* 使用使用者端的登入。

* *[!UICONTROL oAuth]* （預設）：若要使用 [[!DNL OAuth] 授權通訊協定](https://oauth.net/2/).

**[!UICONTROL Access Key]：** ([!DNL Microsoft Merchant Center] 僅限開發人員帳戶使用的存取金鑰。

**[!UICONTROL Account Name]：** 在「搜尋」、「社交」和「商務」中顯示的帳戶名稱。

**[!UICONTROL Login]：** 帳戶的登入名稱或ID。

**[!UICONTROL Password]：** 帳戶的密碼。

**[!UICONTROL Confirm Password]：** 帳戶的密碼。

**[!UICONTROL EF Account Type]：** Search、Social和Commerce是否會存取該帳戶：

* *[!UICONTROL Enabled]* （預設）： Search、Social和Commerce可以登入帳戶以擷取產品資料。

* *[!UICONTROL Disabled]：* Search、Social和Commerce不會登入帳戶，因此不會擷取更新的產品資料。 帳戶啟用時收集的資料仍會儲存，且使用產品資料建立的現有廣告不會根據摘要範本和摘要資料設定進行更新、暫停或刪除。

**[!UICONTROL Account ID]：** 商家帳戶ID。 如果您只有一個帳戶具有指定的登入資訊，則此值為選用值。

**[!UICONTROL Time Zone]：** 廣告商的時區。 使用為廣告商的搜尋、社交和商務帳戶資訊（建立帳戶時設定）設定的相同時區。 您無法變更現有帳戶的值。

>[!MORELIKETHIS]
>
>* [關於廣告網路帳戶](ad-network-account-about.md)
>* [管理廣告網路帳戶](ad-network-account-manage.md)
