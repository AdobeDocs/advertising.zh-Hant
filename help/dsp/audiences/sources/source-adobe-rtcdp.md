---
title: 「搭配使用DSP整合的工作流程 [!DNL Adobe] [!DNL Real-time CDP]"
description: 「瞭解如何啟用DSP以擷取您的 [!DNL Adobe] [!DNL Real-time CDP] 第一方區段。」
feature: DSP Audiences
source-git-commit: fb42e4aacaf0ea22890e0b4a46719725c99fffdc
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# 搭配使用DSP整合的工作流程 [!DNL Adobe Real-Time CDP]

1. [允許DSP將客戶資料區段轉譯為 [!DNL LiveRamp RampIDs]](source-universal-id.md) 在競標環境中可辨識的專案。<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [建立對象來源](source-create.md) 將對象匯入您的DSP帳戶或廣告商帳戶。

1. 在Experience Platform中，使用設定Advertising DSP目的地連線 [!UICONTROL Source Key] 在DSP來源設定中產生的值。

   如需啟用DSP目的地連線、選取區段及存取控制許可權的指示，請參閱&quot;[Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).」

如需其他支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [啟用通用ID合作夥伴的已驗證區段](source-universal-id.md)
>* [建立對象來源以啟用第一方對象](source-create.md)
>* [對象來源設定](source-settings.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目的地目錄概觀](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [搭配使用DSP整合的工作流程 [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
