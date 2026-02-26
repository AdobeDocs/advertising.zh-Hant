---
title: 自訂體驗的創意最佳化和排程
description: 瞭解如何針對目標體驗設定最佳化和廣告排程。
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 24ae6f65552a2c958488be4f1363c08c3f387d37
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# 針對使用決策樹定位的體驗自訂創意最佳化和排程

*僅具有現有創意的目標節點*

根據預設，體驗的創意輪換會以演演算法方式決定以最佳化整體點進率，而創意最佳化設定會套用至所有指派的組合。 您可以針對指定的Advertising DSP自訂目標交替進行演演算法最佳化；根據指定的束序列旋轉束，並在每個束序列上指定曝光次數；或根據相對權重。 您也可以排程特定的創意組合在指定的連續時段內執行，並為每個排程套用自訂創意輪換設定。

>[!NOTE]
>
>這些功能不適用於使用預設創意而非指定創意的節點。

## 設定創意最佳化而不排程

停用創意排程時，創意最佳化設定會套用至所有指派的創意內容。

1. 當您[建立](experience-create-targeting.md)或[編輯](experience-edit-targeting.md)體驗時，請開啟創意最佳化設定：

   1. 將游標停留在目標節點下方的創意葉節點上，並執行下列動作：

      * 針對現有組合，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

      * 針對新組合，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]**&#x200B;並[指派組合](experience-assign-creative-bundles.md)。

1. 按一下「**[!UICONTROL Creative Optimization]**」標籤。

1. 停用&#x200B;**[!UICONTROL Schedule]**。

1. 選取關聯套件組合中廣告變體的創意輪換型別：

   * *[!UICONTROL Weighted]：*&#x200B;根據相對權重，在關聯的創意組合中顯示廣告變體。 以百分比輸入每個束的重量。 若要將相等權重套用至所有關聯的組合，請按一下（![套用相等權重](/help/creative/assets/apply-equal-weight.png "套用相等權重")）。 所有選取套裝的權重總和必須是100。<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的目標，更頻繁地顯示最有效的廣告變體。

      * 針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

   * *[!UICONTROL Sequencing]：*&#x200B;以指定順序顯示關聯的創意組合（先提供組合1，再提供組合2，依此類推），以及每個組合順序中的指定曝光總數。 提供的廣告大小由可用詳細目錄決定。 您可以將序列中的最後一個束配置為a\)無限顯示（預設值）或b\)回圈顯示到第一個束。 例如，您可以在組合1中顯示三(3)次曝光的任何廣告變體，然後在組合2中顯示一(1)次曝光的任何廣告變體，然後在組合3中顯示兩(2)次曝光的任何廣告變體，然後重新開始回圈。 或者，一旦顯示組合3中的廣告變體，您就可以繼續無限期地顯示組合3中的廣告變體，而不是建立回圈。 啟用排序時：

      1. 將指派的組合拖放至所需的順序。

     依預設，指派的組合會依照其加入體驗的順序排序。

      1. 輸入每個序列的曝光次數。

      1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 使用創意排程設定創意最佳化

您可以選擇將特定創意組合排程在體驗開始和結束日期之間的指定連續時段內執行，並為每個排程套用自訂創意輪換設定。 例如，您可以排程組合1在前兩週執行以最佳化點進率，以及組合2在接下來的兩週執行以最佳化指定的自訂目標。

使用排程時，必須在體驗期間排程組合。

1. 當您[建立](experience-create-targeting.md)或[編輯](experience-edit-targeting.md)體驗時，請開啟創意最佳化設定：

   1. 將游標停留在目標節點下方的創意葉節點上，並執行下列動作：

      * 針對現有組合，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

      * 針對新組合，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]**&#x200B;並[指派組合](experience-assign-creative-bundles.md)。

1. 按一下「**[!UICONTROL Creative Optimization]**」標籤。

1. 啟用&#x200B;**[!UICONTROL Schedule]**。

1. 對於第一個排程：

   1. 在左欄中，選取要新增至第一個排程的每個創意套件組合旁的核取方塊。

   1. 指定排程的開始日期和開始時間，以及結束日期和結束時間。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉每個組合中的創意。 以百分比輸入每個束的重量。 若要將相等權重套用至排程中的所有組合，請按一下（![套用相等權重](/help/creative/assets/apply-equal-weight.png "套用相等權重")）。 所有選定套裝的重量最多必須相加100個。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標，以演演算法方式旋轉每個組合中的創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]：*&#x200B;以指定的順序旋轉關聯的創意組合（先提供組合1，再提供組合2，依此類推），並指定各組合順序的曝光總數。 提供的廣告大小由可用詳細目錄決定。 您可以將序列中的最後一個束配置為a\)無限顯示（預設值）或b\)回圈顯示到第一個束。 例如，您可以針對三(3)次曝光在組合1中顯示任何創意，然後針對一(1)次曝光在組合2中顯示任何創意，接著針對兩(2)次曝光在組合3中顯示任何創意，然後再次開始回圈。 或者，一旦「束3」中的創意顯示出來，您就可以繼續無限期地在「束3」中顯示這些創意，而不是建立一個回圈。 啟用排序時：

         1. 將指派的組合拖放至所需的順序。

            依預設，指派的組合會依照其加入體驗的順序排序。

         1. 輸入每個序列的曝光次數。

         1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 對於每個額外的排程：

   1. 按一下&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左欄中，選取要新增至第一個排程的每個創意套件組合旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;根據相對權重手動旋轉每個組合中的創意。 以百分比輸入每個束的重量。 所有選定套裝的重量最多必須相加100個。

      * *[!UICONTROL Algorithmic]：*&#x200B;根據指定的最佳化目標，以演演算法方式旋轉每個組合中的創意。

         * 針對&#x200B;**[!UICONTROL Optimization Goal]**，請選取&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]：*&#x200B;以指定的順序旋轉關聯的創意組合，每個組合順序具有指定的曝光總數。 啟用排序時：

         1. 將指派的組合拖放至所需的順序。

            依預設，指派的組合會依照其加入體驗的順序排序。

         1. 輸入每個序列的曝光次數。

         1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [指派和取消指派創意組合至體驗中的最終節點](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自訂創意作品的追蹤URL](/help/creative/experiences/experience-tracking-urls-targeting.md)
