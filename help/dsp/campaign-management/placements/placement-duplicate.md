---
title: 重複放置
description: 瞭解如何複製一個或多個放置。
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# 重複放置

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

複製一個或多個放置以建立具有類似設定的放置。 您可以：

* 建立多個位置重複項
* 在原始廣告商和廣告活動中或在不同廣告商和廣告活動中重複放置
* （用於原始市場活動中的重複投放）（可選）複製原始廣告
* 修改新放置的狀態和飛行日期

請參閱「」[未複製的內容](#placement-not-duplicated)「 」，以查看未複製的放置設定清單。

1. 在主菜單中，按一下 **[!UICONTROL Campaigns]**。

1. 按一下市場活動的名稱。

1. 在子菜單中，按一下 **[!UICONTROL Placements]**。

1. 執行下列任一操作：

   * 要複製一個位置，請按一下  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** 的子菜單。

   * 要複製多個放置：

      1. 選中每個要複製的放置旁邊的複選框。

      1. 在批量操作工具欄中，按一下 **[!UICONTROL Duplicate]**。

1. 指定新放置設定：

   1. （單次放置）輸入新放置名稱。

   1. 在 **[!UICONTROL Choose Package (Required)]** 菜單，選擇父包或**[!UICONTROL No package]*。

   1. （可選）更改預設設定。

   設定適用於所有選定的放置。

   預設情況下，新投放是針對原始廣告類型的，被分配給原始廣告主和廣告活動，具有從當天開始的飛行時間表，被暫停，並且不包括原始廣告。

   建立多個放置時，新放置名稱會按順序使用約定&lt;*原始_放置名稱#N*>，例如「我的職位安排#2」。

1. 按一下 **[!UICONTROL Submit]**.

## 未複製的內容 {#placement-not-duplicated}

原始放置中的所有設定都重複，但：

* 實驗設定
* （如果更改航班日期）自定義廣告計畫
* （如果不附加廣告）自定義廣告權重和時間安排
* 計畫保證(PG)交易的預設放置和 [!UICONTROL Simple Ad Serving] 交易
* （如果您將職位安排複製到其他市場活動）:
   * 地理目標
   * 事件像素
   * 廣告
   * 位置級 [!DNL DoubleVerify Authentic Brand Safety] 段（覆蓋廣告商級段）

>[!MORELIKETHIS]
>
>* [關於放置管理](placement-about.md)
>* [建立放置](placement-create.md)
>* [編輯放置](placement-edit.md)
>* [查看放置的更改日誌](placement-change-log.md)
>* [放置設定](placement-settings.md)

