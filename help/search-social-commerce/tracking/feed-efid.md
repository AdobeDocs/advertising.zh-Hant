---
title: 使用EF ID摘要的轉換追蹤
description: 瞭解如何使用EF ID摘要來追蹤轉換資料。
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# 使用EF ID摘要的轉換追蹤

在此方法中，每當使用者點按及廣告並到達登陸頁面時，Advertising Cloud就會收集`ef_id`值，且廣告商會儲存轉換資料的`ef_id`值，並將其傳送至資料摘要中。

## 實施概述

*僅限代理商帳戶管理員、[!DNL Adobe]帳戶管理員和系統管理員使用者角色*

1. 使用帳戶或行銷活動追蹤選項&quot;[!UICONTROL EF Redirect]&quot;、重新導向型別&quot;[!UICONTROL Token]&quot;及&quot;[!UICONTROL Auto Upload]&quot;，針對帳戶或行銷活動中的每個關鍵字（用於關鍵字層級的追蹤）或廣告（用於廣告層級的追蹤），自動產生目的地網址或具有Adobe Advertising權杖(ef_id)的最終URL。

   >[!NOTE]
   >* 此方法不需要廣告商使用Adobe Advertising轉換追蹤標籤。
   >* 如果您將現有帳戶或行銷活動的重新導向型別從[!UICONTROL Standard]切換為[!UICONTROL Token] （或反之），則必須重新產生所有適用的追蹤URL。

   一般使用者按一下廣告時，會填入ef_id並附加至登陸頁面URL，且會重新導向至Adobe Advertising伺服器。 然後，ef_id會傳遞至廣告或關鍵字目的地URL或最終URL中的廣告商。 以下是在重新導向期間傳遞給廣告商的目標URL範例：

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. 廣告商會從重新導向擷取ef_id，並將其與相關的轉換資料一起儲存，以包含在摘要檔案中。 請勿變更ef_id或變更其大小寫。

1. （可選用，但建議使用）廣告商可能會為每個交易建立唯一的交易ID，以包含在摘要檔案中。

1. 廣告商會將含有[必要轉換資料](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)的檔案上傳到指定的伺服器位置。

1. 技術服務會剖析上傳檔案中的轉換資料，然後將資料上傳至Adobe Advertising。 然後Adobe Advertising會根據個別關鍵字、廣告和刊登版位追蹤資料，並為每個建立收入預測。

1. 技術服務會根據摘要資料驗證已處理的資料，並檢查是否有任何[孤立交易](/help/search-social-commerce/glossary.md#o-p)。

>[!MORELIKETHIS]
>
>* [轉換摘要檔案的檔案需求](feed-file-requirements.md)
>* [使用EF ID的資料摘要資料需求](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
