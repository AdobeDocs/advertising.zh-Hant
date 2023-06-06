---
title: 管理 [!DNL Microsoft Advertising] 動態再行銷對象
description: 瞭解如何建立和管理 [!DNL Microsoft Advertising] 動態再行銷對象。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# 管理 [!DNL Microsoft Advertising] 動態再行銷對象

*[!DNL Microsoft Advertising]僅限帳戶*

您可以建立 [!DNL Microsoft Advertising] 當您在網頁上使用搜尋引擎的JavaScript轉換和對象追蹤標籤時，動態再行銷對象。 每個對象都是使用包含在其使用者將構成對象的網頁中的指定標籤建立的。 您可以使用相同的追蹤標籤來建立多個對象。 您也可以變更現有對象的名稱和資料來源，或刪除現有對象。

動態再行銷對象具有對象型別»[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot; （例如「動態再行銷過往買家」）。

如需有關動態再行銷以及如何實作必要的JavaScript標籤的詳細資訊，請參閱 [[!DNL Microsoft Advertising] 有關動態再行銷的檔案](https://help.ads.microsoft.com/#apex/ads/en/56910).

## 建立動態的再行銷對象

>[!NOTE]
>
>對象 [!DNL Microsoft Advertising] 帳戶，JavaScript標籤必須包含 [產品ID和頁面型別引數](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. 識別 [!DNL Microsoft Advertising] 通用事件追蹤(UET)標籤，包含在將從中建立對象的網頁中。

   在稍後的步驟中，您將需要標籤名稱。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路和帳戶名稱，然後按一下 **[!UICONTROL Continue]**.

1. 指定對象資訊：

   1. 在 **[!UICONTROL Data Source]** 功能表，選取 **[!UICONTROL Dynamic Remarketing List]**.

   1. 輸入 **[!UICONTROL Audience Name]**.

   1. 從搜尋引擎帳戶的所有可用標籤清單中，選取 [!DNL Microsoft Advertising] 包含在其使用者將構成受眾的網頁中的UET標籤。

   1. 根據相關網頁上的訪客動作，選取對象的訪客型別： *[!UICONTROL General Visitors]*， *[!UICONTROL Product Searchers]*， *[!UICONTROL Product Viewers]*， *[!UICONTROL Past Buyers]*，或 *[!UICONTROL Shopping Cart Abandoners]*.

   1. 指定數量 **[!UICONTROL Membership Days]**，即使用者的Cookie在對象中停留的天數。 值的範圍可以從一(1)到180。

      使用您預期廣告與使用者相關的時間長度。

1. 按一下 **[!UICONTROL Post]**.

>[!NOTE]
>
>您的 [!DNL Microsoft Advertising] 一旦動態再行銷清單包含至少300名使用者，即符合鎖定目標的資格。

## 編輯動態再行銷對象

您可以變更的名稱和資料來源 [!DNL Microsoft Advertising] 動態再行銷對象。 您無法編輯的值 [!UICONTROL Membership Days] 設定。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 選取要編輯的對象旁的核取方塊。

1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

1. 編輯對象資訊：

   1. 在 **[!UICONTROL Data Source]** 區段，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

   1. （可選）變更 **[!UICONTROL Audience Name]**.

   1. （可選）從廣告網路帳戶的所有可用標籤清單中，變更 [!DNL Microsoft Advertising] 包含在其使用者將構成受眾的網頁中的UET標籤。

   1. （選用）根據相關網頁上的訪客動作，變更對象的訪客型別： *[!UICONTROL General Visitors]*， *[!UICONTROL Product Searchers]*， *[!UICONTROL Product Viewers]*， *[!UICONTROL Past Buyers]*，或 *[!UICONTROL Shopping Cart Abandoners]*.

   1. 按一下 **[!UICONTROL Post]**.

## 刪除動態再行銷對象

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. （選用）篩選清單以包含特定對象。

1. 選取要刪除的每個對象旁的核取方塊。

   如需選取多個列的秘訣，請參閱「[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

1. 在確認訊息中，按一下 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [建立 [!DNL Google Ads] 客戶比對對象來自 [!DNL Adobe] 對象](google-audience-from-adobe-audience.md)
>* [建立 [!DNL Google Ads] 來自Adobe Campaign電子郵件清單的客戶比對對象](google-audience-from-campaign-email-list.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)

