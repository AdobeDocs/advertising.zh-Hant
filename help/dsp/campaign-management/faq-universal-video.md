---
title: 關於通用視頻的常見問題
description: 瞭解有關通用視頻廣告的更多資訊。
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 關於通用視頻的常見問題

[通用視頻廣告](/help/dsp/campaign-management/ads/ad-about.md#ad-types) 允許您使用單個視頻放置，從案頭、移動和連接電視環境中為VPAID和VAST清點目標視頻清點。

## 如何建立通用視頻放映和廣告？

通用視頻廣告只能包含通用視頻廣告，通用視頻廣告只能附加到通用視頻廣告。

建立通用視頻放映和廣告，與建立其他類型的放映和視頻的方式類似：

1. 在所需的活動中， [建立通用視頻放置](/help/dsp/campaign-management/placements/placement-create.md)，選擇 [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**。

   您必須至少指定一個目標環境（案頭、移動、連接的電視）。

1. 在和普及視頻播放一樣的運動中， [建立單個通用視頻廣告](/help/dsp/campaign-management/ads/ad-create.md) 或 [建立多個通用視頻廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

   如果建立多個廣告，請確保指定「」[!UICONTROL Universal Video]的 [!UICONTROL Ad Type]:

   * 對於 [!DNL Google] 或 [!DNL Flashtalking] 廣告：在[!UICONTROL Review ad types]&quot;上載檔案後，按一下 **[!UICONTROL Ad Type]** 選擇 **[!UICONTROL Universal Video]**。

   * 對於其他類型的廣告標籤：在您上載的電子錶格檔案中，將每個廣告的「廣告類型」欄位指定為 **[!UICONTROL Universal Video]**。

1. [開啟廣告設定](/help/dsp/campaign-management/ads/ad-edit.md) 為每個新廣告選擇適用的視頻格式：

   * **[!UICONTROL VPAID]:** 可視性始終被測量。
   * **[!UICONTROL VPAID & VAST (Default)]:** 包括不允許可查看性度量的庫存。
   * **[!UICONTROL VAST]**  — 適合連接電視清點。

   請參閱「」[通用視頻廣告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)的雙曲餘切值。

1. [附加新的通用視頻廣告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) 全能視頻放置。

## 選擇連接電視環境進行通用視頻放置時，為什麼某些優化目標和包不可用？

通用視頻放置中的連接電視環境不支援與標準連接電視放置不相容的目標，如每點擊最低成本。 同樣，具有不相容優化目標的包也不可用於選擇。

## 何時 **[!UICONTROL VAST]** 視頻格式用於通用視頻廣告？

使用 **[!UICONTROL VAST]** 下列任何一種情況：

* 放置目標是連接的電視清單。
* 該放置針對來自Google廣告經理、Appnexus、SpotX或Freewheel的視頻清點。 這些SSP不支援VPAID和VAST視頻格式。

## 是否可以將多個通用視頻廣告附加到同一通用視頻放置？

是的。
