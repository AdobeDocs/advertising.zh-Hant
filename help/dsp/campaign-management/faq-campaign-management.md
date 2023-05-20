---
title: 關於Campaign Management的常見問題
description: 瞭解有關市場活動管理的更多資訊，包括更改的延遲期以及在飛行期間進行預算更改時會發生什麼。
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 2fb3f227d74d8c8893a3cb042ea91121a0fae7c0
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 關於Campaign Management的常見問題

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 設定更改的延遲

* 更改放置或包設定時，更改何時生效？

   設定更改通常會立即生效，但可能需要12小時。

   如果是最後一天，請在當天早上做出更改，DSP以便有充足的時間根據更改來重新調整包。 例如，如果你從起步到前載起步，DSP需要重新評估它在整個飛行剩餘時間的分配方式。 如果在航班最後一天，你只剩1小時的時間交貨，別做這種改變。

## 預算更新中期

* 在對職位安排進行更改時，重新分配DSP包預算需要多長時間？

   預算分配基於職位安排績效，該績效以14天平均數進行評估。 對職位安排的更改只有在導致14天平均時間內的績效變化時，才會導致對預算分配的更改。

   當效能發生更改DSP時，在下一個預算優化週期(大約在市場活動時區的午夜(00:00))期間，相應地將包預算重新分配到職位安排之間。

* 在從包中刪除放置並將其添加到另一個包時，如何重新分配預算？

   放置的整個花費歷史記錄將附加到放置，並隨之從包移動到包。

   從包中刪除放置時，該包不再具有放置的花費歷史記錄。 包預算將變為（包預算 — 已刪除的放置預算）/剩餘飛行時間間隔。 然後，將包預算分配給包中剩餘的放置。

   同樣，如果將相同的放置添加到不同的包DSP中，則在為新包中的所有放置分配預算時，會考慮放置的使用歷史記錄。

* 在航班的最後一天，包裹起步如何改變？

   在航班的最後一天，將一天從24小時縮短到23小時，以免超出包裹預算。 此外，包的調步填充策略會自動更改為「[!UICONTROL Frontload]，即使設定為「[!UICONTROL even]&quot; 這意味著65%的日預算應在美國東部標準時間上午11點30分前交付。

>[!MORELIKETHIS]
>
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [設定績效活動的最佳做法](/help/dsp/optimization/campaign-best-practices-performance.md)

