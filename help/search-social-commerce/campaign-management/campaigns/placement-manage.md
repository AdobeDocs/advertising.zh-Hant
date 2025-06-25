---
title: 管理 [!DNL Google Ads] 位置
description: 瞭解如何建立和管理 [!DNL Google Ads] 廣告群組的可出價刊登版位。
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 管理[!DNL Google Ads]個版位

僅&#x200B;*[!DNL Google Ads]個帳戶*

您可以在[支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)中，針對[已同步化的廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)中的顯示網路來建立和編輯廣告群組的版位

## 建立[!DNL Google Ads]個版位

>[!TIP]
>
>若要同時建立多個版位，請使用[行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**。

1. &#x200B;
   1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 選取廣告網路、帳戶、行銷活動和廣告群組，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 設定[位置設定](#placement-settings)。

1. 按一下&#x200B;**[!UICONTROL Post]**。

## 編輯[!DNL Google Ads]版位

>[!TIP]
>
>若要一次編輯多個位置，請使用[行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**。

1. 選取要編輯之每一列旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在資料表上方的工具列中，按一下![編輯](/help/search-social-commerce/assets/edit.png "編輯")。

1. 編輯[位置設定](#placement-settings)。

   若為多個版位，您的變更會套用至所有選取的版位。 對於某些英數字元欄位，您可以將現有值變更為指定值、以指定字串取代現有字串、在每個值的開頭加上指定首碼，或在每個值的結尾附加尾碼。 對於某些貨幣欄位，您可以將現有值變更為指定值，或透過指定百分比或貨幣金額來增加或減少金額，但需有限制。

1. 儲存資料：

   * （單一位置）按一下&#x200B;**[!UICONTROL Post]**。

   * （多個位置）按一下&#x200B;**[!UICONTROL Post Now]**。

## 位置設定 {#placement-settings}

### [!UICONTROL Placement Details]

您的廣告可以出現在內容網路上的&#x200B;**[!UICONTROL Placements]：**&#x200B;網站。 輸入有效的URL，例如www.example.com、example.com或www.example.com/shoes/kids。 若要指定多個字串，請以逗號分隔字串，或在個別行中輸入字串。 URL不能包含問號(`?`)。 **注意：**&#x200B;您可以[從[!UICONTROL Placements] > [!UICONTROL Negatives]檢視，以及廣告群組和行銷活動設定中，排除網站位置](placement-negative-create.md)。

**[!UICONTROL Status]：**&#x200B;位置的顯示狀態： *啟用* （啟用競標；預設值）、*已暫停* （停用競標）或&#x200B;*已刪除* （刪除位置；僅現有位置）。

### [!UICONTROL Bids]

**[!UICONTROL Bid]：** （選用）根據行銷活動競標策略，針對位置型廣告的最高每次點按成本(CPC)或每千次可檢視曝光成本(vCPM)。 此值會覆寫廣告群組層級競標。

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [關於位置](placement-about.md)
>* [建立負面的版位](placement-negative-create.md)
>* [變更刊登版位和負面刊登版位的狀態](placement-status-edit.md)
