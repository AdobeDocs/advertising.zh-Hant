---
title: '"[!DNL Google Ads] campaign設定」'
description: 參考設定 [!DNL Google Ads] 行銷活動。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1958'
ht-degree: 0%

---

# [!DNL Google Ads] 行銷活動設定

## \[行銷活動建立畫面\]

**[!UICONTROL Campaign Type]：** （僅在行銷活動建立期間提供）放置廣告的位置，以及行銷活動可能包含的廣告型別：

* *[!UICONTROL Search Network Only]：* 在搜尋網路上顯示廣告，包括 [!DNL Google] 搜尋結果和（選擇性）搜尋合作夥伴網站。 您必須為每個廣告群組指定關鍵字。

* *[!UICONTROL Search with Display Select]：* 在搜尋網路上顯示廣告(包括 [!DNL Google] 搜尋結果和（可選）搜尋合作夥伴網站)，並可能在顯示網路網站上顯示廣告。 在顯示網路上， [!DNL Google Ads] 無論行銷活動的競標策略為何，都會使用自動競標選擇性地顯示您的廣告。 對於搜尋廣告，您必須為每個廣告群組指定關鍵字；對於顯示廣告，您必須指定位置，並可選擇為每個廣告群組指定關鍵字。

* *[!UICONTROL Shopping Network]：* 顯示產品廣告，其中 [!DNL Google] 根據您的產品自動產生 [!DNL Google Merchant Center] 於 [!DNL Google Shopping]，旁的區域 [!DNL Google] 搜尋結果（與文字廣告分開）和（可選）搜尋合作夥伴網站。 您可以為行銷活動中的每個廣告群組指定要廣告的產品群組。

* *[!UICONTROL Display Network Only]：* 在顯示網路上顯示廣告。 對於每個廣告群組，您必須指定位置，並可選擇指定關鍵字。

* *[!UICONTROL Performance Max]：* （Beta版功能）使用顯示和最佳化跨管道廣告的轉換 [!DNL Google Ads] 智慧型競標。 在行銷活動設定中，您必須指定一或多個資產群組，包括影像、標誌、標題、說明、選用影片和受眾訊號。 [!DNL Google Ads] 自動結合資產，以根據管道提供廣告(例如 [!DNL YouTube]， [!DNL Gmail]，或 [!DNL Search])。

   **附註：**

   * 只有必要的設定可供使用。 如需可選設定，請登入 [!DNL Google Ads] 編輯者。

   * 連結至 [!DNL Google Merchant Center] 不支援產品摘要。

   * 不支援列出群組。 若要管理和檢視清單群組的資料，請登入 [!DNL Google Ads] 編輯者。

   * 支援混合最佳化。 競標策略目標和行銷活動預算是在行銷活動層級設定。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：** 帳戶中唯一的促銷活動名稱。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]：**（僅限現有唯讀Gmail行銷活動）是否：

* *[!UICONTROL Target and Bid]* 只向與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。

* *[!UICONTROL Bid Only]：*  即使未與目標對象相關聯的人，只要他們滿足其他廣告群組層級目標，也能顯示廣告。 不過，您可以針對特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。

**[!UICONTROL Status]：** 行銷活動的顯示狀態： *作用中* 或 *已暫停*. 新廣告行銷活動的預設為 *作用中*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]：** （僅以搜尋網路為目標的行銷活動，包括購物行銷活動）在廣告網路的搜尋合作夥伴網路上顯示您的廣告。 依預設，此選項為 *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：** 行銷活動的競標策略：

* *[!UICONTROL Enhanced CPC]：* (不適用於最高效能或現有的唯讀功能 [!DNL Gmail] 行銷活動)使用廣告網路的增強型每次點按成本(eCPC)模型，此模型可讓廣告網路自動變更每次拍賣的每次點按成本(CPC)競標，藉此嘗試使用廣告網路（而非搜尋、社交和商務）中指定的轉換，來最大化轉換，同時嘗試將平均CPC保持在最大CPC以下。

當您將具有eCPC的行銷活動新增到最佳化的搜尋、社交和商務產品組合時，搜尋、社交和商務會最佳化基本出價，而且 — 當「[!UICONTROL Auto adjust campaign budget limits]」選項已啟用 — 行銷活動預算。 廣告網路會最佳化所有競標調整，並可能根據專屬資料和深入分析，在使用者查詢時變更搜尋、社交和商務產生的競標。 **注意：** 只有在廣告網路上追蹤的總轉換率與產品組合目標一致時，才可在產品組合中使用eCPC行銷活動。 <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* （預設）： （不適用於最高成效行銷活動）使用每次點按成本(CPC)模型。 您可以選擇允許廣告網路變更行銷活動的競標：

   * **[!UICONTROL Enable Enhanced CPC]** （預設為停用）：這等同於使用&quot;[!UICONTROL Enhanced CPC]」選項。

* *[!UICONTROL Maximize Clicks]：* （搜尋、顯示和購物行銷活動）廣告網路（而非「搜尋、社交和商務」）會最佳化競標，以將點按次數最大化。 選擇性地輸入 **[!UICONTROL Max CPC]** （每次點按成本），以確保廣告網路不會為每次點按支付超過特定金額的費用。 **注意：** 當您將使用此策略的行銷活動新增到投資組合時，競標是由點選權重驅動，而不是由投資組合目標驅動。

* *[!UICONTROL Maximize Conversion Value]：* （搜尋、最高成效和智慧型購物行銷活動）廣告網路（而非Search、Social和Commerce）會最佳化競標，以將轉換價值最大化。 選擇性地輸入 **[!UICONTROL Target Return on Ad Spend]** (ROAS)的百分比。 **注意：** 此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。

* *[!UICONTROL Maximize Conversions]：* （搜尋、顯示和最高成效行銷活動）廣告網路（而非Search、Social和Commerce）會最佳化競標，以將轉換最大化。 選擇性地輸入 **[!UICONTROL Target CPA]** （每次收購成本）。 **注意：** 此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。

* *[!UICONTROL Target CPA]：* （顯示行銷活動；現有的搜尋行銷活動）廣告網路（而非Search、Social和Commerce）會根據選購專案最佳化出價 **[!UICONTROL Target CPA]** （每次收購成本），這是您要為收購（轉換）支付的30天平均金額。 **注意：** 此選項適用於混合專案組合（而非標準專案組合）中搭配任何支出策略的行銷活動，但下列情況除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target CPA].

   使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

   對於新的搜尋行銷活動， [!DNL Google Ads] 已將此競標策略取代為 [!UICONTROL Maximize Conversions] 策略使用 [!UICONTROL Target CPA] 值。 對於使用此策略的現有搜尋行銷活動，您只能編輯目標值，這樣做會將策略變更為 [!UICONTROL Maximize Conversions] 使用指定之策略 [!UICONTROL Target CPA] 值。

* *[!UICONTROL Target Impression Share]：* （搜尋行銷活動）廣告網路（而非Search、Social和Commerce）會最佳化競標，以實現目標曝光比重和廣告位置。 選擇性地輸入 **[!UICONTROL Target Impression Share]** 以百分比表示， **[!UICONTROL Target Ad Position]**，和 **[!UICONTROL Max CPC]** （每次點按成本）。 **注意：** 產品組合不支援此選項。

* *[!UICONTROL Target Return on Ad Spend]：*  （顯示和購物行銷活動；現有的搜尋行銷活動）廣告網路（而不是Search、Social和Commerce）會根據指定的最佳化競標 **[!UICONTROL Target ROAS]** （廣告投資報酬率），以百分比表示。 **注意：** 此選項適用於混合專案組合（而非標準專案組合）中搭配任何支出策略的行銷活動，但下列情況除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target ROAS].

   使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

   對於新的搜尋行銷活動， [!DNL Google Ads] 已將此競標策略取代為 [!UICONTROL Maximize Conversion Value] 策略使用 [!UICONTROL Target Return on Ad Spend value]. 對於使用此策略的現有搜尋行銷活動，您只能編輯目標值，這樣做會將策略變更為 [!UICONTROL Maximize Conversion Value] 使用指定之策略 [!UICONTROL Target Return on Ad Spend] 值。

* *[!UICONTROL Viewable CPM]：* (現有，唯讀 [!DNL Gmail] 僅限行銷活動)廣告網路（而非Search、Social和Commerce）僅對測量為可檢視的廣告投標。 **注意：** 任何型別的產品組合均不支援此策略的最佳化。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動產品銷售的國家/地區。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]：** (僅限購物行銷活動；已透過以下專案參與本地購物方案的廣告商： [!DNL Google Merchant Center] 位於美國、英國、DE、FR、JP和AU的商店；選購)允許 [!DNL Google Ads] 自動將您當地的詳細目錄資訊新增至Google.com上的購物廣告。

**秘訣：** 如果您使用此設定，請勿在中排除本機廣告 [!UICONTROL Inventory Filter] 設定。

**注意：** 本機詳細目錄廣告需要兩個額外的摘要，以 [!DNL Google Merchant Center]  — 一個包含您的本機產品資料，另一個包含您的本機產品詳細目錄。 請參閱 [!DNL Google Ads] 說明檔案，以瞭解更多關於 [本地購物廣告](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]：** （僅限搜尋和顯示網路）行銷活動中廣告的一或多個目標語言。

[!DNL Google Ads] 從使用者的語言決定使用者的語言 [!DNL Google] 語言設定或搜尋查詢、目前頁面或最近檢視頁面的語言 [!DNL Google Display Network].

**[!UICONTROL Location Targets]：** 要包含或排除為目標的特定使用者地理位置。 依預設，會鎖定所有位置。 您可以在任意位置組合中包含和排除使用者。 排除專案一律會覆寫包含專案。

* 若要鎖定所有位置，請勿選取任何位置。

* 若要鎖定或排除特定位置，請執行下列動作：

   * （國家、州、大都市區域或城市）按一下 **[!UICONTROL Location Target]** (![位置目標](/help/search-social-commerce/assets/location-target.png "位置目標"))並找到要包含和排除的位置：

      * 若要包含位置及其子位置，請按一下位置旁邊的圓圈，以使用藍色勾號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。

      * 若要排除某個位置，請按一下該位置旁邊的圓圈兩次，以使用紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

      * 若要將位置展開至其子元件（例如美國的州、大都會區域或城市），請按一下位置名稱。

      * 若要搜尋位置，請在輸入欄位中輸入或貼上位置的前三個字元。 在搜尋結果中，按一下 **[!UICONTROL Include]** 在要包含或的位置旁邊 **[!UICONTROL Exclude]** 在要排除的位置旁邊。
   * （位址附近的位置；僅限包含的目標）按一下 **[!UICONTROL Radius Target]** (![Radius目標](/help/search-social-commerce/assets/radius-target.png "Radius目標"))，然後按一下 **[!UICONTROL Address]**. 輸入位址和目標位址周圍的半徑（以英里或公里為單位），然後按一下 **[!UICONTROL Add]**.

   * （地理座標附近的位置；僅限包含的目標）按一下 **[!UICONTROL Radius Target]** (![Radius目標](/help/search-social-commerce/assets/radius-target.png "Radius目標"))，然後按一下 **[!UICONTROL Coordinate]**. 輸入目標位置周圍的經緯度和半徑（以英里或公里為單位），然後按一下 **[!UICONTROL Add]**.

   * (您的附近位置 [!DNL My Business] 可作為位置擴充功能使用的位置；僅限包含的目標)按一下 **[!UICONTROL Location Group Target]** (![位置群組](/help/search-social-commerce/assets/location-group.png "位置群組"))；選擇性地輸入國家、州、大都會區域或城市，在可用位置清單中向下箭頭；然後從清單中選取一或多個位置 [!DNL Google My Business] 位置。 指定目標位置周圍的半徑（以英里或公里為單位），然後按一下 **[!UICONTROL Add]**.


* （若要為包含的目標地點新增競標調整）輸入競標調整值：

* 0%：不調整此位置中廣告的競標。

* \[從–90%到300%\]的其他值：增加或減少此位置廣告的競標。

**注意：**

* 搜尋、Social和商務不提供下列位置目標的自動調整競標調整，因為資料中的限制會 [!DNL Google Ads] 提供將瀏覽者位置對應至位置目標的功能：

   * 半徑目標。

   * 州/省/地區/縣/州以下層級的一些位置 [!DNL Google Ads] 不會傳送瀏覽者URL中的上層位置，包括機場和美國國會選區。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]：** （僅限顯示網路）要鎖定的特定行動電信業者；電信業者會依國家/地區排序。 如果您未選取任何專案，則會鎖定所有專案。

**[!UICONTROL Mobile Carriers]：** （僅限顯示網路）目標的特定作業系統。 如果您未選取任何專案，則會鎖定所有專案。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

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

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

## [!UICONTROL Asset Groups] （每個資產群組）

**[!UICONTROL Asset Group Name]：** 資產群組的名稱。 連結至 [!DNL Google Merchant Center] 不支援產品摘要。

**[!UICONTROL Asset Group Status]：** 資產群組的狀態： *[!UICONTROL Active]* 或 *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]：** 從資產群組建立的所有廣告的最終URL。 <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]：** 廣告最多可包含15張影像，包括：1)至少三張正方形影像、2)至少三張橫向影像，以及3)至少一張縱向影像。 請參閱 [[!DNL Google Ads] 影像規格](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 若要上傳影像：

1. 對於每個影像：

   1. 按一下 **[!UICONTROL +]** 並從您的裝置或網路中選取影像。

   1. 選取長寬比。

   1. 視需要拖曳並放置裁切方塊，以選取影像的可檢視部分，然後按一下 **[!UICONTROL Proceed]**.

1. 完成指定影像時，請按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Logos]：** 至少一個正方形(1:1)標誌和一個橫向(4:1)標誌。 每種大小最多可包含五個檔案。 請參閱 [[!DNL Google Ads] 標誌規格](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 若要上傳影像：

1. 對於每個影像：

   1. 按一下 **[!UICONTROL +]** 並從您的裝置或網路中選取影像。

   1. 視需要拖曳並放置裁切方塊，以選取影像的可檢視部分，然後按一下 **[!UICONTROL Proceed]**.

1. 完成指定影像時，請按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Videos]：** （選用） URL至少要有一個，最多五個， [!DNL YouTube] 影片長度超過10秒。

**[!UICONTROL Headlines]：** 至少3個及最多5個簡短標題，每個標題最多30個字元。 至少一個標題必須至少為15個字元或更少。 如果啟用最終URL擴充的行銷活動層級選項設定於 [!DNL Google Ads]，則 [!DNL Google Ads] 以根據登陸頁面內容的自訂標題取代此值。

**[!UICONTROL Long Headlines]：** 至少一個，最多五個長標題，每個標題最多90個字元。

**[!UICONTROL Descriptions]：** 至少兩個（最多四個）說明，每個說明最多90個字元。 至少一個說明必須至少為30個字元或更少。

**[!UICONTROL Call to Action]：** 要包含在廣告中的行動號召。 依預設， *[!UICONTROL Automated]* 「 」已選取，並且 [!DNL Google Ads] 選取行動號召。 您可以選擇不同的動作。

**[!UICONTROL Business Name]：** 企業名稱，最多25個字元。

**[!UICONTROL Add new asset group]：** 可讓您指定其他資產群組。

>[!MORELIKETHIS]
>
>* [管理行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
