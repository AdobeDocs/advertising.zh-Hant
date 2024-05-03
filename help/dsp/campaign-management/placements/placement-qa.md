---
title: 使用試算表檢閱並修正版位設定
description: 瞭解如何使用試算表檢閱和編輯關鍵位置設定。
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: f352af0ffd5bfeab08f6592b4f3af56a9668feaa
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 0%

---

# 使用試算表檢閱並修正版位設定

您可以以XLSX （Excel試算表）格式下載一或多個刊登版位，或行銷活動中的所有刊登版位的設定，以供檢閱。 使用此功能可快速檢閱下列詳細資訊：

* 行銷活動鎖定哪些對象。
* 刊登版位開始傳送及停止的時間。
* 哪些廣告附加至刊登版位。

然後，您可以進行變更以選取欄位，並一次將欄位上傳回DSP。 可編輯的欄位包括版位名稱、狀態、投標、預算、步調策略和頻率上限。

>[!TIP]
>
>若要對版位設定進行更廣泛的變更，請使用 [大量編輯功能](/help/dsp/campaign-management/placements/placement-edit.md).

## 行銷活動中所有版位的下載設定

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 執行下列任一項作業：

   * 在行銷活動名稱旁，按一下 **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   * 按一下行銷活動名稱以檢視行銷活動詳細資料。 在右上角，按一下 **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   通知訊息會指出檔案何時可供下載。

1. 執行下列任一項作業：

   * 在通知訊息中，按一下 **[!UICONTROL Download].**

   * 在頂端功能表列的右側，按一下 ![工作](/help/dsp/assets/downloads.png). 按一下 **[!UICONTROL Download]** 位於工作旁。

   檔案會儲存至瀏覽器的「下載」資料夾。 請參閱&quot;[已下載/已上傳試算表中的欄](#qa-sheet-columns)&quot;，以取得包含欄的清單。

## 一或多個位置的下載設定

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 選取每個要下載其設定的位置旁的核取方塊。

1. 在大量動作工具列中，按一下 **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

檔案會自動儲存至瀏覽器的「下載」資料夾。 請參閱&quot;[已下載/已上傳試算表中的欄](#qa-sheet-columns)&quot;，以取得包含欄的清單。

## 上傳行銷活動中所有位置的設定

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 執行下列任一項作業：

   * 在行銷活動名稱旁，按一下 **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

   * 按一下行銷活動名稱以檢視行銷活動詳細資料。 在右上角，按一下 **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

1. 在 [!UICONTROL Edit in Excel] 對話方塊：

   1. 將檔案拖放至方塊中，或按一下方塊內部，從您的裝置或網路選取檔案。

   1. 按一下 **[!UICONTROL Upload]**.

1. （選用）若要確認已處理更新，請按一下 ![工作](/help/dsp/assets/downloads.png) 在頂端功能表列的右側。

## 上傳一或多個位置的設定

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 選取每個要上傳其設定的位置旁的核取方塊。

1. 在大量動作工具列中，按一下 **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. 在 [!UICONTROL Edit in Excel] 對話方塊：

   1. 將檔案拖放至方塊中，或按一下方塊內部，從您的裝置或網路選取檔案。

   1. 按一下 **[!UICONTROL Upload]**.

1. （選用）若要確認已處理更新，請按一下 ![工作](/help/dsp/assets/downloads.png) 在頂端功能表列的右側。

## 位置設定已下載/上傳試算表中的欄{#qa-sheet-columns}

>[!TIP]
>
> 在下載的試算表中，所有可編輯的欄都會以藍色反白顯示。

### 行銷活動層級試算表

| 章節 | 欄 | 說明 | 可編輯嗎？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | 位置的數值ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | 位置的名稱。 | 是 |
| [!UICONTROL Basic] | [!UICONTROL Labels] | 任何套用的標籤，用於報表。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | 在「編輯」模式中開啟位置的連結。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | 位置狀態： *[!UICONTROL active]* 或 *[!UICONTROL inactive]*. | 是 |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 位置型別。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 父套件的名稱（如果適用）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 刊登的開始日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 刊登的結束日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 分日是否為 *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<br><b>注意：</b> 若要檢查實際的播出時間表，請在DSP中開啟位置設定。 | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 位置預算（如有）。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 預算間隔： &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*，或 *[!UICONTROL All Time]*.[!UICONTROL >Daily] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | 套件的目標。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目標的目標值。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 投放位置是否朝著 *[!UICONTROL Budget]* 或 *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | 此位置的最高出價。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | 此投放位置的航班步調策略： *[!UICONTROL Even]*， *[!UICONTROL slightly ahead]*， *[!UICONTROL frontload]*，或 *[!UICONTROL aggressive frontload]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | 刊登的當天步調策略： *[!UICONTROL Even]* 或 *[!UICONTROL ASAP]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | 要套用的任何競標前篩選條件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 競標規則（已棄用）是否為 *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 在指定期間放置的主要頻率上限 [!UICONTROL Frequency Cap Interval]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | 主要頻率上限的間隔： *[!UICONTROL Day]*， *[!UICONTROL Week]*，或 *[!UICONTROL Month]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 在指定期間放置的次要頻率上限 [!UICONTROL Secondary Frequency Cap Interval] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | 次要頻率上限的間隔型別： *[!UICONTROL Week]*， *[!UICONTROL Day]*， *[!UICONTROL Hour]*，或 *[!UICONTROL Minute]*. 適用的周數、天數、小時數或分鐘數會由 [!UICONTROL Secondary Frequency Cap Interval Value]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | 「 」的周數、天數、小時數或分鐘數 [!UICONTROL Secondary Frequency Cap] 適用。 例如，如果次要曝光次數上限為每六小時三次曝光，則這裡的值將為 `6`. | 是 |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | 目標地理位置的數量， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | 目標地理位置（以分號分隔），或 *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 排除的地理位置數或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 排除的地理位置（以分號分隔），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 已指定目標公開詳細目錄交易的數量（如果有的話）， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 已指定排除的公開詳細目錄交易數（如果有的話），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | 已指定目標私人詳細目錄交易的數量（如果有的話）， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 已指定排除的私人詳細目錄交易數（如果有的話），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | 目標數量 [!UICONTROL On-Demand Inventory] 交易（若已指定）， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | 已指定排除的「隨選詳細目錄」交易數目，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | 目標流量型別： *[!UICONTROL Website]* 和/或 *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | 要排除輸出流流量的詳細目錄鎖定選項是否為 &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*或 *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>串流廣告通常以快顯視窗或填入內容（在原生體驗中）的形式出現在內容上，而不是在視訊播放器中一般視訊廣告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | 目標網站的品質： *[!UICONTROL Tier 1]*， *[!UICONTROL Tier 2]*， *[!UICONTROL Tier 3]*，或 *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | 已指定的目標網站類別數（若有），或 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 已指定排除的網站類別數（若有的話），或 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 已指定排除的網站（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | 目標網站語言。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | （僅限標準顯示位置）是否允許廣告傳送至未稽核的網站： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 當此版位鎖定私人詳細目錄時，此選項可能會在封鎖的網站上傳送廣告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | 已指定的目標網站數目，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | 已指定的目標對象（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 已指定的排除對象，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | 無論是否要 [!DNL Comscore] 已為位置啟用人口統計區段（和行銷活動中的其他位置）： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 此功能僅可針對下列行銷活動啟用： [!DNL Audience Verification] 功能已啟用 [!DNL Nielsen] 和/或 [!DNL Comscore].  這會產生額外費用。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | 是否要跨裝置延伸廣告目標定位： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 跨裝置目標鎖定會根據行銷活動設定中指定的裝置圖表，將您的目標鎖定延伸至人員的所有已知裝置。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting]  — 包含# | 已指定的目標主題代碼數（若有），或 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 已指定排除的主題代碼數量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | 已指定的目標裝置目標數目，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 已指定排除的裝置目標數目，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | 已指定目標ISP提供者的數量（若有的話），或*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | 已指定排除的ISP提供者數目，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 已套用品牌安全篩選器的數量（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 套用的競標前詐騙封鎖篩選器數（若有），或是 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 已套用競標前可見度篩選器的數量（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | 是否啟用網站安全區塊： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 附加至刊登版位的第三方事件追蹤畫素數量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 附加至刊登版位的轉換追蹤畫素數量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 要以每1000次曝光的不可記帳成本追蹤的靜態第三方費用率（如適用）。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 附加至刊登版位的廣告數量（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 附加至刊登版位的任何廣告名稱，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | 任何附加至刊登版位之廣告的唯一DSP產生廣告ID，以分號分隔。 若要從下載廣告名稱和相關廣告ID的清單 [!UICONTROL Ads] 檢視，建立自訂檢視，其中包括 [!UICONTROL Ad ID] 量度，然後 [匯出資料](/help/dsp/campaign-management/reports/campaign-export-data.md). | 是 |

### 位置層級試算表

| 欄 | 說明 | 可編輯嗎？ |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | 位置的數值ID。 | — |
| [!UICONTROL Placement Name] | 位置的名稱。 | 是 |
| [!UICONTROL Package Name] | 父套件的名稱（如果適用）。 | — |
| [!UICONTROL Start Date] | 刊登的開始日期。 | — |
| [!UICONTROL End Date] | 刊登的結束日期。 | — |
| [!UICONTROL Status] | 位置狀態： *[!UICONTROL active]* 或 *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | 此位置的最高出價。 | 是 |
| [!UICONTROL Budget] | 位置預算（如有）。 | 是 |
| [!UICONTROL Budget Interval] | 預算間隔： &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*，或 *[!UICONTROL All Time]*.[!UICONTROL >Daily] | 是 |
| [!UICONTROL Primary Frequency Cap] | 在指定期間放置的主要頻率上限 [!UICONTROL Primary Frequency Cap Interval]. | 是 |
| [!UICONTROL Primary Frequency Cap Interval] | 主要頻率上限的間隔： *[!UICONTROL Day]*， *[!UICONTROL Week]*，或 *[!UICONTROL Month]*. | 是 |
| [!UICONTROL Secondary Frequency Cap] | 在指定期間放置的次要頻率上限 [!UICONTROL Secondary Frequency Cap Interval] | 是 |
| [!UICONTROL Secondary Frequency Cap Interval] | 次要頻率上限的間隔型別： *[!UICONTROL Week]*， *[!UICONTROL Day]*， *[!UICONTROL Hour]*，或 *[!UICONTROL Minute]*. 適用的周數、天數、小時數或分鐘數會由 [!UICONTROL Secondary Frequency Cap Interval Value]. | 是 |
| [!UICONTROL Secondary Frequency Cap Interval Value] | 「 」的周數、天數、小時數或分鐘數 [!UICONTROL Secondary Frequency Cap] 適用。 例如，如果次要曝光次數上限為每六小時三次曝光，則這裡的值將為 `6`. | 是 |
| [!UICONTROL Attached Ad ID] | 任何附加至刊登版位之廣告的唯一DSP產生廣告ID，以分號分隔。 若要從下載廣告名稱和相關廣告ID的清單 [!UICONTROL Ads] 檢視，建立自訂檢視，其中包括 [!UICONTROL Ad ID] 量度，然後 [匯出資料](/help/dsp/campaign-management/reports/campaign-export-data.md). | 是 |

>[!MORELIKETHIS]
>
>* [編輯位置](/help/dsp/campaign-management/placements/placement-edit.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
