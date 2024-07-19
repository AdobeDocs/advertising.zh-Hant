---
title: 通用視訊常見問題集
description: 進一步瞭解通用視訊廣告。
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 通用視訊常見問題集

[通用視訊廣告](/help/dsp/campaign-management/ads/ad-about.md#ad-types)可讓您使用單一視訊位置，針對桌上型電腦、行動裝置和連線電視環境的VPAID和VAST視訊詳細目錄設定目標。

## 如何建立通用視訊版位和廣告？

通用視訊版位只能包含通用視訊廣告，而通用視訊廣告只能附加至通用視訊版位。

建立通用視訊版位和廣告的方式，與建立其他型別的版位和視訊類似：

1. 在所需的行銷活動中，[建立通用視訊位置](/help/dsp/campaign-management/placements/placement-create.md)，選取[!UICONTROL Placement Type] **[!UICONTROL Universal Video]**。

   您必須至少指定一個要定位的環境（桌上型電腦、行動裝置、連線電視）。

1. 在與通用視訊版位相同的行銷活動中，[建立單一通用視訊廣告](/help/dsp/campaign-management/ads/ad-create.md)或[建立多個通用視訊廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

   如果您建立多個廣告，請務必指定&quot;[!UICONTROL Universal Video]&quot;為[!UICONTROL Ad Type]：

   * 針對[!DNL Google]或[!DNL Flashtalking]廣告：在您上傳檔案之後的&quot;[!UICONTROL Review ad types]&quot;步驟中，按一下「**[!UICONTROL Ad Type]**」欄位並選取&#x200B;**[!UICONTROL Universal Video]**。

   * 對於其他型別的廣告標籤：在您上傳的試算表檔案中，將每個廣告的「廣告型別」欄位指定為&#x200B;**[!UICONTROL Universal Video]**。

1. [開啟每個新廣告的廣告設定](/help/dsp/campaign-management/ads/ad-edit.md)，並選取適用的視訊格式：

   * **[!UICONTROL VPAID]：**&#x200B;可檢視度一律會測量。
   * **[!UICONTROL VPAID & VAST (Default)]：**&#x200B;包含不允許可檢視度測量的詳細目錄。
   * **[!UICONTROL VAST]** — 適用於連線電視清查。

   如需詳細資訊，請參閱[通用視訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)。

1. [將新的通用視訊廣告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)附加至通用視訊位置。

## 為什麼在選取連線電視環境進行通用視訊放置時，某些最佳化目標和套件無法使用？

與標準連線電視位置不相容的目標（例如「最低每次點按成本」），在通用視訊位置中的連線電視環境不受支援。 同樣地，具有不相容最佳化目標的套件也無法選取。

## **[!UICONTROL VAST]**&#x200B;視訊格式何時應該用於通用視訊廣告？

在下列任一情況下使用&#x200B;**[!UICONTROL VAST]**：

* 此位置會鎖定連線電視的詳細目錄。
* 此版位會鎖定來自Google Ad Manager、Appnexus、SpotX或Freewheel的視訊詳細目錄。 這些SSP不支援VPAID &amp; VAST視訊格式。

## 是否可以將多個通用視訊廣告附加至相同的通用視訊位置？

是。
