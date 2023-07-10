---
title: '''[!DNL Microsoft Advertising] 轉換資料'
description: 瞭解型別 [!DNL Microsoft Advertising] — 追蹤的轉換資料可在Search、Social和Commerce中使用。
source-git-commit: 355796d65e5de0dba9111e77fc594a3e50e6ec5e
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 搜尋、社交和商務中的轉換資料

搜尋、Social和Commerce會自動同步您追蹤的所有轉換， [Microsoft Advertising通用事件追蹤(UET)標籤](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) 用於網站轉換（包括瀏覽轉換），用於報告和最佳化。

所有量度都會自動用於行銷活動管理檢視和基本報表，也可用於最佳化Microsoft Advertising行銷活動的產品組合目標。

## 可用的轉換資料

搜尋、Social和Commerce同步資料，以便「[!DNL Include in 'Conversions']「選項」已啟用，提取過去35天的資料，然後在09前每天提取資料的變更:00-10:00 （廣告商的時區）。 歷史資料可能會隨著每次點按追蹤新轉換而每天變更。

兩個交易屬性，分別對應於 [[!DNL Microsoft Advertising] — 追蹤的轉換](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (您設定於 [!DNL Microsoft Advertising])會使用中設定的轉換名稱，自動在Search、Social和Commerce中使用 [!DNL Microsoft Advertising]. 每次轉換的交易屬性包括：

* `<conversion-name>`  — 關鍵字的轉換值（例如Purchase）。

  >[!TIP]
  >
  >在投資組合的目標中使用此型別的屬性，投資組合包括 [!DNL Microsoft Advertising] 具有最大轉換值和目標ROAS競標策略的行銷活動。

* `CT_<conversion-name>`  — 轉換次數（計數），以「CT_」首碼開頭（例如CT_Purchase）。

  >[!TIP]
  >
  >在投資組合的目標中使用此型別的屬性，投資組合包括 [!DNL Microsoft Advertising] 具有最大轉換數和目標CPA競標策略的行銷活動。

可用資料是根據點按時間，以及自帳戶啟用功能之日以來的轉換/交易時間。

<!-- verify below/ if equivalent

[!DNL Microsoft Advertising] records each conversion by [bid unit](/help/search-social-commerce/glossary.md#a-b), device, and click date (not conversion date). Attribution is based on the default attribution setting for each metric in [!DNL Microsoft Advertising]; Adobe Advertising attribution isn't factored in because click event-level data isn't available.
-->

>[!NOTE]
>
>* 如果您有多個帳戶具有相同的轉換名稱，您可能會在Adobe Advertising中看到重複的轉換名稱。 如果發生這種情況， [變更顯示名稱](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 中的其中一個重複量度 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 當兩個不同量度具有相同名稱時，報表並不準確。
>* 競標單位層級的資料符合相同層級廣告網路中的資料。 不過，廣告網路本身的更高層級轉換資料可能包含未歸因至子競標單位的額外轉換。 搜尋、社交和商務中的資料一律會從競標單位層級向上彙整，因此（舉例來說），行銷活動層級報表的總數可能與廣告網路中的行銷活動層級報表不同。
>* 資料差異通常在早上同步之後小於當天稍後尚未同步其他轉換時。 我們建議在早上驗證資料。
>* 對象或地理位置層級的資料無法使用，因此不會用於自動最佳化RLSA和位置競標調整。

## 如何比較中的轉換資料 [!DNL Microsoft Advertising] 在「搜尋」、「社交」和「商務」中使用資料

使用下列報表設定來驗證可比較的資料。

### 要使用的報表設定 [!DNL Microsoft Advertising]

依日期產生所選轉換動作的報表，並包含所有廣告狀態的資料。

### 用於搜尋、社交和商務的報表設定

在「搜尋、Social和商務」中，使用檢視或報表選項來根據點按日期（而非交易日期）檢視轉換。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Create Report]**，將游標停留在上方 **[!UICONTROL Basic Reports]**，然後按一下 **[!UICONTROL Search Engine Account Report]**.

1. 在 [!UICONTROL Report Settings] 視窗中，指定下列報表設定：

   1. 在 **[!UICONTROL Conversions Based]** 在區段中，選取 **[!UICONTROL Click date]**.

   1. 指定您用於「 」的相同日期範圍 [!DNL Microsoft Advertising] 報告。

   1. 在 **[!UICONTROL Search/Content]** 區段，選取 **[!UICONTROL Search Only]**.

   1. 在 **[!UICONTROL Search Engine Hierarchy]** 區段，展開 [!UICONTROL Microsoft Advertising] 區段並選取帳戶。

   1. 開啟 [!UICONTROL Columns] 標籤，然後新增 [!DNL Microsoft Advertising] 您要比較的量度。

1. 按一下 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [實作廣告網路帳戶和行銷活動的概觀](campaign-implemention-overview.md)
>* [監控及管理廣告網路行銷活動的效能](monitor-performance-campaigns.md)
>* [檢視為廣告商追蹤的交易屬性](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.html?lang=en)
