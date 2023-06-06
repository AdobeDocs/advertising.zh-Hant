---
title: 關於購物產品群組
description: 瞭解購物行銷活動中的購物產品群組。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# 關於購物產品群組

*[!DNL Google Ads]和 [!DNL Microsoft Advertising] 僅限購物行銷活動*

在購物行銷活動中，您的產品群組（而非關鍵字）會決定您的商家中心帳戶中要顯示哪些購物廣告的產品。 每個產品群組都以單一產品屬性（例如，類別、產品型別、品牌、條件、產品ID或自訂標籤）為基礎，並對所有相符產品使用相同的出價。 您可以包含或排除每個群組中產品的競標。

您可以在廣告群組層級設定產品群組，以判斷您的商家中心帳戶中的哪些產品會出現在廣告群組的購物廣告中。 即使廣告群組不包含廣告實體，廣告網路仍會顯示產品的廣告。

當相同產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）符合廣告拍賣的資格。 當所有行銷活動具有相同的優先順序時，則符合最高競價的行銷活動條件。

如需有關的詳細資訊 [!DNL Google] 購物行銷活動和廣告，請參閱&quot;[實作 [!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)」和 [Google Ads檔案](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). 如需Microsoft購物行銷活動的詳細資訊，請參閱&quot;[實作 [!DNL Microsoft® Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)」和 [Microsoft廣告檔案](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>不提供支援 [!DNL Google Ads] 在最高成效行銷活動中列出群組，以取代智慧購物行銷活動。 若要管理和檢視清單群組的資料，請使用 [!DNL Google Ads] 編輯者。

## 產品群組階層

您必須先建立全包含式產品群組（稱為「 」），才能使用廣告群組的特定屬性建立產品群組[!UICONTROL All Products].」 您可以從此父項產品群組，為產品子集建立子項產品群組，也可以從子項產品群組建立子項。 一旦您為廣告群組建立了第一個子產品群組，另一個產品群組就會命名為「[!UICONTROL Everything Else]「是使用預設廣告群組競標自動建立的。 當您新增更多產品群組時，「[!UICONTROL Everything Else]「群組會適當地調整，以構成不在其他產品群組中的所有產品。

在廣告群組中，您最多可以建立七個層級的產品群組(不包括「 」[!UICONTROL All Products]&quot;)以包含競標或從競標排除，使一個或多個產品群組在每個層級定位相同的屬性(例如， [!UICONTROL Brand]=Acme代表一個產品群組和 [!UICONTROL Brand]=AcmePlus （相同層級的另一個使用者）。 父產品群組稱為細分，而細分的最低層次稱為單位。 您可以在單位層級設定競標和追蹤範本，或完全排除競標。 廣告群組的整組作用中產品群組會以階層方式套用，以判斷符合資格的產品。 例如，如果您將 [!UICONTROL All Products] 到 [!UICONTROL Brand]=AcmeBasic和 [!UICONTROL Brand]=AcmePlus，然後您進一步將這些產品群組細分為 [!UICONTROL Condition]=全新和設定的出價，則只有具有AcmeBasic和AcmePlus品牌的新產品才能在廣告中宣傳或排除在廣告之外。

![產品群組集範例](/help/search-social-commerce/assets/product-group-list.png "產品群組集範例")

![範例產品群組階層](/help/search-social-commerce/assets/product-group-tree.png "範例產品群組階層")

## 此 [!UICONTROL Product Groups] 檢視

您可以在「 」中建立及編輯產品群組，以及刪除產品群組及其子產品群組。 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 檢視。

## 購物產品群組的追蹤和效能資料

(帳戶/行銷活動具有&quot;[!UICONTROL EF Redirect]&quot;追蹤選項)若要允許Search、Social和Commerce追蹤產品群組的轉換， [使用追蹤URL工具產生產品群組的追蹤URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)，然後執行下列任一項作業：

* (以下專案為必要： [!DNL Google Ads]；的最佳作法 [!DNL Microsoft Advertising])將追蹤網址新增至 [!DNL Tracking Template] 「帳戶」、「促銷活動」或「產品群組」設定中的欄位。 為了便於維護，請儘可能在最高級別新增這些功能。 不包括為帳戶或行銷活動指定的任何附加引數。

   >[!CAUTION]
   >
   >([!DNL Microsoft Advertising])只有在產品摘要的自訂欄中未包含「搜尋」、「社交」和「商務」追蹤URL時，才使用此選項。 如果您同時執行兩者，URL將會包含兩個重新導向，並導致連結損毀。

* ([!DNL Microsoft Advertising] 僅限)將追蹤URL新增至內的產品資料 [!DNL Microsoft Merchant Center] 帳戶。 若要這麼做，請包含追蹤URL，連同 `link` 或 `mobile_link` 欄位（在自訂欄中適當時），稱為 [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) 在產品資訊源中。 使用此方法產生的URL不包含任何在Search、Social和Commerce的帳戶或行銷活動設定中指定的追蹤引數。

您可以在中檢視有關產品群組的資料 [此 [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [管理購物產品群組](product-group-manage.md)
>* [[!DNL Google Ads] 產品群組設定](product-group-settings-google.md)
>* [實作 [!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] 產品群組設定](product-group-settings-microsoft.md)
>* [實作 [!DNL Microsoft® Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)

