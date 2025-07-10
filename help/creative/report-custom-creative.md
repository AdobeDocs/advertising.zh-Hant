---
title: '[!UICONTROL Custom Creative Report]'
description: 瞭解如何產生跨體驗[!UICONTROL Custom Creative Report]。
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '2019'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*已關閉的Beta*

[!UICONTROL Custom Creative Report]可讓您自訂所有廣告體驗的內容與報表資料的傳送。

您可以根據指定條件（例如每15天或每個月1日），在指定時區的03:00產生一次報表，或安排每日、每週或每月產生報表。 報告產生後，您可以從[!UICONTROL Reports] > [!UICONTROL Custom Reports]或以下列型別的已連結[報告目的地](/help/dsp/reports/report-destinations/report-destination-about.md)下載報告：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

## 建立[!UICONTROL Custom Creative Report]

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]**。

1. 指定[報表設定](#report-settings)。

1. 按一下&#x200B;**[!UICONTROL Create Custom Report]**。

## 報表設定 {#report-settings}

**[!UICONTROL Name]：**&#x200B;報告名稱。 長度上限為180個字元。

**[!UICONTROL Report Type]：**&#x200B;報告的型別： *[!UICONTROL Custom Creative Beta]*。

### [!UICONTROL Report Range]節

此區段會決定報表中包含的資料。 若要設定報告排程的日期，請參閱&quot;[!UICONTROL Report run schedule]&quot;區段。

**[!UICONTROL Timezone]：**&#x200B;報告的時區。

**[!UICONTROL Observe Daylight Savings Time]：**&#x200B;會考量報告時間中的日光節約時間。

**範圍：**&#x200B;要產生資料的日期範圍。 可用天數因報表和所選維度而異。 選擇一項：

* **[!UICONTROL Previous Calendar Week]：**&#x200B;包含前一個日曆週的資料。

* **[!UICONTROL Previous Calendar Month]：**&#x200B;包含前一個日曆月的資料。

* **[!UICONTROL Custom Range]：**&#x200B;包含特定開始和結束日期之間的資料。 若要報告前一天的資料，請選取&#x200B;**[!UICONTROL Present]**。

### [!UICONTROL Report Run schedule]節

此區段決定執行報告的日期。 若要設定包含報表資料的日期，請參閱&quot;[!UICONTROL Report range]&quot;區段。

**\[排程\]：**&#x200B;何時產生報表：

* *[!UICONTROL Immediately]*：立即將報表新增至報表佇列。

  >[!NOTE]
  >
  >您也可以[隨時從](/help/dsp/reports/report-run-now.md)檢視[!UICONTROL Reports]執行自訂報告。

* *[!UICONTROL On]\&lt;Date\>：*&#x200B;在帳戶時區的指定完成日期以09:00執行報表。

* *[!UICONTROL Recurring]：*&#x200B;在指定的時間期間根據排程執行報告。

   * **\[排程\]：**&#x200B;執行報告的頻率：

      * *每日*，每N天執行一次報表。 例如，若要每兩週（14天）執行一次報表，請選取此選項並輸入&#x200B;**14**。

      * *每週*，在一週中的指定日期執行報告。 例如，若要每週一和週五執行報表，請選取此選項，然後選取&#x200B;**週一**&#x200B;和&#x200B;**週五**&#x200B;旁的核取方塊。

      * *每月*，針對該月特定數值日（從1到30）執行報表。 例如，在每個月的第一天執行報告，選取此選項並輸入&#x200B;**1**。

   * **從**：報表可以執行的第一個日期。 根據指定的排程，第一個報表例項可能會發生在此日期之後。

   * **直到**：報告到期日，最多可隔四個行事曆月。 在報告到期之前，所有指定的電子郵件目的地都會在到期日七天零一天前收到電子郵件警示。 若要保留更長的報表，請變更此日期。

### [!UICONTROL Apply Filters]節

**[!UICONTROL Filter by]：** （選用）篩選資料所依據的其他維度，無論維度是否包含在報表中作為欄。 可用的篩選器因報告型別而異，可能包括： *[!UICONTROL Advertiser]*、*[!UICONTROL Experience]*、*[!UICONTROL Creative Library]*&#x200B;和&#x200B;*[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->。

若要套用一或多個篩選器，請執行下列動作：

* 選取維度、選取運運算元（*等於*&#x200B;或&#x200B;*不等於*），然後選取適用的值。 例如，若要只傳回前段廣告的資料，請指定&quot;[!UICONTROL Ad Type equals Preroll]&quot;。
* （選用）將其他條件新增至篩選器。
* （選用）新增其他篩選器，每個篩選器一或多個條件。

### [!UICONTROL Build Your Report]節

**[!UICONTROL Select To Add As Report Headers]：**&#x200B;要包含在報告中的資料欄或標題。 若要新增欄，請展開類別並選取欄名稱旁的核取方塊。 可用的欄會依報告而有所不同，並且所有無法使用的量度都會停用。 如需所有選項的說明，請參閱[可用的報表欄](#report-custom-creative-columns)。

**[!UICONTROL Drag to Re-Order Report Headers Below]：**&#x200B;資料行標頭的順序。 您可以拖放任何欄以自訂順序。

**[!UICONTROL Format]：**&#x200B;是以&#x200B;*[!UICONTROL CSV]* （逗號分隔值）還是&#x200B;*[!UICONTROL Tab]* （定位鍵分隔值）格式產生報表。

**[!UICONTROL Headers]：**&#x200B;是&#x200B;*[!UICONTROL Include]*&#x200B;或&#x200B;*[!UICONTROL Do Not Include]*&#x200B;欄標題。

### [!UICONTROL Multi-Touch Conversion Options]節

**[!UICONTROL Attribution Rule Settings]：**&#x200B;設定會因報告型別而異：

* **\[歸因型別\]：** (僅具有Adobe Advertising轉換追蹤的廣告商)在報表中，如何在一連串導致轉換的事件中歸因轉換資料：

   * *[!UICONTROL Unique]：* （預設值）計算維度值（例如裝置或位置）在轉換路徑上的次數。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]：*&#x200B;根據維度值（例如裝置或位置）在轉換路徑上的發生頻率，分配每個轉換的評分。 例如，如果在轉換前共有10次曝光，其中8次在CTV上，2次在行動裝置上，則80%的評分(0.8)會給予予CTV熒幕，而0.2次給予行動裝置。

* **\[規則型別\]：** (僅具有Adobe Advertising轉換追蹤的廣告商)在報表中，如何在一連串導致轉換的事件中歸因轉換資料。 如果要比較規則之間的差異，您可以選擇多個規則。

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

**[!UICONTROL Paths as Columns]：**&#x200B;當相同裝置上發生先前的事件時，要報告哪些轉換型別。 您最多可以包含三種型別。 對於每個選取的型別，每個轉換量度都會包含個別的欄，並附加指定的尾碼（[!UICONTROL (tl)]、[!UICONTROL (ct)]或[!UICONTROL (vt)]）：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]：*&#x200B;包含歸因到點按次數（點進為CT）和曝光數（點進為VT）的轉換。 歸屬於曝光的轉換次數會乘以指定的瀏覽權數。 預設的閱覽權重為100%，這表示歸因於曝光的轉換會計為歸因於點按的轉換值的100%。

* *[!UICONTROL With Clicks (CT)]：*&#x200B;僅包含歸因於點按的轉換。

* *[!UICONTROL Impressions Only (VT)]：*&#x200B;僅包含歸屬於曝光數的轉換，因為轉換路徑中未追蹤任何點按。

### [!UICONTROL Add Report Destinations]節

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

**[!UICONTROL Destination Name]：** （僅限S3、FTP、sFTP和FTP SSL目的地型別）自訂報告傳送至的[報告目的地](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}的名稱。

* 若要指定現有的目的地，請從清單中選取目的地名稱。 您可以分別選取多個目的地名稱。

* 若要建立新的目的地：

   1. 按一下&#x200B;**新增目的地**。

   1. 輸入[報表目的地設定](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"}，然後按一下&#x200B;**儲存**。

   1. 返回報表設定，按一下&#x200B;**重新整理目的地名稱。**

      新目的地現在可從現有目的地的清單中使用，並且您可以選擇將其新增到報表。

## 可用報表欄 {#report-custom-creative-columns}

| 量度型別 | 子型別 | 欄名稱 | 說明 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | 已發佈廣告的維度。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | 提供的廣告是體驗的預設影像廣告或視訊廣告。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | 廣告是根據相對權重（*加權*）或演演算法（*演演算法*）旋轉。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | [!UICONTROL Creative]指派給創意的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | 創意內容的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | 創意型別（例如[!UICONTROL HTML5]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | [!UICONTROL Creative]指派給上層創意內容的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | 上層創意內容的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | 父級創意型別（例如[!UICONTROL HTML5]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | 登陸頁面URL。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | 使用者互動的特定型別。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | 使用者在創意體驗中點按互動的定向流程或導覽路徑。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | 顯示廣告的瀏覽器（例如[!UICONTROL Chrome]或[!UICONTROL Firefox]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | 顯示廣告的作業系統（例如[!UICONTROL Windows]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | 顯示廣告的裝置型別（例如[!UICONTROL Desktop]）。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | 執行廣告的DSP名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | 執行廣告之版位的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | 執行廣告之位置的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | 執行廣告的網站ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | 執行廣告的網站名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | [!UICONTROL Creative]指派給廣告體驗標籤的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | 廣告商的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | 事件的日期和時間。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | [!UICONTROL Creative]指派給體驗的識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | 體驗的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | 通過目標決策樹的特定路徑，可確定向使用者提供的創意體驗變體。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | 廣告標籤的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | 報告資料所屬的城市。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | 報告資料所屬國家/地區的國家/地區代碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | 報告資料所屬的指定市場區域(DMA)。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | 報告資料所屬州的州碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | 報告資料歸因的郵遞區號。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | （動態廣告）目標產品類別ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | （動態廣告）目標產品類別名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | （動態廣告）第一個創意屬性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | （動態廣告）第二個創意屬性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | （動態廣告）第三個創意屬性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | （動態廣告）第四個創意屬性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | （動態廣告）第五個創意屬性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | （動態廣告）目標產品ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | （動態廣告）目標產品名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | 最多五個符合廣告主題的使用者區段的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | 報告資料所屬之重新定位畫素的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | 報告資料所屬的重新定位畫素名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | 報表資料所屬對象區段的屬性。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | 對廣告的所有點按總和。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | 點進率，即點按百分比除以廣告曝光數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | 提供並導致使用者參與的曝光百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 已投放廣告的互動次數。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 廣告印象總數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | 具有重新目標定位Cookie的曝光百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | （僅限動態廣告）產品廣告的所有點按總和。 當產品為Null時，此值為零(0)。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | （僅限動態廣告）產品廣告上所有轉換的總和。 當產品為Null時，此值為零(0)。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | （僅限動態廣告）產品導致轉換的廣告百分比。 當產品為Null時，此值為零(0)。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | （僅限動態廣告）產品廣告的點進率，即點按百分比除以廣告曝光數。 當產品為Null時，此值為零(0)。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | （僅限動態廣告）產品的曝光總數。 當產品為Null時，此值為零(0)。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | （僅限動態廣告）為產品提供的廣告總收入。 當產品為Null時，此值為零(0)。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | 已投放廣告的總收入。 |
| [!UICONTROL Conversion Metrics] | [在報告設定中依廣告商分組] | [廣告商特定轉換] | 指定的廣告商特定轉換量度或Adobe Analytics事件的總計。 |
| [!UICONTROL Custom Goals] | [在報告設定中依廣告商分組] | [廣告商特定自訂目標] | (使用Advertising DSP的廣告商)指定[Advertising DSP自訂目標](/help/dsp/optimization/custom-goal.md)中包含的所有轉換的加權總和。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [體驗層級效能報告](/help/creative/experiences/experience-performance-details.md)
>* [關於DSP自訂報告](/help/dsp/reports/report-about.md){target="_blank"}
>* [關於[!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
