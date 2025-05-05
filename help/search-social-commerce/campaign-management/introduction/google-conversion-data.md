---
title: '[!DNL Google Ads]轉換資料'
description: 瞭解搜尋、社交和Commerce中可用的 [!DNL Google Ads]追蹤轉換資料型別。
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 搜尋、社交和Commerce中的[!DNL Google Ads]轉換資料

搜尋、Social和Commerce會自動將[!DNL Google Ads]搜尋和購物網路上的所有行銷活動的[!DNL Google Ads]追蹤轉換資料同步至Search、Social和Commerce，以利製作報表和進行最佳化。

所有量度都會自動用於行銷活動管理檢視和基本報表，也可用於最佳化的產品組合目標。

## 可用的轉換資料

搜尋、Social和Commerce同步已啟用「[!DNL Include in 'Conversions']」選項的轉換資料，提取過去35天的資料，然後每天以09:00-10:00在廣告商時區提取資料的變更。 歷史資料可能會每天變更，因為每次點按都會追蹤新的轉換。

使用[!DNL Google Ads]中設定的轉換名稱，在Search、Social和Commerce中可自動使用每個[[!DNL Google Ads]追蹤的轉換](https://support.google.com/google-ads/answer/4677036) （您在[!DNL Google Ads]中設定）最多三個量度。 每次轉換的量度包括：

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — （當您追蹤時）關鍵字的轉換值，以「GGL」首碼開頭（例如GGL Purchase）。

* `GGL_CT*` — 轉換次數（計數），以「GGL_CT」首碼開頭（例如GGL_CT_Purchase）。

* `GGL_XD_CT*` — （當轉換型別可使用時，當您追蹤時）跨裝置轉換的數量（計數），由Google測量，以「GGL_XD_CT_」前置詞(例如GGL_XD_CT_Purchase)開頭。

[!DNL Google Ads]會依[競標單位](/help/search-social-commerce/glossary.md#a-b)、裝置和點選日期（非轉換日期）來記錄每次轉換。 歸因是以[!DNL Google Ads]中每個量度的預設歸因設定為基礎；Adobe Advertising歸因未計入中，因為無法使用點選事件層級的資料。

>[!NOTE]
>
>* 如果您有多個帳戶具有相同的轉換名稱，則Adobe Advertising中可能會顯示重複的轉換名稱。 如果發生這種狀況，請在[!UICONTROL Admin] > [!UICONTROL Conversions]中變更其中一個重複量度的顯示名稱[&#128279;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md)。 當兩個不同的量度具有相同的名稱時，報表並不準確。
>* 競標單位層級的資料與相同層級[!DNL Google Ads]中的資料相符。 但是，[!DNL Google Ads]自己的較高層級轉換資料可能包含未歸因至子競標單位的額外轉換。 搜尋、Social和Commerce中的資料一律會從競標單位層級彙總，因此（舉例來說）行銷活動層級報表的總數可能與Google Ads中的行銷活動層級報表不同。
>* 資料差異通常在早上同步後小於當天晚些時候，此時尚未同步其他轉換。 我們建議在早上驗證資料。
>* 轉換資料不適用於[!DNL Google Display Network]、[!DNL Gmail]、[!DNL Mobile App]和[!DNL YouTube]廣告。 當您比較[!DNL Google Ads]中的資料與「搜尋」、「社交」和「Commerce」中的資料時，請篩除這些型別的廣告。
>* [!DNL Google Ads]轉換的資料在對象或地理位置層級無法使用，因此不會用於自動最佳化RLSA和位置競標調整。

## 如何將[!DNL Google Ads]中的轉換資料與「搜尋」、「社交」和「Commerce」中的資料進行比較

如果您將「搜尋」、「社交」和「Commerce」中的資料與[!DNL Google Ads]中的資料進行比較，請使用檢視或報表選項來檢視根據點選日期（而非交易日期）的轉換。

使用下列報表設定驗證可比較的資料。

### 要在[!DNL Google Ads]中使用的報表設定

依日期產生所選轉換動作的報表，並包含所有廣告狀態的資料。

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### 用於搜尋、社交和Commerce的報告設定

在「搜尋」、「社交」和「Commerce」中，使用檢視或報表選項，根據點按日期（而非交易日期）檢視轉換。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Create Report]**，將游標放在&#x200B;**[!UICONTROL Basic Reports]**&#x200B;上，然後按一下&#x200B;**[!UICONTROL Search Engine Account Report]**。

1. 在[!UICONTROL Report Settings]視窗中，指定下列報表設定：

   1. 在&#x200B;**[!UICONTROL Conversions Based]**&#x200B;上區段中，選取&#x200B;**[!UICONTROL Click date]**。

   1. 指定您用於[!DNL Google Ads]報表的相同日期範圍。

   1. 在&#x200B;**[!UICONTROL Search/Content]**&#x200B;區段中，選取&#x200B;**[!UICONTROL Search Only]**。

   1. 在&#x200B;**[!UICONTROL Search Engine Hierarchy]**&#x200B;區段中，展開[!UICONTROL Google Adwords]區段並選取帳戶。

   1. 開啟[!UICONTROL Columns]標籤，然後新增您要比較的[!DNL Google Ads]個量度（以「GGL」開頭）。

1. 按一下&#x200B;**[!UICONTROL Create]**。

>[!MORELIKETHIS]
>
>* [實作廣告網路帳戶和行銷活動的概觀](campaign-implemention-overview.md)
>* [監視和管理廣告網路行銷活動的績效](monitor-performance-campaigns.md)
>* [檢視為廣告商追蹤的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [建立 [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)的轉換標籤
>* [上傳離線轉換資料以進行增強型轉換](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
