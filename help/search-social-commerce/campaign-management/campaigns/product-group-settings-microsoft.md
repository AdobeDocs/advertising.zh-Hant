---
title: 『[!DNL Microsoft Advertising] 產品群組設定
description: 參考設定 [!DNL Microsoft Advertising] 購物產品群組。
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 產品群組設定

## 「所有產品」產品群組

**[!UICONTROL Condition]：** （唯讀）所有產品

**[!UICONTROL Bid]：** （僅包含產品群組）最高每次點按成本(CPC)，為廣告點按的最高金額。 此值僅用於沒有子項產品群組的單位，並且將用來取代廣告群組層級值。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

此範本會覆寫較高層級的範本，且僅用於沒有子產品群組的單位。

## 所有其他產品群組

**[!UICONTROL Condition/Value]：** （現有產品群組的唯讀）要鎖定的產品維度。 針對新產品群組，輸入產品定位所依據的維度，以及所選資訊類別的合格屬性（例如，依品牌定位時為「Acme」，或依條件定位時為「New」）。

一旦您為特定產品維度（即「所有產品」以外的維度）建立產品群組，搜尋、社交和Commerce就會自動為「其他所有專案」建立產品群組。

如需可用產品維度的清單，請參閱&quot;[購物行銷活動產品篩選器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).」 您的維度清單可能會根據行銷活動而有所限制 [!UICONTROL Inventory Filter] 設定。

**[!UICONTROL Excluded]：** （新產品群組選填；現有產品群組為唯讀）排除相符產品廣告的競標。

**[!UICONTROL Bid]：** （僅包含產品群組）最高每次點按成本(CPC)，為廣告點按的最高金額。 此值僅用於沒有子項產品群組的單位，並且將用來取代廣告群組層級值。

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

此範本會覆寫較高層級的範本，且僅用於沒有子產品群組的單位。

>[!MORELIKETHIS]
>
>* [關於購物產品群組](product-group-about.md)
>* [管理購物產品群組](product-group-manage.md)
>* [購物行銷活動產品篩選器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [實作 [!DNL Microsoft Advertising] 購物宣傳](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
