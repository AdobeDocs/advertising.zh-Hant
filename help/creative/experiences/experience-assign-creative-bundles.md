---
title: 指派和取消指派創意套件組合至體驗中的最終節點
description: 瞭解如何將創意內容指派給廣告體驗中的每個目標。
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: 24ae6f65552a2c958488be4f1363c08c3f387d37
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 指派和取消指派創意套件組合至體驗中的最終節點

*僅使用決策樹定位的體驗*

您可以在體驗決策樹的最底層將創意套件組合指派給目標節點。 對於您尚未設定目標的體驗，最下層位於「全部」下。

針對標準廣告體驗，您只能指派標準創意組合。 針對動態廣告體驗，您只能指派動態創意組合。

>[!NOTE]
>
>如果您未指派至少一個創意組合至每個最終節點，則可在您[儲存體驗](experience-create-targeting.md)時，選擇使用每個未指派節點的預設創意。 若要發佈體驗，您必須指派組合或針對每個最終節點使用預設創意。

<!-- 1. [ways to get to the decision tree] -->

1. 執行下列任一項作業：

   * （沒有創意的最終節點）在節點底下，按一下&#x200B;**[!UICONTROL Assign Bundles]**。

   * （具有現有創意的節點）將游標停留在目標節點下方的創意組合方塊上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

1. 選取要指派給目標節點的每個束旁的核取方塊，並取消選取要取消指派的每個束旁的核取方塊。

   只會列出體驗（標準或動態）的相關套件組合型別的套件組合。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. （選擇性） [自訂指派的組合之創意最佳化與排程](experience-optimization-scheduling-targeting.md)。

1. （選擇性） [自訂指派的組合中創作的追蹤URL](experience-tracking-urls-targeting.md)。

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [新增目標節點至最終層級](experience-target-node-add-final.md)
>* [在節點之間插入目標節點](experience-target-node-add-inner.md)
>* [在節點之間新增同層級目標節點](experience-target-node-add-sibling.md)
>* [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [目標體驗設定](experience-settings-targeting.md)
>* [匯出並實作即時體驗的廣告體驗標籤](experience-tag-export.md)
