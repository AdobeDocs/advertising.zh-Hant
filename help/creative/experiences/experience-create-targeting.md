---
title: 建立決策樹定位的體驗
description: 瞭解如何使用決策樹建立目標式廣告體驗。
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 39e2d6afa357f2cbe4037371a1441ddc2ffa9ef2
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 建立決策樹定位的體驗

*已關閉的Beta*

使用決策樹建立目標式廣告體驗。 每個體驗都會使用來自單一創意資料庫的廣告。

>[!NOTE]
>
> 建立目標體驗後，您之後將無法變更為使用不同工作流程的非目標體驗。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 按一下&#x200B;**[!UICONTROL Create New Experience]**。

1. 輸入[一般體驗設定](experience-settings-targeting.md)。

1. 按一下&#x200B;**[!UICONTROL Create]**。

1. 在決策樹中，執行下列動作：

   1. （選擇性）變更決策樹的檢視設定。

      您的設定會儲存到您登出為止。

      * 移動滑桿來放大或縮小。

      * 按一下![以垂直樹狀結構檢視](/help/creative/assets/tree-vertical.png "以垂直樹狀結構檢視")或![以水準樹狀檢視](/help/creative/assets/tree-horizontal.png "以水準樹狀檢視")，在檢視垂直清單和水準清單之間切換。

   1. （可選）以下列任何方式設定廣告目標和對應的創意內容：

      * 目標：

         * [將目標節點新增到體驗中的最終層級](experience-target-node-add-final.md)。

         * [在節點之間插入目標節點](experience-target-node-add-inner.md)。

         * [在節點](experience-target-node-add-sibling.md)之間新增同層級目標節點。

         * [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)。

      * Creative套件組合：

         * [指派和取消指派創意內容給最終節點](experience-assign-creative-bundles.md)。

           如果您未將至少一個束指派給每個最終節點，則可在儲存體驗時，選擇對每個未指派的節點使用預設的創意。 若要發佈體驗，您必須指派組合或針對每個最終節點使用預設創意。

         * [自訂指派組合中創意的追蹤URL](experience-tracking-urls-targeting.md)。

         * [針對指派的組合自訂創意最佳化與排程](experience-optimization-scheduling-targeting.md)。

1. （可選）在決策樹和一般設定之間切換：

   * 若要從決策樹開啟一般設定，請按一下右上角的&#x200B;**[!UICONTROL Experience Form]**。

   * 若要從一般設定開啟決策樹，請按一下右上角的&#x200B;**[!UICONTROL Decision Tree]**。

1. 按一下&#x200B;**[!UICONTROL Save]**，然後執行下列動作。

   * （如果最底層的每個節點至少包含一個創意組合）按一下&#x200B;**[!UICONTROL OK]**。

   * （如果最底層的每個節點不包含至少一個創意搭售方案），請執行下列任一項作業：

      * 若要儲存不含所有必要創意套裝的體驗，請按一下&#x200B;**[!UICONTROL Save as Draft]**。

        您無法為[草稿](experience-about.md#experience-statuses)體驗建立廣告標籤。

      * 若要將預設創意內容指派給尚未指派創意套裝的每個目標，請按一下「**[!UICONTROL Assign Default Creatives]**」。 檢閱已指派預設創意的更新樹狀結構後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

      * 若要繼續編輯決策樹，請按一下&#x200B;**[!UICONTROL Continue Edit]**。

當體驗上線時，[!DNL Creative]會自動為每個適用的創意大小建立廣告標籤。

>[!MORELIKETHIS]
>
>* [目標體驗設定](experience-settings-targeting.md)
>* [新增目標節點至最終層級](experience-target-node-add-final.md)
>* [在節點之間插入目標節點](experience-target-node-add-inner.md)
>* [在節點之間新增同層級目標節點](experience-target-node-add-sibling.md)
>* [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)
>* [將創意內容指派給最終節點](experience-assign-creative-bundles.md)
>* [自訂指派組合中創作的追蹤URL](experience-tracking-urls-targeting.md)
>* [自訂創意最佳化與排程](experience-optimization-scheduling-targeting.md)
>* [匯出並實作即時體驗的廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
