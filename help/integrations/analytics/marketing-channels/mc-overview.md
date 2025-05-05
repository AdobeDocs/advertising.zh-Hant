---
title: ' [!DNL Marketing Channels]的基礎知識'
description: 瞭解 [!DNL Analytics for Advertising] 使用者應該瞭解的 [!DNL Analytics Marketing Channels] 相關重要資訊。
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels]的基礎知識

此頁面說明[!DNL Analytics for Advertising]使用者需要瞭解的[!DNL Analytics Marketing Channels]相關重要資訊。

如需[!DNL Marketing Channels]的完整檔案，請參閱[開始使用 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html?lang=zh-Hant)。

## [!DNL Marketing Channels]的概觀

[!DNL Marketing Channels]是Adobe Analytics的主要功能。 [!DNL Marketing Channels]報表顯示客戶如何透過報表期間到達您的網站，以及每個管道如何影響收入或網站上的行為。

考量下列跨造訪歷程的範例。 訪客每次造訪網站時，都會透過訪客進入的行銷管道表示。 首次造訪（也稱為首次接觸管道）是電子郵件。 「瀏覽時顯示2」為參與管道，而「免費搜尋」則視為「上次接觸管道」。 如果您在[!UICONTROL Attribution IQ]內使用[!UICONTROL Last Touch Attribution]，免費搜尋將接收$250轉換事件的完整評價。 您可以使用Experience CloudID服務，將這些個別的造訪連結在一起，以顯示單一訪客的一個歷程。

![行銷管道中的跨造訪轉換歷程範例](/help/integrations/assets/a4adc-mc-sample-journey.png)

使用[!UICONTROL Marketing Channels]處理規則，您可以建立邏輯集來判斷帶動流量的管道，並追蹤使用者進入您網站時的每個管道。 例如，[!UICONTROL Email]管道將由點選時產生的唯一追蹤代碼指示，當由Adobe Analytics記錄時，會將造訪分類為源自電子郵件行銷活動。

## 處理規則及行銷管道的設定方式

每次使用者存取網站時，都會透過已點按或直接輸入網址列的URL進行。 當使用者進入網站時，[!DNL Analytics]會追蹤可用來判斷造成造訪的管道的資訊。

行銷人員通常會附加查詢字串引數追蹤程式碼到管道URL，以協助追蹤管道對其網站的影響。 您可以設定[!DNL Marketing Channels]處理規則來監聽特定追蹤引數和值，以判斷頻道，而不需要任何其他追蹤。 例如，如果所有電子郵件促銷活動URL都遵循格式`www.adobe.com?cid=email…` （其中URL包含查詢字串引數和值`cid=email`），則您可以建立規則來監聽此追蹤程式碼，並將造訪儲存在[!UICONTROL Email]管道中。

其他管道沒有可追蹤的URL路徑，需要進一步的識別邏輯。 例如，[!UICONTROL Earned Social] （使用者在其中按一下其他使用者在社交網路上有機共用的連結）是重要的追蹤管道。 不過，行銷人員無法將查詢字串引數追蹤程式碼附加至共用的URL。 在此情況下，您可以建立處理規則來監聽感興趣社交網路的反向連結網域，並缺少付費追蹤代碼來判斷管道。 之後，系統會在行銷管道報表中，將符合這些要求的造訪追蹤為「贏取社交」 。

Adobe建議您與分析團隊合作，建立一整組[!DNL Marketing Channels]處理規則，以追蹤與您的業務相關的所有管道。 這麼做可讓您建立強大的歸因報表。

若要瞭解Adobe Advertising如何對建立自訂行銷管道所需的訊號做出貢獻，請參閱&quot;[使用Advertising ID建立 [!DNL Marketing Channels] 規則](mc-ids.md)&quot;。

>[!MORELIKETHIS]
>
>* [使用Adobe Advertising識別碼來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [為什麼管道資料在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之間可能不同
>* [搭配Adobe Advertising資料使用 [!DNL Analytics Marketing Channels] ](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 進行Adobe Advertising報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hant)
>* [總覽 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
