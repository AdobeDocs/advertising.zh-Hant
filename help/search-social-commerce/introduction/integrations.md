---
title: 與Adobe Experience Cloud解決方案和服務整合
description: 瞭解Search、Social和Commerce與Adobe Experience Cloud解決方案和服務的整合。
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# 與Adobe Experience Cloud解決方案和服務整合

Advertising Search、Social和Commerce已整合下列[!DNL Adobe]項產品。

* [來自Adobe Experience Platform的標籤](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — 您可以使用適用於Adobe Experience Platform的[Adobe Advertising Cloud擴充功能](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud)來[為您的廣告登陸頁面建立Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)以及協力廠商追蹤標籤。 如果您的組織沒有Experience Platform帳戶，您仍可以直接在Adobe Experience Cloud客戶免費取得的Adobe Experience Platform資料彙集[的](https://experience.adobe.com/#/data-collection/)使用者介面中安裝此擴充功能。

  若要安裝必要的擴充功能，請聯絡您的組織管理員，以取得在UI中資料收集功能的存取權，並要求他們授與您許可權`manage_properties`。

  **注意：**&#x200B;您也可以直接[在「搜尋」、「社交」和「Commerce」中建立轉換追蹤標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)。

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — （選擇加入功能） Adobe Advertising和[!DNL Analytics]已透過下列方式整合：

   * Adobe Advertising和[!DNL Analytics]可順暢地共用資料。 [!DNL Analytics]可以每天傳送網站互動和轉換資料至Search、Social和Commerce，以供其改善廣告和建立報表。 此外，Adobe Advertising亦可每天從您的廣告網路傳送廣告流量資料（包括曝光數、點按數和成本）至[!DNL Analytics]，以便該資料可在所有報告工具中使用。

     如需每個廣告網路和廣告型別[支援的詳細資訊，請參閱](/help/search-social-commerce/introduction/supported-inventory.md)支援的詳細目錄[!DNL Analytics]。 如需資料交換的詳細資訊，另請參閱&quot;[ [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}的概觀&quot;。

     若要交換資料，必須先設定Adobe Advertising和[!DNL Analytics]。 如需初始設定的詳細資訊，請聯絡您的Adobe客戶團隊。

     >[!NOTE]
     >
     >依預設，[!DNL Analytics]量度不會顯示在「搜尋」、「社交」和「Commerce」畫面中。 在[實作團隊已設定要傳遞至Adobe Advertising的選取標準或自訂事件後，您必須明確](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)讓量度可用於行銷活動管理檢視、投資組合及報告[!DNL Adobe]。 您可以選擇變更顯示的量度名稱（不需要在[!DNL Analytics]中變更它們）。 您可以在UI中檢視量度，以及從[!UICONTROL Admin] > [!UICONTROL Conversions]重新命名量度。

   * 具有[!DNL Analytics]但不具有Audience Manager的廣告商可以從與Adobe Experience Cloud共用的[區段中 [!DNL Google Ads] 建立](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)客戶相符對象[!DNL Analytics]。 廣告商必須實作[Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)並在其網站上部署標籤，才符合資格。 然後，您可以在[!DNL Google Ads]行銷活動中使用對象作為行銷活動層級或廣告群組層級[目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

* Adobe Audience Manager區段 — （選擇加入功能）您可以從將「搜尋」、「社交」和「Commerce」當作目的地的Audience Manager區段[建立 [!DNL Google Ads] 客戶相符對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 這可能包括發佈至Adobe Experience Cloud的[!DNL Analytics]區段，以及使用Adobe Experience Cloud對象庫建立的區段。 然後，您可以在[!DNL Google Ads]行銷活動中使用對象作為行銷活動層級或廣告群組層級[目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

  如需詳細資訊，請參閱[Adobe Advertising與Adobe Audience Manager的整合](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)。

* Adobe Target — 您可以在Search、Social和Commerce與[!DNL Target]之間實作點進訊號共用，在[!DNL Target]中為您的廣告設定A/B測試活動，然後使用[!DNL Analytics] Analysis Workspace檢視測試資料。

* Adobe Campaign — 您可以[使用 [!DNL Google Ads] 內的電子郵件清單，建立和更新 [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)客戶比對對象。

* Adobe Experience Cloud通知 — （透過Adobe Experience Cloud登入時）從每頁頂端的通知連結（[警示通知](/help/search-social-commerce/assets/notifications-panel.png "警示通知")）中，您可以檢視所有Adobe Experience Cloud系統更新、貼文、提及和共用的資產。 如需存取Adobe Experience Cloud的相關資訊，請聯絡您的Adobe客戶團隊。
