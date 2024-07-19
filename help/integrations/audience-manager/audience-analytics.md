---
title: Adobe Advertising客戶的'[!DNL Adobe] [!DNL Audience Analytics] '
description: 瞭解如何將 [!DNL Adobe] [!DNL Audience Analytics]用於廣告使用案例
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Adobe Advertising客戶的[!DNL Adobe] [!DNL Audience Analytics]

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)是Adobe Audience Manager與Adobe Analytics之間的整合，可讓Audience Manager客戶將區段傳送至[!DNL Analytics]，以取得關於網站活動的豐富見解。

Adobe Advertising客戶可藉由使用[!DNL Audience Analytics]而獲益。 整合可讓您：

* 將Adobe Advertising曝光資料直接傳送給[!DNL Analytics]，以判斷上層漏斗活動對下游網站活動的影響。

* 從上層漏斗曝光度廣告判斷行銷管道和網站進入點。

* 將與[!DNL Analytics for Advertising]的整合分層，以便納入[Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html)的第三方人口統計區段（包含[!DNL Analytics for Advertising]資料），以取得使用者設定檔的更多深入解析。

  [!DNL Audience Marketplace]提供使用「啟用」訂閱模式存取協力廠商資料摘要的功能，這可讓購買者將資料傳送至目的地。 若資料用於[!DNL Analytics]目的地，則不會套用啟用費用。

* (使用Advertising DSP的廣告商)新增其他曝光區段，以獲得整體歷程管理見解。

  Advertising DSP可透過Adobe Experience Platform或Audience Manager曝光追蹤畫素的實作，將曝光資料當作可操作的訊號傳送給Audience Manager。 將相同的資料轉送至[!DNL Analytics]可啟用進階資料分析。 如需詳細資訊，請參閱「[Adobe Advertising Media資料與Adobe Audience Manager整合概述](/help/integrations/audience-manager/media-data-integration/overview.md)」。

如需[!DNL Audience Analytics]的詳細資訊，包括其必要條件和工作流程，請參閱&quot;[Audience Analytics概觀](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)&quot;。

## 如何將[!DNL Audience Analytics]資料與Adobe Advertising資料搭配使用的範例

以下範例說明如何在[!DNL Analytics] [!DNL Analysis Workspace]中使用合併的資料。

### 檢視上層漏斗活動對下游活動的影響

使用Audience Manager曝光區段來檢視上層漏斗網站活動對下游網站活動的影響。 在追蹤畫素中加入Adobe Advertising或協力廠商巨集ID，以追蹤對詳細層級的影響，從行銷活動層級到使用者公開所在的網站層級。

主要優點：

* 依漏斗/廣告型別追蹤曝光，並使用[!DNL Audience Analytics]來決定進入率及與客戶歷程下一階段重疊。

* 判斷上層漏斗活動對下游網站活動的影響。

* 連線[!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event -->和[!DNL Audience Analytics]資料<!-- (which includes the user's last exposure event) -->以決定網站的整體歷程。

以下是您可以在[!DNL Analysis Workspace]中建立的報表範例。

![檢視上層漏斗活動對下游網站活動的影響](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 使用[!DNL Audience Analytics]第三方區段資料進行使用者設定檔分析

使用協力廠商Audience Manager區段，以更全面分析使用者如何與您的網站互動。 您可以使用資訊，根據第三方區段的設定檔與媒體行銷活動網站的關鍵績效指標互動的方式，決定要為其啟用媒體的新第三方對象。

>[!TIP]
> 在整個[!DNL Analytics]中使用Audience Manager`Audiences ID`和`Audiences Name`維度，就像[!DNL Analytics]收集的任何其他維度一樣。

以下是您可以在[!DNL Analysis Workspace]中建立的報表範例。

![使用協力廠商區段來豐富使用者設定檔分析](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [與Adobe Audience Manager的Adobe Advertising整合](/help/integrations/audience-manager/overview.md)
