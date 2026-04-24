---
title: About campaign management in Search, Social, & Commerce
description: Learn about campaign management features in Search, Social, & Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tgoMzw4DbEY5evC2s1f6mQHfJYYb7DJzMfFUnc-06Bk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 808
ht-degree: 0%

---

# About campaign management in Search, Social, &amp; Commerce

Search, Social, &amp; Commerce allows you to track and/or manage your search, display/content, social, shopping, audience, and performance max campaigns in one place. Depending on the ad network and campaign type, the available functionality may include synchronization with your ad networks, create and edit abilities, tracking and conversion attribution, reporting, and bid and budget optimization. 如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

As you add and edit campaign data in the [!UICONTROL Campaigns] views, Search, Social, &amp; Commerce immediately pushes the data changes to the ad network. Search, Social, &amp; Commerce also pulls campaign structure data and click data from synced ad network accounts once a day (or more often when new campaigns are detected) and on demand as requested.

## Setting up access to your ad network accounts

To track the performance of ads in an advertiser&#39;s ad network account (and to potentially place bids for the ads), the Adobe Account Team [creates a corresponding account record](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) in Search, Social, &amp; Commerce. The account record includes tracking options.

For accounts that are synchronized via the ad network&#39;s API, the account record also includes the account access credentials. Once the account is enabled, the account data is pulled from with the ad network. You can then view the existing account data as well as create and edit campaign structure and ad data.

## Click tracking to tie clicks to conversions

If you use the Adobe Advertising conversion tracking service, then you must include Search, Social, &amp; Commerce click-tracking code in the landing page suffix, tracking templates, and final/destination URLs for ads, keywords, and placements, sitelinks and product listings. For [supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md) whose campaign settings include &quot;[!UICONTROL EF Redirect]&quot; and &quot;[!UICONTROL Auto Upload],&quot; Search, Social, &amp; Commerce automatically appends its own redirect and tracking code when you save the record, so you don&#39;t need to manually add it. Otherwise, you must manually add the code to your tracking templates or final URLs.

For more information about tracking, see the chapter on &quot;Tracking.&quot;

## Automating bidding and budget management

For [supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md), you can group your campaigns into portfolios, each with a specific business objective and a specific budget or performance target. In standard portfolios, Search, Social, &amp; Commerce optimizes CPC keyword bids and campaign budgets. Hybrid portfolios combine optimization technologies from Search, Social, &amp; Commerce and your ad networks.

For more information about the available portfolio options and how to set up portfolios, see Optimization Guide chapter on &quot;Portfolios,&quot; which is available from within Search, Social, &amp; Commerce.<!-- verify convention for referencing Optimization Guide here -->

## The campaign management views

The campaign management views allow you to monitor and manage your search accounts. The following views are available:

* **[!UICONTROL Campaigns]** — The [!UICONTROL Campaigns] views show data from each connected ad network account. You can view cost, click, impression, and revenue data across all ad network accounts and across individual accounts, campaigns, ad groups, keywords, ads, shopping product groups, placements, auto targets (dynamic search targets), audiences, and ad extension libraries and their associated account entities. For [supported campaign types on supported ad networks](/help/search-social-commerce/introduction/supported-inventory.md), you can create and edit data for individual campaigns and campaign components directly in the interface. You can optionally export the data in most subviews to a spreadsheet file.

  >[!NOTE]
  >
  >Ad-level data isn&#39;t available for [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping, and [!DNL YouTube] campaigns.

* **[!UICONTROL Products]** — The [!UICONTROL Products] views show data for each [[!DNL Google] or [!DNL Microsoft] merchant center account that&#39;s synced](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). The default [!UICONTROL Accounts] subview lists all synced accounts; some user types can add new accounts from this view. The [!UICONTROL Products] subview lists each product within the account.

* **[!UICONTROL Advanced (ACM)]** —  From the [!DNL Advanced] ([!DNL AMC], for Advanced Campaign Management) view, you can set up automated processes to create [dynamic ads and keywords targeted to each item in your inventory](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) according to an ad network-specific ad template you create and the contents of [!DNL Google Merchant Center] accounts or inventory data files you upload to an FTP location. Subviews show details about each feed template for the advertiser and each campaign, ad group, keyword, and ad included in a feed that was propagated through a feed template but not posted to the ad network.

* **[!UICONTROL Bulksheets]** — Use the [!UICONTROL Bulksheets] view to create [bulksheet files](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) containing as much data as you want for an account on a [supported ad network](/help/search-social-commerce/introduction/supported-inventory.md), and then post them to the ad network.

* **[!UICONTROL Audiences]** — [The [!UICONTROL Audiences] views](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) lists all of your [!DNL Google Ads] and [!DNL Microsoft Advertising] audiences generated from various types of user lists. You can create [!DNL Google Ads] audiences from your existing Adobe CX Enterprise audiences and your customer email lists. You can also view and manage audience targets and exclusions for your [!DNL Google Ads] and [!DNL Microsoft Advertising] ads.

* **[!UICONTROL Label Classifications]** — Use this view to create and delete [label classifications](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), which can help you group your labels into meaningful sets.

>[!MORELIKETHIS]
>
>* [Overview of implementing ad network accounts and campaigns](campaign-implemention-overview.md)
>* [Monitor and manage the performance of your ad network campaigns](monitor-performance-campaigns.md)
>* [Google Ads conversion data in Search, Social, &amp; Commerce](google-conversion-data.md)
