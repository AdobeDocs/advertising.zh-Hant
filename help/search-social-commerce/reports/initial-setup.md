---
title: 報告的初始設定任務
description: 瞭解如何在報告中提供量度，以及如何自動化報告。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# 報告的初始設定任務

新使用者應執行下列初始設定工作：

* 建立Adobe廣告正在追蹤的廣告商交易屬性 [可用於報告和其他檢視](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md)，並可選擇使用 [重新命名任何屬性名稱](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 欄標題中顯示的文章內容，以方便閱讀。

   除非您特別指定使用交易屬性，否則報表無法使用這些屬性。

   如果您稍後開始追蹤新的交易屬性，則需要重複此工作。

* （選用）自動化報表產生：

   * 如果您想要定期產生特定時間增量的報表資料，例如 [!UICONTROL Campaign Report] 若為上一週或過去30天，則您可設定 [報告範本](/help/search-social-commerce/reports/automation/templates/template-about.md) 並排程它們每天或在一週或一個月的特定日期執行。 每次排程執行報告時，都會產生新報告。 報表完成後，您可以選擇根據電子郵件通知特定Search、Social和Commerce使用者的電子郵件地址。 [通知設定已設定於 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 如果您想要在自訂格式試算表中檢視最新的每日報表資料，無論是否包含樞紐分析表以及您需要執行進一步計算的任何其他欄，則可以設定每日 [試算表摘要](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). 試算表摘要會每天更新為最新的效能資料，並繼續保留之前日期的資料。 若要設定試算表摘要，您必須先在中建立自訂的試算表範本 [!DNL Microsoft Excel]. 您可以選擇在摘要檔案可用時根據以下內容通知特定Search、Social和Commerce使用者的電子郵件地址 [通知設定已設定於 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 如果您想在FTP位置接收基本和進階報表，則可設定 [以ftp存取基本和進階報表](/help/search-social-commerce/reports/automation/ftp-reports.md) 透過請求FTP帳戶並使用特定命名慣例設定報表範本。

>[!MORELIKETHIS]
>
>* [關於報表](report-about.md)
>* [用於報表的資料](data-used-for-reports.md)

