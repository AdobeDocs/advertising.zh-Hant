---
title: 關於Adobe Advertising轉換和頁面檢視追蹤標籤的常見問題集
description: 請參閱Adobe Advertising轉換與頁面檢視追蹤標籤的比較。
exl-id: 5eb414a7-2f96-47de-b157-a17851653206
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 關於Adobe Advertising轉換和頁面檢視追蹤標籤的常見問題集

下列專案適用於Adobe Advertising轉換追蹤標籤和頁面檢視追蹤標籤。

| | 具有ECID的JS標籤 | JS第3版標籤 | JS版本2標籤 | 影像標籤 |
| ---- | ---- | ---- | ---- | ---- |
| 可以在與其他JS版本相同的網頁上使用 | — | — | — | 不適用 |
| 允許在同一網頁上使用具有相同廣告商使用者ID的多個標籤 | 是 | 是 | 是 | — |
| 允許在同一個網頁上使用具有不同廣告商使用者ID的多個標籤 | 是 | 是 | 否 | 否 |
| 供Adobe Experience Platform的Adobe Advertising擴充功能使用，並與使用Experience Platform產生的其他標籤相容 | 是 | 是 | — | — |
| 允許源自下列專案的所有轉換： [!DNL Apple Safari] 和 [!DNL Mozilla Firefox] 與Adobe AdvertisingJavaScript轉換對應標籤搭配使用時要追蹤的專案 | 是 | 是 | 是 | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* 所有新實作都使用JavaScript版本3。
>* 含ECID的JavaScript標籤會使用 [Adobe Experience Cloud ID (ECID)服務](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 以及舊版ef_id和gsurferid來測量轉換。 此最新標籤會建立 [第一方Experience Clouds_ecid Cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) 並提供與其他Experience Cloud產品更緊密的整合。
>* 只有在廣告商的網頁上已實施JavaScript 2版標籤時，才使用JavaScript 2標籤。
>* 最佳實務是使用JavaScript標籤，而非影像標籤，除非網站有禁止使用這些標籤的原則。
>* 廣告商若想要鎖定在Adobe Experience Cloud中建立、在Adobe Audience Manager中建立或從Audience Manager或Adobe Analytics發佈至Adobe Experience Cloud的受眾，則需要JavaScript標籤。

>[!MORELIKETHIS]
>
>* [關於Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [產生Adobe Advertising轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript轉換追蹤標籤第3版的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript轉換追蹤標籤第2版的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [影像轉換追蹤標籤的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
