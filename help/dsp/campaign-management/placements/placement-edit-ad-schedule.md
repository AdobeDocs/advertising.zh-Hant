---
title: 編輯刊登版位的廣告時程表
description: 瞭解如何變更附加至刊登版位的廣告之廣告排程。
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: bc45e96cf091cba3872b20f6ea691e369b29982f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# 編輯刊登版位的廣告時程表

## 編輯一或多個位置的廣告排程

您可以使用變更附加至多個刊登版位的廣告之排程投放日期和廣告輪換 [!DNL Microsoft Excel] 試算表。 每個廣告都可以在多次飛行期間啟用。

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 選取您要下載其廣告資料之每個版位旁的核取方塊。

1. 在大量動作工具列中，按一下 **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. 當檔案可用時，按一下 **[!UICONTROL Download]** 在瀏覽器頁面頂端的通知中，根據瀏覽器的正常程式下載工作表檔案（XLSX格式）。

   ![下載就緒通知](/help/dsp/assets/download-ready.png "下載就緒通知")

1. 開啟下載的檔案，編輯每個廣告列的航班資訊欄位以包含在航班中，並儲存更新的檔案：

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (例如 [!UICONTROL Flight 1 Start Date] 和 [!UICONTROL Flight 1 End Date])：航班的第一個和最後一個日期。 每個日期使用YYYY-MM-DD格式。 任何包含空白投放日期欄位的廣告都會被視為非參與廣告。

   * **[!UICONTROL Flight N Weight]** (例如 [!UICONTROL Flight 1 Weight])：如何旋轉航班的廣告。 輸入值：

      * 若要平均旋轉航班的廣告，請輸入 `[!UICONTROL Even]`.

      * 若要不均勻地旋轉投放的廣告，請輸入每個廣告旋轉的相對權重，以百分比表示(例如 `40` 40%)。 航班的總重量必須等於100。

1. 上傳已編輯的廣告排程範本：

   1. 選取每個適用位置旁的核取方塊。

   1. 在大量動作工具列中，按一下 **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**，並指定要上傳的檔案。

## 編輯單一位置的廣告排程

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

您可以變更附加至刊登版位的廣告之排程投放日期和廣告輪換。 每個廣告都可以在多次飛行期間啟用。

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 在位置名稱旁，按一下  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

   1. 執行下列任一項作業：

      * 若要新增航班，請按一下 **[!UICONTROL Add Flight]**，然後指定開始日期和結束日期。

      * 若要將現有航班新增至廣告，請按一下 **[!UICONTROL +]** 於小眾測試版欄的廣告列。

      * 若要從廣告中移除現有的航班，請按一下 **[!UICONTROL x]** 於小眾測試版欄的廣告列。

      * （如果有多個廣告具有相同的外觀）若要將廣告旋轉不平均，請按一下 **[!UICONTROL Even Rotation]** 在飛行資訊中，然後輸入旋轉每個廣告的相對權重，以百分比表示。

        總重量必須等於100。

   1. 在右上角，按一下 **[!UICONTROL Continue]**.

   1. 檢閱航班詳細資料，然後按一下 **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [編輯位置](placement-edit.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [位置設定](placement-settings.md)
