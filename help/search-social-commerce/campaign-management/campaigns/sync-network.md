---
title: 手動同步廣告網路資料
description: 瞭解如何手動觸發受支援廣告網路的行銷活動結構和行銷活動實體的同步。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 手動同步廣告網路資料

*[!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft® Advertising] (先前稱為 [!DNL Bing Ads])， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex] 僅限帳戶*

同步是Search、Social和Commerce收集每個廣告商廣告網路帳戶更新資訊的程式。 [支援的廣告網路](/help/search-social-commerce/introduction/supported-inventory.md). 此資料包含廣告商的行銷活動結構和行銷活動實體，包括其在「搜尋」、「社交」和「商務」中管理或報告的大部分屬性。 其中不包含點按資料，也不包含在Search、Social和Commerce外部輸入的競標和競標修飾元（會單獨收集）。

搜尋、Social和Commerce會每天自動與您的廣告網路帳戶同步（同步）一次，並且每當您在其中一個廣告網路偵測到新行銷活動時，也會同步（同步）。 此外，它會立即將搜尋、社交和商務內對行銷活動資料所做的所有變更傳送至廣告網路。

您可以手動要求同步指定帳戶或特定有效和暫停行銷活動中的所有有效和暫停行銷活動。 此任務會收集廣告網路上新增或變更的實體。

針對具有「」的行銷活動[!UICONTROL Auto Upload]」選項，同步作業也會產生並張貼在追蹤範本或目的地URL中遺失或需要變更的追蹤代碼。 系統會根據帳戶設定或行銷活動的追蹤設定中的引數來產生URL。 如果相關專案存在追蹤URL，則除非需要新專案（例如如果關鍵字元合型別、創意文字或帳戶的追蹤引數已變更），否則不會重新產生這些URL。

>[!NOTE]
>
>隨時待命 [建立大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)，您可以選擇在建立大量表單前與廣告網路同步。

1. 在主功能表中，按一下 **[!UICONTROL Search]>[!UICONTROL Campaigns]**. 在子功能表中，選取 **[!UICONTROL Accounts]** 同步特定帳戶中的所有行銷活動，或 **[!UICONTROL Campaigns]** 以同步特定行銷活動。

1. （選用）篩選清單以包含特定帳戶或行銷活動。

1. 選取您要同步的每個帳戶或行銷活動旁的核取方塊。 您一次最多可以同步50個行銷活動。 如果您一次同步超過五個帳戶，工作會分成多個批次，每個批次最多包含五個帳戶。

1. 按一下 **![更多](/help/search-social-commerce/assets/more.png "更多")** 在工具列中，然後選取 **[!UICONTROL Sync]**.

您可以依照以下連結中的同步處理工作狀態： [!UICONTROL Workspace] 檢視。 這項工作可能需要一小時或更久的時間才能顯示。

>[!MORELIKETHIS]
>
>* [下載/建立Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)

