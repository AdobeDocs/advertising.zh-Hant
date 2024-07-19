---
title: 管理 [!DNL Microsoft Advertising] 動態再行銷對象
description: 瞭解如何建立和管理 [!DNL Microsoft Advertising] 動態再行銷對象。
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# 管理[!DNL Microsoft Advertising]動態再行銷對象

僅&#x200B;*[!DNL Microsoft Advertising]個帳戶*

當您在網頁上使用搜尋引擎的JavaScript轉換和對象追蹤標籤時，可以建立[!DNL Microsoft Advertising]動態再行銷對象。 每個受眾都是使用包含在其使用者組成受眾之網頁中的指定標籤所建立。 您可以使用相同的追蹤標籤建立多個對象。 您也可以變更現有對象的名稱和資料來源，或刪除現有對象。

動態再行銷對象具有對象型別「[!UICONTROL Dynamic Remarketing] \&lt;訪客型別\>」（例如「動態再行銷過往買家」）。

如需有關動態再行銷以及如何實作必要的JavaScript標籤的詳細資訊，請參閱有關動態再行銷](https://help.ads.microsoft.com/#apex/ads/en/56910)的[[!DNL Microsoft Advertising] 檔案。

## 建立動態的再行銷對象

>[!NOTE]
>
>對於[!DNL Microsoft Advertising]帳戶，JavaScript標籤必須包含[產品ID和頁面型別引數](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85)。

1. 識別將要建立對象之網頁中所包含的[!DNL Microsoft Advertising]通用事件追蹤(UET)標簽名稱。

   您將在後續步驟中需要標籤名稱。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 選取廣告網路和帳戶名稱，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 指定對象資訊：

   1. 在&#x200B;**[!UICONTROL Data Source]**&#x200B;功能表中，選取&#x200B;**[!UICONTROL Dynamic Remarketing List]**。

   1. 輸入&#x200B;**[!UICONTROL Audience Name]**。

   1. 從搜尋引擎帳戶的所有可用標籤清單中，選取包含在其使用者組成對象之網頁中的[!DNL Microsoft Advertising] UET標簽名稱。

   1. 選取對象的訪客型別，其根據為相關網頁上的訪客動作： *[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]*&#x200B;或&#x200B;*[!UICONTROL Shopping Cart Abandoners]*。

   1. 指定&#x200B;**[!UICONTROL Membership Days]**&#x200B;的數量，這是使用者的Cookie在對象中保留的天數。 值的範圍可以從一(1)到180。

      使用您預期廣告與使用者相關的時間長度。

1. 按一下&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>您的[!DNL Microsoft Advertising]動態再行銷清單一旦包含至少300名使用者，即符合鎖定目標的資格。

## 編輯動態再行銷對象

您可以變更[!DNL Microsoft Advertising]動態再行銷對象的名稱和資料來源。 您無法編輯[!UICONTROL Membership Days]設定的值。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 選取要編輯的對象旁的核取方塊。

1. 在資料表上方的工具列中，按一下![編輯](/help/search-social-commerce/assets/edit.png "編輯")。

1. 編輯對象資訊：

   1. 在&#x200B;**[!UICONTROL Data Source]**&#x200B;區段中，按一下![編輯](/help/search-social-commerce/assets/edit.png "編輯")。

   1. （選用）變更&#x200B;**[!UICONTROL Audience Name]**。

   1. （選擇性）從廣告網路帳戶的所有可用標籤清單中，變更包含在其使用者組成對象之網頁中的[!DNL Microsoft Advertising] UET標簽名稱。

   1. （選擇性）變更對象的訪客型別，其基礎為相關網頁上的訪客動作： *[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]*&#x200B;或&#x200B;*[!UICONTROL Shopping Cart Abandoners]*。

   1. 按一下&#x200B;**[!UICONTROL Post]**。

## 刪除動態再行銷對象

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. （選用）篩選清單以包含特定對象。

1. 選取要刪除的每個對象旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [建立 [!DNL Google Ads] 來自 [!DNL Adobe] 受眾的客戶比對受眾](google-audience-from-adobe-audience.md)
>* [從Adobe Campaign電子郵件清單建立 [!DNL Google Ads] 客戶比對對象](google-audience-from-campaign-email-list.md)
>* [使用客戶資料清單管理客戶比對對象](audience-from-customer-data-list.md)
