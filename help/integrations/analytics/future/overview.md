---
title: Adobe Advertising與Adobe Analytics的整合
description: 瞭解Adobe Advertising如何與Adobe Analytics交換資料，以及如何在Search、Social和Commerce中使用資料。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Adobe Advertising與Adobe Analytics的整合

您可以透過下列方式整合Adobe Advertising與Analytics。

## 在[!DNL Analytics]和Adobe Advertising之間交換資料

### 將[!DNL Analytics]資料提取至Adobe Advertising

透過[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)、[!DNL Search, Social, & Commerce]和DSP提取：

* **[!DNL Analytics]區段：**&#x200B;在[!DNL Analytics]中建立並發佈至Experience Cloud的所有廣告商或機構區段的中繼資料、階層資料和不重複受眾資料。

* **[!DNL Analytics]網站參與量度**

* **[!DNL Analytics]標準、自訂和保留的量度**

### 將Adobe Advertising資料傳送至[!DNL Analytics]

* 來自Adobe Advertising **的**&#x200B;流量量度

* 來自Adobe Advertising **的** Dimension

>[!NOTE]
>
>對於[!DNL Search, Social, & Commerce]，大部分廣告網路和行銷活動型別都支援此功能。 如需詳細資訊，請參閱[!DNL Search, Social, & Commerce]指南中的「支援的詳細目錄」。<!-- add link when that's published in ExL -->

### 使用[!DNL Analytics]區段來建立[!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*只選擇加入[!DNL Advertising Search, Social, & Commerce]的廣告商*

<!-- Verify all -->

在[!DNL Search, Social, & Commerce]內，您可以使用現有的[!DNL Analytics]區段，從使用者ID建立[!DNL Google Ads]個Google客戶比對對象。 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud [!DNL Audience Library]建立的區段。 如需詳細資訊，請參閱&quot;[建立 [!DNL Google Ads] 來自 [!DNL Adobe] 對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)的客戶比對對象。&quot;

[來自使用者ID的客戶相符對象](https://support.google.com/google-ads/answer/9199250)的工作方式與網站標籤型對象類似，但會將非PII ID指派給不重複對象成員，以區別於標準客戶相符和網站標籤型對象的好處。

若要建立必要的使用者ID，您必須在您的網站上使用Adobe Advertising的JavaScript標籤<!-- with a user ID parameter -->。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

![區段建立程式](/help/integrations/assets/ad_search_user_id_pic.png)

建立對象後，您可以在[!DNL Google Ads]行銷活動中將其用作[行銷活動層級或廣告群組層級目標或排除專案](#audience-manager-targets)。

### 使用[!DNL Analytics]區段來鎖定目標或排除廣告 {#analytics-targets}

* （選擇加入的廣告商具有[!DNL Search, Social, & Commerce]）您可以使用任何[!DNL Google Ads]對象，這些對象是[使用 [!DNL Analytics] 區段](#audience-manager-google-audiences)建立的，在您的[!DNL Google Ads]行銷活動中作為行銷活動層級或廣告群組層級目標或排除專案。

* (使用DSP的廣告商)您可以使用現有的[!DNL Analytics]區段作為廣告刊登的目標。 您可以選擇將區段納入可重複使用的受眾中，將其用於多個位置的鎖定目標或排除專案。

* (具有Advertising Creative的廣告商)您可以使用現有的[!DNL Analytics]區段，作為廣告體驗中特定創意內容的目標。
