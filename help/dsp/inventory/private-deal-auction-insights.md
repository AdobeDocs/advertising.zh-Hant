---
title: 檢視私人交易的拍賣深入分析
description: 瞭解如何使用拍賣深入分析來分析私人交易的交易組成。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: bbb99f6a-0276-4eb8-9607-75500d5634d9
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 檢視私人交易的拍賣深入分析

Auction Insights是疑難排解工具，可讓您分析已保證和未保證私人交易的交易組成。 此工具使用資料視覺效果顯示特定時段內[主要拍賣屬性](#auction-attributes)收到的值的趨勢和相對比例。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在交易列中，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Auction Insights]**。

>[!NOTE]
>
>也可以透過版位[!UICONTROL Inspector]工具取得Auction Insights。 若要開啟這些位置，請[開啟位置[!UICONTROL Inspector]](/help/dsp/campaign-management/reports/placement-details-view.md)至[!UICONTROL Inventory tab]，然後按一下交易列中的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Auction Insights]**。

## 拍賣屬性 {#auction-attributes}

區域圖可用於下列拍賣屬性：

* **廣告型別：**&#x200B;拍賣中要求的廣告型別（例如顯示或音訊）。

* **瀏覽器：**&#x200B;拍賣來源瀏覽器(例如Chrome或Firefox)。

* **OS：**&#x200B;拍賣來源作業系統(OS) (例如Android或iOS)。

* **裝置型別：**&#x200B;拍賣來源的裝置（例如行動電話或桌上型電腦）。

* **廣告持續時間：**&#x200B;拍賣中要求的廣告持續時間上限（例如15秒或30秒）。

* **安全：**&#x200B;代表拍賣是否需要安全的HTTPS URL創意資產。 值： <i>安全</i>或<i>不安全</i>。

* **Mime型別：**&#x200B;拍賣中要求的廣告創意MIME型別（例如mp4或mov）。

![拍賣深入分析](/help/dsp/assets/auction-insights.png)

>[!NOTE]
>
>您可以套用特定屬性值的篩選條件來縮小結果的範圍。

>[!MORELIKETHIS]
>
>* [關於私人詳細目錄](private-inventory-about.md)
>* [指定交易ID的位置和廣告](deal-id-attach-placements.md)
>* [檢視交易的詳細報告](deal-view-report.md)
>* Campaign Management檢視中的[效能報表型別](/help/dsp/campaign-management/reports/campaign-reports-about.md)
