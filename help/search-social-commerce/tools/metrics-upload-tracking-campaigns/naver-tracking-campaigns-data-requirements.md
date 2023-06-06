---
title: 以下專案的流量和轉換量度的資料需求： [!DNL Naver] 僅限追蹤的帳戶
description: 參考以下專案的資料上傳需求： [!DNL Naver] 僅限追蹤的帳戶。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 的量度資料需求 [!DNL Naver] 僅限追蹤的帳戶

以下為的資料需求 [!DNL Naver] 僅限追蹤帳戶的流量和轉換量度。

資料檔案必須是TSV、CSV或TXT格式。

以下標題欄位為必填欄位和選用欄位。 每個資料列都必須包含至少一個量度欄位的每日彙總值。

| 標題欄位/欄名稱 | 型別 | 說明 |
| ---- | ---- | ---- |
| 期間 | 日期時間 | 資料套用的日期，格式為 `YYYY.MM.DD.` (例如 `2019.11.15.`，在天后加上句號)。 |
| Campaign | 區分大小寫的字串 | 行銷活動名稱。 |
| 廣告群組（一個字） | 區分大小寫的字串 | 廣告群組名稱。 |
| 關鍵字 | 區分大小寫的字串 | （關鍵字廣告）產生廣告的關鍵字。 |
| [量度] | 整數 | （選用）數量 [無論量度測量的是什麼].</br><br>標準量度包括曝光數、成本和點按次數。 您可以從廣告網路包含您想要的任何其他量度。 將每個量度納入個別欄。<br><br><b>附註：</b><ul><li>「成本」的欄標題必須是「成本(KRW)」。</li><li>若要納入品牌廣告的成本(KRW)，請在廣告群組層級手動將每月固定成本除以日。</li><li>移除標準量度值中的所有逗號。 例如，使用1000而非1,000。</li><li>對於null值，請使用0。</li></ul> |

>[!MORELIKETHIS]
>
>* [實作 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [附錄 — 必要的大量表單資料 [!DNL Naver] 帳戶](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [上傳的流量和轉換量度 [!DNL Naver] 僅限追蹤的帳戶](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)

