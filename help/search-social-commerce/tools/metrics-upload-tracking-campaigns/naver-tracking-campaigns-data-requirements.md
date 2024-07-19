---
title: ' [!DNL Naver] 僅限追蹤帳戶的流量和轉換量度的資料需求'
description: 參考 [!DNL Naver] 只追蹤帳戶的資料上傳需求。
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Naver]只追蹤帳戶的量度資料需求

以下為僅限追蹤帳戶的[!DNL Naver]流量和轉換量度的資料需求。

資料檔案必須是TSV、CSV或TXT格式。

以下標題欄位為必填欄位及選用欄位。 每個資料列都必須包含至少一個量度欄位的每日彙總值。

| 標題欄位/欄名稱 | 型別 | 說明 |
| ---- | ---- | ---- |
| 期間 | 日期時間 | 資料套用的日期，格式為`YYYY.MM.DD.` （例如`2019.11.15.`，一天後有句點）。 |
| Campaign | 區分大小寫的字串 | 行銷活動名稱。 |
| 廣告群組（一個字） | 區分大小寫的字串 | 廣告群組名稱。 |
| 關鍵字 | 區分大小寫的字串 | （關鍵字廣告）產生廣告的關鍵字。 |
| [量度] | 整數 | （選用）度量正在測量]的[數目。</br><br>標準量度包括曝光數、成本和點按數。 您可以從廣告網路包含您想要的任何其他量度。 將每個量度納入個別欄。<br><br><b>附註：</b><ul><li>「成本」的欄標題必須是「成本(KRW)」。</li><li>若要納入品牌廣告的成本(KRW)，請在廣告群組層級手動將每月固定成本除以日。</li><li>移除標準量度值中的所有逗號。 例如，使用1000而非1,000。</li><li>對於null值，請使用0。</li></ul> |

>[!MORELIKETHIS]
>
>* [實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [附錄 —  [!DNL Naver] 帳戶](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)的必要大量表單資料
>* [上傳 [!DNL Naver] 僅限追蹤帳戶](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)的流量和轉換量度
