---
title: '[!UICONTROL Keyword Assist Report]'
description: 瞭解 [!UICONTROL Keyword Assist Report].
exl-id: 07de2880-111b-498f-9f7f-ec15f89230ae
feature: Search Reports, Search Assist Reports
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# 此 [!UICONTROL Keyword Assist Report]

*具有搜尋、社交和商務點選追蹤的廣告商，以及具有Adobe Advertising、Adobe Analytics (具有 [!DNL Analytics] 整合)，或使用權杖在摘要中提供(`ef_id`)僅限*

此 [!UICONTROL Keyword Assist Report] 指出哪些關鍵字或位置可驅動點按。 報表會顯示轉換路徑中收到點按的付費搜尋關鍵字或版位的每個模式，並指出該模式對整體轉換的貢獻。 例如，您可以檢視當使用者第一次按下關鍵字搜尋「皮鞋」產生的廣告，然後在關鍵字搜尋「山羊皮鞋」後按一下廣告，然後下達訂單時，發生的轉換次數；或者，您可以檢視使用者按下關鍵字超過10個產生的廣告後發生的轉換次數。

報表結果包含最多N個最早付費搜尋關鍵字的彙總資料，或是發生在廣告商點按回顧和曝光回顧期間之轉換路徑中的位置點按。 例如，如果您選取的路徑大小為五(5)，則報表會包含轉換路徑，其中最多包含五個最早收到點按的關鍵字或位置，而且會針對每個追蹤的點按模式列出一列。 每一列都包含路徑中的第一個關鍵字或位置以及導致轉換的最後一個關鍵字或位置（即使最後一個關鍵字在指定的路徑大小之外）。 依預設，列會依路徑中的事件數量以遞增順序排列。

>[!NOTE]
>
>如果報表包含啟用內容搜尋行銷活動的版位（不包含關鍵字），則 [!UICONTROL Keyword] 欄會顯示適用的廣告群組名稱，例如「（廣告群組內容）您的廣告群組名稱」。

您可以選擇加入每一列的彙總轉換資料。 當您在報表中包含轉換/收入欄時，每個轉換型別都會以四欄表示，顯示a)轉換總數、b)歸因於該關鍵字模式的整體轉換百分比、c)從第一個事件（在第一個關鍵字）到轉換的平均延遲天數，以及d)從最後一個事件（在最後一個關鍵字）到轉換的平均延遲天數。 當轉換路徑包含的關鍵字超過指定的路徑大小時，報表會包含其他列，彙總因較高關鍵字數而產生的轉換資料（例如包含點按六個關鍵字的所有模式）。

您可以檢視前18個月的資料。

## 可用欄

以下是每個報表可用的欄。 預設會自動包含預設欄。 您可以從報表設定的「欄」區段中新增可用的自訂欄。

| 欄 | 預設？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] 至 [!UICONTROL 5th Keyword] | 預設 | 在廣告商發生的轉換路徑中，最早的五個付費搜尋關鍵字或位置點按 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).<br><br><b>注意：</b> 如果報表包含已啟用內容搜尋行銷活動的版位（其中不包含關鍵字），則這些欄會顯示適用的廣告群組名稱，例如「（廣告群組內容）您的廣告群組名稱」。 |
| [!UICONTROL Path Size] | 預設 | 轉換路徑中發生在廣告商內的關鍵字和/或位置數量 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | 預設 | 轉換路徑中的第一個關鍵字或位置。 |
| [!UICONTROL Last Keyword] | 預設 | 導致轉換的最後一個關鍵字或位置（即使最後一個關鍵字超出指定的路徑大小）。 |
| \[廣告商專屬的自訂（衍生）量度\] | 自訂 | 您建立的自訂量度值（從現有量度計算）。 |
| \[廣告商專用轉換量度\] | 自訂 | 指定的轉換量度或網站參與量度的轉換次數。 |
| [!UICONTROL % of Total] \[轉換量度\] | 自動 | （無法用於報表設定，但會自動包含在每個包含的轉換量度的報表輸出中）歸因於關鍵字和/或位置模式的跨產品組合整體轉換百分比。 |
| [!UICONTROL 6th Keyword] 至 [!UICONTROL 10th Keyword] | 自訂 | 在廣告商發生的轉換路徑中的第六到第十個付費搜尋關鍵字或位置點按 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).<br><br><b>注意：</b> 如果報表包含已啟用內容搜尋行銷活動的版位（其中不包含關鍵字），則這些欄會顯示適用的廣告群組名稱，例如「（廣告群組內容）您的廣告群組名稱」。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[轉換量度\] | 自動 | （無法用於報表設定，但會自動包含在每個轉換量度的報表輸出中）從第一個事件（位於第一個關鍵字或位置）到轉換的平均延遲（以天為單位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[轉換量度\] | 自動 | （無法用於報表設定，但會自動包含在報表輸出中）從上一個事件（在最後一個關鍵字或位置）到轉換的平均延遲天數（以天為單位）。 |
| [!UICONTROL Path Frequency] | 自訂 | 此列的路徑在轉換前發生的次數。 |

>[!MORELIKETHIS]
>
>* [關於協助報表](assist-report-about.md)
>* [此 [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [此 [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [協助報表設定](assist-report-settings.md)
>* [產生協助報告](assist-report-generate.md)
