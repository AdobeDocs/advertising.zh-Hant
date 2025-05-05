---
title: Adobe Advertising與Adobe Audience Manager的整合
description: 瞭解Adobe Advertising與Adobe Audience Manager交換資料的各種方式。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Adobe Advertising與Adobe Audience Manager的整合

您可以透過下列方式整合Adobe Advertising與Audience Manager。

## 同步廣告目標定位的Audience Manager和其他[!DNL Adobe]區段

[!DNL Search, Social, & Commerce]和DSP可以提取廣告商或機構所有Audience Manager和其他[!DNL Adobe]個對象的中繼資料、階層資料和不重複對象資料。 此唯一連線僅適用於使用Adobe Advertising的行銷人員。 請參閱&quot;[匯入廣告目標定位的Adobe Audience Manager區段](/help/integrations/audience-manager/import-audiences.md)&quot;。

### 使用Audience Manager和其他[!DNL Adobe]區段來建立[!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*只選擇加入[!DNL Advertising Search, Social, & Commerce]的廣告商*

在[!DNL Search, Social, & Commerce]內，您可以使用將[!UICONTROL Adobe Media Optimizer (HTTP)]和[!UICONTROL Adobe Media Optimizer Batch Destination]作為目的地的現有Audience Manager區段，從使用者ID建立[!DNL Google Ads]個客戶比對對象。 （[!DNL Media Optimizer]是[!DNL Search, Social, & Commerce]的舊名稱。） 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud [!DNL Audience Library]建立的區段。 如需詳細資訊，請參閱&quot;[建立 [!DNL Google Ads] 來自 [!DNL Adobe] 對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)的客戶比對對象。&quot;

[來自使用者ID的客戶相符對象](https://support.google.com/google-ads/answer/9199250)的工作方式與網站標籤型對象類似，但會將非PII ID指派給不重複對象成員，以區別於標準客戶相符和網站標籤型對象的好處。

若要建立必要的使用者ID，您必須在您的網站上使用Adobe Advertising的JavaScript標籤<!-- with a user ID parameter -->。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

![區段建立程式](/help/integrations/assets/ad_search_user_id_pic.png)

建立對象後，您可以在[!DNL Google Ads]行銷活動中將其用作[行銷活動層級或廣告群組層級目標或排除專案](#audience-manager-targets)。

### 使用Audience Manager和其他[!DNL Adobe]區段來鎖定目標或排除廣告 {#audience-manager-targets}

* （選擇加入的廣告商具有[!DNL Search, Social, & Commerce]）您可以使用任何[!DNL Google Ads]對象，這些對象是[使用 [!DNL Adobe] 區段](#audience-manager-google-audiences)建立的，在您的[!DNL Google Ads]行銷活動中作為行銷活動層級或廣告群組層級目標或排除專案。

* (使用DSP的廣告商)您可以使用現有的[!DNL Adobe]區段作為廣告刊登的目標。 您可以選擇將區段納入可重複使用的受眾中，將其用於多個位置的鎖定目標或排除專案。

* (具有Advertising Creative的廣告商)您可以使用現有的[!DNL Adobe]區段，作為廣告體驗中特定創意內容的目標。

>[!NOTE]
>
>如需有關如何在Audience Manager和Experience Cloud[!DNL Audience Library]介面中建立對象，以及不同對象型別的常見使用案例的詳細資訊，請參閱&quot;[對象建立選項](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=zh-Hant)&quot;。

## 將DSP媒體曝光度資料傳送至Audience Manager

*僅使用DSP的廣告商*

具有Adobe Audience Manager的DSP客戶可以使用畫素呼叫來Audience Manager，從廣告促銷活動擷取資料。 接著，您可以使用行銷活動資料建立規則型特徵，並用來定義新區段，以啟用各種DSP使用案例，例如更進階分割、頻率管理、行銷分析和報表深入分析。

如需詳細資訊，請參閱[傳送DSP媒體曝光資料至Adobe Audience Manager的概觀](/help/integrations/audience-manager/media-data-integration/overview.md)。

## 透過Audience Analytics獲得更豐富的網站活動見解

具有[[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=zh-Hant)的Adobe Advertising客戶可以傳送Adobe Advertising追蹤資料和Audience Manager區段至[!DNL Analytics]，以取得有關網站活動的豐富見解。

如需詳細資訊，請參閱[[!DNL Adobe Audience Analytics] Adobe Advertising客戶](/help/integrations/audience-manager/audience-analytics.md)。
