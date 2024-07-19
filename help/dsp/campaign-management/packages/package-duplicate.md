---
title: 複製套裝
description: 瞭解如何複製套件。
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 複製套裝

複製套件以建立具有類似設定的套件。 您可以：

* 在原始廣告商和行銷活動或不同行銷活動內複製套件
* 選擇性地複製封裝內的版位
* （適用於原始行銷活動內的重複套件）可選擇複製原始廣告和版位層級的事件畫素
* 修改新套件的投放日期

如需未複製的位置設定清單，請參閱&quot;[未複製的專案](#package-not-duplicated)&quot;。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱以開啟[!UICONTROL Packages]檢視。

1. 在封裝名稱旁，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

1. 指定新的封裝設定：

   1. 輸入新封裝名稱。

   1. （選用）變更預設設定。

      根據預設：

      * 新套件會指派給原始廣告商和促銷活動。

      * 新封裝會在當天生效。<!-- and the flight continues for NN  days. -->

      * 原始套件中的版位會複製到新套件。

      * 廣告和版位層級事件畫素不會複製到新封裝。

1. 按一下&#x200B;**[!UICONTROL Submit]**。

## 未複製的內容 {#package-not-duplicated}

來自原始版位的所有設定都會重複，除了：

* 實驗設定
* （如果您變更投放日期）自訂廣告排程
* （如果您未附加廣告）自訂廣告加權和排程
* 程式化預留(PG)交易的預設刊登版位和[!UICONTROL Simple Ad Serving]交易的刊登版位
* （如果復製版位至其他行銷活動）：
   * 地理目標
   * 事件畫素
   * 廣告
   * 位置層級[!DNL DoubleVerify Authentic Brand Safety]區段（覆寫廣告商層級區段）

>[!MORELIKETHIS]
>
>* [關於封裝管理](package-about.md)
>* [建立封裝](package-create.md)
>* [編輯封裝](package-edit.md)
>* [檢視封裝的變更記錄](package-change-log.md)
>* [封裝設定](package-settings.md)
