---
title: 自訂報表設定
description: 請參閱自訂報表設定的說明。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# 自訂報表設定

**[!UICONTROL Name]** 報表名稱。 長度上限為180個字元。

**[!UICONTROL Report Type]** 報表型別： *[!UICONTROL Custom]* （其中包含大多數可用選項）、 *[!UICONTROL Billing]*， *[!UICONTROL Conversion]*， *[!UICONTROL Device]*， *[!UICONTROL Frequency (by Impression)]*，  *[!UICONTROL Frequency (by App/Site)]*， *[!UICONTROL Geo]*， *[!UICONTROL Margin]*， *[!UICONTROL Media Performance]*，  *[!UICONTROL Segment]*， *[!UICONTROL Site]*， *[!UICONTROL Household Reach & Frequency]*，或 *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] 章節

**[!UICONTROL Timezone]：** 報表的時區。

**[!UICONTROL Observe Daylight Savings Time]：** 考量報告時間中的日光節約時間。

**\[日期範圍\]：** 要產生資料的日期範圍。 可用天數因報表和所選維度而異。 選擇一項：

* **[!UICONTROL Previous N days]：** 包括今天之前特定天數的資料。

* **[!UICONTROL Custom]：** 包含特定開始和結束日期之間的資料。 若要報告前一天的資料，請選取 **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]：** 包含前一個日曆月的資料。

**[!UICONTROL Add Filters]：** （選用）篩選資料所依據的其他維度，無論這些維度是否作為欄包含在報表中。 可用的篩選器因報告型別而異，可能包括： *[!UICONTROL Account]*\*， *[!UICONTROL Ad Type]*， *[!UICONTROL Ads]*， *[!UICONTROL Advertiser]*， *[!UICONTROL Campaign]*， *[!UICONTROL Country]*， * *[!UICONTROL Package]*， *[!UICONTROL Placement]*， *[!UICONTROL Video]*、和 *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* 只有當您的組織設定為時，才可用於以下報表型別 [跨帳戶報告](report-about.md#cross-account-reporting)：  [!UICONTROL Custom]， [!UICONTROL Site]， [!UICONTROL Segment]， [!UICONTROL Geo]， [!UICONTROL Device]， [!UICONTROL Frequency (by Impression)]、和 [!UICONTROL Conversion]. 如需跨帳戶報告的詳細資訊，請聯絡您的Adobe客戶團隊。

若要套用一或多個篩選器，請執行下列動作：

* 選取維度，然後選取運運算元(*等於* 或 *不等於*)，然後選取適用的值。 例如，若只要傳回前段廣告的資料，請指定&quot;[!UICONTROL Ad Type equals Preroll].」
* （選用）將其他條件新增至篩選器。
* （選用）新增其他篩選器，每個篩選器一或多個條件。

## [!UICONTROL Build Your Report] 章節

**[!UICONTROL Select To Add As Report Headers]：**  要包含在報表中的資料欄或標題。 若要新增欄，請展開類別並選取欄名稱旁的核取方塊。 可用的欄會依報告而有所不同，並且所有無法使用的量度都會停用。 可用的資料類別包括：

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > 此 [!UICONTROL Household Reach & Frequency] 報表只能包含一個維度。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >此 [!UICONTROL Household Reach & Frequency] 報表可包含重疊量度或非重疊量度，但不能同時包含兩者。

* [!UICONTROL Conversion Metrics] （依廣告商排序）

* [!UICONTROL Custom Goals] （依廣告商排序）

請參閱&quot;[可用報表欄](report-columns.md)」以取得所有選項的說明。

**[!UICONTROL Drag to Re-Order Report Headers Below]：** 欄標題的順序。 您可以拖放任何欄以自訂順序。

**[!UICONTROL Format]：** 是否在中產生報表 *[!UICONTROL CSV]* （逗號分隔值）或 *[!UICONTROL Tab]* （以Tab分隔的值）格式。

**[!UICONTROL Headers]：** 是否要 *[!UICONTROL Include]* 或 *[!UICONTROL Do Not Include]* 欄標題。

## [!UICONTROL Multi-Touch Conversion Options] 章節

**[!UICONTROL Attribution Rule Settings]：** 設定會依報告型別而異：

* **\[歸因型別\]：** ([!UICONTROL Household Conversion] 報告與 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；僅具有Adobe Advertising轉換追蹤的廣告商)在報表中，如何將轉換資料歸因到導致轉換的一系列事件中：

   * *[!UICONTROL Unique]：* （預設）計算維度值（例如裝置或位置）在轉換路徑上的次數。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]：*  根據轉換路徑上維度值（例如裝置或位置）的發生頻率，分配每個轉換的評分。 例如，如果在轉換前共有10次曝光，其中8次在CTV上，2次在行動裝置上，則80%的評分(0.8)會給予予CTV熒幕，而0.2次給予行動裝置。

* **\[規則型別\]：** (全部 [!UICONTROL Custom]， [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]， [!UICONTROL Segment]、和 [!UICONTROL Site] 報告與 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；僅具有Adobe Advertising轉換追蹤的廣告商)在報表中，如何將轉換資料歸因到導致轉換的一系列事件中。 如果要比較規則之間的差異，您可以選擇多個規則。

  >[!NOTE]
  >
  >轉換路徑包含廣告商曝光數或點按回顧期間內的任何曝光數和點按，這些設定於 [!DNL Advertising Search, Social, & Commerce]. 在轉換歸因期間，點按次數會優先於曝光數。 根據歸因規則，轉換路徑中的任何點按都會獲得完整評價。 只有轉換路徑中未追蹤任何點按時，曝光次數才會獲得評分。

   * *[!UICONTROL Last Event]：* 將轉換歸因於轉換路徑中的最後點按或印象。

   * *[!UICONTROL Weight Last More]：* 將轉換歸因於轉換路徑中的所有事件，但給予最後一個事件最大的權重，並連續減少先前事件的權重。

   * *[!UICONTROL Even Distribution]：* 將轉換平均歸因於轉換路徑中的每個事件。

   * *[!UICONTROL Weight First More]：* 將轉換歸因於轉換路徑中的所有事件，但給予第一個事件最大的權重，並連續減少下列事件的權重。

   * *[!UICONTROL First Event]：* 將轉換歸因於轉換路徑中的第一次點按或印象。

   * *[!UICONTROL U-shaped]：* 將轉換歸因於轉換路徑中的所有事件，但給予第一個和最後一個事件的權重最大，給予轉換路徑中間事件的權重則依次較低。

   * *[!UICONTROL Display Only]：*  將轉換歸因於轉換路徑中的最後一個DSP點按或曝光次數。 這包括視訊和連線電視廣告，並排除點選次數 [!DNL Advertising Search, Social, & Commerce] 廣告。

   * *[!UICONTROL Social Only]：* 已過時

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **回顧：** ([!UICONTROL Household Conversion] 報告與 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；僅具有Adobe Advertising轉換追蹤的廣告商)在報表中，轉換事件可歸因於曝光事件的最大天數。 預設值為 *[!UICONTROL 30 days]*，最大為92天。

**[!UICONTROL Paths as Columns]：**  (全部 [!UICONTROL Custom]， [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]， [!UICONTROL Segment]、和 [!UICONTROL Site] 報告與 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄)相同裝置上發生先前事件時要報告的轉換型別。 您最多可以包含三種型別。 對於每個選取的型別，每個轉換量度都會包含個別的欄，並附加指定的尾碼([!UICONTROL (tl)]， [!UICONTROL (ct)]，或 [!UICONTROL (vt)])：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]：* 包含歸因於點按次數（點進為CT）和曝光數（點進為VT）的轉換。 歸屬於曝光的轉換次數會乘以指定的瀏覽權數。 預設的閱覽權重為100%，這表示歸因於曝光的轉換會計為歸因於點按的轉換值的100%。

* *[!UICONTROL With Clicks (CT)]：* 僅包含歸因於點按的轉換。

* *[!UICONTROL Impressions Only (VT)]：* 僅包含歸屬於曝光次數的轉換，因為轉換路徑中未追蹤任何點按。

**[!UICONTROL Conversion Reporting Based On]：**  如何報告轉換資料：

* *[!UICONTROL Conversion Timestamp]：* （預設）轉換與轉換日期相關聯。

* *[!UICONTROL Event Timestamp]：* 轉換會根據造成轉換的曝光或點按日期回報，如指定的所決定 [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] 章節

**[!UICONTROL Destination Type]：** 選擇下列其中一個目的地型別：

* *[!UICONTROL S3]：* 若要將完成的報表傳送至一或多個 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您必須在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL sFTP]：* 若要將完成的報表傳送至一或多個SFTP位置，您必須在的 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL FTP]：* 若要將完成的報表傳送至一或多個FTP位置，您必須在的 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL FTP SSL]（目前為測試版）：* 若要將完成的報表傳送至一或多個FTP SSL位置，您必須在以下位置指定： **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL Email]：* 若要指定電子郵件位址，以便在報告因錯誤而取消時，將已完成的報告或通知傳送至該位址。

>[!NOTE]
>
> 儲存報表後，就無法變更目的地型別。

**[!UICONTROL Email]：** （僅限電子郵件目的地型別）針對每個地址，輸入地址並按一下 **+**.

**[!UICONTROL Destination Name]：** （僅限S3、FTP、sFTP和FTP SSL目的地型別）自訂報表所傳送到之報表目的地的名稱。

* 若要指定現有的目的地，請從清單中選取目的地名稱。 您可以分別選取多個目的地名稱。

* 若要建立新的目的地：

   1. 按一下 **新增目的地**.

   1. 輸入 [報表目的地設定](/help/dsp/reports/report-destinations/report-destination-settings.md)，然後按一下 **儲存**.

   1. 返回報表設定，按一下 **重新整理目的地名稱。**

      新目的地現在可從現有目的地的清單中使用，並且您可以選擇將其新增到報表。

**[!UICONTROL Frequency]：** (針對每個 [!UICONTROL Destination Name])將報表傳送至目的地的頻率： *[!UICONTROL Once]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*，或 *[!UICONTROL Monthly]*.

**[!UICONTROL Start Day]：** (針對每個 [!UICONTROL Destination Name] 與 [!UICONTROL Frequency] 之 *[!UICONTROL Weekly]* 或 *[!UICONTROL Monthly]*)產生報表的日期。 若是每週報告，請選取一週中的某天。 對於月報表，請選取月份的數值日。

## [!UICONTROL Save Report] 章節

**[!UICONTROL When to Generate]：** 何時產生報表： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*. 排程報表在帳戶時區的09:00傳送。

**[!UICONTROL End Date]：** 報告到期日，最長可隔四個月。 在報告到期之前，所有指定的電子郵件收件者都會在到期日七天零一天前收到電子郵件警報。 若要保留更長的報表，請變更報表設定中的到期日。

>[!NOTE]
>
>您可以 [隨時執行自訂報表](report-run-now.md) 從 [!UICONTROL Reports] 檢視。

>[!MORELIKETHIS]
>
>* [關於自訂報表](/help/dsp/reports/report-about.md)
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [複製自訂報告](/help/dsp/reports/report-copy.md)
>* [編輯自訂報告](/help/dsp/reports/report-edit.md)
>* [執行自訂報表](/help/dsp/reports/report-run-now.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)
>* [關於報表目的地](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [可用報表欄](/help/dsp/reports/report-columns.md)
