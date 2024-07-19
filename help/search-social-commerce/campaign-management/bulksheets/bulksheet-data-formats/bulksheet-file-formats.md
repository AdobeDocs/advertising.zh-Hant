---
title: 支援的大量表單檔案格式
description: 請參考Bulksheets的一般檔案需求。
exl-id: f3daf036-8f0c-4c75-9c76-2734abd850ec
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 支援的大量表單檔案格式

## 檔案格式

您可以下載、上傳和張貼支援的廣告網路大量表單檔案，格式如下：

* CSV （逗號分隔值）
* TSV （以定位點分隔的值）
* TXT （Unicode文字），以逗號或定位字元分隔
* ZIP （壓縮）內含一個CSV格式、TSV格式或TXT格式的檔案，並以逗號或定位字元分隔

當您建立/下載大量表單時，它會以指定的檔案格式建立，且檔案中包含所有相關資料。 使用下列資訊編輯檔案中的資料，或手動建立您自己的大量表單。

## 大量表單的基本內容

Bulksheet檔案的第一個記錄（行）包含一組特定的欄名稱，統稱為<i>標題</i>。 標題中的欄名稱以指定的順序排列，並對應於後續資料記錄中的每個欄位。 標題中所需的欄名稱會依廣告網路而有所不同。

每個後續記錄（行）都包含資料，其欄位包含標題中每個欄的值（或沒有值）。

## 檔案大小上限

Bulksheet檔案最大可達2.5 GB，約為250萬列。

>[!NOTE]
>
>當您產生多個行銷活動的大量表單，且合併的資料包含超過500,000列時，行銷活動會將資料分割成兩個或多個檔案（名為`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv`等）。

## 不同檔案型別的格式需求

以索引標籤和逗號分隔的資料欄位需要不同的格式。

### 以索引標籤分隔的TSV檔案和TXT檔案

以索引標籤分隔的TSV檔案和TXT檔案中的資料欄位必須格式化如下：

* 每筆記錄中的欄位會以定位字元分隔。 若要省略欄位的值，請僅使用定位字元。

  範例： `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* 欄位不能包含內嵌的定位字元。

### 以逗號分隔的CSV檔案和TXT檔案

以逗號分隔的CSV檔案和TXT檔案中的資料欄位必須格式化如下：

* 記錄中的欄位以逗號分隔。 若要省略欄位的值，請僅使用逗號。

  範例： `Cruises,5000,Caribbean,,,`

* 任何欄位都可以選擇包含在雙引號(`""`)中。

  範例： `"Cruises","5000","Caribbean",`

* 含有內嵌逗號的欄位必須括在雙引號(`""`)中。

  範例： `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* 含有內嵌雙引號的欄位必須包含在雙引號(`""`)中。

  範例： `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* 含有前置或結尾空格的欄位必須括在雙引號(`""`)中。

  範例： `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](../bulksheet-about.md)
>* [您可以在大量表單中執行的作業](bulksheet-operations.md)
>* [附錄 — Bulksheet錯誤](../bulksheet-errors.md)
>* [下載/建立Bulksheet檔案](../bulksheet-download.md)
