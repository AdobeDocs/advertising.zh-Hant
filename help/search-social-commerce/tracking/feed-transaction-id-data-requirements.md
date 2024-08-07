---
title: 使用交易ID的資料摘要資料需求
description: 參考使用交易ID之資料摘要的資料需求。
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# 使用交易ID的資料摘要資料需求

以下是每種摘要檔案型別的標題欄位和對應資料欄位。

>[!NOTE]
>* 只要後續列中的資料遵循相同順序，標題就可以採用任何順序。 如果您不包含標題，則資料列的順序必須與每個摘要檔案一致。
>* 摘要檔案的每一行都必須包含一個交易的資料，而且該交易必須以交易ID識別。

| 標題欄位/欄名稱 | 型別 | 說明 |
| ---- | ---- | ---- |
| 交易ID (ev_transid) | 區分大小寫的字串 | 與交易相關聯的廣告商產生的識別碼。 由於Adobe Advertising轉換追蹤標籤是用於交易的線上部分，因此這必須與Adobe Advertising為交易前部分提供的交易ID (ev_transid)相同。 這表示交易的線上部分的轉換標籤必須包含唯一交易ID的轉換量度。<br><br>**注意：** Adobe Advertising會使用識別碼來尋找舊的交易資料，並根據商定的插入模式來更新資料（例如，取代現有資料或增加新資料）。 |
| 交易日期 | 日期時間 | 交易的日期。 每個交易的格式必須一致。 |
| 使用者端特定轉換 | 字串 | 正在追蹤的轉換（例如交易型別或金額）。 在開始摘要之前，請先與Adobe Advertising實作團隊討論要包含的轉換。 |

## 範例

以下範例檔案包含兩個轉換量度（產品和收入）的資料。

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [轉換摘要檔案的檔案需求](feed-file-requirements.md)
>* [使用交易ID摘要的轉換追蹤](/help/search-social-commerce/tracking/feed-transaction-id.md)
