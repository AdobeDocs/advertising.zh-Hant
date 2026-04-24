---
title: About audience management in Advertising DSP
description: Learn about audience management features.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
TQID: https://experienceleague.adobe.com/IocF0s67I-vJAUx9Eom-aWEf-Q6H-ZOjczyGr0f9PsA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 1394
ht-degree: 0%

---

# About audience management in Advertising DSP

In DSP, you can create and manage audience segments and audience sets, which you can use as targets for your placements:

* Collect your own first-party audience data by creating and implementing DSP segments. You can later retarget users in the segment with ads or prevent users in the segment from receiving ads. You can create the following types of segments:

   * [Custom segments](/help/dsp/audiences/custom-segment-create.md) to track a) users exposed to ads from desktop and mobile devices and b) users who visit specific webpages. The tracking tag can track either cookie-based users or users associated with ID5 universal IDs.

   * [CCPA opt-out-of-sale segments](/help/dsp/audiences/ccpa-opt-out-segment-create.md) to track the users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA). You can retrieve monthly reports of the user IDs from opt-out-of-sale requests.

     For more information about Adobe Advertising support for CCPA opt-out-of-sale requests, see [Adobe Advertising support for the California Consumer Privacy Act: Consumer opt-out of sale support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Beta feature) [Obtain and use universal IDs for cookieless targeting](/help/dsp/audiences/universal-ids.md):

   * Manually send your authenticated [!DNL LiveRamp] [!DNL RampID] segments directly to DSP.

   * Allow DSP to import first-party segments from your customer data platform and translate them to supported universal ID types.

   * Include third-party segments that contain universal IDs in your placement targets without any extra steps.

* Create an audience library of [reusable audiences](/help/dsp/audiences/reusable-audience-create.md). Saved audiences are composed of any of your available audience segments and any of your other saved audiences. Any changes you make to a saved audience are automatically applied to all placements that target or exclude the audience and to all other audiences that include the saved audience.

  Saved audiences allow media planners to group audiences as needed, by including and excluding multiple segments using complex Boolean logic. The  (targetable) size of each individual segment and the overall active audience size are indicated as you build an audience. Campaign executioners can then simply select one or more saved audiences as placement targets rather than manually configure audience targets for each placement.

Additional audience types are also available for placement targeting.

## Importing first-party and third-party data segments

You have many options to import first-party and third-party data segments into DSP, using the DSP user interface and/or through custom import services.

* DSP can pull in your Adobe Audience Manager and other [!DNL Adobe] audiences for targeting. For prerequisites and instructions, see &quot;[Import Adobe Audience Manager segments for ad targeting](/help/integrations/audience-manager/import-audiences.md).

* DSP can translate first-party data segments from supported customer data platforms to segments with universal IDs using the [Sources feature](/help/dsp/audiences/sources/source-about.md). You can also [manually send your authenticated [!DNL LiveRamp] [!DNL RampID] segments directly to DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP can import your other first-party data segments directly from your data management platform (DMP) and provide them to any set of advertisers, as needed.

* DSP can import custom third-party segments, including complex combinations of third-party segments. You can provide the segments to any set of advertisers, as needed.

如需詳細資訊，請聯絡您的Adobe客戶團隊。

## Audiences available as placement targets

You can target your placements to all of the following types of audiences.

* All user-created audience sets that were saved in DSP.

* All user-created audience segments that were created in DSP:

   * Custom segments for users who visited specific webpages and users exposed to impressions of specific ads.

     No fees are incurred for impressions delivered to universal IDs.

   * CCPA opt-out-of-sale audience segments for users who submitted opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA).

* All of your imported first-party data segments, including segments that were translated to universal IDs.

  Additional fees are charged for impressions delivered to universal IDs. See &quot;[About first-party audience sources](/help/dsp/audiences/sources/source-about.md)&quot; for rates.

* All of your imported custom third-party data segments.

* (Placements targeting the U.S. only) [All third-party data segments available to DSP customers from over 30 providers](/help/dsp/audiences/third-party-data-providers.md), including [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]),[!DNL Lotame], [!DNL Neustar], and many more.

  You can target specific segments, which target users based on audience data (for example, users with specific demographics, interests or intents, and/or behavioral profiles). You can browse by data provider and category, search for segments by name or segment ID, or filter the results by data provider, active segment size, web browser count, or devices count.

  協力廠商區段會產生額外費用，這些費用會顯示在每個區段名稱旁。

* （僅使用Adobe Experience Platform轉換標籤且具有Adobe Advertising JavaScript和[!DNL Real-Time CDP]、Adobe Audience Manager或Adobe Analytics的廣告商）您在[!DNL Real-Time CDP]中建立、在Audience Manager中建立或從Audience Manager或[!DNL Analytics]發佈至Adobe CX Enterprise的所有可用第一方、第二方或第三方受眾區段。

  使用區段的定價是預先議定的，在DSP中不可見。

  [!DNL Analytics]中的區段在您建立或發佈為CX Enterprise對象後約一小時可使用。 直接來自Audience Manager或[!DNL Real-Time CDP]的區段在您共用後24小時內即可使用。

  >[!NOTE]
  >
  >請參閱[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=zh-Hant)、[Analytics](https://experienceleague.adobe.com/docs/analytics.html?lang=zh-Hant)和[the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html?lang=zh-Hant)的檔案，以取得關於在這些解決方案中設定和收集區段資料的資訊。

## 對象人數資料

在對象>所有對象和版位設定的對象鎖定目標區段中，您可以依大小範圍篩選每個區段清單，包括特定裝置型別或通用ID型別的個別範圍。

![依對象人數篩選](/help/dsp/assets/audience-size-filter.png)

您也可以檢視詳細的對象人數資料：

* 系統會顯示所有選取區段和儲存對象的作用中重複資料刪除對象人數，且您可以依裝置型別（瀏覽器、行動或連線電視）檢視詳細資料。

  ![合併的對象人數](/help/dsp/assets/audience-size.png)

* 若為個別區段，作用中對象人數和CPM （若適用）會顯示在區段名稱旁。

  ![個別區段大小](/help/dsp/assets/audience-size-segment.png)

* 您可以檢視有關個別區段或儲存對象的詳細資訊，包括瀏覽器、行動裝置、連線電視和通用ID型別合作夥伴的大小。 對於已儲存的對象，作用中對象總人數是去除重複項的總計。

  ![個別區段或儲存的對象詳細資料](/help/dsp/assets/audience-size-segment-details.png)

## [!UICONTROL Audiences]檢視

### [!UICONTROL All Audiences]檢視

在「[!UICONTROL All Audiences]」檢視或「對象庫」中，您可以儲存和管理可重複使用的對象，其中包括對象區段群組，甚至是其他儲存的對象。 您可以使用受眾作為多個位置的目標。 版位名稱旁會顯示各對象所使用的版位數量。

您可以編輯、複製、刪除、匯出或共用任何對象。

### [!UICONTROL Segments]檢視

在[!UICONTROL Segments]檢視中，所有使用者都可以建立其他自訂區段。

[!UICONTROL Segments]檢視也列出下列區段型別：

* 所有使用者建立的自訂區段皆可供使用者使用。

  您可以檢視您建立的任何自訂區段的追蹤標籤，並和其他使用者共用這些區段。 您也可以編輯或刪除您建立的自訂區段。

  您無法編輯或共用其他使用者與您共用的自訂區段。

* 使用者可使用的所有第一方區段依原樣匯入。

  您無法編輯或共用與您共用的第一方區段。 如果您需要與其他使用者共用第一方區段，請聯絡您的Adobe客戶團隊。

* 所有可供使用者使用的自訂第三方區段。

  您無法編輯或共用與您共用的第三方區段。 如果您需要與其他使用者共用協力廠商區段，請聯絡您的Adobe客戶團隊。

### [!UICONTROL Sources]檢視

在[!UICONTROL Sources]檢視中，您可以在支援的客戶資料平台中設定第一方區段的來源，以將其轉換為包含指定通用ID型別的區段。 來源設定包括自動產生的來源金鑰，您會將其提供給客戶資料平台以建立連線。

如需關於支援的客戶資料平台、支援的通用ID型別以及設定每個客戶資料平台連線的工作流程的詳細資訊，請參閱&quot;[關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)&quot;。

翻譯後的區段可納入可重複使用的對象和無曲別目標定位的放置設定中。

>[!MORELIKETHIS]
>
>* [支援啟用通用ID](/help/dsp/audiences/universal-ids.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [建立和實施自訂區段](custom-segment-create.md)
>* [建立並實作[!UICONTROL CCPA Opt-Out-of-Sale]區段](ccpa-opt-out-segment-create.md)
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](/help/dsp/audiences/sources/source-manage.md)
>* [從 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手動匯入已驗證的區段
>* [可用的協力廠商資料提供者](third-party-data-providers.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
