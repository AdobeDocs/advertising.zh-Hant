---
title: 編輯具有決策樹定位的體驗
description: 瞭解如何使用決策樹編輯目標廣告體驗的設定。
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
source-git-commit: 115b769c2880936c422747b44f43b4be7281916d
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# 編輯具有決策樹定位的體驗

*已關閉的Beta*

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定體驗。

1. 執行下列任一項作業：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Edit]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[一般體驗設定](experience-settings-targeting.md)。

1. （選擇性）若要編輯決策樹，請按一下右上方的&#x200B;**[!UICONTROL Decision Tree]**，然後執行下列任一項作業：

   * （[正在處理](experience-about.md#experience-statuses)個體驗）執行下列其中一項作業：

      * 若要捨棄即時體驗中現有的未張貼變更，請按一下&#x200B;**[!UICONTROL Discard and start again]**。

      * 若要保留現有的未張貼變更，請按一下&#x200B;**[!UICONTROL Continue editing draft]**。

      * 若要編輯體驗詳細資料，請按一下&#x200B;**[!UICONTROL Edit Experience Details]**。

   * （選擇性）變更決策樹的檢視設定。

     您的設定會儲存到您登出為止。

   * 移動滑桿來放大或縮小。

   * 按一下![以垂直樹狀結構檢視](/help/creative/assets/tree-vertical.png "以垂直樹狀結構檢視")或![以水準樹狀檢視](/help/creative/assets/tree-horizontal.png "以水準樹狀檢視")，在檢視垂直清單和水準清單之間切換。

   * （可選）透過下列任何方式變更廣告目標和對應的創意內容：

      * 目標：

        *[將目標節點新增到體驗中的最終層級](experience-target-node-add-final.md)。

         * [在節點之間插入目標節點](experience-target-node-add-inner.md)。

         * [在節點](experience-target-node-add-sibling.md)之間新增同層級目標節點。

         * [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)。

      * Creative套件組合：

         * [指派和取消指派創意內容給最終節點](experience-assign-creative-bundles.md)。

           如果您未將至少一個束指派給每個最終節點，則可在儲存體驗時，選擇對每個未指派的節點使用預設的創意。 若要發佈體驗，您必須指派組合或針對每個最終節點使用預設創意。

         * [自訂指派組合中創意的追蹤URL](experience-tracking-urls-targeting.md)。

         * [針對指派的組合自訂創意最佳化與排程](experience-optimization-scheduling-targeting.md)。

1. 按一下&#x200B;**[!UICONTROL Save]**，然後執行下列動作。

   * （如果最底層的每個節點至少包含一個創意組合）按一下&#x200B;**[!UICONTROL OK]**。

   * （如果最底層的每個節點不包含至少一個創意搭售方案），請執行下列任一項作業：

      * 若要儲存不含所有必要創意套裝的體驗，請按一下&#x200B;**[!UICONTROL Save as Draft]**。

        您無法為[草稿](experience-about.md#experience-statuses)體驗建立廣告標籤。

      * 若要將預設創意內容指派給尚未指派創意套裝的每個目標，請按一下「**[!UICONTROL Assign Default Creatives]**」。 檢閱已指派預設創意的更新樹狀結構後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

      * 若要繼續編輯決策樹，請按一下&#x200B;**[!UICONTROL Continue Edit]**。

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
>* [建立決策樹定位的體驗](experience-create-targeting.md)
