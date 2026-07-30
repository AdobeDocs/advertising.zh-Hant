---
title: '[!DNL Baidu]行銷活動設定'
description: 參考 [!DNL Baidu] 行銷活動的設定。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# [!DNL Baidu]行銷活動設定

## \[頁面頂端]

**[!UICONTROL Campaign Name]：**&#x200B;帳戶中唯一的促銷活動名稱。

**[!UICONTROL Status]：**&#x200B;行銷活動的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新廣告行銷活動的預設值為&#x200B;*作用中*。

## [!UICONTROL Basic Settings]索引標籤

*僅限新行銷活動*

**[!UICONTROL Network]：**&#x200B;廣告網路。

**[!UICONTROL Account]：**&#x200B;廣告網路帳戶。

**[!UICONTROL Campaign Type]：**&#x200B;廣告的放置位置，以及行銷活動可能包含的廣告型別。 唯一的選項是&#x200B;*僅搜尋網路*。

## [!UICONTROL Campaign Details]索引標籤

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]：**(適用於以歐盟(EU)受眾為目標的行銷活動)行銷活動是否根據歐盟法規2024/90提供的廣告需求，包含政治廣告： *[!UICONTROL Yes]*&#x200B;或&#x200B;*[!UICONTROL No]*。

## [!UICONTROL Budget Options]索引標籤

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]：**&#x200B;行銷活動的競標策略：

* *[!UICONTROL Maximize Conversions]：*&#x200B;廣告網路（而非Search、Social和Commerce）會最佳化競標，以最大化轉換次數。 選擇性地輸入&#x200B;**[!UICONTROL Target CPA]** （每次取得的成本）。 **注意：**&#x200B;請將此選項用於具有行銷活動層級最佳化之產品組合中的行銷活動。 在包含行銷活動層級最佳化、搜尋、社交和Commerce的產品組合中，會最佳化Target CPA。

* *[!UICONTROL Maximize Conversion Value]：*&#x200B;廣告網路（而非Search、Social和Commerce）會最佳化競標，以將轉換值最大化。 選擇性地輸入&#x200B;**[!UICONTROL Target Return on Ad Spend]** (ROAS)作為百分比。 **注意：**&#x200B;請將此選項用於具有行銷活動層級最佳化之產品組合中的行銷活動。 在包含行銷活動層級最佳化、搜尋、Social和Commerce的產品組合中，會最佳化Target ROAS。

## [!UICONTROL Campaign Targeting]索引標籤

**[!UICONTROL Languages]：**&#x200B;廣告的語言，應符合您的廣告可能顯示的網站語言。 廣告網路會從各種訊號中判斷使用者的語言，包括使用者的查詢、發佈者的國家/地區以及使用者的語言設定。

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL Additional Campaign Information]索引標籤

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### [!UICONTROL Campaign Tracking]索引標籤

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]：** （僅適用於[!UICONTROL EF Redirect]）藉由新增重新導向（相關時）並將引數附加至相關URL，應追蹤點按數和收入的層級：

* *[!UICONTROL Keyword]：*&#x200B;只追蹤關鍵字層級的資料。

* *[!UICONTROL Creative]：*&#x200B;只追蹤廣告（創意）層級的資料。

* *[!UICONTROL Creative and Keyword]：*&#x200B;若要同時追蹤廣告（創意）和關鍵字層級的資料。

**[!UICONTROL Enable conversion reporting in Adobe Analytics]：**&#x200B;將URL引數新增至帳戶或促銷活動中的廣告，以進行轉換追蹤。

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
