---
title: 『[!UICONTROL Forecast Accuracy (Actuals) Report]『
description: 瞭解 [!UICONTROL Forecast Accuracy (Actuals) Report]，包括資料欄。
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 此 [!UICONTROL Forecast Accuracy (Actuals) Report]

此報表依日期顯示每個產品組合的實際曝光數、點選數、成本和收入資料。

## 可用欄

以下是自動包含在每個報表中的欄。 您無法新增其他欄。

| 欄 | 預設？ | 說明 |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | 預設 | 投資組合所屬投資組合群組的名稱。 |
| [!UICONTROL Portfolio ID] | 預設 | 數值投資組合ID。 |
| [!UICONTROL EF Portfolio Group ID] | 預設 | 投資組合所屬投資組合群組的數值ID。 |
| [!UICONTROL Portfolio] | 預設 | 投資組合。 |
| [!UICONTROL Portfolio Status] | 預設 | 投資組合狀態：<ul><li><i>[!UICONTROL Optimize]：</i> 最佳化功能會收集相關行銷活動的點選和收入資料、模型化資料以最佳化出價，以及最佳化出價和/或行銷活動預算（取決於最佳化型別和行銷活動競標策略）。</li><li><i>[!UICONTROL Active]：</i> 最佳化功能會收集相關行銷活動的點選和收入資料，並將資料模型化，但不會最佳化競標或行銷活動預算。</li><li><i>[!UICONTROL Inactive]：</i> 最佳化功能會收集相關行銷活動的點選資料以用於報表用途，但不會模型化資料，也不會最佳化競標或行銷活動預算。 |
| [!UICONTROL Day of Week] | 預設 | 報告的一週中的某天： <i>[!UICONTROL Sunday]</i>， <i>[!UICONTROL Monday]</i>， <i>[!UICONTROL Tuesday]</i>， <i>[!UICONTROL Wednesday]</i>， <i>[!UICONTROL Thursday]</i>， <i>[!UICONTROL Friday]</i>，或 <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | 預設 | 報告的日期。 |
| [!UICONTROL Device] | 預設 | (Google Ads、Microsoft Advertising、Yahoo！ Display Network， Yahoo！ Japan Ads和Yahoo Native行銷活動)顯示廣告的裝置型別： <i>[!UICONTROL Computers]</i>， <i>[!UICONTROL Mobile]</i>， <i>[!UICONTROL Tablets]</i>， <i>[!UICONTROL Other]</i>，或 <i>[!UICONTROL N/A]</i> （沒有值）。 其他廣告網路的列具有值 <i>[!UICONTROL N/A]</i>.<br><br>在搜尋行銷活動中，如果關鍵字、廣告和/或廣告擴充功能的追蹤範本或目的地URL包含依裝置追蹤資料的引數(<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>)時，轉換資料也會包含在每種裝置型別的列中。 否則，如果轉換資料無法歸因於裝置型別，則會彙總在具有「」的單獨列中[!UICONTROL Device]的「 」值 <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | 預設 | 總收入。 |
| [!UICONTROL Impressions] | 預設 | 曝光總數。 |
| [!UICONTROL Clicks] | 預設 | 點按總數。 |
| [!UICONTROL Cost] | 預設 | 總成本。 |

>[!MORELIKETHIS]
>
>* [關於模型精度報表](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [此 [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [產生模型準確度報告](model-accuracy-report-generate.md)
>* [模型精度報表設定](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
