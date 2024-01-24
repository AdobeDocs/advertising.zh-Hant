---
title: 指定私人交易的版位和廣告
description: 瞭解如何搭配其他刊登版位和廣告使用私人交易。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: d6d295119bc974a87840e757877c1507237a6fa2
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# 指定私人交易的版位和廣告

對於非保證交易，您可以從以下欄位指定交易作為新刊登版位的詳細目錄目標 [!UICONTROL Placements] 檢視。

對於程式化預留(PG)交易，您可以使用指定的廣告從以下網址建立刊登版位： [!UICONTROL Deals] 檢視。

您也可以 [將廣告附加至刊登版位](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) 隨時與PG和無法保證的交易相關聯。

## 指定不保證交易作為刊登的詳細目錄目標

* [從建立版位 [!UICONTROL Placements] 檢視](/help/dsp/campaign-management/placements/placement-create.md). 在 [!UICONTROL Inventory Targeting] 設定，選取私人交易。

## 將刊登版位和廣告附加至PG交易

1. 在主功能表中，按一下 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在交易列中，按一下  **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. 在 [!UICONTROL Ad & Campaign Selection] 設定，選取要用於投放位置的廣告：

       1. 選取廣告商、行銷活動和廣告型別。 選擇性地選取廣告狀態，以篩選廣告。
       
       1. 從可用廣告清單中，選取用於交易的每個廣告旁的核取方塊。
       
       1. 按一下**[!UICONTROL Apply]**。
   
   1. 在位置設定畫面中：

      1. 輸入位置名稱。

      1. （可選）編輯 [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆寫預設競標（自動以交易的CPM值填入）、變更日期範圍或附加更多廣告。

      此交易會在「詳細目錄目標」區段中自動定位。 所有其他鎖定目標選項均不適用。

      1. 按一下 **[!UICONTROL Create placement]**.

發佈者啟用您的PG交易ID後，位置就會開始執行。

>[!NOTE]
>
> 您不需要傳送交易標籤給發行者進行驗證。

>[!MORELIKETHIS]
>
>* [關於私人詳細目錄](private-inventory-about.md)
>* [列出私人交易的刊登版位和廣告](/help/dsp/inventory/private-deal-view-placements.md)
>* [手動建立交易識別碼詳細資料](deal-id-create.md)
>* [手動交易識別碼設定](deal-id-settings.md)
>* [設定程式化保證交易](programmatic-guaranteed-set-up.md)
