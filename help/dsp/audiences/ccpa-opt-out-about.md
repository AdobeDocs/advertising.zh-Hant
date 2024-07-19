---
title: 關於[!UICONTROL CCPA Opt-out-of-Sale]區段和報表
description: 瞭解如何建立區段來追蹤CCPA選擇退出銷售請求中的ID，以及如何擷取ID報表。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 關於[!UICONTROL CCPA Opt-out-of-Sale]區段和報表

您可以根據《加州消費者隱私法》(CCPA)，透過[建立及實作CCPA選擇退出銷售區段](ccpa-opt-out-segment-create.md)，在您的網站上追蹤消費者選擇退出銷售請求的使用者ID。 使用者會無限期留在CCPA選擇退出銷售區段中。

實施區段畫素標籤後，Adobe Advertising會代表廣告商開始收集ID集區。

## 消費者選擇退出銷售報告

Adobe Advertising會產生客戶針對帳戶選擇退出銷售請求所提交的ID每月報表。 資料會合併使用DSP中建立的CCPA選擇退出銷售區段擷取的請求，以及透過Privacy ServiceAPI提交的任何提交。  報告產生於前一個月每個月的第一天。 例如，6月的每月使用者清單可在7月1日取得。

每個報表都可壓縮為GZIP格式，以定位點分隔的文字檔案提供。 在CCPA選擇退出銷售區段中擷取的使用者ID會依區段和廣告商識別。

您可以[從DSP中或使用DSP [!DNL Trafficking API]，擷取前三個月建立的每月報表](ccpa-opt-out-segment-report-retrieve.md)連結。 每個連結的有效期為七天，但每當客戶嘗試擷取連結時，都會重新整理。

>[!MORELIKETHIS]
>
>* [加州消費者隱私法的Adobe Advertising支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [建立並實作[!UICONTROL CCPA Opt-Out-of-Sale]區段](ccpa-opt-out-segment-create.md)
>* [擷取消費者選擇退出銷售報告](ccpa-opt-out-segment-report-retrieve.md)
>* [關於對象管理](audience-about.md)
