---
title: 使用EF ID摘要的轉換追蹤
description: 瞭解如何使用EF ID摘要來追蹤轉換資料。
exl-id: db722a54-a9bf-4a31-a285-a82e6d79c34a
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# 使用EF ID摘要的轉換追蹤

在此方法中，Advertising Cloud會收集 `ef_id` 值：每次使用者點按並進入登陸頁面，而廣告商儲存 `ef_id` 值與轉換資料一起使用，並在資料摘要中傳送。

## 實施概述

*代理商客戶經理， [!DNL Adobe] 僅帳戶管理員和管理員使用者角色*

1. 使用帳戶或行銷活動追蹤選項»[!UICONTROL EF Redirect]，」的重新導向型別[!UICONTROL Token]，」和「[!UICONTROL Auto Upload]&quot;以針對帳戶或促銷活動中的每個關鍵字（適用於關鍵字層級的追蹤）或廣告（適用於廣告層級的追蹤），自動產生目的地URL或具有Adobe Advertising權杖(ef_id)的最終URL。

   >[!NOTE]
   >* 此方法不需要廣告商使用Adobe Advertising轉換追蹤標籤。
   >* 如果您將現有帳戶或行銷活動的重新導向型別從 [!UICONTROL Standard] 至 [!UICONTROL Token]，反之亦然，然後您必須重新產生所有適用的追蹤URL。

   一般使用者按一下廣告時，會填入ef_id並附加至登陸頁面URL，且會重新導向至Adobe Advertising伺服器。 然後，ef_id會傳遞至廣告或關鍵字目的地URL或最終URL中的廣告商。 以下是在重新導向期間傳遞給廣告商的目標URL範例：

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. 廣告商會從重新導向擷取ef_id，並將其與相關的轉換資料一起儲存，以包含在摘要檔案中。 請勿變更ef_id或變更其大小寫。

1. （可選用，但建議使用）廣告商可能會為每個交易建立唯一的交易ID，以包含在摘要檔案中。

1. 廣告商上傳包含 [必要的轉換資料](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) 到指定的伺服器位置。

1. 技術服務會剖析上傳檔案中的轉換資料，然後將資料上傳至Adobe Advertising。 然後Adobe Advertising會根據個別關鍵字、廣告和刊登版位追蹤資料，並為每個建立收入預測。

1. 技術服務會根據摘要資料驗證已處理的資料，並檢查任何 [孤立交易](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [轉換摘要檔案的檔案需求](feed-file-requirements.md)
>* [使用EF ID的資料摘要資料需求](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
