---
title: '[!UICONTROL Channel Assist Report]'
description: 瞭解 [!UICONTROL Channel Assist Report].
exl-id: 49616327-72e9-49c6-90b9-91c7486e8417
feature: Search Reports, Search Assist Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# 此 [!UICONTROL Channel Assist Report]

*具有搜尋、社交和商務點選追蹤的廣告商，以及具有Adobe Advertising、Adobe Analytics (具有 [!DNL Analytics] 整合)，或使用權杖在摘要中提供(`ef_id`)僅限*

此 [!UICONTROL Channel Assist Report] 指出各種行銷管道(搜尋或來自「搜尋」、「社交」和「商務」的社交，或來自Advertising DSP的顯示或影片)如何協助轉換過程。 報表會顯示導致一或多個轉換的每個事件型別模式，對您的整體轉換有哪些貢獻。 例如，您可以檢視當使用者先看到展示廣告曝光次數，然後按一下搜尋廣告，然後下訂單時發生的轉換次數；或者，您可以檢視當使用者與超過10個廣告互動後發生的轉換次數。 事件型別包括搜尋點按、顯示曝光次數和點按、視訊曝光次數和點按，以及其他曝光次數和其他點按。 <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

報表結果包含轉換路徑中每個事件型別模式的彙總資料（最多N個最早的事件型別），這些事件發生在廣告商的事件型別中 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). 例如，若您選取的路徑大小為五(5)，則報表會包含轉換路徑，其中最多會包含五個最早的事件，而且每個追蹤的事件型別模式會有一列（例如「搜尋點選」，然後「顯示曝光數」）。 每一列會顯示一個事件模式，包括路徑中的第一個事件以及導致轉換的最後一個事件（即使最後一個事件在指定的路徑大小以外亦然）。 依預設，列會依路徑中的事件數量以遞增順序排列。

您可以選擇加入每一列的彙總轉換資料。 在報表中加入轉換/收入欄時，每個轉換型別都會以四欄表示，表示a)轉換總數、b)歸因於事件模式的整體轉換百分比、c)從第一個事件到轉換的日平均延遲，以及d)從最後一個事件到轉換的平均延遲（以天為單位）。 當轉換路徑包含的事件數超過指定的路徑大小時，報表會包含其他列，彙總因事件數較高而產生的轉換資料（例如包含六種事件型別的所有模式）。

您可以檢視前18個月的資料。

## 可用欄

以下是每個報表可用的欄。 預設會自動包含預設欄。 您可以從報表設定的「欄」區段中新增可用的自訂欄。

| 欄 | 預設？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] 至 [!UICONTROL 5th Event] | 預設 | 轉換路徑中發生在廣告商內部的五個最早事件型別 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | 預設 | 轉換路徑中發生在廣告商的事件型別數量 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | 預設 | 轉換路徑中第一個（最早）事件的事件型別。 |
| [!UICONTROL Last Event Type] | 預設 | 導致轉換的最後一個事件的事件型別（即使最後一個事件在指定的路徑大小以外亦然）。 |
| \[廣告商專屬的自訂（衍生）量度\] | 自訂 | 您建立的自訂量度值（從現有量度計算）。 |
| \[廣告商特定交易屬性\] | 自訂 | 指定交易屬性或網站參與量度的轉換次數。 |
| [!UICONTROL % of Total] \[transaction property\] | 自動 | （無法用於報表設定，但會自動包含在所包含每個交易屬性的報表輸出中）歸因於事件模式的跨產品組合整體轉換百分比。 |
| [!UICONTROL 6th Event] 至 [!UICONTROL 30th Event] | 自訂 | 轉換路徑中的第六個到第30個事件型別，這些事件發生在廣告商的 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[transaction property\] | 自動 | （無法用於報表設定，但會自動包含在報表輸出中，以包含每個交易屬性）從第一個事件到轉換的平均延遲（以天為單位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[transaction property\] | 自動 | （無法用於報表設定，但會自動納入報表輸出）從上次事件到轉換的平均延遲天數。 |
| [!UICONTROL Path Frequency] | 自訂 | 此列的路徑在轉換前發生的次數。 |

>[!MORELIKETHIS]
>
>* [關於協助報表](assist-report-about.md)
>* [此 [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [此 [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [協助報表設定](assist-report-settings.md)
>* [產生協助報告](assist-report-generate.md)
