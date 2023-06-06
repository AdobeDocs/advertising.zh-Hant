---
title: "[!UICONTROL Keyword Assist Report]"
description: 瞭解 [!UICONTROL Keyword Assist Report].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# 此 [!UICONTROL Keyword Assist Report]

*廣告商具有搜尋、社交和商務點選追蹤，以及來自Adobe廣告的轉換追蹤，Adobe Analytics (具有 [!DNL Analytics] 整合)，或使用權杖在摘要中提供(`ef_id`)僅限*

此 [!UICONTROL Keyword Assist Report] 指出哪些關鍵字或位置會推動點按。 報表會顯示轉換路徑中收到點按的付費搜尋關鍵字或位置的每個模式，並指出該模式對整體轉換的貢獻。 例如，您可以檢視當使用者第一次點選因關鍵字搜尋「皮鞋」而產生的廣告，然後在關鍵字搜尋「山羊皮鞋」後按一下廣告，然後下達訂單時，發生了多少轉換；或者您可以檢視在使用者點選因超過10個關鍵字產生的廣告後發生了多少轉換。

報表結果包含轉換路徑中，在廣告商的點選回顧和曝光回顧期間發生的最多N個最早付費搜尋關鍵字或位置點選的彙總資料。 例如，如果您選取的路徑大小為五(5)，則報表會包含轉換路徑，這些路徑最多包含五個最早收到點按的關鍵字或位置，而且會針對每個追蹤的點按模式包含一個資料列。 每一列包含路徑中的第一個關鍵字或位置，以及導致轉換的最後一個關鍵字或位置（即使最後一個關鍵字在指定的路徑大小之外）。 依預設，列會依路徑中的事件數量以遞增順序排列。

>[!NOTE]
>
>如果報表包含啟用內容搜尋行銷活動的版位（不包含關鍵字），則 [!UICONTROL Keyword] 欄會顯示適用的廣告群組名稱，例如「（廣告群組內容）您的廣告群組名稱」。

您可以選擇性地包含每一列的彙總轉換資料。 在報表中包含轉換/收入欄時，每個轉換型別都會以四欄表示，顯示a)轉換總數、b)歸因於該關鍵字模式的整體轉換百分比、c)從第一個事件（在第一個關鍵字）到轉換的平均延遲天數，以及d)從最後一個事件（在最後一個關鍵字）到轉換的平均延遲天數。 當轉換路徑包含的關鍵字超過指定的路徑大小時，報表會包含其他列，彙總因關鍵字數目較多而產生的轉換資料（例如包含對六個關鍵字點選的所有模式）。

您可以檢視過去18個月的資料。

## 可用欄

以下是每個報表可用的欄。 預設會自動包含預設欄。 您可以從報表設定的「欄」區段中新增可用的自訂欄。

| 欄 | 預設？ | 說明 |
|----|----|
| [!UICONTROL 1st Keyword] 至 [!UICONTROL 5th Keyword] | 預設 | 轉換路徑中最早發生在廣告商的五個付費搜尋關鍵字或位置點按 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).<br><br><b>注意：</b> 如果報表包含啟用內容搜尋行銷活動的版位（不包含關鍵字），則這些欄會顯示適用的廣告群組名稱，例如「（廣告群組內容）您的廣告群組名稱」。 |
| [!UICONTROL Path Size] | 預設 | 轉換路徑中發生在廣告商內的關鍵字和/或版位數目 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | 預設 | 轉換路徑中的第一個關鍵字或位置。 |
| [!UICONTROL Last Keyword] | 預設 | 導致轉換的最後一個關鍵字或位置（即使最後一個關鍵字超出指定的路徑大小）。 |
| \[廣告商專屬的自訂（衍生）量度\] | 自訂 | 您建立的自訂量度值（從現有量度計算）。 |
| \[廣告商特定交易屬性\] | 自訂 | 指定交易屬性或網站參與量度的轉換次數。 |
| [!UICONTROL % of Total] \[transaction property\] | 自動 | （在報表設定中無法使用，但自動包含在所包含每個交易屬性的報表輸出中）歸因於關鍵字和/或位置模式的整個投資組合中的轉換百分比。 |
| [!UICONTROL 6th Keyword] 至 [!UICONTROL 10th Keyword] | 自訂 | 轉換路徑中的第六到第十個付費搜尋關鍵字或位置點按(發生在廣告商的 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).<br><br><b>注意：</b> 如果報表包含啟用內容搜尋行銷活動的版位（不包含關鍵字），則這些欄會顯示適用的廣告群組名稱，例如「（廣告群組內容）您的廣告群組名稱」。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[transaction property\] | 自動 | （在報告設定中無法使用，但自動包含在所包含每個交易屬性的報告輸出中）從第一個事件（在第一個關鍵字或位置）到轉換的平均延遲（以天為單位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[transaction property\] | 自動 | （在報告設定中無法使用，但自動包含在報告輸出中）從上一個事件（在最後一個關鍵字或位置）到轉換的平均延遲（以天為單位）。 |
| [!UICONTROL Path Frequency] | 自訂 | 此列的路徑在轉換前發生的次數。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [關於協助報告](assist-report-about.md)
>* [此 [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [此 [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [協助報表設定](assist-report-settings.md)
>* [產生協助報告](assist-report-generate.md)

