---
title: 與Adobe Experience Cloud解決方案和服務整合
description: 瞭解Search、Social和Commerce與Adobe Experience Cloud解決方案和服務的整合。
source-git-commit: 0c19479cb8ef4e9e037a46ab72f75b7423de5073
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 與Adobe Experience Cloud解決方案和服務整合

Advertising Search、Social和Commerce已整合以下專案 [!DNL Adobe] 產品。

* [來自Adobe Experience Platform的標籤](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html)  — 您可以使用 [Adobe Advertising Cloud擴充功能](https://exchange.adobe.com/apps/ec/100155) ，以便Adobe Experience Platform為您的廣告登陸頁面建立Adobe廣告轉換追蹤標籤，以及第三方追蹤標籤。 (您也可以 [直接在Search、Social和Commerce中建立轉換追蹤標籤](/help/search-social-commerce/tools/conversion-tag-generate.md).) 請聯絡您的Adobe客戶團隊或實作團隊，以取得要包含在標籤中的資訊。

* Adobe Analytics — （選擇加入功能）Adobe廣告和 [!DNL Analytics] 會以下列方式整合：

   * Adobe廣告和 [!DNL Analytics] 順暢地共用資料。 [!DNL Analytics] 可每天傳送網站互動和轉換資料至Search、Social和Commerce，以供其改善廣告和建立報表。 此外，Adobe廣告可每天從您的廣告網路傳送廣告流量資料（包括曝光數、點按數和成本）至 [!DNL Analytics]，資料可在所有報告工具中使用。

      請參閱「[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)」以取得更多關於 [!DNL Analytics] 支援每個廣告網路和廣告型別。 另請參閱&quot;[概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)」以取得資料交換的詳細資訊。

      若要交換資料，請同時使用Adobe廣告和 [!DNL Analytics] 必須初始設定。 如需初始設定的詳細資訊，請聯絡您的Adobe客戶團隊。

      >[!NOTE]
      >
      >根據預設， [!DNL Analytics] 量度在「搜尋」、「社交」和「商務」畫面中不可見。 您必須明確 [讓量度可用於行銷活動管理檢視、投資組合和報表](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) 晚於 [!DNL Adobe] 實作團隊已將選取的標準或自訂事件設定為傳遞至Adobe廣告。 您可以選擇變更顯示的量度名稱（而不需在中變更它們） [!DNL Analytics])。 您可以讓量度在UI中可供檢視，並從以下位置重新命名量度： [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * 廣告商使用 [!DNL Analytics] 但Audience Manager不能 [建立 [!DNL Google Ads] 客戶比對對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) 從 [!DNL Analytics] 與Adobe Experience Cloud共用的區段。 廣告商必須實作 [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) 並在其網站上部署標籤。 然後，您便可以在以下位置使用對象： [!DNL Google Ads] 行銷活動層級或廣告群組層級 [目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) 或 [排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager區段 — （選擇加入功能）您可以 [建立 [!DNL Google Ads] 客戶比對對象](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) 從以「搜尋」、「社交」和「商務」作為目的地的Audience Manager區段。 這可能包括 [!DNL Analytics] 發佈至Adobe Experience Cloud的區段，以及使用Adobe Experience Cloud對象庫建立的區段。 然後，您便可以在以下位置使用對象： [!DNL Google Ads] 行銷活動層級或廣告群組層級 [目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) 或 [排除專案](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

   請參閱「[AdobeAdvertising與Adobe Audience Manager的整合](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)」以取得詳細資訊。

* Adobe Target — 您可以在Search、Social和Commerce之間實施點進訊號共用，以及 [!DNL Target]，在中設定A/B測試活動 [!DNL Target] ，然後使用 [!DNL Analytics] Analysis Workspace以檢視測試資料。

* Adobe Campaign — 您可以 [建立和更新 [!DNL Google Ads] 使用電子郵件清單的客戶比對對象，範圍： [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud通知 — (當您透過Adobe Experience Cloud登入時)從通知連結([警示通知](/help/search-social-commerce/assets/notifications-panel.png "警示通知"))在每個頁面頂端，您可以檢視所有Adobe Experience Cloud系統更新、貼文、提及和共用的資產。 如需存取Adobe Experience Cloud的相關資訊，請聯絡您的Adobe客戶團隊。

