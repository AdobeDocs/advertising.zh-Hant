---
title: 自訂體驗的創意最佳化和排程
description: 瞭解如何針對目標體驗設定最佳化和廣告排程。
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
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
source-wordcount: '1244'
ht-degree: 0%
---
# 針對使用決策樹定位的體驗自訂創意最佳化和排程

*僅具有現有創意的目標節點*

依預設，體驗會針對所有指派套裝的整體點進率，最佳化創意輪換。 您可以自訂旋轉設定，或排程特定組合以於連續時間週期執行，每個排程都有個別的旋轉設定。

>[!NOTE]
>
>這些功能不適用於使用預設創意而非指定創意的節點。

您可以直接在AI導向編輯器(Beta)的畫布或手動編輯器中配置這些設定。 在任一編輯器中，儲存組合對話方塊會更新工作樹狀結構；您也必須從樹狀結構標題[儲存體驗](#save)。

## 旋轉設定 {#rotation-settings}

* **[!UICONTROL Weighted]：**&#x200B;根據相對權重，在關聯的創意組合中顯示廣告變體。

* **[!UICONTROL Algorithmic]：**&#x200B;根據指定的最佳化目標（例如點進率或Advertising DSP自訂目標），更頻繁地顯示最有效的廣告變體。

* **[!UICONTROL Sequence]（AI驅動編輯器）或[!UICONTROL Sequencing] （手動編輯器）：**&#x200B;以指定順序顯示關聯的創意組合，以及序列中每個組合的指定曝光次數。 依預設，套件組合會依其新增至體驗的順序排序。 提供的廣告大小由可用詳細目錄決定。 最終束可以無限期地提供（預設），或序列可以回圈到第一個束。

  例如，序列可提供組合1中的廣告變體給三個印象，組合2給一個印象，而組合3給兩個印象，然後重複這些變化。 沒有回圈，套件3會無限期繼續提供。

## 設定創意最佳化而不排程

停用創意排程時，創意最佳化設定會套用至所有指派的創意內容。

### 使用AI導向編輯器(Beta) {#without-scheduling-ai}

1. 當您[建立](experience-create-targeting.md#ai-editor)或[編輯](experience-edit-targeting.md#ai-editor)體驗時，請按一下創意分葉節點上的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

   若要取得不含組合的最終節點，請先按一下&#x200B;**[!UICONTROL Assign Bundles]**&#x200B;和[指派組合](experience-assign-creative-bundles.md#ai-editor)。

1. 開啟&#x200B;**[!UICONTROL Creative optimisation]**&#x200B;標籤。

1. 停用&#x200B;**[!UICONTROL Schedule]**。

1. 選取創意輪換型別並設定其設定：

   * **[!UICONTROL Weighted]：**&#x200B;輸入每個組合列的相對權重。 總重量必須為100。 若要平均分配權重，請按一下&#x200B;**[!UICONTROL Apply equal weight]**。

   * **[!UICONTROL Algorithmic]：**&#x200B;選取&#x200B;**[!UICONTROL Optimization goals]**&#x200B;選項。 如果您選擇自訂目標，請在&#x200B;**[!UICONTROL Custom objective]**&#x200B;中選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

   * **[!UICONTROL Sequence]：**&#x200B;將組合拖曳到所需的順序，然後輸入每個順序的曝光次數。 啟用&#x200B;**[!UICONTROL Keep in loop]**&#x200B;以重複該順序，或保持停用狀態以將最後一個組合曝光數設定為&#x200B;**[!UICONTROL Infinite]**。

1. 在對話方塊中按一下&#x200B;**[!UICONTROL Save]**。

1. [儲存體驗](#save)。

### 使用手動編輯器 {#without-scheduling-manual}

[在執行這些步驟之前，請先開啟手動編輯器](experience-edit-targeting.md#experience-open)。

1. 當您[建立](experience-create-targeting.md)或[編輯](experience-edit-targeting.md)體驗時，請開啟創意最佳化設定：

   1. 將游標停留在目標節點下方的創意葉節點上，並執行下列動作：

      * 針對現有組合，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

      * 針對新組合，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]**&#x200B;並[指派組合](experience-assign-creative-bundles.md)。

   1. 按一下「**[!UICONTROL Creative Optimization]**」標籤。

1. 停用&#x200B;**[!UICONTROL Schedule]**。

1. 選取關聯套件組合中廣告變體的創意輪換型別：

   * *[!UICONTROL Weighted]：*&#x200B;以百分比輸入每個套件的權重。 若要將相等權重套用至所有關聯的組合，請按一下（![套用相等權重](/help/creative/assets/apply-equal-weight.png "套用相等權重")）。 所有選定套裝的重量最多必須相加100個。

   * *[!UICONTROL Algorithmic]：*&#x200B;針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。 如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

   * *[!UICONTROL Sequencing]:*

     1. 將指派的組合拖放至所需的順序。

     1. 輸入每個序列的曝光次數。

     1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 使用創意排程設定創意最佳化

您可以選擇將特定創意組合排程在體驗開始和結束日期之間的指定連續時段內執行，並為每個排程套用自訂創意輪換設定。 例如，您可以排程組合1在前兩週執行以最佳化點進率，以及組合2在接下來的兩週執行以最佳化指定的自訂目標。

使用排程時，必須在體驗期間排程組合。

### 使用AI導向編輯器(Beta) {#with-scheduling-ai}

1. 當您[建立](experience-create-targeting.md#ai-editor)或[編輯](experience-edit-targeting.md#ai-editor)體驗時，請按一下創意分葉節點上的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

   若要取得不含組合的最終節點，請先按一下&#x200B;**[!UICONTROL Assign Bundles]**&#x200B;和[指派組合](experience-assign-creative-bundles.md#ai-editor)。

1. 開啟&#x200B;**[!UICONTROL Creative optimisation]**&#x200B;標籤，然後啟用&#x200B;**[!UICONTROL Schedule]**。

1. 選取排程的&#x200B;**[!UICONTROL Timezone]**。

1. 對於第一個排程：

   1. 選取每個要包含在左欄中的束旁的核取方塊。

   1. 指定開始和結束日期及時間。

   1. 選取創意輪換型別並設定其設定：

      * **[!UICONTROL Weighted]：**&#x200B;輸入排程中每個組合列的相對權重。 總重量必須為100。 若要平均分配權重，請按一下&#x200B;**[!UICONTROL Apply equal weight]**。

      * **[!UICONTROL Algorithmic]：**&#x200B;選取&#x200B;**[!UICONTROL Optimization goals]**&#x200B;選項。 如果您選擇自訂目標，請在&#x200B;**[!UICONTROL Custom objective]**&#x200B;中選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

      * **[!UICONTROL Sequence]：**&#x200B;將組合拖曳到所需的順序，然後輸入每個順序的曝光次數。 啟用&#x200B;**[!UICONTROL Keep in loop]**&#x200B;以重複該順序，或保持停用狀態以將最後一個組合曝光數設定為&#x200B;**[!UICONTROL Infinite]**。

1. 對於每個額外的排程，按一下&#x200B;**[!UICONTROL + Add Schedule]**，選取其排程卡片，並設定其組合、日期與時間以及輪換設定。

   束核取方塊會套用至選取的排程，而非所有排程。 請確定這些排程涵蓋指派的套裝所涵蓋的整個體驗期間。

1. 在對話方塊中按一下&#x200B;**[!UICONTROL Save]**。

1. [儲存體驗](#save)。

### 使用手動編輯器 {#with-scheduling-manual}

[在執行這些步驟之前，請先開啟手動編輯器](experience-edit-targeting.md#experience-open)。

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

      * *[!UICONTROL Weighted]：*&#x200B;以百分比輸入每個套件的權重。 若要將相等權重套用至排程中的所有組合，請按一下（![套用相等權重](/help/creative/assets/apply-equal-weight.png "套用相等權重")）。 所有選定套裝的重量最多必須相加100個。

      * *[!UICONTROL Algorithmic]：*&#x200B;針對&#x200B;**[!UICONTROL Optimization Goal]**，選取&#x200B;*[!UICONTROL Click Through Rate]*、（標準視訊廣告體驗） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。 如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]:*

        1. 將指派的組合拖放至所需的順序。

        1. 輸入每個序列的曝光次數。

        1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 對於每個額外的排程：

   1. 按一下&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左欄中，選取要新增至第一個排程的每個創意套件組合旁的核取方塊。

   1. 指定排程的開始和結束日期。

   1. 選取創意旋轉型別：

      * *[!UICONTROL Weighted]：*&#x200B;以百分比輸入每個套件的權重。 所有選定套裝的重量最多必須相加100個。

      * *[!UICONTROL Algorithmic]：*&#x200B;對於&#x200B;**[!UICONTROL Optimization Goal]**，請選取&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。 如果您選取&#x200B;*[!UICONTROL Custom Objective]*，則請選取現有的[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]:*

        1. 將指派的組合拖放至所需的順序。

        1. 輸入每個序列的曝光次數。

        1. 對於最後一個序列，將是否變更為a\)無限期地顯示序列中的最後一個束(*[!UICONTROL Infinite]* （預設值）或b\)回圈到顯示最後一個束(*[!UICONTROL Keep in Loop]*)之後的第一個束。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 儲存體驗 {#save}

以下步驟適用於兩個編輯器。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [指派和取消指派創意組合至體驗中的最終節點](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自訂創意作品的追蹤URL](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [檢視體驗的變更記錄](/help/creative/experiences/experience-view-change-log.md)
