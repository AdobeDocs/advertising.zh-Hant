---
title: 實作 [!DNL Google Ads] 購物行銷活動
description: 瞭解設定 [!DNL Google Ads] 購物行銷活動的工作流程。
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 實施[!DNL Google Ads]購物行銷活動

購物行銷活動中的廣告會使用您現有[!DNL Google Merchant Center]產品摘要中的產品相關資料（而非關鍵字），來決定顯示廣告的方式和位置。

[!DNL Google Ads]行銷活動可使用[!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network]&quot;鎖定目標[!DNL Google Shopping Network]。 [!DNL Google Shopping]行銷活動的設定包含優先順序（[!UICONTROL High]、[!UICONTROL Medium]或[!UICONTROL Low]）。 您可以選擇使用行銷活動層級設定，在購物廣告中顯示當地詳細目錄資訊。

您可以在廣告群組層級設定多重層級&#x200B;*[產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)*，以控制哪些產品會與您的購物廣告一起顯示。 產品群組是以任何產品屬性（類別、產品型別、品牌、條件、產品ID和自訂標籤）為基礎，您可以建立最多七個層級的產品群組，以納入競標或從競標排除。 您可以針對所有相符產品使用相同出價，在最低層級產品群組設定出價。 當同一個產品包含在多個行銷活動中時，[!DNL Google Ads]會先使用行銷活動層級的優先順序來判斷哪個行銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。

## 設定[!DNL Google Ads]購物行銷活動的步驟

您可以使用[!DNL Google Shopping]的[詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)、使用[大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)或個別使用，來設定購物行銷活動。 下列指示包含建立個別實體的連結。

1. 設定您的[!DNL Google Merchant Center]帳戶，並填入產品資料。

1. [允許搜尋、社交和Commerce從 [!DNL Google Merchant Center] 帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)下載資料。

1. [在購物網路上建立行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)。

1. [在行銷活動中建立廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，並設定所有廣告的預設競標。

   您可以覆寫個別產品群組的預設競標。

1. 為廣告群組建立產品群組：

   1. [建立「所有產品」產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. （選擇性） [建立子產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   >[!NOTE]
   >您不需要建立購物廣告。 即使廣告群組不包含廣告實體，[!DNL Google Ads]仍會顯示產品的廣告。

1. （選擇性）若要追蹤廣告上的點按，[使用追蹤URL工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生追蹤URL，然後將其新增至帳戶、行銷活動或產品群組設定。

1. [產生[!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)和[該[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)以監視效能。

1. 必要時：

   1. [編輯行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)以調整行銷活動預算。

      如果行銷活動屬於產品組合的一部分，則產品組合設定&quot;[!UICONTROL Auto adjust campaign budget limits]&quot;可讓Search、Social和Commerce最佳化產品組合中所有行銷活動的預算。

   1. [調整現有產品群組的最高出價](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)、[刪除您不再想要建立廣告的產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)，或新增[新的「所有產品」產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)或[新的子產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)以建立其他產品的廣告。

>[!NOTE]
>
>* 檢視使用[大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)和[詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md)管理[!DNL Google Shopping]行銷活動和產品群組的必要欄位。
>* 如需[!DNL Google Shopping]行銷活動的詳細資訊，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/2454022)。
