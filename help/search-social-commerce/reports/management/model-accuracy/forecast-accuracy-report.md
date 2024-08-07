---
title: '[!UICONTROL Forecast Accuracy Report]'
description: 瞭解預測準確度報表，包括資料欄。
exl-id: f0c42323-eb0d-461a-ab09-440fd1bfc960
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# [!UICONTROL Forecast Accuracy Report]

此報表會依日期顯示指定投資組合的成本和收入模型的準確度。 依預設，它包括每個產品組合的每日預測和實際收入、成本和點按次數，以及預測的準確性。 其中包括目前對應至產品組合之行銷活動的資料。

您可以檢視前18個月的資料。

>[!NOTE]
>
>* 此報告提供與投資組合層級[!UICONTROL Model Accuracy Report]相同的資料，除了您可以跨多個投資組合執行它以及可以變更歸因規則。 您也可以使用自訂引數執行及排程報表，也可以用它建立試算表摘要。
>
>* 最佳實務是檢視過去至少七天的[!UICONTROL Forecast Accuracy Report]，因為無論投資組合的支出策略為何，大部分投資組合都會看到固有的一週中某日趨勢。 最佳化功能會考量此趨勢，並據此分配支出。
>
>* 對於成本預測，過去七天10%的偏差被認為是可接受的，因此預測支出的90%到110%之間的實際支出是正常的。 對於收入預測，過去七天中的15%偏差被認為是可接受的，因此預測支出的85%到115%之間的實際收入是正常的。 應該調查偏差較大的預測。
>
>* 當產品組合中的關鍵字與競標轉換限制相關聯時，產品組合因競標轉換導致的總金額超支或少支。 因此，預測成本欄會隨著支出的增加或減少而偏離目標支出。

## 可用欄

以下是每個報表可用的欄。 預設會自動包含預設欄。 您可以從報告設定的[!UICONTROL Columns]區段新增可用的自訂欄。

| 欄 | 預設？ | 說明 |
|----|----|----|
| [!UICONTROL Portfolio] | 預設 | 投資組合。 |
| [!UICONTROL Day of Week] | 預設 | 報告的星期幾： <i>[!UICONTROL Sunday]</i>、<i>[!UICONTROL Monday]</i>、<i>[!UICONTROL Tuesday]</i>、<i>[!UICONTROL Wednesday]</i>、<i>[!UICONTROL Thursday]</i>、<i>[!UICONTROL Friday]</i>或<i>[!UICONTROL Saturday]</i>。 |
| [!UICONTROL Start Date] | 預設 | 報告的第一天。 |
| [!UICONTROL End Date] | 預設 | 最後報告日期。 |
| [!UICONTROL Predicted Revenue] | 預設 | 投資組合的預測收入。 |
| [!UICONTROL Revenue] | 預設 | 投資組合的實際收入。 |
| [!UICONTROL Revenue Accuracy] | 預設 | 收入預測的準確度，以百分比表示。 |
| [!UICONTROL Predicted Cost] | 預設 | 投資組合的預測成本。 |
| [!UICONTROL Cost] | 預設 | 投資組合的實際成本。 |
| [!UICONTROL Cost Accuracy] | 預設 | 成本預測的準確度，以百分比表示。 |
| [!UICONTROL Predicted Clicks] | 預設 | 專案組合預測的點按次數。 |
| [!UICONTROL Clicks] | 預設 | 投資組合的實際點按次數。 |
| [!UICONTROL Click Accuracy] | 預設 | 點按預測的準確度，以百分比表示。 |
| [!UICONTROL EF Portfolio Group ID] | 預設 | 投資組合所屬投資組合群組的數值ID。 |
| [!UICONTROL Portfolio Group Name] | 預設 | 投資組合所屬投資組合群組的名稱。 |
| [!UICONTROL Portfolio ID] | 預設 | 數值投資組合ID。 |

>[!MORELIKETHIS]
>
>* [關於模型準確度報告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [該[!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [產生模型正確性報告](model-accuracy-report-generate.md)
>* [模型正確性報表設定](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
