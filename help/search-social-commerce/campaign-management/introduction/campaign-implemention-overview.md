---
title: 實作廣告網路帳戶和行銷活動的概觀
description: 瞭解設定、同步和管理您的廣告網路帳戶的相關工作。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# 實作廣告網路帳戶和行銷活動的概觀

Adobe可與每個廣告商合作，設定其廣告網路帳戶和促銷活動。 這包括設定Search、Social和Commerce來連線廣告商帳戶並與之同步、視需要建立新的行銷活動和行銷活動元件、設定元件廣告的追蹤、選擇將行銷活動新增至產品組合，以允許Search、Social和Commerce最佳化廣告競標，以及驗證初始成本、點選和收入資料。

啟用行銷活動並選擇性新增至產品組合後，Adobe客戶管理團隊、機構團隊或廣告商（視服務等級合約的條款而定）將需要監視每個行銷活動，並視需要變更相關元件和設定，以達到廣告商的目標。

此頁面包含所有帳戶型別的相關資訊，包括如何設定已同步化帳戶的促銷活動結構。 有關設定追蹤帳戶的其他指示 [!DNL Naver]，請參閱「[實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).」

## 帳戶和行銷活動的初始設定任務

[!DNL Adobe] 及/或您的機構將與您合作進行下列工作：

1. （新廣告商帳戶）設定管理帳戶：

   1. 設定廣告商的帳戶。

   1. （如有必要）為廣告商建立使用者帳戶，以檢視和管理其行銷活動資料並產生報表。

1. （部分廣告網路）取得「搜尋、社交和商務」的授權，以使用廣告網路的API和「搜尋、社交和商務」使用者介面存取每個帳戶。

1. 對於每個廣告網路帳戶：

   1. （如有需要）在廣告網路上設定帳戶。

   1. 與帳戶整合依據 [建立對應的帳戶記錄](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) 在包含帳戶存取認證和追蹤選項的「搜尋、社交和商務」中，將帳戶狀態設定為「已啟用」。

      然後搜尋、Social和Commerce會與廣告網路同步。 如果帳戶已包含行銷活動資料，則可在24小時內取得資料。

   1. ([您可以建立/編輯的廣告型別](/help/search-social-commerce/introduction/supported-inventory.md) （位於搜尋、Social和Commerce中）如果帳戶尚未包含行銷活動資料，則透過以下任何可用於廣告型別的方法，從Search、Social和Commerce中建立行銷活動結構和行銷活動元件：

      * (Google Ads、Microsoft Advertising、Yahoo！ Ads和Yandex帳戶)設定 [建立動態廣告和關鍵字的自動化程式，其目標鎖定在您的詳細目錄中的每個專案](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 根據您建立的廣告網路特定廣告範本，以及您上傳至FTP位置的詳細目錄資料檔案內容。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ Japan Ads和Yandex帳戶)上傳 [大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 包含您想要的帳戶資料量，然後張貼至廣告網路。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ Japan Ads，僅限Yandex帳戶)將個別元件的資料直接輸入介面。 對於大多數行銷活動和廣告型別，您可以在行銷活動層級、廣告群組層級，以及個別關鍵字、版位和廣告層級建立資料。
      不過，有些行銷活動和廣告型別需要唯一的工作流程。 請參閱設定說明 [[!DNL Microsoft Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)， [[!DNL Google Ads] 動態搜尋廣告](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md)， [[!DNL Google Ads] 最高成效行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md)、和 [[!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] 僅限追蹤的帳戶)上傳 [大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 有資料可在Search、Social和Commerce中複製現有行銷活動、廣告群組和關鍵字，無需將其張貼至 [!DNL Naver].


1. 設定Adobe廣告將追蹤轉換之所有廣告的追蹤：

   1. (廣告商與Adobe廣告轉換追蹤服務)如有必要， [設定點選追蹤](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) 適用於廣告，以及關鍵字、版位和廣告擴充功能的可選專案，透過產生和上傳搜尋、社交和商務點選追蹤URL進行。

      對象 [!DNL Google Ads] 最高成效行銷活動，設定 [行銷活動的追蹤設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. 針對僅限追蹤的行銷活動，您必須改用大量表單產生目的地URL，然後使用廣告網路的原生編輯器將產生的目的地URL新增至相關實體。

   1. 設定轉換追蹤。 根據實作，這可能涉及將轉換追蹤標籤新增到廣告商的網頁，和/或針對廣告商已單獨收集的轉換資料設定每日摘要拖放。

      如果您使用Adobe廣告轉換追蹤服務，即可產生轉換追蹤標籤 [在Search、Social和Commerce中](/help/search-social-commerce/tools/conversion-tag-generate.md) 或 [使用Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. 驗證所追蹤的資料。

   如需設定追蹤的詳細資訊，請參閱「追蹤」一章。

1. (使用Adobe Analytics的廣告商) [整合Adobe Advertising和Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) 以便交換資料。

1. (允許搜尋、社交和商務將競標和/或行銷活動預算最佳化； [支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md) 僅限) [將行銷活動指派至投資組合](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   如果產品組合尚未啟動（最佳化競標和/或預算），則讓最佳化功能收集足夠的資料，以便建立成本和收入模型，讓您在啟動產品組合之前建立產品組合的基準績效。

   如果投資組合已啟動，則啟用投資組合的學習。 如需詳細資訊，請參閱「調整投資組合策略」。 在新增行銷活動後，雖然最佳化功能會收集行銷活動競標單位的資料，但您應預期產品組合會不穩定。 競標會自動在一至三週內調整。

   如需關於產品組合的詳細資訊，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。<!-- verify convention for referencing Optimization Guide here -->

1. （如果將會追蹤廣告商的任何新轉換） [讓轉換可用](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) 報表、行銷活動管理檢視和產品組合目標。

1. 對於每個行銷活動，確認Search、Social和Commerce從廣告網路接收點按和成本資料，並使用廣告商自己的收入資料驗證Search、Social和Commerce中顯示的收入資料。

1. （可選）設定報表範本、試算表摘要及排程報表的FTP傳送，以自動化報表。

   如需指示，請參閱「報表」一章。

>[!MORELIKETHIS]
>
>* [關於Search、Social和Commerce中的促銷活動管理](campaign-management-about.md)
>* [監控及管理廣告網路行銷活動的效能](monitor-performance-campaigns.md)
>* [搜尋、社交和商務中的Google Ads轉換資料](google-conversion-data.md)
>* [支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)

