---
title: 關於 [!UICONTROL CCPA Opt-out-of-Sale] 區段與報表
description: 了解如何建立區段以追蹤CCPA選擇退出銷售請求的ID，以及如何擷取ID的報表。
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 關於 [!UICONTROL CCPA Opt-out-of-Sale] 區段與報表

您可以根據加州消費者隱私法(CCPA)，在您的網站上追蹤來自消費者選擇退出銷售請求的使用者ID，依 [建立並實作CCPA選擇退出銷售區段](ccpa-opt-out-segment-create.md). 使用者無限期保留在CCPA選擇退出銷售的區段中。

實作區段像素標籤後，Adobe廣告將開始代表廣告商收集一組ID。

## 消費者選擇退出銷售報表

Adobe廣告會產生客戶針對帳戶選擇退出銷售請求所提交的ID每月報表。 資料整合了使用在DSP中建立的CCPA選擇退出銷售區段所擷取的請求，以及透過Privacy ServiceAPI提交的任何請求。  報表是在前一個月的每月第一日產生。 例如，6月的每月使用者清單可在7月1日提供。

每個報表都以Tab分隔的文字檔壓縮為GZIP格式。 在CCPA選擇退出銷售區段中擷取的使用者ID是由區段和廣告商識別。

您可以 [擷取每月報表的連結](ccpa-opt-out-segment-report-retrieve.md) 是在前三個月建立，可在DSP內或透過使用DSP [!DNL Trafficking API]. 每個連結的有效期為7天，但每次客戶嘗試擷取時都會重新整理。

>[!MORELIKETHIS]
>
>* [加州消費者隱私法的Adobe廣告支援：消費者選擇退出支援](/help/privacy/ccpa-opt-out-of-sale.md)
>* [建立和實作 [!UICONTROL CCPA Opt-Out-of-Sale] 區段](ccpa-opt-out-segment-create.md)
>* [擷取消費者選擇退出銷售報表](ccpa-opt-out-segment-report-retrieve.md)
>* [關於Audience Management](audience-about.md)

