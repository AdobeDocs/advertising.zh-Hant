---
title: 複製行銷活動
description: 瞭解如何複製行銷活動。
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# 複製行銷活動

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

複製行銷活動，以使用類似設定建立新的行銷活動。 您可以：

* 為原始廣告商或其他廣告商複製行銷活動

* 選擇性地複製原始套件和版位

* 修改新行銷活動的投放日期

如需未複製的位置設定清單，請參閱&quot;[未複製的專案](#campaign-not-duplicated)&quot;。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 在行銷活動名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**」。

1. 指定新的行銷活動設定：

   1. 輸入新的行銷活動名稱和結束投放日期。

   1. （選用）變更預設設定。

      依預設，新行銷活動會指派給原始廣告商、具有從當天開始的航班排程，並包括原始套件和位置。

1. 按一下&#x200B;**[!UICONTROL Submit]**。

## 未複製的內容 {#campaign-not-duplicated}

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

## 設定新行銷活動的最佳實務

>[!TIP]
>
>* 使用Bulksheets一次[變更多個行銷活動元件](/help/dsp/campaign-management/campaign-components-review-edit.md)。
>* 使用廣告標籤工作表來[上傳多個協力廠商廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

* 暫停新的行銷活動，直到您準備好要啟動為止。

* 考量下列事項，並視需要編輯新的行銷活動設定：

   * 帳戶是否有足夠的資金來因應新的行銷活動預算？

   * 新行銷活動是否需要與舊行銷活動不同的預算？

   * 上傳創意，包括任何必要的自訂廣告權重和排程，並將其附加至版位。

   * 視需要附加事件畫素至版位和廣告。

   * 視需要納入地理目標和位置層級[!DNL DoubleVerify Authentic Brand Safety]區段以進行位置。

   * 針對程式化預留交易，請使用新交易ID並建立預設刊登版位。

   * 視需要建立[!UICONTROL Simple Ad Serving]個交易的新版位。

* 對於效能行銷活動（也就是套件使用自訂最佳化目標的行銷活動），請對每個套件使用[[!UICONTROL Linked Package for Optimization Learnings Carryover]設定](/help/dsp/campaign-management/packages/package-settings.md)，以使用先前行銷活動的歷史資料作為最佳化套件的輸入。

>[!MORELIKETHIS]
>
>* [關於行銷活動管理](campaign-about.md)
>* [建立行銷活動](campaign-create.md)
>* [編輯行銷活動](campaign-edit.md)
>* [檢視行銷活動的變更記錄](campaign-change-log.md)
>* [行銷活動設定](campaign-settings.md)
