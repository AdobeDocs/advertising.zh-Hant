---
title: 使用試算表檢閱和編輯位置設定
description: 瞭解如何使用試算表檢閱和編輯關鍵位置設定。
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# 使用試算表檢閱和編輯位置設定

您可以以XLSX （Excel試算表）格式下載一或多個刊登版位，或行銷活動中的所有刊登版位的設定，以供檢閱。 使用此功能可快速檢閱下列詳細資訊：

* 行銷活動鎖定哪些對象。
* 刊登版位開始傳送及停止的時間。
* 哪些廣告附加至刊登版位。

然後，您可以進行變更以選取欄位，並一次將欄位上傳回DSP。 可編輯的欄位包括版位名稱、狀態、投標、預算、步調策略和頻率上限。

>[!TIP]
>
>若要編輯一或多個位置的多個欄位，請參閱[編輯位置](/help/dsp/campaign-management/placements/placement-edit.md)。

## 行銷活動中所有版位的下載設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 在行銷活動名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**」。

   * 按一下行銷活動名稱以檢視行銷活動詳細資料。 按一下右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**。

   通知訊息會指出檔案何時可供下載。

1. 執行下列任一項作業：

   * 在通知訊息中，按一下&#x200B;**[!UICONTROL Download].**

   * 在頂端功能表列的右側，按一下![工作](/help/dsp/assets/downloads.png)。 按一下工作旁的&#x200B;**[!UICONTROL Download]**。

   檔案會儲存至瀏覽器的「下載」資料夾。 如需所包含欄的清單，請參閱[已下載/上傳試算表](#qa-sheet-columns)中的欄。

## 一或多個位置的下載設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下&#x200B;**[!UICONTROL Placements]**。

1. 選取每個要下載其設定的位置旁的核取方塊。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**。

檔案會自動儲存至瀏覽器的「下載」資料夾。 如需所包含欄的清單，請參閱[已下載/上傳試算表](#qa-sheet-columns)中的欄。

## 上傳行銷活動中所有位置的設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 在行銷活動名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**」。

   * 按一下行銷活動名稱以檢視行銷活動詳細資料。 按一下右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**。

1. 在[!UICONTROL Edit in Excel]對話方塊：

   1. 將檔案拖放至方塊中，或按一下方塊內部，從您的裝置或網路選取檔案。

   1. 按一下&#x200B;**[!UICONTROL Upload]**。

1. （選擇性）若要確認已處理更新，請按一下頂端功能表列右側的![工作](/help/dsp/assets/downloads.png)。

## 上傳一或多個位置的設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下&#x200B;**[!UICONTROL Placements]**。

1. 選取每個要上傳其設定的位置旁的核取方塊。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**。

1. 在[!UICONTROL Edit in Excel]對話方塊：

   1. 將檔案拖放至方塊中，或按一下方塊內部，從您的裝置或網路選取檔案。

   1. 按一下&#x200B;**[!UICONTROL Upload]**。

1. （選擇性）若要確認已處理更新，請按一下頂端功能表列右側的![工作](/help/dsp/assets/downloads.png)。

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
| [!UICONTROL Basic] | [!UICONTROL Status] | 位置狀態： *[!UICONTROL active]*&#x200B;或&#x200B;*[!UICONTROL inactive]*。 | 是 |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 位置型別。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 父套件的名稱（如果適用）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 刊登的開始日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 刊登的結束日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 分日是&#x200B;*[!UICONTROL ON]*&#x200B;還是&#x200B;*[!UICONTROL OFF]*。<br><b>注意：</b>若要檢查實際的日時段排程，請在DSP中開啟位置設定。 | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 位置預算（如有）。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 預算間隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | 套件的目標。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目標的目標值。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 位置是朝著&#x200B;*[!UICONTROL Budget]*&#x200B;還是&#x200B;*[!UICONTROL Impressions]*&#x200B;步調。 | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | 此位置的最高出價。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | 此位置的航班步調策略： *[!UICONTROL Even]*、*[!UICONTROL slightly ahead]*、*[!UICONTROL frontload]*&#x200B;或&#x200B;*[!UICONTROL aggressive frontload]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | 此位置的當天步調策略： *[!UICONTROL Even]*&#x200B;或&#x200B;*[!UICONTROL ASAP]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | 要套用的任何競標前篩選條件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 競標規則（已棄用）是&#x200B;*[!UICONTROL ON]*&#x200B;還是&#x200B;*[!UICONTROL OFF]*。 | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 指定[!UICONTROL Frequency Cap Interval]期間位置的主要頻率上限。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | 主要頻率上限的間隔： *[!UICONTROL Day]*、*[!UICONTROL Week]*&#x200B;或&#x200B;*[!UICONTROL Month]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 在指定[!UICONTROL Secondary Frequency Cap Interval]期間放置的次要頻率上限 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | 次要頻率上限的間隔型別： *[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*&#x200B;或&#x200B;*[!UICONTROL Minute]*。 [!UICONTROL Secondary Frequency Cap Interval Value]會指出適用的周數、天數、小時數或分鐘數。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]適用的周數、天數、小時或分鐘。 例如，如果次要曝光次數上限為每六小時三次曝光，則這裡的值將是`6`。 | 是 |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | 目標地理位置&#x200B;*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*&#x200B;的數量。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | 目標地理位置，以分號或&#x200B;*[!UICONTROL All Locations]*&#x200B;分隔。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 排除的地理位置數或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 排除的地理位置，以分號或&#x200B;*[!UICONTROL None]*&#x200B;分隔。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 已指定目標公開詳細目錄交易的數量（若有的話）、*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 已指定排除的公開詳細目錄交易的數量（若有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | 已指定目標私人詳細目錄交易的數量（若有的話）、*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 已指定排除的私人詳細目錄交易的數量（若有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | 已指定目標[!UICONTROL On-Demand Inventory]交易的數量（若有的話）、*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | 已指定排除的隨選詳細目錄交易數（若有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | 流量的目標型別： *[!UICONTROL Website]*&#x200B;和/或&#x200B;*[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | 要排除輸出流流量的詳細目錄鎖定選項是&lt;i[!UICONTROL >ON]*還是&#x200B;*[!UICONTROL OFF]*。<br>外流廣告通常以快顯視窗或填入內容（在原生體驗中）的形式出現在內容上，而不是在視訊播放器中一般視訊廣告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | 要定位的網站品質： *[!UICONTROL Tier 1]*、*[!UICONTROL Tier 2]*、*[!UICONTROL Tier 3]*&#x200B;或&#x200B;*[!UICONTROL All Sites]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | 已指定目標網站類別的數目（若有的話），或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 已指定排除的網站類別數（若有的話），或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 已指定排除的網站（如果有的話）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | 目標網站語言。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | （僅限標準顯示位置）是否允許未稽核網站上的廣告傳遞： *[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。 當此版位鎖定私人詳細目錄時，此選項可能會在封鎖的網站上傳送廣告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | 已指定目標網站的數目（若有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | 已指定目標對象（若有的話）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 已指定排除的對象，或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | 是否針對位置（以及行銷活動中的其他位置）啟用[!DNL Comscore]人口統計區段： *[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。 此功能只能針對[!DNL Nielsen]和/或[!DNL Comscore]啟用[!DNL Audience Verification]功能的行銷活動啟用。  這會產生額外費用。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | 是否要跨裝置延伸廣告目標定位： *[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。 跨裝置目標鎖定會根據行銷活動設定中指定的裝置圖表，將您的目標鎖定延伸至人員的所有已知裝置。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] — 包含# | 已指定目標主題程式碼的數目（若有的話），或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 已指定排除的主題代碼數量（若有的話）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | 已指定的目標裝置目標數目，或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 已指定排除的裝置目標數目（若有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | 已指定目標ISP提供者的數目，或是*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | 已指定排除的ISP提供者數目（若有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 已套用品牌安全篩選器的數目（若有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 套用的競標前詐騙封鎖篩選數目（若有指定）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 套用的競標前可檢視度篩選器的數目（如果有的話），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | 是否啟用網站安全區塊： *[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 附加至位置的協力廠商事件追蹤畫素數，或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 附加至位置或&#x200B;*[!UICONTROL None]*&#x200B;的轉換追蹤畫素數目。 | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 要以每1000次曝光的不可記帳成本追蹤的靜態第三方費用率（如適用）。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 附加至此位置的廣告數量（若有），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 附加至該位置的任何廣告的名稱，或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | 任何附加至刊登版位之廣告的唯一DSP產生廣告ID，以分號分隔。 若要從[!UICONTROL Ads]檢視下載廣告名稱和相關聯的廣告ID清單，請建立包含[!UICONTROL Ad ID]量度的自訂檢視，然後[匯出資料](/help/dsp/campaign-management/reports/campaign-export-data.md)。 | 是 |

### 位置層級試算表

| 欄 | 說明 | 可編輯嗎？ |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | 位置的數值ID。 | — |
| [!UICONTROL Placement Name] | 位置的名稱。 | 是 |
| [!UICONTROL Package Name] | 父套件的名稱（如果適用）。 | — |
| [!UICONTROL Start Date] | 刊登的開始日期。 | — |
| [!UICONTROL End Date] | 刊登的結束日期。 | — |
| [!UICONTROL Status] | 位置狀態： *[!UICONTROL active]*&#x200B;或&#x200B;*[!UICONTROL inactive]*。 | — |
| [!UICONTROL Max Bid] | 此位置的最高出價。 | 是 |
| [!UICONTROL Budget] | 位置預算（如有）。 | 是 |
| [!UICONTROL Budget Interval] | 預算間隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Primary Frequency Cap] | 指定[!UICONTROL Primary Frequency Cap Interval]期間位置的主要頻率上限。 | 是 |
| [!UICONTROL Primary Frequency Cap Interval] | 主要頻率上限的間隔： *[!UICONTROL Day]*、*[!UICONTROL Week]*&#x200B;或&#x200B;*[!UICONTROL Month]*。 | 是 |
| [!UICONTROL Secondary Frequency Cap] | 在指定[!UICONTROL Secondary Frequency Cap Interval]期間放置的次要頻率上限 | 是 |
| [!UICONTROL Secondary Frequency Cap Interval] | 次要頻率上限的間隔型別： *[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*&#x200B;或&#x200B;*[!UICONTROL Minute]*。 [!UICONTROL Secondary Frequency Cap Interval Value]會指出適用的周數、天數、小時數或分鐘數。 | 是 |
| [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]適用的周數、天數、小時或分鐘。 例如，如果次要曝光次數上限為每六小時三次曝光，則這裡的值將是`6`。 | 是 |
| [!UICONTROL Attached Ad ID] | 任何附加至刊登版位之廣告的唯一DSP產生廣告ID，以分號分隔。 若要從[!UICONTROL Ads]檢視下載廣告名稱和相關聯的廣告ID清單，請建立包含[!UICONTROL Ad ID]量度的自訂檢視，然後[匯出資料](/help/dsp/campaign-management/reports/campaign-export-data.md)。 | 是 |

>[!MORELIKETHIS]
>
>* [編輯版位](/help/dsp/campaign-management/placements/placement-edit.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
