---
title: '[!DNL Microsoft Ads]個詳細目錄摘要的購物廣告範本設定'
description: 請參考詳細目錄摘要之 [!DNL Microsoft Ads] 購物廣告範本的設定。
exl-id: a0dd6542-0516-406a-b8c5-2e102ec7ab3d
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# 詳細目錄摘要的[!DNL Microsoft Ads]購物廣告範本設定

使用購物廣告範本來設定購物廣告。

>[!NOTE]
>
>* 在範本中保留下列字元以指定欄名稱和修飾元名稱，因此禁止在所有屬性欄位中做為文字： `[ ] < > `


## \[在所有索引標籤上方\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[左側面板\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]：** （使用者端摘要檔案的範本為選用）行銷活動層級追蹤範本，可指定所有離登陸網域重新導向與追蹤引數，並將最終URL內嵌在引數中。 此值會覆寫帳戶層級設定，但更精細層級的追蹤範本（以關鍵字為最精細）會覆寫此值。

* 針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），請執行下列任一項作業：

   * （建議）針對Microsoft購物行銷活動使用[追蹤範本格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)。 如果整個帳戶都專用於購物廣告，您可以改為在帳戶層級定義追蹤範本。

   * 如果您改為使用[!DNL bingads_redirect]欄（使用[正確格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)）在摘要中包含每個產品的值，請輸入引數`{lpurl}`。 您可以選擇將第三方重新導向與追蹤新增至`{lpurl}`引數。

* 對於協力廠商重新導向和追蹤，請輸入值。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]：**&#x200B;其產品用於行銷活動的商家帳戶的客戶識別碼。

**[!UICONTROL Sales Country]：**促銷活動產品銷售的國家/地區。 因為產品是相關聯的
若使用目標國家/地區，此設定會決定促銷活動中要公告哪些產品。

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Campaign Priority]：**當多個行銷活動廣告
相同的產品： *[!UICONTROL Low]* （新行銷活動的預設值）、*[!UICONTROL Medium]*&#x200B;或&#x200B;*[!UICONTROL High]*。 當同一個產品包含在多個行銷活動中時，廣告網路會使用
行銷活動優先順序會先決定哪個行銷活動（及相關競標）適用於廣告拍賣。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]：** （選用）廣告群組層級追蹤範本，可指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。 此值會覆寫帳戶和促銷活動層級的設定，但更精細層級的追蹤範本會覆寫此值。

若為Adobe Advertising轉換追蹤，則不需要輸入值。 行銷活動層級值就足夠了。

對於協力廠商重新導向和追蹤，請輸入值。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]：**&#x200B;預設、包含所有功能的產品群組&quot;[!UICONTROL All products]&quot;。 您無法刪除此上層產品群組，但是當摘要中缺少所有較低層級時，系統會自動刪除該群組。

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]：** （沒有子產品群組的單位；選擇性）產品的追蹤範本
群組，這會指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在[!DNL ValueTrack]引數中。 此範本會覆寫較高層級的範本。

若為Adobe Advertising轉換追蹤，則不需要輸入值。 行銷活動層級值就足夠了。

對於協力廠商重新導向和追蹤，請輸入值。

**[!UICONTROL Initial Bid]：**&#x200B;每個廣告的初始出價。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [關於使用詳細目錄摘要自動化廣告管理](../inventory-feeds-about.md)
>* [管理修飾元](../modifiers-manage.md)
>* [管理詳細目錄資料摘要檔案](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [透過範本傳播摘要資料](../feed-data-propagate.md)
>* [從詳細目錄摘要張貼行銷活動資料至廣告網路](../propagated-data-post.md)
