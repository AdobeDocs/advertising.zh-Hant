---
title: 復寫 [!DNL Google Ads] 中的行銷活動 [!DNL Microsoft Advertising]
description: 瞭解如何在中匯出同步的行銷活動 [!DNL Google Ads] 帳戶直接進入已同步的 [!DNL Microsoft Advertising] 帳戶。
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# 復寫 [!DNL Google Ads] 中的行銷活動 [!DNL Microsoft Advertising]

您可在以下位置匯出已同步的行銷活動： [!DNL Google Ads] 帳戶直接進入已同步的 [!DNL Microsoft Advertising] 帳戶為增強型CPC (eCPC)行銷活動。 現有競標和行銷活動預算已縮放。 現有的搜尋、社交和Commerce追蹤不會匯入。

您可以復寫下列行銷活動型別及其行銷活動結構：

* [!DNL Google Ads] 搜尋行銷活動，並將其顯示至 [!DNL Microsoft Advertising] 搜尋和顯示行銷活動。

* [!DNL Google Display Network] 行銷活動（包括廣告影像）移至 [!DNL Microsoft Advertising] Microsoft Audience Network上的對象行銷活動。

  如果您想要復寫購物摘要型顯示行銷活動，請先復寫您的 [!DNL Google Merchant Center] 產品優惠目標為 [!DNL Microsoft Merchant Center]. 復寫行銷活動時，選取 [!DNL Microsoft Merchant Center] 存放在「匯入選項」中，將存放區連結至您的摘要式對象行銷活動。

* [!DNL Google Ads] 將最高成效行銷活動（包括地區詳細目錄廣告）設為 [!DNL Microsoft Advertising] 最高成效行銷活動。

您可以選擇更新行銷活動一次；每週或每月；或根據 [!DNL Microsoft Advertising]的建議排程。 您可以選擇在每次匯入工作執行或發生錯誤或變更時設定通知。 一旦您將行銷活動匯入 [!DNL Microsoft Advertising]，您可以檢查匯入工作的狀態、檢閱任何錯誤記錄檔、手動執行匯入工作，以及編輯、暫停、啟用或刪除匯入排程。

並非所有行銷活動資訊都會複製，因此您可能需要將部分資訊新增至 [!DNL Microsoft Advertising] 行銷活動。 如需匯入哪些資料的詳細資訊，請參閱 [!DNL Microsoft Advertising] 「」的說明[從何處匯入 [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).」 由於搜尋、社交和Commerce追蹤不會匯入，因此您也應該在 [帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)， [行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)， [廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，或 [廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 設定。

## 復寫 [!DNL Google Ads] 行銷活動

>[!NOTE]
>
>如果您想要複製購物摘要型顯示行銷活動，請先執行 [復寫您的 [!DNL Google Merchant Center] 中的產品優惠方案 [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). 復寫行銷活動時，選取 [!DNL Microsoft Merchant Center] 儲存在匯入選項中，將存放區連結至您的摘要式對象行銷活動。

另請參閱 [匯入來源 [!DNL Google Ads] 行銷活動](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. 在「搜尋、社交和Commerce」主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 按一下 **[!UICONTROL +Import]**.

1. 指定 [匯入設定](#campaign-import-settings)：

   1. 在 **[!UICONTROL Select accounts]** 區段：

      1. 選取來源和目的地帳戶。

      1. 按一下 **[!UICONTROL Get Credential Id from MSA]**.

      1. 登入目的地 [!DNL Microsoft Advertising] 帳戶，複製顯示的認證ID，並將值貼到 **[!UICONTROL Credential ID]** 欄位。

   1. 在 **[!UICONTROL Select campaigns & ad groups]** 區段，指定要匯入的行銷活動和廣告群組。

   1. 在 **[!UICONTROL Customize your import]** 區段，指定要匯入的專案型別。

   1. 在 **[!UICONTROL Set schedule]** 區段，指定執行匯入工作的時間。

1. 按一下 **[!UICONTROL Post]**.

1. （可選）在中新增搜尋、社交和Commerce追蹤 [帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)， [行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)， [廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，或 [廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 設定。

## 編輯行銷活動匯入工作的排程設定

另請參閱 [匯入來源 [!DNL Google Ads] 行銷活動](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 選取匯入工作旁的核取方塊，然後按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

1. 在 **[!UICONTROL Set schedule]** 區段，指定 [排程設定](#campaign-import-settings).

1. 按一下 **[!UICONTROL Post]**.

## 檢視您的行銷活動匯入工作

您可以列出所有匯入作業，包括來源 [!DNL Google Ads] 帳戶，目標 [!DNL Microsoft Advertising] 帳戶、匯入時間或排程，以及建立工作的使用者。 當您多次執行匯入工作時（包括定期排程的匯入期間），每次發生的情況都會列為一個單獨的工作。

* 執行下列任一項作業：

   * 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     依預設，檢視會開啟至 [!UICONTROL List of Import Jobs] 標籤。

   * 從 [[!UICONTROL Import Logs] 標籤](#campaign-import-log)，按一下 **[!UICONTROL List of Import Jobs]** 標籤。

## 執行行銷活動匯入工作

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 選取匯入工作旁的核取方塊。

1. 按一下 ![立即執行](/help/search-social-commerce/assets/run.png "立即執行").

## 檢視行銷活動匯入工作的記錄 {#campaign-import-log}

您可以列出所有已完成或失敗的匯入工作，包括開始時間、來源 [!DNL Google Ads] 帳戶，目標 [!DNL Microsoft Advertising] 帳戶、建立工作的使用者、成功和失敗的作業數目，以及接收每個工作之通知的任何電子郵件地址。 您可以檢視目標變更的詳細資料 [!DNL Microsoft Advertising] 每個工作發生的帳戶，包括新增、同步、刪除的專案數，以及在帳戶中為每個實體層級（例如促銷活動或關鍵字）產生錯誤的專案數。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 按一下 **[!UICONTROL Import Logs]** 標籤。

1. （選擇性）若要檢視任何匯入工作的詳細資訊，請按一下 [!UICONTROL Summary] 欄。

## 行銷活動匯入工作設定 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]：** 已同步 [!DNL Google Ads] 從中匯出行銷活動資料的帳戶。

**[!UICONTROL Credential ID]：** 此ID可以 [!DNL Microsoft Advertising] 使用表示 [!DNL Google Ads] 認證。

自動產生 [!DNL Microsoft Advertising] 無法取得匯入的認證，原因如下 [!DNL Microsoft Advertising] 限制。 請聯絡您的Adobe帳戶團隊，他們將會產生憑證並提供ID。

**[!UICONTROL Target Microsoft Ads account]：** 已同步 [!DNL Microsoft Advertising] 行銷活動資料匯入到的帳戶。

### [!UICONTROL Select campaigns & ad groups]

**\[要匯入的資料\]：** 指定要匯入的資料：

* *[!UICONTROL Import all new and existing campaigns]：* 匯入已存在的所有行銷活動以及中不存在之行銷活動的資料 [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]：* 以選取特定行銷活動和廣告群組。

   * 若要將行銷活動展開至其子廣告群組，請按一下 **[!UICONTROL >]** 促銷活動名稱之後。

   * 若要選取行銷活動或廣告群組，請選取專案以顯示核取記號。

   * 若要移除行銷活動或廣告群組：

      * 在 [!UICONTROL Campaigns] 或 [!UICONTROL Adgroups] 欄，取消選取行銷活動或廣告群組，讓核取記號消失。

      * 在 [!UICONTROL Selected] 欄，按一下 ![刪除](/help/search-social-commerce/assets/delete.png "刪除").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]：** 可讓您指定要匯入的專案、競標和預算，以及其他選項。

**[!UICONTROL What to import]：** 定義要匯入的專案。 預設會選取匯入料號類別的選項，並選取所有料號型別。 若只要包含特定專案型別，請按一下 **[!UICONTROL Show advanced options]** 並變更要納入的專案型別。

**[!UICONTROL Bids and budgets]：** 定義要匯入、更新和自訂的競標和預算設定。

**[!UICONTROL Other options]：** 定義如何處理匯入的登陸頁面URL、追蹤範本和其他行銷活動、廣告和目標定位選項。

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]：** 匯入工作的名稱。

**[!UICONTROL When]：** 何時匯入指定的行銷活動： *自動* (讓 [!DNL Microsoft Advertising] 設定排程以將行銷活動最佳化)， *[!UICONTROL Now]* （在您發佈工作設定時執行工作）， *[!UICONTROL Once]* 在指定的時間， *[!UICONTROL Daily]* 在指定的時間， *[!UICONTROL Weekly]* 在指定的時間，或 *[!UICONTROL Monthly]* 在指定的時間。

**[!UICONTROL Receive email notifications]：** 是否以及何時要將有關匯入工作的電子郵件通知傳送至「傳送報告至」欄位中的電子郵件地址。

**[!UICONTROL Send reports to]：** 用於接收匯入作業相關通知的電子郵件地址。 以逗號(`,`)。
