---
title: 使用Bulksheets檢閱和編輯位置設定
description: 瞭解如何使用試算表大量檢閱和編輯關鍵位置設定。
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# 使用Bulksheets檢閱和編輯位置設定

您可以以XLSX （[!DNL Microsoft Excel]試算表）格式下載一或多個刊登版位，或行銷活動中的所有刊登版位的設定，以供檢閱。 使用此功能可快速檢閱下列詳細資訊：

* 行銷活動鎖定哪些對象。
* 刊登版位開始傳送及停止的時間。
* 哪些廣告附加至刊登版位。

若要一次更新多個設定，您可以變更選取欄位、儲存檔案，然後將編輯過的Bulksheet檔案上傳回DSP。 可編輯欄位包含大部分可編輯的設定。

>[!TIP]
>
>若要快速編輯一或多個位置的多個欄位，請參閱[編輯位置](/help/dsp/campaign-management/placements/placement-edit.md)。

## 行銷活動中所有版位的下載設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 在行銷活動旁邊，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

   * 按一下行銷活動名稱。 按一下右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

1. 在[!UICONTROL Bulksheet Download]對話方塊中，取消選取您要從下載檔案中排除其設定的任何促銷活動元件，然後按一下&#x200B;**[!UICONTROL Download]**。

依預設，會選取與封裝相關聯的所有版位和廣告的設定。

通知訊息會指出檔案何時可供下載。

1. 若要下載檔案，請執行下列任一項作業：

   * 在通知訊息中，按一下&#x200B;**[!UICONTROL Download].**

   * 在頂端功能表列的右側，按一下![工作](/help/dsp/assets/downloads.png)。 按一下工作旁的&#x200B;**[!UICONTROL Download]**。

   檔案已儲存至瀏覽器的[下載]資料夾。<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

## 特定位置的下載設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下&#x200B;**[!UICONTROL Placements]**。

1. 選取每個要下載其設定的位置旁的核取方塊。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

   通知訊息會指出何時可下載Bulksheet檔案。

1. 若要下載Bulksheet，請執行下列任一項作業：

   * 在通知訊息中，按一下&#x200B;**[!UICONTROL Download].**

   * 在頂端功能表列的右側，按一下![工作](/help/dsp/assets/downloads.png)。 按一下工作旁的&#x200B;**[!UICONTROL Download]**。

   檔案已儲存至瀏覽器的[下載]資料夾。<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

   若要編輯任何設定，請直接編輯檔案，然後上傳變更。  所有可編輯的欄都會以藍色反白。 若要針對欄位使用正確的格式，請從相關的封裝設定或位置設定中選取並複製值。 對於某些目標設定，例如時段、自訂目標和轉換量度，設定中提供了複製選項。

## 上傳含有位置設定的Bulksheet {#upload-bulksheet-placement}

您可以在大量表單檔案中上傳版位、以及與版位相關聯的廣告和套件的設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 在上層行銷活動旁邊，按一下「**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**」。

   * 按一下行銷活動名稱。 按一下右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**。

     此選項可從[!UICONTROL Packages]、[!UICONTROL Placements]或[!UICONTROL Ads]標籤取得。

   * 在子功能表中按一下&#x200B;**[!UICONTROL Placements]**，然後選取任何位置的核取方塊。 在大量動作工具列中，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**。

1. 在[!UICONTROL Upload Bulksheet]對話方塊：

   1. 將檔案拖放至方塊中，或按一下方塊內部，從您的裝置或網路選取檔案。

   1. 按一下&#x200B;**[!UICONTROL Upload]**。

1. （選擇性）若要確認已處理更新，請按一下頂端功能表列右側的![工作](/help/dsp/assets/downloads.png)。

當任何設定更新失敗時，您可以下載帶有顏色編碼的批次工作表錯誤檔案，以顯示哪些設定（列）已儲存且失敗，以及每次失敗的原因。 然後，您可以在相同檔案中解決問題，並再次上傳它以處理更正的資訊。

<!--
## Placement Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded bulksheet, all editable columns are highlighted in blue.

### [!UICONTROL Placements] Sheet

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don't see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |

### [!UICONTROL Placement_AdSchedules] Sheet

| [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Placement Name] | The name of the placement. | &mdash; |
| [!UICONTROL Ad ID] | The numeric ID of the ad. | &mdash; |
| [!UICONTROL Ad Name] | The name of the ad. | Yes |
| [!UICONTROL Start Date] | The start date of the ad. | &mdash; |
| [!UICONTROL End Date] | The end date of the ad. | &mdash; |
| [!UICONTROL Adobe Ad Approval Status] | The status of the Advertising DSP approval process, such as *Approved* or *Incomplete*. | &mdash; |
| [!UICONTROL Flight 1 Start Date] - [!UICONTROL Flight 12 Start Date] | The start date for a specific flight. | Yes |
| [!UICONTROL Flight 1 End Date] - [!UICONTROL Flight 12 End Date] | The end date for a specific flight. | Yes |
| [!UICONTROL Flight 1 Weight] - [!UICONTROL Flight 12 Weight] | How to rotate a specific ad for a specific flight:  *Even* to rotate the ad evenly, or a relative weight by which to rotate the ad, as a percentage (such as `40` for 40%); the total weights for all ads in the flight must equal 100. | Yes |

### [!UICONTROL Placement_BidMultipliers] Sheet

*Available in campaign-level bulksheets only*

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL Country] | The bid multiplier and the name of the country, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL State] | The bid multiplier and the name of the state. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL City] | The bid multiplier and the name of the city, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL DMA] | (U.S. locations only) The bid multiplier and the designated market area, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL Postal code] | The bid multiplier and the postal code, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory Source] | The bid multiplier and the public inventory source, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory Feed] | The bid multiplier and the public inventory feed, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL OnDemand Inventory Source] | The bid multiplier and the OnDemand inventory source, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL OnDemand Inventory Feed] | The bid multiplier and the OnDemand inventory feed, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Sites/Apps] | [!UICONTROL Domains] | The bid multiplier and the domains, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Sites/Apps] | [!UICONTROL Category] | The bid multiplier and the site/app category, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Audience] | [!UICONTROL Daypart] | The bid multiplier and the daypart interval, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Audience] | [!UICONTROL Topics - Comscore] | The bid multiplier and the [!DNL Comscore] topics, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Ads.txt] | The bid multiplier and the level of [Ads.txt](https://iabtechlab.com/ads-txt-about/) pre-bid filtering to use, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |

-->

<!-- LOTS MORE THAN I HAD ORIGINALLY DOCUMENTED -- BELOW ARE THE LAST, BUT NOT ALL:

| Brand Safety | Brand Safety - Contextual Filtering # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Fraud blocking # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Viewability # |  |  |
| Brand Safety | Site Safety Block |  |  |
| Tracking | Tracking Pixels # |  |  |
| Tracking | Conversion Pixels # |  |  |
| Tracking | 3rd-party fees |  |  |
| # of Ads Attached |  |  |
| Ads |  Ad Names |  |  |
| Ads | Attached Ad ID |  |  |
| Environment | Environment |  |  |
-->

<!-- 
Check on Brand Safety - Contextual Filtering # with new DV feature/fct change.
-->

>[!MORELIKETHIS]
>
>* [使用Bulksheets檢閱和編輯Campaign元件設定](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [編輯版位](/help/dsp/campaign-management/placements/placement-edit.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
