---
title: 轉換摘要檔案的檔案需求
description: 參考轉換摘要檔案的需求。
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# 轉換摘要檔案的檔案需求

以下是摘要檔案的檔案格式、必要和選用資料欄位、檔案名稱和檔案傳輸通訊協定需求。

## 檔案格式

資料檔案必須是純文字(TXT)、逗號分隔值(CSV)或定位點分隔值(TSV)格式。 檔案可能由標題列和資料列組成，其值由定位字元、逗號或其他字元（但不含空格）分隔：

* **標頭列：** （選擇性）檔案的第一行是標頭，以特定順序指定必要的欄位名稱（或欄名稱），並以定位字元或逗號分隔。 必要的欄名稱包含Adobe Advertising追蹤為轉換的轉換量度。

* **資料列：**&#x200B;每個後續行都包含與標題順序相同的資料欄位，並以定位字元或逗號分隔。 如果第一個記錄不是標題，則每個資料列都必須以指定順序包含所有可能的欄位。 所有ID和轉換量度的值都必須是英數字元。

  如果一或多個廣告上的多次點按導致一項交易，則您必須決定歸因於交易的點按ID和追蹤ID。 因為會針對每個交易報告唯一ID，所以您可以更新個別交易。

## 檔案命名慣例

檔案名稱必須包含日期且必須一致。 例如，如果您使用YYYYMMDD.txt格式，則在2011年5月15日傳送的檔案必須命名為20110515.txt。

## 檔案傳輸通訊協定

使用連線埠22，透過SFTP傳輸通訊協定傳送檔案。 您必須提供公開金鑰資訊。  您的Adobe帳戶團隊或實作團隊會提供您伺服器位置，以及系統傳輸檔案所需的認證。

>[!TIP]
>
>轉換資料摘要一天會處理多次。 在當地時間午夜12:00後儘快上傳每日摘要，讓Adobe Advertising可以處理您的資料，並在凌晨於報表UI中提供。

>[!MORELIKETHIS]
>
>* [使用EF ID的資料摘要資料需求](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [使用交易ID的資料摘要資料需求](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
