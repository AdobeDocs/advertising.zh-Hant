---
title: 自訂體驗的追蹤URL
description: 瞭解如何使用決策樹定位來自訂體驗中每個創意內容的追蹤URL。
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
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
source-wordcount: '448'
ht-degree: 0%
---
# 使用決策樹定位來自訂體驗中創意分子的追蹤URL

*僅具有現有創意的目標節點*

對於決策樹鎖定目標的體驗，您可以為體驗使用的每個個別創意建立最多五個自訂曝光追蹤URL和五個自訂點選追蹤URL。 當登入頁面覆寫可用時，您也可以指定自訂登入頁面URL。 您可以從任一決策樹編輯器中自訂追蹤URL。

自訂URL僅用於從體驗建立的廣告，不會儲存在[!UICONTROL Creative Libraries]的基本創意設定中。

標準體驗及使用預設創意的節點皆可使用此登陸頁面覆寫。 對於指派的動態套件組合，登入頁面由摘要決定，且不會顯示登入頁面標籤。

## 使用AI導向編輯器(Beta) {#ai-editor}

當您[建立](experience-create-targeting.md#ai-editor)或[編輯](experience-edit-targeting.md#ai-editor)體驗時，請使用畫布控制項：

1. 在目標節點下方的創意分葉節點上，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**。

1. 選取&#x200B;**[!UICONTROL Click Tracking URLs]**、**[!UICONTROL Impression Tracking URLs]**&#x200B;或（可用時） **[!UICONTROL Landing URL]**&#x200B;索引標籤。

   創意會依組合分組。 體驗的預設創意大小會決定可用的創意大小。

1. 展開您要編輯的創意內容，然後執行下列任一項作業：

   * 若要新增或編輯自訂URL，請在輸入欄位中輸入URL。

   * 若要新增另一個自訂追蹤URL，請按一下&#x200B;**[!UICONTROL Add URL]**，然後在輸入欄位中輸入URL。

   * 若要移除自訂URL，請按一下&#x200B;**[!UICONTROL Delete URL]**。

   在已編輯的欄位外按一下，並在儲存之前更正任何驗證錯誤。

1. 在對話方塊中按一下&#x200B;**[!UICONTROL Save]**&#x200B;以更新工作樹狀結構。

1. 從樹狀結構標頭[儲存體驗](#save)。

## 使用手動編輯器 {#manual-editor}

[在執行這些步驟之前，請先開啟手動編輯器](experience-edit-targeting.md#experience-open)。

1. 在目標節點下方的創意分葉節點上，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**。

1. 選取&#x200B;**[!UICONTROL Click Tracking URLs]**、**[!UICONTROL Impression Tracking URLs]**&#x200B;或（可用時） **[!UICONTROL Landing URLs]**&#x200B;索引標籤。

   標籤會列出指派的組合中的創意。 體驗的預設創意大小決定可用的創意大小。<!-- There's no distinct "Creative Sizes" setting. -->

1. 展開您要編輯的創意內容，然後執行下列任一項作業：

   * 若要新增或編輯自訂URL，請在輸入欄位中輸入URL。

   * 若要新增另一個自訂追蹤URL，請按一下&#x200B;**[!UICONTROL +]**，然後在輸入欄位中輸入URL。

   * 若要移除自訂URL，請將游標停留在創意列上，然後按一下![刪除](/help/creative/assets/delete.png "刪除")。

1. 在對話方塊中按一下&#x200B;**[!UICONTROL Save]**&#x200B;以更新工作樹狀結構。

1. 從樹狀結構標頭[儲存體驗](#save)。

## 儲存體驗 {#save}

以下步驟適用於兩個編輯器。 單獨儲存追蹤URL對話方塊不會儲存或發佈體驗。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [指派和取消指派創意組合至體驗中的最終節點](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自訂沒有決策樹定位之體驗的追蹤URL](experience-tracking-urls-no-targeting.md)
