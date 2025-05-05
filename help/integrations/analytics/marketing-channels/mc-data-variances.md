---
title: 為什麼管道資料在Adobe Advertising和 [!DNL Marketing Channels]之間可能不同
description: 瞭解AMO ID所追蹤的管道資料為何與 [!DNL Analytics Marketing Channels]所追蹤的管道資料有所不同。
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# 為什麼管道資料在Adobe Advertising和[!DNL Marketing Channels]之間可能不同

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

瞭解Adobe Advertising與[!DNL Marketing Channels]資料集整合的使用者所遇到的一個常見問題是「造成AMO ID與[!DNL Marketing Channels]之間資料差異的原因？」 或者，有時候，「資料為何中斷？ 我需要所有量度在報告中相符。」 幸運的是，差異並不表示資料「已損壞」，而是預期的甚至需要的差異。 讓我們來看看為何會以這種方式設計整合。

這兩個資料集的主要使用案例不同：

* [!DNL Marketing Channels]： [!DNL Marketing Channels]的主要使用案例是將多個管道中的資料與通用歸因模型進行比較。 分析人員可以使用[!UICONTROL Marketing Channel]維度來取得有關管道如何彼此互動的更多深入分析。 此深入分析有助於促進如何投資於每個管道的宏觀決策，並可引導您深入分析來自每個管道的訪客與網站的互動情形。

  因此，[!DNL Analytics] [!UICONTROL Marketing Channel]維度已設定為擷取及追蹤所有管道。 [!DNL Marketing Channels]也可以設定為擷取Advertising DSP閱覽和點進，而且這是與其他行銷管道相關連結。

* Adobe AdvertisingAMO ID：Adobe AdvertisingAMO ID資料的主要使用案例是提供進階[!DNL Adobe Sensei]支援的競標演演算法。 演演算法會自動做出每天數以千計的微觀層級競標決定，以最大化廣告支出，並達成[!DNL DSP]行銷活動或[!DNL Search, Social, & Commerce]產品組合的目標。 演演算法可連結的行銷活動中的轉換資料越多，演演算法做出這些競標決策的效能就越好。

  為了收集此資料，[!DNL Analytics for Advertising]整合會在Adobe Analytics的AMO ID維度中傳遞可轉譯為點進和檢視追蹤程式碼的原始AMO ID，此維度會儲存為自訂變數(eVar)或保留變數(rVar)。 其他頻道的點進次數未在AMO ID維度中設定，因此AMO ID維度無法追蹤來自這些其他頻道的登入。 結果是AMO ID會在[!DNL Marketing Channels]進入點持續存在。

如需有關Adobe Advertising追蹤資料和[!DNL Analytics]追蹤資料之間可能的資料差異的詳細資訊，請參閱[介於 [!DNL Analytics] 和Adobe Advertising](../data-variances.md)之間的預期資料差異。

>[!MORELIKETHIS]
>
>* [預期資料差異介於 [!DNL Analytics] 和Adobe Advertising](/help/integrations/analytics/data-variances.md)之間
>* [基礎（共 [!DNL Analytics Marketing Channels]](mc-overview.md)個）
>* [使用Adobe Advertising識別碼來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [搭配Adobe Advertising資料使用 [!DNL Analytics Marketing Channels] ](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 進行Adobe Advertising報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hant)
