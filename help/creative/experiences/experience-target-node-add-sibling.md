---
title: 在體驗中的節點之間新增同層級目標節點
description: 瞭解如何將同層級節點新增至具有目標或與具有目標之節點位於相同層級的任何節點。
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# 在體驗中的節點之間新增同層級目標節點

*僅使用決策樹定位的體驗*
*已關閉的Beta版*

您可以將同層級節點新增至任何具有目標的節點，或與具有目標的節點位於相同層級的節點。

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. 在您要新增同層級節點的節點上方，按一下[新增]。![](/help/creative/assets/add.png "")，然後選取&#x200B;**[!UICONTROL Insert Sibling Target]**。

1. 指定目標：

   * 針對「Adobe對象」目標，請執行以下作業：

      1. 按一下&#x200B;**[!UICONTROL Click to Browse]**&#x200B;以開啟您的[!UICONTROL Audience Targeting]選項、開啟&#x200B;**[!UICONTROL Adobe Segments]**&#x200B;標籤、指定一或多個廣告商的[!DNL Adobe]對象目標，然後按一下&#x200B;**[!UICONTROL Save]**。

      1. （選擇性）若要在指定多個對象時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能會為每個指定對象建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的對象。

      1. 按一下&#x200B;**[!UICONTROL Apply]**。

   * 針對地理目標，請執行下列動作：

      1. 按一下&#x200B;**[!UICONTROL Click to Browse]**&#x200B;開啟您的[!UICONTROL Geo Targeting]選項，指定一或多個地理目標，然後按一下&#x200B;**[!UICONTROL Save]**。

         郵遞區號目標具有大量編輯選項。 若要貼上多個郵遞區號，請按一下「**[!UICONTROL Paste postal codes]**」標籤、選取國家、貼上或輸入郵遞區號（以逗號分隔或分行），然後按一下「**[!UICONTROL Include All]**」。 若要移除包含的郵遞區號目標，請將游標停留在目標上，然後按一下![移除](/help/creative/assets/delete.png "移除") **[!UICONTROL Remove]**。

      1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能會為每個指定的地理目標建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的位置。

      1. 按一下&#x200B;**[!UICONTROL Apply]**。

   * 針對資料傳遞目標，請輸入單一資料傳遞值，然後按一下&#x200B;**[!UICONTROL Apply]**。

   機碼值組的機碼已在[體驗設定](experience-settings-targeting.md)的[!UICONTROL Advanced]區段的&#x200B;**[!UICONTROL Data Pass]**&#x200B;欄位中設定，您無法新增其他機碼。

   * 如果要重新定位畫素目標，請選取要使用的重新定位畫素，以及顯示創意所必須呈現之任何畫素屬性的必要值。 然後按一下&#x200B;**[!UICONTROL Apply]**。

     重新目標畫素的屬性是在[重新目標畫素設定](/help/creative/pixels/retargeting-pixel-manage.md)中設定。

   * 針對裝置目標，請執行下列動作：

      1. 選取目標。

      1. （選擇性）若要在指定多個地理目標時建立多個目標節點，請選取&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能會為每個指定的地理目標建立個別的目標節點（具有個別的創意組合）。 如果您不分割目標，則使用者必須屬於所有指定的位置。

      1. 按一下&#x200B;**[!UICONTROL Apply]**。

1. 執行下列任一項作業：

   * （選擇性） [將創意內容](experience-assign-creative-bundles.md)指派給新的目標節點。

   * （選用）若要儲存體驗：

      1. 按一下&#x200B;**[!UICONTROL Save]**，然後再按&#x200B;**[!UICONTROL OK]**。

      1. （如果最底層的每個節點不包含至少一個創意內容）：執行下列任一項作業：

         * 若要儲存不含所有必要創意套裝的體驗，請按一下&#x200B;**[!UICONTROL Save as Draft]**。

           您無法為草稿體驗建立廣告標籤。

         * 若要將預設創意內容指派給尚未指派創意套裝的每個目標，請按一下「**[!UICONTROL Assign Default Creatives]**」。 檢閱已指派預設創意的更新樹狀結構後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

         * 若要繼續編輯決策樹，請按一下&#x200B;**[!UICONTROL Continue Edit]**。

>[!MORELIKETHIS]
>
>* [新增目標節點至最終層級](experience-target-node-add-final.md)
>* [在節點之間插入目標節點](experience-target-node-add-inner.md)
>* [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)
>* [將創意內容指派給最終節點](experience-assign-creative-bundles.md)
>* [刪除目標節點或創意分葉節點](/help/creative/experiences/experience-target-node-delete.md)
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [目標體驗設定](experience-settings-targeting.md)
