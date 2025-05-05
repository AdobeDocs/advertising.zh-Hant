---
title: 自訂報表設定
description: 請參閱自訂報表設定的說明。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '1541'
ht-degree: 0%

---

# 自訂報表設定

**[!UICONTROL Name]：**&#x200B;報告名稱。 長度上限為180個字元。

**[!UICONTROL Report Type]：**&#x200B;報告的型別： *[!UICONTROL Custom]* （包含最可用的選項）、*[!UICONTROL Billing]*、*[!UICONTROL Conversion]*、*[!UICONTROL Device]*、*[!UICONTROL Frequency (by Impression)]*、*[!UICONTROL Frequency (by App/Site)]*、*[!UICONTROL Geo]*、*[!UICONTROL Margin]*、*[!UICONTROL Media Performance]*、*[!UICONTROL Segment]*、*[!UICONTROL Site]*、*[!UICONTROL Household Reach & Frequency]*、*[!UICONTROL Household Conversions]*、*[!UICONTROL Path to Conversions Beta]*、*[!UICONTROL Path Length Beta]*&#x200B;或&#x200B;*[!UICONTROL Time to Conversion Beta]*。

## [!UICONTROL Report Range]節

此區段會決定報表中包含的資料。 若要設定報告排程的日期，請參閱&quot;[!UICONTROL Report run schedule]&quot;區段。

**[!UICONTROL Timezone]：**&#x200B;報告的時區。

**[!UICONTROL Observe Daylight Savings Time]：**&#x200B;會考量報告時間中的日光節約時間。

**範圍：**&#x200B;要產生資料的日期範圍。 可用天數因報表和所選維度而異。 選擇一項：

* **[!UICONTROL Previous Calendar Week]：**&#x200B;包含前一個日曆週的資料。

* **[!UICONTROL Previous Calendar Month]：**&#x200B;包含前一個日曆月的資料。

* **[!UICONTROL Custom Range]：**&#x200B;包含特定開始和結束日期之間的資料。 若要報告前一天的資料，請選取&#x200B;**[!UICONTROL Present]**。

## [!UICONTROL Report Run schedule]節

此區段決定執行報告的日期。 若要設定包含報表資料的日期，請參閱&quot;[!UICONTROL Report range]&quot;區段。

**\[排程\]：**&#x200B;何時產生報表：

* *[!UICONTROL Immediately]*：立即將報表新增至報表佇列。

  >[!NOTE]
  >
  >您也可以[隨時從[!UICONTROL Reports]檢視](report-run-now.md)執行自訂報告。

* *[!UICONTROL On]\&lt;Date\>：*&#x200B;在帳戶時區的指定完成日期以09:00執行報表。

* *[!UICONTROL Recurring]：*&#x200B;在指定的時間期間根據排程執行報告。

   * **\[排程\]：**&#x200B;執行報告的頻率：

      * *每日*，每N天執行一次報表。 例如，若要每兩週（14天）執行一次報表，請選取此選項並輸入&#x200B;**14**。

      * *每週*，在一週中的指定日期執行報告。 例如，若要每週一和週五執行報表，請選取此選項，然後選取&#x200B;**週一**&#x200B;和&#x200B;**週五**&#x200B;旁的核取方塊。

      * *每月*，針對該月特定數值日（從1到30）執行報表。 例如，在每個月的第一天執行報告，選取此選項並輸入&#x200B;**1**。

   * **從**：報表可以執行的第一個日期。 根據指定的排程，第一個報表例項可能會發生在此日期之後。

   * **直到**：報告到期日，最多可隔四個行事曆月。 在報告到期之前，所有指定的電子郵件目的地都會在到期日七天零一天前收到電子郵件警示。 若要保留更長的報表，請變更此日期。

## [!UICONTROL Apply Filters]節

**[!UICONTROL Filter by]：** （選用）篩選資料所依據的其他維度，無論維度是否包含在報表中作為欄。 可用的篩選器依報告型別而異，可能包括： *[!UICONTROL Account]*\*、*[!UICONTROL Ad Type]*、*[!UICONTROL Ads]*、*[!UICONTROL Advertiser]*、*[!UICONTROL Campaign]*、*[!UICONTROL Country]*、* *[!UICONTROL Package]*、*[!UICONTROL Placement]*、*[!UICONTROL Video]*&#x200B;和&#x200B;*[!UICONTROL Video Duration]*。

若要套用一或多個篩選器，請執行下列動作：

* 選取維度、選取運運算元（*等於*&#x200B;或&#x200B;*不等於*），然後選取適用的值。 例如，若要只傳回前段廣告的資料，請指定&quot;[!UICONTROL Ad Type equals Preroll]&quot;。
* （選用）將其他條件新增至篩選器。
* （選用）新增其他篩選器，每個篩選器一或多個條件。

\* *[!UICONTROL Account]*&#x200B;只有在您的組織已設定為[跨帳戶報告](report-about.md#cross-account-reporting)時，才可用於下列報告型別： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]以及[!UICONTROL Conversion]。 如需跨帳戶報告的詳細資訊，請連絡您的Adobe客戶團隊。

**[!UICONTROL Include data from Adobe Advertising SSC]：** （僅轉換路徑、路徑長度和轉換時間報表）包含指定Advertising Search、Social和Commerce行銷活動之搜尋廣告點選資料。 選取此選項時：

1. 使用&#x200B;**篩選依據[!UICONTROL SSC Account]**&#x200B;篩選器選取搜尋、社交和Commerce帳戶。

1. 使用&#x200B;**篩選依據[!UICONTROL SSC Campaign]**&#x200B;篩選器選取行銷活動。

   若要選取多個行銷活動，請按一下第二個和後續行銷活動的&#x200B;**[!UICONTROL Add Criteria]**。

## [!UICONTROL Build Your Report]節

**[!UICONTROL Select To Add As Report Headers]：**&#x200B;要包含在報告中的資料欄或標題。 若要新增欄，請展開類別並選取欄名稱旁的核取方塊。 可用的欄會依報告而有所不同，並且所有無法使用的量度都會停用。 可用的資料類別可能包括：

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > [!UICONTROL Household Reach & Frequency]和[!UICONTROL Path to Conversion]報表只能包含一個維度。
  > [!UICONTROL Path Length]和[!UICONTROL Time to Conversion]報表不包含維度。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >[!UICONTROL Household Reach & Frequency]報表可包含重疊量度或非重疊量度，但不能同時包含兩者。

* [!UICONTROL Conversion Metrics] （依廣告商排序）

* [!UICONTROL Custom Goals] （依廣告商排序）

如需所有選項的說明，請參閱[可用的報表欄](report-columns.md)。

**[!UICONTROL Drag to Re-Order Report Headers Below]：**&#x200B;資料行標頭的順序。 您可以拖放任何欄以自訂順序。

**[!UICONTROL Format]：**&#x200B;是以&#x200B;*[!UICONTROL CSV]* （逗號分隔值）還是&#x200B;*[!UICONTROL Tab]* （定位鍵分隔值）格式產生報表。

**[!UICONTROL Headers]：**&#x200B;是&#x200B;*[!UICONTROL Include]*&#x200B;或&#x200B;*[!UICONTROL Do Not Include]*&#x200B;欄標題。

## [!UICONTROL Multi-Touch Conversion Options]節

**[!UICONTROL Attribution Rule Settings]：**&#x200B;設定會因報告型別而異：

* **\[歸因型別\]：** ([!UICONTROL Household Conversion]個具有[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]欄的報告；僅具有Adobe Advertising轉換追蹤的廣告商)在報告內，如何將轉換資料歸因到導致轉換的一系列事件中：

   * *[!UICONTROL Unique]：* （預設值）計算維度值（例如裝置或位置）在轉換路徑上的次數。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]：*&#x200B;根據維度值（例如裝置或位置）在轉換路徑上的發生頻率，分配每個轉換的評分。 例如，如果在轉換前共有10次曝光，其中8次在CTV上，2次在行動裝置上，則80%的評分(0.8)會給予予CTV熒幕，而0.2次給予行動裝置。

* **\[規則型別\]：** (所有具有[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]欄的[!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment]和[!UICONTROL Site]報告；僅具有Adobe Advertising轉換追蹤的廣告商)在報告中，如何在一連串導致轉換的事件中歸因轉換資料。 如果要比較規則之間的差異，您可以選擇多個規則。

  >[!NOTE]
  >
  >轉換路徑包含廣告商曝光或點按回顧期間內的任何曝光次數和點按，這些設定在[!DNL Advertising Search, Social, & Commerce]。 在轉換歸因期間，點按次數會優先於曝光數。 根據歸因規則，轉換路徑中的任何點按都會獲得完整評價。 只有轉換路徑中未追蹤任何點按時，曝光次數才會獲得評分。

   * *[!UICONTROL Last Event]：*&#x200B;轉換路徑中上次點按或曝光的屬性轉換。

   * *[!UICONTROL Weight Last More]：*&#x200B;屬性會轉換至轉換路徑中的所有事件，但會給予最後一個事件最大的權重，並依序給予前一個事件較小的權重。

   * *[!UICONTROL Even Distribution]：*&#x200B;屬性轉換與轉換路徑中的每個事件相同。

   * *[!UICONTROL Weight First More]：*&#x200B;屬性轉換至轉換路徑中的所有事件，但給予第一個事件最大的權重，並連續給予下列事件較小的權重。

   * *[!UICONTROL First Event]：*&#x200B;屬性轉換至轉換路徑中的第一次點按或印象。

   * *[!UICONTROL U-shaped]：*&#x200B;將轉換歸因於轉換路徑中的所有事件，但給予第一個和最後一個事件的權重最大，而連續減少轉換路徑中間事件的權重。

   * *[!UICONTROL Display Only]：*&#x200B;轉換路徑中最後一次DSP點按或曝光的屬性轉換。 這包括視訊和連線電視廣告，並排除[!DNL Advertising Search, Social, & Commerce]廣告的點按次數。

   * *[!UICONTROL Social Only]：*&#x200B;已過時

另請參閱&quot;[如何計算Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md)的歸因規則。&quot;

* **回顧：** ([!UICONTROL Household Conversion]個具有[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]欄的報告，以及[!UICONTROL Path to Conversion]、[!UICONTROL Path Length]或[!UICONTROL Time to Conversion]個僅具有[!UICONTROL Conversion Metrics]欄的報告；僅具有Adobe Advertising轉換追蹤的廣告商)在報告內，轉換事件可歸因至其的曝光事件或點按事件（[!UICONTROL Path to Conversion]、[!UICONTROL Path Length]或[!UICONTROL Time to Conversion]報告）後的最大天數。 預設值為&#x200B;*[!UICONTROL 30 days]*，最大值為92天。

  >[!TIP]
  >
  >如果您使用[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)，則請使用您在[!DNL Analytics]中使用的相同回顧期間。

**[!UICONTROL Paths as Columns]：** （所有[!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment]和[!UICONTROL Site]報告包含[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]欄）當相同裝置上發生先前的事件時，要報告的轉換型別。 您最多可以包含三種型別。 對於每個選取的型別，每個轉換量度都會包含個別的欄，並附加指定的尾碼（[!UICONTROL (tl)]、[!UICONTROL (ct)]或[!UICONTROL (vt)]）：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]：*&#x200B;包含歸因到點按次數（點進為CT）和曝光數（點進為VT）的轉換。 歸屬於曝光的轉換次數會乘以指定的瀏覽權數。 預設的閱覽權重為100%，這表示歸因於曝光的轉換會計為歸因於點按的轉換值的100%。

* *[!UICONTROL With Clicks (CT)]：*&#x200B;僅包含歸因於點按的轉換。

* *[!UICONTROL Impressions Only (VT)]：*&#x200B;僅包含歸屬於曝光數的轉換，因為轉換路徑中未追蹤任何點按。

**[!UICONTROL Conversion Reporting Based On]：**&#x200B;如何報告轉換資料：

* *[!UICONTROL Conversion Timestamp]：* （預設）轉換與轉換日期相關聯。

* *[!UICONTROL Event Timestamp]：*&#x200B;轉換是根據造成轉換的曝光或點按日期（由指定的[!UICONTROL Attribution Rule Settings]決定）回報。

## [!UICONTROL Add Report Destinations]節

**[!UICONTROL Destination Type]：**&#x200B;傳送已完成報告和錯誤通知的位置。 儲存報表後，就無法變更目的地型別。

>[!NOTE]
>
>您一律可以從[!UICONTROL Reports] > [!UICONTROL Custom Reports]檢視下載完成的報告。

* *[!UICONTROL None]：*&#x200B;不傳遞任何報告或通知。

* *[!UICONTROL S3]：*&#x200B;若要將已完成的報告傳送至一或多個[!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您必須在&#x200B;**[!UICONTROL Destination Name]**&#x200B;欄位中選取該位置。

* *[!UICONTROL sFTP]：*&#x200B;若要將完成的報表傳送至一或多個SFTP位置，您必須在&#x200B;**[!UICONTROL Destination Name]**&#x200B;欄位中選取該位置。

* *[!UICONTROL FTP]：*&#x200B;若要將完成的報表傳送至一或多個FTP位置，您必須在&#x200B;**[!UICONTROL Destination Name]**&#x200B;欄位中選取該位置。

* *[!UICONTROL FTP SSL] (目前在Beta中)：*&#x200B;若要將完成的報表傳送至一或多個FTP SSL位置，您必須在&#x200B;**[!UICONTROL Destination Name]**&#x200B;欄位中選取該位置。

* *[!UICONTROL Email]：*&#x200B;若要指定電子郵件位址，以便在報告因錯誤而取消時，將已完成的報告或通知傳送至該位址。

**[!UICONTROL Email]：** （僅限電子郵件目的地型別）針對每個地址，輸入地址並按一下&#x200B;**+**。

**[!UICONTROL Destination Name]：** （僅限S3、FTP、sFTP和FTP SSL目的地型別）自訂報告傳送到的報告目的地的名稱。

* 若要指定現有的目的地，請從清單中選取目的地名稱。 您可以分別選取多個目的地名稱。

* 若要建立新的目的地：

   1. 按一下&#x200B;**新增目的地**。

   1. 輸入[報表目的地設定](/help/dsp/reports/report-destinations/report-destination-settings.md)，然後按一下&#x200B;**儲存**。

   1. 返回報表設定，按一下&#x200B;**重新整理目的地名稱。**

      新目的地現在可從現有目的地的清單中使用，並且您可以選擇將其新增到報表。

>[!MORELIKETHIS]
>
>* [關於自訂報告](/help/dsp/reports/report-about.md)
>* [建立自訂報告](/help/dsp/reports/report-create.md)
>* [複製自訂報告](/help/dsp/reports/report-copy.md)
>* [編輯自訂報告](/help/dsp/reports/report-edit.md)
>* [下載自訂報告](/help/dsp/reports/report-download.md)
>* [執行自訂報告](/help/dsp/reports/report-run-now.md)
>* [自訂報告設定](/help/dsp/reports/report-settings.md)
>* [關於報告目的地](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [可用的報告欄](/help/dsp/reports/report-columns.md)
