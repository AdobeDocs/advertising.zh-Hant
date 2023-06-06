---
title: '"[!DNL Google Ads] 轉換資料」'
description: 瞭解型別 [!DNL Google Ads] — 追蹤的轉換資料可在Search、Social和Commerce中使用。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] 搜尋、社交和商務中的轉換資料

搜尋、社交和商務會自動同步 [!DNL Google Ads] — 追蹤您所有行銷活動的轉換資料，於 [!DNL Google Ads] 搜尋和購物網路至搜尋、社交和商務，以進行報告和最佳化。 搜尋、Social和Commerce同步資料，以便「[!DNL Include in 'Conversions']「選項」已啟用，提取過去30天的資料，然後每天提取資料的變更。

## 可用的轉換資料

每個最多三個交易屬性 [[!DNL Google Ads] — 追蹤的轉換](https://support.google.com/google-ads/answer/4677036) (您設定於 [!DNL Google Ads])會使用中設定的轉換名稱，自動在Search、Social和Commerce中使用 [!DNL Google Ads]. 每次轉換的交易屬性包括：

* `GGL*` — （追蹤時）關鍵字的轉換值總和，以「GGL」首碼開頭（例如GGL Purchase）。

* `GGL_CT*`  — 轉換次數（計數），以「GGL_CT」前置詞（例如GGL_CT_Purchase）開頭。

* `GGL_XD_CT*` — （適用於轉換型別時，追蹤時）跨裝置轉換的數量（計數），由Google測量，以「GGL_XD_CT_」前置詞(例如GGL_XD_CT_Purchase)開頭。

自該帳戶啟用該功能當日起即可取得資料，且每日會在09前更新:00-10:00 （廣告商的時區）。

[!DNL Google Ads] 每次轉換的記錄方式 [競標單位](/help/search-social-commerce/glossary.md#a-b)，裝置，然後按一下日期（不是轉換日期）。 歸因會以中每個量度的預設歸因設定為基礎 [!DNL Google Ads]；由於無法使用點選事件層級的資料，因此不會將Adobe廣告歸因計算在內。 每天，Search、Social和Commerce都會提取前30天的轉換資料，然後使用開始的點按日期計算自前一天以來的任何增量轉換 [!DNL Google Ads] 並將前一天指定為交易日期。 因此，歷史資料可能會隨著每次點按追蹤新轉換而每天變更。 如果您將「搜尋、社交和商務」中的資料與中的 [!DNL Google Ads]，使用檢視或報表選項來檢視&quot;[!UICONTROL Conversions by: Click date]「」（非依交易日期）。

所有量度都會自動用於行銷活動管理檢視和基本報表，也可用於最佳化的投資組合目標。

>[!NOTE]
>
>* 如果您有多個帳戶具有相同的轉換名稱，您可能會在Adobe廣告中看到重複的轉換名稱。 如果發生這種情況， [變更顯示名稱](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 中的其中一個重複量度 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 當兩個不同量度具有相同名稱時，報表並不準確。
>* 競標單位層級的資料符合中的資料 [!DNL Google Ads] 在相同層級。 不過， [!DNL Google Ads]&#39;自己的更高層級的轉換資料可能包括未歸因到子競標單位的其他轉換。 搜尋、社交和商務中的資料一律會從競標單位層級向上彙整，因此（舉例來說），行銷活動層級報表的總數可能與Google Ads中的行銷活動層級報表不同。
>* 資料差異通常在早上同步之後小於當天稍後尚未同步其他轉換時。 我們建議在早上驗證資料。
>* 轉換資料不可用於 [!DNL Google Display Network]， [!DNL Gmail]， [!DNL Mobile App]、和 [!DNL YouTube] 廣告。 當您比較以下專案的資料時，請篩選掉這些型別的廣告： [!DNL Google Ads] 在「搜尋」、「社交」和「商務」中提供資料。
>* 資料 [!DNL Google Ads] 無法在對象或地理位置層級進行轉換，因此不會用於自動最佳化RLSA和位置競標調整。


## 如何比較中的轉換資料 [!DNL Google Ads] 在「搜尋」、「社交」和「商務」中使用資料

使用下列報表設定來驗證可比較的資料。

### 要使用的報表設定 [!DNL Google Ads]

1. 在主工具列中，選取 **[!DNL Reports]>[!DNL Report]**.

1. 選取 **[!DNL + Custom]>[!DNL Table]**.

1. 從左窗格，指定報表中的列和欄：

   1. 搜尋 **[!DNL Day]** 欄位並拖曳至 [!DNL Row] 區段。

   1. 搜尋 **[!DNL All conv].** 欄位並拖曳至 [!DNL Column] 區段。

   1. 搜尋 **[!DNL Conversion action]** 欄位並拖曳至 [!DNL Column] 區段。

1. 在報表設定工具列中，選取 **[!DNL Filter]>[!DNL Ad status]**，然後選取所有方塊。

1. 在報表設定工具列中，選取 **[!DNL Download]>[!DNL Excel .csv]**.

### 用於搜尋、社交和商務的報表設定

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Create Report]**，將游標停留在上方 **[!UICONTROL Basic Reports]**，然後按一下 **[!UICONTROL Search Engine Account Report]**.

1. 在 [!UICONTROL Report Settings] 視窗中，指定下列報表設定：

   1. 在 **[!UICONTROL Conversions Based]** 在區段中，選取 **[!UICONTROL Click date]**.

   1. 指定您用於「 」的相同日期範圍 [!DNL Google Ads] 報告。

   1. 在 **[!UICONTROL Search/Content]** 區段，選取 **[!UICONTROL Search Only]**.

   1. 在 **[!UICONTROL Search Engine Hierarchy]** 區段，展開 [!UICONTROL Google Adwords] 區段並選取帳戶。

   1. 開啟 [!UICONTROL Columns] 標籤，然後新增 [!DNL Google Ads] 要比較的量度（從「GGL」開始）。

1. 按一下 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [關於Search、Social和Commerce中的促銷活動管理](campaign-management-about.md)
>* [實作廣告網路帳戶和行銷活動的概觀](campaign-implemention-overview.md)
>* [監控及管理廣告網路行銷活動的效能](monitor-performance-campaigns.md)

