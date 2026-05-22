---
title: 從 [!DNL LiveRamp]手動匯入已驗證的區段
description: 瞭解如何透過 [!DNL LiveRamp]啟用已驗證的對象。
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
TQID: https://experienceleague.adobe.com/ln4e1Jmq7vRhOIeg25UwNR8yToni5CuokxAcmEPMwEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# 從[!DNL LiveRamp]手動匯入已驗證的區段

您可以使用[!DNL LiveRamp] [!DNL Connect]儀表板手動將已驗證的[!DNL LiveRamp]區段傳送至DSP。 您可以將匯入的區段用於放置目標定位。 就第一方區段而言，費用為交付的每一顯示廣告曝光數0.15美元，以及交付的每一視訊廣告曝光數0.25美元。

每個匯入工作的區段對應和上傳最多可能需要七天時間。

<!--
Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. 在[!DNL Connect]儀表板中完成下列步驟：

   1. 啟用目的地拼貼&#x200B;**[!DNL AAC API 1P Onboarding]**。

   1. 僅將[!DNL Identifier Settings]設定為&#x200B;**[!DNL Ramp ID]**。

      ![識別碼設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （選擇性）如果您仍要接收Cookie型識別碼，請建立第二個[!DNL AAC API 1P Onboarding]目的地並選取&quot;[!DNL Cookies]&quot;、&quot;[!DNL IDFA]&quot;和&quot;[!DNL AAID]&quot;。

   1. 驗證在您的對象庫中（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或在位置設定中建立或編輯對象時，即可使用該對象庫）是否已匯入整個區段計數。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=zh-Hant)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
>* [從 [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)匯入第一方區段
