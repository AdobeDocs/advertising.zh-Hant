---
title: （新UI）僅管理 [!DNL Naver] 帳戶以進行追蹤
description: 瞭解如何在 [!DNL Naver] 帳戶的全新UI中設定和管理帳戶詳細資料。
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# （新UI）管理[!DNL Naver]帳戶僅供追蹤

*Beta功能*

下列是管理[[!DNL Naver] 帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)的指示，以追蹤、報告您直接從廣告網路購買的廣告並加以視覺化效能。 搜尋、Social和Commerce不會將資料與廣告網路同步、提供自動競標，也不會提供任何型別的最佳化或模擬。

如需可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

## 建立廣告網路帳戶詳細資料 {#create-account}

若要啟用帳戶追蹤，您必須建立包含帳戶存取認證且狀態為&#x200B;*已啟用*&#x200B;的對應帳戶記錄。

>[!NOTE]
>
>若要在廣告網路上建立實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 按一下&#x200B;**[!UICONTROL Create Account]**。

1. 按一下廣告網路的名稱，然後按一下&#x200B;**[!UICONTROL Next]**。

1. 指定[帳戶設定](#account-settings-naver)：

   1. 在&#x200B;**[!UICONTROL Enter Account Details]**&#x200B;標籤上，指定一般帳戶設定。

   1. （具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商）按一下「**[!UICONTROL Set up Adobe Analytics]**」標籤，然後選取所有[!DNL Analytics]報告套裝以用於追蹤和報告行銷活動活動。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 編輯廣告網路帳戶詳細資料 {#edit-account}

若要變更帳戶名稱、變更帳戶狀態或變更[!DNL Analytics]用於追蹤和報告的報表套裝，請編輯帳戶詳細資料。

>[!NOTE]
>
>若要編輯廣告網路上的實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 以下列任一方式選取該帳戶：

   * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

   * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[帳戶設定](#account-settings-api)：

   1. （選擇性）在&#x200B;**[!UICONTROL Account Details]**&#x200B;索引標籤上，編輯帳戶詳細資料。

   1. （選用；具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商）按一下「**[!UICONTROL Set up Adobe Analytics]**」標籤，然後編輯[!DNL Analytics]報告套裝，以用於追蹤和報告行銷活動活動。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 按一下&#x200B;**[!UICONTROL Save]**。

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## 廣告網路帳戶設定 {#account-settings-api}

### [!UICONTROL Account Details]索引標籤

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]：**&#x200B;要顯示在Search、Social和Commerce中的帳戶名稱。

>[!NOTE]
>
>如果您已整合「搜尋」、「社交」和「Commerce-Adobe Analytics」，並變更搜尋帳戶的名稱，請要求您的Adobe帳戶團隊更新對應。

**[!UICONTROL Network Account ID]：**&#x200B;廣告網路所指派的帳戶識別碼。

**[!UICONTROL Currency]：**&#x200B;帳戶所用貨幣的縮寫。

**[!UICONTROL Time Zone]：**&#x200B;廣告商的時區。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]：**&#x200B;搜尋、Social和Commerce會與帳戶同步行銷活動資料（若有支援），並針對產品組合中的行銷活動推送自動競標和/或行銷活動預算。

## [!UICONTROL Setup Analytics]索引標籤

**[!UICONTROL Adobe Analytics Report Suite]：** （具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商；選擇性）一或多個Analytics報告套裝會傳送您為廣告網路上傳的資料（包括帳戶的實體分類和點按資料），給Search、Social和Commerce傳送這些資料。

若要讓資料顯示在報表套裝中，(a)必須為帳戶設定伺服器端AMO ID功能，或(b)必須啟用&quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot;的廣告商層級設定。 此外，廣告商的[!DNL Analytics]帳戶必須設定為從Search、Social和Commerce接收資料。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

>[!MORELIKETHIS]
>
>* [實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [關於廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
