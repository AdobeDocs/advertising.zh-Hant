---
title: 關於[!UICONTROL CCPA Opt-out-of-Sale]個區段和報表
description: 瞭解如何建立區段來追蹤CCPA選擇退出銷售請求中的ID，以及如何擷取ID報表。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
TQID: https://experienceleague.adobe.com/Bp8Fj0z7lqSXmHd-aJQa6ocQyj6FVQuydArNBucpJp4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: c193c532-b70e-4556-bde7-857186cbe140
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 0%

---

# 關於[!UICONTROL CCPA Opt-out-of-Sale]個區段和報表

您可以根據《加州消費者隱私法》(CCPA)，透過[建立及實作CCPA選擇退出銷售區段](ccpa-opt-out-segment-create.md)，在您的網站上追蹤消費者選擇退出銷售請求的使用者ID。 使用者會無限期留在CCPA選擇退出銷售區段中。

實施區段畫素標籤後，Adobe Advertising會開始代表廣告商收集一個ID集區。

## 消費者選擇退出銷售報告

Adobe Advertising會產生客戶針對帳戶選擇退出銷售請求所提交的ID每月報表。 資料會合併使用DSP中建立的CCPA選擇退出銷售區段擷取的請求，以及透過Privacy Service API提交的任何提交。  報告產生於前一個月每個月的第一天。 例如，6月的每月使用者清單可在7月1日取得。

每個報表都可壓縮為GZIP格式，以定位點分隔的文字檔案提供。 在CCPA選擇退出銷售區段中擷取的使用者ID會依區段和廣告商識別。

您可以[從DSP中或使用DSP ](ccpa-opt-out-segment-report-retrieve.md)，擷取前三個月建立的每月報表[!DNL Trafficking API]連結。 每個連結的有效期為七天，但每當客戶嘗試擷取連結時，都會重新整理。

>[!MORELIKETHIS]
>
>* [加州消費者隱私法的Adobe Advertising支援：消費者選擇退出銷售支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [建立並實作[!UICONTROL CCPA Opt-Out-of-Sale]區段](ccpa-opt-out-segment-create.md)
>* [擷取消費者選擇退出銷售報告](ccpa-opt-out-segment-report-retrieve.md)
>* [關於對象管理](audience-about.md)
