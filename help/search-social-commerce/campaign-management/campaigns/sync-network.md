---
title: 手動同步處理廣告網路資料
description: 瞭解如何針對支援的廣告網路，手動觸發行銷活動結構和行銷活動實體的同步。
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: c4600e6ef41193f09722052ef9b16fe5d07bdaaf
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 手動同步處理廣告網路資料

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （先前為[!DNL Bing Ads]）、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和現有的[!DNL Baidu]帳戶僅限*

同步是Search、Social和Commerce在[支援的廣告網路](/help/search-social-commerce/introduction/supported-inventory.md)上收集每個廣告商已連線廣告網路帳戶之更新資訊的程式。 此資料包含廣告商的促銷活動結構和促銷活動實體，包括在「搜尋」、「社交」和「Commerce」中管理或報告的大部分屬性。 其中不包含點按資料，也不包含在Search、Social和Commerce外部輸入的競標和競標修飾詞，這些資料會單獨收集。

搜尋、Social和Commerce會每天自動與您的廣告網路帳戶同步（同步）一次，也可在偵測到您其中一個廣告網路上的新促銷活動時同步。 此外，它會立即將所有從「搜尋」、「社交」和「Commerce」內所做的行銷活動資料變更傳送至廣告網路。

您可以手動請求同步處理指定帳戶或特定使用中及暫停行銷活動中的所有使用中及暫停的行銷活動。 此任務會收集廣告網路上新增或變更的實體。

對於具有「[!UICONTROL Auto Upload]」選項的促銷活動，同步作業也會產生並張貼在追蹤範本或目的地URL中遺失或需要變更的追蹤代碼。 系統會根據帳戶設定或促銷活動之追蹤設定中的引數產生URL。 如果相關專案有追蹤URL存在，則不會重新產生，除非需要新專案（例如如果關鍵字元合型別、創意文字或帳戶的追蹤引數已變更）。

>[!NOTE]
>
>每當[建立Bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)時，您都可以選擇在建立Bulksheet之前與廣告網路同步。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]>[!UICONTROL Campaigns]**。 在子功能表中，選取&#x200B;**[!UICONTROL Accounts]**&#x200B;以同步特定帳戶中的所有促銷活動，或選取&#x200B;**[!UICONTROL Campaigns]**&#x200B;以同步特定促銷活動。

1. （選用）篩選清單以包含特定帳戶或行銷活動。

1. 選取您要同步之每個帳戶或行銷活動旁的核取方塊。 您一次最多可以同步50個行銷活動。 如果您一次同步超過五個帳戶，工作會分成批次，每個批次最多五個帳戶。

1. 按一下工具列中的&#x200B;![**更多**](/help/search-social-commerce/assets/more.png "&#x200B;更多")，然後選取&#x200B;**[!UICONTROL Sync]**。

您可以在[!UICONTROL Workspace]檢視中追蹤同步處理工作的狀態。 這項工作可能需要
一小時或更久後才會出現。

>[!MORELIKETHIS]
>
>* [下載/建立Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
