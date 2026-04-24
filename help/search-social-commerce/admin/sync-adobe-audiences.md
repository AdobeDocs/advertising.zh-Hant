---
title: Sync [!DNL Adobe] audiences
description: Learn how to sync metadata, hierarchy data, and unique audience data for your [!DNL Adobe] audiences.
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
TQID: https://experienceleague.adobe.com/PKWhdnMHVAI3aI--1vdCeqnX6b8j34uvHycZLw1Yvjw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# Sync [!DNL Adobe] audiences

*[!DNL Direct Access]client managers and administrators only*

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

You can allow Search, Social, &amp; Commerce to pull in metadata, hierarchy data, and unique audience data for all of an advertiser&#39;s or agency&#39;s [!DNL Adobe] audiences into the [!UICONTROL Campaigns] > [!UICONTROL Audiences] views. This information includes data for:

* Adobe Audience Manager segments

* Adobe Analytics segments that are published to Adobe CX Enterprise

* Segments that are created using the Adobe CX Enterprise [!DNL Audience Library]

To be eligible, the advertiser or agency must implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) and provide its organization ID (formerly called [!DNL IMS Org ID]).

The initial sync takes about 24 hours. After that, data is synced in real time, with a one- to two- second delay.

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**。

1. Enter the unique organization ID for the advertiser&#39;s Adobe CX Enterprise account, and then click **[!UICONTROL Submit]**.

   If you don&#39;t know the advertiser&#39;s organization ID, look it up in the **[!UICONTROL IMS Org ID]** field in the advertiser&#39;s settings at [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [About audiences](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integration with Adobe CX Enterprise solutions and services](/help/search-social-commerce/introduction/integrations.md)
