---
title: （新UI）在Microsoft Advertising中複製Google Ads行銷活動
description: 瞭解如何將Google Ads帳戶中同步的行銷活動直接匯出至同步的Microsoft Advertising帳戶。
feature: Search Campaign Management
exl-id: d4f8e452-7b3d-4a1f-9c3e-6b8d2e5a4917
source-git-commit: 3f769f18ce006278b12a62f8d837d60affffda65
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# （新UI）在[!DNL Microsoft Advertising]中復寫[!DNL Google Ads]個行銷活動

*Beta功能*

您可以將[!DNL Google Ads]帳戶中同步的行銷活動直接匯出到同步的[!DNL Microsoft Advertising]帳戶，做為增強型CPC (eCPC)行銷活動。 現有競標和行銷活動預算已縮放。 現有的搜尋、社交和Commerce追蹤不會匯入。

您可以復寫下列行銷活動型別及其行銷活動結構：

* [!DNL Google Ads]在[!DNL Microsoft Advertising]個搜尋和顯示行銷活動中搜尋和顯示行銷活動。

* 在Microsoft Audience Network上將[!DNL Google Display Network]個行銷活動（包括廣告影像）匯入[!DNL Microsoft Advertising]個對象行銷活動。

  如果您想要復寫購物摘要型顯示行銷活動，請先將您的[!DNL Google Merchant Center]產品優惠復寫至[!DNL Microsoft Merchant Center]。 復寫行銷活動時，在匯入選項中選取[!DNL Microsoft Merchant Center]存放區，以將存放區連結至您的摘要式對象行銷活動。

* 將[!DNL Google Ads]個最高成效行銷活動（包括本地詳細目錄廣告）轉換為最高[!DNL Microsoft Advertising]成效行銷活動。

您可以選擇更新一次行銷活動；每日、每週或每月；或根據[!DNL Microsoft Advertising]的建議排程。 您可以選擇在每次匯入工作執行或發生錯誤或變更時設定通知。 將行銷活動匯入[!DNL Microsoft Advertising]後，您可以檢查匯入工作的狀態、檢閱任何錯誤記錄檔、手動執行匯入工作，以及編輯、暫停、啟用或刪除匯入排程。

並非所有行銷活動資訊都已復寫，您可能需要將一些資訊新增到[!DNL Microsoft Advertising]行銷活動。 如需匯入哪些資料的詳細資訊，請參閱[!DNL Microsoft Advertising]有關「[哪些資料是從 [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"}匯入」的說明。 因為未匯入搜尋、社交和Commerce追蹤，您也應該在[帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)或[廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)設定中新增追蹤。

## 復寫[!DNL Google Ads]個行銷活動

>[!NOTE]
>
>如果您想要復寫購物摘要型顯示行銷活動，請先在 [!DNL Microsoft Merchant Center][&#128279;](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}中復寫您的 [!DNL Google Merchant Center] 產品選件。 復寫行銷活動時，在匯入選項中選取[!DNL Microsoft Merchant Center]存放區，以將存放區連結至您的摘要式對象行銷活動。

檢視[從 [!DNL Google Ads] 行銷活動](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}匯入的專案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 按一下&#x200B;**[!UICONTROL Import Campaigns]**。

1. 指定[匯入設定](#campaign-import-settings)：

   1. 在&#x200B;**[!UICONTROL Select accounts]**&#x200B;步驟中：

      1. 在&#x200B;**[!UICONTROL Import Name]**&#x200B;欄位中輸入匯入工作的名稱。

      1. 選取來源[!DNL Google Ads]帳戶和目標[!DNL Microsoft Advertising]帳戶。

      1. 輸入您的&#x200B;**[!UICONTROL Credential ID]**。 如果您沒有認證ID，請連絡您的Adobe帳戶團隊 — 因為[!DNL Microsoft Advertising]限制，無法自動產生。

      1. 按一下&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Select campaigns & ad groups]**&#x200B;步驟中，指定要匯入的行銷活動和廣告群組，然後按一下&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Customize your import]**&#x200B;步驟中，選擇性地指定要匯入的專案型別、競標與預算設定，以及其他選項，然後按一下&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Set schedule]**&#x200B;步驟中，指定何時執行匯入工作以及如何接收通知。

1. 檢閱摘要中的選取專案，然後按一下&#x200B;**[!UICONTROL Start Import]**。

1. （選用）在[帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)或[廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)設定中新增搜尋、社交和Commerce追蹤。

## 編輯行銷活動匯入工作的排程設定

檢視[從 [!DNL Google Ads] 行銷活動](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}匯入的專案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 按一下「**[!UICONTROL Jobs]**」標籤。

1. 按一下匯入工作的名稱，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Set schedule]**&#x200B;步驟中，指定[排程設定](#campaign-import-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 檢視您的行銷活動匯入工作

您可以列出所有匯入工作，包括來源[!DNL Google Ads]帳戶、目標[!DNL Microsoft Advertising]帳戶、匯入時間或排程，以及建立工作的使用者。 當您多次執行匯入工作時（包括定期排程的匯入期間），每次發生的情況都會列為一個單獨的工作。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

   依預設，檢視會開啟至&#x200B;**[!UICONTROL Jobs]**&#x200B;標籤。

## 執行行銷活動匯入工作

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 按一下「**[!UICONTROL Jobs]**」標籤。

1. 選取匯入工作旁的核取方塊，然後按一下&#x200B;**[!UICONTROL Run Now]**。

## 檢視行銷活動匯入工作的記錄 {#campaign-import-log}

您可以列出所有已完成或失敗的匯入工作，包括開始時間、來源[!DNL Google Ads]帳戶、目標[!DNL Microsoft Advertising]帳戶、建立工作的使用者、成功和失敗的作業數目，以及接收每個工作之通知的任何電子郵件地址。 您可以檢視每個工作目標[!DNL Microsoft Advertising]帳戶變更的詳細資料，包括新增、同步、刪除的專案數，以及帳戶中每個實體層級（例如促銷活動或關鍵字）產生錯誤的專案數。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 按一下「**[!UICONTROL Logs]**」標籤。

1. （選擇性）若要檢視任何匯入工作的詳細資料，請按一下[!UICONTROL Summary]欄中的值。

## 行銷活動匯入工作設定 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Import Name]：**&#x200B;識別匯入工作的名稱。

**[!UICONTROL Source Google Ads account]：**&#x200B;從中匯出行銷活動資料的已同步[!DNL Google Ads]帳戶。

**[!UICONTROL Target Microsoft Ads account]：**&#x200B;已同步的[!DNL Microsoft Advertising]帳戶已匯入行銷活動資料。

**[!UICONTROL Credential ID]：** [!DNL Microsoft Advertising]用來代表您[!DNL Google Ads]認證的ID。 因為[!DNL Microsoft Advertising]限制，無法自動產生匯入的[!DNL Microsoft Advertising]認證。 請聯絡您的Adobe帳戶團隊，他們將會產生認證並提供ID。

### [!UICONTROL Select campaigns & ad groups]

**\[要匯入的資料\]：**&#x200B;要匯入的資料：

* *[!UICONTROL Import all new and existing campaigns]：*&#x200B;若要匯入[!DNL Microsoft Advertising]中已存在和不存在之所有行銷活動的資料。

* *[!UICONTROL Import specific campaigns and adgroups]：*&#x200B;若要選取特定行銷活動和廣告群組。

   * 若要將行銷活動展開至其子廣告群組，請按一下行銷活動名稱后面的&#x200B;**[!UICONTROL >]**。

   * 若要選取行銷活動或廣告群組，請選取專案以顯示核取記號。

   * 若要移除行銷活動或廣告群組，請取消選取專案或按一下[!UICONTROL Selected]欄中的刪除圖示。

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]：**&#x200B;可讓您指定要匯入的專案、競標和預算，以及其他選項。

**[!UICONTROL What to import]：**&#x200B;定義要匯入的專案。 預設會選取匯入料號類別的選項，並選取所有料號型別。 若要僅包含特定專案型別，請按一下&#x200B;**[!UICONTROL Show advanced options]**&#x200B;並變更要包含的專案型別。 您也可以選擇將UET標籤ID與任何先前未匯入[!DNL Microsoft Advertising]的再行銷清單或對象建立關聯。

**[!UICONTROL Bids and budgets]：**&#x200B;定義要匯入、更新和自訂的競標與預算設定，包括以指定百分比針對[!DNL Microsoft Advertising]增加或減少競標與預算的選項。

**[!UICONTROL Other options]：**&#x200B;定義如何處理匯入的登陸頁面URL、追蹤範本，以及其他行銷活動、廣告和目標選項，包括尋找和取代文字及插入尾碼的選項。

### [!UICONTROL Set schedule]

**[!UICONTROL When]：**&#x200B;何時匯入指定的行銷活動： *自動* （讓[!DNL Microsoft Advertising]設定排程以最佳方式最佳化您的行銷活動）、*[!UICONTROL Now]* （在您張貼工作設定時執行工作）、*[!UICONTROL Once]*&#x200B;在指定時間、*[!UICONTROL Daily]*&#x200B;在指定時間、*[!UICONTROL Weekly]*&#x200B;在指定時間，或是&#x200B;*[!UICONTROL Monthly]*&#x200B;在指定時間。

**[!UICONTROL Receive email notifications]：**&#x200B;是否及何時將匯入工作的相關電子郵件通知傳送至[!UICONTROL Send reports to]欄位中的地址： *[!UICONTROL No emails]*、*[!UICONTROL Only if there are changes or errors]* （預設值）、*[!UICONTROL Only if there are errors]*&#x200B;或&#x200B;*[!UICONTROL Every time this import runs]*。

**[!UICONTROL Send reports to]：**&#x200B;接收匯入工作相關通知的電子郵件地址。 以逗號(`,`)分隔多個位址。

>[!MORELIKETHIS]
>
>* [管理廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
