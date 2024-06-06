---
title: 關於第一方對象來源
description: 瞭解如何將第一方區段中的其他使用者識別碼轉換為通用ID以用於無cookie目標定位。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 關於第一方對象來源

*Beta功能*

DSP可擷取第一方區段(由您客戶資料平台(CDP)內建立的雜湊電子郵件ID所組成)，並將它們轉換為區段（由通用ID所組成）。 每個產生的ID都會以人物為基礎，而廣告頻率上限則會套用在ID層級<!-- Move that info. to somewhere else? -->.

區段詳細資料包括每個通用ID型別的大小，以及Cookie或裝置ID追蹤的每個裝置型別的大小。

## 通用識別碼型別 {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

您可以將第一方區段轉譯為具有下列通用ID合作夥伴的驗證（確定性） ID的區段。

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution)：

   * 用於重新定位登入的使用者。

     [!DNL RampIDs] 適用於北美、澳洲和紐西蘭的使用者。

     費用是每個展示廣告曝光數0.15美元和每個影片廣告曝光數0.25美元。

   * 使用進行測量 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com)：

   * 用於重新定位登入的使用者。

     [!DNL UID2 IDs] 不適用於歐洲經濟區和其他國家/地區的使用者。 請參閱 [被禁止的國家/地區清單](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     費用是每個展示廣告曝光數0.15美元和每個影片廣告曝光數0.25美元。

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## 支援第一方區段的客戶資料平台

DSP已建立下列CDP的聯結器，以快速內嵌您的第一方區段。

DSP也可以使用批次、串流或API型資料共用來連線至任何其他CDP。 若要與新的CDP整合，請聯絡您的Adobe客戶團隊。

### [!DNL Adobe Real-Time Customer Data Platform]

DSP是整合的 *目的地* 的 [此 [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hant)，是Adobe Experience Platform的一部分。

在 [!DNL Real-Time CDP]，目的地是指與外部資料平台的連線，可順暢地啟用資料。 您可以使用目的地，針對DSP中的目標定位廣告啟用雜湊電子郵件地址。 如需目的地的詳細資訊，請參閱Experience Platform [目的地指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括產品概觀，產品說明 [建立目的地工作區](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [建立目的地連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、和 [將資料啟用至目的地](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

啟用DSP以擷取您的 [!DNL Adobe] [!DNL Real-time CDP] 第一方區段並將雜湊電子郵件地址轉換為通用ID，請參閱&quot;[轉換使用者ID來源 [!DNL Adobe Real-Time CDP] 至通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md).」

### [!DNL ActionIQ]

您可以從以下位置分享您組織的第一方資料： [!DNL Action IQ] 客戶資料平台，搭配DSP將雜湊電子郵件地址轉換為通用ID，以便在DSP中使用目標定位廣告。 此整合需要自訂。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

### [!DNL Tealium]

您可以從以下位置分享您組織的第一方資料： [!DNL Tealium] 客戶資料平台使用 [!DNL Amazon Web Services]. 如需更多有關在DSP中將雜湊電子郵件地址轉換為通用識別碼的資訊，請參閱&quot;[轉換使用者ID來源 [!DNL Tealium] 至通用ID](/help/dsp/audiences/sources/source-tealium.md).」

>[!MORELIKETHIS]
>
>* [轉換使用者ID來源 [!DNL Adobe Real-Time CDP] 至通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [轉換使用者ID來源 [!DNL Tealium] 至通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [對象來源設定](source-settings.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
