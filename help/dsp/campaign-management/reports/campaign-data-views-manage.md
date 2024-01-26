---
title: 管理您的Campaign資料檢視
description: 瞭解如何自訂行銷活動、套件、版位和廣告的資料檢視。
feature: DSP Campaign Data Views
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# 管理您的Campaign資料檢視

您可以自訂出現在行銷活動管理檢視中的資料([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])。

## 管理資料視覺效果 {#data-visualizations-manage}

您可以跨行銷活動或單一行銷活動變更所有資料視覺效果的量度和圖表模式。 對單一行銷活動所做的變更，會套用至該行銷活動的所有資料視覺效果，包括 [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads] 檢視。

### 變更資料視覺效果的量度

1. 在資料視覺效果的右上方，按一下 ![設定](/help/dsp/assets/settings-chart.png).

1. 選取量度。

   您不能選取相同的量度兩次。

1. 按一下 **[!UICONTROL Apply]**.

### 變更資料視覺效果的顯示模式

* 在資料視覺效果的右上方，按一下 [!UICONTROL Overlay] 切換(![重疊切換](/help/dsp/assets/overlay.png))，以在覆蓋模式（所有圖表棧疊在一起）和格狀圖模式（三個個別的圖表）之間變更。

## 管理資料表 {#data-tables-manage}

在所有行銷活動管理檢視中([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])，您可以自訂顯示在資料表格中的資料。

### 管理欄檢視 {#column-views-manage}

每個行銷活動管理層級([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])包含內建 [!UICONTROL Pacing] 和 [!UICONTROL Performance] 包含該實體相關度量的檢視。 根據預設， [!UICONTROL Pacing] 顯示檢視，以便您一眼即可識別表現不佳的行銷活動和行銷活動元件。 您可以選擇建立和編輯自訂欄集合。

![欄檢視選擇器](/help/dsp/assets/column-view-selector.png)

DSP會將您最近的檢視儲存為預設檢視，因此每次您返回頁面時，都可檢視與您相關的測量結果。

#### 變更欄檢視 {#column-view-change}

* 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下所需欄檢視的名稱。

#### 建立自訂欄檢視 {#column-view-create}

1. 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下 **[!UICONTROL Create View]**.

1. 指定要包含在檢視中的量度：

   1. 在可用量度清單中，選取每個要包含的量度旁的核取方塊。

      所有量度都是依類別的字母順序排列： [!UICONTROL Settings]， [!UICONTROL Spend]， [!UICONTROL Pacing]， [!UICONTROL Reporting] (DSP追蹤的標準量度)、 [!UICONTROL Viewability]、和 [!UICONTROL Conversions]. 量度附加了「(」[!UICONTROL Lifetime])」從行銷活動開始傳回值，無論頁面上選取的日期範圍為何。

   1. 視需要編輯欄順序，方法是按一下右側面板中的欄名稱，並將它們拖曳到所需位置。

   有些欄的位置固定，無法移動或移除。

1. 套用或儲存設定：

   * 若要暫時套用設定而不儲存至檢視，請按一下 **[!UICONTROL Apply].**

   * 若要將設定儲存至新的自訂欄檢視，請按一下 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 視窗，輸入新檢視的名稱，然後按一下 **[!UICONTROL Save]**.

#### 編輯欄檢視 {#column-view-edit}

>[!NOTE]
>
>您無法將變更儲存到標準（預先定義）欄檢視，但可以暫時套用變更或將變更儲存到新的自訂檢視。

1. 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下現有的欄檢視名稱。

1. 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下 **[!UICONTROL Edit View]**.

1. 編輯要納入檢視中的量度：

   1. 在可用量度清單中，選取每個要包含的量度旁的核取方塊，並清除每個要排除的量度旁的核取方塊。

      所有量度都是依類別的字母順序排列： [!UICONTROL Settings]， [!UICONTROL Spend]， [!UICONTROL Pacing]， [!UICONTROL Reporting] (DSP追蹤的標準量度)、 [!UICONTROL Viewability]、和 [!UICONTROL Conversions]. 量度附加了「(」[!UICONTROL Lifetime])」從行銷活動開始傳回值，無論頁面上選取的日期範圍為何。

   1. 視需要編輯欄順序，方法是按一下右側面板中的欄名稱，並將它們拖曳到所需位置。

   有些欄的位置固定，無法移動或移除。

1. 套用或儲存設定：

   * （僅限自訂檢視）若要儲存設定，請按一下 **[!UICONTROL Save]**.

   * 若要暫時套用設定而不儲存至檢視，請按一下 **[!UICONTROL Apply].**

   * 若要將設定儲存至新的自訂欄檢視，請按一下 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 視窗，輸入新檢視的名稱，然後按一下 **[!UICONTROL Save]**.

### 篩選行銷活動資料 {#filter-data-tables}

篩選器會變更目前標籤上顯示的資料。 可用的篩選器會依實體型別而異，但可能包括實體名稱、狀態和其他屬性欄。

1. 在主工具列中，按一下 ![篩選按鈕](/help/dsp/assets/filter.png).
1. 對於每個要套用的篩選，請按一下左欄中的篩選名稱，然後指定篩選值。
1. 按一下 **[!UICONTROL Apply]**.

#### 可用的篩選器

下列篩選器適用於您的 [!UICONTROL Campaigns]， [!UICONTROL Packages]、和 [!UICONTROL Placements] 檢視：

* [!UICONTROL Campaigns] 檢視篩選器：
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] 檢視篩選器：
   * [!UICONTROL Custom flights] （無論它們是否存在）
   * [!UICONTROL Custom goal] （如果適用）
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] 檢視篩選器：
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] （如果適用）
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than]， [!UICONTROL greater than]，或 [!UICONTROL equal to] 指定值)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] 或 [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] 檢視篩選器：
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### 變更日期範圍

使用任何資料表格上方的日期範圍選取器，變更用於所有標準和自訂檢視的日期範圍。

![日期範圍選擇器](/help/dsp/assets/date-range-selector.png "日期範圍選擇器")

* 針對預設範圍：從常用時間增量清單中選取。 預設值為 [!UICONTROL Last 30 days]*.

* 針對特定範圍，請執行下列任一項作業：

   * 按一下 ![行事曆](/help/dsp/assets/calendar.png "行事曆")，然後按一下日曆中的開始日期和結束日期。

   * 在日期範圍內按一下，然後輸入開始日期和結束日期，或在行事曆中選取它們。

     您可以輸入數值（從M-D-YY到MM-DD-YYYY）及/或月份名稱或縮寫（例如1月或1月）。

### 排序資料欄

您可以依遞增順序（A至Z、1至10）或遞減順序（Z至A、10至1）排序任何資料欄。

* 按一下欄標題，在升序和降序之間切換。


### 指定資料列數

在任何頁面的右下方、旁邊 **[!UICONTROL Items per page]** ，選取 *[!UICONTROL 25]*， *[!UICONTROL 50]*，或 *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [關於Campaign Management檢視中的效能報表](campaign-reports-about.md)
>* [檢視位置的網站、廣告和頻率詳細資訊](placement-details-view.md)
>* [檢視刊登版位預測報表](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [檢視位置診斷報告](placement-diagnostics.md)
>* [從Campaign Management檢視匯出資料](campaign-export-data.md)
>* [影片：DSP帳戶結構和使用者介面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
