---
title: 實作廣告網路帳戶和行銷活動的概觀
description: 瞭解設定、同步及管理廣告網路帳戶的相關工作。
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# 實作廣告網路帳戶和行銷活動的概觀

Adobe可與每個廣告商合作，設定其廣告網路帳戶和促銷活動。 這包括設定Search、Social和Commerce來連線廣告商的帳戶並與其同步、視需要建立新的行銷活動和行銷活動元件、設定元件廣告的追蹤、選擇將行銷活動新增至產品組合以允許Search、Social和Commerce最佳化廣告競標，以及驗證初始成本、點選和收入資料。

啟用行銷活動並選擇性地新增至產品組合後，Adobe客戶管理團隊、機構團隊或廣告商（視服務等級協定的條款而定）將需要監視每個行銷活動，並視需要變更相關元件和設定以達成廣告商的目標。

此頁面包含所有帳戶型別的相關資訊，包括如何設定已同步帳戶的促銷活動結構。 如需為[!DNL Naver]設定僅追蹤帳戶的其他指示，請參閱[實作 [!DNL Naver] 僅追蹤帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)。

## 帳戶和行銷活動的初始設定任務

[!DNL Adobe]和/或您的機構將與您合作進行下列工作：

1. （新廣告商帳戶）設定管理帳戶：

   1. 設定廣告商的帳戶。

   1. （如有必要）為廣告商建立使用者帳戶，以檢視和管理其行銷活動資料並產生報表。

1. （部分廣告網路）取得搜尋、社交和Commerce的授權，以使用廣告網路的API和搜尋、社交和Commerce使用者介面存取每個帳戶。

1. 對於每個廣告網路帳戶：

   1. （如有必要）在廣告網路上設定帳戶。

   1. 透過[在Search、Social和Commerce中建立包含帳戶存取認證和追蹤選項的對應帳戶記錄](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account)，並將帳戶狀態設定為enabled，與帳戶整合。

      然後搜尋、社交和Commerce會與廣告網路同步。 如果帳戶已包含行銷活動資料，則可在24小時內取得資料。

   1. ([您可以在Search、Social和Commerce中建立/編輯](/help/search-social-commerce/introduction/supported-inventory.md)的廣告型別)如果帳戶尚未包含行銷活動資料，則透過以下任何可用於廣告型別的方法，從Search、Social和Commerce中建立行銷活動結構和行銷活動元件：

      * (Google Ads、Microsoft Advertising、Yahoo！ 僅限廣告和Yandex帳戶)設定[自動化程式，以根據您建立的廣告網路特定廣告範本，以及您上傳至FTP位置的詳細目錄資料檔案內容，建立針對詳細目錄中的每個專案的動態廣告和關鍵字](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ Japan Ads，僅限Yandex帳戶)上傳[大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，其中包含您想要的帳戶資料量，然後再張貼至廣告網路。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ Japan Ads （僅限Yandex帳戶）將個別元件的資料直接輸入介面。 對於大多數行銷活動和廣告型別，您可以在行銷活動層級、廣告群組層級，以及個別關鍵字、版位和廣告層級建立資料。

      然而，有些行銷活動和廣告型別需要唯一的工作流程。 請參閱設定[[!DNL Microsoft Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)、[[!DNL Google Ads] 動態搜尋廣告](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md)、[[!DNL Google Ads] 最高成效行銷活動](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md)和[[!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)的說明。

   1. （僅限[!DNL Naver]個追蹤帳戶）上傳含有資料的[大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，以復寫Search、Social和Commerce中的現有行銷活動、廣告群組和關鍵字，而不需將其發佈至[!DNL Naver]。

1. 設定Adobe Advertising將追蹤轉換之所有廣告的追蹤：

   1. (使用Adobe Advertising轉換追蹤服務的廣告商)如有必要，請產生/上傳搜尋、社交和Commerce點選追蹤URL，以[設定廣告的點選追蹤](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)，並可選擇設定關鍵字、刊登版位和廣告副檔名。

      針對[!DNL Google Ads]最高成效行銷活動，請在[行銷活動的追蹤設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)中設定所有追蹤。

1. 若是僅限追蹤的促銷活動，您必須改用大量表單來產生目的地URL，然後使用廣告網路的原生編輯器將產生的目的地URL新增至相關實體。

   1. 設定轉換追蹤。 根據實作，這可能涉及將轉換追蹤標籤新增到廣告商的網頁，和/或針對廣告商已單獨收集的轉換資料設定每日摘要拖放。

      如果您使用Adobe Advertising轉換追蹤服務，則可以使用Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html)在Search、Social和Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md)內產生轉換追蹤標籤[或[。

   1. 驗證所追蹤的資料。

   如需設定追蹤的詳細資訊，請參閱「追蹤」一章。

1. (使用Adobe Analytics的廣告商) [整合Adobe Advertising和Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)，以便交換資料。

1. (允許搜尋、Social和Commerce最佳化出價、行銷活動預算和/或行銷活動出價策略目標；僅[支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)) [將行銷活動指派給產品組合](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md)。

   如果產品組合尚未啟動（最佳化出價和/或預算），則讓最佳化功能收集足夠的資料，以便建立成本和收入模型，以便在啟動產品組合之前建立產品組合的基準績效。

   如果投資組合已啟動，則啟用投資組合的學習。 如需詳細資訊，請參閱「調整投資組合策略」。 當您新增行銷活動時，最佳化功能會收集行銷活動競標單位的資料，而產品組合可能會不穩定。 投標會在一到三週內自動調整。

   如需產品組合的詳細資訊，請參閱Search、Social和Commerce中的「最佳化指南」。<!-- verify convention for referencing Optimization Guide here -->

1. （如果將會追蹤廣告商的任何新轉換） [讓轉換可用於報告、行銷活動管理檢視和產品組合目標](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)。

1. 對於各個促銷活動，確認Search、Social和Commerce收到來自廣告網路的點按和成本資料，並使用廣告商自己的收入資料驗證Search、Social和Commerce中顯示的收入資料。

1. （選用）設定報表範本、試算表摘要及FTP傳送排程報表，以自動化報表。

   如需指示，請參閱「報表」一章。

>[!MORELIKETHIS]
>
>* [關於搜尋、社交和Commerce中的行銷活動管理](campaign-management-about.md)
>* [監視和管理廣告網路行銷活動的績效](monitor-performance-campaigns.md)
>* [搜尋、社交和Commerce中的Google廣告轉換資料](google-conversion-data.md)
>* [支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)
