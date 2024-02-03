---
title: 『[!DNL Microsoft® Advertising] 行銷活動設定'
description: 參考設定 [!DNL Microsoft® Advertising] 行銷活動。
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 6b5c37b02191cf7097eb547f9ad58f347824579c
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] 行銷活動設定

## \[行銷活動建立畫面\]

**[!UICONTROL Campaign Type]：** （僅適用於建立行銷活動期間）廣告的放置位置，以及行銷活動可能包含的廣告型別：

* *[!UICONTROL Search]：* 在搜尋網路上顯示文字廣告。

* *[!UICONTROL Shopping Network]：* 顯示產品廣告 — 針對您產品在 [!DNL Microsoft® Merchant Center] 產品目錄 — 在購物網路上。

* *[!UICONTROL Audience]：* 在上顯示原生/顯示廣告 [!DNL Microsoft® Audience Network]. 您可以a)將行銷活動連結至中的商家中心商店，自動產生摘要型廣告 [!UICONTROL Shopping Settings] 或b)使用文字資產和上傳的影像建立回應式廣告。 這兩個選項都需要您以使用者目標定位來建立廣告群組。

* *[!UICONTROL Shopping Campaigns for Brands]：* （Beta版功能）透過搜尋和受眾網路中的連結零售商促銷您的產品。 您可以建立子廣告群組和產品群組（要促銷的應用程式），以及促銷活動的選用產品廣告； [!DNL Microsoft® Advertising] 自動為產品群組建立廣告。

* *[!UICONTROL Microsoft® Store Ads Campaign]：* （Beta版功能）推廣以下網站所提供的應用程式和遊戲： [!DNL Microsoft® Store]. 您可以為行銷活動建立子廣告群組、產品群組和可選產品廣告； [!DNL Microsoft® Advertising] 自動為產品群組建立廣告。

* *[!UICONTROL Audience CTV Video]：* （Beta版功能）在對象網路上顯示連線電視(CTV)視訊廣告。

* *[!UICONTROL Audience Video]：* （Beta版功能）在對象網路上顯示標準影片廣告。

* *[!UICONTROL Performance Max]：* （Beta版功能）顯示所有網路上的多種廣告型別。 在中個別指派資產群組 [!DNL Microsoft® Advertising] 廣告編輯器。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：** 帳戶中唯一的促銷活動名稱。 長度上限為128個字元。

**[!UICONTROL Status]：** 行銷活動的顯示狀態： *作用中* 或 *已暫停*. 新廣告行銷活動的預設為 *作用中*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：** 行銷活動的競標策略：

* *[!UICONTROL CPV]* （僅限對象CTV視訊行銷活動）使用每次檢視成本(CPV)模型。 <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]：* （對象、搜尋和購物網路的行銷活動）使用廣告網路的增強型每次點按成本(eCPC)模型，此模型可讓廣告網路自動變更每個拍賣的每次點按成本(CPC)競標，以嘗試使用廣告網路內指定的轉換（而非搜尋、社交和商務），來最大化轉換率，同時嘗試將平均CPC保持在最大CPC以下。

  當您將具有eCPC的行銷活動新增到最佳化的搜尋、社交和商務產品組合時，搜尋、社交和商務會最佳化基本競標，並且 — [!UICONTROL Auto adjust campaign budget limits]&quot;選項已啟用 — 行銷活動預算。 廣告網路會最佳化所有競標調整，並可能會在使用者查詢時根據專有資料和深入分析變更搜尋、社交和商務產生的競標。 **注意：** 只有在廣告網路上追蹤的轉換總數與產品組合目標一致時，才可在產品組合中使用eCPC行銷活動。

* *[!UICONTROL Manual CPC]*：(品牌的購物行銷活動； [!DNL Microsoft Store Ads] 行銷活動；已棄用 [!DNL Microsoft® Advertising] 2021年其他促銷活動型別)使用每次點按成本(CPC)模型。 對於某些廣告型別，您可以選擇允許廣告網路變更行銷活動的競標：

   * **[!UICONTROL Enable Enhanced CPC]** （預設為停用）：這等同於使用&quot;[!UICONTROL Enhanced CPC]」選項。

* *[!UICONTROL Manual CPA]：* ([!DNL Microsoft Store Ads] 行銷活動)使用每次取得的成本(CPA)模型。

* *[!UICONTROL Manual CPM]* （僅限對象行銷活動和對象視訊行銷活動）使用每千次曝光成本(CPM)模型，您可針對此模型指定每1,000次檢視曝光的支出專案。 當具有此競標策略的行銷活動包含在產品組合中時，系統不會最佳化。

* *[!UICONTROL Maximize Clicks]：* （搜尋和購物行銷活動）廣告網路（而非Search、Social和Commerce）會最佳化競標以最大化點按次數。 選擇性地輸入 **[!UICONTROL Max CPC]** （每次點按成本），確保廣告網路不會為每次點按支付超過特定金額的費用。 **注意：** 當您將使用此策略的行銷活動新增到產品組合時，競標是由點按權重驅動，而不是由產品組合目標驅動。

* *[!UICONTROL Maximize Conversion Value]：* （搜尋和購物/智慧型購物網路、最高成效行銷活動）廣告網路（而非Search、Social和Commerce）會最佳化競標，以將轉換價值最大化。 選擇性地輸入 **[!UICONTROL Target Return on Ad Spend]** (ROAS)的百分比。 **注意：** 此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。

* *[!UICONTROL Maximize Conversions]：* (搜尋網路或對象網路上的最高成效行銷活動和行銷活動（但對象視訊或連線電視除外）)廣告網路（而非Search、Social和Commerce）會最佳化競標，以將轉換最大化。 選擇性地輸入 **[!UICONTROL Target CPC]** （每次點按成本）。 對於對象行銷活動，您也可以輸入選填欄位 **[!UICONTROL Target CPA]** （每次收購成本）。 **注意：** 此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。

* *[!UICONTROL Target CPA]：* （搜尋網路上的行銷活動）廣告網路（而非Search、Social和Commerce）會根據選購專案最佳化出價 **[!UICONTROL Target CPA]** （每次收購成本），這是您要為收購（轉換）支付的30天平均金額。 **注意：** 此選項用於混合產品組合（但不是標準產品組合）中具有任何支出策略的行銷活動，但 [!UICONTROL Weekly] 或 [!UICONTROL Google Target CPA].

  使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

* *[!UICONTROL Target Impression Share]：* （搜尋網路上的行銷活動）廣告網路（而非Search、Social和Commerce）會最佳化競標，以實現目標曝光比重和廣告位置。 選擇性地輸入 **[!UICONTROL Target Impression Share]** 以百分比表示， **[!UICONTROL Target Ad Position]**，和 **[!UICONTROL Max CPC]** （每次點按成本）。 **注意：** 混合專案組合不支援此選項。

* *[!UICONTROL Target Return on Ad Spend]：*  （搜尋和購物網路上的行銷活動）廣告網路（而非Search、Social和Commerce）會根據您的 **[!UICONTROL Target ROAS]** （廣告投資報酬率），以百分比指定。 選擇性地輸入 **[!UICONTROL Max CPC]** （每次點按成本），確保廣告網路不會為每次點按支付超過特定金額的費用。 **注意：** 此選項用於混合產品組合（但不是標準產品組合）中具有任何支出策略的行銷活動，但 [!UICONTROL Weekly] 或 [!UICONTROL Google Target ROAS].

  使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動產品銷售的國家/地區。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]：** （僅限對象行銷活動；選用）將行銷活動與特定商家中心商店連結，以提供自動化摘要型廣告，而非回應式廣告。 選取此選項時，請指定 [!UICONTROL Merchant ID] 和 [!UICONTROL Products]. 您需要為行銷活動建立廣告群組，但不需要建立廣告。

將行銷活動連結至商店並儲存設定後，您就無法變更此選項。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]：** （僅限連結至商戶中心商店的對象行銷活動）要廣告的產品。 根據預設， *[!UICONTROL All products]* 已選取。 若只要通告具有特定屬性的產品，請選取 *[!UICONTROL Filter products]* 並指定最多七種產品維度和屬性組合，以便篩選您的產品。 所有指定的值都必須適用於廣告，才能在產品中顯示。 例如，若要顯示Acme寵物用品的廣告，您可以建立篩選器 `Custom Label 1=animals`， `Category=pet supplies`、和 `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

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

**[!UICONTROL Negative Websites]：** （僅限顯示/原生網路上的行銷活動；選用）顯示網路上的網站（您不想要顯示廣告）。 請輸入有效的URL，例如www.example.com。 若要指定多個字串，請以逗號分隔字串，或在個別行中輸入字串。

如需可用性的相關資訊，請參閱Microsoft® Advertising說明»[防止廣告出現在特定網站上](https://help.ads.microsoft.com/#apex/bae/en/14061/0).」

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

**[!UICONTROL Track Product Group]：** (適用於 [!UICONTROL EF Redirect] 僅限)未實作

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]：** 是否要 *[!UICONTROL Use account conversion goals for this campaign]* （預設）或 *[!UICONTROL Use campaign specific conversion goals]*. 如果您選擇指定行銷活動的轉換目標，請從所有可用目標清單中選取目標。 **注意：** 目標每天都會同步處理，因此可能不會列出過去24小時內建立的目標。 若要更新清單， [手動同步處理廣告網路資料](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

如果行銷活動屬於產品組合的一部分，則使用與產品組合目標相同的轉換目標。 使用不同的轉換目標可能會影響產品組合績效。

>[!MORELIKETHIS]
>
>* [管理行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
