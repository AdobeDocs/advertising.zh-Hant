---
title: 管理廣告群組
description: 瞭解如何建立及管理廣告群組。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e120af366651028227306e993e73f125f29a431f
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# 管理廣告群組

<!-- Go through all -->

*Beta功能*

廣告群組包含一組廣告及其相關關鍵字。 行銷活動中以顯示網路為目標的廣告群組也可以包含版位，即顯示網路上的廣告可出現位置。 適用於廣告群組所有元件的廣告群組設定，會因廣告網路而異。

當您[透過API連線存取廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，且Search、Social和Commerce已將帳戶資料與廣告網路同步之後，您就可以為[支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)建立廣告群組。 您也可以編輯及變更廣告群組的狀態。

如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

## 關於[!UICONTROL Ad Groups]檢視 {#ad-group-view-about}

[!UICONTROL Manage] > [!UICONTROL Ad Groups]檢視會列出所選廣告商帳戶之篩選檢視中的所有廣告群組。

### 可用動作

* [建立廣告群組](#ad-group-create)

* [從列重新命名廣告群組](#ad-group-rename)

* [編輯廣告群組設定](#ad-group-edit)

* [從列中變更廣告群組的狀態或刪除廣告群組](#ad-group-status)

* [在[!UICONTROL Ad Groups]檢視中檢視效能圖表](#ad-group-performance-graph)

* [將競標限制指派給廣告群組，並從廣告群組取消指派限制](#ad-group-constraints)

* [將標籤分類指派給廣告群組，並從廣告群組移除標籤分類](#ad-group-classifications)

* [從[!UICONTROL Ad Groups]檢視管理資料檢視報告](#ad-group-reports)

## 建立廣告群組 {#ad-group-create}

>[!TIP]
>
>若要一次建立大量廣告群組，請使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 按一下&#x200B;**[!UICONTROL Create Ad Group]**。

1. 指定[百度](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)、[Google廣告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)、[LY廣告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)廣告群組設定。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯]。![](/help/search-social-commerce/assets/edit-new.png "[編輯]。")並變更廣告群組設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

稍後，您可以設定廣告群組中個別關鍵字或位置的競標，選擇性地覆寫廣告群組層級的競標。

## 重新命名廣告群組 {#ad-group-rename}

快速重新命名廣告群組，無需開啟完整的廣告群組設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 將游標停留在廣告群組列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Rename]**。

1. 編輯名稱，然後按一下&#x200B;**[!UICONTROL Apply]**。

## 編輯廣告群組設定 {#ad-group-edit}

您可以編輯個別廣告群組的設定。 您也可以一次編輯多個廣告群組的部分欄位，包括所有選定廣告群組通用的部分廣告群組詳細資料、預算選項和URL選項。

>[!TIP]
>
>您也可以使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->大量編輯資料 [行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 執行下列任一項作業：

   * 將游標停留在實體名稱上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

   * 選取廣告群組旁的核取方塊。 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[百度](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)、[Google廣告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)、[LY廣告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)廣告群組設定。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯]。![](/help/search-social-commerce/assets/edit-new.png "[編輯]。")並變更廣告群組設定。

1. 按一下&#x200B;**[!UICONTROL Update]**。

## 變更廣告群組的狀態 {#ad-group-status}

快速變更廣告群組的狀態，無需開啟完整的廣告群組設定。

您可以暫停支援廣告網路上的任何作用中廣告群組，以停用其競標。 您稍後可以透過將狀態變回作用中來繼續競標。

您也可以刪除任何作用中或暫停的廣告群組。 已刪除的廣告群組會從廣告網路中刪除。 當您將其納入資料篩選器時，仍可顯示這些值，但您無法加以變更。

### 啟動或暫停廣告群組

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 將游標停留在廣告群組列上，然後按一下[!UICONTROL Status]欄旁的![編輯](/help/search-social-commerce/assets/edit.png "編輯")。

1. 變更狀態：

   * 若要啟用暫停的廣告群組，請選取&#x200B;**[!UICONTROL Active]**。

   * 若要暫停使用中的廣告群組，請選取&#x200B;**[!UICONTROL Paused]**。

### 刪除廣告群組

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 執行下列任一項作業：

   * 將游標停留在廣告群組列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Delete]**。

   * 將游標停留在廣告群組列上，然後按一下[!UICONTROL Status]欄旁的![編輯](/help/search-social-commerce/assets/edit.png "編輯")。 選取&#x200B;**[!UICONTROL Deleted]**。

## 管理廣告群組的競標限制指派 {#ad-group-constraints}

每個圖元只能有一個限制。 限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體指派限制。

取消指定限制會移除與帳號元件及其所有子元件的關聯，且這些元件無法再使用該限制的報表資料。 取消指定限制並不會刪除限制或帳戶元件本身。

### 從新[!UICONTROL Ad Groups]檢視將競標限制指派給選取的廣告群組

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 選取您要將單一限制指定至的每個廣告群組旁的核取方塊。

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

### 從新[!UICONTROL Ad Groups]檢視中移除所選廣告群組的競標條件約束

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 選取每個廣告群組旁的核取方塊，您會從中取消指派限制。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

### 從舊版[!UICONTROL Campaigns]檢視移除搜尋競標單位的競標條件約束

>[!NOTE]
>
>若要刪除限制，使其無法用於未來用途，請參閱「競標限制」上「最佳化指南」一章中的「刪除搜尋競標單位的限制」，可於搜尋、社交和Commerce中使用。

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，選取帳戶元件檢視。

1. 選取要從中移除限制之每個元件旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 在確認對話方塊中，選取&#x200B;**[!UICONTROL Yes, Unassign]**。

## 將標籤分類指派給廣告群組 {#ad-group-classifications}

>[!NOTE]
>
>標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

### 將分類值指派給廣告群組

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 選取您要指派標籤值的每個廣告群組旁的核取方塊。

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

### 從廣告群組移除標籤分類值

移除分類值會移除與帳戶元件及其所有子元件的關聯。 這些元件不再提供分類值的報表資料。 移除分類值不會刪除值或帳戶元件。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 選取每個廣告群組旁的核取方塊，您將從中移除標籤值。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 選取每個分類值旁的核取方塊，以從選取的實體中移除。

   若要選取所有指派的值，請按一下&#x200B;**[!UICONTROL Select All]**。 若要取消選取所有指派的值，請按一下&#x200B;**[!UICONTROL Deselect All]**。

1. 按一下&#x200B;**[!UICONTROL Unassign Selected]**。

## 在[!UICONTROL Ad Groups]檢視中檢視效能圖表 {#ad-group-performance-graph}

開啟並設定效能圖表，其中最多可包含三個合計檢視表內指定日期範圍內所有廣告群組的量度。

### 檢視效能圖表

1. 在資料表的上方，按一下![圖表](/help/search-social-commerce/assets/charts.png "圖表")。

1. （選用）指定要納入圖表的貨幣和最多三個量度。

### 隱藏可見的效能圖表

* 在資料表的上方，按一下![圖表](/help/search-social-commerce/assets/charts.png "圖表")。

## 從[!UICONTROL Ad Groups]檢視管理資料檢視報告 {#ad-group-reports}

產生一份報表，其中包含[!UICONTROL Ad Groups]檢視中一或多個廣告群組的資料列，然後以Microsoft Excel工作表檔案（XLXS格式）格式下載報表。 報表會包含檢視中的所有可見欄。

您可以刪除任何產生的報表。

另請參閱&quot;>* [（舊版UI）從行銷活動管理檢視下載資料](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot;和&quot;[（舊版UI）從[!UICONTROL Downloads]功能表](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)刪除效能資料報告或Bulksheet檔案。&quot;

### 產生含有已篩選資料列的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 指定您要下載其資料的廣告群組：

   * 若要下載特定廣告群組的資料，請選取廣告群組旁的核取方塊。

   * 若要下載所有廣告群組的資料，您不需要選取任何核取方塊。 預設會包含所有廣告群組。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]設定中，輸入唯一的報告名稱，然後按一下&#x200B;**[!UICONTROL Generate]**。

   依預設，檔案名稱為「ad group_YYYYYMMDD_NNNN」，其中「NNNN」為循序工作編號（例如「ad group_20250402_1326）。

   檔案已新增至[!UICONTROL Recently Generated]清單。

1. （選擇性）若要在檔案完成後下載檔案，請按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 下載完成的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 刪除已完成的報告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![刪除](/help/search-social-commerce/assets/delete-new.png "刪除")。

>[!MORELIKETHIS]
>
>* [管理搜尋競標單位的限制](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理行銷活動的限制指派](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [管理關鍵字](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)的限制指派
>* [管理位置的限制指派](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [&#x200B; （舊版UI）從行銷活動管理檢視下載資料](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [（舊版UI）從[!UICONTROL Downloads]功能表刪除效能資料報告或大量表單檔案](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] 廣告群組設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] 廣告群組設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)
>* [[!DNL LY Ads] 廣告群組設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] 廣告群組設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] 廣告群組設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)
