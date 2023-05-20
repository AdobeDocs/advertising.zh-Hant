---
title: 提交PG交易的廣告以 [!DNL FreeWheel]
description: 瞭解如何請求批准與發佈者在 [!DNL Freewheel]。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 提交計畫保證交易的廣告以 [!DNL Freewheel]

*與 [!DNL FreeWheel] 僅限程式保證權限*

一旦 [接受在FreeWheel上與發行商進行有計畫的保證交易](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)包括選擇廣告和建立用於交易的寫程式保證預設放置，您必須將廣告提交到 [!DNL Freewheel] 供審批。

>[!PREREQUISITES]
>
>與您的Adobe客戶團隊合作，確保 [!DNL DSP] 帳戶有權使用 [!DNL FreeWheel] 程式化保證的工作流。

1. 複製與 [!DNL Freewheel] 交易：

   1. 按一下市場活動的名稱。

   1. 在子菜單中，按一下 **[!UICONTROL Ads]**。

   1. 按一下  **[!UICONTROL ...]** > **[!UICONTROL Edit]** 地址欄。

   1. 開啟廣告設定後，請在瀏覽器地址欄中顯示的URL中複製字母數字廣告鍵。

      例如，在以下URL中，ad鍵為 `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. 將廣告提交到 [!DNL Freewheel]:

   1. 執行下列任一操作：

      * 在廣告名稱旁，按一下  **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**。

      * 在主菜單中，按一下 **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**。 在交易行中，按一下 ![「選項」菜單](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**。
   1. 驗證交易ID，輸入 **[!UICONTROL Ad Key]** 在步驟1中複製，然後按一下 **[!UICONTROL Submit]**。

   廣告必須在運行前提交和批准。

1. [檢查廣告提交狀態](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [中計畫保證交易設定概述 [!DNL Freewheel]](freewheel-overview.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [檢查廣告狀態 [!DNL FreeWheel] 計畫擔保交易](freewheel-check-status.md)
>* [錯誤代碼 [!DNL Freewheel] 廣告提交](freewheel-error-codes.md)

