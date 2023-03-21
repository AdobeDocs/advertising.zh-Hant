---
title: Adobe廣告整合Adobe Analytics
description: 了解Adobe廣告如何與Adobe Analytics交換資料，以及如何在搜尋、社交和商務中使用資料。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: def6a3a8d1de1f9f80dee6ecd1a18667afc79fd3
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Adobe廣告整合Adobe Analytics

您可以透過下列方式整合Adobe廣告與Analytics。

## 之間交換資料 [!A分析] 和Adobe廣告

### 提取 [!A分析] 資料放入Adobe廣告

使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] 和DSP加入：

* **[!DNL Analytics]區段：**  在下列位置建立之廣告商或代理的所有區段的中繼資料、階層資料和不重複對象資料： [!DNL Analytics] 並發佈至Experience Cloud。

* **[!DNL Analytics]網站參與量度**

* **[!DNL Analytics]標準、自訂和保留量度**

### 傳送Adobe廣告資料至 [!A分析]

* **來自Adobe廣告的流量量度**

* **Dimension來自Adobe廣告**

>[!NOTE]
>
>針對 [!DNL Search, Social, & Commerce]，則大部分的廣告網路和行銷活動類型都支援此功能。 請參閱 [!DNL Search, Social, & Commerce] 指南，以取得詳細資訊。<!-- add link when that's published in ExL -->

### 使用 [!DNL Analytics] 要建立的區段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*選擇加入的廣告商 [!DNL Advertising Search, Social, & Commerce] 僅限*

<!-- Verify all -->

內 [!DNL Search, Social, & Commerce]，您可以建立 [!DNL Google Ads] Google客戶會使用您現有的 [!DNL Analytics] 區段。 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]. 如需詳細資訊，請參閱 [!DNL Search, Social, & Commerce].

[客戶比對來自使用者ID的受眾](https://support.google.com/google-ads/answer/9199250) 類似網站標籤型受眾，但會將非PII ID指派給不重複受眾成員，以獲得比標準客戶比對和網站標籤型受眾更明顯的優點。

若要建立必要的使用者ID，您必須使用Adobe廣告JavaScript標籤 <!-- with a user ID parameter -->在您的網站上。 如需詳細資訊，請連絡您的Adobe帳戶團隊。

![區段建立程式](/help/integrations/assets/ad_search_user_id_pic.png)

建立對象後，即可在 [!DNL Google Ads] 行銷活動 [促銷活動層級或廣告群組層級的目標或排除](#audience-manager-targets).

### 使用 [!DNL Analytics] 要定位或排除廣告的區段 {#analytics-targets}

* (選擇加入的廣告商搭配 [!DNL Search, Social, & Commerce])您可以使用 [!DNL Google Ads] 對象 [使用 [!DNL Analytics] 區段](#audience-manager-google-audiences) 作為促銷活動層級或廣告群組層級的目標或排除 [!DNL Google Ads] 行銷活動。

* (具有DSP的廣告商)您可以使用現有的 [!DNL Analytics] 區段作為廣告版位的目標。 您可以選擇將區段納入可重複使用的對象中，以用作多個版位的目標或排除。

* （廣告商與廣告創意）您可以使用現有的 [!DNL Analytics] 區段作為廣告體驗中特定創意的目標。
