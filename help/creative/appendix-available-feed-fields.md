---
title: 動態廣告摘要檔案的可用欄位
description: 瞭解您可以在用於建立動態廣告的摘要檔案中包含的欄位。
feature: Creative Dynamic Ads
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 附錄：動態廣告摘要檔案的可用欄位

Advertising Creative後端提供下列摘要欄位。 您可以上傳使用您組織特定欄位名稱的[摘要檔案](/help/creative/feeds/asset-manage.md)。 不過，您必須先將摘要檔案中的每個欄位對應到[摘要範本](/help/creative/feeds/catalog-manage.md)中的下列其中一個欄位，才能從摘要檔案建立[目錄](/help/creative/feeds/feed-template-manage.md)，您將使用該欄位來建立目錄。

您的摘要檔案中唯一必須具備同等值的欄位是`PART_NUM`。

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| 欄位名稱 | 資料型別 | 必填？ |
|------------|-----------|-----------|
| PART_NUM | varchar(64) | 是 |
| PRODUCT_NAME | 文字 | 否 |
| PRODUCT_URL | 文字 | 否 |
| 價格 | decimal(10,2) | 否 |
| DISCOUNT_PRICE | decimal(10,2) | 否 |
| 影像 | varchar(1024) | 否 |
| IMAGE_HEIGHT | int | 否 |
| IMAGE_WIDTH | int | 否 |
| IMAGE_1 | varchar(1024) | 否 |
| IMAGE_2 | varchar(1024) | 否 |
| IMAGE_3 | varchar(1024) | 否 |
| IMAGE_4 | varchar(1024) | 否 |
| IMAGE_5 | varchar(1024) | 否 |
| IMAGE_6 | varchar(1024) | 否 |
| IMAGE_7 | varchar(1024) | 否 |
| IMAGE_8 | varchar(1024) | 否 |
| IMAGE_9 | varchar(1024) | 否 |
| IMAGE_10 | varchar(1024) | 否 |
| TEXT_1 | 文字 | 否 |
| TEXT_2 | 文字 | 否 |
| TEXT_3 | 文字 | 否 |
| TEXT_4 | 文字 | 否 |
| TEXT_5 | 文字 | 否 |
| TEXT_6 | 文字 | 否 |
| TEXT_7 | 文字 | 否 |
| TEXT_8 | 文字 | 否 |
| TEXT_9 | 文字 | 否 |
| TEXT_10 | 文字 | 否 |
| TEXT_11 | 文字 | 否 |
| TEXT_12 | 文字 | 否 |
| TEXT_13 | 文字 | 否 |
| TEXT_14 | 文字 | 否 |
| TEXT_15 | 文字 | 否 |
| ADDITIONAL_PRICE_1 | decimal(10,2) | 否 |
| ADDITIONAL_PRICE_2 | decimal(10,2) | 否 |
| ADDITIONAL_PRICE_3 | decimal(10,2) | 否 |
| AD_SIZE | varchar(32) | 否 |
| 排名 | int | 否 |
| 國家 | 文字 | 否 |
| 狀態 | 文字 | 否 |
| 城市 | 文字 | 否 |
| ZIP | 文字 | 否 |
| DMA | 文字 | 否 |
| PROFILE_FILTER_1 | 文字 | 否 |
| PROFILE_FILTER_2 | 文字 | 否 |
| PROFILE_FILTER_3 | 文字 | 否 |
| PROFILE_FILTER_4 | 文字 | 否 |
| PROFILE_FILTER_5 | 文字 | 否 |
| DATAPASS_FILTER_1 | 文字 | 否 |
| DATAPASS_FILTER_2 | 文字 | 否 |
| DATAPASS_FILTER_3 | 文字 | 否 |
| DATAPASS_FILTER_4 | 文字 | 否 |
| DATAPASS_FILTER_5 | 文字 | 否 |
| AUDIENCE_SEGMENT | 文字 | 否 |
| 語言 | 文字 | 否 |
| Creative_ATTRIBUTE_1 | varchar(256) | 否 |
| Creative_ATTRIBUTE_2 | varchar(256) | 否 |
| Creative_ATTRIBUTE_3 | varchar(256) | 否 |
| Creative_ATTRIBUTE_4 | varchar(256) | 否 |
| Creative_ATTRIBUTE_5 | varchar(256) | 否 |
| Creative_ATTRIBUTE_6 | varchar(256) | 否 |
| Creative_ATTRIBUTE_7 | varchar(256) | 否 |
| Creative_ATTRIBUTE_8 | varchar(256) | 否 |
| Creative_ATTRIBUTE_9 | varchar(256) | 否 |
| Creative_ATTRIBUTE_10 | varchar(256) | 否 |
| IS_DEFAULT | 列舉 | 否 |

>[!MORELIKETHIS]
>
>* [動態廣告的工作流程](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理資產檔案](/help/creative/feeds/asset-manage.md)
>* [管理摘要範本](/help/creative/feeds/feed-template-manage.md)
>* [管理目錄](/help/creative/feeds/catalog-manage.md)
