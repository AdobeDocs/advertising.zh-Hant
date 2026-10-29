---
title: 管理版位
description: 瞭解如何建立和管理Google廣告版位和負面版位，並為版位指派限制。
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1383'
ht-degree: 0%
---
# 管理版位

*Beta功能*

僅&#x200B;*[!DNL Google Ads]個帳戶*

版位是顯示網路上可顯示廣告的位置。 刊登版位設定包含最高出價和選用的追蹤引數。 位置層級設定會覆寫廣告群組或行銷活動設定。 負數版位會防止廣告在指定網站上顯示。

當您[透過API連線存取廣告網路帳戶](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)，且Search、Social和Commerce已將帳戶資料與廣告網路同步之後，您就可以在[支援的促銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md) （以顯示網路為目標）中建立廣告群組的版位。 您也可以編輯和變更版位狀態，以及建立和刪除負面版位。

>[!NOTE]
>
>[!DNL Google Ads]未提供廣告層級的成效資料給位置。

## 關於[!UICONTROL Placements]檢視 {#placement-view-about}

[!UICONTROL Targeting] > [!UICONTROL Placements]檢視包含所選廣告商帳戶的兩個標籤：

* [!UICONTROL Placements]索引標籤會列出篩選檢視中的所有可競標位置。

* [!UICONTROL Negatives]索引標籤會列出篩選檢視中的所有負面版位。

檢視頁面需要[!UICONTROL View Placements]許可權。 建立版位或負面版位、編輯版位、變更版位狀態，以及刪除版位或負面版位需要[!UICONTROL Edit Placements]許可權。

### 可用動作

* [建立產品建議放置環境](#placement-create)

* [建立負面版位](#placement-negative-create)

* [編輯位置設定](#placement-edit)

* [變更刊登版位的狀態，或刪除、刊登版位和負刊登版位](#placement-status)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

* [將限制指派給版位，並從版位取消指派限制](#placement-constraints)

* [將標籤分類指派給位置](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## 建立產品建議放置環境 {#placement-create}

>[!TIP]
>
>若要一次建立大量版位，請使用[行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;索引標籤上，按一下&#x200B;**[!UICONTROL Create Placement]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步驟中，選取網路、帳戶、行銷活動和廣告群組。

1. 輸入[位置設定](#placement-create-settings)。

   若要建立多個版位，請以逗號分隔網站URL。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯] ![&#x200B; &#x200B;](/help/search-social-commerce/assets/edit-new.png " [編輯] ") **[!UICONTROL Edit]**&#x200B;並變更實體和/或位置設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 建立負面版位 {#placement-negative-create}

您可以針對以顯示網路為目標的[!DNL Google Ads]行銷活動或廣告群組建立負面的版位。

>[!NOTE]
>
>您也可以在[廣告群組設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)和[行銷活動設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)中建立和編輯負面的版位。

>[!TIP]
>
>若要一次建立大量負面刊登版位，請使用[行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Negatives]**&#x200B;索引標籤上，按一下&#x200B;**[!UICONTROL Create Negative]**，然後按&#x200B;**[!UICONTROL Campaign Negative]**&#x200B;或&#x200B;**[!UICONTROL Ad Group Negative]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步驟中，選取網路、帳戶、行銷活動，以及（針對廣告群組層級的負面位置）廣告群組。

1. 在&#x200B;**[!UICONTROL Manage Websites]**&#x200B;步驟中，輸入負面的網站URL，例如`www.example.com`或`example.com/shoes`。

   請使用逗號分隔多個URL。 此表單接受網站URL，而非主題或類別字串。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯] ![&#x200B; &#x200B;](/help/search-social-commerce/assets/edit-new.png " [編輯] ") **[!UICONTROL Edit]**，然後變更實體和/或負面的網站URL。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 編輯位置設定 {#placement-edit}

您可以編輯一或多個位置的狀態、競標、基本URL和追蹤範本。 您無法變更目標網站URL或編輯已刪除的位置。

>[!TIP]
>
>若要一次編輯大量位置資料，請使用[行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;索引標籤上，選取要編輯之每個位置旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Edit Placements]**&#x200B;面板中，編輯[位置設定](#placement-edit-settings)。

   若為多個版位，您的變更會套用至所有選取的版位。 您可以將出價設定為指定值，或透過指定百分比或貨幣金額（有限制）來增加或減少出價。 對於URL，您可以取代現有值、尋找及取代文字、新增首碼或附加尾碼。

   當選取的位置使用多種貨幣時，會停用競標編輯。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 變更刊登版位和負面刊登版位的狀態 {#placement-status}

您可以暫停作用中、可競標的位置，以停用該位置的競標。 您稍後可以透過將狀態變回作用中來繼續競標。

您也可以刪除作用中或暫停的版位或負的版位。 刪除的位置會從廣告網路中刪除。 當您將其納入資料篩選器時，仍可顯示這些值，但您無法加以變更。

### 啟動或暫停位置

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;索引標籤上，選擇性地篩選清單，然後選取您要變更其狀態的每個位置旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Placement Details]**&#x200B;區段中，變更&#x200B;**[!UICONTROL Status]**：

   * 若要啟用暫停的版位，請選取&#x200B;**[!UICONTROL Active]**。

   * 若要暫停作用中的位置，請選取&#x200B;**[!UICONTROL Paused]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

### 刪除版位或負面版位

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;或&#x200B;**[!UICONTROL Negatives]**&#x200B;索引標籤上，選擇性地篩選清單，然後選取要刪除的每個位置或負面位置旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

## 管理位置的限制指派 {#placement-constraints}

您可以為行銷活動、廣告群組、關鍵字、位置、單位層級產品群組及動態搜尋目標指派及移除競標限制。 每個圖元只能有一個限制。

限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體指派限制。

取消指定限制會移除與帳號元件及其所有子元件的關聯，且這些元件無法再使用該限制的報表資料。 取消指定限制並不會刪除限制或帳戶元件本身。

>[!NOTE]
>
>* 如果您稍後編輯非可變廣告的關鍵字或廣告復本（因此建立新的關鍵字或廣告），則限制不會指派給新圖元。
>* 作用中限制僅限制最佳化舊關鍵字層級產品組合中已指派競標單位的競標。 若競標單位位於作用中產品組合、混合產品組合或不在產品組合中，則會忽略這些專案。

### 將限制指派給位置 {#placement-constraint-assign}

您可以將單一限制指派給一或多個位置。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;標籤上，選取要指派單一限制之每個位置旁的核取方塊。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

### 從版位取消指派限制 {#placement-constraint-unassign}

取消指派限制並不會刪除它。 若要刪除限制，使其無法供未來使用，請參閱&quot;[管理搜尋競標單位的限制](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status)&quot;。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;索引標籤上，選取要從中取消指派限制之每個位置旁的核取方塊。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

## 位置設定 {#placement-settings}

### 建立版位時的設定 {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]：**&#x200B;廣告網路。 僅支援[!DNL Google Ads]。

**[!UICONTROL Account]：**&#x200B;廣告網路帳戶。

**[!UICONTROL Campaign]：**&#x200B;行銷活動。

**[!UICONTROL Ad Group]：**&#x200B;廣告群組。

#### [!UICONTROL Placement Details]

顯示網路上可顯示您廣告的&#x200B;**[!UICONTROL Placements]：**&#x200B;網站。 請輸入有效的網站URL，例如`www.example.com`、`example.com`或`example.com/shoes`。 請使用逗號分隔多個URL。 URL不能包含問號(`?`)。

若要改為排除網站，請從「[!UICONTROL Targeting]」>「[!UICONTROL Placements]」>「[!UICONTROL Negatives]」索引標籤中[建立負面版位](#placement-negative-create)，或使用廣告群組和行銷活動設定。

**[!UICONTROL Status]：**&#x200B;位置的顯示狀態： *[!UICONTROL Active]* （啟用競標）或&#x200B;*[!UICONTROL Paused]* （停用競標）。

#### [!UICONTROL Bids]

**[!UICONTROL Bid]：** （選用）根據行銷活動競標策略，針對位置型廣告的最高每次點按成本(CPC)或每千次可檢視曝光成本(vCPM)。 此值會覆寫廣告群組層級競標。

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>新UI建立表單需要基底URL和追蹤範本（指定時）以`http://`或`https://`開頭。

### 編輯版位時的設定 {#placement-edit-settings}

[!UICONTROL Edit Placements]面板支援一或多個選取位置的下列設定。 您無法變更目標網站URL。

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]：** *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]：**&#x200B;如何變更出價：

* *[!UICONTROL Set to]：*&#x200B;以指定的值取代現有的競標。

* *[!UICONTROL Increase]：*&#x200B;將現有競標增加指定的金額或百分比。

* *[!UICONTROL Decrease]：*&#x200B;將現有競標減少指定的金額或百分比。

**[!UICONTROL Modifier type]：** （增加或減少）調整使用&#x200B;*[!UICONTROL Currency]*&#x200B;或&#x200B;*[!UICONTROL Percentage]*。

**[!UICONTROL Set value]：**&#x200B;新的競標或調整金額。 最小值為0.01。

**[!UICONTROL Max limit]：** （增加或減少；選擇性）調整後競標的上限。 上升時為最高出價，下降時為最低出價。 最小限制值為0.01。

當選取的位置使用多種貨幣時，會停用競標編輯。

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**，**[!UICONTROL Tracking Template]：**&#x200B;針對每個欄位，選取如何修改值：

* *[!UICONTROL Set To]：*&#x200B;取代值。 輸入以`http://`或`https://`開頭的有效網站URL。

* *[!UICONTROL Find/Replace]：*&#x200B;取代值內的指定文字。 輸入要尋找的文字和取代文字。

* *[!UICONTROL Add Suffix]：*&#x200B;附加文字到值。 輸入字尾文字。

* *[!UICONTROL Add Prefix]：*&#x200B;在值的開頭新增文字。 輸入前置詞文字。

>[!NOTE]
>
>所有新的基底URL都必須是以`http://`或`https://`開頭的有效URL。

>[!MORELIKETHIS]
>
>* [管理搜尋競標單位的限制](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理標籤分類](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
