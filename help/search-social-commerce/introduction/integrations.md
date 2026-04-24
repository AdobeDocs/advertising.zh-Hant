---
title: Integration with Adobe CX Enterprise solutions and services
description: Learn about Search, Social, & Commerce integrations with Adobe CX Enterprise solutions and services.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
TQID: https://experienceleague.adobe.com/vIjCxWutfGn8H9-TqxLvztNazb9RWq7ECeoOQXLfyEw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: f2860a4b-f905-4545-bead-1bbc92564592
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 619
ht-degree: 0%

---

# Integration with Adobe CX Enterprise solutions and services

Advertising Search, Social, &amp; Commerce is integrated with the following [!DNL Adobe] products.

* [Tags from Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — You can use the [Adobe Advertising Cloud Extension](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) for Adobe Experience Platform to [create Adobe Advertising conversion tracking tags](/help/search-social-commerce/tools/conversion-tag-generate.md), as well as third-party tracking tags, for your ad landing pages. If your organization doesn&#39;t have an Experience Platform account, then you can still install the extension directly in the [user interface for Adobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection/), which is available for free to Adobe CX Enterprise customers.

  To install the required extension, contact your organization administrator for access to Data Collection features in the UI and ask them to grant you the `manage_properties` permission.

  **Note:** You can also [create conversion tracking tags directly within Search, Social, &amp; Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — (Opt-in feature) Adobe Advertising and [!DNL Analytics] are integrated in the following ways:

   * Adobe Advertising and [!DNL Analytics] seamlessly share data. [!DNL Analytics] can send site engagement and conversion data daily to Search, Social, &amp; Commerce, where the data is available for ad optimization and for reporting. Also, Adobe Advertising can send ad traffic data — including impressions, clicks, and cost — from your ad networks daily to [!DNL Analytics], where the data is available in all reporting tools.

     See &quot;[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)&quot; for more information about [!DNL Analytics] support for each ad network and ad type. See also &quot;[Overview of [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; for more information about the data exchange.

     To exchange data, both Adobe Advertising and [!DNL Analytics] must be initially configured. Contact your Adobe Account Team for more information about the initial setup.

     >[!NOTE]
     >
     >By default, the [!DNL Analytics] metrics aren&#39;t visible in Search, Social, &amp; Commerce screens. You must explicitly [make the metrics available in campaign management views, portfolios, and reports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) after the [!DNL Adobe] implementation team has configured selected standard or custom events to pass into Adobe Advertising. 您可以選擇變更顯示的量度名稱（不需要在[!DNL Analytics]中變更它們）。 您可以在UI中檢視量度，以及從[!UICONTROL Admin] > [!UICONTROL Conversions]重新命名量度。

   * 具有[!DNL Analytics]但不具有Audience Manager的廣告商可以從與Adobe CX Enterprise共用的[!DNL Analytics]區段中[建立 [!DNL Google Ads] 客戶相符對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 廣告商必須實作[Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)並在其網站上部署標籤，才符合資格。 然後，您可以在[!DNL Google Ads]行銷活動中使用對象作為行銷活動層級或廣告群組層級[目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

* Adobe Audience Manager區段 — （選擇加入功能）您可以從將「搜尋」、「社交」和「Commerce」當作目的地的Audience Manager區段[建立 [!DNL Google Ads] 客戶相符對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 這可能包括發佈至Adobe CX Enterprise的[!DNL Analytics]區段，以及使用Adobe CX Enterprise對象庫建立的區段。 然後，您可以在[!DNL Google Ads]行銷活動中使用對象作為行銷活動層級或廣告群組層級[目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

  如需詳細資訊，請參閱[Adobe Advertising與Adobe Audience Manager的整合](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)。

* Adobe Target — 您可以在Search、Social和Commerce與[!DNL Target]之間實作點進訊號共用，在[!DNL Target]中為您的廣告設定A/B測試活動，然後使用[!DNL Analytics] Analysis Workspace檢視測試資料。

* Adobe Campaign — 您可以[使用 [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)內的電子郵件清單，建立和更新 [!DNL Google Ads] 客戶比對對象。

* Adobe CX Enterprise通知 — （透過Adobe CX Enterprise登入時）從每頁頂端的通知連結（[警示通知](/help/search-social-commerce/assets/notifications-panel.png "Alert Notifications")）中，您可以檢視所有Adobe CX Enterprise系統更新、貼文、提及和共用的資產。 如需存取Adobe CX Enterprise的相關資訊，請聯絡您的Adobe客戶團隊。
