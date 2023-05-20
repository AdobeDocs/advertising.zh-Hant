---
title: 使用 [!DNL Marketing Channels] Adobe廣告資料
description: 瞭解如何使用Adobe廣告資料 [!DNL Analytics Marketing Channels]。
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# 使用 [!DNL Analytics Marketing Channels] Adobe廣告資料

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

同時使用Adobe廣告和 [!DNL Analytics Marketing Channels] 報告時，您可以深入瞭解數字媒體如何影響站點活動。

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

下圖顯示Adobe廣告和 [!DNL Marketing Channels] 跟蹤組成一名遊客旅行的個人訪問。 Adobe廣告報告 [!DNL Analytics] 僅限於使用AMO ID通過Adobe廣告進行的付費顯示、搜索、社交和商業渠道廣告。 但是， [!DNL Marketing Channels] 跟蹤配置在 [!DNL Marketing Channels] 處理規則。

![Adobe廣告 [!DNL Marketing Channels] 跟蹤訪客旅行中的個人訪問](/help/integrations/assets/a4adc-mc-sample-journey2.png)

在第一次訪問中，用戶通過電子郵件活動進入網站，執行十個頁面視圖，然後離開。 在第二次訪問中，用戶通過顯示廣告進入站點，執行十個頁面視圖，然後離開。 在第三次訪問中，用戶通過自然搜索進入站點，執行了五個頁面視圖，執行了$250的轉換，然後左轉。 注意跟蹤中 [!DNL Marketing Channels] 和Adobe廣告。 Adobe廣告公司在此次旅行中唯一追蹤的渠道是 [!UICONTROL Display]。 Adobe廣告跟蹤 [!UICONTROL Display] 渠道訪問並將後續接洽資料（如頁面視圖）和轉換歸回該廣告的影響。 [!DNL Marketing Channels]另一方面，對所有渠道都進行了全面的介紹。

由於AMO ID在訪問者旅程中持續存在，因此您可以使用AMO ID資料查看Adobe廣告對其他營銷渠道的影響。 AMO ID [預設情況下持續60天](/help/integrations/analytics/overview.md)，但您可以根據需要配置持久性。

## 如何將Adobe廣告與營銷渠道資料相結合分析媒體表現

在 [!DNL Analytics]，您可以將Adobe廣告堅持付費廣告資料與 [!DNL Marketing Channels] 全面訪問資料，以便更好地分析您的介質效能，從而更好地影響客戶的旅程。

以下分析使用Adobe廣告資料來顯示顯示廣告如何影響站點轉換的不同版本。 所有三列都使用相同的轉換度量，但每列都講述不同的故事：

* 第1列查看訪問者旅途中持續的AMO ID資料。 第1清單示，641個應用程式啟動在某一時刻通過瀏覽或點擊事件與Adobe廣告連結。 此視圖不包含任何其他視圖 [!DNL Marketing Channels] 考慮歸屬。

* 在 [!DNL Marketing Channels] 但是，641個應用程式啟動被歸於其他營銷渠道。 最後兩列將641個應用程式啟動並將資料限制為 [!UICONTROL Display Click-Through] 和 [!UICONTROL Display View-Through] 頻道，顯示在最後一個觸摸屬性模型中發生的轉換。

![顯示廣告如何影響站點轉換的示例](/help/integrations/assets/a4adc-mc-display-impact.png)

可以進一步分析。 您可以通過市場營銷渠道進一步細分Adobe廣告行，以查看Adobe廣告轉換的歸屬於641個應用程式啟動的位置。 您已經知道，其中5個轉換歸因於上次觸摸顯示「點擊」，19個歸因於上次觸摸顯示「查看」。 這仍有617個申請開始歸於其他營銷渠道。 您可以將最後一個觸摸頻道維拖放到廣告行項目DSP的頂部，以顯示其餘應用程式啟動的頻道屬性，並顯示顯示頻道的跨頻道影響。

![如何添加上次觸摸通道維](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

現在，您可以看到剩餘的「應用程式啟動」是如何歸屬的。 電子郵件為357個上次觸摸應用程式啟動（AMO ID保留）授予信用。 使用此類分析，您可以看到Adobe廣告顯示廣告在所有渠道中產生的影響。 只有一個資料集和屬性模型，這種洞察力就不可用。

![顯示通道交叉通道影響的示例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

通過使用「堆棧圖」集「100%堆疊」來顯示趨勢資料，可以進一步改進分析。 此可視化功能使您能夠更輕鬆地監控哪些最後一次接觸式市場推廣渠道受顯示器市場推廣活動影響更大。

![顯示通道的趨勢交叉通道影響示例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Adobe廣告ID建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [渠道資料為何會因Adobe廣告和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [視頻：使用 [!DNL Marketing Channels] 用於Adobe廣告報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

