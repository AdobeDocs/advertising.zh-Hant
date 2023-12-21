---
title: 建立對象來源以啟用第一方對象
description: 瞭解如何建立來源以將受眾匯入您的帳戶或廣告商帳戶。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# 建立對象來源以啟用第一方對象

<!-- Will this remain for admin users/Adobe Account Team users only? -->

在DSP中建立來源，將第一方對象匯入您的DSP帳戶或廣告商帳戶。

如需從特定客戶資料平台擷取區段所需的其他步驟，請參閱 [對象專用啟動工作流程](source-about.md)

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 按一下 **[!UICONTROL Add Source]**.

1. 在 [!UICONTROL Select a Type] 選單，選取來源型別。

   * *[!UICONTROL RT-CDP]*： [此 [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*：此 [[!DNL Tealium] 客戶資料平台](source-about.md).

1. 指定 [!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 輸入剩餘的 [來源設定](source-settings.md).

   保留 [!UICONTROL Source Key] 所產生的值。 您稍後需要該值。

1. 按一下 **[!UICONTROL Save]**.

>[!NOTE]
>
>在您建立客戶資料平台的來源後，您將需要完成其他步驟。 請參閱 [啟用工作流程 [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> 和 [啟用工作流程 [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [對象來源設定](source-settings.md)
>* [關於從受眾來源啟用已驗證的區段](source-about.md)
>* [啟用通用ID合作夥伴的已驗證區段](source-universal-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
