---
title: Analysis Workspace中的Adobe Advertising量度
description: Analysis Workspace中的Adobe Advertising量度
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Analysis Workspace中的Adobe Advertising量度

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

>[!NOTE]
>
>* Adobe Advertising會將流量量度和維度傳遞至 [!DNL Analytics] 每日。
>* [!DNL Analytics] 擷取Adobe Advertising點進和檢視點進。
>* 的 [!DNL Search, Social, & Commerce]中，大部分的廣告網路和促銷活動型別都支援此功能。 請參閱&quot;[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)中的&quot; [!DNL Search, Social, & Commerce] 指南，以取得詳細資訊。

## 來自Adobe Advertising的流量量度

Adobe Advertising流量量度 [!DNL Analytics] 開頭通常為「Adobe Advertising」，但「[!UICONTROL AMO ID Instances].」 不過，對於使用自訂事件（而不是保留事件）最初建立點按數、成本和曝光次數的量度的長期客戶，這些量度仍以「AMO」開頭。

| 流量量度 | 說明 |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] 或（部分舊客戶） [!UICONTROL AMO Clicks] | Adobe Advertising點按總數。 |
| [!UICONTROL Adobe Advertising Cost] 或（部分舊客戶） [!UICONTROL AMO Cost] | 以報表套裝貨幣為單位的Adobe Advertising支出。 |
| [!UICONTROL Adobe Advertising Impressions] 或（部分舊客戶） [!UICONTROL AMO Impressions] | Adobe Advertising曝光次數。 |
| [!UICONTROL Adobe Advertising Measurable Impressions] | 已針對可檢視度檢測成功初始化的提供曝光數。 此值的計算方式為（儀器曝光次數 — 無法測量的曝光次數）。 |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Adobe Advertising影片被檢視的分鐘數。 |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | 判斷為無法檢視的曝光次數。 此值的計算方式為([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable])。 |
| [!UICONTROL Adobe Advertising Viewable Impressions] | 根據版位組態測量為可檢視的曝光次數。 |
| [!UICONTROL Adobe Advertising Views] | 廣告的檢視次數。 當檢視器起始Adobe Advertising影片時會計入一次檢視。 |
| [!UICONTROL Adobe Advertising Views 25% Complete] | 觀看了至少25%之Adobe Advertising影片的檢視次數。 |
| [!UICONTROL Adobe Advertising Views 50% Complete] | 觀看了至少50%之Adobe Advertising影片的檢視次數。 |
| [!UICONTROL Adobe Advertising Views 75% Complete] | 觀看了至少75%之Adobe Advertising影片的檢視次數。 |
| [!UICONTROL Adobe Advertising Views 100% Complete] | 觀看了100%Adobe Advertising影片的檢視次數。 |
| [!UICONTROL AMO ID Instances] | 次數 [!UICONTROL AMO ID] 已設定。 |

## Adobe AdvertisingDimension

>[!NOTE]
>
>中的所有Adobe Advertising維度 [!DNL Analytics] 後面接著&quot;[!DNL (AMO ID)].」

| 維度 | 適用的Adobe Advertising資料 | 說明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告DSP或搜尋引擎名稱 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 帳戶名稱。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | RTB ([!DNL DSP])或廣告網路名稱([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 行銷活動名稱。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 套件([!DNL DSP])或投資組合([!DNL Search, Social, & Commerce])名稱。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] 資料 | 位置名稱。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告群組名稱。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 關鍵字。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 搜尋相符型別。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 關鍵字和相符型別。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告型別，例如 `text`， `video`， `display`，或 `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告型別([!DNL DSP])或廣告標題([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告說明([!DNL DSP])或廣告內文([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告中顯示的URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告的目的地URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 登入頁面專案是瀏覽還是點進。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 產品清單廣告的產品目標。 |

## 實用的Adobe Advertising自訂計算量度

請考慮為您的Adobe Advertising資料建立下列量度。

* 登陸頁面例項的點按次數([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])：這是按下廣告並進入登陸頁面的人數%。
* 可測量的比率([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* 可檢視的曝光率([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* 每次檢視成本([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* 每次點按成本([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe Advertising中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)
