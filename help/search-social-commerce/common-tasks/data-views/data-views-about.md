---
title: 關於自訂行銷活動管理檢視中的資料
description: 瞭解您可以在行銷活動資料檢視中自訂的資料型別。
exl-id: 89f36865-9275-494e-ac33-d41fa30faa2a
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/PnBql37yqK03DWH2OhLf8hnCBPOwFAVZxD65NNZu0VU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 2f170883b2876ea4a7b39e814df598d337f7ca07
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---
# 關於自訂行銷活動管理檢視中的資料

在大多數行銷活動資料檢視中，您可以自訂顯示在資料表格中的資料。 您可以透過下列方式自訂資料：

* [編輯特定實體檢視（例如[!UICONTROL Campaigns]）之整個預設檢視的設定](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md##view-edit)，以包含特定欄順序、篩選器、日期範圍、歸因規則等，並暫時套用設定或儲存它們。 您也可以[建立其他自訂檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#create-custom-view)、[複製現有檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#view-clone)和[套用任何檢視](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#apply-a-default-or-custom-view)。

* [使用工具列中的[!UICONTROL Custom Columns]控制項變更資料行及其排序順序](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md)。 在新的UI中，如果工具列太窄而無法顯示控制項，請按一下&#x200B;**[!UICONTROL Actions]>[!UICONTROL Custom Columns]**。 您也可以從檢視中的任何欄標題快速[只變更欄](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md)。

* （僅舊版使用者介面） [從左側導覽面板](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/filter-using-left-panel.md)，您可以：

  * 依廣告網路瀏覽或搜尋實體，並依實體的狀態以及帳戶、行銷活動及廣告群組或廣告集的狀態進行篩選。 按一下面板中的任何實體或實體群組可載入子實體的檢視（例如，按一下促銷活動名稱可檢視其子廣告群組）。

  * 依投資組合或投資組合群組瀏覽或搜尋行銷活動，並按實體的狀態以及投資組合群組、投資組合和行銷活動的狀態進行篩選。 按一下面板中的任何投資組合群組、投資組合或促銷活動，可在目前實體檢視中載入投資組合群組、投資組合或促銷活動的資料。

  * 存取、編輯和重設您的預設檢視；以及存取、編輯和刪除您的自訂檢視。 按一下任何檢視名稱即可載入適當的檢視。

* 對任何可用的資料欄套用篩選器，以變更顯示在目前索引標籤上的資料。 您可以從欄標題[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)建立篩選器[，或從工具列](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)上的按鈕建立。 對於行銷活動管理檢視，當您開啟子實體時，會適當地維護篩選器。 例如，如果您檢視有\> 100次點按的行銷活動，然後在該行銷活動中開啟廣告群組，則只會顯示有\> 100次點按的廣告群組。

* [變更您尚未儲存特定日期範圍的所有預設和自訂檢視中使用的日期範圍](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md)。

* [根據特定資料行中的值重新排序資料](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-sort.md)。

* 控制是否要在任何頁面底部顯示25列、50列、100列、（僅舊版使用者介面） 200列或（僅舊版使用者介面） [!UICONTROL Continuous Scroll]。

<!--

## (New UI) Data table tools {#grid-controls-new-ui}

In applicable management views, the toolbar includes the following controls:

* On the left, the [!UICONTROL Filter] control appears before grid search. Where supported, the [!UICONTROL Conversion based on] selector follows search and lets you select [!UICONTROL Click Date] or [!UICONTROL Transaction Date].

* On the right, operational actions, such as [!UICONTROL Reports], appear alongside view and display controls. The available controls depend on the view and your permissions.

* When the available width is reduced, controls move into the [!UICONTROL Actions] menu. This can happen when you narrow the window or open the AI Assistant panel. If a control isn't visible in the toolbar, look for it in [!UICONTROL Actions]. In wider layouts, controls remain inline.

* Within [!UICONTROL Actions], a horizontal divider separates operational actions from view and display controls, such as the current view, [!UICONTROL Custom Columns], [!UICONTROL Compressed Mode], and [!UICONTROL Charts], where available.

* The primary create button remains outside [!UICONTROL Actions].

The [!UICONTROL Refresh] icon is beside the page title in applicable views. The date range control is in the page header. For instructions on comparing two date ranges and changing the comparison format, see "[Filter data by date range](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)."

### Change the grid density

* Where available, click **[!UICONTROL Compressed Mode]** in the toolbar or **[!UICONTROL Actions]** menu to turn compact grid spacing on or off.

  The toolbar button is selected when compressed mode is on. In [!UICONTROL Actions], a switch indicates the current state.

### Show or hide charts

* Where available, click **[!UICONTROL Charts]** in the toolbar or **[!UICONTROL Actions]** menu.

  The toolbar button is selected when charts are shown. In [!UICONTROL Actions], a switch indicates whether charts are shown. Click the control again to hide the charts.

-->
