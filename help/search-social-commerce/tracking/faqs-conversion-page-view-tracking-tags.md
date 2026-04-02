---
title: 關於Adobe Advertising轉換和頁面檢視追蹤標籤的常見問題集
description: 請參閱Adobe Advertising轉換與頁面檢視追蹤標籤的比較。
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ckLRjqXGTShwM2TTyULRKjPwL5RYVWkiVVSkwMmvxE8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# 關於Adobe Advertising轉換和頁面檢視追蹤標籤的常見問題集

下列專案適用於Adobe Advertising轉換追蹤標籤和頁面檢視追蹤標籤。

| | 具有ECID的JS標籤 | JS第3版標籤 | JS版本2標籤 | 影像標籤 |
| ---- | ---- | ---- | ---- | ---- |
| 可以在與其他JS版本相同的網頁上使用 | — | — | — | 不適用 |
| 允許在同一網頁上使用具有相同廣告商使用者ID的多個標籤 | 是 | 是 | 是 | — |
| 允許在同一個網頁上使用具有不同廣告商使用者ID的多個標籤 | 是 | 是 | — | — |
| 供Adobe Experience Platform的Adobe Advertising擴充功能使用，並與使用Experience Platform產生的其他標籤相容 | 是 | 是 | — | — |
| 允許與Adobe Advertising JavaScript轉換對應標籤一起使用時，追蹤源自[!DNL Apple Safari]和[!DNL Mozilla Firefox]的所有轉換 | 是 | 是 | 是 | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* 所有新實作都使用JavaScript版本3。
>* 具有ECID的JavaScript標籤使用[Adobe Experience Cloud ID (ECID) Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html)以及舊版ef_id和gsurferid來測量轉換。 此最新標籤會建立[第一方Experience Cloud s_ecid Cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html)，並提供與其他Experience Cloud產品更緊密整合的功能。
>* 只有在廣告商的網頁上已實作標籤時，才使用JavaScript第2版標籤。
>* 最佳實務是使用JavaScript標籤，而非影像標籤，除非網站設有禁止使用這些標籤的原則。
>* 廣告商若想要鎖定在Adobe Experience Cloud中建立、在Adobe Audience Manager中建立或從Audience Manager或Adobe Analytics發佈至Adobe Experience Cloud的受眾，則需要JavaScript標籤。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [產生Adobe Advertising轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript轉換追蹤標籤格式3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript轉換追蹤標籤2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)版的格式
>* [影像轉換追蹤標籤的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!--
 add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
