---
title: 基本 [!DNL Marketing Channels]
description: 瞭解關於 [!DNL Analytics Marketing Channels] 那 [!DNL Analytics for Advertising] 用戶應該理解。
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 基本 [!DNL Analytics Marketing Channels]

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

本頁說明有關 [!DNL Analytics Marketing Channels] 那 [!DNL Analytics for Advertising] 用戶需要理解。

有關 [!DNL Marketing Channels]，請參閱「」[入門 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)&quot;

## 概述 [!DNL Marketing Channels]

[!DNL Marketing Channels] 是Adobe Analytics的關鍵特徵。 [!DNL Marketing Channels] 報告顯示客戶如何通過報告窗口到達您的網站，以及每個渠道如何影響收入或現場行為。

請考慮以下交叉訪問旅程示例。 訪問您網站的每次訪問都由訪問者輸入的營銷渠道來表示。 第一次訪問，也稱為「First Touch Channel」，是電子郵件。 「訪問2時顯示」是參與的頻道，「自然搜索」被視為「上次觸摸」頻道。 如果您使用 [!UICONTROL Last Touch Attribution] 內 [!UICONTROL Attribution IQ],Natural Search將獲得250美元轉換事件的全額貸項。 使用Experience Cloud身份證服務，您可以將這些個人訪問聯繫在一起，以顯示單個訪問者的一次旅程。

![市場營銷渠道中的交叉訪問轉換過程示例](/help/integrations/assets/a4adc-mc-sample-journey.png)

使用 [!UICONTROL Marketing Channels] 處理規則，您可以建立一組邏輯來確定驅動通信的通道，並在用戶到達您的站點時跟蹤每個通道。 例如， [!UICONTROL Email] 頻道將由按一下時生成的唯一跟蹤代碼來表示，當Adobe Analytics登錄時，該代碼會將訪問歸類為來自電子郵件營銷活動。

## 處理規則和如何設定市場營銷渠道

每次用戶訪問網站時，都會通過他們按一下或直接鍵入到地址欄的URL進行訪問。 當用戶進入網站時， [!DNL Analytics] 跟蹤可用於確定訪問渠道的資訊。

通常，營銷人員會將查詢字串參數跟蹤代碼附加到通道URL，以幫助跟蹤通道對其站點的影響。 您可以配置 [!DNL Marketing Channels] 處理規則以偵聽特定跟蹤參數和值以確定沒有任何附加跟蹤的通道。 例如，如果所有電子郵件市場活動URL都遵循格式 `www.adobe.com?cid=email…` (其中URL包含查詢字串參數和值 `cid=email`)，然後可以建立規則來偵聽此跟蹤代碼並將訪問儲存在 [!UICONTROL Email] 頻道。

其他頻道沒有可跟蹤的URL路徑，需要進一步的邏輯進行標識。 比如說， [!UICONTROL Earned Social]用戶點擊另一個用戶在社交網路上有機共用的連結，是跟蹤的重要渠道。 但是，商家無法將查詢字串參數跟蹤代碼附加到共用的URL。 在這種情況下，您可以建立處理規則來偵聽興趣社交網路的引用域以及沒有付費跟蹤代碼來確定通道。 然後，在「營銷渠道」報告中，將以「掙得的社會」的形式跟蹤滿足這些要求的訪問。

Adobe建議與分析團隊合作，構建一組 [!DNL Marketing Channels] 處理規則以跟蹤與您的業務相關的所有渠道。 這樣可以建立功能強大的屬性報告。

要瞭解Adobe廣告可以如何促進建立自定義營銷渠道所需的信號，請參閱[使用廣告ID建立 [!DNL Marketing Channels] 規則](mc-ids.md)&quot;

>[!MORELIKETHIS]
>
>* [使用Adobe廣告ID建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [渠道資料為何會因Adobe廣告和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] Adobe廣告資料](mc-ac-data.md)
>* [視頻：使用 [!DNL Marketing Channels] 用於Adobe廣告報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

