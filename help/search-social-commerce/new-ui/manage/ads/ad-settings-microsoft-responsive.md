---
title: '[!DNL Microsoft Advertising]個回應式廣告設定'
description: 參考 [!DNL Microsoft Advertising] 回應式廣告的設定。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 243
ht-degree: 0%

---

# [!DNL Microsoft Advertising]個回應式（對象）廣告設定

回應式廣告格式可用於[!DNL Microsoft Audience Network]上的影像型、視訊型和連線電視視訊型對象廣告。 廣告網路會使用最有效的廣告元素組合，以動態方式組合回應式廣告。

## [!UICONTROL Basic Settings]

*僅限新廣告*

**[!UICONTROL Network]：**&#x200B;廣告網路。

**[!UICONTROL Account]：**&#x200B;廣告網路帳戶。

**[!UICONTROL Campaign]：**&#x200B;行銷活動。

**[!UICONTROL Ad Group]：**&#x200B;廣告群組。

## [!UICONTROL Audience CTV Video Ad Details]

<!-- I can't find a video ad -- this same header is used for image ads. Need to verify the video ad settings and when you'll get them -->

### 視訊廣告

**[!UICONTROL Videos]：**&#x200B;一個視訊廣告的URL。

**[!UICONTROL Status]：**&#x200B;廣告狀態： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

### 影像廣告)

>[!NOTE]
>
>廣告網路會使用商店的產品資訊和廣告群組層級的使用者目標定位，自動為連結至商家中心商店的對象行銷活動建立廣告。 您不需要手動建立廣告。

**[!UICONTROL Images]：**&#x200B;廣告的最多15個JPEG或PNG影像。 至少加入一個長寬比為1.91:1的影像。 檢視[對象廣告影像](https://help.ads.microsoft.com/#apex/ads/en/56912/0)允許的外觀比例和維度。

針對對象廣告，[!DNL Microsoft Advertising]會針對所有可能的長寬比自動裁切此影像。

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]：**&#x200B;公司名稱，最多25個字元。 它可用於僅限呼叫的廣告格式。

**[!UICONTROL Short Headlines]：**&#x200B;至少3個字元及最多15個字元的簡短標題，其中至少一個字元及每個字元的上限為30個字元。

**[!UICONTROL Long Headlines]：**&#x200B;至少有三個、最多5個長標題，每個標題最多90個字元。

**[!UICONTROL Ad Text]：**&#x200B;說明至少有兩個，最多四個，每個至少有一個單字，最多有90個字元。

**[!UICONTROL Status]：**&#x200B;廣告狀態： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [管理廣告](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
