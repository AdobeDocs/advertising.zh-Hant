---
title: 關於購物產品群組
description: 瞭解購物行銷活動中的購物產品群組。
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# 關於購物產品群組

*[!DNL Google Ads]和 [!DNL Microsoft Advertising] 僅限購物行銷活動*

在購物行銷活動中，您的產品群組（而非關鍵字）會決定您的商家中心帳戶中要顯示哪些購物廣告的產品。 每個產品群組都以單一產品屬性（例如，類別、產品型別、品牌、條件、產品ID或自訂標籤）為基礎，並對所有相符產品使用相同出價。 您可以加入或排除每個群組中產品的競標。

您可以在廣告群組層級設定產品群組，以決定您的商家中心帳戶中的哪些產品會出現在廣告群組的購物廣告中。 即使廣告群組不包含廣告實體，廣告網路仍會顯示產品的廣告。

當同一個產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）適用於廣告拍賣。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。

有關詳細資訊 [!DNL Google] 購物行銷活動和廣告，請參閱&quot;[實作 [!DNL Google Ads] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)」和 [Google Ads檔案](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). 有關詳細資訊 [!DNL Microsoft] 購物行銷活動，請參閱&quot;[實作 [!DNL Microsoft Advertising] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)」和 [[!DNL Microsoft Advertising] 檔案](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>不提供支援 [!DNL Google Ads] 在最高成效行銷活動中列出群組，以取代智慧購物行銷活動。 若要管理和檢視清單群組的資料，請使用 [!DNL Google Ads] 編輯者。

## 產品群組階層

您必須先建立全包含式產品群組（稱為「 」），才能使用廣告群組的特定屬性建立產品群組[!UICONTROL All Products].」 您可以從此父產品群組，建立產品子集的子產品群組，也可以從子產品群組建立子系。 當您為廣告群組建立第一個子產品群組後，就會出現另一個名為「[!UICONTROL Everything Else]「是使用預設廣告群組競標自動建立的。 當您新增更多產品群組時，「[!UICONTROL Everything Else]「群組已據此調整，因此其組成所有不在其他產品群組中的產品。

在廣告群組中，您最多可以建立七個層級的產品群組(不包括&quot;[!UICONTROL All Products]&quot;)包含競標或從中排除，使一個或多個產品群組在每個層級定位相同的屬性(例如， [!UICONTROL Brand]=Acme代表一個產品群組和 [!UICONTROL Brand]=AcmePlus （相同層級中的另一個）。 父產品群組稱為細分，而最低的細分層級稱為單位。 您可以在單位層級設定競標和追蹤範本，或完全排除競標。 廣告群組的整組作用中產品群組會依階層套用，以決定符合資格的產品。 例如，如果細分 [!UICONTROL All Products] 到 [!UICONTROL Brand]=AcmeBasic和 [!UICONTROL Brand]=AcmePlus，然後您進一步將這些產品群組細分為 [!UICONTROL Condition]=新的和設定的出價，則只有具有AcmeBasic和AcmePlus品牌的新產品才會在廣告中刊登或排除在廣告之外。

![產品群組集範例](/help/search-social-commerce/assets/product-group-list.png "產品群組集範例")

![範例產品群組階層](/help/search-social-commerce/assets/product-group-tree.png "範例產品群組階層")

## 此 [!UICONTROL Product Groups] 檢視

您可以建立和編輯產品群組，並刪除產品群組及其子產品群組，位於 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 檢視。

## 購物產品群組的追蹤和效能資料

(帳戶/促銷活動具有&quot;[!UICONTROL EF Redirect]「追蹤選項)若要允許搜尋、社交和Commerce追蹤產品群組的轉換， [使用追蹤URL工具產生產品群組的追蹤URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)，然後執行下列任一項作業：

* (下列專案需要： [!DNL Google Ads]；的最佳作法 [!DNL Microsoft Advertising])將追蹤網址新增至 [!DNL Tracking Template] 「帳戶」、「促銷活動」或「產品群組」設定的欄位。 為了便於維護，請儘可能在最高級別新增這些功能。 不包括為帳戶或行銷活動指定的任何附加引數。

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising])只有在產品摘要的自訂欄中未包含「搜尋」、「社交」和「Commerce」追蹤URL時，才使用此選項。 如果兩者都執行，URL將包含兩個重新導向，並導致連結損毀。

* ([!DNL Microsoft Advertising] 僅限)將追蹤URL新增至中的產品資料 [!DNL Microsoft Merchant Center] 帳戶。 若要這麼做，請納入追蹤URL，連同 `link` 或 `mobile_link` 欄位（在自訂欄中適當時），稱為 [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) 在產品資訊源中。 使用此方法產生的URL不包含帳戶中指定的任何追蹤引數，或搜尋、Social和Commerce內的促銷活動設定。

您可以在中檢視產品群組的相關資料 [此 [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [管理購物產品群組](product-group-manage.md)
>* [[!DNL Google Ads] 產品群組設定](product-group-settings-google.md)
>* [實作 [!DNL Google Ads] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] 產品群組設定](product-group-settings-microsoft.md)
>* [實作 [!DNL Microsoft Advertising] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
