---
title: 自訂體驗的創意最佳化和排程
description: 瞭解如何
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 7fee6e0f6e8ad6dbf0329d707af7303ac7229dc9
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# 針對使用決策樹定位的體驗自訂創意最佳化和排程

*僅具有現有創意的目標節點*
*已關閉的Beta版*

根據預設，體驗的創意輪換會以演演算法方式決定以最佳化整體點進率，而創意最佳化設定會套用至所有指派的組合。 您可以自訂創意輪換，以根據相對權重手動執行每個組合中的創意，或針對指定的Advertising DSP自訂目標進行演演算法最佳化。 您也可以排程特定的創意組合在指定的連續時段內執行，並為每個排程套用自訂創意輪換設定。

>[!NOTE]
>
>這些功能不適用於使用預設創意而非指定創意的節點。

## 設定創意最佳化而不排程

停用創意排程時，創意最佳化設定會套用至所有指派的創意內容。

1. 將游標停留在目標節點下方的創意葉節點上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**。

1. 停用&#x200B;**[!UICONTROL Schedule]**。

1. 選取創意旋轉型別：

   * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉每個組合中的創意。 以百分比輸入每個束的重量。 所有套裝的重量最多必須相加100。

   * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標，以演演算法方式旋轉每個組合中的創意。

      * 針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 使用創意排程設定創意最佳化

您可以選擇將特定創意組合排程在體驗開始和結束日期之間的指定連續時段內執行，並為每個排程套用自訂創意輪換設定。 例如，您可以排程組合1在前兩週執行以最佳化點進率，以及組合2在接下來的兩週執行以最佳化指定的自訂目標。

使用排程時，必須在體驗期間排程組合。

1. 將游標停留在目標節點下方的創意葉節點上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**。

1. 啟用&#x200B;**[!UICONTROL Schedule]**。

1. 對於第一個排程：

   1. 在左欄中，選取要新增至第一個排程的每個創意套件組合旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉每個組合中的創意。 以百分比輸入每個束的重量。 所有選定套裝的重量最多必須相加100個。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標，以演演算法方式旋轉每個組合中的創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

1. 對於每個額外的排程：

   1. 按一下&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左欄中，選取要新增至第一個排程的每個創意套件組合旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉每個組合中的創意。 以百分比輸入每個束的重量。 所有選定套裝的重量最多必須相加100個。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標，以演演算法方式旋轉每個組合中的創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，請選取&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [指派和取消指派創意組合至體驗中的最終節點](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自訂創意作品的追蹤URL](/help/creative/experiences/experience-tracking-urls-targeting.md)
