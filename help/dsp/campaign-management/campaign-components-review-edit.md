---
title: 使用Bulksheets檢閱和編輯Campaign元件設定
description: 瞭解如何使用試算表大量檢閱和編輯重要套件、位置和廣告設定。
feature: DSP Placements
exl-id: 1ec8362a-d37b-4fd7-becd-3a5b4f0c9504
source-git-commit: 7af6788f2aae3a2fb9e2048676dbe1955c2e56d9
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# 使用Bulksheets檢閱和編輯Campaign元件設定

您可以在XLSX （[!DNL Microsoft Excel]試算表）格式的單一行銷活動中下載套件、版位和廣告的設定，以檢閱和編輯設定。 根據預設，下載的檔案&#x200B;*大量表單*&#x200B;包含封裝設定、封裝航班資訊、位置設定和位置廣告排程的個別標籤。 您可以選擇排除某些行銷活動元件型別的設定。

若要一次更新多個設定，請上傳包含變更的有效Bulksheet檔案。 若要建立大量表單，請使用現有設定來編輯已下載的大量表單。 可編輯欄位包含大部分通常可編輯的設定。 未使用的設定欄位包含空白值。

>[!NOTE]
>
>您也可以僅下載及編輯特定套件和特定位置的設定。 請參閱[使用Bulksheets檢閱和編輯封裝設定](/help/dsp/campaign-management/packages/package-qa.md)和[使用Bulksheets檢閱和編輯位置設定](/help/dsp/campaign-management/placements/placement-qa.md)。

## 行銷活動中套件、版位和廣告的下載設定 {#download-bulksheet-campaign}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 在行銷活動旁邊，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

   * 按一下行銷活動名稱。 按一下右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

1. 在[!UICONTROL Bulksheet Download]對話方塊中，取消選取您要從下載檔案中排除其設定的任何促銷活動元件，然後按一下&#x200B;**[!UICONTROL Download]**。

依預設，會選取所有行銷活動元件的設定。

通知訊息會指出檔案何時可供下載。

1. 若要下載檔案，請執行下列任一項作業：

   * 在通知訊息中，按一下&#x200B;**[!UICONTROL Download].**

   * 在頂端功能表列的右側，按一下![工作](/help/dsp/assets/downloads.png)。 按一下工作旁的&#x200B;**[!UICONTROL Download]**。

     檔案已儲存至瀏覽器的[下載]資料夾。<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     若要編輯任何設定，請直接編輯檔案，然後上傳變更。 所有可編輯的欄都會以藍色反白。 若要針對欄位使用正確的格式，請從相關的封裝設定或位置設定中選取並複製值。 對於某些目標設定，例如時段、自訂目標和轉換量度，設定中提供了複製選項。

## 上傳含有行銷活動套件、位置和廣告設定的大量表單{#upload-bulksheet-campaign-components}

一次在填入的大量工作表中上傳單一行銷活動中套件、位置和廣告的設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 在行銷活動旁邊，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**。

   * 按一下行銷活動名稱。 按一下右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**。

1. 在[!UICONTROL Upload Bulksheet]對話方塊：

   1. 將檔案拖放至方塊中，或按一下方塊內部，從您的裝置或網路選取檔案。

   1. 按一下&#x200B;**[!UICONTROL Upload]**。

1. （選擇性）若要確認已處理更新，請按一下頂端功能表列右側的![工作](/help/dsp/assets/downloads.png)。

當任何設定更新失敗時，您可以下載帶有顏色編碼的批次工作表錯誤檔案，以顯示哪些設定（列）已儲存且失敗，以及每次失敗的原因。 然後，您可以在相同檔案中解決問題，並再次上傳它以處理更正的資訊。


<!--
## Placement Setting Columns in Downloaded/Uploaded Spreadsheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded spreadsheet, all editable columns are highlighted in blue.

### Campaign-level Spreadsheets

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
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Whether the Inventory Targeting option to exclude outstream traffic is <i[!UICONTROL >ON]* or *[!UICONTROL OFF]*.<br>Outstream ads usually appear over the content as a pop-up or stuffed into content (in the native experience), rather than as regular video ads in a video player. | &mdash; |
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
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |
-->

>[!MORELIKETHIS]
>
>* [使用Bulksheets檢閱及編輯封裝設定](/help/dsp/campaign-management/packages/package-qa.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [使用Bulksheets檢閱和編輯位置設定](/help/dsp/campaign-management/placements/placement-qa.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [連線電視設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [顯示廣告設定](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [行動廣告設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [原生顯示廣告設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [前段廣告設定](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [通用視訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
