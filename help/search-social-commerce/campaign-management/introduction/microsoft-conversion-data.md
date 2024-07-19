---
title: '[!DNL Microsoft Advertising]轉換資料'
description: 瞭解搜尋、社交和Commerce中可用的 [!DNL Microsoft Advertising]追蹤轉換資料型別。
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 搜尋、社交和Commerce中的[!DNL Microsoft Advertising]轉換資料

搜尋、Social和Commerce會自動同步您[[!DNL Microsoft Advertising] 通用事件追蹤(UET)標籤](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking)所追蹤的所有網站轉換次數，包括瀏覽轉換，以便報告和最佳化。

所有量度都會自動用於行銷活動管理檢視和基本報告，也可用於產品組合目標以最佳化[!DNL Microsoft Advertising]個行銷活動。

## 可用的轉換資料

搜尋、Social和Commerce同步已啟用「[!DNL Include in 'Conversions']」選項的轉換資料，提取過去35天的資料，然後每天以09:00-10:00在廣告商時區提取資料的變更。 歷史資料可能會每天變更，因為每次點按都會追蹤新的轉換。

每個追蹤[[!DNL Microsoft Advertising]的轉換](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) （您在[!DNL Microsoft Advertising]中設定）有兩個量度，可在Search、Social和Commerce中使用[!DNL Microsoft Advertising]中設定的轉換名稱自動使用。 每次轉換的量度包括：

* `<conversion-name>` — 關鍵字的轉換值（例如Purchase）。

  >[!TIP]
  >
  >在投資組合的目標中使用此型別的轉換量度，投資組合包含具有最大轉換值和目標ROAS競標策略的[!DNL Microsoft Advertising]行銷活動。

* `CT_<conversion-name>` — 轉換次數（計數），以「CT_」首碼開頭（例如CT_Purchase）。

  >[!TIP]
  >
  >在包含[!DNL Microsoft Advertising]個行銷活動且具有最大轉換數和目標CPA競標策略的產品組合的目標中，使用此型別的轉換量度。

根據點按時間和從帳戶啟用功能之日開始的轉換/交易時間，可使用資料。

[!DNL Microsoft Advertising]會依[競標單位](/help/search-social-commerce/glossary.md#a-b)、裝置和點選日期（非轉換日期）來記錄每次轉換。 歸因是以[!DNL Microsoft Advertising]中每個量度的預設歸因設定為基礎；Adobe Advertising歸因未計入中，因為無法使用點選事件層級的資料。

>[!NOTE]
>
>* 如果您有多個帳戶具有相同的轉換名稱，您可能會在Adobe Advertising中看到重複的轉換名稱。 如果發生這種狀況，請在[!UICONTROL Admin] > [!UICONTROL Conversions]中變更其中一個重複量度的顯示名稱](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md)。 [當兩個不同的量度具有相同的名稱時，報表並不準確。
>* 競標單位層級的資料符合相同層級廣告網路中的資料。 不過，廣告網路自己的更高層級轉換資料可能包含未歸因至子競標單位的額外轉換。 搜尋、Social和Commerce中的資料一律會從競標單位層級彙總，因此（舉例來說）行銷活動層級報表的總數可能與廣告網路中的行銷活動層級報表不同。
>* 資料差異通常在早上同步後小於當天晚些時候，此時尚未同步其他轉換。 我們建議在早上驗證資料。
>* 對象或地理位置層級沒有資料，因此不會用來自動最佳化RLSA和位置競標調整。

## 如何將[!DNL Microsoft Advertising]中的轉換資料與「搜尋」、「社交」和「Commerce」中的資料進行比較

使用下列報表設定驗證可比較的資料。

### 要在[!DNL Microsoft Advertising]中使用的報表設定

依日期產生所選轉換動作的報表，並包含所有廣告狀態的資料。

### 用於搜尋、社交和Commerce的報告設定

在「搜尋」、「社交」和「Commerce」中，使用檢視或報表選項，根據點按日期（而非交易日期）檢視轉換。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Create Report]**，將游標放在&#x200B;**[!UICONTROL Basic Reports]**&#x200B;上，然後按一下&#x200B;**[!UICONTROL Search Engine Account Report]**。

1. 在[!UICONTROL Report Settings]視窗中，指定下列報表設定：

   1. 在&#x200B;**[!UICONTROL Conversions Based]**&#x200B;上區段中，選取&#x200B;**[!UICONTROL Click date]**。

   1. 指定您用於[!DNL Microsoft Advertising]報表的相同日期範圍。

   1. 在&#x200B;**[!UICONTROL Search/Content]**&#x200B;區段中，選取&#x200B;**[!UICONTROL Search Only]**。

   1. 在&#x200B;**[!UICONTROL Search Engine Hierarchy]**&#x200B;區段中，展開[!UICONTROL Microsoft Advertising]區段並選取帳戶。

   1. 開啟「[!UICONTROL Columns]」標籤，然後新增您要比較的[!DNL Microsoft Advertising]個量度。

1. 按一下&#x200B;**[!UICONTROL Create]**。

>[!MORELIKETHIS]
>
>* [實作廣告網路帳戶和行銷活動的概觀](campaign-implemention-overview.md)
>* [監視和管理廣告網路行銷活動的績效](monitor-performance-campaigns.md)
>* [檢視為廣告商追蹤的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
