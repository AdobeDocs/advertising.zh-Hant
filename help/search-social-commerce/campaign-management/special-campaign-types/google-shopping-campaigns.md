---
title: 實作 [!DNL Google Ads] 購物宣傳
description: 瞭解設定的工作流程 [!DNL Google Ads] 購物行銷活動。
exl-id: aab61d94-861f-4072-b044-f9ae6759e028
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 實作 [!DNL Google Ads] 購物宣傳

購物行銷活動中的廣告會使用您現有產品中的相關資料 [!DNL Google Merchant Center] 由產品摘要（而非關鍵字）決定顯示廣告的方式和位置。

[!DNL Google Ads] 行銷活動可以鎖定目標 [!DNL Google Shopping Network] 使用 [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].」 的設定 [!DNL Google Shopping] 行銷活動包含優先順序([!UICONTROL High]， [!UICONTROL Medium]，或 [!UICONTROL Low])。 您可以選擇使用行銷活動層級設定，在購物廣告中顯示當地詳細目錄資訊。

您可以透過設定多層級，控制哪些產品會與您的購物廣告一起顯示 *[產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* 在廣告群組層級。 產品群組是以任何產品屬性（類別、產品型別、品牌、條件、產品ID和自訂標籤）為基礎，您可以建立最多七個層級的產品群組，以納入競標或從競標排除。 您可以針對所有相符產品使用相同出價，在最低層級產品群組設定出價。 同一個產品包含在多個行銷活動中時， [!DNL Google Ads] 會先使用行銷活動層級的優先順序，以判斷哪個行銷活動（及相關競標）適用於廣告拍賣。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。

## 設定步驟 [!DNL Google Ads] 購物宣傳

您可以使用來設定購物行銷活動 [詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 的 [!DNL Google Shopping]，使用 [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，或個別執行。 下列指示包含建立個別實體的連結。

1. 設定您的 [!DNL Google Merchant Center] 帳戶，並填入產品資料。

1. [允許搜尋、社交和商務從 [!DNL Google Merchant Center] 帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [建立行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 在購物網路上。

1. [建立廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ，並為所有廣告設定預設競標。

您可以覆寫個別產品群組的預設競標。

1. 為廣告群組建立產品群組：

   1. [建立「所有產品」產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. （可選） [建立子產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >您不需要建立購物廣告。 即使廣告群組不包含廣告實體， [!DNL Google Ads] 仍會顯示產品的廣告。

1. （選用）若要追蹤廣告的點按次數， [使用追蹤URL工具產生追蹤URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)，然後將其新增至帳戶、行銷活動或產品群組設定。

1. 監控效能依據 [產生 [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) 和 [此 [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. 必要時：

   1. [編輯行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 以調整行銷活動預算。

      如果行銷活動是產品組合的一部分，則產品組合設定&quot;[!UICONTROL Auto adjust campaign budget limits]&quot;可讓Search、Social和Commerce最佳化產品組合中所有行銷活動的預算。

   1. [調整現有產品群組的最高出價](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)， [刪除產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) 您不再想要為其建立廣告，或新增 [全新「所有產品」產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md))或 [新的子產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) 為其他產品製作廣告。

>[!NOTE]
>
>* 檢視管理所需的欄位 [!DNL Google Shopping] 行銷活動和產品群組使用 [Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) 和 [詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* 有關詳細資訊 [!DNL Google Shopping] 行銷活動，請參閱 [[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/2454022).
