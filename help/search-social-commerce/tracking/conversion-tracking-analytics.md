---
title: Adobe Analytics轉換追蹤
description: 瞭解如何在Adobe廣告中對您的行銷活動使用Adobe Analytics轉換追蹤。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Adobe Analytics轉換追蹤

*僅整合AdobeAdvertising-Adobe Analytics的廣告商*

對於整合Advertising-Adobe AnalyticsAdobe的廣告商，Advertising Cloud可將您的廣告點選數和曝光數與網站參與度和轉換量度連結起來，追蹤的量度是 [!DNL Analytics] 當您使用包含Token的重新導向(`ef_id` 引數)，以取得更多資訊。 [競標單位](/help/search-social-commerce/glossary.md#a-b). 此 [!DNL Analytics] 資料會透過每日摘要檔案自動傳送至Advertising Cloud。

請參閱「[概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html)」以取得整合的詳細資訊。

>[!PREREQUISITES]
>
> 搜尋、社交和商務廣告商帳戶中的時區， [!DNL Analytics] 報表套裝，且廣告網路帳戶必須相符。 如果兩者不符，系統間就會出現資料差異。

## 實施概述

1. 在 [!DNL Analytics]，您的Search、Social和Commerce實作團隊會修改每個報表套裝的下列組態設定：

   * 的有效期 `ef_id` eVar已變更，以符合Adobe廣告商的點選回顧視窗。

   * AdobeAdvertising使用者ID。

   * 用於最佳化的標準和自訂事件。

1. 在Search、Social和Commerce中，您的實作團隊：

   1. 將現有的廣告網路帳戶階層同步至Search、Social和Commerce。

   1. 使用「」新增重新導向`ef_id`&quot; token傳遞至追蹤URL並將它們張貼至廣告網路。
   此步驟會在重新導向前附加至Adobe廣告追蹤伺服器（以下專案除外）： [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 瀏覽器中支援平行追蹤的廣告)，並在廣告點選時將動態填入的「ef_id」引數新增至URL。 平行追蹤套用時，會將一般使用者從您的廣告直接傳送至您的最終URL，而您的追蹤範本URL （包含點選測量）會載入背景。

整合完成後，Search、Social和Commerce會自動接收所有追蹤的頁面上的事件資料 [!DNL Analytics] 適用於已設定的報表套裝。

>[!MORELIKETHIS]
>
>* [轉換追蹤選項](conversion-tracking-about.md)

