---
title: 通用視訊的常見問題集
description: 深入了解通用視訊廣告。
feature: DSP Placements, DSP Ads
source-git-commit: 17a47e9d7ddb18b36da998d289f949e540beded8
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 通用視訊的常見問題集

[通用視訊廣告](/help/dsp/campaign-management/ads/ad-about.md) 可讓您透過單一視訊位置，從案頭、行動裝置和連線電視環境，針對VPAID和VAST詳細目錄鎖定視訊詳細目錄。

## 如何建立通用視訊版位和廣告？

通用視訊版位只能包含通用視訊廣告，而通用視訊廣告只能附加至通用視訊版位。

建立通用視訊版位和廣告的方式與建立其他版位和視訊類型的方式類似：

1. 在所需的行銷活動中， [建立通用視訊放置](/help/dsp/campaign-management/placements/placement-create.md)，選取 [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   您必須指定至少一個要定位的環境（案頭、行動裝置、連線電視）。

1. 在與通用視訊版位相同的行銷活動中， [建立單一通用視訊廣告](/help/dsp/campaign-management/ads/ad-create.md) 或 [建立多個通用視訊廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   如果您建立多個廣告，請務必指定「[!UICONTROL Universal Video]」作為 [!UICONTROL Ad Type]:

   * 針對 [!DNL Google] 或 [!DNL Flashtalking] 廣告：在「[!UICONTROL Review ad types]上傳檔案後，按一下 **[!UICONTROL Ad Type]** 欄位和選取 **[!UICONTROL Universal Video]**.

   * 對於其他類型的廣告標籤：在您上傳的試算表檔案中，將每個廣告的「廣告類型」欄位指定為 **[!UICONTROL Universal Video]**.

1. [開啟廣告設定](/help/dsp/campaign-management/ads/ad-edit.md) 針對每個新廣告，並選取適用的視訊格式：

   * **[!UICONTROL VPAID]:** 可見度一律測量。
   * **[!UICONTROL VPAID & VAST (Default)]:** 包含不允許檢視度測量的庫存。
   * **[!UICONTROL VAST]**  — 適用於連接電視清點。

   請參閱「[通用視訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)」以取得詳細資訊。

1. [附加新的通用視訊廣告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) 到通用視訊放置。

## 為何選取連線電視環境以進行通用視訊放置時，無法使用某些最佳化目標和套件？

通用視訊版位中的連線電視環境不支援與標準連線電視版位不相容的目標，例如每次點按最低成本。 同樣，具有不相容最佳化目標的套件也無法供選取。

## 何時 **[!UICONTROL VAST]** 通用視訊廣告使用視訊格式？

使用 **[!UICONTROL VAST]** 在下列任一情況下：

* 放置目標是連接的電視清單。
* 此位置會鎖定來自Google廣告管理員、Appnexus、SpotX或Freewheel的視訊詳細目錄。 這些SSP不支援VPAID和VAST視訊格式。

## 可以將多個通用視訊廣告附加至相同的通用視訊位置嗎？

是。
