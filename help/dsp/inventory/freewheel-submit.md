---
title: 將PG交易的廣告提交至 [!DNL FreeWheel]
description: 瞭解如何在 [!DNL Freewheel]上向發佈者要求核准程式化預留交易的廣告。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# 向[!DNL Freewheel]提交程式化保證交易的廣告

*只具有[!DNL FreeWheel]程式化保證許可權的*&#x200B;帳戶

一旦您[在FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)上接受與發佈者的程式化保證交易，包括選取廣告並建立用於交易的程式化保證預設位置，您必須將廣告提交給[!DNL Freewheel]進行核准。

>[!PREREQUISITES]
>
>請與您的Adobe帳戶團隊合作，確保您的[!DNL DSP]帳戶擁有使用[!DNL FreeWheel]程式化保證工作流程的許可權。

1. 複製與[!DNL Freewheel]交易搭配使用之廣告的廣告金鑰：

   1. 按一下行銷活動的名稱。

   1. 在子功能表中，按一下&#x200B;**[!UICONTROL Ads]**。

   1. 按一下廣告名稱旁的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

   1. 廣告設定開啟後，複製瀏覽器位址列中所顯示URL中的英數字元廣告金鑰。

      例如，在以下URL中，廣告金鑰是`3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. 將廣告提交至[!DNL Freewheel]：

   1. 執行下列任一項作業：

      * 在廣告名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**」。

      * 在主功能表中，按一下&#x200B;**[!UICONTROL Inventory]** > **[!UICONTROL Deals]**。 在交易列中，按一下![選項功能表](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**。

   1. 驗證交易識別碼，輸入您在步驟1中複製的&#x200B;**[!UICONTROL Ad Key]**，然後按一下&#x200B;**[!UICONTROL Submit]**。

   廣告必須先提交並核准，才能執行。

1. [檢查廣告提交狀態](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [在 [!DNL Freewheel]](freewheel-overview.md)中設定程式化預留交易的概觀
>* [在交易識別碼收件匣中接受交易](deal-id-inbox-accept.md)
>* [檢查 [!DNL FreeWheel] 程式化預留交易的廣告狀態](freewheel-check-status.md)
>*  [!DNL Freewheel] 廣告提交的[錯誤碼](freewheel-error-codes.md)
