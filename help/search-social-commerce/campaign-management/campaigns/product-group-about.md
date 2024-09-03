---
title: 關於購物產品群組
description: 瞭解購物行銷活動中的購物產品群組。
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# 關於購物產品群組

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]購物行銷活動*

在購物行銷活動中，您的產品群組（而非關鍵字）會決定您的商家中心帳戶中要顯示哪些購物廣告的產品。 每個產品群組都以單一產品屬性（例如，類別、產品型別、品牌、條件、產品ID或自訂標籤）為基礎，並對所有相符產品使用相同出價。 您可以加入或排除每個群組中產品的競標。

您可以在廣告群組層級設定產品群組，以決定您的商家中心帳戶中的哪些產品會出現在廣告群組的購物廣告中。 即使廣告群組不包含廣告實體，廣告網路仍會顯示產品的廣告。

當同一個產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）適用於廣告拍賣。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。

如需[!DNL Google]購物行銷活動和廣告的詳細資訊，請參閱[實作 [!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)和[Google廣告檔案](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1)。 如需[!DNL Microsoft]購物行銷活動的詳細資訊，請參閱[實作 [!DNL Microsoft Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)和[[!DNL Microsoft Advertising] 檔案](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500)。

>[!NOTE]
>
>[!DNL Google Ads]無法提供支援，因為列出最高成效行銷活動中的群組，這些行銷活動正在取代智慧購物行銷活動。 若要管理和檢視清單群組的資料，請使用[!DNL Google Ads]編輯器。

## 產品群組階層

您必須先建立名為「[!UICONTROL All Products]」的全包含式產品群組，才能使用廣告群組的特定屬性建立產品群組。 您可以從此父產品群組，建立產品子集的子產品群組，也可以從子產品群組建立子系。 一旦您為廣告群組建立第一個子產品群組，就會使用預設廣告群組競標，自動建立另一個名為「[!UICONTROL Everything Else]」的產品群組。 當您新增更多產品群組時，&quot;[!UICONTROL Everything Else]&quot;群組會適當地調整，使其構成不在其他產品群組中的所有產品。

在廣告群組內，您可以建立最多七個層級的產品群組（不包括&quot;[!UICONTROL All Products]&quot;）來包含或排除競標，且每個層級中一或多個產品群組皆以相同屬性為目標（例如，[!UICONTROL Brand]=Acme代表一個產品群組，[!UICONTROL Brand]=AcmePlus代表另一個相同層級）。 父產品群組稱為細分，而最低的細分層級稱為單位。 您可以在單位層級設定競標和追蹤範本，或完全排除競標。 廣告群組的整組作用中產品群組會依階層套用，以決定符合資格的產品。 例如，如果您將[!UICONTROL All Products]細分為[!UICONTROL Brand]=AcmeBasic和[!UICONTROL Brand]=AcmePlus，然後進一步將每個產品群組細分為[!UICONTROL Condition]=New和設定出價，則只有具有AcmeBasic和AcmePlus品牌的新產品才會被廣告或從廣告中排除。

![產品群組集範例](/help/search-social-commerce/assets/product-group-list.png "產品群組集範例")

![產品群組階層範例](/help/search-social-commerce/assets/product-group-tree.png "產品群組階層範例")

## [!UICONTROL Product Groups]檢視

您可以在[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups]檢視中建立和編輯產品群組，以及刪除產品群組及其子產品群組。

## 購物產品群組的追蹤和效能資料

（具有「[!UICONTROL EF Redirect]」追蹤選項的帳戶/行銷活動）若要允許搜尋、社交和Commerce追蹤產品群組的轉換，[使用「追蹤URL」工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)產生產品群組的追蹤URL，然後執行下列任一項作業：

* （[!DNL Google Ads]的必要專案；[!DNL Microsoft Advertising]的最佳實務）將追蹤URL新增至帳戶、行銷活動或產品群組設定中的[!DNL Tracking Template]欄位。 為了便於維護，請儘可能在最高級別新增這些功能。 不包括為帳戶或行銷活動指定的任何附加引數。

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising])只有在產品摘要的自訂欄中未包含「搜尋」、「社交」和「Commerce」追蹤URL時，才使用此選項。 如果兩者都執行，URL將包含兩個重新導向，並導致連結損毀。

* （僅限[!DNL Microsoft Advertising]）將追蹤URL新增至[!DNL Microsoft Merchant Center]帳戶內的產品資料。 若要這麼做，請在產品摘要內名為[`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0)的自訂欄位中，加入追蹤URL以及適當的`link`或`mobile_link`欄位中的值。 使用此方法產生的URL不包含帳戶中指定的任何追蹤引數，或搜尋、Social和Commerce內的促銷活動設定。

您可以在[ [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md)中檢視產品群組的相關資料。

>[!MORELIKETHIS]
>
>* [管理購物產品群組](product-group-manage.md)
>* [[!DNL Google Ads] 產品群組設定](product-group-settings-google.md)
>* [實作 [!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] 產品群組設定](product-group-settings-microsoft.md)
>* [實作 [!DNL Microsoft Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
