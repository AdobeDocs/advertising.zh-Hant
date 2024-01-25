---
title: 管理Campaign資料檢視
description: 瞭解如何自訂行銷活動、套件、版位和廣告的資料檢視。
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# 管理Campaign資料檢視

## 管理資料視覺效果

您可以跨行銷活動或單一行銷活動變更所有資料視覺效果的量度和圖表模式。 對單一行銷活動所做的變更，會套用至該行銷活動的所有資料視覺效果，包括 [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads] 索引標籤。

### 變更資料視覺效果的量度

1. 在資料視覺效果的右上方，按一下 ![設定](/help/dsp/assets/settings-chart.png).
1. 選取量度。
您不能選取相同的量度兩次。
1. 按一下 **[!UICONTROL Apply]**.

### 變更資料視覺效果的顯示模式

* 在資料視覺效果的右上方，按一下 [!UICONTROL Overlay] 切換(![重疊切換](/help/dsp/assets/overlay.png))，以在覆蓋模式（所有圖表棧疊在一起）和格狀圖模式（三個個別的圖表）之間變更。

## 管理資料表

在所有行銷活動管理檢視中([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])，您可以自訂顯示在資料表格中的資料。

### 變更欄檢視

* 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下所需欄檢視的名稱。

### 建立自訂欄檢視

1. 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下 **[!UICONTROL Create View]**.

1. 指定要包含在檢視中的量度：

   1. 在可用量度清單中，選取每個要包含的量度旁的核取方塊。

   1. 視需要編輯欄順序，方法是按一下右側面板中的欄名稱，並將它們拖曳到所需位置。

   有些欄的位置固定，無法移動或移除。

1. 套用或儲存設定：

   * 若要暫時套用設定而不儲存至檢視，請按一下 **[!UICONTROL Apply].**

   * 若要將設定儲存至新的自訂欄檢視，請按一下 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 視窗，輸入新檢視的名稱，然後按一下 **[!UICONTROL Save]**.

### 編輯自訂欄檢視

>[!NOTE]
>
>您無法編輯標準（預先定義）欄檢視。

1. 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下現有的欄檢視名稱。

1. 在「檢視」選取器中，按一下 ![向下鍵](/help/dsp/assets/chevron-down.png)，然後按一下 **[!UICONTROL Edit View]**.

1. 編輯要納入檢視中的量度：

   1. 在可用量度清單中，選取每個要包含的量度旁的核取方塊，並清除每個要排除的量度旁的核取方塊。

   1. 視需要編輯欄順序，方法是按一下右側面板中的欄名稱，並將它們拖曳到所需位置。

   有些欄的位置固定，無法移動或移除。

1. 套用或儲存設定：

   * 若要暫時套用設定而不儲存至檢視，請按一下 **[!UICONTROL Apply].**

   * 若要將設定儲存至新的自訂欄檢視，請按一下 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 視窗，輸入新檢視的名稱，然後按一下 **[!UICONTROL Save]**.

### 篩選行銷活動資料

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

### 排序資料欄

您可以依遞增順序（A至Z、1至10）或遞減順序（Z至A、10至1）排序任何資料欄。

* 按一下欄標題，在升序和降序之間切換。

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [關於平台內報表](campaign-reports-about.md)
>* [管理資料視覺效果](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [變更欄檢視](column-view-change.md)
>* [建立自訂欄檢視](column-view-create.md)
>* [編輯自訂欄檢視](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [篩選行銷活動資料](campaign-data-filter.md)
>* [排序資料欄](campaign-data-sort.md)
>* [檢視位置的網站、廣告和頻率詳細資訊](placement-details-view.md)
>* [檢視刊登版位預測報表](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [檢視位置診斷報告](placement-diagnostics.md)
>* [從Campaign Management檢視匯出資料](campaign-export-data.md)
>* [影片：DSP帳戶結構和使用者介面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
