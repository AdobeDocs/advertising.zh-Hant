---
title: 產生基本報表或進階報表
description: 瞭解如何產生自訂的基本或進階報告。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 產生基本報表或進階報表

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Create Report]**，將游標停留在上方 **[!UICONTROL Basic Reports]** 或 **[!UICONTROL Advanced Reports]**，然後按一下 [報告型別](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. （選用）在 [!UICONTROL Report Settings] 視窗，變更預設值 [報告設定](basic-advanced-report-settings.md)：

   1. （可選）輸入報表和範本的自訂名稱（如果您將報表另存為範本）。

   1. （可選）若要將報表設定儲存為範本，請選取旁邊的核取方塊 **[!UICONTROL Save as template]**.

   1. （選用）在 **[!UICONTROL Basic Settings]** 標籤中，選取現有報表範本以使用或變更報表的預設基本設定。

   1. （可選）按一下 **[!UICONTROL Columns tab]**，並變更報表中的預設欄。

      預設情況下，報表中的所有貨幣資料都會以美元的格式顯示（例如1,000.00）。 若要以正確的貨幣格式顯示值（但不含CSV和TSV格式的任何貨幣符號），請新增&quot;[!UICONTROL Currency]」欄放入報表。 如果報表包含使用不同貨幣的帳戶資料，則任何「[!UICONTROL Total]「貨幣值是欄中所有數字的總和，不考慮貨幣。

   1. (選擇性； [!UICONTROL Campaign Report]， [!UICONTROL Ad Group Report]， [!UICONTROL Ad Variation Report]， [!UICONTROL Keyword Report]、和 [!UICONTROL Label Classification Report] 僅限)按一下 **[!UICONTROL Classifications]** 標籤，並將報表結果限製為僅包含特定標籤分類。

   1. （可選）按一下 **[!UICONTROL Advanced Filters]** 標籤，並變更預設進階選項。

   1. （可選）按一下 **[!UICONTROL Attribution]** 標籤，並變更預設歸因規則。

   1. （可選）按一下 **[!UICONTROL Scheduling and Delivery]** 標籤，並變更預設的排程和傳送選項。

1. （可用時為選用）若要預覽報表的前50行，請按一下 **[!UICONTROL Preview]**. 完成後，按一下 **[!UICONTROL Back]** 以返回「報表設定」頁面。

   >[!NOTE]
   >
   >「預覽」按鈕適用於所有基本和進階報表，但 [!UICONTROL Campaign Hourly Report]， [!UICONTROL Ad Variation Report]， [!UICONTROL Keyword Report]， [!UICONTROL Domain Referral Report]、和 [!UICONTROL Transaction Report].

1. 按一下 **[!UICONTROL Create]**.

如果您未指定報表排程，則會立即執行報表；否則，會根據指定的排程執行。 報表名稱會新增至 [[!UICONTROL Latest Reports] 檢視](/help/search-social-commerce/reports/report-about.md). 如果您將報表另存為範本，它也會新增至 [[!UICONTROL Templates] 檢視](/help/search-social-commerce/reports/report-about.md). 報告完成時，檔案可供開啟或儲存；範本可立即使用。

如果您輸入了任何電子郵件地址作為通知，每個收件者都會在報告工作完成或失敗時收到通知(根據使用者的 [已設定的通知設定](/help/search-social-commerce/notifications/notification-edit.md) （報表）。

>[!MORELIKETHIS]
>
>* [關於基本和進階報告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [基本和進階報表設定](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [基本和進階報表的報表欄](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [刪除報告](/help/search-social-commerce/reports/management/report-delete.md)

