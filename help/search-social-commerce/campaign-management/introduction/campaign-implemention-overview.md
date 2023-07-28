---
title: 實作廣告網路帳戶和行銷活動的概觀
description: 瞭解設定、同步及管理廣告網路帳戶的相關工作。
exl-id: 401c5ebb-258c-4614-96e8-ca604fc698c0
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# 實作廣告網路帳戶和行銷活動的概觀

Adobe可與每個廣告商合作，設定其廣告網路帳戶和促銷活動。 這包括設定「搜尋」、「Social」和「Commerce」來連線廣告商的帳戶並與其同步、視需要建立新的行銷活動和行銷活動元件、設定元件廣告的追蹤、選擇將行銷活動新增至產品組合以允許「搜尋」、「Social」和「Commerce」最佳化廣告的競標，以及驗證初始成本、點選和收入資料。

啟用行銷活動並選擇性地新增至產品組合後，Adobe客戶管理團隊、機構團隊或廣告商（視服務等級協定的條款而定）將需要監視每個行銷活動，並視需要變更相關元件和設定以達成廣告商的目標。

此頁面包含所有帳戶型別的相關資訊，包括如何設定已同步帳戶的促銷活動結構。 有關設定僅限追蹤帳戶的其他指示 [!DNL Naver]，請參閱&quot;[實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).」

## 帳戶和行銷活動的初始設定任務

[!DNL Adobe] 及/或您的機構將與您合作，進行下列工作：

1. （新廣告商帳戶）設定管理帳戶：

   1. 設定廣告商的帳戶。

   1. （如有必要）為廣告商建立使用者帳戶，以檢視和管理其行銷活動資料並產生報表。

1. （部分廣告網路）取得「搜尋、社交和商務」的授權，可使用廣告網路的API和「搜尋、社交和商務」使用者介面存取每個帳戶。

1. 對於每個廣告網路帳戶：

   1. （如有必要）在廣告網路上設定帳戶。

   1. 透過以下方式與帳戶整合 [建立對應的帳戶記錄](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) 在包含帳戶存取認證和追蹤選項的「搜尋、社交和商務」中，將帳戶狀態設定為「已啟用」。

      然後搜尋、社交和商務會與廣告網路同步。 如果帳戶已包含行銷活動資料，則可在24小時內取得資料。

   1. ([您可以建立/編輯的廣告型別](/help/search-social-commerce/introduction/supported-inventory.md) （位於「搜尋、社交和商務」）如果帳戶尚未包含促銷活動資料，則透過以下適用於廣告型別的任意方法，從「搜尋、社交和商務」中建立促銷活動結構和促銷活動元件：

      * (Google Ads、Microsoft Advertising、Yahoo！ Ads，僅限Yandex帳戶)設定 [自動化程式，可針對您詳細目錄中的每個專案建立動態廣告和關鍵字](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 根據您建立的廣告網路專用廣告範本，以及您上傳至FTP位置的詳細目錄資料檔案內容。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ Japan Ads，僅限Yandex帳戶)上傳 [大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 包含您想要的帳戶資料，然後張貼至廣告網路。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ Japan Ads （僅限Yandex帳戶）將個別元件的資料直接輸入介面。 對於大多數行銷活動和廣告型別，您可以在行銷活動層級、廣告群組層級，以及個別關鍵字、版位和廣告層級建立資料。

      然而，有些行銷活動和廣告型別需要唯一的工作流程。 請參閱設定說明 [[!DNL Microsoft Advertising] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)， [[!DNL Google Ads] 動態搜尋廣告](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md)， [[!DNL Google Ads] 最高成效行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md)、和 [[!DNL Google Ads] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] 僅限追蹤的帳戶)上傳 [大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 有資料可複製Search、Social和Commerce中的現有行銷活動、廣告群組和關鍵字，無需將其張貼到 [!DNL Naver].

1. 設定Adobe Advertising將追蹤轉換之所有廣告的追蹤：

   1. (具有Adobe Advertising轉換追蹤服務的廣告商)如有需要， [設定點選追蹤](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) 適用於廣告，以及關鍵字、位置和廣告擴充功能的可選專案，方法是產生並上傳搜尋、社交和商務點選追蹤URL。

      的 [!DNL Google Ads] 最佳化行銷活動，設定中的所有追蹤 [行銷活動的追蹤設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. 若是僅限追蹤的促銷活動，您必須改用大量表單來產生目的地URL，然後使用廣告網路的原生編輯器將產生的目的地URL新增至相關實體。

   1. 設定轉換追蹤。 根據實作，這可能涉及將轉換追蹤標籤新增到廣告商的網頁，和/或針對廣告商已單獨收集的轉換資料設定每日摘要拖放。

      如果您使用Adobe Advertising轉換追蹤服務，即可產生轉換追蹤標籤 [在搜尋、社交和商務中](/help/search-social-commerce/tools/conversion-tag-generate.md) 或 [使用Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. 驗證所追蹤的資料。

   如需設定追蹤的詳細資訊，請參閱「追蹤」一章。

1. (使用Adobe Analytics的廣告商) [整合Adobe Advertising和Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) 以便交換資料。

1. (允許搜尋、社交和商務將競標和/或行銷活動預算最佳化； [支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md) 僅限) [將行銷活動指派至投資組合](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   如果產品組合尚未啟動（最佳化出價和/或預算），則讓最佳化功能收集足夠的資料，以便建立成本和收入模型，以便在啟動產品組合之前建立產品組合的基準績效。

   如果投資組合已啟動，則啟用投資組合的學習。 如需詳細資訊，請參閱「調整投資組合策略」。 當您新增行銷活動時，最佳化功能會收集行銷活動競標單位的資料，而產品組合可能會不穩定。 投標會在一到三週內自動調整。

   如需產品組合的詳細資訊，請參閱最佳化指南，此指南可在「搜尋、社交和商務」中取得。<!-- verify convention for referencing Optimization Guide here -->

1. （如果將會追蹤廣告商的任何新轉換） [讓轉換可供使用](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) 適用於報表、行銷活動管理檢視和產品組合目標。

1. 對於每個促銷活動，確認Search、Social和Commerce從廣告網路接收點按和成本資料，並使用廣告商自己的收入資料驗證Search、Social和Commerce中顯示的收入資料。

1. （選用）設定報表範本、試算表摘要及FTP傳送排程報表，以自動化報表。

   如需指示，請參閱「報表」一章。

>[!MORELIKETHIS]
>
>* [關於搜尋、社交和商務中的行銷活動管理](campaign-management-about.md)
>* [監視和管理廣告網路行銷活動的績效](monitor-performance-campaigns.md)
>* [搜尋、社交和商務中的Google Ads轉換資料](google-conversion-data.md)
>* [支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)
