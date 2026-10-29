---
title: 管理[!DNL Google Ads]動態搜尋目標
description: 瞭解如何建立和管理[!DNL Google Ads]動態搜尋目標。
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%
---
# 管理[!DNL Google Ads]動態搜尋目標

僅&#x200B;*[!DNL Google Ads]個帳戶*

您可以建立、編輯和變更使用搜尋網路之[!DNL Google Ads]行銷活動的動態搜尋目標狀態。

## 什麼是動態搜尋目標？

動態搜尋目標會定義廣告網路是使用您網站中的所有頁面還是頁面子集，來鎖定您的動態搜尋廣告。 在廣告群組層級設定動態搜尋目標；這些目標會套用至相同廣告群組中的所有動態搜尋廣告。

根據您的行銷活動設定，動態搜尋目標可能是必要或選用的：

* 若未在行銷活動的&quot;[!UICONTROL DSA Options]&quot;區段中指定網站網域和語言，您必須建立動態搜尋目標。

* 當您在促銷活動的&quot;[!UICONTROL DSA Options]&quot;區段中指定網站網域和語言時，您可以選擇建立動態搜尋目標。

  [!DNL Google Ads]會根據這些設定所指定的網站內容，自動顯示您的動態搜尋廣告。

若要最佳追蹤效能，請為每個動態搜尋目標設定一個廣告群組的行銷活動，並包含以所有條件為目標的廣告群組。

如需[!DNL Google Ads]動態搜尋廣告的詳細資訊，請參閱https://support.google.com/google-ads/answer/2471185。

## [!UICONTROL Auto Targets]檢視 {#auto-target-view-about}

[!UICONTROL Targeting] > [!UICONTROL Auto Targets]檢視會列出所選廣告商帳戶之篩選檢視中的所有動態搜尋目標。 您也可以管理動態搜尋目標。

檢視資料需要[!UICONTROL View Auto Targets]許可權。 建立目標及編輯其競標或狀態需要[!UICONTROL Edit Auto Targets]許可權。

### 可用動作

* [建立動態搜尋目標](#auto-target-create)

* [編輯動態搜尋目標的設定](#auto-target-edit)

* [變更動態搜尋目標的狀態或刪除](#auto-target-status)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

* [將限制](#constraint-assign)指派給動態搜尋目標，以及[從動態搜尋目標移除限制](#constraint-unassign)

* [指派標籤分類](#classification-values-assign)給動態搜尋目標，以及[從動態搜尋目標移除標籤分類](#classification-values-remove)

>[!NOTE]
>
>您可以上傳[大量工作表檔案](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)並張貼至廣告網路，一次建立及編輯大量目標資料（包括標籤和限制指派）。

## 建立[!DNL Google Ads]動態搜尋目標 {#auto-target-create}

您可以建立動態搜尋目標，以定義網站中的頁面（即廣告顯示URL中使用的網域），其內容是用來鎖定相同廣告群組中的動態搜尋廣告。

您可以鎖定所有已編制索引的頁面，或指定最多三個條件。

>[!NOTE]
>
>若要最佳追蹤效能，請使用[!UICONTROL All]選項為每個行銷活動僅一個廣告群組建立目標。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create Auto Target]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;中，選取廣告網路、帳戶、行銷活動和廣告群組。

1. 指定其餘的[動態搜尋目標設定](#auto-target-create-settings)。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 檢閱設定。 若要變更任何設定，請按一下適用區段中的![編輯](/help/search-social-commerce/assets/edit-new.png "編輯") **[!UICONTROL Edit]**，然後變更設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 編輯[!DNL Google Ads]動態搜尋目標設定 {#auto-target-edit}

您可以編輯一或多個動態搜尋目標的狀態或最高出價。 您無法變更已鎖定目標的條件。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 選取要編輯之每一列旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Edit Auto Targets]**&#x200B;面板中，編輯[狀態和競標設定](#auto-target-edit-settings)。

   您的變更會套用至所有選取的目標。 您未變更的設定會保留其現有值。

   當選取的目標使用多種貨幣時，將會停用競標編輯。 您仍可變更其狀態。

1. 按一下&#x200B;**[!UICONTROL Save]**。

您也可以按一下單一目標的競標值，直接在資料表格中編輯其競標。

## 變更[!DNL Google Ads]動態搜尋目標的狀態或刪除 {#auto-target-status}

您可以暫停作用中的動態搜尋目標，以停止將其用於相同廣告群組中的動態搜尋廣告。 您稍後可以透過將目標的狀態變更回作用中來繼續使用該目標。 您也可以刪除動態搜尋目標。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. （可選）篩選清單以包含特定的動態搜尋目標。

1. 執行下列任一項作業：

   * 若要變更一個目標的狀態，請按一下&#x200B;**[!UICONTROL Status]**&#x200B;欄中的值，然後選取&#x200B;**[!UICONTROL Active]**&#x200B;或&#x200B;**[!UICONTROL Paused]**。

   * 若要變更多個目標的狀態，請選取每個目標旁的核取方塊，按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**，在&#x200B;**[!UICONTROL Edit Auto Targets]**&#x200B;面板中選取&#x200B;**[!UICONTROL Status]**，然後按一下&#x200B;**[!UICONTROL Save]**。

   * 若要刪除一或多個目標，請選取每個目標旁的核取方塊，按一下大量動作工具列中的&#x200B;**[!UICONTROL ...]>[!UICONTROL Delete]**，然後按一下確認訊息中的&#x200B;**[!UICONTROL Confirm]**。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

## 管理動態搜尋目標的限制指派 {#constraints}

### 指派限制給動態搜尋目標 {#constraint-assign}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 選取每個動態搜尋目標旁的核取方塊，您將為其指定單一限制。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

### 從選取的動態搜尋目標移除限制 {#constraint-unassign}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 選取每個動態搜尋目標旁的核取方塊，您會從中取消指派限制。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

## 管理動態搜尋目標的分類值 {#classification-values}

### 指派分類值給動態搜尋目標 {#classification-values-assign}

>[!NOTE]
>
>標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入動態搜尋目標的值。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 選取您要指派標籤值的每個動態搜尋目標旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**。

1. 請針對每個適用的分類值，執行下列動作：

   1. 在&#x200B;**[!UICONTROL Classifications]**&#x200B;欄中指定分類：

      * 若要使用現有的分類，請按一下分類名稱將其展開。

      * 若要建立分類，請按一下欄標題中的[!UICONTROL +]。 在輸入欄位中輸入分類名稱，然後按一下[儲存] ![ ](/help/search-social-commerce/assets/save-checkmark.png " [儲存] ")，立即儲存分類。 若要使用新分類，請按一下分類名稱將其展開。

        名稱必須包含[ASCII字元32-126](https://www.asciitable.com/)，最大長度為27個單位元組字元。

   1. 在&#x200B;**[!UICONTROL Value Name]**&#x200B;欄中，指定所選分類的值：

      * 若要使用現有值，請選取該值。

      * 若要建立值，請按一下欄標題中的[!UICONTROL +]。 在輸入欄位中輸入值，然後按一下![儲存](/help/search-social-commerce/assets/save-checkmark.png "儲存")，立即儲存值並依預設選取。

        長度上限為100個字元，可包含ASCII和非ASCII字元。

1. 按一下&#x200B;**+[!UICONTROL Assign Now]**。

### 從動態搜尋目標中移除標籤分類值 {#classification-values-remove}

移除分類值會移除與帳戶元件及其所有子元件的關聯。 這些元件不再提供分類值的報表資料。 移除分類值不會刪除值或帳戶元件。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 選取每個動態搜尋目標旁的核取方塊，您會從其中移除標籤值。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 選取每個分類值旁的核取方塊，以從選取的實體中移除。

   若要選取所有指派的值，請按一下&#x200B;**[!UICONTROL Select All]**。 若要取消選取所有指派的值，請按一下&#x200B;**[!UICONTROL Deselect All]**。

1. 按一下&#x200B;**[!UICONTROL Unassign Selected]**。

## [!DNL Google Ads]動態搜尋目標設定 {#dynamic-search-target-settings}

### 建立期間可用的設定 {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**自動鎖定目標：**&#x200B;其內容用於鎖定廣告群組中的動態搜尋廣告的索引頁面：

* *[!UICONTROL All]* （預設值）：鎖定所有已編制索引的頁面。

* *[!UICONTROL Specific]：*&#x200B;目標頁面最多符合三個條件。 選取條件並輸入其值。 若要新增另一個條件，請按一下&#x200B;**[!UICONTROL And]**。 條件會與AND結合，因此頁面必須符合所有指定的條件。 按一下&#x200B;**[!UICONTROL Reset]**&#x200B;以清除條件。

  * *[!UICONTROL Category]：*&#x200B;頁面的[!DNL Google Ads]內容類別等於指定的值。 輸入值。

  * *[!UICONTROL URL]：*&#x200B;頁面的URL包含指定的值，例如`shoes.example.com`。 請輸入有效的URL。

  * *[!UICONTROL Page Title]：*&#x200B;頁面標題包含指定的文字。 輸入值。

  * *[!UICONTROL Page Content]：*&#x200B;頁面內容包含指定的文字。 輸入值。

建立目標後就無法變更目標條件。

**[!UICONTROL Status]：**&#x200B;目標的狀態：

* *[!UICONTROL Active]* （預設值）：啟用競標。

* *[!UICONTROL Paused]：*&#x200B;停用競標。

**[!UICONTROL Bid]：**&#x200B;目標的每次點按成本上限(CPC)。 此值會覆寫廣告群組層級競標。 此欄位是選擇性的；當您輸入競標時，帳戶貨幣的最小值為0.01。

>[!NOTE]
>
>如果目標在最佳化的產品組合中，則會套用一天特定的CPC競標。 之後，最佳化功能會根據自己的計算來放置競標。

### 編輯期間可用的設定 {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]：**&#x200B;選取&#x200B;**[!UICONTROL Active]**&#x200B;或&#x200B;**[!UICONTROL Paused]**。

#### [!UICONTROL Bid details]

選取的目標使用多種貨幣時，便會停用競標編輯。

**[!UICONTROL Bid adjustment]：**&#x200B;如何變更出價上限：

* *[!UICONTROL Set to]：*&#x200B;以[!UICONTROL Set value]中的金額取代每個競標。

* *[!UICONTROL Increase]：*&#x200B;在[!UICONTROL Set value]中以金額或百分比增加每個競標。

* *[!UICONTROL Decrease]：*&#x200B;在[!UICONTROL Set value]中以金額或百分比減少每個競標。

**[!UICONTROL Modifier type]：** （針對[!UICONTROL Increase]和[!UICONTROL Decrease]）選取&#x200B;**[!UICONTROL Currency]**&#x200B;或&#x200B;**[!UICONTROL Percentage]**。

**[!UICONTROL Set value]：**&#x200B;新的出價，或變更每個出價的金額或百分比。 最小值為0.01。

**[!UICONTROL Max limit]：** （選擇性；適用於[!UICONTROL Increase]和[!UICONTROL Decrease]）帳戶貨幣的限制。 如果是提高，這是最高出價。 如果是降低，這是所產生的最低出價。 輸入限制時，最小值為0.01。

>[!MORELIKETHIS]
>
>* [（新UI）管理搜尋競標單位的限制](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [ （新UI）管理標籤分類](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
