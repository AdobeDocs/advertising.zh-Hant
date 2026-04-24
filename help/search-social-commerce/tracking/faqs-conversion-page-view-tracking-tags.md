---
title: FAQs about Adobe Advertising conversion and page view tracking tags
description: See a comparison of the Adobe Advertising conversion and page view tracking tags.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ckLRjqXGTShwM2TTyULRKjPwL5RYVWkiVVSkwMmvxE8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 45b15880c20d516e4bab1ec664a45ebdf8ffbdcc
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 0%

---

# FAQs about Adobe Advertising conversion and page view tracking tags

The following apply to Adobe Advertising conversion tracking tags and page view tracking tags.

| | JS Tags with ECID | JS Version 3 Tags | JS Version 2 Tags | Image Tags |
| ---- | ---- | ---- | ---- | ---- |
| Can be used on the same webpage as another JS version | — | — | — | n/a |
| Allows the use of multiple tags with the same advertiser user IDs on the same webpage | Yes | Yes | Yes | — |
| Allows the use of multiple tags with different advertiser user IDs on the same webpage | Yes | Yes | — | — |
| Used by the Adobe Advertising extension for Adobe Experience Platform, and compatible with other tags generated using Experience Platform | Yes | Yes | — | — |
| Allows all conversions that originate from [!DNL Apple Safari] and [!DNL Mozilla Firefox] to be tracked when used with the Adobe Advertising JavaScript conversion mapping tag | Yes | Yes | Yes | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* All new implementations use JavaScript Version 3.
>* The JavaScript tag with ECID uses the [Adobe Experience Cloud ID (ECID) Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hant) as well as the legacy ef_id and gsurferid to measure conversions. This latest tag creates [first-party CX Enterprise s_ecid cookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html?lang=zh-Hant) and provides tighter integration with other CX Enterprise products.
>* Use JavaScript Version 2 tags only when they&#39;re already implemented tags on the advertiser&#39;s webpages.
>* The best practice is to use JavaScript tags instead of image tags unless the site has a policy against using them.
>* JavaScript tags are required for advertisers who want to target audiences created in Adobe CX Enterprise, created in Adobe Audience Manager, or published to Adobe CX Enterprise from Audience Manager or Adobe Analytics.

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generate an Adobe Advertising conversion tag](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript轉換追蹤標籤格式3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript轉換追蹤標籤2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)版的格式
>* [影像轉換追蹤標籤的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!--
 add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
