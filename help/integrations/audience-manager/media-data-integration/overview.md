---
title: 傳送DSP Media Exposure資料至Adobe Audience Manager概述
description: 瞭解如何使用Audience Manager事件畫素，從Advertising DSP行銷活動中擷取曝光層級和點選層級的資料
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: c204955ec48826d00a5f78e5be4849f53d09e224
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 傳送DSP Media Exposure資料至Adobe Audience Manager概述

*僅使用Advertising DSP的廣告商*

*僅整合Adobe Advertising-Adobe Audience Manager的廣告商*

具有Adobe Audience Manager的Advertising DSP客戶可以使用Audience Manager事件畫素，從DSP促銷活動擷取曝光層級資料和點按層級資料。 事件畫素會將資料當作可操作的訊號傳送至Audience Manager。 這些訊號可啟用各種DSP使用案例，例如更進階的分段、頻率管理、行銷分析和報表深入分析。

DSP不會向您收取傳送這些訊號給Audience Manager的費用。 不過，您需根據Audience Manager合約，根據伺服器呼叫支付標準Audience Manager擷取成本。 Audience Manager會移除以兩種不同方式追蹤的重複事件，因此每個事件只會收費一次。

>[!NOTE]
>
> Audience Manager也支援從廣告伺服器記錄檔擷取資料，因此提供的彈性較低。 本檔案未涵蓋該程式。

## 主要優點

* DSP促銷活動資料會即時流入Audience Manager，而您可以用它來建立規則型特徵，以用來定義區段。

* 區段可在使用者特徵和區段資格後立即用於鎖定目標，以支援即時鎖定目標工作。

* 您可以將行銷活動資料用於多種使用案例，例如跨創意內容的頻率限定、重新定位接觸到先前行銷活動的使用者，以及分析下游網站行為和登入點。

* 彙總資料可提供行銷活動績效的統一檢視，有助於識別自訂轉換路徑，並可用於透過Audience Manager[!DNL Audience Optimization Reports]或透過[[!DNL Audience Analytics] 與Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md)的整合來改善導致轉換的事件順序。

## 如何追蹤資料

Audience Manager曝光次數和點選事件畫素會以Cookie為基礎。 畫素不會擷取在沒有Cookie的環境中發生的事件，例如行動應用程式和連線電視(CTV)。<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### 曝光追蹤畫素

當您在廣告中附加1xl畫素透明事件追蹤畫素時，Audience Manager會追蹤廣告的曝光資料。 每次將廣告提供給使用者並由網頁瀏覽器載入時，都會載入事件畫素。 此畫素是從使用者端專屬的子網域[`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)載入，這是Audience Manager的舊版網域，且包含索引鍵值配對的引數。 事件呼叫會收集曝光次數和轉換資料，並傳送給Audience Manager資料收集伺服器。

### 點選追蹤畫素

Audience Manager追蹤的點按次數與曝光數類似，不同之處在於它不會在每次提供廣告時載入透明事件畫素。 相反地，點選資料會在廣告的點進URL中追蹤。 廣告指向[`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)的使用者端特定子網域，這是Audience Manager的舊網域，可供Audience Manager資料收集伺服器處理。 然後，伺服器會將使用者重新導向至預期的登陸頁面。 URL包含做為機碼值組的引數。

>[!NOTE]
>
>如果您的組織使用[!DNL Analytics]追蹤，則您可能不需要Audience Manager點選追蹤。 Adobe Analytics會擷取點選訊號，並可透過[伺服器端轉送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html)傳送給Audience Manager。

>[!MORELIKETHIS]
>
>* [收集來自Advertising DSP行銷活動的點按和曝光資料](collect.md)
>* [使用案例](use-cases.md)
