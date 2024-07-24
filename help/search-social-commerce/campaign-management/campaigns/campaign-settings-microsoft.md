---
title: '[!DNL Microsoft Advertising]行銷活動設定'
description: 參考 [!DNL Microsoft Advertising] 行銷活動的設定。
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: b8aa2461d261af50e1bf66c4ae29e4e453dfd182
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]行銷活動設定

## \[行銷活動建立畫面\]

**[!UICONTROL Campaign Type]：** （僅在行銷活動建立期間可用）廣告的放置位置以及廣告型別
行銷活動可能包含：

* *[!UICONTROL Search]：*&#x200B;在搜尋網路上顯示文字廣告。

* *[!UICONTROL Shopping Network]：*&#x200B;在購物網路上顯示產品廣告 — 針對您[!DNL Microsoft Merchant Center]產品目錄中的產品。

* *[!UICONTROL Audience]：*&#x200B;在[!DNL Microsoft Audience Network]上顯示原生/顯示廣告。 您可以a)將行銷活動連結至[!UICONTROL Shopping Settings]區段中的商家中心商店，以自動產生摘要型廣告，或b)使用文字資產和上傳的影像建立回應式廣告。 這兩個選項都需要您以使用者目標定位來建立廣告群組。

* *[!UICONTROL Shopping Campaigns for Brands]：*&#x200B;透過所有搜尋和受眾網路的連結零售商，推廣您的產品。 您可以建立子廣告群組和產品群組（要促銷的應用程式），以及促銷活動的選用產品廣告；[!DNL Microsoft Advertising]會自動為產品群組建立廣告。 若為品牌的購物促銷活動，請使用競標策略[!UICONTROL Manual CPC]；若為品牌的購物促銷活動，請使用競標策略[!UICONTROL Cost per Sale]。

* *[!UICONTROL Microsoft Store Ads Campaign]：*&#x200B;推廣您在[!DNL Microsoft Store]中可用的應用程式和遊戲。 您可以為行銷活動建立子廣告群組、產品群組和選用產品廣告；[!DNL Microsoft Advertising]會自動為產品群組建立廣告。

* *[!UICONTROL Audience CTV Video]：*&#x200B;在對象網路上顯示連線電視(CTV)視訊廣告。

* *[!UICONTROL Audience Video]：*&#x200B;在對象網路上顯示標準視訊廣告。

* *[!UICONTROL Performance Max]：*&#x200B;使用[!DNL Microsoft Advertising]智慧型出價顯示所有網路上的多個廣告型別。 在行銷活動設定中，您必須指定一或多個資產群組，包括影像、標誌、標題、說明、選用的行動號召和受眾訊號。 廣告網路會自動結合資產，以根據頻道提供廣告。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：**&#x200B;帳戶中唯一的促銷活動名稱。 長度上限為128個字元。

**[!UICONTROL Status]：**&#x200B;行銷活動的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新廣告行銷活動的預設值為&#x200B;*作用中*。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：**&#x200B;行銷活動的競標策略：

* *[!UICONTROL Cost per Sale]：* （僅限購物行銷活動）廣告網路(而非Search、Social和Commerce)會根據[!UICONTROL Target CPS] （每次銷售成本）最佳化出價。 您只會在產品廣告點選後，於24小時內完成銷售後才付款。 **注意：**&#x200B;請勿在產品組合中包含採用此競標策略的行銷活動。 搜尋、社交和Commerce最佳化不適用於具有此競標策略的行銷活動。

  一旦您儲存具有此競標策略的品牌的購物行銷活動，您就無法變更競標策略。 對於其他購物行銷活動型別，此策略僅適用於新行銷活動。

* *[!UICONTROL CPV]* （僅限對象CTV視訊行銷活動）使用每次檢視成本(CPV)模型。 搜尋、Social和Commerce未針對採用此競標策略、且包含在產品組合中的行銷活動提供最佳化。

* *[!UICONTROL Enhanced CPC]：* （對象、搜尋和購物網路的行銷活動）使用廣告網路的增強型每次點按成本(eCPC)模型，此模型可讓廣告網路自動變更每個拍賣的每次點按成本(CPC)競標，以嘗試使用廣告網路內指定的轉換(不在「搜尋」、「社交」和「Commerce」中)，來最大化轉換率，同時嘗試將平均CPC保持在最大CPC以下。

  當您將具有eCPC的行銷活動新增到最佳化的搜尋、社交和Commerce產品組合時，搜尋、社交和Commerce會最佳化基本競標，並且在啟用「[!UICONTROL Auto adjust campaign budget limits]」選項時最佳化行銷活動預算。 廣告網路會最佳化所有競標調整，並可能會在使用者查詢時根據專有資料和深入分析變更搜尋、社交和Commerce產生的競標。 **警告：**&#x200B;只有當廣告網路上的追蹤轉換總數符合產品組合目標時，才會在產品組合中使用eCPC行銷活動。

* *[!UICONTROL Manual CPC]*： （品牌的購物行銷活動； [!DNL Microsoft Store Ads]個行銷活動；其他行銷活動型別已棄用）使用每次點按成本(CPC)模型。 對於某些廣告型別，您可以選擇允許廣告網路變更行銷活動的競標：

   * **[!UICONTROL Enable Enhanced CPC]** （預設為停用）：此選項與使用&quot;[!UICONTROL Enhanced CPC]&quot;選項相同。

* *[!UICONTROL Manual CPA]：* （[!DNL Microsoft Store Ads]個行銷活動）使用每次贏取成本(CPA)模型。

* *[!UICONTROL Manual CPM]* （僅限對象行銷活動和對象視訊行銷活動）使用每千次曝光成本(CPM)模型，您可針對此模型指定每1,000次檢視曝光的支出專案。 當具有此競標策略的行銷活動包含在產品組合中時，系統不會最佳化。

* *[!UICONTROL Maximize Clicks]：* （搜尋和購物行銷活動）廣告網路(而非Search、Social和Commerce)會最佳化競標，以將點按次數最大化。 選擇性地輸入&#x200B;**[!UICONTROL Max CPC]** （每次點按成本），以確保廣告網路不會為每次點按支付超過特定金額的金額。 **警告：**&#x200B;當您將此策略的行銷活動新增至產品組合時，點按權重（不是產品組合目標）會驅動出價。

* *[!UICONTROL Maximize Conversion Value]：* （搜尋和購物/智慧型購物網路、最高成效行銷活動）廣告網路(而非Search、Social和Commerce)會最佳化競標，以將轉換價值最大化。 選擇性地輸入&#x200B;**[!UICONTROL Target Return on Ad Spend]** (ROAS)作為百分比。 **注意：**&#x200B;此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。 在混合專案組合中，「搜尋」、「社交」和「Commerce」會最佳化Target ROAS。

* *[!UICONTROL Maximize Conversions]：* (搜尋網路或對象網路上的最高成效行銷活動和行銷活動（但對象視訊或連線電視除外）)廣告網路(而非Search、Social和Commerce)會最佳化競標，以最大化轉換次數。 選擇性地輸入&#x200B;**[!UICONTROL Target CPC]** （每次點按成本）。 針對對象行銷活動，您也可以輸入選用的&#x200B;**[!UICONTROL Target CPA]** （每次贏取成本）。 **注意：**&#x200B;此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。 在混合專案組合中，「搜尋」、「社交」和「Commerce」會最佳化Target CPA。

* *[!UICONTROL Target CPA]：* （搜尋網路上的行銷活動）廣告網路(不是Search、Social和Commerce)會根據選擇性的&#x200B;**[!UICONTROL Target CPA]** （每次贏取成本）來最佳化競標，這是您想要為贏取（轉換）支付的30天平均金額。 **注意：**&#x200B;將此選項用於具有任何支出策略（除了[!UICONTROL Weekly]或[!UICONTROL Google Target CPA]）的混合產品組合（而非標準產品組合）中的行銷活動。 在混合專案組合中，「搜尋」、「社交」和「Commerce」會最佳化Target CPA。

  使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

* *[!UICONTROL Target Impression Share]：* （搜尋網路上的行銷活動）廣告網路(而非Search、Social和Commerce)會最佳化競標，以實現目標曝光比重和廣告位置。 選擇性地輸入&#x200B;**[!UICONTROL Target Impression Share]**&#x200B;作為百分比、**[!UICONTROL Target Ad Position]**&#x200B;和&#x200B;**[!UICONTROL Max CPC]** （每次點按成本）。 **注意：**&#x200B;混合專案組合不支援此選項。

* *[!UICONTROL Target Return on Ad Spend]：* （搜尋和購物網路上的行銷活動）廣告網路(不是Search、Social和Commerce)會根據以百分比指定的您的&#x200B;**[!UICONTROL Target ROAS]** （廣告投資報酬率）來最佳化競標。 選擇性地輸入&#x200B;**[!UICONTROL Max CPC]** （每次點按成本），以確保廣告網路不會為每次點按支付超過特定金額的金額。 **注意：**&#x200B;將此選項用於具有任何支出策略（除了[!UICONTROL Weekly]或[!UICONTROL Google Target ROAS]）的混合產品組合（而非標準產品組合）中的行銷活動。 在混合專案組合中，「搜尋」、「社交」和「Commerce」會最佳化Target ROAS。

  使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動的國家/地區
促銷活動的產品已售出。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]：** （僅限對象行銷活動；選用）針對自動化摘要型廣告（而非回應式廣告）將行銷活動與特定商家中心商店連結。 選取此選項時，請指定[!UICONTROL Merchant ID]和[!UICONTROL Products]。 您需要為行銷活動建立廣告群組，但不需要建立廣告。

將行銷活動連結至商店並儲存設定後，您就無法變更此選項。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]：** （僅連結至商戶中心商店的對象行銷活動）要廣告的產品。 預設會選取&#x200B;*[!UICONTROL All products]*。 若要僅廣告具有特定屬性的產品，請選取&#x200B;*[!UICONTROL Filter products]*&#x200B;並指定最多七個產品維度和屬性組合，以便篩選您的產品。 所有指定的值都必須適用於廣告，才能在產品中顯示。 例如，若要顯示Acme寵物用品的廣告，您可以建立篩選器`Custom Label 1=animals`、`Category=pet supplies`和`Brand=Acme Pet Supplies`。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]：** （僅限最高成效行銷活動）廣告的語言，應符合您的廣告可以出現的網站語言。 [!DNL Microsoft Advertising]會根據各種訊號判斷使用者的語言，包括使用者的查詢、發行者的國家/地區以及使用者的語言設定。

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]：** （僅限顯示/原生網路的行銷活動；選擇性）您不想顯示廣告的顯示網路網站。 請輸入有效的URL，例如www.example.com。 若要指定多個字串，請以逗號分隔字串，或在個別行中輸入字串。

如需可用性相關資訊，請參閱Microsoft Advertising說明，以&quot;[防止廣告出現在特定網站](https://help.ads.microsoft.com/#apex/bae/en/14061/0)&quot;。

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]：** （僅適用於[!UICONTROL EF Redirect]）未實作

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] （每個資產群組）

**[!UICONTROL Asset Group Name]：**&#x200B;資產資料夾（資產群組）的名稱。

**[!UICONTROL Asset Group Status]：**&#x200B;資產群組的狀態： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

**[!UICONTROL Final URL]：**&#x200B;從資產群組建立的所有廣告的最終URL。

**[!UICONTROL Images]：**&#x200B;廣告的最多20個影像，包含至少一個正方形影像和一個橫向影像。 請參閱[[!DNL Microsoft Advertising] 影像指導方針](https://help.ads.microsoft.com/#apex/ads/en/60204/0)。 您可以上傳影像或從[!UICONTROL Asset Library]中選取影像 — 但無法在同一作業中同時選取兩者。

* 若要上傳影像：

   1. 在[!UICONTROL Upload from Device]標籤上，按一下&#x200B;**[!UICONTROL +]**&#x200B;並從您的裝置或網路選取影像。

   1. 對於每個影像：

      1. 選取外觀比例。

      1. 視需要拖曳並放置裁切方塊以選取影像的可檢視部分，並視需要調整影像的可檢視部分大小。

      1. （選擇性）選取其他外觀比例，並視需要為每個選取的外觀比例重新定位和調整影像大小。

         系統會為每個選取的外觀比例建立一個資產。

      1. 按一下&#x200B;**[!UICONTROL Proceed]**。

   1. 當您完成指定影像時，請按一下&#x200B;**[!UICONTROL Upload]**。

* 若要從您的[!UICONTROL Asset Library]選取影像，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取影像。

**[!UICONTROL Logos]：**&#x200B;至少一個標誌。 您最多可以包含五個。 請參閱[[!DNL Microsoft Advertising] 資產准則](https://help.ads.microsoft.com/#apex/ads/en/60204/0)。 您可以上傳影像或從[!UICONTROL Asset Library]中選取影像 — 但無法在同一作業中同時選取兩者。

* 若要上傳影像：

   1. 在[!UICONTROL Upload from Device]標籤上，按一下&#x200B;**[!UICONTROL +]**&#x200B;並從您的裝置或網路選取影像。

   1. 對於每個影像：

      1. 選取外觀比例。

      1. 視需要拖曳並放置裁切方塊以選取影像的可檢視部分，並視需要調整影像的可檢視部分大小。

      1. （選擇性）選取其他外觀比例，並視需要為每個選取的外觀比例重新定位和調整影像大小。

         系統會為每個選取的外觀比例建立一個資產。

      1. 按一下&#x200B;**[!UICONTROL Proceed]**。

   1. 當您完成指定影像時，請按一下&#x200B;**[!UICONTROL Upload]**。

* 若要從您的[!UICONTROL Asset Library]選取影像，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取影像。

**[!UICONTROL Headlines]：**&#x200B;至少有三個及最多15個簡短標題，每個標題最多30個字元。 您可以輸入文字或從[!UICONTROL Asset Library]中選取資產，但無法在同一作業中同時輸入文字或選取資產。

* 若要輸入文字，請執行下列動作：

   1. 在[!UICONTROL Enter Text]索引標籤上，輸入文字。

   1. （選擇性）若要新增其他文字字串，請按一下&#x200B;**[!UICONTROL + Add]**&#x200B;並輸入字串。

* 若要從您的[!UICONTROL Asset Library]中選取資產，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取資產。

**[!UICONTROL Long Headlines]：**&#x200B;至少有一個和最多5個長標題，每個標題最多90個字元。 您可以輸入文字或從[!UICONTROL Asset Library]中選取資產，但無法在同一作業中同時輸入文字或選取資產。

* 若要輸入文字，請執行下列動作：

   1. 在[!UICONTROL Enter Text]索引標籤上，輸入文字。

   1. （選擇性）若要新增其他文字字串，請按一下&#x200B;**[!UICONTROL + Add]**&#x200B;並輸入字串。

* 若要從您的[!UICONTROL Asset Library]中選取資產，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取資產。

**[!UICONTROL Descriptions]：**&#x200B;說明至少有兩個，最多五個，每個說明最多90個字元。 您可以輸入文字或從[!UICONTROL Asset Library]中選取資產，但無法在同一作業中同時輸入文字或選取資產。

* 若要輸入文字，請執行下列動作：

   1. 在[!UICONTROL Enter Text]索引標籤上，輸入文字。

   1. （選擇性）若要新增其他文字字串，請按一下&#x200B;**[!UICONTROL + Add]**&#x200B;並輸入字串。

* 若要從您的[!UICONTROL Asset Library]中選取資產，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取資產。

**[!UICONTROL Call to Action]：**&#x200B;要包含在廣告中的行動號召。 預設會選取&#x200B;*[!UICONTROL Act Now]*。

**[!UICONTROL Business Name]：**&#x200B;公司名稱，最多25個字元。 它不能包含指令碼、HTML或其他標籤語言。

**[!UICONTROL Audience Signal]：** （選用） [!DNL Microsoft Advertising]個對象，以作為行銷活動的對象訊號。 [!DNL Microsoft Advertising]機器學習模型會使用受眾來尋找類似的網頁瀏覽者來鎖定目標，也可能會向未指定為訊號的受眾顯示廣告，以協助您達成效能目標。 選擇最可能轉換的對象。

>[!NOTE]
>對象訊號與[廣告群組層級對象目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)不同。

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]：**&#x200B;可讓您指定另一個資產群組。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]：**&#x200B;是&#x200B;*[!UICONTROL Use account conversion goals for this campaign]* （預設）或&#x200B;*[!UICONTROL Use campaign specific conversion goals]*。 如果您選擇指定行銷活動的轉換目標，請從所有可用目標清單中選取目標。 **注意：**&#x200B;目標會每天同步處理，因此可能無法列出過去24小時內建立的目標。 若要更新清單，[請手動同步處理廣告網路資料](/help/search-social-commerce/campaign-management/campaigns/sync-network.md)。

>[!TIP]
>
>如果行銷活動是混合專案組合的一部分，最佳實務是使用符合專案組合目標中的轉換目標的行銷活動層級目標；包含其他轉換目標可能會影響專案組合績效。
>
> 不過，對於混合產品組合中您[將目標上傳至廣告網路](/help/search-social-commerce/tools/objective-upload-to-networks.md)的行銷活動，請在廣告網路的編輯器內（而非此處）執行下列動作： a)新增上傳的搜尋、社交和Commerce產品組合目標量度（以「O_ACS_OBJ」開頭）作為行銷活動的轉換目標，以及b)新增任何包含由[!DNL Microsoft Advertising]通用事件追蹤(UET)標籤追蹤的轉換的行銷活動目標，因為廣告網路追蹤的量度未上傳至具有目標的廣告網路。

>[!MORELIKETHIS]
>
>* [管理行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
