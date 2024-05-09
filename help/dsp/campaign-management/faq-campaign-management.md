---
title: Campaign Management常見問題集
description: 進一步瞭解行銷活動管理，包括變更的延遲期間，以及您在航班期間變更預算時會發生什麼事。
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Campaign Management常見問題集

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 設定變更的延遲

* 當您變更位置或封裝設定時，變更何時生效？

  設定變更通常會立即生效，但最多可能需要12小時的時間。

  如果這是交貨的最後一天，請在當天早些時候進行變更，以便DSP有充足的時間根據變更重新校準套件。 例如，如果您從偶數步調變更為前載步調，DSP需要重新評估其如何分配在剩餘的飛行期間的支出。 如果您在航班的最後一天只剩一小時可送達，請勿進行這類變更。

## 飛行中預算更新

* 當您變更版位時，DSP需要多久才能重新分配套件預算？

  預算配置是以位置績效為基礎，使用14天平均評估。 只有在14天平均期間造成績效變更時，對刊登位置的變更才會導致預算配置變更。

  當發生效能變更時，DSP會在下一個預算最佳化週期(大約在行銷活動時區的午夜(00:00))期間，在版位之間相應地重新分配套件預算。

* 從封裝中移除版位並新增至另一個封裝時，如何重新分配預算？

  版位的整個花費歷史記錄會附加至版位，並隨其從封裝移至封裝。

  當您從套件中移除版位時，套件將不再具有任何版位支出的歷史記錄。 套件預算會變成（套件預算 — 已移除版位預算） /剩餘的投放時間間隔。 然後，套件預算會分配至套件中剩餘的版位。

  同樣地，如果您將相同版位新增至不同的套件，DSP會在為新套件中的所有版位分配預算時，考量版位的支出歷史記錄。

* 套件步調在航班最後一天會有何改變？

  在航班的最後一天，該日會從24小時縮短為23小時，這樣就不會超出套件預算。 此外，套件的步調填充策略會自動變更為&quot;[!UICONTROL Frontload]，」，即使它設定為「[!UICONTROL even].」 這表示每日預算的65%應於東部標準時間上午11:30前送達。

>[!MORELIKETHIS]
>
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)
