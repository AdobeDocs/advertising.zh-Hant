---
title: '[!UICONTROL Campaign Assist Report]'
description: 瞭解[!UICONTROL Campaign Assist Report]。
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# [!UICONTROL Campaign Assist Report]

*廣告商具有搜尋、社交及Commerce點選追蹤，以及來自Adobe Advertising、Adobe Analytics （具有[!DNL Analytics]整合）的轉換追蹤，或僅在摘要中使用權杖(`ef_id`)提供*

[!UICONTROL Campaign Assist Report]指出哪些行銷活動協助了轉換過程。 這些報告會報告其廣告導致一或多次轉換的每種行銷活動模式對整體轉換的貢獻。 例如，您可以檢視當使用者先看到來自促銷活動A的廣告，然後按一下來自促銷活動B的廣告，接著下達訂單時，發生了多少次轉換。 同樣地，您可以檢視使用者與超過10個行銷活動的廣告互動後發生的轉換次數。

報表結果包含轉換路徑中每種行銷活動模式的彙總資料（最多N個最早的行銷活動），適用於在廣告商的[點按回顧期間](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)內發生的事件。 例如，如果您選取的路徑大小為五(5)，則報表會包含轉換路徑，其中最多包含五個最早的行銷活動，而且對於已追蹤事件的行銷活動每個模式，會有一列。 每一列會顯示一個行銷活動模式，包括路徑中的第一個行銷活動，以及導致轉換的最後一個行銷活動（即使最後一個行銷活動超出指定的路徑大小亦然）。 依預設，這些列會依路徑中的行銷活動數量以遞增順序排列。

您可以選擇加入彙總的每列轉換資料，包括您的自訂量度。 當您在報告中包含轉換/收入欄時，每個轉換型別都會以四欄顯示，顯示a)轉換總數、b)歸因於該行銷活動模式的整體轉換百分比、c)從第一個事件（在第一個行銷活動中）到轉換的平均延遲天數，以及d)從最後一個事件（在最後一個行銷活動中）到轉換的平均延遲天數。 當轉換路徑包含的行銷活動多於指定的路徑大小時，則報表會包含其他列，彙總因較高行銷活動數而產生的轉換資料（例如包含六個行銷活動的所有模式）。

您也可以選擇在行銷活動名稱（例如`<campaign name> (Google) click`）之後包含廣告網路及/或事件型別。

您可以檢視前18個月的資料。

>[!TIP]
>
>如果您的品牌關鍵字與一般關鍵字位於不同的促銷活動，則報表會指出您的品牌關鍵字是否對轉換有貢獻。

## 可用欄

以下是每個報表可用的欄。 預設會自動包含預設欄。 您可以從報表設定的「欄」區段中新增可用的自訂欄。

| 欄 | 預設？ | 說明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign]至[!UICONTROL 5th Campaign] | 預設 | 轉換路徑中發生在廣告商的[點按回顧期間](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)內的最早五個行銷活動。<br><br>如果您在實體名稱后面加上任何報告選項，以指出廣告網路、帳戶名稱或事件型別，則該資訊會包含在行銷活動名稱（例如「`"<"campaign name> [Google] [Account1] [impression]`」）後面。 |
| [!UICONTROL Path Size] | 預設 | 轉換路徑中發生在廣告商的[點按回顧期間](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)內的行銷活動數目。 |
| [!UICONTROL First Campaign] | 預設 | 轉換路徑中的第一個行銷活動。 |
| [!UICONTROL Last Campaign] | 預設 | 導致轉換的最後一個行銷活動（即使最後一個關鍵字超出指定的路徑大小）。<br><br>如果您在實體名稱后面加上任何報告選項，以指出廣告網路、帳戶名稱或事件型別，則該資訊會包含在行銷活動名稱（例如「`"<"campaign name> [Google] [Account1] [impression]`」）後面。 |
| \[廣告商專屬的自訂（衍生）量度\] | 自訂 | 您建立的自訂量度值（從現有量度計算）。 |
| \[廣告商專用轉換量度\] | 自訂 | 指定的轉換量度或網站參與量度的轉換次數。 |
| [!UICONTROL % of Total] \[轉換量度\] | 自動 | （無法用於報表設定，但會自動納入每個包含的轉換量度的報表輸出）特定轉換量度（因行銷活動模式而產生）的轉換次數。 |
| [!UICONTROL 6th Campaign]至[!UICONTROL 20th Campaign] | 自訂 | 轉換路徑中在廣告商的[點按回顧期間](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)內發生的第六到第二十個行銷活動。<br><br>如果您在實體名稱后面加上任何報告選項，以指出廣告網路、帳戶名稱或事件型別，則該資訊會包含在行銷活動名稱（例如「`"<"campaign name> [Baidu] [Account1] [click]`」）後面。 |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[轉換量度\] | 自動 | （無法用於報表設定，但會自動包含在每個轉換量度的報表輸出中）從第一個事件（在第一個促銷活動中）到轉換的平均延遲（以天為單位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[轉換量度\] | 自動 | （無法用於報告設定，但會自動包含在報告輸出中）從上次事件（在最後一次行銷活動中）到轉換的平均延遲天數。 |
| [!UICONTROL EF Campaign ID] | 自訂 | 搜尋、Social和Commerce指派給行銷活動的數值ID。 |
| [!UICONTROL EF Portfolio Group ID] | 自訂 | 投資組合所屬投資組合群組的數值ID。 |
| [!UICONTROL EF Search Engine ID] | 自訂 | 搜尋、Social和Commerce指派給廣告網路的數值ID： <i>[!UICONTROL 3]</i>的[!DNL Google Ads]、<i>[!UICONTROL 10]</i>的[!DNL Microsoft Advertising]、<i>[!UICONTROL 45]</i>的[!DNL Meta]、<i>[!UICONTROL 86]</i>的[!DNL Yahoo! Display Network]、<i>[!UICONTROL 87]</i>的[!DNL Naver]、<i>[!UICONTROL 88]</i>的[!DNL Baidu]、<i>[!UICONTROL 90]</i>的[!DNL Yandex]、<i>[!UICONTROL 94]</i>的[!DNL Yahoo! Japan Ads]、<i>[!UICONTROL 105]</i>的[!DNL Yahoo Native] （已棄用），或<i>[!UICONTROL 106]</i>的[!DNL Pinterest] （已棄用）。 |
| [!UICONTROL Portfolio ID] | 數值投資組合ID。 |  |
| [!UICONTROL User SE Account ID] | Search、Social和Commerce指派給廣告網路的數值ID。 |  |

>[!MORELIKETHIS]
>
>* [關於協助報告](assist-report-about.md)
>* [該[!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [該[!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [協助報告設定](assist-report-settings.md)
>* [產生協助報告](assist-report-generate.md)
