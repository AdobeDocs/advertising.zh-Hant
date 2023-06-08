---
title: 管理 [!DNL Google Ads] 位置
description: 瞭解如何建立和管理可出價刊登版位 [!DNL Google Ads] 廣告群組。
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 位置

*[!DNL Google Ads]僅限帳戶*

您可以在中建立和編輯廣告群組的版位 [支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md) 以內的顯示網路為目標 [已同步的廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## 建立 [!DNL Google Ads] 位置

>[!TIP]
>
>若要一次建立多個版位，請使用 [行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路、帳戶、行銷活動和廣告群組，然後按一下 **[!UICONTROL Continue]**.

1. 設定 [位置設定](#placement-settings).

1. 按一下 **[!UICONTROL Post]**.

## 編輯 [!DNL Google Ads] 位置

>[!TIP]
>
>若要一次編輯多個版位，請使用 [行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. 選取要編輯的每一列旁的核取方塊。

   如需選取多個列的秘訣，請參閱「[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯") .

1. 編輯 [位置設定](#placement-settings).

   若為多個版位，您的變更會套用至所有選取的版位。 對於某些英數字元欄位，您可以將現有值變更為指定值、將現有字串取代為指定字串、將指定首碼新增至每個值的開頭，或在每個值的結尾附加尾碼。 對於某些貨幣欄位，您可以將現有值變更為指定值，或透過指定百分比或貨幣金額來增加或減少金額，並設定限制。

1. 儲存資料：

   * （單一位置）按一下 **[!UICONTROL Post]**.

   * （多個位置）按一下 **[!UICONTROL Post Now]**.

## 位置設定 {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]：** 內容網路上可顯示您廣告的網站。 輸入有效的URL，例如www.example.com、example.com或www.example.com/shoes/kids。 若要指定多個字串，請以逗號分隔字串，或在個別行中輸入字串。 URL不能包含問號(`?`)。 **注意：** 您可以 [排除網站位置](placement-negative-create.md) 從 [!UICONTROL Placements] > [!UICONTROL Negatives] 在廣告群組和行銷活動設定中檢視和。

**[!UICONTROL Status]：** 位置的顯示狀態： *作用中* （啟用競標；預設）， *已暫停* （停用競標），或 *已刪除* （刪除版位；僅限現有版位）。

### [!UICONTROL Bids]

**[!UICONTROL Bid]：** （選用）投放型廣告的最大每次點按成本(CPC)或每千次可檢視曝光成本(vCPM)，視促銷活動競標策略而定。 此值會覆寫廣告群組層級競標。

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
>* [建立負面版位](placement-negative-create.md)
>* [變更刊登版位和負面刊登版位的狀態](placement-status-edit.md)
