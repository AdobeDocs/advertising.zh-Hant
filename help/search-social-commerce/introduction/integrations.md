---
title: 與Adobe Experience Cloud解決方案和服務整合
description: 瞭解Search、Social和Commerce與Adobe Experience Cloud解決方案和服務的整合。
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# 與Adobe Experience Cloud解決方案和服務整合

Advertising Search、Social和Commerce已整合下列[!DNL Adobe]項產品。

* [來自Adobe Experience Platform的標籤](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=zh-Hant) — 您可以使用適用於Adobe Experience Platform的[Adobe Advertising Cloud擴充功能](https://exchange.adobe.com/apps/ec/100155)，為您的廣告登陸頁面建立Adobe Advertising轉換追蹤標籤以及協力廠商追蹤標籤。 (您也可以直接[在「搜尋」、「社交」和「Commerce」](/help/search-social-commerce/tools/conversion-tag-generate.md)中建立轉換追蹤標籤。) 請聯絡您的Adobe客戶團隊或實作團隊，以取得要包含在標籤中的資訊。

* Adobe Analytics — （選擇加入功能）Adobe Advertising和[!DNL Analytics]會以下列方式整合：

   * Adobe Advertising與[!DNL Analytics]可順暢地共用資料。 [!DNL Analytics]可以每天傳送網站互動和轉換資料至Search、Social和Commerce，以供其改善廣告和建立報表。 此外，Adobe Advertising可以每天從您的廣告網路傳送廣告流量資料（包括曝光數、點按數和成本）至[!DNL Analytics]，以便在所有報告工具中取得這些資料。

     如需每個廣告網路和廣告型別[!DNL Analytics]支援的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。 如需資料交換的詳細資訊，另請參閱&quot;[&#x200B; [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=zh-Hant){target="_blank"}的概觀&quot;。

     若要交換資料，必須先設定Adobe Advertising和[!DNL Analytics]。 如需初始設定的詳細資訊，請聯絡您的Adobe客戶團隊。

     >[!NOTE]
     >
     >依預設，[!DNL Analytics]量度不會顯示在「搜尋」、「社交」和「Commerce」畫面中。 在[!DNL Adobe]實作團隊已設定要傳遞至Adobe Advertising的選取標準或自訂事件後，您必須明確[讓量度可用於行銷活動管理檢視、投資組合及報告](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)。 您可以選擇變更顯示的量度名稱（不需要在[!DNL Analytics]中變更它們）。 您可以在UI中檢視量度，以及從[!UICONTROL Admin] > [!UICONTROL Conversions]重新命名量度。

   * 具有[!DNL Analytics]但不Audience Manager的廣告商可以從與Adobe Experience Cloud共用的[!DNL Analytics]區段中[建立 [!DNL Google Ads] 客戶相符對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 廣告商必須實作[Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)並在其網站上部署標籤，才符合資格。 然後，您可以在[!DNL Google Ads]行銷活動中使用對象作為行銷活動層級或廣告群組層級[目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

* Adobe Audience Manager區段 — （選擇加入功能）您可以從將「搜尋」、「社交」和「Commerce」當作目的地的Audience Manager區段[建立 [!DNL Google Ads] 客戶相符對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 這可能包括發佈至Adobe Experience Cloud的[!DNL Analytics]區段，以及使用Adobe Experience Cloud對象庫建立的區段。 然後，您可以在[!DNL Google Ads]行銷活動中使用對象作為行銷活動層級或廣告群組層級[目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

  如需詳細資訊，請參閱「[Adobe Advertising與Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html?lang=zh-Hant)的整合」。

* Adobe Target — 您可以在Search、Social和Commerce與[!DNL Target]之間實作點進訊號共用，在[!DNL Target]中為您的廣告設定A/B測試活動，然後使用[!DNL Analytics] Analysis Workspace檢視測試資料。

* Adobe Campaign — 您可以[使用 [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)內的電子郵件清單，建立和更新 [!DNL Google Ads] 客戶比對對象。

* Adobe Experience Cloud通知 — (透過Adobe Experience Cloud登入時)從每頁頂端的通知連結（[警示通知](/help/search-social-commerce/assets/notifications-panel.png "警示通知")）中，您可以檢視所有Adobe Experience Cloud系統更新、貼文、提及和共用的資產。 如需存取Adobe Experience Cloud的相關資訊，請聯絡您的Adobe客戶團隊。
