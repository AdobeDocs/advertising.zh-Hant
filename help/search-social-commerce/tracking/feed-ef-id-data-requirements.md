---
title: 使用EF ID的資料摘要資料需求
description: 參考使用EF ID之資料摘要的資料需求。
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# 使用EF ID的資料摘要資料需求

以下是每種摘要檔案型別的標題欄位和對應資料欄位。

>[!NOTE]
>* 只要後續列中的資料遵循相同順序，標題就可以採用任何順序。 如果您不包含標題，則資料列的順序必須與每個摘要檔案一致。
>* 摘要檔案的每一行都必須包含一個交易的資料，而該交易必須由Adobe Advertising產生的ef_id (token)識別。

| 標題欄位/欄名稱 | 型別 | 說明 |
| ---- | ---- | ---- |
| EF ID | 區分大小寫的字串 | 您在點選交易時擷取的ef_id （代號），包含瀏覽者ID、點選時間和網路型別。 請勿變更值。 |
| 交易ID | 區分大小寫的字串 | （可選用，但建議使用）廣告商產生的交易ID。 即使重新導向時使用了ef_id來追蹤交易，最佳實務還是要將此納入每個交易。 |
| 交易日期 | 日期時間 | 交易的日期。 每個交易的格式必須一致。 |
| 使用者端特定轉換 | 字串 | 正在追蹤的轉換（例如交易型別或金額）。 在開始摘要之前，請先與Adobe Advertising實作團隊討論要包含的轉換。 |

## 範例

以下範例檔案包含兩個轉換量度（產品和收入）的資料。

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [轉換摘要檔案的檔案需求](feed-file-requirements.md)
>* [使用EF ID摘要的轉換追蹤](/help/search-social-commerce/tracking/feed-efid.md)
