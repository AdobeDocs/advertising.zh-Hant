---
title: 渠道資料為何會因Adobe廣告和 [!DNL Marketing Channels]
description: 瞭解AMO ID跟蹤的通道資料為何會因跟蹤的通道資料而有所不同 [!DNL Analytics Marketing Channels]。
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 渠道資料為何會因Adobe廣告和 [!DNL Marketing Channels]

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

用戶學習Adobe廣告與 [!DNL Marketing Channels] 資料集是「導致AMO ID和 [!DNL Marketing Channels]?&quot; 或者，有時，「為什麼資料被破壞？ 我需要所有指標在報告中匹配。」 幸運的是，差異並不表示資料被「破壞」 ，差異是預期甚至是期望的。 讓我們看看為什麼整合是這樣設計的。

這兩個資料集具有不同的主要使用情形：

* [!DNL Marketing Channels]:用於 [!DNL Marketing Channels] 就是用一個通用的屬性模型來比較多個通道的資料。 分析師可以 [!UICONTROL Marketing Channel] 更深入地瞭解頻道如何相互交互。 這一洞見有助於在宏觀層面決定如何投資每個渠道，並有助於瞭解每個渠道的訪問者如何與網站互動。

   的 [!DNL Analytics] [!UICONTROL Marketing Channel] 因此，維配置為捕獲和跟蹤所有通道。 [!DNL Marketing Channels] 還可以配置為捕獲DSP廣告視圖和點擊提取，並且它與其他營銷渠道相關。

* Adobe廣告AMO ID:Adobe廣告AMO ID資料的主要使用情形是提供高級 [!DNL Adobe Sensei]競價算法。 算法自動做出每天成千上萬個微層次的投標決策，以最大化廣告支出，並實現目標 [!DNL DSP] 活動或 [!DNL Search, Social, & Commerce] 投資組合。 算法與市場活動關聯的轉換資料越多，算法就越能做出這些競標決策。

   要收集此資料， [!DNL Analytics for Advertising] 整合會傳遞原始AMO ID，這些AMO ID可以在Adobe Analytics的AMO ID維中轉換為點擊和查看跟蹤代碼，該維儲存為自定義變數(eVar)或保留變數(rVar)。 在AMO ID維中未設定其他通道的點擊提取，因此AMO ID維無法跟蹤來自這些其他通道的條目。 結果是AMO ID持續到 [!DNL Marketing Channels] 輸入點。

有關Adobe廣告跟蹤資料和 [!DNL Analytics] — 跟蹤的資料，請參閱&quot;[預期資料差異 [!DNL Analytics] 和Adobe廣告](../data-variances.md)&quot;

>[!MORELIKETHIS]
>
>* [預期資料差異 [!DNL Analytics] 和Adobe廣告](/help/integrations/analytics/data-variances.md)
>* [基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Adobe廣告ID建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [使用 [!DNL Analytics Marketing Channels] Adobe廣告資料](mc-ac-data.md)
>* [視頻：使用 [!DNL Marketing Channels] 用於Adobe廣告報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)

