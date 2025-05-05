---
title: Adobe Analytics轉換追蹤
description: 瞭解如何在Adobe Advertising中對您的行銷活動使用Adobe Analytics轉換追蹤。
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: a6dc9edb12484499069a68222a3007ae08d9dfea
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analytics轉換追蹤

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

對於與Adobe Advertising-Adobe Analytics整合的廣告商，當您在[競標單位](/help/search-social-commerce/glossary.md#a-b)的點選追蹤URL中使用包含Token （`ef_id`引數）的重新導向，則Advertising Cloud可以將您的廣告點選次數和曝光次數與[!DNL Analytics]追蹤的網站參與和轉換量度連結。 [!DNL Analytics]資料會透過每日摘要檔案自動傳送至Advertising Cloud。

如需整合的詳細資訊，請參閱「[ [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/zh-hant/docs/advertising/integrations/analytics/overview){target="_blank"}的概觀」。

>[!PREREQUISITES]
>
> 搜尋、社交及Commerce廣告商帳戶、[!DNL Analytics]報表套裝和廣告網路帳戶中的時區必須相符。 如果兩者不符，系統間就會發生資料差異。

## 實施概述

1. 在[!DNL Analytics]中，您的搜尋、社交和Commerce實作團隊會修改每個報表套裝的下列組態設定：

   * `ef_id` [!DNL eVar]的到期日已變更，以符合廣告商的Adobe Advertising點按回顧期間。

   * Adobe Advertising的使用者ID。

   * 用於最佳化的標準和自訂事件。

1. 在「搜尋」、「社交」和「Commerce」中，您的實作團隊：

   1. 將現有的廣告網路帳戶階層同步至搜尋、社交和Commerce。

   1. 新增傳遞至追蹤URL且具有&quot;`ef_id`&quot;權杖的重新導向，並將它們張貼至廣告網路。

   此步驟會在重新導向前附加至Adobe Advertising追蹤伺服器（支援平行追蹤的瀏覽器中除了[!DNL Google Ads]和[!DNL Microsoft Advertising]個廣告），並在廣告點選時新增動態填入的&quot;ef_id&quot;引數至URL。 平行追蹤套用時，一般使用者會直接從您的廣告傳送至您的最終URL，而您的追蹤範本URL （包含點選測量）會載入背景。

整合完成後，搜尋、Social和Commerce會自動接收在[!DNL Analytics]中針對已設定報表套裝追蹤的所有頁面上的事件資料。

>[!MORELIKETHIS]
>
>* [轉換追蹤選項](conversion-tracking-about.md)
