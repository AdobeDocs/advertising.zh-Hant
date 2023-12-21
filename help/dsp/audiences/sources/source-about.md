---
title: 關於從受眾來源啟用已驗證的區段
description: 瞭解如何從客戶資料平台擷取第一方區段。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: e3e8753db31bc835c49eb2037fdcd7696a895a8c
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 關於從受眾來源啟用已驗證的區段

DSP可內嵌第一方區段(由客戶資料平台(CDP)內建立的雜湊電子郵件ID或通用ID所組成)。 您可以使用內嵌區段作為版位目標。

以下CDP已建立聯結器，但DSP也可以使用批次、串流或API型資料共用來連線至任何CDP。 若要與新的CDP整合，請聯絡您的Adobe客戶團隊。

## [!DNL Adobe Real-Time Customer Data Platform]

DSP已整合至 [此 [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hant)，是Adobe Experience Platform的一部分。

在 [!DNL Real-Time CDP]， *目的地* 是與外部資料平台的連線，可順暢地啟用資料。 例如，您可以使用目的地來針對各種DSP支援的數位格式啟用已知的客戶關係（例如雜湊電子郵件地址）。 如需目的地的詳細資訊，請參閱Experience Platform [目的地指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括產品概觀，產品說明 [建立目的地工作區](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [建立目的地連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、和 [將資料啟用至目的地](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

請參閱&quot;[搭配使用DSP整合的工作流程 [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md).」

## [!DNL ActionIQ]

您可以從以下位置分享您組織的第一方資料： [!DNL Action IQ] 客戶資料平台與DSP。 接著，您可以使用將DSP版位鎖定至區段 [!DNL RampIDs] 或 [!DNL Unified IDs 2.0].

此整合需要自訂。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

## [!DNL Tealium]

您可以從以下位置分享您組織的第一方資料： [!DNL Tealium] 客戶資料平台使用 [!DNL Amazon Web Services]. 接著，您可以使用將DSP版位鎖定至區段 [!DNL RampIDs]. 請參閱&quot;[搭配使用DSP整合的工作流程 [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md).」

>[!MORELIKETHIS]
>
>* [搭配使用DSP整合的工作流程 [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [搭配使用DSP整合的工作流程 [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [建立對象來源以啟用第一方對象](source-create.md)
>* [對象來源設定](source-settings.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
