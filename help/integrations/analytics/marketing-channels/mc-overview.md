---
title: ' [!DNL Marketing Channels]的基礎知識'
description: 瞭解 [!DNL Analytics for Advertising] 使用者應該瞭解的 [!DNL Analytics Marketing Channels] 相關重要資訊。
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
TQID: https://experienceleague.adobe.com/NJ4LPss-g-J06PuvdCaUktHPyP7MARdJK84-D8gnwAk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: beb7a3c1-66ab-4786-b879-7621375b3c40
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 561
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels]的基礎知識

此頁面說明[!DNL Analytics for Advertising]使用者需要瞭解的[!DNL Analytics Marketing Channels]相關重要資訊。

如需[!DNL Marketing Channels]的完整檔案，請參閱[開始使用 [!DNL Marketing Channels]](https://experienceleague.adobe.com/en/docs/analytics/components/marketing-channels/c-getting-started-mchannel)。

## [!DNL Marketing Channels]的概觀

[!DNL Marketing Channels]是Adobe Analytics的主要功能。 [!DNL Marketing Channels]報表顯示客戶如何透過報表期間到達您的網站，以及每個管道如何影響收入或網站上的行為。

考量下列跨造訪歷程的範例。 訪客每次造訪網站時，都會透過訪客進入的行銷管道表示。 首次造訪（也稱為首次接觸管道）是電子郵件。 「瀏覽時顯示2」為參與管道，而「免費搜尋」則視為「上次接觸管道」。 如果您在[!UICONTROL Attribution IQ]內使用[!UICONTROL Last Touch Attribution]，則免費搜尋會收到$250轉換事件的完整評價。 您可以使用Adobe CX Enterprise ID Service將這些個別造訪連結在一起，以顯示單一訪客的歷程。

![行銷管道中的跨造訪轉換歷程範例](/help/integrations/assets/a4adc-mc-sample-journey.png)

使用[!UICONTROL Marketing Channels]處理規則，您可以建立邏輯集來判斷帶動流量的管道，並在使用者進入您的網站時追蹤每個管道。 例如，[!UICONTROL Email]頻道是以點按時產生的唯一追蹤代碼表示，由Adobe Analytics記錄時，會將造訪分類為源自電子郵件行銷活動。

## 處理規則及行銷管道的設定方式

每次使用者存取網站時，都會透過已點按或直接輸入網址列的URL進行。 當使用者進入網站時，[!DNL Analytics]會追蹤可用來判斷造成造訪的管道的資訊。

行銷人員通常會附加查詢字串引數追蹤程式碼到管道URL，以協助追蹤管道對其網站的影響。 您可以設定[!DNL Marketing Channels]處理規則來監聽特定追蹤引數和值，以判斷頻道，而不需要任何其他追蹤。 例如，如果所有電子郵件促銷活動URL都遵循格式`www.adobe.com?cid=email…` （其中URL包含查詢字串引數和值`cid=email`），則您可以建立規則來監聽此追蹤程式碼，並將造訪儲存在[!UICONTROL Email]管道中。

其他管道沒有可追蹤的URL路徑，需要進一步的識別邏輯。 例如，[!UICONTROL Earned Social] （使用者在其中按一下其他使用者在社交網路上有機共用的連結）是重要的追蹤管道。 不過，行銷人員無法將查詢字串引數追蹤程式碼附加至共用的URL。 在此情況下，您可以建立處理規則來監聽感興趣社交網路的反向連結網域，並缺少付費追蹤代碼來判斷管道。 之後，符合這些要求的造訪將在「行銷管道」報表中追蹤為「贏取社交」 。

Adobe建議您與您的[!DNL Analytics]團隊合作，建立追蹤所有相關管道的完整[!DNL Marketing Channels]處理規則集。 這麼做可讓您建立強大的歸因報表。

若要瞭解Adobe Advertising如何對建立自訂行銷管道所需的訊號做出貢獻，請參閱[使用Adobe Advertising ID來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)。

>[!MORELIKETHIS]
>
>* [使用Adobe Advertising ID來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [為什麼管道資料在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之間會有所不同
>* [搭配Adobe Advertising資料使用 [!DNL Analytics Marketing Channels] ](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 進行Adobe Advertising報告](https://experienceleague.adobe.com/en/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc)
>* [總覽 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
