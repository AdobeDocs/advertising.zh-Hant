---
title: 手動匯入已驗證的區段，從 [!DNL LiveRamp]
description: 瞭解如何透過啟用已驗證的對象 [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 手動匯入已驗證的區段，從 [!DNL LiveRamp]

*Beta功能*

您可以手動傳送已驗證的郵件 [!DNL LiveRamp] 區段至DSP，使用 [!DNL LiveRamp] [!DNL Connect] 儀表板。 您可以將匯入的區段用於放置目標定位。 就第一方區段而言，費用為交付的每一顯示廣告曝光數0.15美元，以及交付的每一視訊廣告曝光數0.25美元。

每個匯入工作的區段對應和上傳最多可能需要七天時間。

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. 在「 」中完成以下步驟 [!DNL Connect] 儀表板：

   1. 啟用目的地圖磚 **[!DNL AAC API 1P Onboarding]**.

   1. 設定 [!DNL Identifier Settings] 至 **[!DNL Ramp ID]** 僅限。

      ![識別碼設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （選用）如果您仍要接收Cookie型識別碼，請建立第二個 [!DNL AAC API 1P Onboarding] 目的地並排顯示&quot;[!DNL Cookies]，&quot; &quot;[!DNL IDFA]，」和「[!DNL AAID]「」已選取。

   1. 在您的對象庫中驗證（當您從以下位置建立或編輯對象時可使用此庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 或在位置設定內)，表示已匯入整個區段計數。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [對象來源設定](source-settings.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
