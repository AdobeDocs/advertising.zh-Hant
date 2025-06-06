---
title: 將目標節點新增到體驗中的最終層級
description: 瞭解如何將目標節點新增至廣告體驗的最終目標層級。
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: 05bcaa63779856cfea2f9cd3a0ab5d5e9d3d472a
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# 將目標節點新增到體驗中的最終層級

*僅使用決策樹定位的體驗*
*已關閉的Beta版*

將目標節點新增至體驗的最底層節點時（無論是根「全部」節點、目標特定節點還是「其他一切」節點），您可以直接定義目標，而不需要建立同層級節點。 新增底層的節點會在相同層級建立目標節點和其他「其他一切」節點。

>[!NOTE]
>
>若要在決策樹的現有層級之間插入目標節點，請參閱[在體驗中的節點之間插入目標節點](experience-target-node-add-inner.md)。

<!-- 1. [ways to get to the decision tree] -->

1. 在您要插入目標的節點底下，按一下[新增]。![](/help/creative/assets/add.png "")，然後選取&#x200B;**[!UICONTROL Insert New Target]**。

1. 指定目標：

   * 針對Adobe對象目標，請選取「**[!UICONTROL Adobe Audience]**」，然後執行下列動作：

      1. 按一下&#x200B;**[!UICONTROL Click to Browse]**&#x200B;以開啟您的[!UICONTROL Audience Targeting]選項、開啟&#x200B;**[!UICONTROL Adobe Segments]**&#x200B;標籤、指定一或多個廣告商的[!DNL Adobe]對象目標，然後按一下&#x200B;**[!UICONTROL Create]**。

      1. （選擇性）若要在指定多個對象時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能會為每個指定對象建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的對象（[!DNL Boolean] `AND`陳述式）。

      1. 按一下&#x200B;**[!UICONTROL Apply]**。

   * 若為地理目標，請選取單一地理類別（例如[!UICONTROL Geo: Country]），然後執行下列動作：

      1. 按一下&#x200B;**[!UICONTROL Click to Browse]**&#x200B;開啟您的[!UICONTROL Geo Targeting]選項，指定一或多個地理目標，然後按一下&#x200B;**[!UICONTROL Save]**。

         郵遞區號目標具有大量編輯選項。 若要貼上多個郵遞區號，請按一下「**[!UICONTROL Paste postal codes]**」標籤、選取國家、貼上或輸入郵遞區號（以逗號分隔或分行），然後按一下「**[!UICONTROL Include All]**」。 若要移除包含的郵遞區號目標，請將游標停留在目標上，然後按一下![移除](/help/creative/assets/delete.png "移除") **[!UICONTROL Remove]**。

      1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能會為每個指定的地理目標建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的位置（[!DNL Boolean] `AND`陳述式）。

      1. 按一下&#x200B;**[!UICONTROL Apply]**。

   * 針對資料傳遞目標，選取&#x200B;**[!UICONTROL Data Pass]**，並選擇性地自訂資料傳遞金鑰，輸入單一資料傳遞值，然後按一下&#x200B;**[!UICONTROL Apply]**。

   已在[體驗設定](experience-settings-targeting.md)的[!UICONTROL Advanced]區段的&#x200B;**[!UICONTROL Data Pass]**&#x200B;欄位中設定機碼值組的機碼預設值。 您可以選擇自訂金鑰。

   * 對於重新定位畫素目標，請選取&#x200B;**[!UICONTROL RT Pixel]**，選取要使用的單一重新定位畫素，以及顯示創意所需的任何畫素屬性值，然後按一下&#x200B;**[!UICONTROL Apply]**。

     重新目標畫素的屬性是在[重新目標畫素設定](/help/creative/pixels/retargeting-pixel-manage.md)中設定。

   * 針對裝置目標，請執行下列動作：

      1. 選取單一目標類別（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;或&#x200B;**[!UICONTROL Device: Browser]**），然後選取目標。

      1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能會為每個指定的地理目標建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的位置（[!DNL Boolean] `AND`陳述式）。

      1. 按一下&#x200B;**[!UICONTROL Apply]**。

1. 執行下列任一項作業：

   * （選擇性） [將創意內容](experience-assign-creative-bundles.md)指派給新的目標節點和「其他一切」節點。

   * （選用）若要儲存體驗：

      1. 按一下&#x200B;**[!UICONTROL Save]**，然後再按&#x200B;**[!UICONTROL OK]**。

      1. （如果最底層的每個節點不包含至少一個創意內容）：執行下列任一項作業：

         * 若要儲存不含所有必要創意套裝的體驗，請按一下&#x200B;**[!UICONTROL Save as Draft]**。

           您無法為草稿體驗建立廣告標籤。

         * 若要將預設創意內容指派給尚未指派創意套裝的每個目標，請按一下「**[!UICONTROL Assign Default Creatives]**」。 檢閱已指派預設創意的更新樹狀結構後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

         * 若要繼續編輯決策樹，請按一下&#x200B;**[!UICONTROL Continue Edit]**。

>[!MORELIKETHIS]
>
>* [在節點之間插入目標節點](experience-target-node-add-inner.md)
>* [在節點之間新增同層級目標節點](experience-target-node-add-sibling.md)
>* [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)
>* [將創意內容指派給最終節點](experience-assign-creative-bundles.md)
>* [刪除目標節點或創意分葉節點](/help/creative/experiences/experience-target-node-delete.md)
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [目標體驗設定](experience-settings-targeting.md)
