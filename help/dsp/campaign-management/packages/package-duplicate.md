---
title: 複製包
description: 瞭解如何複製包。
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 複製包

複製包以建立具有類似設定的包。 您可以：

* 在原始廣告商和活動中或在不同的廣告商中複製包
* （可選）複製包中的放置
* （對於原始市場活動中的重複包）可選地複製原始廣告和放置級事件像素
* 修改新包的航班日期

請參閱「」[未複製的內容](#package-not-duplicated)「 」，以查看未複製的放置設定清單。

1. 在主菜單中，按一下 **[!UICONTROL Campaigns]**。

1. 按一下市場活動的名稱以開啟 [!UICONTROL Packages] 的子菜單。

1. 在包名稱旁邊，按一下  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

1. 指定新包設定：

   1. 輸入新包名稱。

   1. （可選）更改預設設定。

      預設情況下：

      * 新包被分配給原始廣告商和活動。

      * 新包在當天處於活動狀態。<!-- and the flight continues for NN  days. -->

      * 原始包中的放置將被複製到新包中。

      * 廣告和放置級事件像素不會複製到新包中。

1. 按一下 **[!UICONTROL Submit]**.

## 未複製的內容 {#package-not-duplicated}

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
>* [關於包管理](package-about.md)
>* [建立包](package-create.md)
>* [編輯包](package-edit.md)
>* [查看包的更改日誌](package-change-log.md)
>* [包設定](package-settings.md)

