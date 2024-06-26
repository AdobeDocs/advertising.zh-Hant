---
title: 報告的初始設定任務
description: 瞭解如何在報表中使用量度，以及如何自動化報表。
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 報告的初始設定任務

新使用者應該執行下列初始設定工作：

* 建立Adobe Advertising正在追蹤廣告商的轉換量度 [可用於報告和其他檢視](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)，並可選擇使用 [重新命名任何轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md會顯示在欄標題中，以供閱讀。

  除非您特別指定使用交易屬性，否則報表無法使用這些屬性。

  如果您稍後開始追蹤新的轉換量度，則必須重複此工作。

* （選用）自動化報表產生：

   * 如果您想要定期產生特定時間增量的報表資料，例如 [!UICONTROL Campaign Report] 針對上週或過去30天，您可以設定 [報告範本](/help/search-social-commerce/reports/automation/templates/template-about.md) 並排程每天或一週或一月中的特定日執行它們。 每次計畫執行報告時，都會產生新報告。 您可以選擇在報表完成後，根據電子郵件通知特定搜尋、社交和Commerce使用者的電子郵件地址 [通知設定已設定於 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 如果您想要在自訂格式試算表中檢視最新的每日報表資料，無論是否包含樞紐分析表以及您需要執行進一步計算的任何其他欄，則可以設定每日 [試算表摘要](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). 試算表摘要每天都會以最新的效能資料更新，並繼續保留之前日期的資料。 若要設定試算表摘要，您必須先在中建立自訂試算表範本 [!DNL Microsoft Excel]. 您可選擇在摘要檔案可供使用時，根據以下專案通知特定搜尋、社交和Commerce使用者的電子郵件地址 [通知設定已設定於 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 如果您想在FTP位置接收基本和進階報表，則可設定 [以ftp存取基本和進階報表](/help/search-social-commerce/reports/automation/ftp-reports.md) 透過請求FTP帳戶並使用特定命名慣例設定報表範本。

>[!MORELIKETHIS]
>
>* [關於報表](report-about.md)
>* [用於報表的資料](data-used-for-reports.md)
