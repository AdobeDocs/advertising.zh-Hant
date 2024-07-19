---
title: 實作 [!DNL Microsoft Advertising] 購物行銷活動
description: 瞭解設定 [!DNL Microsoft Advertising] 購物行銷活動的工作流程。
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 實施[!DNL Microsoft Advertising]購物行銷活動

購物行銷活動中的廣告會使用您現有[!DNL Microsoft Merchant Center]產品摘要中的產品相關資料（而非關鍵字），來決定顯示廣告的方式和位置。

[!DNL Microsoft]購物行銷活動目標為[!DNL Microsoft Advertising Shopping Network]。 購物行銷活動的設定包含指定的產品銷售國家/地區和優先順序（[!DNL High]、[!DNL Medium]或[!DNL Low]）。 您可以選擇篩選詳細目錄，以廣告宣傳具有特定屬性的產品，以及鎖定或排除特定位置和裝置型別。

您可以在廣告群組層級設定多重層級&#x200B;*[產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)*，以控制哪些產品會與您的購物廣告一起顯示。 產品群組是以任何產品屬性（類別、產品型別、品牌、條件、產品ID和自訂標籤）為基礎，您最多可以建立7個層級的產品群組，以納入或排除出價，不包括&quot;[!DNL Add Products]&quot;。 您可以針對所有相符產品使用相同出價，在最低層級產品群組設定出價。 當同一個產品包含在多個行銷活動中時，[!DNL Microsoft Advertising]會先使用行銷活動層級的優先順序來判斷哪個行銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。

## 設定[!DNL Microsoft Advertising]購物行銷活動的步驟

您可以使用[!DNL Microsoft Advertising]的[詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)、使用[大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)或個別使用，來設定購物行銷活動。 下列指示包含建立個別實體的連結。

1. 設定您的[!DNL Microsoft Merchant Center]帳戶，並填入產品資料。

1. [允許搜尋、社交和Commerce從 [!DNL Microsoft Merchant Center] 帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)下載資料。

1. [在購物網路上建立行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)。

1. [在行銷活動中建立廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，並設定所有廣告的預設競標。

   您可以覆寫個別產品群組的預設競標。

1. 為廣告群組建立產品群組：

   1. [建立「所有產品」產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. （選擇性） [建立子產品群組](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. 建立[產品廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) （包含[促銷活動行），以可能包含在廣告群組中的每個購物廣告](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md)中。

      Microsoft Advertising會動態產生每個廣告的廣告復本和登陸頁面URL。

      >[!NOTE]
      >
      >即使廣告群組不包含廣告實體，[!DNL Microsoft Advertising]仍會顯示產品的廣告。

1. （選擇性）若要追蹤廣告上的點選次數，[請使用追蹤URL工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生追蹤URL。 最佳實務是將追蹤URL新增至帳戶、行銷活動或產品群組設定中的[!UICONTROL Tracking Template]欄位。 為了便於維護，請儘可能在最上層新增。

   或者，您也可以將追蹤URL新增至[!DNL Microsoft Merchant Center]帳戶內的產品資料。 若要這麼做，請在產品摘要的自訂欄「[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)」中，加入追蹤URL以及適當的「連結」或「mobile_link」欄位中的值。 「bingads_redirect」欄位中的值會取代「link」和「mobile_link」欄位中的值。 使用此方法產生的URL不包含任何在「搜尋」、「社交」和「Commerce」帳戶或促銷活動設定中指定的追蹤引數。

1. 由[產生[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)來監視效能。

1. 必要時：

   1. [編輯行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)以調整行銷活動預算。

      如果行銷活動屬於產品組合的一部分，則產品組合設定&quot;[!UICONTROL Auto adjust campaign budget limits]&quot;可讓Search、Social和Commerce最佳化產品組合中所有行銷活動的預算。

   1. 調整現有產品群組的最高出價、刪除您不再想要建立廣告的產品群組，或新增「所有產品」產品群組或新的子產品群組，以建立其他產品的廣告。

>[!NOTE]
>
>* 檢視使用[大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)和[詳細目錄摘要範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md)管理[!DNL Microsoft Shopping]行銷活動和產品群組的必要欄位。
>* 如需[!DNL Microsoft Shopping]行銷活動的詳細資訊，請參閱[[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/50903)。
