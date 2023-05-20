---
title: Adobe在Analysis Workspace的廣告指標
description: Adobe在Analysis Workspace的廣告指標
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 5dd3772de945660e76321dac935de5ebcab5979a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Adobe在Analysis Workspace的廣告指標

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

>[!NOTE]
>
>* Adobe廣告將流量度量和維度傳遞給 [!DNL Analytics] 每天。
>* [!DNL Analytics] 捕獲Adobe廣告即時點擊和查看。
   > 對於 [!DNL Search, Social, & Commerce]，此功能對大多數廣告網路和市場活動類型都受支援。 請參閱中的「支援的清單」 [!DNL Search, Social, & Commerce] 的子菜單。<!-- add link when that's published in ExL -->


## 來自Adobe廣告的流量度量

>[!NOTE]
>
>所有Adobe廣告流量指標 [!DNL Analytics] 從&quot;AMO&quot;開始。

| 流量度量 | 說明 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Adobe廣告印象數。 |
| [!UICONTROL AMO Clicks] | Adobe廣告點擊總數。 |
| [!UICONTROL AMO Cost] | Adobe廣告支出以報表套件的幣種表示。 |
| [!UICONTROL AMO ID Instance] | 設定Adobe廣告ID的次數。 |
| [!UICONTROL AMO Minutes Viewed] | 查看Adobe廣告視頻的分鐘數。 |
| [!UICONTROL AMO Views] | 廣告上的視圖數。 當觀看者啟動Adobe廣告視頻時，視圖被計數。 |
| [!UICONTROL AMO Views 25% Complete] | 至少25%的Adobe廣告視頻被觀看的觀看次數。 |
| [!UICONTROL AMO Views 50% Complete] | 至少50%的Adobe廣告視頻被觀看的視圖數。 |
| [!UICONTROL AMO Views 75% Complete] | 至少75%的Adobe廣告視頻被觀看的觀看次數。 |
| [!UICONTROL AMO Views 100% Complete] | 100%的Adobe廣告視頻被觀看的視圖數。 |
| [!UICONTROL AMO Viewable Impressions] | 根據放置配置測量可查看的印痕數。 |
| [!UICONTROL AMO Not Viewable Impressions] | 確定不可查看的印數。 此值的計算方式為([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable])。 |
| [!UICONTROL AMO Measurable Impressions] | 已成功初始化可查看性工具的印數。 此值計算為（工具印記 — 不可測印記數）。 |

## Adobe廣告Dimension

>[!NOTE]
>
>所有Adobe廣告維度 [!DNL Analytics] 後跟&quot;(AMO ID)&quot;。

| Dimension | 適用的Adobe廣告資料 | 說明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告DSP或搜索引擎名稱 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 帳戶名。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | RTB([!DNL DSP])或ad網路名稱([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 市場活動名稱。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 包([!DNL DSP])或組合([!DNL Search, Social, & Commerce])名稱。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] 資料 | 放置名稱。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告組名稱。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 關鍵字。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 搜索匹配類型。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 關鍵字和匹配類型。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告類型，如 `text`。 `video`。 `display`或 `native`。 |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告類型([!DNL DSP]或廣告標題([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告說明([!DNL DSP]或廣告正文([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告中顯示的URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告的目標URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 登錄頁條目是直通視圖還是按一下直通。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 產品清單廣告的產品目標。 |

## 用於Adobe廣告的有用自定義計算度量

請考慮為Adobe廣告資料建立以下度量。

* 按一下到登錄頁實例([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]):這是點擊廣告並登錄登錄頁的人的百分比。
* 可衡量的比率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 可視印象率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* 每個視圖的成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* 每次按一下的成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe廣告中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)

