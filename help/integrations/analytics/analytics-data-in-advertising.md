---
title: '[!DNL Analytics]資料Adobe Advertising'
description: '[!DNL Analytics]資料Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Adobe Advertising中的[!DNL Analytics]資料

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

## Analytics區段

在[!DNL Analytics]中建立並發佈至Experience Cloud的所有區段。

新區段需要24到48小時才會在Adobe Advertising中顯示。 現有區段的更新會在約八小時內同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 網站參與量度

>[!NOTE]
>
>* [!DNL Analytics]將EF ID [!DNL eVar]的事件傳入Adobe Advertising。  預設整合不支援將計算量度或其他維度([!DNL eVars])傳送至Adobe Advertising。 不過，如果計算量度可在自訂事件中完整擷取，則Adobe Advertising可擷取自訂事件。
>* [!DNL Analytics]每小時傳遞資料給Adobe Advertising。

* [!UICONTROL Timespent_secs_1stvisit]：訪客首次造訪期間在網站上逗留的秒數。
* [!UICONTROL Timespent_secs_total]：在點按回顧期間內，所有造訪在網站上逗留的總秒數。
* [!UICONTROL Pageviews_1stvisit]：訪客首次造訪期間網站上的頁面檢視次數。
* [!UICONTROL Pageviews_total]：點按回顧期間內的所有造訪在網站上檢視的頁面總數。
* [[!UICONTROL Bounces]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]： [!DNL Analytics]收集[!UICONTROL EF ID]的次數。

## 轉換量度

[!DNL Analytics]每日傳遞轉換量度至Adobe Advertising。

### 標準轉換量度

* [[!UICONTROL Revenue]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals]個量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 自訂轉換量度

這些量度是報表套裝專用，因此每個客戶和報表套裝的可用量度會有所不同。

### 從[!DNL eVars]和[!DNL Props]建立的自訂轉換量度

可用的量度因每個客戶而異。 請參閱&quot;[從Adobe Analytics [!DNL eVars] 和 [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)建立轉換量度。&quot;

### 保留的轉換量度

這些量度是報表套裝專用，因此每個客戶和報表套裝的可用量度會有所不同。

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* 在Analysis Workspace中[Adobe Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
