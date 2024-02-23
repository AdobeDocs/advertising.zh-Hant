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

## 同步Audience Manager和其他 [!DNL Adobe] 廣告定位的區段

[!DNL Search, Social, & Commerce] 而DSP可針對廣告商或機構的所有其他Audience Manager，提取中繼資料、階層資料以及不重複受眾資料 [!DNL Adobe] 對象。 此唯一連線僅適用於使用Adobe Advertising的行銷人員。 請參閱&quot;[匯入Adobe Audience Manager區段以鎖定廣告](/help/integrations/audience-manager/import-audiences.md).」

### 使用Audience Manager和其他 [!DNL Adobe] 要建立的區段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*選擇加入的廣告商，搭配 [!DNL Advertising Search, Social, & Commerce] 僅限*

範圍 [!DNL Search, Social, & Commerce]，您可以建立 [!DNL Google Ads] Audience Manager客戶比對來自使用者ID的受眾，使用您具備 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作為目的地。 ([!DNL Media Optimizer] 是以前的名稱 [!DNL Search, Social, & Commerce].) 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]. 如需詳細資訊，請參閱&quot;[建立 [!DNL Google Ads] 客戶比對來自的對象 [!DNL Adobe] 對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).」

[客戶比對來自使用者ID的受眾](https://support.google.com/google-ads/answer/9199250) 類似網站標籤型受眾的運作方式，但非PII ID會指派給不重複受眾成員，以享有標準客戶比對和網站標籤型受眾的不同優點。

若要建立必要的使用者ID，您必須使用Adobe Advertising的JavaScript標籤 <!-- with a user ID parameter -->在您的網站上。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

![區段建立流程](/help/integrations/assets/ad_search_user_id_pic.png)

建立對象後，您便可以在以下位置使用它們： [!DNL Google Ads] 行銷活動為 [行銷活動層級或廣告群組層級目標或排除專案](#audience-manager-targets).

### 使用Audience Manager和其他 [!DNL Adobe] 要鎖定或排除廣告的區段 {#audience-manager-targets}

* (選擇加入的廣告商，搭配 [!DNL Search, Social, & Commerce])您可以使用任何 [!DNL Google Ads] 曾經是 [建立方式 [!DNL Adobe] 區段](#audience-manager-google-audiences) 作為行銷活動層級或廣告群組層級目標或排除專案，在 [!DNL Google Ads] 行銷活動。

* (使用DSP的廣告商)您可以使用現有的 [!DNL Adobe] 區段作為廣告投放的目標。 您可以選擇將區段納入可重複使用的受眾中，將其用於多個位置的鎖定目標或排除專案。

* (具有Advertising Creative的廣告商)您可以使用現有的 [!DNL Adobe] 區段作為廣告體驗中特定創意的目標。

>[!NOTE]
>
>如需如何在Audience Manager和Experience Cloud中建立對象的詳細資訊 [!DNL Audience Library] 介面以及不同對象型別的常見使用案例，請參閱&quot;[對象建立選項](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).」

## 將DSP媒體曝光度資料傳送至Audience Manager

*僅使用DSP的廣告商*

具有Adobe Audience Manager的DSP客戶可以使用畫素呼叫來Audience Manager，從廣告促銷活動擷取資料。 接著，您可以使用行銷活動資料建立規則型特徵，並用來定義新區段，以啟用各種DSP使用案例，例如更進階分割、頻率管理、行銷分析和報表深入分析。

請參閱&quot;[傳送DSP Media Exposure資料至Adobe Audience Manager概述](/help/integrations/audience-manager/media-data-integration/overview.md)」以取得詳細資訊。

## 透過Audience Analytics獲得更豐富的網站活動見解

Adobe Advertising客戶使用 [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可傳送追蹤Adobe Advertising的資料和Audience Manager區段至 [!DNL Analytics] 以取得關於網站活動的深入分析。

如需詳細資訊，請參閱&quot;[[!DNL Adobe Audience Analytics] Adobe Advertising客戶](/help/integrations/audience-manager/audience-analytics.md).」
