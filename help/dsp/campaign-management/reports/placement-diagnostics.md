---
title: 檢視位置診斷報告
description: 瞭解如何診斷版位設定和步調的問題。
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 檢視位置診斷報告

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

一旦行銷活動上線，診斷報告可協助您診斷位置設定和步調的問題。

## 位置診斷報表中的資訊

* **[!UICONTROL Change Log]：**&#x200B;顯示金鑰位置設定的變更，例如名稱、狀態和最高出價。 每個專案都包含變更者的日期和使用者名稱。

* **[!UICONTROL Ad Approvals]：**&#x200B;顯示詳細目錄提供者是否核准或拒絕廣告。 您可以選擇變更任何廣告的狀態（例如，暫停已拒絕的廣告）或開啟廣告設定。

* **[!UICONTROL Non Bids]：**&#x200B;顯示DSP未對位置競標的原因。

## 開啟位置診斷報告

1. 開啟「診斷」報告：

   1. 開啟位置設定：

      1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

      1. 按一下行銷活動的名稱，然後按一下&#x200B;**[!UICONTROL Placements]**。

      1. 在位置名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Edit]**」。

   1. 按一下右上角的![放置診斷](/help/dsp/assets/placement-diagnostics.png)。

1. 執行下列任一項作業：

   * 若要檢視變更記錄：

      1. 按一下&#x200B;**[!UICONTROL Change Log]**。

      1. （可選）篩選報表結果：

         * 在日期功能表中，將報告期間從預設的「最近14天」變更為另一個期間（*[!UICONTROL Last 30 days]、* *[!UICONTROL Last 60 days]、* *[!UICONTROL Last 90 days]、*&#x200B;或&#x200B;*[!UICONTROL Last 1 year]*）。

         * 在左側功能表中，依特定使用者名稱篩選報表。

         * 在右側功能表中，依特定位置設定篩選報表。

   * 若要檢視廣告核准的狀態：

      1. 按一下右上角的&#x200B;**[!UICONTROL Ad Approvals]**。

      1. （選擇性）若要暫停或啟用廣告，請按一下「廣告」欄中的狀態引數（![狀態引數](/help/dsp/assets/status-switch.png)）。

      1. （選擇性）若要開啟廣告的設定，請按一下廣告旁的&#x200B;**[!UICONTROL View Ad]**。

   * 若要瞭解DSP為何沒有對位置競標：

      1. 按一下右上角的&#x200B;**[!UICONTROL Non Bids]**。

      1. （選用）若要依特定私人交易目標篩選位置，請選取交易。<!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. （可選）若要變更日期範圍，請按一下日期欄位，然後選取不同的日期或日期範圍。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* Campaign Management檢視中的[效能報表型別](campaign-reports-about.md)
>* [檢視刊登版位預測報告](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
