---
title: 編輯具有決策樹定位的體驗
description: 瞭解如何使用AI驅動或手動決策樹編輯器編輯目標廣告體驗。
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%
---
# 編輯具有決策樹定位的體驗

AI導向編輯器(Beta)依預設會針對具有鎖定目標的體驗開啟。 您可以使用AI代理程式、直接編輯畫布或開啟現有的手動編輯器。

## 開啟體驗 {#experience-open}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定體驗。

1. 執行下列任一項作業：

   * 若要開啟AI驅動編輯器：

     * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Edit]**。

     * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Edit]**。

   * 若要開啟手動編輯器：

     * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Create Decision Tree Manually (Legacy)]**。

     * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Create Decision Tree Manually (Legacy)]**。

     * 在AI驅動編輯器中，

## 使用AI導向編輯器編輯(Beta) {#ai-editor}

1. [開啟體驗](#experience-open)。

1. 說明您想在交談中進行的目標定位變更。 透過其目標識別受影響的分支，或當顯示在畫布上時，透過其節點ID識別受影響的分支。

1. 檢閱更新的樹狀結構，並說明任何進一步的變更。 在與畫布互動之前，請等候助理完成處理。

1. （選用）直接在畫布中進行變更：

   * [新增最終層級目標](experience-target-node-add-final.md#ai-editor)、[插入目標層級](experience-target-node-add-inner.md#ai-editor)或[新增同層級目標](experience-target-node-add-sibling.md#ai-editor)。

   * 按一下目標旁的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**，變更值，然後按一下&#x200B;**[!UICONTROL Edit Node]**&#x200B;以編輯目標的條件。

   * [複製子節點和創意](experience-target-node-copy.md#ai-editor)或[刪除節點](experience-target-node-delete.md#ai-editor)。

   * [指派或取消指派創意組合](experience-assign-creative-bundles.md#ai-editor)。

   * [自訂創意最佳化和排程](experience-optimization-scheduling-targeting.md)或[追蹤URL](experience-tracking-urls-targeting.md#ai-editor)。

1. [儲存體驗](#save)。

## 使用手動編輯器編輯 {#manual-editor}

1. [開啟體驗](#experience-open)。

1. （狀態為`[processing](experience-about.md#experience-statuses)`的體驗）如果系統提示您存在未張貼的草稿，請執行下列其中一個動作：

   * 按一下&#x200B;**[!UICONTROL Continue editing draft]**&#x200B;以檢閱並繼續編輯草稿。

   * 按一下&#x200B;**[!UICONTROL Discard and start again]**&#x200B;以捨棄草稿並從即時版本開始。

   * 按一下&#x200B;**[!UICONTROL Cancel this edit]**&#x200B;停止編輯。

1. （選擇性）調整縮放滑桿，或按一下![以垂直樹狀結構檢視](/help/creative/assets/tree-vertical.png "以垂直樹狀結構檢視")或![以水準樹狀檢視](/help/creative/assets/tree-horizontal.png "以水準樹狀檢視")以變更方向。

   您的檢視設定會儲存到您登出為止。

1. 視需要變更目標和創意：

   * [新增最終層級目標](experience-target-node-add-final.md#manual-editor)、[在節點之間插入目標](experience-target-node-add-inner.md#manual-editor)，或[新增同層級目標](experience-target-node-add-sibling.md#manual-editor)。

   * [複製子節點和創意](experience-target-node-copy.md#manual-editor)或[刪除節點](experience-target-node-delete.md#manual-editor)。

   * [指派或取消指派創意組合](experience-assign-creative-bundles.md#manual-editor)。

   * [自訂創意最佳化和排程](experience-optimization-scheduling-targeting.md)或[追蹤URL](experience-tracking-urls-targeting.md#manual-editor)。

1. [儲存體驗](#save)。

## 切換編輯器或編輯體驗設定 {#switch-editors}

>[!IMPORTANT]
>
>在離開AI驅動編輯器之前，請儲存您要保留的任何樹狀結構變更。 切換到手動編輯器或體驗表單不會傳輸未儲存的變更。

* **手動編輯器的AI驅動編輯器：**&#x200B;按一下&#x200B;**[!UICONTROL Manual Decision Tree]**。 在確認對話方塊中，按一下&#x200B;**[!UICONTROL Yes]**&#x200B;以捨棄未儲存的變更並開啟手動編輯器，或按一下&#x200B;**[!UICONTROL No]**&#x200B;以保留。

* **AI驅動編輯器的一般設定：**&#x200B;按一下&#x200B;**[!UICONTROL Experience Form]**，然後按一下&#x200B;**[!UICONTROL Yes]**&#x200B;以捨棄未儲存的樹狀結構變更並開啟表單。 編輯[一般體驗設定](experience-settings-targeting.md)，然後按一下&#x200B;**[!UICONTROL Save]**。

* **手動編輯一般設定：**&#x200B;儲存您要保留的任何樹狀結構變更，然後按一下&#x200B;**[!UICONTROL Experience Form]**。 編輯[一般體驗設定](experience-settings-targeting.md)，然後按一下&#x200B;**[!UICONTROL Save]**。

* **AI驅動編輯器的一般設定：**&#x200B;按一下&#x200B;**[!UICONTROL Decision Tree]**。 儲存目標體驗一般設定的變更也會開啟AI導向的編輯器。

* **手動編輯器為AI驅動編輯器：**&#x200B;儲存您的樹狀結構變更，返回[!UICONTROL Experiences]檢視，然後選取&#x200B;**[!UICONTROL Edit]**&#x200B;進行體驗。

若要離開AI驅動編輯器而不開啟另一個編輯器，請按一下&#x200B;**[!UICONTROL Cancel]**。 按一下&#x200B;**[!UICONTROL Yes]**&#x200B;以捨棄未儲存的樹狀結構變更，或按一下&#x200B;**[!UICONTROL No]**&#x200B;以繼續編輯。

## 儲存體驗 {#save}

以下步驟適用於兩個編輯器。

{{$include /help/_includes/experience-save.md}}

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
>* [檢視體驗的變更記錄](/help/creative/experiences/experience-view-change-log.md)
