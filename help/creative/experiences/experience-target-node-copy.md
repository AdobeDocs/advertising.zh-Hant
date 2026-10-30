---
title: 將子節點複製到相同層級的另一個目標節點
description: 瞭解如何將父目標節點的所有子節點複製到相同層級的另一個目標節點
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: 'https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%
---
# 將子節點複製到相同層級的另一個目標節點

*僅使用決策樹定位的體驗*

您可以將父目標節點的所有子節點（包括所有子目標以及指派給它們的創意組合）複製到相同層級的另一個目標節點。 您可以透過以下方式複製節點：(a)將複製的節點新增到現有框架，或(b)完全取代現有框架。<!-- Give the main use case or an example to explain. -->

此功能不會影響為父節點指定的目標，只會影響子節點。

## 使用AI導向編輯器(Beta) {#ai-editor}

當您[建立](experience-create-targeting.md#ai-editor)或[編輯](experience-edit-targeting.md#ai-editor)體驗時，請使用畫布控制項：

1. 在您要複製其子系的上層節點上，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Copy Children]**。

1. 在相同層級的目的地節點上，按一下&#x200B;**[!UICONTROL ...]**，然後選擇下列其中一項：

   * 若要在不移除現有子項的情況下新增複製的子專案標和創意，請按一下&#x200B;**[!UICONTROL Add]**。

   * 若要以複製的子項取代現有的子專案標和創意，請按一下&#x200B;**[!UICONTROL Replace]**。

   當樹狀結構不支援動作時，就會停用動作。 在繼續之前，請檢閱任何警告。

1. 檢閱目的地分支，然後[儲存體驗](#save)。

## 使用手動編輯器 {#manual-editor}

[在執行這些步驟之前，請先開啟手動編輯器](experience-edit-targeting.md#experience-open)。

1. 按一下您要複製其子系的父節點，按一下[新增] ![](/help/creative/assets/add.png "")，然後a\)選取&#x200B;**[!UICONTROL Copy Children ctrl+c]**&#x200B;或b\)在鍵盤上輸入&#x200B;**[!UICONTROL Ctrl+C]** ([!DNL Microsoft Windows])或&#x200B;**[!UICONTROL Command-C]** ([!DNL Apple Macintosh])。

1. 執行下列任一項作業：

   * 若要取代節點的所有子項節點和創意，請按一下您要將複製資訊貼到其中的節點，按一下&#x200B;**[!UICONTROL ...]**，然後a\)選取&#x200B;**[!UICONTROL Replace ctrl+shift+v]**&#x200B;或b\)在鍵盤上輸入&#x200B;**[!UICONTROL Ctrl+Shift+V]** ([!DNL Microsoft Windows])或&#x200B;**[!UICONTROL Command-Shift-V]** ([!DNL Apple Macintosh])。

   * （具有多個子目標的節點，沒有「全部」節點，僅沒有創意）若要將所有子節點和創意新增至節點，而不刪除現有的節點，請按一下您要貼上複製資訊的節點，按一下「**[!UICONTROL ...]**」，然後a\)選取「**[!UICONTROL Add ctrl+v]**」或b\)，在鍵盤上輸入「**[!UICONTROL Ctrl+V]**」([!DNL Microsoft Windows])或「**[!UICONTROL Command-V]**」([!DNL Apple Macintosh])。

## 儲存體驗 {#save}

以下步驟適用於兩個編輯器。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [新增目標節點至最終層級](experience-target-node-add-final.md)
>* [在節點之間插入目標節點](experience-target-node-add-inner.md)
>* [在節點之間新增同層級目標節點](experience-target-node-add-sibling.md)
>* [將創意內容指派給最終節點](experience-assign-creative-bundles.md)
>* [刪除目標節點或創意分葉節點](/help/creative/experiences/experience-target-node-delete.md)
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [目標體驗設定](experience-settings-targeting.md)
