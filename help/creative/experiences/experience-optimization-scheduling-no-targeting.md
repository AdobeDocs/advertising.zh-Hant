---
title: 自訂體驗的創意最佳化和排程
description: 瞭解如何在不鎖定目標的情況下為體驗設定最佳化和廣告排程。
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---

# 針對沒有決策樹定位的體驗自訂創意最佳化和排程

*僅使用現有創意的體驗*

根據預設，廣告體驗標籤的創意輪換會以演演算法方式決定以最佳化整體點進率，而創意最佳化設定會套用至所有指派的創意內容。 您可以自訂創意輪換，以根據相對權重手動執行創意或對指定的Advertising DSP自訂目標進行演演算法最佳化。 您也可以排程特定創意在指定的連續時段內執行，並為每個排程套用自訂創意輪換設定。

## 設定創意最佳化而不排程

停用創意排程時，創意最佳化設定會套用至所有指派的創意內容。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 執行下列任一項作業：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**。

1. 將游標停留在適用廣告標籤的列上，然後按一下![廣告排程](/help/creative/assets/edit-gray.png "編輯追蹤URL") **[!UICONTROL Creative Optimization]**。&lt;！— Tag Manager只有清單檢視，但自2/2起沒有卡片檢視。 >

1. 停用&#x200B;**[!UICONTROL Schedule]**。

1. 選取關聯套件組合中廣告變體的創意輪換型別：

   * *[!UICONTROL Weighted]：*&#x200B;根據相對權重，在關聯的創意組合中顯示廣告變體。 以百分比輸入每個束的重量。 所有選取套裝的權重總和必須是100。<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的目標，更頻繁地顯示最有效的廣告變體。

      * 針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

   * *[!UICONTROL Sequencing]：*&#x200B;以指定順序顯示關聯的創意組合（先提供組合1，再提供組合2，依此類推），以及每個組合順序中的指定曝光總數。 提供的廣告大小由可用詳細目錄決定。 您可以將序列中的最後一個束配置為a\)無限顯示（預設值）或b\)回圈顯示到第一個束。 例如，您可以在組合1中顯示三(3)次曝光的任何廣告變體，然後在組合2中顯示一(1)次曝光的任何廣告變體，然後在組合3中顯示兩(2)次曝光的任何廣告變體，然後重新開始回圈。 或者，一旦顯示組合3中的廣告變體，您就可以繼續無限期地顯示組合3中的廣告變體，而不是建立回圈。 啟用排序時：

      1. 將指派的組合拖放至所需的順序。

     依預設，指派的組合會依照其加入體驗的順序排序。

      1. 輸入每個序列的曝光次數。

      1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 使用創意排程設定創意最佳化

您可以選擇將廣告體驗標籤使用的特定創意內容排程，在體驗開始和結束日期之間的指定連續時段內執行，並為每個排程套用自訂創意輪換設定。 例如，您可以將Creative 1排程在前兩週執行，以最佳化點進率，並將Creative 2排程在接下來的兩週執行，以最佳化指定的自訂目標。

使用排程時，您必須依照體驗的持續時間排程創意。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 執行下列任一項作業：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**。

1. 將游標停留在適用廣告標籤的列上，然後按一下![廣告排程](/help/creative/assets/edit-gray.png "編輯追蹤URL") **[!UICONTROL Creative Optimization]**。 <!-- For targeted experiences, this is "Edit Schedules" -->&lt;！— Tag Manager只有清單檢視，但自2/2起沒有卡片檢視。 >

1. 啟用&#x200B;**[!UICONTROL Schedule]**。

1. 對於第一個排程：

   1. 在左欄中，選取每個要新增至第一個排程的創意內容旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉創意。 以百分比輸入每個創意內容的權重。 所有選取創意的權重加起來最多必須為100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標以演演算法方式旋轉創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

      * *[!UICONTROL Sequencing]：*&#x200B;以指定的順序旋轉關聯的創意組合（先提供組合1，再提供組合2，依此類推），並指定各組合順序的曝光總數。 提供的廣告大小由可用詳細目錄決定。 您可以將序列中的最後一個束配置為a\)無限顯示（預設值）或b\)回圈顯示到第一個束。 例如，您可以針對三(3)次曝光在組合1中顯示任何創意，然後針對一(1)次曝光在組合2中顯示任何創意，接著針對兩(2)次曝光在組合3中顯示任何創意，然後再次開始回圈。 或者，一旦「束3」中的創意顯示出來，您就可以繼續無限期地在「束3」中顯示這些創意，而不是建立一個回圈。 啟用排序時：

         1. 將指派的組合拖放至所需的順序。

            依預設，指派的組合會依照其加入體驗的順序排序。

         1. 輸入每個序列的曝光次數。

         1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 對於每個額外的排程：

   1. 按一下&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左欄中，選取每個要新增至第一個排程的創意內容旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉創意。 以百分比輸入每個創意內容的權重。 所有選取創意的權重加起來最多必須為100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標以演演算法方式旋轉創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，請選取&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

      * *[!UICONTROL Sequencing]：*&#x200B;以指定的順序旋轉關聯的創意組合，每個組合順序具有指定的曝光總數。 啟用排序時：

         1. 將指派的組合拖放至所需的順序。

            依預設，指派的組合會依照其加入體驗的順序排序。

         1. 輸入每個序列的曝光次數。

         1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [手動建立適用創意大小的廣告標籤](/help/creative/experiences/experience-tag-create-manually.md)
>* [將創意內容指派給體驗的廣告標籤，而不需鎖定目標](experience-tag-assign-creatives.md)
>* [自訂沒有決策樹定位之體驗的追蹤URL](experience-tracking-urls-no-targeting.md)
