---
title: 管理位置的競標乘數
description: 瞭解如何建立和編輯位置目標的競標倍數。
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: c23da6494c6d4ce89735f3f63f89f5320ca02a40
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 2%

---

# 管理位置的競標乘數

您可以針對現有的位置目標建立和管理競標乘數，讓競標乘以增減競標。 [符合資格的目標型別](#bid-multiplier-by-target). 您可以手動編輯競標乘數值，或上傳含有值的試算表。

依預設，目標的競標乘數為1.00，這表示不會針對該目標調整競標。 值的範圍介於0.10到10.00之間。例如，競標修飾詞0.5會將6美元的競標降低為3美元(0.5 x 6)。 當拍賣符合多個競標修飾詞的資格時，所有適用的競標修飾詞都會相乘。 競標修飾詞絕不會將競標提高到超過最高競標。

您可以為設定競標乘數（具有1.00以外的值） [目標數目有限](#bid-multiplier-limits-by-target).

此功能可與您現有的位置目標搭配使用。 若要變更您的刊登版位選取的目標，請參閱&quot;[編輯版位](/help/dsp/campaign-management/placements/placement-edit.md).」

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 在位置名稱旁，按一下  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 調整合格目標的競標乘數：

   * 若要手動調整競標倍增值，請移至 [目標專屬標籤](#bid-multiplier-by-target) ([!UICONTROL Geo]， [!UICONTROL Inventory]， [!UICONTROL Sites]， [!UICONTROL Audience]、和 [!UICONTROL Brand Safety])，並編輯位置目標的現有值。

     大多數目標類別會在左側列出子類別。 按一下子類別，管理該子類別的競標乘數（如適用）。

   * 若要上傳具有競標倍增值的CSV檔案來覆寫現有值：

      1. 按一下 **[!UICONTROL CSV File Edit]** 在右上角。

      1. a)按一下 **[!UICONTROL Download Template]** 並使用使用者介面中顯示的相同語法和對應的競標倍增值輸入目標，或b)使用相同資訊編輯先前下載的範本。 將已編輯的檔案儲存至您的裝置或網路。

      1. 按一下 **[!UICONTROL Next]** 以移至 [!UICONTROL Upload File] 區段，然後a)將編輯的檔案拖放至方塊中，或b)按一下方塊內部，以從您的裝置或網路中選取檔案。

      1. 驗證中已上傳的資料 [!UICONTROL Review & Submit] 區段，然後按一下 **[!UICONTROL Save]**.

## 適用於競標倍增器的目標型別 {#bid-multiplier-by-target}

您只能為包含的目標（而非排除的目標）設定競標修飾詞。

* **地理目標**：地理位置（國家、州和城市）、郵遞區號和DMA

* **詳細目錄目標**：公開詳細目錄和的來源和摘要 [!UICONTROL On Demand] 詳細目錄

* **網站目標：** 已鎖定目標（但未排除）網站/應用程式、網站類別

* **對象目標：** 區段、時段、主題

* **ads.txt目標：** （當您選擇退出ads.txt時，這可讓您從所有賣家購買詳細目錄） ads.txt sellers only、ads.txt direct sellers和ads.txt sellers plus sites without ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## 按目標型別列出的競標乘數上限 {#bid-multiplier-limits-by-target}

您可以為有限數量的目標設定競標乘數（具有1.00以外的值）。 例如，您可以為最多20個國家/地區目標設定競標倍數。 以下列出每種目標型別可以有競標倍數的最大目標數量。

| 類別 | 引數 | 最大數量 |
| -------- | --------- | ----- |
| 地理 | 國家 | 20 |
| 地理 | 狀態 | 100 |
| 地理 | 城市 | 100 |
| 地理 | Metro | 100 |
| 地理 | 郵遞區號 | 100 |
| 詳細目錄 | 來源 | 100 |
| 詳細目錄 | 動態消息 | 100 |
| 網站 | 網站類別 | 100 |
| 網站 | 網站/應用程式 | 100 |
| 對象 | 區段 | 500 |
| 對象 | 主題 | 100 |
| 品牌安全 | Ads.txt | 不適用 |

>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [編輯版位](placement-edit.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [位置設定](placement-settings.md)
