---
title: '[!DNL Microsoft Advertising]回應式廣告設定'
description: 參考 [!DNL Microsoft Advertising] 回應式廣告的設定。
exl-id: 29404500-d929-4683-be71-150ea8ab805d
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]個回應式（對象）廣告設定

回應式廣告格式可用於[!DNL Microsoft Audience Network]上的影像型、視訊型和連線電視視訊型對象廣告。 廣告網路會使用最有效的廣告元素組合，以動態方式組合回應式廣告。

## [!UICONTROL Ad Settings] （適用於視訊廣告）和[!UICONTROL Audience CTV Video Ad Details]

**[!UICONTROL Videos]：**&#x200B;一個視訊廣告的URL。

**[!UICONTROL Status]：**&#x200B;廣告狀態。

## [!UICONTROL Responsive Ad Details] （適用於影像廣告）

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

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [關於廣告](ad-about.md)
>* [管理廣告](ad-manage.md)
>* [[!DNL Microsoft Advertising] 延展的動態搜尋廣告設定](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] 多媒體廣告設定](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] 產品廣告設定](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] 回應式搜尋廣告設定](ad-settings-microsoft-rsa.md)
