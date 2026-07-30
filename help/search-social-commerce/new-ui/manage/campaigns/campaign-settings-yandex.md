---
title: '[!DNL Yandex]行銷活動設定'
description: 參考 [!DNL Yandex] 行銷活動的設定。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# [!DNL Yandex]行銷活動設定

## \[頁面頂端]

**[!UICONTROL Campaign Name]：**&#x200B;帳戶中唯一的促銷活動名稱。

**[!UICONTROL Status]：**&#x200B;行銷活動的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新廣告行銷活動的預設值為&#x200B;*作用中*。

## [!UICONTROL Basic Settings]索引標籤

*僅限新行銷活動*

**[!UICONTROL Network]：**&#x200B;廣告網路。

**[!UICONTROL Account]：**&#x200B;廣告網路帳戶。

**[!UICONTROL Campaign Type]：**&#x200B;廣告的放置位置：

* *[!UICONTROL Search Network Only]：*&#x200B;在搜尋網路上顯示文字廣告。 您必須指定每個廣告群組的關鍵字。

* *[!UICONTROL Search and Display Network]：*&#x200B;在搜尋網路和[!DNL Yandex Advertising Network]上顯示文字廣告。 針對搜尋廣告，您必須指定每個廣告群組的搜尋關鍵字。 針對顯示廣告，您必須針對要針對每個廣告群組進行廣告的網站，指定關鍵字。

* *[!UICONTROL Display Network Only]：*&#x200B;在[!DNL Yandex Advertising Network]上顯示文字廣告。 對於每個廣告群組，您必須為要廣告的網站指定關鍵字。

## [!UICONTROL Campaign Details]索引標籤

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## [!UICONTROL Budget Options]索引標籤

**[!UICONTROL Budget]：**&#x200B;預算，這是您希望每天（平均）或行銷活動存留期花費的金額，視帳戶的預算型別而定。 最低預算為6 300日元、10歐元或10美元。

**附註：**

* 新行銷活動具有競標管理策略「最高可用位置」。

* 根據搜尋條件，如果您將此行銷活動指派給設定為允許自動調整行銷活動預算限制的產品組合，則您實際上可能在任何指定日、月或期限上花費比指定預算更多或少的預算。

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Additional Campaign Information]索引標籤

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]：** （僅適用於[!UICONTROL EF Redirect]；唯讀）應追蹤點按和收入的層級。 只有&#x200B;*[!UICONTROL Creative]*&#x200B;可用於[!DNL Yandex] — 僅在廣告（創意）層級追蹤資料。

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [管理行銷活動](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
