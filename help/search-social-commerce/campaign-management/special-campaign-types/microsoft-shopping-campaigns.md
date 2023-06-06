---
title: 實作 [!DNL Microsoft® Advertising] 購物行銷活動
description: 瞭解設定的工作流程 [!DNL Microsoft® Advertising] 購物行銷活動。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# 實作 [!DNL Microsoft® Advertising] 購物行銷活動

購物行銷活動中的廣告會使用您現有廣告中產品的相關資料 [!DNL Microsoft® Merchant Center] 產品摘要（而非關鍵字）將決定顯示廣告的方式和位置。

[!DNL Microsoft®] 購物行銷活動目標為 [!DNL Microsoft® Advertising Shopping Network]. 購物行銷活動的設定包括銷售產品的指定國家/地區和優先順序([!DNL High]， [!DNL Medium]，或 [!DNL Low])。 您可以選擇篩選詳細目錄，以廣告具有特定屬性的產品，以及鎖定或排除特定位置和裝置型別。

您可以透過設定多層級，控制哪些產品會與您的購物廣告一起顯示 *[產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* 在廣告群組層級。 產品群組是以任何產品屬性（類別、產品型別、品牌、條件、產品ID和自訂標籤）為基礎，而您最多可以建立7個層級的產品群組，以納入競標或排除在競標之外，但不包括「[!DNL Add Products].」 您可以針對所有相符產品使用相同的競標，在最低層級產品群組設定競標。 當同一個產品包含在多個行銷活動中時， [!DNL Microsoft® Advertising] 會先使用行銷活動層級優先順序來判斷哪個行銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則符合最高競價的行銷活動條件。

## 設定步驟 [!DNL Microsoft® Advertising] 購物行銷活動

您可以使用設定購物行銷活動 [詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 的 [!DNL Microsoft® Advertising]，使用 [大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，或個別執行。 下列指示包含建立個別實體的連結。

1. 設定您的 [!DNL Microsoft® Merchant Center] 帳戶，並填入產品資料。

1. [允許搜尋、社交和商務從以下位置下載資料： [!DNL Microsoft® Merchant Center] 帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [建立行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 在購物網路上。

1. [建立廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ，並為所有廣告設定預設競標。

您可以覆寫個別產品群組的預設競標。

1. 為廣告群組建立產品群組：

   1. [建立「所有產品」產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. （可選） [建立子產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. 建立 [產品廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 替換為 [可能包含在每個購物廣告中的促銷活動行](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) 在廣告群組中。

      Microsoft® Advertising會動態產生每個廣告的廣告文案和登陸頁面URL。

      >[!NOTE]
      >
      >即使廣告群組不包含廣告實體， [!DNL Microsoft® Advertising] 仍會顯示產品的廣告。

1. （選用）若要追蹤廣告的點按次數， [使用「追蹤URL」工具產生追蹤URL](/help/search-social-commerce/tools/click-tracking-url-generate.md). 最佳實務是將追蹤URL新增至 [!UICONTROL Tracking Template] 「帳戶」、「促銷活動」或「產品群組」設定中的欄位。 為便於維護，請儘可能在最高級別新增。

   或者，您也可以將追蹤URL新增至 [!DNL Microsoft® Merchant Center] 帳戶。 若要這麼做，請將追蹤URL連同「link」或「mobile_link」欄位（如果適用）中的值，一併納入自訂欄»[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)」在產品資訊源中。 「bingads_redirect」欄位中的值會取代「link」和「mobile_link」欄位中的值。 使用此方法產生的URL不包含任何在Search、Social和Commerce帳戶或行銷活動設定中指定的追蹤引數。

1. 監控效能依據 [產生 [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. 必要時：

   1. [編輯行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 以調整行銷活動預算。

      如果行銷活動是產品組合的一部分，則產品組合設定&quot;[!UICONTROL Auto adjust campaign budget limits]&quot;可讓Search、Social和Commerce最佳化產品組合中所有行銷活動的預算。

   1. 調整現有產品群組的最高出價、刪除您不再想要建立廣告的產品群組，或新增「所有產品」產品群組或新的子產品群組，以針對其他產品建立廣告。

>[!NOTE]
>
>* 檢視管理所需的欄位 [!DNL Microsoft® Shopping] 行銷活動和產品群組使用 [大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) 和 [詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* 如需有關的詳細資訊 [!DNL Microsoft® Shopping] 行銷活動，請參閱 [[!DNL Microsoft® Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/50903).

