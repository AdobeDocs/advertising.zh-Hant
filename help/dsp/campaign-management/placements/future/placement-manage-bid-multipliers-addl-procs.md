---
title: 管理位置的競標乘數
description: 瞭解如何建立和編輯指定位置目標的競標乘數。
feature: DSP Placements
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 管理位置的競標乘數


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

您可以使用此功能變更現有位置目標的競標倍數。

若要變更您的刊登版位選取的目標，請參閱&quot;[編輯版位](/help/dsp/campaign-management/placements/placement-edit.md).」

## 管理一或多個位置的競標乘數

對於所有選取的位置，您可以手動編輯值或上傳包含值的試算表。

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 選取您要管理其競標倍數的每個位置旁的核取方塊。

1. 在大量動作工具列中，按一下 **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 手動或上傳具有目標值的CSV檔案來調整合格目標的競標倍數：

   * 若要手動調整競標倍增值，請移至每個目標特定標籤([!UICONTROL Geo]， [!UICONTROL Inventory]， [!UICONTROL Sites]， [!UICONTROL Audience]、和[!UICONTROL Brand Safety])，並編輯位置目標的現有值。

   相同的變更會套用至所有選取的版位。

   * 若要上傳含有競標倍增值的CSV檔案以覆寫現有值：

     >[!NOTE]
     >
     >如果您將欄位留空，則會刪除該目標型別的所有值。<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there only one data row is applicable for all. -->

      1. 按一下 **[!UICONTROL CSV Edit]** 在右上角。

      1. a)按一下 **[!UICONTROL Download Template]** 並編輯競標倍增值，或b)編輯先前下載的範本。 將已編輯的檔案儲存至您的裝置或網路。

      1. a)將編輯的檔案拖放至方塊中，或b)按一下方塊內部，從您的裝置或網路中選取檔案。

   1. 按一下 **[!UICONTROL Upload]**.

   依預設，目標的競標乘數為1.00，這表示不會針對該目標調整競標。 值的範圍介於0.10到10.00之間。例如，競標修飾詞0.5會將6美元的競標降低為3美元(0.5 x 6)。 您可以為設定競標乘數（具有1.00以外的值） [目標數目有限](#bid-multiplier-limits-by-target).

   當拍賣符合多個競標修飾詞的資格時，所有適用的競標修飾詞都會相乘。

   競標修飾詞絕不會將競標提高到超過最高競標。

1. 按一下 **[!UICONTROL Save]**.

-->

## 上傳試算表以管理單一位置的競標倍數<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

上傳檔案中的變更會覆寫現有的競標乘數值。<!-- what if you delete a row? -->

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 在位置名稱旁，按一下  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. a)按一下 **[!UICONTROL Download Template]** 並編輯競標倍增值，或b)編輯先前下載的範本。 將已編輯的檔案儲存至您的裝置或網路。

   依預設，目標的競標乘數為1.00，這表示不會針對該目標調整競標。 值的範圍介於0.10到10.00之間。例如，競標修飾詞0.5會將6美元的競標降低為3美元(0.5 x 6)。 您可以為設定競標乘數（具有1.00以外的值） [目標數目有限](#bid-multiplier-limits-by-target).

   當拍賣符合多個競標修飾詞的資格時，所有適用的競標修飾詞都會相乘。

   競標修飾詞絕不會將競標提高到超過最高競標。

1. a)將編輯的檔案拖放至方塊中，或b)按一下方塊內部，從您的裝置或網路中選取檔案。

1. 按一下 **[!UICONTROL Upload]**.

1. 按一下 **[!UICONTROL Save]**.

## 適用於競標倍增器的目標型別 {#bid-multiplier-by-target}

未在此處複製

## 按目標型別列出的競標乘數上限 {#bid-multiplier-limits-by-target}

未在此處複製

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
