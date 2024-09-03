---
title: '[!DNL Google Ads]行銷活動設定'
description: 參考 [!DNL Google Ads] 行銷活動的設定。
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: c4fa1ffa1dd21b2889ea18cb6a1a7cdec477bcfe
workflow-type: tm+mt
source-wordcount: '2503'
ht-degree: 0%

---

# [!DNL Google Ads]行銷活動設定

## \[行銷活動建立畫面\]

**[!UICONTROL Campaign Type]：** （僅在行銷活動建立期間可用）廣告的放置位置以及廣告型別
行銷活動可能包含：

* *[!UICONTROL Search Network Only]：*&#x200B;在搜尋網路上顯示廣告，包括[!DNL Google]個搜尋結果，以及（選擇性）搜尋夥伴網站。 您必須指定每個廣告群組的關鍵字。

* *[!UICONTROL Search with Display Select]：*&#x200B;在搜尋網路上顯示廣告（包含[!DNL Google]個搜尋結果，並可選擇顯示搜尋夥伴網站），並可能顯示在顯示網路上的廣告。 無論行銷活動的競標策略為何，[!DNL Google Ads]在顯示網路上，都會使用自動競標選擇性地顯示您的廣告。 對於搜尋廣告，請指定每個廣告群組的關鍵字；對於顯示廣告，請指定位置，並選擇性地指定每個廣告群組的關鍵字。

* *[!UICONTROL Shopping Network]：*&#x200B;顯示[!DNL Google]根據您在[!DNL Google Shopping]上的[!DNL Google Merchant Center]中的產品自動產生的產品廣告、[!DNL Google]搜尋結果旁的區域（與文字廣告分開），以及（選擇性）搜尋合作夥伴網站。 您可以為行銷活動中的每個廣告群組指定要廣告的產品群組。

* *[!UICONTROL Display Network Only]：*&#x200B;在顯示網路上顯示廣告。 您必須為每個廣告群組指定位置，並可選擇指定關鍵字。

* *[!UICONTROL Performance Max]：*&#x200B;使用[!DNL Google Ads]智慧型出價顯示並最佳化跨管道廣告的轉換。 在行銷活動設定中，您必須指定一或多個資產群組，包括影像、標誌、標題、說明、選用影片和對象訊號。 [!DNL Google Ads]會自動結合資產，以根據頻道（例如[!DNL YouTube]、[!DNL Gmail]或[!DNL Search]）提供廣告。

  **附註：**

   * 只有必要的設定可供使用。 如需選擇性設定，請登入[!DNL Google Ads]編輯器。

   * 不支援[!DNL Google Merchant Center]產品摘要的連結。

   * 不支援列出群組。 若要管理和檢視清單群組的資料，請登入[!DNL Google Ads]編輯器。

   * 支援混合最佳化。 在行銷活動層級設定競標策略目標和行銷活動預算。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：**&#x200B;帳戶中唯一的促銷活動名稱。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]：**（僅限現有、唯讀的Gmail行銷活動）是否：

* *[!UICONTROL Target and Bid]*&#x200B;只對與目標對象相關聯且滿足廣告群組之任何其他目標的使用者顯示廣告。

* *[!UICONTROL Bid Only]：*&#x200B;若要顯示廣告，即使是未與目標對象相關聯的使用者，只要他們符合其他廣告群組層級的目標即可。 不過，您可以為特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。

**[!UICONTROL Status]：**&#x200B;行銷活動的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新廣告行銷活動的預設值為&#x200B;*作用中*。

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]：** （僅以搜尋網路為目標的行銷活動，包括購物行銷活動）節目
您在廣告網路的搜尋合作夥伴網路上的廣告。 依預設，此選項為*[!UICONTROL Off]*。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：**&#x200B;行銷活動的競標策略：

* *[!UICONTROL Enhanced CPC]：* （不適用於最高成效或現有的唯讀[!DNL Gmail]行銷活動）使用廣告網路的增強型每次點按成本(eCPC)模型，此模型可讓廣告網路自動變更每個拍賣的每次點按成本(CPC)競標，以嘗試使用廣告網路內指定的轉換(不在「搜尋」、「社交」和「Commerce」中)，將平均每次點按成本(CPC)保持在最高CPC以下，藉此最大化轉換率。

當您將具有eCPC的行銷活動新增到最佳化的搜尋、社交和Commerce產品組合時，搜尋、社交和Commerce會最佳化基本競標，並且在啟用「[!UICONTROL Auto adjust campaign budget limits]」選項時最佳化行銷活動預算。 廣告網路會最佳化所有競標調整，並可能會在使用者查詢時根據專有資料和深入分析變更搜尋、社交和Commerce產生的競標。 **警告：**&#x200B;只有當廣告網路上的追蹤轉換總數符合產品組合目標時，才會在產品組合中使用eCPC行銷活動。<!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* （預設）： （不適用於最高成效行銷活動）使用每次點按成本(CPC)模型。 您可以選擇允許廣告網路變更行銷活動的競標：

   * **[!UICONTROL Enable Enhanced CPC]** （預設為停用）：這與使用&quot;[!UICONTROL Enhanced CPC]&quot;選項相同。

* *[!UICONTROL Maximize Clicks]：* （搜尋、顯示和購物行銷活動）廣告網路(而非Search、Social和Commerce)會最佳化競標，以將點按次數最大化。 選擇性地輸入&#x200B;**[!UICONTROL Max CPC]** （每次點按成本），以確保廣告網路不會為每次點按支付超過特定金額的金額。 **警告：**&#x200B;當您將此策略的行銷活動新增至產品組合時，出價是由點按權重驅動，而不是由產品組合目標驅動。

* *[!UICONTROL Maximize Conversion Value]：* （搜尋、最高成效和智慧型購物行銷活動）廣告網路(而非Search、Social和Commerce)會最佳化競標，以將轉換價值最大化。 選擇性地輸入&#x200B;**[!UICONTROL Target Return on Ad Spend]** (ROAS)作為百分比。 **注意：**&#x200B;此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。 在混合專案組合中，搜尋、Social和Commerce會最佳化行銷活動層級或（可用時）廣告群組層級的Target ROAS。

* *[!UICONTROL Maximize Conversions]：* （搜尋、顯示和效能最大化行銷活動）廣告網路(而非Search、Social和Commerce)會最佳化競標，以將轉換最大化。 選擇性地輸入&#x200B;**[!UICONTROL Target CPA]** （每次取得的成本）。 **注意：**&#x200B;此選項適用於混合專案組合中的行銷活動，但不適用於標準專案組合。 在混合專案組合中，「搜尋」、「社交」和「Commerce」會最佳化行銷活動層級或（可用時）廣告群組層級的目標CPA。

* *[!UICONTROL Target CPA]：* （顯示行銷活動）廣告網路(而非Search、Social和Commerce)會根據選擇性的&#x200B;**[!UICONTROL Target CPA]** （每次贏取成本）來最佳化競標，這是您想要為贏取（轉換）支付的30天平均金額。 **注意：**&#x200B;將此選項用於具有任何支出策略（除了[!UICONTROL Weekly]或[!UICONTROL Google Target CPA]）的混合產品組合（而非標準產品組合）中的行銷活動。 在混合專案組合中，「搜尋」、「社交」和「Commerce」會最佳化行銷活動層級或（可用時）廣告群組層級的目標CPA。

  使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

* *[!UICONTROL Target Impression Share]：* （搜尋行銷活動）廣告網路(而非Search、Social和Commerce)會最佳化競標，以實現目標曝光比重和廣告位置。 選擇性地輸入&#x200B;**[!UICONTROL Target Impression Share]**&#x200B;作為百分比、**[!UICONTROL Target Ad Position]**&#x200B;和&#x200B;**[!UICONTROL Max CPC]** （每次點按成本）。 **注意：**&#x200B;投資組合不支援此選項。

* *[!UICONTROL Target Return on Ad Spend]：* （顯示和購物行銷活動）廣告網路(不是Search、Social和Commerce)會根據指定的百分比&#x200B;**[!UICONTROL Target ROAS]** （廣告投資報酬率）來最佳化競標。 **注意：**&#x200B;將此選項用於具有任何支出策略（除了[!UICONTROL Weekly]或[!UICONTROL Google Target ROAS]）的混合產品組合（而非標準產品組合）中的行銷活動。 在混合專案組合中，搜尋、Social和Commerce會最佳化行銷活動層級或（可用時）廣告群組層級的Target ROAS。

  使用此競標策略的行銷活動無法使用平均位置和CPC競標資料。

* *[!UICONTROL Viewable CPM]：* （僅限現有、唯讀的[!DNL Gmail]行銷活動）廣告網路(而非Search、Social和Commerce)僅針對測量為可檢視的廣告出價。 **注意：**&#x200B;任何型別的投資組合都不支援此策略的最佳化。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （僅限購物行銷活動；現有行銷活動為唯讀）行銷活動的國家/地區
促銷活動的產品已售出。 由於產品與目標國家/地區相關聯，此設定會決定行銷活動中要廣告的產品。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]：** （僅限購物行銷活動；廣告商已參與當地購物方案，在美國、英國、DE、FR、JP和AU有[!DNL Google Merchant Center]家商店；選擇性）允許[!DNL Google Ads]自動將您的當地詳細目錄資訊新增到Google.com上的購物廣告中。

**秘訣：**&#x200B;如果您使用此設定，請勿在[!UICONTROL Inventory Filter]設定中排除本機廣告。

**注意：**&#x200B;本機詳細目錄廣告需要[!DNL Google Merchant Center]的兩個額外摘要 — 一個包含您的本機產品資料，另一個包含您的本機產品詳細目錄。 請參閱[!DNL Google Ads]檔案以取得有關[本機購物廣告](https://www.google.com/retail/local-inventory-ads/)的詳細資訊。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]：** （僅限搜尋和顯示網路）行銷活動中廣告的一或多個目標語言。

[!DNL Google Ads]會根據使用者的[!DNL Google]語言設定或搜尋查詢、目前頁面或最近在[!DNL Google Display Network]檢視的頁面的語言，來決定使用者的語言。

**[!UICONTROL Location Targets]：**&#x200B;要納入或排除為目標的特定使用者地理位置。 依預設，會鎖定所有位置。 您可以在任意位置組合中包含和排除使用者。 排除專案一律會覆寫包含專案。

* 若要鎖定所有位置，請勿選取任何位置。

* 若要鎖定或排除特定位置：

   * （國家、州、大都市區域或城市）按一下&#x200B;**[!UICONTROL Location Target]** （![定位目標](/help/search-social-commerce/assets/location-target.png "定位目標")）並找出要包含和排除的位置：

      * 若要包含位置及其子位置，請按一下相鄰的圓圈，以顯示藍色核取記號（![包含](/help/search-social-commerce/assets/include.png "包含")）。

      * 若要排除位置，請按兩下鄰接的圓圈，以顯示紅色核取記號（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

      * 若要將位置展開至其子元件（例如美國的州、大都市區域或城市），請按一下位置名稱。

      * 若要搜尋位置，請在輸入欄位中輸入或貼上位置的前三個字元。 在搜尋結果中，按一下要包含的位置旁的&#x200B;**[!UICONTROL Include]**&#x200B;或要排除的位置旁的&#x200B;**[!UICONTROL Exclude]**。

   * （位址附近的位置；僅限包含的目標）按一下&#x200B;**[!UICONTROL Radius Target]** （![Radius目標](/help/search-social-commerce/assets/radius-target.png "Radius目標")），然後按一下&#x200B;**[!UICONTROL Address]**。 輸入位址及目標位址周圍半徑（以英里或公里為單位），然後按一下&#x200B;**[!UICONTROL Add]**。

   * （地理座標附近的位置；僅限包含的目標）按一下&#x200B;**[!UICONTROL Radius Target]** （![Radius目標](/help/search-social-commerce/assets/radius-target.png "Radius目標")），然後按一下&#x200B;**[!UICONTROL Coordinate]**。 輸入目標位置周圍的經緯度與半徑（以英里或公里為單位），然後按一下&#x200B;**[!UICONTROL Add]**。

* （若要為包含的目標地點新增競標調整）請輸入競標調整值：

* 0%：不調整此位置中廣告的競標。

* \[從–90%到300%\]的其他值：增加或減少此位置廣告的競標。

**附註：**

* 搜尋、社交和Commerce不提供下列位置目標的自動調整競標調整，因為[!DNL Google Ads]提供將瀏覽者位置對應至位置目標的資料存在限制：

   * 半徑目標。

   * 某些位於州/省/地區/縣/州層級以下的位置，[!DNL Google Ads]不會傳送瀏覽者URL中的上層位置，包括機場和美國國會選區。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]：** （僅限顯示網路）要定位的特定行動電信業者；電信業者已排序
依國家/地區。 如果您未選取任何專案，則會鎖定所有專案。

**[!UICONTROL Mobile Carriers]：** （僅限顯示網路）要鎖定目標的特定作業系統。 如果您未選取任何專案，則會鎖定所有專案。

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

**[!UICONTROL Track Product Group]：** （僅適用於[!UICONTROL EF Redirect]）未實作

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] （每個資產群組）

**[!UICONTROL Asset Group Name]：**&#x200B;資產群組的名稱。 不支援[!DNL Google Merchant Center]產品摘要的連結。

**[!UICONTROL Asset Group Status]：**&#x200B;資產群組的狀態： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

**[!UICONTROL Final URL]：**&#x200B;從資產群組建立的所有廣告的最終URL。<!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]：**&#x200B;廣告的最多15個影像，包括下列大小： 1)至少三個正方形影像、2)至少三個橫向影像，以及3)至少一個直向影像。 請參閱[[!DNL Google Ads] 影像規格](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications)。 您可以上傳影像或從[!UICONTROL Asset Library]中選取影像 — 但無法在同一作業中同時選取兩者。

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

**[!UICONTROL Logos]：**&#x200B;至少一個正方形(1:1)標誌和一個橫向(4:1)標誌。 每個大小最多可包含5個。 檢視[[!DNL Google Ads] 標誌規格](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications)。 您可以上傳影像或從[!UICONTROL Asset Library]中選取影像 — 但無法在同一作業中同時選取兩者。

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

**[!UICONTROL Videos]：** （選用）長度至少10秒的至少一個、最多5個[!DNL YouTube]影片。 您可以輸入URL或從[!UICONTROL Asset Library]中選取URL — 但無法在同一作業中同時選取兩者。

* 若要輸入URL：

   1. 在[!UICONTROL Enter Video Url]標籤上，輸入URL。

   1. （選擇性）若要新增其他URL，請按一下&#x200B;**[!UICONTROL + Add]**&#x200B;並輸入URL。

* 若要從您的[!UICONTROL Asset Library]選取視訊，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取視訊。

**[!UICONTROL Headlines]：**&#x200B;至少有三個及五個簡短標題，每個標題最多30個字元。 至少一個標題必須至少為15個字元或更少。 如果啟用URL最終擴充的行銷活動層級選項設定在[!DNL Google Ads]內，則[!DNL Google Ads]會根據登入頁面內容，以自訂標題取代此值。

您可以輸入文字或從[!UICONTROL Asset Library]中選取資產，但無法在同一作業中同時輸入文字或選取資產。

* 若要輸入文字，請執行下列動作：

   1. 在[!UICONTROL Enter Text]索引標籤上，輸入文字。

   1. （選擇性）若要新增其他文字字串，請按一下&#x200B;**[!UICONTROL + Add]**&#x200B;並輸入字串。

* 若要從您的[!UICONTROL Asset Library]中選取資產，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取資產。

**[!UICONTROL Long Headlines]：**&#x200B;至少有一個和最多5個長標題，每個標題最多90個字元。 您可以輸入文字或從[!UICONTROL Asset Library]中選取資產，但無法在同一作業中同時輸入文字或選取資產。

* 若要輸入文字，請執行下列動作：

   1. 在[!UICONTROL Enter Text]索引標籤上，輸入文字。

   1. （選擇性）若要新增其他文字字串，請按一下&#x200B;**[!UICONTROL + Add]**&#x200B;並輸入字串。

* 若要從您的[!UICONTROL Asset Library]中選取資產，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取資產。

**[!UICONTROL Descriptions]：**&#x200B;說明至少有兩個，最多四個，每個說明最多90個字元。 至少一個說明必須至少為30個字元或更少。 您可以輸入文字或從[!UICONTROL Asset Library]中選取資產，但無法在同一作業中同時輸入文字或選取資產。

* 若要輸入文字，請執行下列動作：

   1. 在[!UICONTROL Enter Text]索引標籤上，輸入文字。

   1. （選擇性）若要新增其他文字字串，請按一下&#x200B;**[!UICONTROL + Add]**&#x200B;並輸入字串。

* 若要從您的[!UICONTROL Asset Library]中選取資產，請按一下&#x200B;**[!UICONTROL Asset Library]**&#x200B;並選取資產。

**[!UICONTROL Call to Action]：**&#x200B;要包含在廣告中的行動號召。 依預設，已選取&#x200B;*[!UICONTROL Automated]*，且[!DNL Google Ads]已選取呼叫動作。 您可以選擇不同的動作。

**[!UICONTROL Business Name]：**&#x200B;公司名稱，最多25個字元。

**[!UICONTROL Audience Signal]：** （選用） [!DNL Google Ads]個對象，以作為行銷活動的對象訊號。 [!DNL Google Ads]機器學習模型會使用受眾來尋找類似的網頁瀏覽者來鎖定目標，也可能會向未指定為訊號的受眾顯示廣告，以協助您達成效能目標。 選擇最可能轉換的對象。

>[!NOTE]
>對象訊號與[行銷活動層級和廣告群組層級的對象目標](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)不同。

**[!UICONTROL Primary Status]：** （最高成效行銷活動中現有資產群組的唯讀欄位）為何資產群組會或不會以完整容量提供服務。 它會考慮資產群組狀態以及其他訊號，例如原則和品質核准。 值可能包括&#x200B;*合格，* *有限，* *不適用，* *已暫停，* *擱置中，* *已移除，* *未知，*&#x200B;或未指定&#x200B;*未指定。*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]：** （最高成效行銷活動中現有資產群組的唯讀欄位）有關資產群組主要狀態的更多詳細資料。 值可能包括&#x200B;*ASSET_GROUP_DISAPPROVED，* *ASSET_GROUP_LIMITED，* *ASSET_GROUP_PAUSED，* *ASSET_GROUP_REMOVED，* *ASSET_GROUP_UNDER_REVIEW，* *CAMPAIGN_ENDED，* *CAMPAIGN_PAUSED，* ** {CAMPAIGN_REMOVED，**&#x200B;未知，*或未指定*。**

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]：**&#x200B;是&#x200B;*[!UICONTROL Use account conversion goals for this campaign]* （預設）或&#x200B;*[!UICONTROL Use campaign specific conversion goals]*。 如果您選擇指定行銷活動的轉換目標，請選取標準目標及/或建立行銷活動的自訂目標。

目標每天都會同步處理，因此可能不會列出過去24小時內建立的現有目標。 若要更新清單，[請手動同步處理廣告網路資料](/help/search-social-commerce/campaign-management/campaigns/sync-network.md)。

若要建立自訂轉換目標，請按一下&#x200B;**[!UICONTROL + Add custom goal]**、輸入自訂目標名稱、選取要包含在自訂目標中的[轉換動作](https://support.google.com/google-ads/answer/6032150)，然後按一下&#x200B;**[!UICONTROL Save]**。 **注意：**&#x200B;每個行銷活動只能有一個自訂目標。

>[!TIP]
>
>如果行銷活動是混合專案組合的一部分，最佳實務是使用符合專案組合目標中的轉換目標的行銷活動層級目標；包含其他轉換目標可能會影響專案組合績效。
>
>不過，對於混合產品組合中您[將目標上傳至廣告網路](/help/search-social-commerce/tools/objective-upload-to-networks.md)的行銷活動，請在廣告網路的編輯器中執行下列動作，而非這裡： a)新增上傳的搜尋、社交和Commerce產品組合目標量度（以「O_ACS_OBJ」開頭）作為行銷活動的轉換動作，以及b)新增任何包含[!DNL Google]追蹤轉換的行銷活動目標，因為廣告網路追蹤量度未上傳至具有目標的廣告網路。

>[!MORELIKETHIS]
>
>* [管理行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

