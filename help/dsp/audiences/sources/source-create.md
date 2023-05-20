---
title: 建立受眾源以激活第一方受眾
description: 瞭解如何建立源以將受眾導入您的帳戶或廣告商帳戶。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 3347bfbaec92bb13428a39207954f895eb4f5d6d
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---

# 建立受眾源以激活第一方受眾

<!-- Will this remain for admin users/Adobe Account Team users only? -->

建立源以將受眾導入您的DSP帳戶或廣告商帳戶。 當前，可以從 [這樣 [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)。

>[!NOTE]
>
>建立源後 [!DNL Real-Time CDP]，您需要激活 [!DNL Real-Time CDP] 通過Adobe廣DSP告目標 [!DNL Real-Time CDP] 開始導入。 請參閱 [激活工作流中的步驟](source-about.md#workflow-sources)。

1. 在主菜單中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 按一下 [!UICONTROL Add Source].

1. 在 [!UICONTROL Select a Type] 的子菜單。

   *[!UICONTROL RT-CDP]*:此源類型，用於 [這樣 [!DNL Adobe Real-Time Customer Data Profile]](source-about.md)，也請參見Wiki頁。

1. 指定 [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*。

1. 輸入剩餘 [源設定](source-settings.md)。

   保留副本 [!UICONTROL Source Key] 即產生。 你以後需要這個價值。

1. 按一下 **[!UICONTROL Save]**.

1. 在Experience Platform中，使DSP用 [!UICONTROL Source Key] 在源設定中生DSP成的。

   有關激活目標連接DSP、選擇段和訪問控制權限的說明，請參見「」[Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)&quot;

>[!MORELIKETHIS]
>
>* [受眾源設定](source-settings.md)
>* [關於從受眾源激活經過驗證的段](source-about.md)
>* [從持久ID合作夥伴激活經過驗證的段](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於受眾管理](/help/dsp/audiences/audience-about.md)

