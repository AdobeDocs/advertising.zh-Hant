---
title: Adobe Analytics轉換追蹤
description: 瞭解如何在Adobe Advertising中對您的行銷活動使用Adobe Analytics轉換追蹤。
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Adobe Analytics轉換追蹤

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

對於整合Adobe Advertising-Adobe Analytics的廣告商，Advertising Cloud可讓您的廣告點選數和曝光數與網站參與度和轉換量度連結起來，追蹤的量度是 [!DNL Analytics] 當您使用包含Token的重新導向(`ef_id` 引數)，以取得更多資訊。 [競標單位](/help/search-social-commerce/glossary.md#a-b). 此 [!DNL Analytics] 資料會透過每日摘要檔案自動傳送至Advertising Cloud。

請參閱&quot;[概觀 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}」以取得整合的詳細資訊。

>[!PREREQUISITES]
>
> 搜尋、社交和商務廣告商帳戶中的時區， [!DNL Analytics] 報表套裝，且廣告網路帳戶必須相符。 如果兩者不符，系統間就會出現資料差異。

## 實施概述

1. 在 [!DNL Analytics]，您的搜尋、社交和商務實作團隊會修改每個報表套裝的下列組態設定：

   * 的有效期 `ef_id` [!DNL eVar] 已變更，以符合廣告商的Adobe Advertising點按回顧期間。

   * Adobe Advertising的使用者ID。

   * 用於最佳化的標準和自訂事件。

1. 在Search、Social和Commerce中，您的實作團隊：

   1. 將現有的廣告網路帳戶階層同步至「搜尋」、「社交」和「商務」。

   1. 使用&quot;新增重新導向`ef_id`&quot; token傳遞至追蹤URL並將它們張貼至廣告網路。

   此步驟會在重新導向前附加至Adobe Advertising追蹤伺服器（以下步驟除外） [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 在支援平行追蹤的瀏覽器中新增廣告)，並在廣告點選時將動態填入的「ef_id」引數新增至URL。 平行追蹤套用時，一般使用者會直接從您的廣告傳送至您的最終URL，而您的追蹤範本URL （包含點選測量）會載入背景。

整合完成後，Search、Social和Commerce會自動接收中追蹤的所有頁面上的事件資料 [!DNL Analytics] 針對已設定的報表套裝。

>[!MORELIKETHIS]
>
>* [轉換追蹤選項](conversion-tracking-about.md)
