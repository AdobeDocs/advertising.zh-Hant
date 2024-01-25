---
title: 關於平台內報表
description: 瞭解行銷活動管理檢視中包含的報告資料。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 833e3d3a15546518ec627f859d601285e30381b7
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# 關於平台內報表

<!-- rename "About Performance Reports in Campaign Management Views?" -->
行銷活動管理檢視包含完整的報告資料。 可用的報表可協助您識別執行良好的套件和位置，以及需要您注意的套件和位置。 快速動作按鈕也讓您提高生產力。

## 所有行銷活動檢視

此 [!UICONTROL Campaigns] 檢視會開啟一組效能資料圖表，以及您帳戶中所有行銷活動的清單。

### 圖表檢視 {#chart-view}

您可以 [自訂時間序列趨勢圖](campaign-data-visualization-manage.md) 使用三個量度在所有行銷活動間轉換。 根據預設，資料屬於 [!UICONTROL Net Spend]， [!UICONTROL Impressions]、和 [!UICONTROL Net CPM] 都包含在個別的圖表（格子圖）中。 您可以選擇變更量度。 若要啟用時間序列趨勢圖中的每小時資料，請將日期選取範圍變更為單日([!UICONTROL Today]， [!UICONTROL Yesterday]或特定日期)。

![三個量度的個別趨勢圖](/help/dsp/assets/trend-chart-separate.png)

您也可以選擇覆蓋這三個量度，輕鬆偵測異常和區域，藉此改善規模或效能。

![趨勢圖（含覆蓋）](/help/dsp/assets/trend-chart.png)

### 表格檢視

![行銷活動清單](/help/dsp/assets/campaigns-list.png)

依預設，每個行銷活動列都包含步調和傳送量度。 步調量度包括 [!UICONTROL Gross Spend (Lifetime)]，包括測量行銷活動中所有套件的實際實際目標上支出與預期目標上支出，以便您一眼即可識別表現不佳的行銷活動。 您可以選擇性 [變更欄檢視](column-view-change.md) 或平均 [建立自訂欄檢視](column-view-create.md).

您可以進一步進行 [自訂資料表](campaign-data-views-about.md) 其他方式和 [篩選可見的資料](campaign-data-filter.md).

<!--
An "Alerts" column indicates when a campaign (or any child entity under it) has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

若要檢視行銷活動的詳細資訊，請按一下行銷活動名稱。

## 單一行銷活動報告 {#single-campaign-reporting}

在行銷活動中，您可以根據行銷活動實體來篩選資料： [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads]. 您可以進一步進行 [篩選可見的資料](campaign-data-filter.md) 以僅包含您想要看到的套件、版位或廣告。

![行銷活動實體標籤](/help/dsp/assets/campaign-subtabs.png)

### 圖表檢視

對於每個行銷活動，您可以 [自訂時間序列趨勢圖](campaign-data-visualization-manage.md) 提供三個量度，可在各個實體檢視中使用。 促銷活動的所有趨勢圖表都會保留相同的量度。

請參閱 [跨行銷活動量度的「圖表檢視」區段](#chart-view) 以取得詳細資訊。

### 表格檢視

在每個實體標籤中，預設情況下每一列都包含步調和傳送量度，但您可以 [變更欄檢視](column-view-change.md) 或平均 [建立自訂欄檢視](column-view-create.md) 以套用至促銷活動的所有子標籤。 您可以進一步進行 [自訂資料表](campaign-data-views-about.md) 其他方式。 每個資料表都包含 [!UICONTROL Subtotals] 列，顯示所有可見列中的每個量度之總和或平均值。

<!--
An "Alerts" column indicates when a package, placement, or ad &mdash; or any child entity under a package or placement &mdash; has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

### 刊登 [!UICONTROL Inspector] {#placement-inspector}

對於每個位置，您可以 [開啟（詳細資料檢視） [!UICONTROL Inspector])](placement-details-view.md)，包括下列深入資料：

* **[!UICONTROL Sites]：** 此版位曾有曝光的所有網站。

  此 [!UICONTROL Sites] 索引標籤包含搜尋和篩選功能、在主要頁面上可用的相同標準和自訂欄檢視選項，以及 [!UICONTROL Exclude] 按鈕來快速排除位置。

* **[!UICONTROL Ads]：** 位置中的所有廣告。

  此 [!UICONTROL Ads] 索引標籤包括搜尋和篩選功能、主要頁面上可用的相同標準和自訂欄檢視選項，以及每列中的快速動作按鈕，例如 [!UICONTROL Pause] （讓您可以快速暫停廣告）。

* **[!UICONTROL Frequency]：** 此投放位置的每個廣告頻率層級的資料，包括：
   * 廣告頻率層級（例如「1」，適用於使用者看過一次廣告的所有例項）
   * 裝置/瀏覽器或人員的預估不重複數量(視指定的 [!UICONTROL Cross Device Level] （適用於促銷活動）在指定頻率層級收到曝光數
   * 指定頻率層級的預估曝光次數
   * 指定頻率等級的預估平均頻率。 此值等於（預估曝光次數）/（預估不重複值）。

* **[!UICONTROL Inventory]：** 此位置所定位之所有交易的資訊。

  此 [!UICONTROL Inventory] 索引標籤可讓您透過顯示效能統計資料來快速進行疑難排解，例如 [!UICONTROL Auctions]， [!UICONTROL Bids]、和 [!UICONTROL Win Rate]. 索引標籤包括搜尋和篩選功能、主要頁面上可用的相同標準和自訂欄檢視選項，以及每列中的快速動作按鈕，包括 [!UICONTROL Edit]， [!UICONTROL View Report]、和 [[!UICONTROL Auction Insights] 以取得進一步的疑難排解](/help/dsp/inventory/private-deal-auction-insights.md).

#### 疑難排解詳細目錄

| 問題 | 可能的原因 | 要採取的動作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 發佈者尚未開始傳送競標要求。 | 請連絡發佈商以啟動交易。 |
| | 交易設定不正確，例如輸入不正確的外部交易ID。 | 確認交易詳細資料並編輯交易。 |
| [!UICONTROL Auctions but no Bids] | 位置鎖定目標不符合交易的傳入競標要求。 <br><br> 例如，刊登版位可能會將目標定位為不符合交易資格的地理位置。 | 視需要編輯位置目標，以避免目標錯配。 |
| | 投放位置沒有有效的廣告，且該廣告具有交易所需的媒體型別。 | 建立並附加具有正確媒體型別的廣告至投放位置。 |
| | 位置沒有足夠的預算。 | 增加版位預算以允許對傳入的請求投標。 |
| | 刊登投放日期與交易的曝光傳送日期不重疊。 | 視需要編輯位置的投放日期。 |
| [!UICONTROL Low Win Rate] | 位置的最高出價（下限或固定）低於交易要求的最低出價。 | 增加投放位置的 [!UICONTROL Max Bid] 視需要。 |
| | 此位置使用限制競標的競標前篩選條件。 | 降低競標前篩選器的臨界值，以允許更多競標。 |
| | 此位置的對象鎖定目標太嚴格。 | 檢查指定的對象目標是否有足夠的活躍使用者，並儘可能展開對象。 |

![位置檢測器](/help/dsp/assets/placement-inspector.png)

您可以將資料匯出 [!UICONTROL Sites]， [!UICONTROL Ads]，或 [!UICONTROL Frequency] 定位至瀏覽器的預設下載資料夾，作為XLSM格式的報表。

### 其他型別的行銷活動層級報告

對於其他資料劃分，檢視 [行銷活動層級報告頁面](/help/dsp/campaign-management/campaigns/campaign-view-report.md). 此 <!--legacy --> 報告包含下列區段： [!UICONTROL Geography]， [!UICONTROL Device]， [!UICONTROL Viewability]、和 [!UICONTROL Audience Performance] 資料。

>[!MORELIKETHIS]
>
>* [檢視位置的網站、廣告和頻率詳細資訊](placement-details-view.md)
>* [關於Campaign資料檢視](campaign-data-views-about.md)
>* [建立自訂欄檢視](column-view-create.md)
>* [變更欄檢視](column-view-change.md)
>* [管理資料視覺效果](campaign-data-visualization-manage.md)
>* [從Campaign Management檢視匯出資料](campaign-export-data.md)
>* [檢視行銷活動的詳細報告](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
