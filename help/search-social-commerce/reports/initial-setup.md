---
title: 報告的初始設定任務
description: 瞭解如何在報表中使用量度，以及如何自動化報表。
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
TQID: https://experienceleague.adobe.com/N50b-O0oFBV6ZMXcFx8gRvLs3M1hN696d43VGlgkg44
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# 報告的初始設定任務

新使用者應該執行下列初始設定工作：

* 讓Adobe Advertising為廣告商[追蹤的轉換量度可用於報告和其他檢視](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)，並選擇性[重新命名任何轉換量度]&#x200B;(/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md)，這些量度會顯示在欄標題中，以供閱讀。

  除非您特別指定使用交易屬性，否則報表無法使用這些屬性。

  如果您稍後開始追蹤新的轉換量度，則必須重複此工作。

* （選用）自動化報表產生：

   * 如果您想要定期產生特定時間增量的報表資料，例如上週或過去30天的[!UICONTROL Campaign Report]，則可以設定[報表範本](/help/search-social-commerce/reports/automation/templates/template-about.md)，並排程這些範本每天或一週或一月的特定日期執行。 每次計畫執行報告時，都會產生新報告。 您可以選擇在報表完成時，根據[中設定的[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md)通知設定，通知特定Search、Social和Commerce使用者的電子郵件地址。

   * 如果您想要在自訂格式試算表中檢視最新的每日報表資料，無論是否包含樞紐分析表以及您需要執行進一步計算的任何其他欄，則可以設定每日[試算表摘要](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)。 試算表摘要每天都會以最新的效能資料更新，並繼續保留之前日期的資料。 若要設定試算表摘要，您必須先在[!DNL Microsoft Excel]中建立自訂的試算表範本。 您可以選擇根據在[中設定的[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md)通知設定，在摘要檔案可用時通知特定Search、Social和Commerce使用者的電子郵件地址。

   * 如果您想要在FTP位置接收基本和進階報表，則您可以要求FTP帳戶並使用特定命名慣例設定報表範本，以設定[對基本和進階報表的FTP存取](/help/search-social-commerce/reports/automation/ftp-reports.md)。

>[!MORELIKETHIS]
>
>* [關於報告](report-about.md)
>* [用於報告的資料](data-used-for-reports.md)
