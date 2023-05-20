---
title: 關於 [!UICONTROL CCPA Opt-out-of-Sale] 段和報告
description: 瞭解如何建立段以跟蹤CCPA選擇退出銷售請求中的ID以及如何檢索ID的報告。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 關於 [!UICONTROL CCPA Opt-out-of-Sale] 段和報告

您可以根據加利福尼亞消費者隱私法(CCPA)，通過 [建立並實施CCPA選擇不可銷售的部門](ccpa-opt-out-segment-create.md)。 用戶無限期地留在CCPA選擇不銷售的部門。

一旦實現段像素標籤，Adobe廣告將開始代表廣告商收集ID池。

## 消費者選擇不可銷售報告

Adobe廣告生成客戶已提交的ID的月度報告，這些ID要求客戶選擇不銷售。 資料整合了使用CCPA選擇退出銷售段捕獲的請求，這些請求是在中建立的，DSP以及通過Privacy ServiceAPI提交的任何資料。  在上個月的每月一日生成報告。 例如，6月的月度用戶清單在7月1日可用。

每個報告都可以作為以制表符分隔的文本檔案壓縮為GZIP格式。 在CCPA選擇退出銷售分段中捕獲的用戶ID由分段和廣告商標識。

你可以 [檢索指向每月報告的連結](ccpa-opt-out-segment-report-retrieve.md) 建立的，可從內部建立，DSP也可使用DSP [!DNL Trafficking API]。 每個連結的有效期為七天，但每次客戶嘗試檢索一個連結時都會刷新。

>[!MORELIKETHIS]
>
>* [Adobe對加利福尼亞消費者隱私法的廣告支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [建立和實施 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [檢索消費者選擇不可銷售報表](ccpa-opt-out-segment-report-retrieve.md)
>* [關於受眾管理](audience-about.md)

