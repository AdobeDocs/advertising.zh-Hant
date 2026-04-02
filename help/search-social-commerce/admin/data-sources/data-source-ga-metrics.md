---
title: 可用的 [!DNL Google Analytics] 個量度
description: 參考資料來源可用的 [!DNL Google Analytics] 量度。
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/hRYeNcQu4uUTCAHXcF9zaZfQm-mw6kDlqvs2AxZhED8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2: id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 0%

---

# 附錄 — 可用的[!DNL Google Analytics]量度

下列量度，除了上述的排除專案外，在[!DNL Google Analytics]的客戶實作中啟用後即可使用。

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| 類別 | 已排除 | 註解 |
| ---- | ---- | ---- |
| \[全部\] | 資料型別為「百分比」的量度 | 以百分比顯示的量度一律會排除在外。 |
| 使用者 | ga:1dayUsers、ga:7dayUsers、ga:14dayUsers、ga:28dayUsers、ga:sessionsPerUser | — |
| 工作階段 | ga:uniqueDimensionCombinations | — |
| 目標轉換 | — | — |
| 頁面追蹤 | ga:entrances， ga:timeOnPage， ga:exits | — |
| 內部搜尋 | — | 內部搜尋所有量度的易記名稱會以值「InternalSearch：」為前置詞。 |
| 事件追蹤 | — | — |
| 電子商務 | — | — |
| 社互動動 | — | — |
| 例外 | — | — |
| 自訂變數或欄 | ga :calcMetric_* | 計算量度一律會排除。 |

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定a [!DNL Google Analytics] 資料來源的先決條件](data-source-prerequisites.md)
>* [將 [!DNL Google Analytics] 檢視設定為資料來源](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停同步處理資料來源](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
