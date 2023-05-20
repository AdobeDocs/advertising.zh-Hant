---
title: Adobe廣告與Adobe Analytics的整合
description: 瞭解Adobe廣告如何與Adobe Analytics交換資料，以及如何在搜索、社交和商務中使用資料。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 06996ee9eb635fe204c0c3938e6937e8871c8a90
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Adobe廣告與Adobe Analytics的整合

您可以通過以下方式將Adobe廣告與分析整合。

## 交換資料 [!DNL Analytics] 和Adobe廣告

### 拉 [!DNL Analytics] 資料到Adobe廣告

與 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)。[!DNL Search, Social, & Commerce] 並DSP拉入：

* **[!DNL Analytics]分部：**  建立於的廣告商或代理的所有網段的元資料、層次結構資料和唯一受眾資料 [!DNL Analytics] 出版給Experience Cloud。

* **[!DNL Analytics]站點項目指標**

* **[!DNL Analytics]標準、自定義和保留度量**

### 將Adobe廣告資料發送到 [!DNL Analytics]

* **來自Adobe廣告的流量指標**

* **DimensionAdobe廣告**

>[!NOTE]
>
>對於 [!DNL Search, Social, & Commerce]，此功能對大多數廣告網路和市場活動類型都受支援。 請參閱中的「支援的清單」 [!DNL Search, Social, & Commerce] 的子菜單。<!-- add link when that's published in ExL -->

### 使用 [!DNL Analytics] 要建立的段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*具有 [!DNL Advertising Search, Social, & Commerce] 僅*

<!-- Verify all -->

在 [!DNL Search, Social, & Commerce]，您可以建立 [!DNL Google Ads] Google客戶使用現有ID與用戶受眾匹配 [!DNL Analytics] 段。 這包括發佈給Adobe Experience Cloud的Adobe Analytics部分和使用Adobe Experience Cloud建立的部分 [!DNL Audience Library]。 有關詳細資訊，請參閱 [!DNL Search, Social, & Commerce]。

[客戶與用戶ID的受眾匹配](https://support.google.com/google-ads/answer/9199250) 像基於網站標籤的受眾一樣工作，但會將非PII ID分配給唯一的受眾成員，以獲得比標準客戶匹配和基於網站標籤的受眾更明顯的好處。

要建立必要的用戶ID，必須使用Adobe廣告JavaScript標籤 <!-- with a user ID parameter -->在你的網站上。 請聯繫您的Adobe客戶團隊以瞭解詳細資訊。

![段建立過程](/help/integrations/assets/ad_search_user_id_pic.png)

建立受眾後，您可以在 [!DNL Google Ads] 活動 [市場活動級或廣告組級目標或排除](#audience-manager-targets)。

### 使用 [!DNL Analytics] 目標或排除廣告的段 {#analytics-targets}

* (具有 [!DNL Search, Social, & Commerce])可以使用 [!DNL Google Ads] 觀眾 [建立時 [!DNL Analytics] 段](#audience-manager-google-audiences) 作為市場活動級別或廣告組級別目標或排除項 [!DNL Google Ads] 活動。

* (具有的廣DSP告商)您可以使用現有 [!DNL Analytics] 作為廣告投放的目標。 您可以選擇將段包括在可重複使用的受眾中，您可以將這些段用作多個放置的目標或排除。

* （具有廣告創意的廣告商）您可以使用現有 [!DNL Analytics] 作為廣告體驗中特定創意的目標。
