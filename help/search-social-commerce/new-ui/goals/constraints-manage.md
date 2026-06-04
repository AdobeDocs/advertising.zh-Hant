---
title: 管理搜尋競標單位的限制
description: 瞭解限制條件，以限制舊式關鍵字層級產品組合中CPC促銷活動競標單位的競標。
feature: Search Campaign Management, Search Optimization
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: c800239a-06eb-4249-9aef-771973d24d35
source-git-commit: 9cc395a6b0fe25435ca6ed022f8da767d525d68e
workflow-type: tm+mt
source-wordcount: 2660
ht-degree: 0%

---

# 管理搜尋競標單位的限制

*僅適用於舊版關鍵字層級產品組合中CPC行銷活動的競標單位*

競標單位限制是限制所有[競標單位](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html)的最佳化競標，以及與限制關聯的成本和收入模型的規則。

## 關於限制

每個限制都會套用至特定貨幣，並選擇性地包含在指定資料評估期間必須符合以套用規則的觸發條件。 要評估的資料可包括管道型別、比對型別、點選資料、轉換資料或衍生量度。 例如，您可以將出價限制在特定貨幣範圍內、以指定金額持續增加或減少出價，或根據投資組合的平均出價來出價。 每個限制都有適用的開始日期，且會在特定日期到期或無限期套用。

設定限制後，您可以將其指派給特定競標單位，或指派給特定廣告群組或促銷活動內的所有競標單位。 每個競標單位可以有一個限制。 限制由子實體繼承，但可以覆寫。 在最低層次指定的限制一律會覆寫在父層次指定的限制。 當您將限制指派給競標單位時，無論競標單位產生多少收入，當競標單位具有成本和收入模型時，競標都會在該競標單位的指定限制內運作。

>[!CAUTION]
>
>將限制指定給競標單位時，您會覆寫競標最佳化系統的決定，並自行承擔該競標單位的ROI責任。

>[!NOTE]
>
>* 作用中限制僅限制最佳化舊關鍵字層級產品組合中已指派競標單位的競標。 混合產品組合、作用中產品組合或不在產品組合中的競標單位會忽略它們。 **提示：**&#x200B;在產品組合設定中，開啟產品組合選項以「自動調整行銷活動預算限制」。 建議的「多個」值為「1」。
>* 若競標單位的資料不足，無法產生成本和收入模型，則會忽略競標限制。
>* （具有CPC或eCPC競標策略的行銷活動）當競標限制與產品組合層級競標限制衝突時，該限制會覆寫產品組合層級限制。 例如，如果產品組合的最低出價是5美元，但您限制產品組合中的出價單位為最低出價3美元，則出價單位將出價為3美元或更高。 不過，限制競標單位的整體支出是由產品組合的[「在限制周圍支出」引數](#spend-around-constraints)所決定。
>* 限制會根據基本競標運作。 對基本競標進行的任何競標調整型別（例如提高行動裝置上一般使用者的競標）都可將競標移到限制允許範圍之外。 例如，如果限制需要最大CPC為6美元，則基礎競標已經是6美元，而產品組合會自動最佳化行動裝置50%-60%的競標調整，則最大CPC為9.00-9.60美元，而不是6美元。

### 限制型別 {#constraint-types}

* **[!UICONTROL Bid]：**&#x200B;將競標限制在貨幣範圍。

* **[!UICONTROL Bid Shift]：**&#x200B;在競標範圍內，以指定數量持續變更所有關聯競標單位的最佳化競標。 出價轉換會導致相關的產品組合因出價轉換導致的總金額而過度或過少花費，無論產品組合的「在限制下花費」設定為何。 注意：如果目前的CPC競標已經等於或大於「最高競標」，或等於或小於「最低競標」，則限制會忽略且競標不會變更。 此外，如果沒有足夠的資料以產生成本和收入模型，競標班次限制不會套用至競標單位。

* **[!UICONTROL Incremental Bidding]：** （只適用於沒有曝光的關鍵字）以指定的速率遞增或遞減競標，直到競標達到指定的目標為止。

* **[!UICONTROL Search Engine Min Bid]：** （僅限[!DNL Google Ads]個帳戶）使用搜尋引擎決定的最小CPC出價作為您的最小出價。 當搜尋引擎變更其最低出價時，您的出價也會隨之變更。 您可以選擇為所有關聯的競標單位指定其他競標限制。

* **[!UICONTROL Impression Share]：** （僅具有完全相符專案的[!DNL Google Ads]和[!DNL Microsoft Advertising] CPC行銷活動）當廣告在最小和最大曝光分享之間時，將競標限制在貨幣範圍。 **注意：**&#x200B;當限制不具成本效益時，最佳化功能可能會覆寫它。

### 何時套用限制

限制競標單位的一些原因包括：

* 以快速公開未經測試的關鍵字和廣告。

* 降低新產品組合、帳戶、行銷活動和廣告群組的風險。 例如，在啟動產品組合之前，您可以設定高流量競標單位的最大競標，然後每天逐漸提高值。 這可讓競標模型每天調整，而不會有大幅競標增加的風險。

* 以確保轉換率高的尾部關鍵字不會降低競價。

* 提升品牌或促銷活動中重要的特定辭彙。

### 在UI中檢視限制相關資訊的位置

除了開啟[[!UICONTROL Constraints]檢視](#constraints-view)之外，您還可以透過下列方式檢視限制的相關資訊：

* 您所有的限制都是名為「[!UICONTROL Constraints]」的單一[標籤分類](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html)的標籤值。

   * &quot;[!UICONTROL Constraints]&quot;包含在預設和自訂檢視設定以及排程報告的&quot;[!UICONTROL Classifications]&quot;清單中。 您可以在想要檢視指定給相關圖元的限制的位置新增欄。

   * 當您下載大量表單時，[!UICONTROL Download Bulksheet]對話方塊中適用實體的[!UICONTROL Classifications]欄下會列出[!UICONTROL Constraints]。 當您包含欄時，下載的大量工作表會包含指定給相關圖元的任何限制。

  [!UICONTROL Constraints]分類未包含在[!UICONTROL Label Classifications]檢視中 — [!UICONTROL Constraints]檢視是獨立的。 [!UICONTROL Constraints]分類也不包含在30標籤分類限制中。

* [ [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)包含使用標籤分類架構之限制的成本、點選及（選擇性）轉換資料。

### [!UICONTROL Constraints]檢視 {#constraints-view}

[!UICONTROL Goals] > [!UICONTROL Constraints]檢視會列出所有限制。 可用欄包括限制狀態；限制型別、開始和結束日期；與限制關聯的促銷活動、廣告群組、關鍵字、廣告、位置、自動目標和產品群組的數量；曝光數、點按數和成本資料；以及所有可見轉換量度的收入資料。<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>[!UICONTROL Constraints]檢視中資料列的效能資料可能不符合指派限制之最上層實體的效能資料。 因為在最低層級指定的限制一律會覆寫在父層級指定的限制，所以指定給促銷活動或廣告群組的限制可能不會持續指定給子廣告群組和關鍵字。 例如，如果促銷活動A被指派為限制A，則促銷活動A中的所有廣告群組和關鍵字會自動繼承限制A。但是，這些廣告群組和關鍵字稍後可以指派給其他限制，例如「限制B」，然後它們就會失去與「限制A」的關聯。

>[!NOTE]
>
>從相關實體管理檢視（例如促銷活動層級限制的[!UICONTROL Campaigns]檢視），將限制指派給競標單位，以及取消指派。

#### 可用動作

* [建立限制](#constraint-create)。

* [編輯限制設定](#constraint-edit)。

* [變更條件約束的狀態](#constraint-change-status)。

## 建立限制 {#constraint-create}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Constraints]**。

1. 在資料表格上方的右上角工具列中，按一下&#x200B;**[!UICONTROL Create Constraint]**。

1. 輸入[限制設定](#constraint-settings)。

   若要在[!UICONTROL Constraint Type]標籤與[!UICONTROL Conditions]標籤之間移動，請按一下您要開啟的標籤，或按一下[!UICONTROL Next]與[!UICONTROL Back]按鈕。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**&#x200B;以檢閱設定。

1. 按一下&#x200B;**[!UICONTROL Save]**。

建立限制後，您可以[將其指派給促銷活動、廣告群組、關鍵字、位置及單位層級產品群組](#constraint-assign)。

## 編輯限制設定 {#constraint-edit}

您可以一次編輯一個限制的設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Constraints]**。

1. （選擇性）從工具列](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[欄標題](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)篩選清單[。

1. 選取要編輯的限制旁的核取方塊。

1. 在大量動作工具列中按一下![編輯](/help/search-social-commerce/assets/edit-new.png "編輯")。

1. 編輯[限制設定](#constraint-settings)。

   若要在[!UICONTROL Constraint Type]標籤與[!UICONTROL Conditions]標籤之間移動，請按一下您要開啟的標籤，或按一下[!UICONTROL Next]與[!UICONTROL Back]按鈕。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**&#x200B;以檢閱設定。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 變更限制的狀態 {#constraint-change-status}

您可以暫停任何作用中的限制以將其停用。 您稍後可以將其狀態變更回&#x200B;*作用中*，以啟用它。

您也可以刪除限制，這會移除與帳戶元件的所有關聯，並使限制無法供日後使用。 限制的報表資料已無法使用。 **注意：**&#x200B;若要將限制與帳戶元件解除關聯，請參閱[從搜尋競標單位取消指派限制](#constraints-unassign)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Constraints]**。

1. （選擇性）從工具列](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[欄標題](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)篩選清單[。

1. 選取每個要變更其狀態的限制旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中，按一下狀態按鈕：

   * 若要啟動所有選取的列，請按一下[啟動] ![ ](/help/search-social-commerce/assets/activate-new.png " ")。

   * 若要暫停所有選取的列，請按一下![暫停](/help/search-social-commerce/assets/pause-new.png "暫停")。

   * 若要刪除所有選取的列，請按一下[刪除]。![](/help/search-social-commerce/assets/delete-new.png "")

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 限制設定 {#constraint-settings}

| 標籤 | 引數 | 說明 |
|---|---|---|
| \[基本資訊\] | [!UICONTROL Constraint Name] | 限制的唯一名稱。 |
| | [!UICONTROL Currency] | 任何適用競標單位競標所使用的貨幣。 已使用不同貨幣的競標單位會被忽略。 |
| | [!UICONTROL Status] | 限制的狀態：<ul><li>**作用中：** （預設）條件約束會在指定的條件和日期範圍內套用。</li><li>**已暫停：**&#x200B;未套用條件約束。</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | 限制的型別。 如需限制型別與每個限制型別適用廣告網路的說明，請參閱[限制型別](#constraint-types)。 |
| | [!UICONTROL Start Date] | 限制生效的第一天。 預設為當天。 若要變更日期，請輸入日期或按一下![行事曆](/help/search-social-commerce/assets/calendar-new.png "行事曆")開啟行事曆並選取日期。 |
| | [結束日期] | 限制是否會在特定日期失效。 若要無限期套用限制（例如當競標單位是公司品牌的核心時），請將此欄位留空。 若要結束特定日期的限制，請輸入日期或按一下![行事曆](/help/search-social-commerce/assets/calendar-new.png "行事曆")開啟行事曆並選取日期。 **注意：**&#x200B;限制無法在明天之前到期。 |
| | [!UICONTROL Set constraint options for Bid] | （僅限[!UICONTROL Bid]個限制）設定包括：<ul><li>**[!UICONTROL Min Bid]：**&#x200B;相關競標單位的最低基礎競標。</li><li>**[!UICONTROL Max Bid]：**&#x200B;相關競標單位的最大基礎競標。</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | （僅限[!UICONTROL Bid Shift]個限制）要持續套用至基本競價的競標轉換型別和金額：<ul><li>*[!UICONTROL Increases]：*&#x200B;以指定的百分比或貨幣值增加競標。 輸入要變更的金額，然後選取&#x200B;*$*&#x200B;或&#x200B;*%*。 同時輸入&#x200B;**[!UICONTROL Max Limit]**，這是套用限制時的最高可能競標（上限）。 **注意：**&#x200B;如果目前的CPC競標已經等於或大於[!UICONTROL Max Limit]，則會忽略限制且不會變更競標。</li><li>*[!UICONTROL Decreases]：*&#x200B;以指定的百分比或貨幣值減少競標。 輸入要變更的金額，然後選取&#x200B;*$或%*。 同時輸入&#x200B;**[!UICONTROL Min Limit]**，這是套用限制時的最低出價（下限）。 **注意：**&#x200B;如果目前的CPC競標已經等於或小於[!UICONTROL Min Limit]，則會忽略限制且不會變更競標。</li></ul>**附註：**<ul><li>不論投資組合的&quot;[!UICONTROL Spend Around Constraints]&quot;設定為何，競標轉換導致的總金額中，競標轉換將導致相關投資組合出現支出過多或不足的情況。</li><li>如果您指定限制的結束日期，且最佳化功能會自動調整產品組合中行銷活動的支出限制，則競標不會單純在結束日期後恢復為原始金額，而是會調整為最佳金額。</li><li>競標轉換不會套用至資料不足無法產生成本和收入模型的競標單位。</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | （僅限[!UICONTROL Incremental Bidding]個限制）競標目標，以及遞增或遞減競標直到達到目標為止的頻率與數量：<ul><li>**[!UICONTROL Bid target]：**&#x200B;目標競標金額。</li><li>**[!UICONTROL Incrementally change bids by]**&#x200B;和&#x200B;**[型別]：**&#x200B;要以增量方式增加或減少出價的數目，以及要依貨幣值(**$**)或百分比(*%*)變更出價。</li><li>**[!UICONTROL Every __ days]：**&#x200B;遞增出價的頻率。</li></ul>例如，假設其中一個關鍵字目前的競標是100美分，而您想要每天變更10%的競標，直到達到500美分的競標目標為止。 在設定限制後的第1天，該關鍵字的競標是110美分（目前競標+ 10%）。 第2天的出價為120美分（第1天的目前出價+ 20%），以此類推。 不過，如果競標目標是50美分，而其他引數相同，則競標會逐步減少，直到競標達到50美分。 |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | （[!UICONTROL Search Engine Min Bid]個限制）使用在Google ([!UICONTROL Google First Page CPC])上搜尋結果第一頁顯示競標單位所需的最低競標。 選擇性地輸入&#x200B;**[!UICONTROL Min Bid]**&#x200B;值及/或&#x200B;**[!UICONTROL Max Bid]**&#x200B;值，以定義限制的合格競標範圍。 例如，若您指定2.50 USD的[!UICONTROL Min Bid]與4 USD的[!UICONTROL Max Bid]，則如果[!DNL Google Ads]第一頁競標低於2.50 USD或高於4 USD，則您將不會競標出價單位。 |
| | [!UICONTROL Set constraint options for Impression Share] | （僅限[!UICONTROL Impression Share]個限制）設定包括：<ul><li>**[!UICONTROL Min Bid]** （選擇性）相關競標單位的最低基礎競標。</li><li>**[!UICONTROL Max Bid]：** （選擇性）相關競標單位的最大基底競標。</li><li>**[!UICONTROL Min Impression Share]：**&#x200B;最低曝光比重（以百分比表示）將會觸發適用競標單位的限制。 必須介於10到90之間。 **注意：**&#x200B;當限制不具成本效益時，最佳化功能可能會覆寫它。</li><li>**[!UICONTROL Max Impression Share]：**&#x200B;最高曝光比重（以百分比表示）將會觸發適用競標單位的限制。 它必須介於10到90之間。**注意：**&#x200B;當限制不具成本效益時，最佳化功能可能會覆寫它。</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | 是否將條件套用至限制：<ul><li>*[!UICONTROL No Condition]：* （預設）在指定的日期範圍內無條件套用限制。</li><li>*[!UICONTROL Satisfy]：*&#x200B;只有在指定的資料評估期間符合指定的條件時，才會套用限制。</li></ul> |
| | [!UICONTROL Data Evaluation Period] | （設定條件時）為指定條件評估資料的時間期間。 如果您選取&#x200B;*[!UICONTROL Custom date range]，**請以`MM-DD-YYYY`格式輸入每個日期（例如2026年3月29日的03-29-2026）或按一下![行事曆按鈕](/help/search-social-commerce/assets/calendar-new.png "行事曆按鈕")開啟行事曆並選取每個日期，以指定&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**。 |
| | [!UICONTROL When to Apply Constraints] | （設定條件時）必須符合多少篩選條件才能套用限制：<ul><li>*[!UICONTROL Match All Filters]：*&#x200B;在符合每個指定的篩選條件時套用限制。</li><li>*[!UICONTROL Match Any Filters]：*&#x200B;至少符合一個指定的篩選條件時，套用條件約束。</li></ul> |
| | [!UICONTROL Filters] | （設定條件時）必須符合的一或多個條件。 若要建立篩選器，請從清單中選取屬性或量度。 針對屬性（例如[!UICONTROL Channel Type]），在清單中選取適用的值。 針對量度（例如[!UICONTROL Clicks]），請選取運運算元，然後輸入適用的值。 例如，若要只傳回超過100次點按的競標單位，請選取&#x200B;**點按**，選取&#x200B;**大於**，然後在輸入欄位中輸入`100`。</li></ul> |

## 將限制指派給搜尋競標單位 {#constraint-assign}

您可以將競標單位限制套用至任何促銷活動、廣告群組、關鍵字、位置或動態搜尋目標（自動鎖定目標）。

每個圖元只能有一個限制。 您可以同時將單一限制指定給一或多個圖元。

>[!NOTE]
>
>* 如果您稍後編輯廣告的關鍵字或廣告復本（因而建立新的關鍵字或廣告），則限制不會指派給新實體。
>* 檢視[[!UICONTROL Campaigns]檢視](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)、[[!UICONTROL Ad Groups]檢視](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)、[[!UICONTROL Keywords]檢視](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)或[[!UICONTROL Placements]檢視](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)中的相同指示。<!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. 從主功能表，開啟相關的管理檢視。

   例如，若要指派行銷活動層級的限制，請移至[!UICONTROL Manage] > [!UICONTROL Campaigns]。

1. （選擇性）從工具列](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[欄標題](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)篩選清單[。

1. 選取要為其指定單一限制的每個圖元旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

## 從搜尋競標單位取消指派限制 {#constraints-unassign}

>[!NOTE]
>
>* 若要刪除限制，使其無法供未來使用，請參閱[變更限制的狀態](#constraint-change-status)。
>* 檢視[[!UICONTROL Campaigns]檢視](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)、[[!UICONTROL Ad Groups]檢視](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)、[[!UICONTROL Keywords]檢視](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)或[[!UICONTROL Placements]檢視](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)中的相同指示。<!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. 在主功能表中，開啟相關的管理檢視。

   例如，若要取消指派行銷活動層級限制，請移至[!UICONTROL Manage] > [!UICONTROL Campaigns]。

1. 選取要取消指定限制的每個圖元旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

>[!MORELIKETHIS]
>
>* [管理行銷活動的限制指派](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [管理廣告群組的限制指派](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [管理關鍵字](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)的限制指派
>* [管理位置的限制指派](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
>* [該[!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)
