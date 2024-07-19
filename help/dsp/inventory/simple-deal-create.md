---
title: 建立[!UICONTROL Simple Ad Serving]交易
description: 瞭解如何為[!UICONTROL Simple Ad Serving]交易建立追蹤畫素。
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 建立[!UICONTROL Simple Ad Serving]交易

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Create]**，然後選取&#x200B;**[!UICONTROL Simple Ad Serving]**。

1. 輸入[交易設定](simple-deal-settings.md)：

   1. 在[!UICONTROL Select Ad Source]區段中，指定發行者、廣告商和促銷活動以及廣告型別的相關資訊，然後按一下&#x200B;**[!UICONTROL Next]**。

   1. 在[!UICONTROL Select Ad(s)]區段中，指定要用作DSP中Proxy的廣告：

      1. 執行下列任一項作業：

         * 針對現有廣告，選取要使用的廣告。

         * 針對新廣告，請建立Proxy [協力廠商廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

      >[!NOTE]
      > DSP不提供您指定的廣告。 發佈者提供廣告。

      1. 按一下&#x200B;**[!UICONTROL Next]**。

   1. 在摘要詳細資訊中，編輯摘要詳細資訊，然後按一下&#x200B;**[!UICONTROL Next]**。

      DSP會自動為廣告產生名為「SAS位置 — &lt;*交易名稱*>」的位置。 在位置中，交易會自動在[!UICONTROL Inventory Targets]區段中定位。 所有其他鎖定目標選項均不適用。

1. 以下列其中一種方式將事件追蹤畫素傳送給發佈者，以進行實作：

   * （選擇性）從[!UICONTROL Activate Tag with Publisher]畫面傳送交易標籤給發佈者。

     完成上述步驟後，DSP會產生電子郵件訊息，您可傳送給發行者。 訊息包含交易詳細資料、從中擷取交易標籤的連結，以及連結的授權代碼。

      1. 檢閱交易詳細資料，然後執行下列任一項作業：

         * 若要將資訊貼到您裝置上電子郵件應用程式的電子郵件訊息中，請按一下&#x200B;**[!UICONTROL Email & Done]**&#x200B;並選取電子郵件應用程式。 [!UICONTROL CC:]欄位已預先填入[!DNL Adobe]支援地址。 然後，您可以將訊息傳送給發行者的適當連絡人。

         * 若要將資訊複製到剪貼簿，請按一下&#x200B;**[!UICONTROL Copy Email]。**&#x200B;您可以手動將內容貼入電子郵件訊息，並傳送給發行者的適當連絡人。 您必須包含副本（副本：）至`publisher-support-global@adobe.com`。 當您完成複製郵件時，請按一下&#x200B;**[!UICONTROL Email & Done]**。

      1. （如有必要）請洽詢發佈者，檢視標籤是否包含適當的巨集，讓標籤可與發佈者的廣告伺服器搭配使用。

   * （選用）手動將事件追蹤畫素傳送給發佈者：

      1. 在[!UICONTROL Deals]檢視中的交易列中，按一下![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**。

         事件畫素包括[!UICONTROL Clickthrough]畫素和[!UICONTROL Impression]畫素。 視訊和音訊廣告也包含按四分位數結束的事件畫素（從[!UICONTROL 25% Complete]到[!UICONTROL 100% Complete]）。

      1. 複製事件追蹤畫素，並將其提供給您的發佈者。

>[!MORELIKETHIS]
>
>* [關於[!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving]設定](simple-deal-settings.md)
>* [檢視交易的詳細報告](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
