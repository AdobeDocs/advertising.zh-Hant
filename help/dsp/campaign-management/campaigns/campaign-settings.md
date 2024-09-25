---
title: Campaign設定
description: 請參閱可用行銷活動設定的說明。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Campaign設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]：**&#x200B;行銷活動名稱。

**[!UICONTROL Advertiser]：** （現有行銷活動的唯讀）適用的廣告商（品牌）。 選取現有廣告商或建立新廣告商。

**[!UICONTROL Advertiser URL]：**&#x200B;廣告商的官方頁面。 此欄位可加快您與詳細目錄合作夥伴的廣告核准流程。

**[!UICONTROL Timezone]：** （現有行銷活動的唯讀）報告和競標的時區。

**[!UICONTROL Customer PO]：** （選擇性）插入訂單/採購單的客戶採購單。

**[行銷活動日期]：**&#x200B;行銷活動開始和結束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]：**&#x200B;是否要管理行銷活動的利潤： *[!UICONTROL Yes]*&#x200B;或&#x200B;*[!UICONTROL No]* （預設值）。

當您選擇&#x200B;*[!UICONTROL Yes]，*&#x200B;時，請指定利潤型別和金額：

* **[!UICONTROL Margin Type]：**&#x200B;利潤型別。 一旦啟用利潤管理並儲存行銷活動，您就無法變更利潤型別。

   * *[!UICONTROL Fixed]：* （預設值）允許DSP根據[!UICONTROL Gross Budget]的固定利潤百分比自動計算並限制支出。

   * *[!UICONTROL Dynamic]：*&#x200B;可讓您針對行銷活動中的每個套件和位置指定個別的[!UICONTROL Budget Reserve %]和[!UICONTROL Gross Budget]，以管理至位置層級的邊界。 DSP會根據每個位置的財務效率進行最佳化，而不保證特定利潤。 對於由多個明細行料號所組成的插入訂單，請使用此選項，您已同意以固定費率傳送固定數量的單位或單位型態。

* **[!UICONTROL Fixed Margin %]：** （僅具有固定邊界的行銷活動）每個插入訂單<!-- impression? -->的預設加成（以百分比表示）。 此金額已從[!UICONTROL Gross Budget]中扣除，以定義淨行銷活動預算。

* **[!UICONTROL Budget Reserve %]：** （只有固定邊界的行銷活動；選擇性）保留[!UICONTROL Gross Budget]的指定百分比作為保護。 此金額已從[!UICONTROL Gross Budget]中扣除，以定義淨行銷活動預算。

**[!UICONTROL Gross Budget]：** （僅具有利潤管理的行銷活動）套用指定邊際調整前的行銷活動預算總額。

您可以選擇新增額外的每日、每週或每月毛額預算：

1. 按一下&#x200B;**[!UICONTROL Add an additional Gross Budget]**。

1. 輸入&#x200B;**[!UICONTROL Gross Budget]**&#x200B;並選取預算間隔： *[!UICONTROL Daily]、* *[!UICONTROL Weekly]、*&#x200B;或&#x200B;*[!UICONTROL Monthly]*。

系統會根據利潤設定自動計算總淨預算（即促銷活動的支出上限），並顯示在此值下方。

**[!UICONTROL Budget]：** （沒有利潤管理的行銷活動）整體行銷活動預算。

**[!UICONTROL Estimated Tax Withholding]：**&#x200B;在帳戶層級針對國家/地區或當地稅捐預扣全部廣告費用、廣告服務費用及/或資料費用的支出百分比。 費率是預算編列與調整用途的估計值，因此開立商業發票的稅率可能有所不同。

若要預估要預扣的稅捐，請執行下列步驟：

1. 按一下&#x200B;**[!UICONTROL Update rates here]**。

1. 以百分比指定&#x200B;**[!UICONTROL Estimated tax rate]**。

1. 選取要預扣稅捐之各費用型態旁的核取方塊。 費用型別包括：

   * *[!UICONTROL Include estimated tax - ads fee]：*&#x200B;適用於所有Advertising DSP媒體支出，包括行銷活動管理費用的稅捐。

   * *[!UICONTROL Include estimated tax - ad serving fee]：*&#x200B;適用於Advertising DSP的所有支出，媒體和資料除外。 不含行銷活動管理費用的稅項

   * *[!UICONTROL Include estimated tax - data fee]：*&#x200B;適用於Advertising DSP上的所有資料支出。

1. 按一下&#x200B;**[!UICONTROL Submit]**。

>[!NOTE]
>
>* 在美國，各州在包含廣告、廣告服務和資料的稅務費用方面可能有所不同。 若為其他國家中的組織，請納入所有三種型別的稅捐費用，以說明VAT。
>
>* 您也可以在帳戶的費用設定中設定這些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]：** （自2020年6月22日以來建立的現有行銷活動為唯讀；不適用於2020年6月22日之前建立的行銷活動）DSP鎖定廣告並套用頻率上限的層級： *相同裝置*&#x200B;以鎖定裝置為目標，或&#x200B;*人物*&#x200B;以所有已知裝置上的人員為目標。 **注意：**&#x200B;目標為通用ID的位置不提供跨裝置支援。

**[!UICONTROL Device Graph]：** （現有行銷活動的唯讀；僅具有以人物為基礎的跨裝置目標定位的行銷活動）用於跨裝置目標定位和頻率管理的裝置圖表：

* *[!UICONTROL LiveRamp - U.S. only]：*&#x200B;對於使用[!DNL LiveRamp]裝置圖表所傳遞的曝光數（亦即目標受眾區段中找不到的裝置），跨裝置目標定位為$0.35 CPM的所有廣告商都可使用。 您可以在位置層級設定跨裝置目標定位。

  此選項也可供所有廣告商使用，且不需支付任何費用，以進行頻率管理和歸因測量。

  跨裝置支援僅適用於以舊版ID為目標的位置，不適用於以通用ID （包括[!DNL LiveRamps]）為目標的位置。 通用ID的目標定位、頻率管理和歸因只會套用在ID層級。

**[!UICONTROL Frequency Cap]：** （選擇性）從行銷活動中提供不重複裝置、通用ID或人員（視指定的[!UICONTROL Cross Device Level]和位置的[!UICONTROL Targeting]設定而定）的次數。 選項包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每日、每週或每月的特定金額。

>[!NOTE]
>
> 您可以在行銷活動、封裝和位置層級設定頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Packages]：**&#x200B;要包含在行銷活動中的[套件](/help/dsp/campaign-management/packages/package-about.md)。 選取現有的封裝和/或建立要包含的封裝。 如果您建立封裝，請參閱[封裝設定](/help/dsp/campaign-management/packages/package-settings.md)的說明，以取得詳細資訊。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>下列設定僅啟用測量和報告功能。 效能最佳化僅在套件和位置層級執行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]：** （選擇性）使用指定的設定，啟用[!DNL IAS]可檢視度、詐騙、品牌安全和對象驗證的測量與報告。 需額外付費。

* **[!UICONTROL Measure On]：**&#x200B;要測量的詳細目錄： *[!UICONTROL Display and VPAID video inventory]* （預設）或&#x200B;*[!UICONTROL Display, VPAID & VAST video inventory]*。

  >[!NOTE]
  >
  >視訊可檢視度僅可在VPAID詳細目錄中測量。

* **[!UICONTROL IAS Account ID (AnID)]：** （具有自己[!DNL IAS]帳戶的廣告商；選擇性）組織的[!DNL IAS]帳戶識別碼，[!DNL IAS]將直接針對使用收費。

* **[!UICONTROL IAS Team ID]：** （具有自己[!DNL IAS]帳戶的廣告商；選擇性）組織[!DNL IAS]帳戶的團隊識別碼，[!DNL IAS]將直接針對使用收費。<!-- verify -->

#### 對象驗證

**[!UICONTROL Comscore Campaign Ratings]：** （選擇性）使用指定的設定，啟用[!DNL Comscore]已驗證的[!DNL Campaign Ratings]對象驗證測量與報告。 需額外付費。

* **[!UICONTROL Target Gender]：**&#x200B;目標的性別： *[!UICONTROL Both]* （預設）、*[!UICONTROL Male]*&#x200B;或&#x200B;*[!UICONTROL Female]*

* **[!UICONTROL Target Age]：**&#x200B;目標期限範圍。 視需要使用左右滑桿來縮小範圍。

* **[!UICONTROL Target Country]：** （選擇性）目標國家/地區。 [!DNL Comscore]只測量支援國家/地區的曝光數。

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]：**&#x200B;啟用位置層級[!UICONTROL Attention Score]量度的追蹤（各曝光的[!DNL Adelaide] &quot;[!DNL Attention Units]&quot;加權平均數）。 除了[!DNL Roku]個連線電視、僅限VPAID的影片前段和非播客的音訊之外，所有版位型別都能使用量度。 DSP會自動附加JavaScript標籤至所有相關的創意內容，[!DNL Adelaide]會追蹤曝光資料並每天傳送給DSP。 您可以使用日期，以手動方式，將您的支出最佳化為具有較高關注度的刊登策略。

[!UICONTROL Attention Score]欄位可在報告的[!UICONTROL Metrics]區段中；在[!UICONTROL Campaigns]、[!UICONTROL Packages]和[!UICONTROL Placements]檢視中；以及在[位置詳細資料檢視](/help/dsp/campaign-management/reports/placement-details-view.md)的[!UICONTROL Sites]、[!UICONTROL Ads]和[!UICONTROL Inventory]索引標籤中。

使用[!DNL Adelaide]區段進行測量，將會針對含有[!DNL Adelaide]測量標籤的廣告所傳遞的每個曝光產生CPM費用。 此費用與[位置層級關注目標定位](/help/dsp/campaign-management/placements/placement-settings.md)的費用不同。

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]：**&#x200B;根據指定的敏感度等級，啟用使用[!DNL IAB Open Video Viewability (OpenVV)]技術的第一方可檢視度測量與報告：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [關於Campaign Management](campaign-about.md)
>* [建立行銷活動](campaign-create.md)
>* [編輯行銷活動](campaign-edit.md)
>* [檢視行銷活動的變更記錄](campaign-change-log.md)
