---
title: 可用的 [!DNL Google Analytics] 個量度
description: 參考資料來源可用的 [!DNL Google Analytics] 量度。
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 附錄 — 可用的[!DNL Google Analytics]量度

下列量度，除了上述的排除專案外，在[!DNL Google Analytics]的客戶實作中啟用後即可使用。

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| 類別 | 已排除 | 註解 |
| ---- | ---- | ---- |
| \[全部\] | 資料型別為「百分比」的量度 | 以百分比顯示的量度一律會排除在外。 |
| 使用者 | ga：1dayUsers， ga：7dayUsers， ga：14dayUsers， ga：28dayUsers， ga：sessionsPerUser | — |
| 工作階段 | ga：uniqueDimensionCombinations | — |
| 目標轉換 | — | — |
| 頁面追蹤 | ga：entraces， ga：timeOnPage， ga：exits | — |
| 內部搜尋 | — | 內部搜尋所有量度的易記名稱會以值「InternalSearch：」為前置詞。 |
| 事件追蹤 | — | — |
| 電子商務 | — | — |
| 社互動動 | — | — |
| 例外 | — | — |
| 自訂變數或欄 | ga：calcMetric_* | 計算量度一律會排除。 |

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定a [!DNL Google Analytics] 資料來源的先決條件](data-source-prerequisites.md)
>* [將 [!DNL Google Analytics] 檢視設定為資料來源](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停同步處理資料來源](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
