---
title: 管理自訂報表
description: 瞭解如何產生和管理跨體驗[!UICONTROL Custom Creative Report]。
feature: Creative Reporting
source-git-commit: 455a63be51ca56610cc15ba498e69eeae52ffdba
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

您可以建立、複製、編輯、執行、下載和刪除自訂報告。

## 建立自訂報表 {#report-create}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]**。

1. 指定[報表設定](#report-settings)。

1. 按一下&#x200B;**[!UICONTROL Create Custom Report]**。

## 複製自訂報表

複製自訂報告以使用類似設定建立新報告。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在報告名稱旁邊，按一下「**[!UICONTROL ...]** > **[!UICONTROL Copy]**」。

1. （選擇性）視需要編輯[報告設定](#report-settings.md)。

   報表名稱預設為「\&lt;*現有報表名稱*\> \#2」（或序列中的下一個編號）。

## 編輯自訂報表 {#report-edit}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在報告名稱旁邊，按一下「**[!UICONTROL ...]** > **[!UICONTROL Edit]**」。

1. 編輯[報告設定](#report-settings.md)。

1. 按一下&#x200B;**[!UICONTROL Edit Custom Report]**。

## 執行自訂報表 &lbrace;report-run-now&rbrace;

您可以執行尚未過期且目前未執行的任何報告。

>[!NOTE]
>
>您也可以在您[建立](#report-create)或[編輯](#report-edit)自訂報表時執行它。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在報告名稱旁邊，按一下「**[!UICONTROL ...]** > **[!UICONTROL Run Now]**」。

   報表完成時，會傳送至報表設定中指定的目的地。

## 下載自訂報表

您可以下載任何過去四個月完成的報表執行個體，其狀態為&quot;[!UICONTROL Ready to Download]&quot;或&quot;[!UICONTROL Completed]&quot;。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在報表列的[!UICONTROL Download Report]欄中，執行下列動作：

   * 若要下載最新的報表執行個體，請按一下&#x200B;**[!UICONTROL Download]**。

   * （具有多個執行個體的報表）按一下![旁的](/help/dsp/assets/chevron-down.png "向下箭頭")向下箭頭[!UICONTROL Download]，然後按一下您要下載之報表的完成日期。 可下載的報表執行個體會以下載圖示(![下載圖示](/help/dsp/assets/indicator-downloadable.png "下載圖示"))標示。

     當有許多執行個體可用時，如有必要，請按一下清單底部的&#x200B;**[!UICONTROL Load More]**。

     當報表在當天執行多次時，該天的報表執行個體會依時間順序列出，最新的執行個體會位於頂端。

     失敗的報表工作以錯誤圖示（![錯誤指示器](/help/dsp/assets/indicator-critical.png "錯誤指示器")）表示，無法下載。 將游標放在錯誤圖示上，即可取得錯誤說明。

## 刪除自訂報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在報告名稱旁邊，按一下「**[!UICONTROL ...]** > **[!UICONTROL Delete]**」。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

## 報表設定 {#report-settings}

**[!UICONTROL Name]：**&#x200B;報告名稱。 長度上限為180個字元。

**[!UICONTROL Report Type]：**&#x200B;報告的型別。

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
  >您也可以[隨時從](#report-run-now)檢視[!UICONTROL Reports]執行自訂報告。

* *[!UICONTROL On]\&lt;Date\>：*&#x200B;在帳戶時區的指定完成日期(09:00)執行報表。

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

**[!UICONTROL Select To Add As Report Headers]：**&#x200B;要包含在報告中的資料欄或標題。 若要新增欄，請展開類別並選取欄名稱旁的核取方塊。 可用的欄會依報告而有所不同，而且所有無法使用的量度都會停用。<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]：**&#x200B;資料行標頭的順序。 您可以拖放任何欄以自訂順序。

**[!UICONTROL Format]：**&#x200B;是以&#x200B;*[!UICONTROL CSV]* （逗號分隔值）還是&#x200B;*[!UICONTROL Tab]* （定位鍵分隔值）格式產生報表。

**[!UICONTROL Headers]：**&#x200B;是&#x200B;*[!UICONTROL Include]*&#x200B;或&#x200B;*[!UICONTROL Do Not Include]*&#x200B;欄標題。

### [!UICONTROL Multi-Touch Conversion Options]節

**[!UICONTROL Attribution Rule Settings]：**&#x200B;設定會因報告型別而異：

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


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [體驗層級效能報告](/help/creative/experiences/experience-performance-details.md)
>* [關於DSP自訂報告](/help/dsp/reports/report-about.md){target="_blank"}
>* [關於[!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
