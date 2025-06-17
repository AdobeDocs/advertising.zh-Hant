---
title: 自訂體驗的創意最佳化和排程
description: 瞭解如何
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 006b0c61c28f5fac111ccdcc007e1752e05da63f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# 針對沒有決策樹定位的體驗自訂創意最佳化和排程

*僅使用現有創意的體驗*
*已關閉的Beta版*

根據預設，廣告體驗標籤的創意輪換會以演演算法方式決定以最佳化整體點進率，而創意最佳化設定會套用至所有指派的創意內容。 您可以自訂創意輪換，以根據相對權重手動執行創意或對指定的Advertising DSP自訂目標進行演演算法最佳化。 您也可以排程特定創意在指定的連續時段內執行，並為每個排程套用自訂創意輪換設定。

## 設定創意最佳化而不排程

停用創意排程時，創意最佳化設定會套用至所有指派的創意內容。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 執行下列任一項作業：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**

1. 將游標停留在適用廣告標籤的列上，然後按一下![廣告排程](/help/creative/assets/edit-gray.png "編輯追蹤URL") **[!UICONTROL Ad Schedule]**。 <!-- For targeted experiences, this is "Edit Schedules" -->&lt;！— Tag Manager只有清單檢視，但自2/2起沒有卡片檢視。 >

1. 停用&#x200B;**[!UICONTROL Schedule]**。

1. 選取創意旋轉型別：

   * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉創意。 以百分比輸入每個創意內容的權重。 所有選取創意的權重加起來最多必須為100。

   * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標以演演算法方式旋轉創意。

      * 針對&#x200B;**[!UICONTROL Optimization Goal]**，請選取&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 使用創意排程設定創意最佳化

您可以選擇將廣告體驗標籤使用的特定創意內容排程，在體驗開始和結束日期之間的指定連續時段內執行，並為每個排程套用自訂創意輪換設定。 例如，您可以將Creative 1排程在前兩週執行，以最佳化點進率，並將Creative 2排程在接下來的兩週執行，以最佳化指定的自訂目標。

使用排程時，您必須依照體驗的持續時間排程創意。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 執行下列任一項作業：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**

1. 將游標停留在適用廣告標籤的列上，然後按一下![廣告排程](/help/creative/assets/edit-gray.png "編輯追蹤URL") **[!UICONTROL Ad Schedule]**。 <!-- For targeted experiences, this is "Edit Schedules" -->&lt;！— Tag Manager只有清單檢視，但自2/2起沒有卡片檢視。 >

1. 啟用&#x200B;**[!UICONTROL Schedule]**。

1. 對於第一個排程：

   1. 在左欄中，選取每個要新增至第一個排程的創意內容旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉創意。 以百分比輸入每個創意內容的權重。 所有選取創意的權重加起來最多必須為100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標以演演算法方式旋轉創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，請選取&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 對於每個額外的排程：

   1. 按一下&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左欄中，選取每個要新增至第一個排程的創意內容旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉創意。 以百分比輸入每個創意內容的權重。 所有選取創意的權重加起來最多必須為100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標以演演算法方式旋轉創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，請選取&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [手動建立適用創意大小的廣告標籤](/help/creative/experiences/experience-tag-create-manually.md)
>* [將創意內容指派給體驗的廣告標籤，而不需鎖定目標](experience-tag-assign-creatives.md)
>* [自訂沒有決策樹定位之體驗的追蹤URL](experience-tracking-urls-no-targeting.md)
