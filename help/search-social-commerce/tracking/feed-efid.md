---
title: 使用EF ID摘要的轉換追蹤
description: 瞭解如何使用EF ID摘要來追蹤轉換資料。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# 使用EF ID摘要的轉換追蹤

在此方法中，Advertising Cloud會收集 `ef_id` 當使用者每次點按及廣告並到達登陸頁面，而廣告商儲存 `ef_id` 值和轉換資料，並在資料摘要中傳送。

## 實施概述

*代理商客戶經理， [!DNL Adobe] 僅帳戶管理員和管理員使用者角色*

1. 使用帳戶或行銷活動追蹤選項»[!UICONTROL EF Redirect]，」的重新導向型別[!UICONTROL Token]，」和「[!UICONTROL Auto Upload]&quot;以針對帳戶或促銷活動中的每個關鍵字（用於關鍵字層級的追蹤）或廣告（用於廣告層級的追蹤），自動產生目的地URL或具有Adobe廣告權杖(ef_id)的最終URL。

   >[!NOTE]
   >* 此方法不需要廣告商使用Adobe廣告轉換追蹤標籤。
   >* 如果您將現有帳戶或行銷活動的重新導向型別從 [!UICONTROL Standard] 至 [!UICONTROL Token]，反之亦然，則必須重新產生所有適用的追蹤URL。


   一般使用者按一下廣告時，會填入ef_id並將其附加至登陸頁面URL，接著會重新導向至AdobeAdvertising伺服器。 然後，會將ef_id傳遞至廣告或關鍵字目的地URL或最終URL中的廣告商。 以下是在重新導向期間傳遞給廣告商的目標URL範例：

   http://pixel.everesttech.net/1180/cq?ev_sid=3&amp;ev_ln={keyword}&amp;ev_crx={creative}&amp;ev_mt={matchtype}&amp;ev_n={network}&amp;ev_ltx=&amp;ev_pl={placement}&amp;url=http%3A//www.example.com&amp;ef_id=D59Nu0u@BD0AAM1q:20110630172936:s

1. 廣告商會從重新導向擷取ef_id，並將其與相關的轉換資料儲存，以包含在摘要檔案中。 請勿變更ef_id或變更其大小寫。

1. （可選用，但建議使用）廣告商可能會為每個交易建立唯一的交易ID，以包含在摘要檔案中。

1. 廣告商上傳的檔案包含 [必要的轉換資料](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) 至指定的伺服器位置。

1. 技術服務會剖析上傳檔案中的轉換資料，然後將資料上傳至Adobe廣告。 Adobe廣告接著會根據個別關鍵字、廣告和刊登版位追蹤資料，並為每個關鍵字建立收入預測。

1. 技術服務會根據摘要資料驗證已處理的資料，並檢查是否有任何 [孤立交易](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [轉換摘要檔案的檔案需求](feed-file-requirements.md)
>* [使用EF ID的資料摘要資料需求](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)



