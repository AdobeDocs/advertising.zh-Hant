---
title: （新UI）手動同步處理廣告網路資料
description: 瞭解如何從新的UI手動觸發受支援廣告網路的行銷活動結構和行銷活動實體的同步。
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# （新UI）透過API連線手動同步處理廣告網路資料

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （先前為[!DNL Bing Ads]）、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和現有的[!DNL Baidu]帳戶僅限*

同步是Search、Social和Commerce在[支援的廣告網路](/help/search-social-commerce/introduction/supported-inventory.md)上收集每個廣告商已連線廣告網路帳戶之更新資訊的程式。 此資料包含廣告商的促銷活動結構和促銷活動實體，包括在「搜尋」、「社交」和「Commerce」中管理或報告的大部分屬性。 其中不包含點按資料，也不包含在Search、Social和Commerce外部輸入的競標和競標修飾詞，這些資料會單獨收集。

搜尋、Social和Commerce會每天自動與您的廣告網路帳戶同步（同步）一次，也可在偵測到您其中一個廣告網路上的新促銷活動時同步。 此外，它會立即將所有從「搜尋」、「社交」和「Commerce」內所做的行銷活動資料變更傳送至廣告網路。

您可以手動要求同步處理指定帳戶<!--Not available as of 2/23:  or in specific active and paused campaigns -->中所有使用中及暫停的行銷活動。 此任務會收集廣告網路上新增或變更的實體。

對於具有「[!UICONTROL Auto Update]」選項的促銷活動，同步作業也會產生並張貼在追蹤範本或目的地URL中遺失或需要變更的追蹤代碼。 系統會根據帳戶設定或促銷活動之追蹤設定中的引數產生URL。 如果相關專案有追蹤URL存在，則不會重新產生，除非需要新專案（例如如果關鍵字元合型別、創意文字或帳戶的追蹤引數已變更）。

>[!NOTE]
>
>每當[建立Bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)時，您都可以選擇在建立Bulksheet之前與廣告網路同步。

## 同步廣告網路帳戶中的行銷活動

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 選取帳戶名稱旁的核取方塊。

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**。

   * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

您可以在[!UICONTROL Workspace]檢視中追蹤同步處理工作的狀態。 這項工作可能需要
一小時或更久後才會出現。

>[!MORELIKETHIS]
>
>* [下載/建立Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
