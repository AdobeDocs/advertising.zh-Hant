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

## 資料交換介於 [!DNL Analytics] 和Adobe Advertising

### 提取 [!DNL Analytics] 將資料匯入Adobe Advertising

替換為 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)，[!DNL Search, Social, & Commerce] 和DSP提取專案：

* **[!DNL Analytics]區段：**  在中建立之所有廣告商或代理商區段的中繼資料、階層資料和唯一受眾資料 [!DNL Analytics] 並發佈至Experience Cloud。

* **[!DNL Analytics]網站參與量度**

* **[!DNL Analytics]標準、自訂和保留的量度**

### 傳送Adobe Advertising資料至 [!DNL Analytics]

* **來自Adobe Advertising的流量量度**

* **來自Adobe Advertising的Dimension**

>[!NOTE]
>
>的 [!DNL Search, Social, & Commerce]中，大部分的廣告網路和促銷活動型別都支援此功能。 請參閱以下主題中的「支援詳細目錄」： [!DNL Search, Social, & Commerce] 指南，以取得詳細資訊。<!-- add link when that's published in ExL -->

### 使用 [!DNL Analytics] 要建立的區段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*選擇加入的廣告商，搭配 [!DNL Advertising Search, Social, & Commerce] 僅限*

<!-- Verify all -->

範圍 [!DNL Search, Social, & Commerce]，您可以建立 [!DNL Google Ads] Google客戶使用您現有的從使用者ID比對對象 [!DNL Analytics] 區段。 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]. 如需詳細資訊，請參閱&quot;[建立 [!DNL Google Ads] 客戶比對來自的對象 [!DNL Adobe] 對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).」

[客戶比對來自使用者ID的受眾](https://support.google.com/google-ads/answer/9199250) 類似網站標籤型受眾的運作方式，但非PII ID會指派給不重複受眾成員，以享有標準客戶比對和網站標籤型受眾的不同優點。

若要建立必要的使用者ID，您必須使用Adobe Advertising的JavaScript標籤 <!-- with a user ID parameter -->在您的網站上。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

![區段建立流程](/help/integrations/assets/ad_search_user_id_pic.png)

建立對象後，您便可以在以下位置使用它們： [!DNL Google Ads] 行銷活動為 [行銷活動層級或廣告群組層級目標或排除專案](#audience-manager-targets).

### 使用 [!DNL Analytics] 要鎖定或排除廣告的區段 {#analytics-targets}

* (選擇加入的廣告商，搭配 [!DNL Search, Social, & Commerce])您可以使用任何 [!DNL Google Ads] 曾經是 [建立方式 [!DNL Analytics] 區段](#audience-manager-google-audiences) 作為行銷活動層級或廣告群組層級目標或排除專案，在 [!DNL Google Ads] 行銷活動。

* (使用DSP的廣告商)您可以使用現有的 [!DNL Analytics] 區段作為廣告投放的目標。 您可以選擇將區段納入可重複使用的受眾中，將其用於多個位置的鎖定目標或排除專案。

* (具有Advertising Creative的廣告商)您可以使用現有的 [!DNL Analytics] 區段作為廣告體驗中特定創意的目標。
