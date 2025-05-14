---
title: 復製版位
description: 瞭解如何複製一或多個刊登版位。
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# 復製版位

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

複製一或多個版位，以使用類似設定建立版位。 您可以：

* 為版位製作多個重複專案
* 在原始廣告商和行銷活動內或不同廣告商和行銷活動內復製版位
* （適用於原始行銷活動中的重複版位）可選擇複製原始廣告
* 修改新刊登版位的狀態與投放日期

如需未複製的位置設定清單，請參閱&quot;[未複製的專案](#placement-not-duplicated)&quot;。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下&#x200B;**[!UICONTROL Placements]**。

1. 執行下列任一項作業：

   * 若要複製一個位置，請按一下封裝名稱旁的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

   * 若要複製多個版位：

      1. 選取每個要複製的位置旁的核取方塊。

      1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Duplicate]**。

1. 指定新的位置設定：

   1. （單一版位）輸入新版位名稱。

   1. 在&#x200B;**[!UICONTROL Choose Package (Required)]**&#x200B;功能表中，選取父封裝或**[!UICONTROL No package]*。

   1. （選用）變更預設設定。

   這些設定會套用至所有選取的版位。

   依預設，新版位會用於原始廣告型別、指派給原始廣告商和促銷活動、具有從當天開始的航班排程、暫停且不包含原始廣告。

   當您建立多個版位時，新版位名稱會依序附加一個數字，使用慣例&lt;*original_placement_name #N*>，例如「我的版位#2」。

1. 按一下&#x200B;**[!UICONTROL Submit]**。

## 未複製的內容 {#placement-not-duplicated}

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

## 設定新刊登版位的最佳實務

>[!TIP]
>
>* 使用Bulksheets一次[變更多個行銷活動元件](/help/dsp/campaign-management/campaign-components-review-edit.md)。
>* 使用廣告標籤工作表來[上傳多個協力廠商廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

* 暫停新位置，直到您準備好要啟動它們為止。

* 請考量下列事項，並視需要編輯新的位置設定：

   * 帳戶是否有足夠的資金來因應新的職位安排預算？

   * 新刊登版位是否需要與舊刊登版位不同的預算？

   * 上傳創意，包括任何必要的自訂廣告權重和排程，並將其附加至版位。

   * 視需要附加事件畫素至版位和廣告。

   * 視需要納入地理目標和位置層級[!DNL DoubleVerify Authentic Brand Safety]區段至位置。

   * 針對程式化預留交易，請使用新交易ID並建立預設刊登版位。

   * 視需要建立[!UICONTROL Simple Ad Serving]個交易的新版位。

>[!MORELIKETHIS]
>
>* [關於位置管理](placement-about.md)
>* [建立位置](placement-create.md)
>* [編輯版位](placement-edit.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [位置設定](placement-settings.md)
