---
title: '"[!DNL Analytics] Data inAdobe廣告'
description: '"[!DNL Analytics] Data inAdobe廣告'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Adobe廣告中的資料

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

## 分析段

建立的所有段 [!DNL Analytics] 出版給Experience Cloud。

新片段需要24至48小時才能出現在Adobe廣告中。 對現有段的更新將在大約八小時內同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 站點項目指標

>[!NOTE]
>
>* [!DNL Analytics] 將EF IDeVar的事件傳遞到Adobe廣告。  預設整合不支援將計算的度量或其他維(eVar)發送到Adobe廣告。 但是，如果計算的度量可以在自定義事件中完全捕獲，則Adobe廣告可以接收自定義事件。
>* [!DNL Analytics] 每小時將資料傳遞給Adobe廣告。


* [!UICONTROL Timespent_secs_1stvisit]:訪問者首次訪問時在站點上花費的秒數。
* [!UICONTROL Timespent_secs_total]:按一下回望窗口內所有訪問站點所花費的總秒數。
* [!UICONTROL Pageviews_1stvisit]:訪問者首次訪問期間站點上的頁面視圖數。
* [!UICONTROL Pageviews_total]:按一下回望窗口內所有訪問站點上的頁面視圖總數。
* [[!UICONTROL Bounces] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]:那次 [!DNL Analytics] 收集 [!UICONTROL EF ID]。

## 轉換度量

[!DNL Analytics] 每天將轉換度量傳遞給Adobe廣告。

### 標準轉換度量

* [[!UICONTROL Revenue] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 自定義轉換度量

這些指標是特定於報告套件的，因此每個客戶和報告套件的可用指標各不相同。

### 保留轉換度量

這些指標是特定於報告套件的，因此每個客戶和報告套件的可用指標各不相同。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe在Analysis Workspace的廣告指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)

