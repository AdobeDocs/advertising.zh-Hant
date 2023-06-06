---
title: 使用交易ID摘要的轉換追蹤
description: 瞭解如何使用交易ID摘要來追蹤轉換資料。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# 使用交易ID摘要的轉換追蹤

當廣告商同時具有線上和離線交易時，Adobe廣告可以透過Adobe廣告轉換追蹤畫素來追蹤線上交易，而廣告商可以使用交易ID來追蹤離線交易，並透過摘要來傳遞：

* 對於線上交易，Adobe廣告會追蹤您廣告上的點按次數，以及您網站上產生的交易。

* 廣告商必須追蹤離線轉換，並將交易層級的摘要檔案傳送至Adobe廣告。

## 實施概述

*代理商客戶經理， [!DNL Adobe] 僅帳戶管理員和管理員使用者角色*

1. 使用帳戶或行銷活動追蹤選項»[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]&quot;，為帳戶或行銷活動中的每個關鍵字（用於關鍵字層級的追蹤）或廣告（用於廣告層級的追蹤）自動產生目的地URL或最終URL。

1. 設定線上轉換的Adobe廣告轉換追蹤。 此程式與使用Adobe廣告畫素型轉換追蹤的廣告商相同。 產生包含唯一交易ID的引數的轉換標籤很重要(`ev_transid=<transid>`)。

1. 對於每個交易的離線部分，廣告商會產生與交易線上部分相同的交易ID，以包含在摘要檔案中。

1. 廣告商上傳的檔案包含 [必要的轉換資料](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) 至指定的伺服器位置。

1. 技術服務會剖析上傳檔案中的轉換資料，然後將資料上傳至Adobe廣告。 Adobe廣告接著會根據個別關鍵字、廣告和刊登版位追蹤資料，並為每個關鍵字建立收入預測。

1. 技術服務會根據摘要資料驗證已處理的資料，並檢查是否有任何 [孤立交易](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [轉換摘要檔案的檔案需求](feed-file-requirements.md)
>* [使用交易ID的資料摘要資料需求](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

