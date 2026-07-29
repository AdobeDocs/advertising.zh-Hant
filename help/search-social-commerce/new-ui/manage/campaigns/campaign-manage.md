---
title: 管理行銷活動
description: 瞭解如何建立和管理廣告行銷活動。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 7dc3ea3fe1fcb701d9d064b184922ed96626cd4a
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# 管理行銷活動

*Beta功能*

行銷活動是廣告網路帳戶的主要元件。 對於大多數行銷活動型別，它是由一組廣告群組或廣告集所組成。 行銷活動設定包含行銷活動預算引數、廣告目標，以及行銷活動中所有廣告的選用追蹤引數。 行銷活動層級追蹤引數會覆寫帳戶層級引數，但本身可能在較低層級覆寫。

一旦您[透過API連線存取廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，且Search、Social和Commerce已同步處理帳戶資料與廣告網路，您就可以使用[支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)來建立新的行銷活動。 您也可以編輯及變更行銷活動的狀態。

如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

## 關於[!UICONTROL Campaigns]檢視 {#campaign-view-about}

[!UICONTROL Manage] > [!UICONTROL Campaigns]檢視表會針對選取的廣告商帳戶，列出篩選檢視表中的所有行銷活動。 您可以按一下行銷活動名稱，開啟行銷活動中的廣告群組清單。

當您在[!UICONTROL Campaigns]檢視中新增及編輯行銷活動資料時，搜尋、社交和Commerce會立即將資料變更推送至廣告網路。 搜尋、Social和Commerce也會提取行銷活動結構資料，並每日點按資料，或是在偵測到新行銷活動時更頻繁地提取資料。 對於所有同步的廣告網路，您也可以視需求同步帳戶。

搜尋、社交和Commerce會每小時從同步的[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶提取效能資料，並每天提取其他同步廣告網路帳戶的效能資料。

### 可用動作

* [建立行銷活動](#campaign-create)

* [從列重新命名行銷活動](#campaign-rename)

* [編輯行銷活動設定](#campaign-edit)

* [從列變更行銷活動的狀態或刪除行銷活動](#campaign-status)

* [將行銷活動指派至產品組合，並從產品組合中移除行銷活動](#campaign-portfolio)

* [在[!UICONTROL Campaigns]檢視中檢視效能圖表](#campaign-performance-graph)

* [為行銷活動指派競標限制，並從行銷活動中取消指派限制](#campaign-constraints)

* [將目標限制指派給行銷活動，並從行銷活動取消指派目標限制](#campaign-target-constraints)

* [將標籤分類指派給促銷活動，並從促銷活動中移除標籤分類](#campaign-classifications)

* [從[!UICONTROL Campaigns]檢視管理資料檢視報告](#campaign-reports)

## 建立行銷活動 {#campaign-create}

>[!NOTE]
>
>* 建立行銷活動之前，請在廣告商的網頁中[實作轉換追蹤標籤](/help/search-social-commerce/tracking/conversion-tracking-about.md)。
>* 若要一次建立大量行銷活動，請使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 按一下&#x200B;**[!UICONTROL Create Campaign]**。

1. 指定[百度](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-baidu.md)、[Google廣告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-google.md)、[LY廣告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yandex.md)行銷活動設定。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯]。![](/help/search-social-commerce/assets/edit-new.png "[編輯]。")並變更行銷活動設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

視建立行銷活動的廣告網路而定，您可能需要先建立關聯的廣告群組和廣告，才能將行銷活動推送至廣告網路。

## 重新命名行銷活動 {#campaign-rename}

快速重新命名行銷活動，無需開啟完整的行銷活動設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 將游標停留在行銷活動列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Rename]**。

1. 編輯名稱，然後按一下&#x200B;**[!UICONTROL Apply]**。

## 編輯行銷活動設定 {#campaign-edit}

您可以編輯個別行銷活動的設定。 您也可以一次編輯多個行銷活動的某些欄位，包括某些行銷活動詳細資料、預算選項，以及所有選定行銷活動通用的URL選項。

>[!TIP]
>
>您也可以使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->大量編輯資料 [行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 將游標停留在實體名稱上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

   * 選取行銷活動旁的核取方塊。 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[百度](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-baidu.md)，[Google廣告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-google.md)，[LY廣告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yahoo-japan.md)，<!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-meta.md), --> [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yandex.md)行銷活動設定。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯]。![](/help/search-social-commerce/assets/edit-new.png "[編輯]。")並變更行銷活動設定。

1. 按一下&#x200B;**[!UICONTROL Update]**。

根據建立行銷活動的廣告網路而定，行銷活動可能需要在推送至廣告網路之前包含廣告群組和廣告。

## 變更行銷活動的狀態 {#campaign-status}

快速變更行銷活動的狀態，無需開啟完整的行銷活動設定。

您可以暫停支援廣告網路上的任何作用中行銷活動，以停用其上的競標。 您稍後可以透過將狀態變回作用中來繼續競標。

您也可以刪除任何作用中或暫停的行銷活動。 已刪除的行銷活動會從廣告網路中刪除。 當您將其納入資料篩選器時，仍可顯示這些值，但您無法加以變更。

### 啟動或暫停行銷活動

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 將游標停留在行銷活動列上，然後按一下[!UICONTROL Status]欄旁的![編輯](/help/search-social-commerce/assets/edit.png "編輯")。

1. 變更狀態：

   * 若要啟用暫停的行銷活動，請選取&#x200B;**[!UICONTROL Active]**。

   * 若要暫停作用中的行銷活動，請選取&#x200B;**[!UICONTROL Paused]**。

### 刪除行銷活動

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 執行下列任一項作業：

   * 將游標停留在行銷活動列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Delete]**。

   * 將游標停留在行銷活動列上，然後按一下[!UICONTROL Status]欄旁的![編輯](/help/search-social-commerce/assets/edit.png "編輯")。 選取&#x200B;**[!UICONTROL Deleted]**。

## 將行銷活動指派至投資組合 {#campaign-portfolio}

將行銷活動指派給最佳化的產品組合，可讓Search、Social和Commerce針對行銷活動中的關鍵字和廣告，最佳化出價、行銷活動預算和競標策略目標。 您可以在建立投資組合時，或透過編輯投資組合的設定，從[!UICONTROL Campaigns]檢視將行銷活動指派給投資組合。

並非所有行銷活動型別和廣告網路都符合最佳化條件；請參閱您可以包含在產品組合中的[支援行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)清單。 此外，請確認每個行銷活動競標策略[&#128279;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)的最佳化支援。

>[!NOTE]
>
>每個行銷活動只能指派給一個投資組合。 如果您將已與其他投資組合關聯的行銷活動指派給新投資組合，則會將其從原始投資組合中移除。

### 從[!UICONTROL Campaigns]檢視將行銷活動指派給現有投資組合

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取每個行銷活動旁的核取方塊，以指派至單一投資組合。

1. 在大量動作工具列中，按一下「**+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]**」。

1. 選取投資組合。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

### 從[!UICONTROL Campaigns]檢視將行銷活動指派給新的投資組合

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取您要為其建立新投資組合的每個行銷活動旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**。

1. 在[!UICONTROL Create Portfolio]畫面中，指定投資組合設定。

   您先前選取的行銷活動已指派給行銷活動。 您可以選擇編輯投資組合的行銷活動清單。

   如需產品組合設定的詳細資訊，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

### 從[!UICONTROL Portfolios]檢視變更投資組合的行銷活動指派

當您從產品組合中移除行銷活動時，搜尋、社交和Commerce無法最佳化該行銷活動的出價、行銷活動預算和競標策略目標。

此動作會記錄在該投資組合的變更歷史記錄中。

如需最佳化的詳細資訊，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 選取投資組合旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 在投資組合設定中，前往[!UICONTROL Assign Campaigns]區段並變更行銷活動指派。

   如需產品組合設定的詳細資訊，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 檢閱設定並視需要進行變更，然後按一下&#x200B;**[!UICONTROL Save]**。

## 管理行銷活動的競標限制指派 {#campaign-constraints}

每個圖元只能有一個限制。 限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體指派限制。

取消指定限制會移除與帳號元件及其所有子元件的關聯，且這些元件無法再使用該限制的報表資料。 取消指定限制並不會刪除限制或帳戶元件本身。

>[!NOTE]
>
>作用中限制僅限制最佳化舊關鍵字層級產品組合中已指派競標單位的競標。 若競標單位位於作用中產品組合、混合產品組合或不在產品組合中，則會忽略這些專案。

### 從新[!UICONTROL Campaigns]檢視將競標限制指派給選取的行銷活動

您可以將單一限制指派給一或多個行銷活動。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取您要指派單一限制之每個行銷活動旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

### 從舊版[!UICONTROL Campaigns]檢視將競標限制指派給選取的搜尋競標單位

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，選取帳戶元件檢視。

1. 選取每個相關列旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取適用的限制。

1. （選擇性）輸入其他詳細資料：

   1. 在[!UICONTROL Additional Details]旁邊，按一下&#x200B;**[!UICONTROL Open]**&#x200B;以展開詳細資料。

   1. 輸入選用的&#x200B;**[!UICONTROL Project Name]**&#x200B;和/或選用的&#x200B;**[!UICONTROL Description]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

### 從新的[!UICONTROL Campaigns]檢視中移除所選行銷活動的競標限制

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取每個行銷活動旁的核取方塊，您會從中取消指派限制。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

### 從舊版[!UICONTROL Campaigns]檢視移除搜尋競標單位的競標條件約束

>[!NOTE]
>
>若要刪除限制，使其無法用於未來用途，請參閱「競標限制」上「最佳化指南」一章中的「刪除搜尋競標單位的限制」，可於搜尋、社交和Commerce中使用。<!-- verify convention for referencing Optimization Guide here -->

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，選取帳戶元件檢視。

1. 選取要從中移除限制之每個元件旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 在確認對話方塊中，選取&#x200B;**[!UICONTROL Yes, Unassign]**。

## 管理行銷活動的目標限制指派 {#campaign-target-constraints}

### 從新[!UICONTROL Campaigns]檢視指派目標限制給選取的行銷活動

您可以將單一目標限制指派給一或多個行銷活動。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取您要指派單一目標限制之每個行銷活動旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

### 從新[!UICONTROL Campaigns]檢視中移除所選行銷活動的目標限制

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取每個行銷活動旁的核取方塊，您會從中取消指派目標限制。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

## 指派標籤分類至行銷活動 {#campaign-classifications}

>[!NOTE]
>
>標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

### 指派分類值給行銷活動

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取您要指派標籤值的每個行銷活動旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**。

1. 請針對每個適用的分類值，執行下列動作：

   1. 在&#x200B;**[!UICONTROL Classifications]**&#x200B;欄中指定分類：

      * 若要使用現有的分類，請按一下分類名稱將其展開。

      * 若要建立分類，請按一下欄標題中的[!UICONTROL +]。 在輸入欄位中輸入分類名稱，然後按一下[儲存] ![&#x200B; &#x200B;](/help/search-social-commerce/assets/save-checkmark.png " [儲存] ")，立即儲存分類。 若要使用新分類，請按一下分類名稱將其展開。

        名稱必須包含[ASCII字元32-126](https://www.asciitable.com/)，最大長度為27個單位元組字元。

   1. 在&#x200B;**[!UICONTROL Value Name]**&#x200B;欄中，指定所選分類的值：

      * 若要使用現有值，請選取該值。

      * 若要建立值，請按一下欄標題中的[!UICONTROL +]。 在輸入欄位中輸入值，然後按一下![儲存](/help/search-social-commerce/assets/save-checkmark.png "儲存")，立即儲存值並依預設選取。

        長度上限為100個字元，可包含ASCII和非ASCII字元。

1. 按一下&#x200B;**+[!UICONTROL Assign Now]**。

### 從行銷活動中移除標籤分類值

移除分類值會移除與帳戶元件及其所有子元件的關聯。 這些元件不再提供分類值的報表資料。 移除分類值不會刪除值或帳戶元件。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取每個行銷活動旁的核取方塊，您會從其中移除標籤值。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 選取每個分類值旁的核取方塊，以從選取的實體中移除。

   若要選取所有指派的值，請按一下&#x200B;**[!UICONTROL Select All]**。 若要取消選取所有指派的值，請按一下&#x200B;**[!UICONTROL Deselect All]**。

1. 按一下&#x200B;**[!UICONTROL Unassign Selected]**。

## 在[!UICONTROL Campaigns]檢視中檢視效能圖表 {#campaign-performance-graph}

開啟並設定績效圖表，其中最多可包含三個量度，總計是檢視中指定日期範圍之所有促銷活動的量度。

### 檢視效能圖表

1. 在資料表的上方，按一下![圖表](/help/search-social-commerce/assets/charts.png "圖表")。

1. （選用）指定要納入圖表的貨幣和最多三個量度。

### 隱藏可見的效能圖表

* 在資料表的上方，按一下![圖表](/help/search-social-commerce/assets/charts.png "圖表")。

## 從[!UICONTROL Campaigns]檢視管理資料檢視報告 {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

產生一份報表，其中包含[!UICONTROL Campaigns]檢視中一或多個行銷活動的資料列，然後以Microsoft Excel工作表檔案（XLXS格式）格式下載報表。 報表會包含檢視中的所有可見欄。

您可以刪除任何產生的報表。

另請參閱&quot;>* [（舊版UI）從行銷活動管理檢視下載資料](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot;和&quot;[（舊版UI）從[!UICONTROL Downloads]功能表](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)刪除效能資料報告或Bulksheet檔案。&quot;

### 產生含有已篩選資料列的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 指定要下載其資料的行銷活動：

   * 若要下載特定行銷活動的資料，請選取行銷活動旁的核取方塊。

   * 若要下載所有行銷活動的資料，您不需要選取任何核取方塊。 預設會包含所有行銷活動。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]設定中，輸入唯一的報告名稱，然後按一下&#x200B;**[!UICONTROL Generate]**。

   依預設，檔案名稱為「campaign_YYYYYMMDD_NNNN」，其中「NNNN」為循序工作編號（例如「campaign_20250402_1326）。

   檔案已新增至[!UICONTROL Recently Generated]清單。

1. （選擇性）若要在檔案完成後下載檔案，請按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 下載完成的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 刪除已完成的報告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![刪除](/help/search-social-commerce/assets/delete-new.png "刪除")。

>[!MORELIKETHIS]
>
>* [管理搜尋競標單位的限制](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理廣告群組的限制指派](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [管理關鍵字](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)的限制指派
>* [管理位置的限制指派](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [&#x200B; （舊版UI）從行銷活動管理檢視下載資料](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [（舊版UI）從[!UICONTROL Downloads]功能表刪除效能資料報告或大量表單檔案](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] 行銷活動設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-baidu.md)
>* [[!DNL Google Ads] 行銷活動設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-google.md)
>* [[!DNL LY Ads] 行銷活動設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] 行銷活動設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-microsoft.md)
>* [[!DNL Yandex] 行銷活動設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-meta.md) -->

