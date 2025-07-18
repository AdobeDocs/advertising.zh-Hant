---
title: 管理預設和自訂檢視
description: 瞭解如何自訂您的預設檢視和自訂檢視。
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 399974645b5083e735ff7aa94eba0a1115b4ddeb
workflow-type: tm+mt
source-wordcount: '4453'
ht-degree: 0%

---

# 管理預設和自訂檢視

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

您的預設檢視和自訂檢視可讓您自訂在搜尋促銷活動資料檢視中顯示的效能資料。 檢視設定包括要包含的欄、篩選器、日期範圍、轉換歸因設定和其他進階設定 — 您可以暫時套用設定或儲存它們。 （例外：您無法儲存預設檢視表的篩選器。） 每個預設和標準自訂檢視僅適用於特定檢視（例如[!UICONTROL Portfolios]或[!UICONTROL Campaigns]）和特定廣告商帳戶。 在舊版使用者介面中，每個通用自訂檢視都適用於特定廣告商的實體檢視，因此不能包含因實體型別而異的屬性欄（例如實體名稱或狀態）。

預設檢視會在您每次登入時顯示。 您可以隨時建立其他自訂檢視並套用檢視。 您可以選擇將您建立的任何自訂檢視共用給其他所有可以檢視廣告商資料的使用者。 只有建立自訂檢視的人員可以將其刪除。

在舊版使用者介面中，每個檢視都可做為左側面板[!UICONTROL Custom Views]區段中的捷徑使用。

## 套用預設或自訂檢視

### （新UI）套用預設或自訂檢視至管理檢視

1. 在資料表上方，按一下目前套用的檢視的名稱（![檢視](/help/search-social-commerce/assets/view.png "檢視")）。

1. 視需要按一下任何標籤（[!UICONTROL All Views]、[!UICONTROL Private]、[!UICONTROL Shared by Me]和[!UICONTROL From Others]）以尋找檢視。

1. 將游標停留在檢視表名稱上，然後按一下&#x200B;**[!UICONTROL Apply]**。

### （舊版UI）套用預設或自訂檢視至行銷活動管理檢視

* （預設檢視）在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]** \> **\[實體型別\]**。

* （自訂檢視）從左側導覽面板：

   1. 在左側面板中，按一下&#x200B;**[!UICONTROL Custom Views]**&#x200B;功能表以展開它。

      檢視會依適用的實體排序。

   1. 展開可用的功能表。

      &quot;[!UICONTROL Universal Views]&quot;包含可用於所有實體檢視的自訂檢視。 所有其他自訂檢視會依實體型別分組。

   1. 按一下檢視名稱。

      如果檢視是通用的，或套用至目前圖元，則會根據檢視組態重新顯示資料表。 如果檢視套用至不同的實體，則會根據檢視組態顯示適用實體的資料。

## 建立自訂檢視 {#create-custom-view}

>[!NOTE]
>
>除了您為自訂檢視指定的檢視設定外，也會儲存目前的欄排序順序。

### （新UI）從管理檢視建立自訂檢視

*可在[!UICONTROL Simulations]、[!UICONTROL Portfolios]、[!UICONTROL Campaigns]和[!UICONTROL Ad Groups]檢視中使用*

自訂檢視專屬於單一檢視（例如[!UICONTROL Portfolios]檢視）。

1. 在資料表上方，按一下目前套用的檢視的名稱（![檢視](/help/search-social-commerce/assets/view.png "檢視")）。

1. 按一下&#x200B;**[!UICONTROL Create View]**。

1. 指定[自訂檢視設定](#view-settings-new-ui)。

1. 儲存檢視：

   * 若要儲存並套用檢視，請按一下&#x200B;**[!UICONTROL Save & Apply]**。

   * 若要儲存檢視而不套用，請按一下&#x200B;**[!UICONTROL Save]**。

### （舊版UI）從行銷活動管理檢視建立自訂檢視

自訂檢視僅適用於行銷活動管理檢視。

1. 在資料表上方的工具列右側，按一下目前檢視的名稱（可能是&quot;[!UICONTROL Default]&quot;）。

1. 指定[自訂檢視設定](#view-settings)。

1. 按一下&#x200B;**[!UICONTROL Save as New]**。

1. 輸入新檢視的名稱，然後按一下&#x200B;**[!UICONTROL Save]**。

   >[!TIP]
   >
   >使用可協助您識別標籤及其適用資訊的名稱（例如「暫停的行銷活動」或「前50名廣告」）。

## 編輯預設或自訂檢視 {#view-edit}

### （新增UI）編輯預設或自訂檢視

*可在[!UICONTROL Simulations]、[!UICONTROL Portfolios]、[!UICONTROL Campaigns]和[!UICONTROL Ad Groups]檢視中使用*

1. 在資料表上方，按一下目前套用的檢視的名稱（![檢視](/help/search-social-commerce/assets/view.png "檢視")）。

1. 視需要按一下任何標籤（[!UICONTROL All Views]、[!UICONTROL Private]、[!UICONTROL Shared by Me]和[!UICONTROL From Others]）以尋找檢視。

1. 將游標停留在檢視表名稱上，然後按一下![編輯](/help/search-social-commerce/assets/edit-new.png)。

1. 編輯[自訂檢視設定](#view-settings-new-ui)。

1. 儲存檢視：

   * 若要儲存變更而不套用變更，請按一下&#x200B;**[!UICONTROL Save]**。

   * 若要儲存變更並套用變更，請按一下&#x200B;**[!UICONTROL Apply]**.<!-- Should be Save & Apply -->

### （舊版UI）編輯預設或自訂檢視

1. 開啟檢視設定：

   * （如果您已套用檢視）在資料表格上方的工具列右側，按一下目前檢視的名稱（可能是&quot;[!UICONTROL Default]&quot;）。

   * （未套用的自訂檢視）在左側面板中，按一下![自訂檢視](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "自訂檢視")以展開[!UICONTROL Custom Views]功能表。 按一下自訂檢視名稱。

1. 編輯[檢視設定](#view-settings)。

   >[!NOTE]
   >
   >您可以將篩選的變更套用至預設檢視設定，但不能儲存。

1. 套用或儲存設定：

   * 若要暫時套用設定而不儲存至檢視，請按一下&#x200B;**[!UICONTROL Apply]**。

     設定會套用至標籤，直到您離開最上層管理檢視或（如果適用）[檢視其他廣告商的資料](/help/search-social-commerce/common-tasks/change-advertiser.md)為止。

   * （針對您建立的預設檢視和自訂檢視）若要將設定儲存到目前檢視，請按一下&#x200B;**[!UICONTROL Save]**。

   * 若要將設定儲存至新的自訂檢視，請按一下&#x200B;**[!UICONTROL Save As]**。 在[!UICONTROL Enter New Custom View Name]視窗中輸入新檢視的名稱，然後按一下&#x200B;**[!UICONTROL Save]**。

## （新增UI）複製預設或自訂檢視 {#view-clone}

*可在[!UICONTROL Simulations]、[!UICONTROL Portfolios]、[!UICONTROL Campaigns]和[!UICONTROL Ad Groups]檢視中使用*

1. 在資料表上方，按一下目前套用的檢視的名稱（![檢視](/help/search-social-commerce/assets/view.png "檢視")）。

1. 視需要按一下任何標籤（[!UICONTROL All Views]、[!UICONTROL Private]、[!UICONTROL Shared by Me]和[!UICONTROL From Others]）以尋找檢視。

1. 將游標停留在檢視表名稱上，然後按一下![複製](/help/search-social-commerce/assets/clone-new.png)。

1. 輸入新的檢視名稱，並視需要編輯[自訂檢視設定](#view-settings-new-ui)。

1. 儲存檢視：

   * 若要儲存並套用檢視，請按一下&#x200B;**[!UICONTROL Save & Apply]**。

   * 若要儲存檢視而不套用，請按一下&#x200B;**[!UICONTROL Save]**。

## 將預設檢視重設為系統預設設定

還原預設檢視設定會移除您已儲存的所有設定，並重新套用系統預設設定。

系統預設設定會因管理檢視而異。 對於大多數的管理檢視，系統預設檢視會顯示已啟用帳戶中專案及作用中專案（例如，僅作用中行銷活動中的作用中廣告群組）前一天的資料，其資料會依成本排序，而轉換資料則根據交易日期而定。

* 從新的使用者介面：

   1. 在資料表上方，按一下目前套用的檢視的名稱（![檢視](/help/search-social-commerce/assets/view.png "檢視")）。

   1. 視需要按一下任何標籤（[!UICONTROL All Views]、[!UICONTROL Private]、[!UICONTROL Shared by Me]和[!UICONTROL From Others]）以尋找檢視。

   1. 將游標停留在檢視名稱上，然後按一下![回覆](/help/search-social-commerce/assets/revert-new.png)。

* 從舊版行銷活動管理檢視：

   1. 在左側面板中，按一下![自訂檢視](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "自訂檢視")以展開[!UICONTROL Custom Views]功能表。

      檢視會依適用的實體排序。

   1. 在檢視名稱旁邊，按一下![還原為預設設定](/help/search-social-commerce/assets/restore.png "還原為預設設定")。

## 刪除自訂檢視

您可以刪除您建立的任何自訂檢視。

如果您刪除套用至目前標籤的自訂檢視，標籤會繼續顯示自訂檢視，直到您移出檢視集（例如，從[!UICONTROL Search]功能表內的檢視移至[!UICONTROL Reports]功能表）或（如果適用）當您[檢視其他廣告商的資料](/help/search-social-commerce/common-tasks/change-advertiser.md)為止。

* 從新的使用者介面：

   1. 在資料表上方，按一下目前套用的檢視的名稱（![檢視](/help/search-social-commerce/assets/view.png "檢視")）。

   1. 視需要按一下任何標籤（[!UICONTROL All Views]、[!UICONTROL Private]、[!UICONTROL Shared by Me]和[!UICONTROL From Others]）以尋找檢視。

   1. 將游標停留在檢視表名稱上，然後按一下![刪除](/help/search-social-commerce/assets/delete-new.png)。

   1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

* 從舊版行銷活動管理檢視：

   1. 在左側面板中，按一下![自訂檢視](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "自訂檢視")以展開[!UICONTROL Custom Views]功能表。

   1. 將游標放在自訂檢視名稱上，然後按一下![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

   1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Continue]**。

## 預設和自訂檢視設定

<!-- Simplify attribution rule definitions here and elsewhere and include links to "How attribution rules are calculated -->

### （新UI）預設和自訂檢視設定 {#view-settings-new-ui}

| **標籤** | **欄位** | **描述** |
| --- | --- | --- |
| [在所有索引標籤上方] | 名稱 | 檢視的唯一名稱。 您無法編輯預設檢視的名稱。<p><b>秘訣：</b>使用可協助您識別標籤及其適用資訊的名稱（例如「暫停的行銷活動」或「前50個廣告」）。 |
|   | 與其他使用者共用 | （僅限自訂檢視；選用）讓其他所有可以檢視廣告商資料的使用者都能檢視此檢視。 其他使用者無法編輯或刪除檢視，但他們可以從設定建立新檢視。 |
| 欄 | 選取的欄和順序 | 顯示的資料欄及其順序：<ul><li> （若要新增欄）在[可用欄]清單中，按一下欄名稱，然後將其拖曳到[選取的欄和順序]清單中，或按一下![向右鍵](/help/search-social-commerce/assets/chevron-right.png)將其移動到該處。</li><li>（若要變更資料行的水平位置）在[選取的資料行與順序]清單中，按一下資料行名稱，然後將其拖曳到想要的位置，或按一下[向上鍵] &lbrace;1&rbrack;或[向下鍵] ![ ](/help/search-social-commerce/assets/chevron-up.png)，將其移動到該位置。 ![](/help/search-social-commerce/assets/chevron-down.png)頂端欄名稱會顯示在左欄。</li><li>（若要移除欄）在[選取的欄和順序]清單中，按一下欄名稱，然後將其拖曳到[可用的欄]清單中，或按一下![向左鍵](/help/search-social-commerce/assets/chevron-left.png)將其移動到該處。</li></ul><b>篩選資料</b><p>若只要列出特定型別的資料，請按一下清單旁邊的任何圖示：<ul><li>屬性名稱和ID的![屬性圖示](/help/search-social-commerce/assets/properties-icon-new.png)，例如[!UICONTROL Portfolio Name]或[!UICONTROL Status]</li><li>標準流量量度的![流量圖示](/help/search-social-commerce/assets/traffic-metrics-icon-new.png)，例如曝光數和點按數</li><li>![收入圖示](/help/search-social-commerce/assets/revenue-metrics-icon-new.png) （針對廣告商追蹤的轉換量度，包括從Analytics同步的轉換和網站參與量度）</li><li>![自訂圖示](/help/search-social-commerce/assets/custom-metrics-icon-new.png) （針對廣告商建立的自訂量度）</li><li>![分類圖示](/help/search-social-commerce/assets/classifications-icon-new.png) （用於標籤分類）。</li></ul> <b>其他附註：</b><ul><li>若要新增、建立或編輯新量度，請參閱&quot;[建立自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md)&quot;、&quot;[編輯自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md)&quot;以及&quot;[刪除自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md)&quot;。</li><li>如果報表包含不同貨幣帳戶的資料，則以貨幣為基礎的欄（例如成本和CPC）不會包含總計。</li><li>您可以[從欄標題功能表](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md)暫時編輯欄集合，以及[從[!UICONTROL Columns]圖示](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md)編輯和排序欄集合。 （![欄圖示](/help/search-social-commerce/assets/custom-columns.png "欄圖示")）。</li></ul> |
|   | 排序依據： | 資料排序所依據的欄。 每種報表型別的預設值都不同。 |
|   | 排序順序 | 要以&#x200B;**遞增**&#x200B;或&#x200B;**遞減**&#x200B;的順序排序資料。 |
| 篩選器 | [篩選器定義] | （選用）套用至資料的篩選器。 套用篩選器時，只有在資料行的值符合指定准則時，才會傳回資料列。<p>若要套用每個篩選器：<ol><li>在[!UICONTROL Add Filter]功能表中，選取欄名稱。 此清單包含所有可用的欄，並依欄型別排序，屬性欄優先。</li><li>在欄上定義篩選</li></ol>（具有輸入欄位的篩選器）從第二個功能表選取運運算元，然後輸入適用的值。 值不區分大小寫。<p>例如，如果您已選取「點按」欄且只想傳回點按超過100次的列，則選取&#x200B;_\>_&#x200B;並在輸入欄位中輸入`100`。<p>根據資料型別，可用的運運算元可能包括<i>大於</i>、<i>小於</i>、<i>等於</i>、<i>包含</i>、<i>不包含</i>、<i>開頭為</i>、<i>結尾為</i>、<i>無值</i>或<i>具有值</i> <i>在</i>之前、<i>在</i>之後，或<i>無日期</i>。<p>（沒有輸入欄位的篩選器）按一下[選取清單專案]功能表旁的![向下箭頭](/help/search-social-commerce/assets/arrow-down-expand.png)，然後選取每個要包含的值旁的核取方塊。<p><b>附註：</b><ul><li>您可以將篩選的變更套用至預設檢視設定，但不能儲存。</li><li>您也可以[在檢視中暫時變更適用的篩選器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)。</li></ul> |
| 其他設定 | 日期範圍 | （選取「包含日期範圍」時）<p>要產生資料的日期範圍。 選擇一個選項：<ul><li><i>[預設範圍]</i>：一般時間增量清單，範圍從<i>今天</i>到<i>最近180天</i>。 從清單中選擇一個；預設值為<i>Yesterday</i>。 注意： <i>上個月</i>、<i>最近3個月</i>和<i>最近6個月</i>會顯示前一個日曆月的資料。</li><li><i>自訂日期範圍：</i>指定開始日期和結束日期。 以MM/DD/YYYY或M/D/YYYY格式輸入日期，或按一下欄位旁的![行事曆圖示](/help/search-social-commerce/assets/calendar.png)並選取日期。</li></ul> |
|   | 比較 | 比較指定日期範圍的資料與第二日期範圍的資料。 選取此選項時，請指定第二個日期範圍。 會為每個一般資料欄新增兩個額外的欄。 例如，報表不只包括「曝光數」的一欄，而是「曝光數範圍1」、「曝光數範圍2」和「曝光數差異」的欄。<p><b>附註：</b><ul><li>衍生量度的差異欄不會顯示。</li><li>比較大型日期範圍的報表可能需要更長的時間才能產生。</li></ul> |
|   | 比較格式 | （啟用[!UICONTROL Comparison]時）如何表示&quot;[_資料欄位_]&#x200B;差異&quot;欄中兩個所選日期範圍之間的資料差異。 選擇一個選項：<ul><li><i>差異</i> （預設）：將差異顯示為數值。</li><li><i>%變更</i>：以百分比顯示差異。</li></ul> |
|   | 歸因規則 | (僅使用Adobe Advertising畫素式轉換追蹤服務的廣告商)在索引標籤中，如何在一系列導致轉換的事件中歸因轉換資料（可能跨多個廣告頻道和產品組合）。 依預設，會選取在廣告商層級轉換歸因設定中指定的規則。<ul><li> <i>第一個事件</i>：將轉換歸因於廣告商的點按回顧期間內的系列中的第一個付費點按，如果沒有發生付費點按，則歸因於廣告商的點按回顧期間內的最後一個點按。</li><li><i>加權第一個事件更多</i>：將轉換歸因於發生在廣告商的點選回顧視窗和曝光回顧視窗內的系列中的所有事件，但給予第一個事件最大的權重，並連續減少對以下事件的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>平均分佈</i>：將轉換平均歸因於發生在廣告商的點按回顧視窗和曝光回顧視窗中的序列中的每個事件。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>加權最後一個事件更多</i>：將轉換歸因於發生在廣告商的點選回顧視窗和曝光回顧視窗內的系列中的所有事件，但給予最後一個事件最大的權重，並連續減少對先前事件的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>上次事件</i> （預設值）：將轉換歸因於廣告商的點選回顧期間內的系列中最後一次付費點選，如果沒有發生付費點選，則歸因於廣告商的曝光回顧期間內的最後一次曝光。</li><li><i>U形</i>：將轉換歸因於發生在廣告商的點按回顧視窗和曝光回顧視窗內的系列中的所有事件，但給予第一個事件和最後一個事件最大的權重，並連續減少對轉換路徑中間事件的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li></ul><p><b>附註：</b><ul><li>除了上次事件之外，所有歸因規則都僅適用於具有Adobe Advertising點選追蹤以及來自Adobe Advertising或Adobe Analytics （與Analytics整合）的轉換追蹤的廣告商。</li><li>歸因規則適用於任何頻道中付費廣告的點按。 它們不適用於付費搜尋廣告的曝光數，無法在事件層級進行追蹤。</li><li>當您使用任何歸因規則（一個「最後事件」規則除外）報告轉換資料時，導致轉換的事件可能會發生在多個產品組合中。 若是如此，只有當這些產品組合中的廣告或關鍵字包含在檢視中時，檢視才會包含轉換的資料。</li><li>針對預設檢視，建議您在競標最佳化期間保留預設歸因規則，該規則用於計算每個競標單位的[目標值](/help/search-social-commerce/glossary.md#o-p) （原稱為「加權收入」）。</li></ul> |
|   | 轉換依據 | 如何報告轉換資料：<ul><li><i>按一下日期</i>：若要檢視在指定期間內因按一下而發生的交易。 當產品組合在點按和交易之間有重大延遲時，此選項可用於計算產品組合的每次點按歷史收入，其指示一段時間內預期的收入行為。</li><li><i>交易日期</i> （預設值）：檢視交易日期在指定期間內發生的交易。 這表示在指定期間內已賺取多少收入。</li></ul> |

### （舊版UI）預設和自訂檢視設定 {#view-settings}

| **標籤** | **欄位** | **描述** |
| --- | --- | --- |
| [在所有索引標籤上方] | 名稱 | 檢視的唯一名稱。 您無法編輯預設檢視的名稱。<p><b>秘訣：</b>使用可協助您識別標籤及其適用資訊的名稱（例如「暫停的行銷活動」或「前50個廣告」）。 |
|   | 通用檢視 | （現有檢視為唯讀）讓資料設定可用於所有實體檢視（行銷活動、廣告等）。 通用檢視可包含量度和標籤分類欄，但不能包含屬性欄（例如實體名稱和狀態），因為它們會因實體型別而異 — 以及所有其他檢視屬性。 任何篩選條件都會套用至實體檢視（若適用），否則會予以忽略。 所有量度篩選器都會在本機進行評估（例如，對於點按\> 1000，「促銷活動」檢視會顯示超過1000次點按的促銷活動，而「廣告群組」檢視會顯示超過1000次點按的廣告群組）。<p>通用檢視的屬性欄是從實體的預設檢視中提取。 您可以在預設檢視設定中變更特定實體的預設屬性欄。<p>啟用或停用此選項後，您無法將變更儲存到現有檢視，但可以建立含有變更的新檢視。 |
|   | 共用 | （僅限現有自訂檢視；選用）讓其他所有可以檢視廣告商資料的使用者都能檢視此檢視。 其他使用者無法編輯或刪除檢視，但他們可以從設定建立新檢視。 在您的檢視清單中，其他人員正在共用的每個檢視都會以斜體顯示，例如「_績效最佳的行銷活動_」。 |
| 欄 | 選取的欄和順序 | 顯示的資料欄及其順序：<ul><li> （若要新增欄）在[可用欄]清單中，按一下欄名稱，然後將其拖曳到[選取的欄和順序]清單中，或按一下![向右鍵](/help/search-social-commerce/assets/chevron-right.png)將其移動到該處。</li><li>（若要變更資料行的水平位置）在[選取的資料行與順序]清單中，按一下資料行名稱，然後將其拖曳到想要的位置，或按一下[向上鍵] &lbrace;1&rbrack;或[向下鍵] ![ ](/help/search-social-commerce/assets/chevron-up.png)，將其移動到該位置。 ![](/help/search-social-commerce/assets/chevron-down.png)頂端欄名稱會顯示在左欄。</li><li>（若要移除欄）在[選取的欄和順序]清單中，按一下欄名稱，然後將其拖曳到[可用的欄]清單中，或按一下![向左鍵](/help/search-social-commerce/assets/chevron-left.png)將其移動到該處。</li></ul><b>篩選資料</b><p>若只要列出特定型別的資料，請按一下清單旁邊的任何圖示：<ul><li>搜尋元件的屬性名稱和ID的![屬性圖示](/help/search-social-commerce/assets/properties-icon.png)，例如Status</li><li>標準流量量度的![流量圖示](/help/search-social-commerce/assets/traffic-metrics-icon.png)，例如曝光數和點按數</li><li>![收入圖示](/help/search-social-commerce/assets/revenue-metrics-icon.png) （針對廣告商追蹤的轉換量度，包括從Analytics同步的轉換和網站參與量度）</li><li>![自訂圖示](/help/search-social-commerce/assets/custom-metrics-icon.png) （適用於廣告商建立的自訂衍生量度）</li><li>![分類圖示](/help/search-social-commerce/assets/classifications-icon.png) （用於標籤分類）。</li></ul> <b>其他附註：</b><ul><li>若要新增、建立或編輯新量度，請參閱&quot;[建立自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md)&quot;、&quot;[編輯自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md)&quot;以及&quot;[刪除自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md)&quot;。</li><li>如果報表包含不同貨幣帳戶的資料，則以貨幣為基礎的欄（例如成本和CPC）不會包含總計。</li><li>您可以[從欄標題功能表](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md)暫時編輯欄集合，以及[從[!UICONTROL Columns]圖示](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md)編輯和排序欄集合。 （![欄圖示](/help/search-social-commerce/assets/custom-columns.png "欄圖示")）。</li></ul> |
|   | 排序方式 | 資料排序所依據的欄。 每種報表型別的預設值都不同。 |
|   | 排序順序 | 要以&#x200B;**遞增**&#x200B;或&#x200B;**遞減**&#x200B;的順序排序資料。 移動滑桿以選取選項。 |
| 篩選器 | [篩選器定義] | （選用）套用至資料的篩選器。 套用篩選器時，只有在資料行的值符合指定准則時，才會傳回資料列。<p>若要套用每個篩選器：<ol><li>在[!UICONTROL Add Filter]功能表中，選取欄名稱。 此清單包含所有可用的欄，並依欄型別排序，屬性欄優先。</li><li>在欄上定義篩選</li></ol>（具有輸入欄位的篩選器）從第二個功能表選取運運算元，然後輸入適用的值。 值不區分大小寫。<p>例如，如果您已選取「點按」欄且只想傳回點按超過100次的列，則選取&#x200B;_\>_&#x200B;並在輸入欄位中輸入`100`。<p>根據資料型別，可用的運運算元可能包括<i>大於</i>、<i>小於</i>、<i>等於</i>、<i>包含</i>、<i>不包含</i>、<i>開頭為</i>、<i>結尾為</i>、<i>無值</i>或<i>具有值</i> <i>在</i>之前、<i>在</i>之後，或<i>無日期</i>。<p>（沒有輸入欄位的篩選器）按一下[選取清單專案]功能表旁的![向下箭頭](/help/search-social-commerce/assets/arrow-down-expand.png)，然後選取每個要包含的值旁的核取方塊。<p><b>附註：</b><ul><li>您可以將篩選的變更套用至預設檢視設定，但不能儲存。</li><li>您也可以[在檢視中暫時變更適用的篩選器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)。</li></ul> |
|   | 僅包含具有效能資料的列 | （僅限廣告群組、關鍵字、產品群組、位置及自動目標檢視） <p>只包含具有指定日期期間之效能資料的列。 依預設，選取此選項可縮短頁面載入時間。 <p><b>警告</b>：如果您取消選取選項，而檢視包含許多沒有效能資料的實體，則需要較長時間才能顯示資料。<p> <b>附註</b>：您可以套用，但無法將篩選的變更儲存到預設的檢視設定。 預設檢視一律僅顯示具有效能資料的實體。 |
| 日期 | 日期範圍 | （選取「包含日期範圍」時）<p>要產生資料的日期範圍。 選擇一個選項：<ul><li><i>[預設範圍]</i>：一般時間增量清單，範圍從<i>今天</i>到<i>最近180天</i>。 從清單中選擇一個；預設值為<i>Yesterday</i>。 注意： <i>上個月</i>、<i>最近3個月</i>和<i>最近6個月</i>會顯示前一個日曆月的資料。</li><li><i>自訂日期範圍：</i>指定開始日期和結束日期。 以MM/DD/YYYY或M/D/YYYY格式輸入日期，或按一下欄位旁的![行事曆圖示](/help/search-social-commerce/assets/calendar.png)並選取日期。</li></ul> |
|   | 比較 | 比較指定日期範圍的資料與第二日期範圍的資料。 選取此選項時，請指定第二個日期範圍。 會為每個一般資料欄新增兩個額外的欄。 例如，報表不只包括「曝光數」的一欄，而是「曝光數範圍1」、「曝光數範圍2」和「曝光數差異」的欄。<p><b>附註：</b><ul><li>衍生量度的差異欄不會顯示。</li><li>比較大型日期範圍的報表可能需要更長的時間才能產生。</li></ul> |
|   | 比較格式 | （啟用[!UICONTROL Comparison]時）如何表示&quot;[_資料欄位_]&#x200B;差異&quot;欄中兩個所選日期範圍之間的資料差異。 選擇一個選項：<ul><li><i>差異</i> （預設）：將差異顯示為數值。</li><li><i>%變更</i>：以百分比顯示差異。</li></ul> |
| 其他設定 | 使用預設 | 套用廣告商層級轉換歸因設定中指定的歸因設定。 |
|   | 歸因規則 | (僅使用Adobe Advertising畫素式轉換追蹤服務的廣告商)在索引標籤中，如何在一系列導致轉換的事件中歸因轉換資料（可能跨多個廣告頻道和產品組合）。 依預設，會選取在廣告商層級轉換歸因設定中指定的規則。<ul><li> <i>第一個事件</i>：將轉換歸因於廣告商的點按回顧期間內的系列中的第一個付費點按，如果沒有發生付費點按，則歸因於廣告商的點按回顧期間內的最後一個點按。</li><li><i>加權第一個事件更多</i>：將轉換歸因於發生在廣告商的點選回顧視窗和曝光回顧視窗內的系列中的所有事件，但給予第一個事件最大的權重，並連續減少對以下事件的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>平均分佈</i>：將轉換平均歸因於發生在廣告商的點按回顧視窗和曝光回顧視窗中的序列中的每個事件。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>加權最後一個事件更多</i>：將轉換歸因於發生在廣告商的點選回顧視窗和曝光回顧視窗內的系列中的所有事件，但給予最後一個事件最大的權重，並連續減少對先前事件的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>上次事件</i> （預設值）：將轉換歸因於廣告商的點選回顧期間內的系列中最後一次付費點選，如果沒有發生付費點選，則歸因於廣告商的曝光回顧期間內的最後一次曝光。</li><li><i>U形</i>：將轉換歸因於發生在廣告商的點按回顧視窗和曝光回顧視窗內的系列中的所有事件，但給予第一個事件和最後一個事件最大的權重，並連續減少對轉換路徑中間事件的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li></ul><p><b>附註：</b><ul><li>除了上次事件之外，所有歸因規則都僅適用於具有Adobe Advertising點選追蹤以及來自Adobe Advertising或Adobe Analytics （與Analytics整合）的轉換追蹤的廣告商。</li><li>歸因規則適用於任何頻道中付費廣告的點按。 它們不適用於付費搜尋廣告的曝光數，無法在事件層級進行追蹤。</li><li>當您使用任何歸因規則（一個「最後事件」規則除外）報告轉換資料時，導致轉換的事件可能會發生在多個產品組合中。 若是如此，只有當這些產品組合中的廣告或關鍵字包含在檢視中時，檢視才會包含轉換的資料。</li><li>針對預設檢視，建議您在競標最佳化期間保留預設歸因規則，該規則用於計算每個競標單位的[目標值](/help/search-social-commerce/glossary.md#o-p) （原稱為「加權收入」）。</li></ul> |
|   | 轉換依據 | 如何報告轉換資料：<ul><li><i>按一下日期</i>：若要檢視在指定期間內因按一下而發生的交易。 當產品組合在點按和交易之間有重大延遲時，此選項可用於計算產品組合的每次點按歷史收入，其指示一段時間內預期的收入行為。</li><li><i>交易日期</i> （預設值）：檢視交易日期在指定期間內發生的交易。 這表示在指定期間內已賺取多少收入。</li></ul> |
