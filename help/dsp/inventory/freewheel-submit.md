---
title: 向 [!DNL FreeWheel]提交PG交易的廣告
description: 瞭解如何在 [!DNL FreeWheel]上向發佈者要求核准程式化預留交易的廣告。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
TQID: https://experienceleague.adobe.com/f6Cu6mG77YOjwshI4xVbkLSkykAhqXonfSMg5ynDK5g
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# 向[!DNL FreeWheel]提交程式化預留交易的廣告

*只具有[!DNL FreeWheel]程式化保證許可權的*&#x200B;帳戶

一旦您[在FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)上接受與發佈者的程式化保證交易，包括選取廣告並建立用於交易的程式化保證預設位置，您必須將廣告提交給[!DNL FreeWheel]進行核准。

>[!PREREQUISITES]
>
>請與您的Adobe帳戶團隊合作，確保您的[!DNL DSP]帳戶擁有使用[!DNL FreeWheel]程式化保證工作流程的許可權。

1. 複製與[!DNL FreeWheel]交易搭配使用之廣告的廣告金鑰：

   1. 按一下行銷活動的名稱。

   1. 在子功能表中，按一下&#x200B;**[!UICONTROL Ads]**。

   1. 按一下廣告名稱旁的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

   1. 廣告設定開啟後，複製瀏覽器位址列中所顯示URL中的英數字元廣告金鑰。

      例如，在以下URL中，廣告金鑰是`3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. 將廣告提交至[!DNL FreeWheel]：

   1. 執行下列任一項作業：

      * 在廣告名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**」。

      * 在主功能表中，按一下&#x200B;**[!UICONTROL Inventory]** > **[!UICONTROL Deals]**。 在交易列中，按一下![選項功能表](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**。

   1. 驗證交易識別碼，輸入您在步驟1中複製的&#x200B;**[!UICONTROL Ad Key]**，然後按一下&#x200B;**[!UICONTROL Submit]**。

   廣告必須先提交並核准，才能執行。

1. [檢查廣告提交狀態](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [在 [!DNL FreeWheel]](freewheel-overview.md)中設定程式化預留交易的概觀
>* [在[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)中接受交易
>* [檢查 [!DNL FreeWheel] PG交易的廣告狀態](freewheel-check-status.md)
>* [&#x200B; [!DNL FreeWheel] 廣告提交的錯誤碼](freewheel-error-codes.md)
