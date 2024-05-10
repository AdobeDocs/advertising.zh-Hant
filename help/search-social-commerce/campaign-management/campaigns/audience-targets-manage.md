---
title: 管理行銷活動和廣告群組的對象目標
description: 瞭解如何設定和管理您的對象目標 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 行銷活動和廣告群組。
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 0a858fb9437439d2755f1a9679b0849c614293b7
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# 管理您的對象目標 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 行銷活動和廣告群組

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 僅限*

[!DNL Google Ads] 行銷活動和廣告群組，以及 [!DNL Microsoft® Advertising] 廣告群組，可以鎖定來自相同廣告網路的特定對象。 廣告網路會決定要鎖定目標對象的大小。

>[!NOTE]
>
>排除專案一律會覆寫包含專案/目標。

您可以設定對象目標、編輯對象目標的競標修飾詞以及變更對象目標的狀態。

## 設定對象目標

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路和帳戶名稱，然後按一下 **[!UICONTROL Continue]**.

1. 設定特定行銷活動和廣告群組的對象目標：

   1. 選取指定廣告網路的適用對象。

      您可以選擇搜尋包含至少三個字元之特定文字字串的對象。 如需任何相符的受眾，請按一下 **[!UICONTROL Include]** 以選取它。

      [!DNL Google Ads] 客戶比對對象僅適用於搜尋和購物行銷活動。

   1. 指定目標：

      1. （選用）若要展開促銷活動及其子廣告群組，請按一下促銷活動名稱。

      1. （選用）若要依據名稱中包含的文字字串來篩選行銷活動清單或廣告群組清單，請按一下 ![篩選](/help/search-social-commerce/assets/filter.png "篩選") ，在輸入欄位中輸入或貼上文字字串，然後按下 **[!UICONTROL Enter]** 機碼。

      1. 按一下旁邊的空白圓圈，使用藍色核取記號(![選取](/help/search-social-commerce/assets/include.png "選取"))顯示。

      您無法同時設定上層行銷活動和下層廣告群組（會自動使用目標）的目標。

1. 按一下 **[!UICONTROL Post]**.

1. （選擇性）從以下任一種方式設定目標的競標調整： [!UICONTROL Targets] 檢視：

   * 按一下 **[!UICONTROL Bid Adjustment]** 欄並輸入值。

   * 選取目標列旁的核取方塊。 在工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯")，輸入競標修飾詞，然後按一下 **[!UICONTROL Post]**.

   值可包括：

   * *0%：* 不調整此對象廣告的競標。

   * /[*從–90%到900%的其他值*/]：增加或減少此對象廣告的競標。 例如，如果關鍵字層級的競標是1美元，而特定對象目標的競標調整是50%，則該對象的競標會增加到1.50美元。

## 編輯對象目標的競標修飾詞

您可以變更所有對象型別（市場內對象除外）的競標修飾詞和對象目標狀態。

>[!NOTE]
>
>當父級行銷活動使用CPC競標策略，並且在設定為自動最佳化對象目標競標調整值的產品組合中，搜尋、Social和Commerce會自動最佳化競標修飾元。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. 執行下列任一項作業：

   * 若要編輯一個目標的競標修飾詞，請按一下 **[!UICONTROL Bid Adjustment]** 欄並編輯競標調整。

   * 若要編輯其他目標的競標修飾詞，請執行下列步驟：

      1. 選取每個要編輯的目標旁的核取方塊。

         如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

      1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

      1. 編輯 **[!UICONTROL Bid Modifier]** 和/或 **[!UICONTROL Status]** 欄位。

         對於 [!UICONTROL Bid Modifier] 欄位，您可以選擇將現有值變更為指定值，或透過指定百分比或貨幣金額來增加或減少金額，並設定限制。

         對於設定值，值可以包括：

         * *0%：* 不調整此對象廣告的競標。

         * /[*從–90%到900%的其他值*/]：增加或減少此對象廣告的競標。 例如，如果關鍵字層級的競標是1美元，而特定對象目標的競標調整是50%，則該對象的競標會增加到1.50美元。

         若為多個目標，您的變更會套用至所有選取的目標。

      1. （選用）按一下 **[!UICONTROL Additional Details]** 並選擇性地輸入專案名稱與摘要。

      1. 按一下 **[!UICONTROL Post]**.

## 變更對象目標的狀態

您可以暫停作用中的對象目標，以停用其上的競標。 您稍後可以透過將狀態變回作用中來繼續競標。

您也可以刪除作用中或暫停的搜尋對象目標。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. （選用）篩選清單以包含特定對象目標。

1. 選取每個您想要變更其狀態之對象目標旁的核取方塊。

   如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

1. 在工具列中按一下狀態按鈕：

   * 若要啟動列，請按一下 ![啟動](/help/search-social-commerce/assets/activate.png "啟動").

   * 若要暫停列，請按一下 ![暫停](/help/search-social-commerce/assets/pause.png "暫停").

   * 若要刪除列，請按一下 ![更多動作](/help/search-social-commerce/assets/more.png "更多動作") 並選取 **[!UICONTROL Delete]**. 在確認訊息中，按一下 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [關於對象](audience-about.md)
>* [管理行銷活動和廣告群組的對象排除](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
