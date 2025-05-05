---
title: 使用 [!DNL Marketing Channels] 與Adobe Advertising資料
description: 瞭解如何在 [!DNL Analytics Marketing Channels]中使用Adobe Advertising資料。
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# 使用[!DNL Analytics Marketing Channels]與Adobe Advertising資料

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

藉由同時使用Adobe Advertising和[!DNL Analytics Marketing Channels]報表，您可以獲得數位媒體如何影響網站活動的寶貴見解。

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

下圖顯示Adobe Advertising和[!DNL Marketing Channels]如何追蹤組成一個訪客歷程的個別造訪。 [!DNL Analytics]中的Adobe Advertising報表僅限於使用AMO ID透過Adobe Advertising販賣的付費顯示、搜尋、社交和商務管道廣告。 不過，[!DNL Marketing Channels]會追蹤[!DNL Marketing Channels]處理規則中設定的所有管道。

![Adobe Advertising和[!DNL Marketing Channels]如何追蹤訪客歷程中的個別造訪](/help/integrations/assets/a4adc-mc-sample-journey2.png)

在第一次造訪中，使用者透過電子郵件行銷活動進入網站，執行了十次頁面檢視，然後離開。 在第二次造訪中，使用者透過顯示廣告進入網站，執行了十次頁面檢視，然後離開。 在第三次造訪中，使用者透過免費搜尋進入網站、執行了五個頁面檢視、執行了$250的轉換，最後是向左。 請注意[!DNL Marketing Channels]與Adobe Advertising之間的追蹤差異。 Adobe Advertising在此歷程中追蹤的唯一管道是[!UICONTROL Display]。 Adobe Advertising會追蹤[!UICONTROL Display]管道造訪，並將後續參與資料（例如頁面檢視）和轉換歸因於該廣告的影響。 另一方面，[!DNL Marketing Channels]則提供所有色版的完整檢視。

由於AMO ID會在訪客的歷程中持續存在，因此您可以使用AMO ID資料來瞭解Adobe Advertising如何影響其他行銷管道。 AMO ID [預設會保留60天](/help/integrations/analytics/overview.md)，但您可以視需要設定持續性。

## 如何結合Adobe Advertising和行銷管道資料來分析媒體效能

在[!DNL Analytics]內，您可以結合持續付費廣告資料的Adobe Advertising和[!DNL Marketing Channels]完整的造訪資料，以更好地分析您的媒體效能，進而更能影響客戶歷程。

下列分析使用Adobe Advertising資料來顯示不同版本的顯示廣告如何影響網站轉換。 這三欄皆使用相同的轉換量度，但每一欄所講述的故事不同：

* 欄1會檢視持續存在於訪客歷程中的AMO ID資料。 欄1表示641應用程式啟動在某個時間點透過檢視或點進事件與Adobe Advertising廣告連結。 此檢視未考慮任何其他[!DNL Marketing Channels]歸因。

* 但是，在[!DNL Marketing Channels]資料集中，641應用程式開始被歸因到其他行銷管道。 最後兩欄採用641應用程式啟動並將資料限製為[!UICONTROL Display Click-Through]和[!UICONTROL Display View-Through]管道，顯示上次接觸歸因模型中發生的轉換。

![顯示廣告如何影響網站轉換的範例](/help/integrations/assets/a4adc-mc-display-impact.png)

您可以進一步執行此分析。 您可以進一步依行銷管道劃分Adobe Advertising列，以檢視Adobe Advertising轉換歸因於641應用程式開始的位置。 您已經知道其中5次轉換歸屬於上次接觸顯示點進，19次歸屬於上次接觸顯示檢視。 如此仍會將617應用程式開始歸因於其他行銷管道。 您可以將上次接觸管道維度拖放至Advertising DSP條列專案上方，以顯現其餘應用程式啟動的管道歸因，並顯示顯示管道的跨管道影響。

![如何新增上次接觸管道維度](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

現在您可以檢視剩餘的應用程式開始時間的歸因方式。 357個上次接觸應用程式開始的電子郵件會獲得評分，持續保留AMO ID。 使用此型別的分析，您可以檢視Adobe Advertising顯示廣告對所有管道的影響。 由於只有一個資料集和歸因模型，因此這類深入分析將不可用。

![顯示管道的跨管道影響範例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

您可以使用棧疊圖表設定「100%棧疊」來顯示一段時間內的趨勢資料，藉此進一步改善分析。 此視覺效果可讓您更輕鬆地監視哪些上次接觸行銷管道較受您的顯示行銷活動影響較大。

![顯示管道的趨勢跨管道影響範例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [基礎（共 [!DNL Analytics Marketing Channels]](mc-overview.md)個）
>* [使用Adobe Advertising識別碼來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [為什麼管道資料在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之間可能不同
>* [影片：使用 [!DNL Marketing Channels] 進行Adobe Advertising報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hant)
>* [總覽 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
