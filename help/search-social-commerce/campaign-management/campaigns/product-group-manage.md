---
title: 管理購物產品群組
description: 瞭解如何在購物行銷活動中建立和管理購物產品群組。
exl-id: 25912abd-1ddb-443f-a16d-7efe57093677
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# 管理購物產品群組

*[!DNL Google Ads]和 [!DNL Microsoft Advertising] 僅限購物行銷活動*

您可以建立和編輯產品群組，並刪除產品群組及其子產品群組，位於 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 檢視。

## 建立&quot;[!UICONTROL All Products]&quot;產品群組

您必須先建立全包含式產品群組（稱為「 」），才能建立具有特定屬性的產品群組[!UICONTROL All Products].」 每個廣告群組只能有一個&quot;[!UICONTROL All Products]「群組。

>[!TIP]
>
>若要同時建立多個帳戶元件，請使用 [行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路、帳戶、行銷活動和廣告群組，然後按一下 **[!UICONTROL Continue]**.

1. 指定 [[!DNL Google Ads] 產品群組設定](product-group-settings-google.md) 或 [[!DNL Microsoft Advertising] 產品群組設定](product-group-settings-microsoft.md).

1. 按一下 **[!UICONTROL Post]**.

## 在現有產品群組中建立子產品群組節點

建立至少包含所有內容的「[!UICONTROL All Products]「群組」若為廣告群組，您可以為要納入競標或排除競標的產品子集建立子產品群組節點，而一或多個產品群組會在每個層級鎖定相同的屬性(例如， [!UICONTROL Brand]=Acme代表一個產品群組和 [!UICONTROL Brand]=AcmePlus供相同層級的其他使用。 您可以建立最多七個層級的子產品群組節點，不包括「[!UICONTROL All Products]「。

>[!NOTE]
>
>您無法為「」建立子產品群組[!UICONTROL Everything Else]「產品群組。

>[!TIP]
>
>若要同時建立多個帳戶元件，請使用 [行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. （選擇性）若要在樹狀檢視中檢視產品群組及其子產品群組節點，請將游標停留在產品群組名稱上，按一下 ![功能表圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表圖示")，然後選取 **[!UICONTROL Tree View]**.

1. 將游標停留在產品群組名稱上，按一下 ![向下箭頭功能表](/help/search-social-commerce/assets/arrow-dropdown-menu.png "向下箭頭功能表")，然後選取 **[!UICONTROL + Add Node]**.

1. 指定 [[!DNL Google Ads] 產品群組設定](product-group-settings-google.md) 或 [[!DNL Microsoft Advertising] 產品群組設定](product-group-settings-microsoft.md)，包括產品維度和屬性。

1. 按一下 **[!UICONTROL Post]**.

## 編輯產品群組節點設定

您可以編輯廣告群組中包含之單位產品群組節點（沒有子產品群組節點的產品群組）的競標與追蹤範本。 您無法編輯已排除的單位產品群組或已包含或已排除的細分節點的任何資訊，這些節點是具有子項產品群組節點的產品群組。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. （選擇性）若要在樹狀檢視中檢視產品群組及其子產品群組節點，請將游標停留在產品群組名稱上，按一下 ![功能表圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表圖示")，然後選取 **[!UICONTROL Tree View]**.

1. 執行下列任一項作業：

   1. （若要編輯單一產品群組節點的設定）將游標停留在產品群組名稱上，請按一下 ![功能表圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表圖示")，然後選取 **[!UICONTROL + Edit Node]**.

   1. （若要編輯一或多個廣告群組的設定），請執行下列動作：

      1. 選取每個節點旁的核取方塊。

         如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

      1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

1. 編輯 [[!DNL Google Ads] 產品群組設定](product-group-settings-google.md) 或 [[!DNL Microsoft Advertising] 產品群組設定](product-group-settings-microsoft.md).

   若為多個節點，您的變更會套用至所有選取的節點。 對於 [!UICONTROL Bid] 欄位，您可以選擇將現有值變更為指定值，或透過指定百分比或貨幣金額來增加或減少金額，並設定限制。 對於 [!UICONTROL Tracking Template] 欄位，您可以將現有值變更為指定值、將現有字串取代為指定字串、將指定首碼新增至每個值的開頭或附加尾碼至每個值的結尾。

1. （選用）按一下 **[!UICONTROL Additional Details]** 並選擇性地輸入專案名稱與摘要。

1. 按一下 **[!UICONTROL Post]**.

## 刪除產品群組節點

您可以刪除任何產品群組（當其他產品群組位於相同層級時，則除了「其他所有專案」群組），這些產品群組用於決定您的商家中心帳戶中的哪些產品包含在廣告群組的購物廣告中。 刪除產品群組將會刪除所有子產品群組。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. （選用）篩選清單以包含特定產品群組。

1. 執行下列任一項作業：

   * 若要刪除產品群組，請按一下 **[!UICONTROL Status]** 欄並選取 **[!UICONTROL Delete]**.

   * 若要刪除一或多個產品群組，請執行下列動作：

      1. 選取要刪除的每個產品群組旁的核取方塊。

         如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

      1. 在工具列中，按一下 ![更多](/help/search-social-commerce/assets/more.png "更多") 並選取 **[!UICONTROL Delete]**.

      1. 在確認訊息中，按一下 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [關於購物產品群組](product-group-about.md)
>* [[!DNL Google Ads] 產品群組設定](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] 產品群組設定](product-group-settings-microsoft.md)
