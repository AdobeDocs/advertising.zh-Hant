---
title: 設定用於資料上載的廣告網路帳戶
description: 瞭解如何設定及管理廣告網路帳戶的帳戶詳細資料。
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: 00565a6c9e784472fab9c9d223c83b0c7cbb91b1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# 管理資料上傳的廣告網路帳戶

<!-- Edit all, including title and metadata -->

下列是管理您將為其上傳帳戶資料的廣告網路帳戶的帳戶詳細資訊的指示。

如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

>[!NOTE]
>
>如需有關使用廣告網路的API管理廣告網路帳戶(搜尋、社交和Commerce同步)的帳戶詳細資訊的指示，請改為參閱「透過API連線管理廣告網路帳戶[」。](../api-accounts/api-account-manage.md)

## 建立帳戶詳細資料 {#create-account}

1. 按一下&#x200B;**[!UICONTROL Create Account]**。

1. 按一下廣告網路的名稱，然後按一下&#x200B;**[!UICONTROL Next]**。

1. 指定[帳戶設定](#account-settings)：

   1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;標籤上，編輯帳戶詳細資料。

   1. （具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商）按一下「**[!UICONTROL Set up Adobe Analytics]**」標籤，然後編輯[!DNL Analytics]報告套裝，以用於追蹤和報告行銷活動活動。

   1. （選擇性）在&#x200B;**[!UICONTROL Upload File]**&#x200B;索引標籤上，上傳帳戶的資料檔案。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 編輯帳戶詳細資料 {#edit-account}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 以下列任一方式選取該帳戶：

   * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

   * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[帳戶設定](#account-settings-upload)：

   1. （選擇性）在&#x200B;**[!UICONTROL Account Details]**&#x200B;索引標籤上，編輯帳戶詳細資料。

   1. （選用；具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商）按一下「**[!UICONTROL Set up Adobe Analytics]**」標籤，然後編輯[!DNL Analytics]報告套裝，以用於追蹤和報告行銷活動活動。

   1. （選擇性）在&#x200B;**[!UICONTROL Upload File]**&#x200B;索引標籤上，上傳帳戶的資料檔案。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 啟用或停用廣告網路帳戶 {#enable-disable-account}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 執行下列任一項作業：

   * （從[!UICONTROL Accounts]檢視）：

      * （若要啟用帳戶）選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Activate]**。

      * （若要停用帳戶）選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Pause]**。

   * （從帳戶設定）：

      1. 以下列任一方式選取該帳戶：

         * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

         * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

      1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;標籤上，關閉&#x200B;**[!UICONTROL Account enabled]**。

      1. 按一下&#x200B;**[!UICONTROL Save]**。

## 帳戶設定 {#account-settings-upload}

### [!UICONTROL Account Details]索引標籤

**[!UICONTROL Account Name]：**&#x200B;要顯示在Search、Social和Commerce中的帳戶名稱。

>[!NOTE]
>
>如果您已整合「搜尋」、「社交」和「Commerce-Adobe Analytics」，並變更搜尋帳戶的名稱，然後通知您的Adobe帳戶團隊，讓他們可以更新對應。

**[!UICONTROL Network Account ID]：**&#x200B;廣告網路所指派的帳戶識別碼。 此ID僅用於報表。 搜尋、社交和Commerce不會直接連線到廣告網路帳戶。

**[!UICONTROL Currency]：** （現有帳戶的唯讀）帳戶所使用的貨幣縮寫。

**[!UICONTROL Time Zone]：** （現有帳戶的唯讀）廣告商的時區。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]：**&#x200B;搜尋、Social和Commerce允許針對指定的S3儲存貯體自動擷取資料。

## [!UICONTROL Setup Analytics]索引標籤

**[!UICONTROL Adobe Analytics Report Suite]：** （具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商；選擇性）一或多個Analytics報告套裝會傳送您為廣告網路上傳的資料（包括帳戶的實體分類和點按資料），給Search、Social和Commerce傳送這些資料。

若要讓資料顯示在報表套裝中，(a)必須為帳戶設定伺服器端AMO ID功能，或(b)必須啟用&quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot;的廣告商層級設定。 此外，廣告商的[!DNL Analytics]帳戶必須設定為從Search、Social和Commerce接收資料。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

### [!UICONTROL Upload File]索引標籤

（選用）上傳帳戶的資料檔案。<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
