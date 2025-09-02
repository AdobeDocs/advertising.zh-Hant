---
title: Customer Journey Analytics中的Adobe Advertising量度和維度
description: 參考Customer Journey Analytics中可用的Adobe Advertising量度和維度。
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: eddd9c997ada380d5624703b82bca189be90b893
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Customer Journey Analytics中的Adobe Advertising量度和維度

*僅整合Adobe Advertising-Customer Journey Analytics的廣告商*

>[!NOTE]
>
>* Adobe Advertising每日傳遞流量量度和維度至[!DNL Customer Journey Analytics]。
>* [!DNL Web SDK]會即時擷取Adobe Advertising點進和檢視點進，並將它們傳遞給Customer Journey Analytics。

## Adobe Advertising流量量度

<!-- Verify column names -->

>[!NOTE]
>
>* &#x200B;
>* 「XDM欄位名稱」是Adobe Experience Platform中的欄位名稱。
>* 「XDM欄位顯示名稱」表示Customer Journey Analytics中的顯示名稱。

| Adobe Advertising欄位名稱 | XDM欄位名稱 | XDM欄位顯示名稱 | Source |
|------------------------------|----------------|------------------------|--------|
| 日期 | 日期 | 全部 | |
| AMO ID | skwcid | ADOBE ADVERTISING ID | 全部 |
| AMO曝光數 | adobe_advertising_impressions | Adobe Advertising曝光數 | 全部 |
| AMO點按次數 | adobe_advertising_clicks | Adobe Advertising點按次數 | 全部 |
| AMO成本 | adobe_advertising_cost | Adobe Advertising成本 | 全部 |
| 貨幣代碼 | 貨幣 | 貨幣 | 全部 |
| AMO檢視 | adobe_advertising_views | Adobe Advertising檢視 | Ad Cloud DSP |
| AMO檢視完成25% | adobe_advertising_views_25_pct | Adobe Advertising檢視完成25% | Ad Cloud DSP |
| AMO檢視完成50% | adobe_advertising_views_50_pct | Adobe Advertising檢視50%完成 | Ad Cloud DSP |
| AMO檢視完成75% | adobe_advertising_views_75_pct | Adobe Advertising檢視75%完成 | Ad Cloud DSP |
| AMO檢視100%完成 | adobe_advertising_views_100_pct | Adobe Advertising檢視100%完成 | Ad Cloud DSP |
| AMO已檢視分鐘數 | adobe_advertising_minutes_viewed | Adobe Advertising已檢視分鐘數 | Ad Cloud DSP |
| AMO可檢視的曝光數 | adobe_advertising_viewable_impressions | Adobe Advertising可檢視的曝光數 | Ad Cloud DSP |
| AMO無法檢視的曝光數 | adobe_advertising_not_viewable_impressions | Adobe Advertising不可檢視的曝光數 | Ad Cloud DSP |
| AMO可衡量的曝光數 | adobe_advertising_measurement_impressions | Adobe Advertising可衡量的曝光數 | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Adobe Advertising維度

>[!NOTE]
>
>* 「XDM欄位」是Adobe Experience Platform中的欄位名稱。
>* 「XDM欄位顯示名稱」表示Customer Journey Analytics中的顯示名稱。

| Adobe Advertising欄位名稱 | XDM欄位名稱 | XDM欄位顯示名稱 | Source |
|------------------------------|----------------|------------------------|--------|
| 索引鍵 | skwcid | ADOBE ADVERTISING ID |
| 廣告平台 | adobe_advertising_ad_platform | Adobe Advertising廣告平台 |
| 帳戶 | adobe_advertising_account | Adobe Advertising帳戶 |
| Campaign | adobe_advertising_campaign | Adobe Advertising行銷活動 |
| 廣告群組 | adobe_advertising_ad_group | Adobe Advertising廣告群組 |
| 關鍵字 | adobe_advertising_keyword | Adobe Advertising關鍵字 |
| 廣告 | adobe_advertising_ad | Adobe Advertising廣告 |
| 產品建議放置環境 | adobe_advertising_placement | Adobe Advertising位置 |
| 比對型別 | adobe_advertising_match_type | Adobe Advertising相符型別 |
| 廣告標題 | adobe_advertising_ad_title | Adobe Advertising廣告標題 |
| 廣告說明 | adobe_advertising_ad_description | Adobe Advertising廣告說明 |
| 廣告目的地URL | adobe_advertising_ad_destination_url | Adobe Advertising廣告目的地URL |
| 廣告顯示URL | adobe_advertising_ad_display_url | Adobe Advertising廣告顯示URL |
| 裝置 | adobe_advertising_device | Adobe Advertising裝置 |
| 關鍵字比對型別 | adobe_advertising_keyword_matchtype | Adobe Advertising關鍵字MatchType |
| 網路 | adobe_advertising_network | Adobe Advertising網路 |
| 廣告型別 | adobe_advertising_ad_type | Adobe Advertising廣告型別 |
| 產品目標 | adobe_advertising_product_target | Adobe Advertising產品目標 |
| 登陸型別 | adobe_advertising_landing_type | Adobe Advertising登陸型別 |
| 最佳化 | adobe_advertising_optimization | Adobe Advertising最佳化 |

>[!MORELIKETHIS]
>
>* [總覽](overview.md)
>* [必要條件](prerequisites.md)
>* [個Adobe Advertising ID已由 [!DNL Customer Journey Analytics]](ids.md)使用
