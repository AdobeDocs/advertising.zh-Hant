---
title: 關於第一方對象來源
description: 瞭解如何將第一方區段中的其他使用者識別碼轉換為通用ID以用於無cookie目標定位。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
TQID: https://experienceleague.adobe.com/8wdjwhNF-KDspEa1wSYWwlDOJxc3LiyqnSwEE-Fq9bY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 0%

---

# 關於第一方對象來源

對象來源功能可讓您依原樣匯入包含通用ID的第一方區段，或將其轉換為包含指定通用ID型別的區段：

* 澳洲的廣告商可匯入已包含[!DNL AdFixus]通用ID的第一方區段。

* DSP可擷取第一方區段(由其他客戶資料平台(CDP)內建的雜湊電子郵件ID、Cookie和行動廣告ID (MAID)組成)，並將它們轉換為區段（由[!DNL LiveRamp] [!DNL RampIDs]和[!DNL Unified ID 2.0 (UID2.0)] ID組成）。

對於所有ID型別，每個產生的ID都是以人物為基礎的，而廣告頻率上限則套用在ID層級<!-- Move that info. to somewhere else? -->。 區段詳細資料包括每個通用ID型別的大小，以及Cookie或裝置ID追蹤的每個裝置型別的大小。

## 您可以轉譯為第一方區段的通用ID型別 {#universal-id-types}

<!--
  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

您可以將第一方區段從[!DNL ActionIQ]、[!DNL Adobe]、[!DNL Real-time CDP]、[!DNL Amperity]、[!DNL Optimizely]和[!DNL Tealium]轉譯為具有下列通用ID合作夥伴的已驗證（確定性） ID的區段。

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * 用於重新定位登入的使用者。

     [!DNL RampIDs]適用於北美、澳洲和紐西蘭的使用者。

     費用是每個展示廣告曝光數0.15美元和每個影片廣告曝光數0.25美元。

   * 針對使用[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)的測量。

* [[!DNL Unified ID 2.0 (UID2.0)] 識別碼](https://unifiedid.com)：

   * 用於重新定位登入的使用者。

     [!DNL UID2 IDs]不適用於歐洲經濟區和其他國家/地區的使用者。 檢視禁止的國家[清單](/help/policies/universal-id-policy.md#prohibited-countries-uid2)。

     費用是每個展示廣告曝光數0.15美元和每個影片廣告曝光數0.25美元。

<!--
 Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. Contact your Adobe Account Team for instructions.
-->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## 第一方區段的支援客戶資料平台

DSP已建立下列CDP的聯結器，以快速內嵌您的第一方區段。

DSP也可以使用批次、串流或API型資料共用，連線至任何其他CDP。 若要與新的CDP整合，請聯絡您的Adobe客戶團隊。

### [!DNL ActionIQ]

您可以與DSP共用您組織從[!DNL ActionIQ]客戶資料平台的第一方資料，以將雜湊電子郵件地址轉換為通用ID，以便在DSP中鎖定目標廣告。 此整合需要自訂。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

### [!DNL Adobe Real-Time CDP]

DSP是[the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hant)的整合式&#x200B;*目的地*，它是Adobe Experience Platform的一部分。

在[!DNL Real-Time CDP]中，目的地是與外部資料平台的連線，可順暢地啟用資料。 您可以在DSP中使用目的地來啟用雜湊電子郵件地址、Cookie和行動廣告ID，以用於目標定位廣告。 如需有關目的地的詳細資訊，請參閱Experience Platform [目的地指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html?lang=zh-Hant)，包括產品概述、[建立目的地工作區](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html?lang=zh-Hant)和[建立目的地連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=zh-Hant)的指示，以及[啟用資料至目的地](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html?lang=zh-Hant)。

若要讓DSP擷取您的[!DNL Adobe] [!DNL Real-time CDP]第一方區段，並將雜湊電子郵件地址、Cookie和行動廣告ID轉換為通用ID，請參閱[將使用者ID從 [!DNL Adobe Real-Time CDP] 轉換為通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)。

### [!DNL AdFixus]

澳洲廣告商可以使用Advertising DSP與[!DNL AdFixus]的整合，匯入包含[!DNL AdFixus]通用ID的第一方區段。 此路徑與將CDP聯結器內的雜湊電子郵件ID或MAID轉譯為[!DNL RampIDs]或[!DNL UID2] ID不同。 如需詳細資訊，請參閱&quot;[從 [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)匯入第一方區段&quot;。

### [!DNL Amperity]

您可以與DSP共用您組織從[!DNL Amperity]客戶資料平台的第一方資料，以將雜湊電子郵件地址轉換為通用ID，以便在DSP中鎖定目標廣告。 如需詳細資訊，請參閱[將使用者ID從 [!DNL Amperity] 轉換為通用ID](/help/dsp/audiences/sources/source-amperity.md)。

### [!DNL Optimizely]

您可以與DSP共用您組織從[!DNL Optimizely]客戶資料平台的第一方資料，以將雜湊電子郵件地址轉換為通用ID，以便在DSP中鎖定目標廣告。 如需詳細資訊，請參閱[將使用者ID從 [!DNL Optimizely] 轉換為通用ID](/help/dsp/audiences/sources/source-optimizely.md)。

### [!DNL Tealium]

您可以使用[!DNL Amazon Web Services]從[!DNL Tealium]客戶資料平台共用您組織的第一方資料。 如需更多有關在DSP中將雜湊電子郵件地址轉換為通用識別碼的資訊，請參閱[將使用者ID從 [!DNL Tealium] 轉換為通用識別碼](/help/dsp/audiences/sources/source-tealium.md)。

>[!MORELIKETHIS]
>
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [將使用者ID從 [!DNL Adobe Real-Time CDP] 轉換為通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [將使用者ID從 [!DNL Amperity] 轉換為通用ID](/help/dsp/audiences/sources/source-amperity.md)
>* [將使用者ID從 [!DNL Optimizely] 轉換為通用ID](/help/dsp/audiences/sources/source-optimizely.md)
>* [將使用者ID從 [!DNL Tealium] 轉換為通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [從 [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)匯入第一方區段
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
