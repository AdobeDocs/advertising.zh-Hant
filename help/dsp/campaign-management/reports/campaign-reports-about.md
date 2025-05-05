---
title: Campaign Management檢視中的效能報表型別
description: 瞭解行銷活動管理檢視中包含的報告資料。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: eba8e9813f8daea58b30f7890ac2dca2498f326f
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Campaign Management檢視中的效能報表型別

行銷活動管理檢視包含完整的報告資料。 可用的報表可協助您識別執行良好的套件和位置，以及需要您注意的套件和位置。 快速動作按鈕也讓您提高生產力。

## 所有行銷活動檢視

[!UICONTROL Campaigns]檢視會開啟一組效能資料圖表，以及您帳戶中所有行銷活動的清單。

### 圖表檢視 {#chart-view}

您可使用三個量度[自訂所有行銷活動中的時間序列趨勢圖](campaign-data-views-manage.md#data-visualizations-manage)。 根據預設，[!UICONTROL Net Spend]、[!UICONTROL Impressions]和[!UICONTROL Net CPM]的資料會包含在個別的圖表（格子圖）中。 您可以選擇變更量度。 若要啟用時間序列趨勢圖中的每小時資料，請將日期選取範圍變更為單日（[!UICONTROL Today]、[!UICONTROL Yesterday]或特定日）。

針對三個量度![個別趨勢圖](/help/dsp/assets/trend-chart-separate.png)

您也可以選擇覆蓋這三個量度，輕鬆偵測異常和區域，藉此改善規模或效能。

![趨勢圖表與覆蓋](/help/dsp/assets/trend-chart.png)

### 表格檢視

![行銷活動清單](/help/dsp/assets/campaigns-list.png)

依預設，每個行銷活動列都包含步調和傳送量度。 步調量度包含[!UICONTROL Gross Spend (Lifetime)]，其中包括對行銷活動中所有套件的實際實際實際目標上支出與預期目標上支出的量度，因此您可以一眼就識別表現不佳的行銷活動。 您可以選擇性[變更資料行檢視](campaign-data-views-manage.md#column-view-change)或甚至[建立自訂資料行檢視](campaign-data-views-manage.md#column-view-create)。

您可以進一步以其他方式[自訂資料表](campaign-data-views-manage.md#data-tables-manage)，並[篩選可見的資料](campaign-data-views-manage.md#filter-data-tables)。

若要檢視行銷活動的詳細資訊，請按一下行銷活動名稱。

#### 警示指示器

「[!UICONTROL Alerts]」欄指出行銷活動或其下的任何子實體何時發生問題。 工具列右側的[!UICONTROL Pulse Panel]圖示也會指出是否有任何警報可供列出的實體使用。 如需詳細資訊，請參閱[檢視警示](campaign-alerts.md)。

## 單一行銷活動報告 {#single-campaign-reporting}

在促銷活動中，您可以根據促銷活動實體來篩選資料： [!UICONTROL Packages]、[!UICONTROL Placements]和[!UICONTROL Ads]。 您可以進一步[篩選可見的資料](campaign-data-views-manage.md#filter-data-tables)，以僅包含您要檢視的封裝、位置或廣告。

![行銷活動實體標籤](/help/dsp/assets/campaign-subtabs.png)

### 圖表檢視

對於每個行銷活動，您可以[使用三個量度（可在每個實體檢視中使用）自訂時間序列趨勢圖](campaign-data-views-manage.md#data-visualizations-manage)。 促銷活動的所有趨勢圖表都會保留相同的量度。

如需詳細資訊，請參閱跨促銷活動量度[&#128279;](#chart-view)的「圖表檢視」區段。

### 表格檢視

每個實體索引標籤中，預設會包含步調和傳送量度，但您可以[變更欄檢視](campaign-data-views-manage.md#column-view-change)，甚至[建立自訂欄檢視](campaign-data-views-manage.md#column-view-create)，以套用至行銷活動的所有子索引標籤。 您可以進一步以其他方式[自訂資料表](campaign-data-views-manage.md#data-tables-manage)。 每個資料表都包含一個[!UICONTROL Subtotals]列，這個列會顯示所有可見列中每個量度的總和或平均值。

#### 警示指示器

「[!UICONTROL Alerts]」欄會指出套件、位置或廣告（或套件或位置下的任何子實體）何時發生問題。 「[!UICONTROL Alerts]」欄指出行銷活動或其下的任何子實體何時發生問題。 工具列右側的[!UICONTROL Pulse Panel]圖示也會指出是否有任何警報可供列出的實體使用。 如需詳細資訊，請參閱[檢視警示](campaign-alerts.md)。

### 其他型別的行銷活動層級報告

針對其他資料劃分，請檢視[行銷活動層級報告頁面](/help/dsp/campaign-management/campaigns/campaign-view-report.md)。 報告包含有關[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]和[!UICONTROL Audience Performance]資料的區段。

### 其他型別的位置層級報表

針對其他資料劃分，請檢視[位置層級報表頁面](/help/dsp/campaign-management/placements/placement-view-report.md)。 報告包含有關[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、[!UICONTROL Audience Performance]、[!UICONTROL Notifications]和[!UICONTROL Ads]資料的區段。

此外，您可以在位置設定中檢視下列資料：

* [A （詳細資料檢視[!UICONTROL Inspector]）](placement-details-view.md)，顯示位置的所有目標網站、廣告、頻率資料和交易。

* [位置預測報告](/help/dsp/campaign-management/reports/placement-forecast.md)。

* [位置診斷報告](/help/dsp/campaign-management/reports/placement-diagnostics.md)。


### 其他型別的廣告層級報告

針對其他資料劃分，請檢視[廣告層級報表頁面](/help/dsp/campaign-management/ads/ad-view-report.md)。 報表包含[!UICONTROL Overview]、[!UICONTROL Geography]和[!UICONTROL Viewability]資料。

>[!MORELIKETHIS]
>
>* [檢視位置](placement-details-view.md)的網站、廣告和頻率詳細資訊
>* [管理您的行銷活動資料檢視](campaign-data-views-manage.md)
>* [從Campaign Management檢視匯出資料](campaign-export-data.md)
>* [檢視行銷活動的詳細報告](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [檢視警示](campaign-alerts.md)
