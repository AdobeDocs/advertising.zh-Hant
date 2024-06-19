---
title: Campaign設定
description: 請參閱可用行銷活動設定的說明。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: d572a406be9271c6ca14d35740f04d15ddbf7364
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Campaign設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]：** 行銷活動名稱。

**[!UICONTROL Advertiser]：** （現有行銷活動的唯讀）適用的廣告商（品牌）。 選取現有廣告商或建立新廣告商。

**[!UICONTROL Advertiser URL]：** 廣告商的官方頁面。 此欄位可加快您與詳細目錄合作夥伴的廣告核准流程。

**[!UICONTROL Timezone]：** （現有行銷活動的唯讀）報告和競標的時區。

**[!UICONTROL Customer PO]：** （選擇性）插入訂單/採購單的客戶採購單。

**[促銷活動日期]：** 行銷活動的開始和結束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]：** 是否要管理行銷活動的邊界： *[!UICONTROL Yes]* 或 *[!UICONTROL No]* （預設）。

當您選擇 *[!UICONTROL Yes]，* 指定利潤型別和金額：

* **[!UICONTROL Margin Type]：** 邊界型別。 一旦啟用利潤管理並儲存行銷活動，您就無法變更利潤型別。

   * *[!UICONTROL Fixed]：* （預設值）允許DSP根據的固定利潤百分比自動計算和限制支出， [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]：* 可讓您透過指定個別的「 」來向下管理版位層級的邊界 [!UICONTROL Budget Reserve %] 和 [!UICONTROL Gross Budget] 行銷活動中的每個套件和位置。 DSP會根據每個位置的財務效率進行最佳化，而不保證特定利潤。 對於由多個明細行料號所組成的插入訂單，請使用此選項，您已同意以固定費率傳送固定數量的單位或單位型態。

* **[!UICONTROL Fixed Margin %]：** （僅具有固定邊界的行銷活動）每個插入順序的預設標籤 <!-- impression? -->，以百分比顯示。 此金額已從以下專案扣除： [!UICONTROL Gross Budget] 以定義淨促銷活動預算。

* **[!UICONTROL Budget Reserve %]：** （僅限固定邊界的行銷活動；選擇性）保留指定的百分比 [!UICONTROL Gross Budget] 作為安全保障。 此金額已從以下專案扣除： [!UICONTROL Gross Budget] 以定義淨促銷活動預算。

**[!UICONTROL Gross Budget]：** （僅限具有利潤管理的行銷活動）套用指定邊際調整前的行銷活動總預算。

您可以選擇新增額外的每日、每週或每月毛額預算：

1. 按一下 **[!UICONTROL Add an additional Gross Budget]**.

1. 輸入 **[!UICONTROL Gross Budget]** 並選取預算間隔： *[!UICONTROL Daily]，* *[!UICONTROL Weekly]，* 或 *[!UICONTROL Monthly]*.

系統會根據利潤設定自動計算總淨預算（即促銷活動的支出上限），並顯示在此值下方。

**[!UICONTROL Budget]：** （沒有利潤管理的行銷活動）整體行銷活動預算。

**[!UICONTROL Estimated Tax Withholding]：** 針對國家/地區或地方稅種，在帳戶層級預扣廣告費用、廣告服務費用和/或資料費用中的總支出百分比。 費率是預算編列與調整用途的估計值，因此開立商業發票的稅率可能有所不同。

若要預估要預扣的稅捐，請執行下列步驟：

1. 按一下 **[!UICONTROL Update rates here]**.

1. 指定 **[!UICONTROL Estimated tax rate]**，以百分比顯示。

1. 選取要預扣稅捐之各費用型態旁的核取方塊。 費用型別包括：

   * *[!UICONTROL Include estimated tax - ads fee]：* 適用於所有Advertising DSP媒體支出，包括促銷活動管理費用稅捐。

   * *[!UICONTROL Include estimated tax - ad serving fee]：* 適用於所有在Advertising DSP上的支出，媒體和資料除外。 不含行銷活動管理費用的稅項

   * *[!UICONTROL Include estimated tax - data fee]：* 套用至Advertising DSP上的所有資料支出。

1. 按一下 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 在美國，各州在包含廣告、廣告服務和資料的稅務費用方面可能有所不同。 若為其他國家中的組織，請納入所有三種型別的稅捐費用，以說明VAT。
>
>* 您也可以在帳戶的費用設定中設定這些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]：** （自2020年6月22日起建立的現有行銷活動為唯讀；2020年6月22日之前建立的行銷活動不適用） DSP鎖定廣告並套用頻率上限的層級： *相同裝置* 以裝置為目標或 *人員* 跨所有已知裝置鎖定使用者。 **注意：** 目標為通用ID的位置不提供跨裝置支援。

**[!UICONTROL Device Graph]：** （現有行銷活動的唯讀；僅具有以人物為基礎的跨裝置目標定位的行銷活動）用於跨裝置目標定位和頻率管理的裝置圖表：

* *[!UICONTROL LiveRamp - U.S. only]：* 跨裝置目標定位為$0.35 CPM的所有廣告商都可使用，此廣告商可在廣告中取得透過以下方式傳送的曝光數： [!DNL LiveRamp] 裝置圖表（也就是說，在目標對象區段中找不到裝置）。 您可以在位置層級設定跨裝置目標定位。

  此選項也可供所有廣告商使用，且不需支付任何費用，以進行頻率管理和歸因測量。

  跨裝置支援僅適用於以舊版ID為目標的位置，不適用於以通用ID為目標的位置(包括 [!DNL LiveRamps])。 通用ID的目標定位、頻率管理和歸因只會套用在ID層級。

**[!UICONTROL Frequency Cap]：** （選用）不重複裝置、通用ID或人員（視指定的而定）的次數 [!UICONTROL Cross Device Level] 和位置的 [!UICONTROL Targeting] 設定)，即可從行銷活動中提供廣告。 選項包括 *[!UICONTROL Unlimited]* 或每日、周或月的特定金額。

>[!NOTE]
>
> 您可以在行銷活動、封裝和位置層級設定頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Packages]：** 此 [套件](/help/dsp/campaign-management/packages/package-about.md) 以包含在行銷活動中。 選取現有的封裝和/或建立要包含的封裝。 如果您建立套裝程式，請參閱 [封裝設定](/help/dsp/campaign-management/packages/package-settings.md) 以取得詳細資訊。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>下列設定僅啟用測量和報告功能。 效能最佳化僅在套件和位置層級執行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]：** （選用）啟用 [!DNL IAS] 使用指定設定，測量並報告可檢視度、詐騙、品牌安全和對象驗證的相關資訊。 需額外付費。

* **[!UICONTROL Measure On]：** 要測量的存貨： *[!UICONTROL Display and VPAID video inventory]* （預設）或 *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >視訊可檢視度僅可在VPAID詳細目錄中測量。

* **[!UICONTROL IAS Account ID (AnID)]：** (有自己的廣告商 [!DNL IAS] 帳戶；選擇性)組織的 [!DNL IAS] 帳戶ID，其中 [!DNL IAS] 將直接開立使用帳單。

* **[!UICONTROL IAS Team ID]：** (有自己的廣告商 [!DNL IAS] 帳戶；選擇性)組織的團隊ID [!DNL IAS] 帳戶，其中 [!DNL IAS] 將直接開立使用帳單。 <!-- verify -->

**[!UICONTROL MOAT]：** （選用）啟用 [!DNL MOAT] 可檢視度、詐騙、品牌安全和對象驗證的測量與報告。 需額外付費。

#### 對象驗證

**[!UICONTROL comScore Campaign Ratings]：** （選用）啟用 [!DNL Comscore] 已驗證 [!DNL Campaign Ratings] 使用指定設定測量及報告對象驗證。 需額外付費。

* **[!UICONTROL Target Gender]：** 目標性別： *[!UICONTROL Both]* （預設）， *[!UICONTROL Male]*，或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]：** 目標的年齡範圍。 視需要使用左右滑桿來縮小範圍。

* **[!UICONTROL Target Country]：** （選用）要鎖定的國家/地區。 [!DNL Comscore] 衡量僅支援國家/地區的曝光數。

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]：** 啟用位置層級的追蹤 [!UICONTROL Attention Score] 量度(的加權平均數 [!DNL Adelaide] &quot;[!DNL Attention Units]」的閱聽)。 量度適用於所有位置型別，但不包括 [!DNL Roku] 連線電視、VPAID-only前段，以及不是播客的音訊。 DSP會自動附加JavaScript標籤至所有相關的創意內容，以及 [!DNL Adelaide] 會追蹤曝光資料並每天傳送給DSP。 您可以使用日期，以手動方式，將您的支出最佳化為具有較高關注度的刊登策略。

此 [!UICONTROL Attention Score] 欄位位於 [!UICONTROL Metrics] 報表區段；在 [!UICONTROL Campaigns]， [!UICONTROL Packages]、和 [!UICONTROL Placements] 檢視；以及在 [!UICONTROL Sites]， [!UICONTROL Ads]、和 [!UICONTROL Inventory] 的索引標籤 [位置詳細資料檢視](/help/dsp/campaign-management/reports/placement-details-view.md).

使用 [!DNL Adelaide] 測量用的區段會針對以下專案提供的廣告每次曝光產生CPM費用： [!DNL Adelaide] 測量標籤。 此費用與下列專案之費用不同 [位置層級關注目標定位](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]：** 啟用第一方可檢視度測量及報告，使用 [!DNL IAB Open Video Viewability (OpenVV)] 技術，根據指定的敏感度等級：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [關於Campaign Management](campaign-about.md)
>* [建立行銷活動](campaign-create.md)
>* [編輯行銷活動](campaign-edit.md)
>* [檢視行銷活動的變更記錄](campaign-change-log.md)
