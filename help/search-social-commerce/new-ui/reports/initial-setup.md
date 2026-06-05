---
title: （新UI）報表的初始設定任務
description: 瞭解如何在報表中使用量度，以及如何自動化報表。
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# （新UI）報表的初始設定任務

新使用者應該執行下列初始設定工作：

* 讓Adobe Advertising追蹤的廣告商轉換量度可用於報告和其他檢視，並可選擇重新命名欄標題中顯示的任何轉換量度，以方便閱讀。 請參閱&quot;[管理廣告商的轉換量度](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)&quot;。

  除非您特別指定使用交易屬性，否則報表無法使用這些屬性。

  如果您稍後開始追蹤新的轉換量度，則必須重複此工作。

* （選用）自動化報表產生：

   * 如果您想要定期產生特定時間增量的報表資料，例如上週或過去30天的[!UICONTROL Campaign Report]，則可以設定[報表範本](report-templates-manage.md)，並排程這些範本每天或一週或一月的特定日期執行。 每次計畫執行報告時，都會產生新報告。 您可以選擇在報表完成時，根據[!UICONTROL Notification Center]&rbrack;[Manage custom alerts]&#x200B;(/help/search-social-commerce/new-ui/notifications-manage.md)中設定的&lbrack;通知設定，通知特定Search、Social和Commerce使用者的電子郵件地址。

   * 如果您想要在自訂格式試算表中檢視最新的每日報表資料，無論是否包含樞紐分析表以及您需要執行進一步計算的任何其他欄，則可以設定每日[試算表摘要](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)。 試算表摘要每天都會以最新的效能資料更新，並繼續保留之前日期的資料。 若要設定試算表摘要，您必須先在[!DNL Microsoft Excel]中建立自訂的試算表範本。 您可以選擇根據在[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/new-ui/notifications-manage.md)中設定的通知設定，在摘要檔案可用時通知特定Search、Social和Commerce使用者的電子郵件地址。

   * 如果您想要在FTP位置接收基本和進階報表，則您可以要求FTP帳戶並使用特定命名慣例設定報表範本，以設定[對基本和進階報表的FTP存取](/help/search-social-commerce/new-ui/reports/ftp-reports.md)。

>[!MORELIKETHIS]
>
>* [關於報告](report-about.md)
>* [用於報告的資料](data-used-for-reports.md)
