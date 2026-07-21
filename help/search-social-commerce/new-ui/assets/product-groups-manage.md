---
title: 管理購物產品群組
description: 瞭解、建立、編輯和刪除購物產品群組，以及參考Google Ads和Microsoft Advertising的產品群組設定。
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# 管理購物產品群組

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]購物行銷活動*

您可以在[!UICONTROL Assets] > [!UICONTROL Shopping]的[!UICONTROL Product Groups]檢視中建立及管理產品群組。

您可以在[ [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)中檢視產品群組的相關資料。

## 什麼是產品群組？

在購物行銷活動中，您的產品群組（而非關鍵字）會決定您的商家中心帳戶中要顯示哪些購物廣告的產品。 每個產品群組都以單一產品屬性（例如，類別、產品型別、品牌、條件、產品ID或自訂標籤）為基礎，並對所有相符產品使用相同出價。 您可以加入或排除每個群組中產品的競標。

您可以在廣告群組層級設定產品群組，以決定您的商家中心帳戶中的哪些產品會出現在廣告群組的購物廣告中。 即使廣告群組不包含廣告實體，廣告網路仍會顯示產品的廣告。

當同一個產品包含在多個促銷活動中時，廣告網路會先使用促銷活動優先順序來判斷哪個促銷活動（及相關競標）適用於廣告拍賣。 當所有行銷活動具有相同的優先順序時，則適用最高競價的行銷活動。

如需[!DNL Google]購物行銷活動和廣告的詳細資訊，請參閱[實作 [!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)和[Google廣告檔案](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1)。 如需[!DNL Microsoft]購物行銷活動的詳細資訊，請參閱[實作 [!DNL Microsoft Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)和[[!DNL Microsoft Advertising] 檔案](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500)。

>[!NOTE]
>
>[!DNL Google Ads]無法支援在最高成效行銷活動中列出群組。 若要管理和檢視清單群組的資料，請使用[!DNL Google Ads]編輯器。

### 產品群組階層

您必須先建立名為「[!UICONTROL All Products]」的全包含式產品群組，才能使用廣告群組的特定屬性建立產品群組。 您可以從此父產品群組，建立產品子集的子產品群組，也可以從子產品群組建立子系。 一旦您為廣告群組建立第一個子產品群組，就會使用預設廣告群組競標，自動建立另一個名為「[!UICONTROL Everything Else]」的產品群組。 當您新增更多產品群組時，&quot;[!UICONTROL Everything Else]&quot;群組會適當地調整，使其構成不在其他產品群組中的所有產品。

在廣告群組內，您可以建立最多七個層級的產品群組（不包括&quot;[!UICONTROL All Products]&quot;）來包含或排除競標，且每個層級中一或多個產品群組皆以相同屬性為目標（例如，[!UICONTROL Brand]=Acme代表一個產品群組，[!UICONTROL Brand]=AcmePlus代表另一個相同層級）。 父產品群組稱為細分，而最低的細分層級稱為單位。 您可以在單位層級設定競標和追蹤範本，或完全排除競標。 廣告群組的整組作用中產品群組會依階層套用，以決定符合資格的產品。 例如，如果您將[!UICONTROL All Products]細分為[!UICONTROL Brand]=AcmeBasic和[!UICONTROL Brand]=AcmePlus，然後進一步將每個產品群組細分為[!UICONTROL Condition]=New和設定出價，則只有具有AcmeBasic和AcmePlus品牌的新產品才會被廣告或從廣告中排除。

![產品群組集範例](/help/search-social-commerce/assets/product-group-list-new.png "產品群組集範例")

![產品群組階層範例](/help/search-social-commerce/assets/product-group-tree-new.png "產品群組階層範例")

### 產品篩選器 {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

另請參閱[!DNL Google Ads]說明&quot;[使用產品群組](https://support.google.com/google-ads/answer/6275317)管理購物行銷活動&quot;以及[!DNL Microsoft Advertising]說明&quot;[瞭解並使用產品群組](https://help.ads.microsoft.com/#apex/bae/en/56782)&quot;。

| 購物網路 | 產品Dimension | 屬性 | 附註 |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]： [!UICONTROL Category=]<br><br>Microsoft： [!UICONTROL Category 1=]至[!UICONTROL Category 5=] | \[類別識別碼\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[品牌\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[專案識別碼\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]： [!UICONTROL Product Type (1st level)=]至[!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]： [!UICONTROL Product Type=] | \[產品型別\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=]至[!UICONTROL Custom Label 4=] | \[自訂標籤的屬性\] | — |
| [!DNL Google Ads] | 頻道= | [!UICONTROL Local], [!UICONTROL Online] | 若要只顯示本機產品或線上產品的廣告。<br><br><b>注意：</b>若要建立本機產品的廣告，必須啟用[本機詳細目錄廣告]選項，而且您必須透過[!DNL Google Merchant Center]參與本機購物方案。 |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | 是否顯示只適用於單一管道（僅限本機或僅限線上）的產品廣告，或是適用於多個管道（本機或線上）的產品廣告。 |

## [!UICONTROL Product Groups]檢視

在[!UICONTROL Assets] > [!UICONTROL Shopping]檢視的[!UICONTROL Product Groups]檢視會列出所選廣告商帳戶之篩選檢視中的所有產品群組。 您也可以建立和管理產品群組。

### 可用的動作<!-- Go through all -->

* [建立&quot;[!UICONTROL All Products]&quot;產品群組](#product-group-create-all-products)

* [在現有產品群組中建立子產品群組節點](#node-add)

* 編輯產品群組節點的設定：

  * [編輯任何設定](#node-edit)

  * [僅編輯[!UICONTROL Tracking Template]](#node-edit-tracking-template)

  * [僅編輯[!UICONTROL Max CPC]](#node-edit-maxcpc)

* [刪除產品群組節點](#node-delete)

* [將限制](#constraint-assign)指派給產品群組，以及[從產品群組移除限制](#constraint-unassign)

* [將標籤分類](#classification-values-assign)指派給產品群組，以及[從產品群組移除標籤分類](#classification-values-remove)

>[!NOTE]
>
>您可以上傳[大量工作表檔案](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)並將它們張貼到廣告網路，一次建立及編輯大量產品群組資料（包括標籤和限制指派）。

## 建立&quot;[!UICONTROL All Products]&quot;產品群組 {#product-group-create-all-products}

您必須先建立名為「[!UICONTROL All Products]」的全包含式產品群組，才能建立具有特定屬性的產品群組。 每個廣告群組只能有一個&quot;[!UICONTROL All Products]&quot;群組。

>[!TIP]
>
>若要同時建立多個帳戶元件，請使用[行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Create Product Group]**。

1. 選取廣告網路、帳戶、行銷活動和廣告群組，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 指定[Google Ads產品群組設定](#google-ads-product-group-settings)或[Microsoft Advertising產品群組設定](#microsoft-advertising-product-group-settings)。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯] ![ ](/help/search-social-commerce/assets/edit-new.png " [編輯] ")並變更[3} Google Ads產品群組設定](#google-ads-product-group-settings)或[5} Microsoft Advertising產品群組設定](#microsoft-advertising-product-group-settings)。[[

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 在現有產品群組中建立子產品群組節點 {#product-group-create-child}

當您為廣告群組建立至少包含所有的「[!UICONTROL All Products]」群組後，您可以為要納入競標或排除的產品子集建立子產品群組節點，讓一或多個產品群組在每個層級中鎖定相同的屬性（例如，一個產品群組為[!UICONTROL Brand]=Acme，而另一個層級為[!UICONTROL Brand]=AcmePlus）。 您最多可以建立7個層級的子產品群組節點，不包括&quot;[!UICONTROL All Products]&quot;。

>[!NOTE]
>
>您無法為&quot;[!UICONTROL Everything Else]&quot;產品群組建立子產品群組。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. （選擇性）若要在樹狀檢視中檢視產品群組及其子產品群組節點，請將游標停留在產品群組名稱上，按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Tree View]**。

1. 將游標停留在產品群組名稱上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL + Add Node]**。

1. 指定[Google Ads產品群組設定](#google-ads-product-group-settings)或[Microsoft Advertising產品群組設定](#microsoft-advertising-product-group-settings)。

1. 按一下&#x200B;**[!UICONTROL Center]**。

## 編輯產品群組節點的任何設定 {#node-edit}

您可以編輯廣告群組中包含之單位產品群組節點（沒有子產品群組節點的產品群組）的競標與追蹤範本。 您無法編輯已排除的單位產品群組或已包含或已排除的細分節點的任何資訊，這些節點是具有子項產品群組節點的產品群組。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. （選擇性）若要在樹狀檢視中檢視產品群組及其子產品群組節點，請將游標停留在產品群組名稱上，按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Tree View]**。

1. 將游標停留在產品群組名稱上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL + Edit Node]**。

1. 編輯[Google廣告產品群組設定](#google-ads-product-group-settings)或[Microsoft Advertising產品群組設定](#microsoft-advertising-product-group-settings)。

1. 按一下&#x200B;**[!UICONTROL Update]**。

## 僅編輯產品群組節點的[!UICONTROL Tracking Template] {#node-edit-tracking-template}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 將游標停留在產品群組名稱上，然後按一下「**[!UICONTROL ...]>[!UICONTROL Tree View]**」以在「樹狀檢視」中檢視產品群組及其子產品群組節點。

1. 在&#x200B;**[!UICONTROL Tracking Template]**&#x200B;欄中按一下![編輯](/help/search-social-commerce/assets/edit-new.png "編輯")。

1. 變更&#x200B;**[!UICONTROL Tracking Template]**&#x200B;值，然後按一下&#x200B;**[!UICONTROL Save]**。

## 僅編輯產品群組節點的[!UICONTROL Max CPC] {#node-edit-maxcpc}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 將游標停留在產品群組名稱上，然後按一下「**[!UICONTROL ...]>[!UICONTROL Tree View]**」以在「樹狀檢視」中檢視產品群組及其子產品群組節點。

1. 在&#x200B;**[!UICONTROL Max CPC]**&#x200B;欄中按一下![編輯](/help/search-social-commerce/assets/edit-new.png "編輯")。

1. 變更&#x200B;**[!UICONTROL Max CPC]**&#x200B;值，然後按一下&#x200B;**[!UICONTROL Save]**。

## 刪除產品群組節點 {#node-delete}

您可以刪除任何產品群組（當其他產品群組位於相同層級時，則除了「其他所有專案」群組），這些產品群組用於決定您的商家中心帳戶中的哪些產品包含在廣告群組的購物廣告中。 刪除產品群組將會刪除所有子產品群組。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 將游標停留在產品群組名稱上，然後按一下「**[!UICONTROL ...]>[!UICONTROL Tree View]**」以在「樹狀檢視」中檢視產品群組及其子產品群組節點。

1. 按一下&#x200B;**[!UICONTROL Status]**&#x200B;欄並選取&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

## 將限制指派給所選產品群組 {#constraint-assign}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 選取要為其指定單一限制之每個產品群組旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

## 從選取的產品群組移除限制 {#constraint-unassign}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 選取每個產品群組旁的核取方塊，您會從中取消指定限制。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

## 將分類值指派給產品群組 {#classification-values-assign}

>[!NOTE]
>
>標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 選取要指派標籤值的每個產品群組旁的核取方塊。

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

## 從產品群組中移除標籤分類值 {#classification-values-remove}

移除分類值會移除與帳戶元件及其所有子元件的關聯。 這些元件不再提供分類值的報表資料。 移除分類值不會刪除值或帳戶元件。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 選取每個產品群組旁的核取方塊，您將從中移除標籤值。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 選取每個分類值旁的核取方塊，以從選取的實體中移除。

   若要選取所有指派的值，請按一下&#x200B;**[!UICONTROL Select All]**。 若要取消選取所有指派的值，請按一下&#x200B;**[!UICONTROL Deselect All]**。

1. 按一下&#x200B;**[!UICONTROL Unassign Selected]**。

## [!DNL Google Ads]產品群組設定 {#google-ads-product-group-settings}

### 「所有產品」產品群組

**[!UICONTROL Network]：** （僅限新產品群組）廣告網路。

**[!UICONTROL Account]：** （僅限新產品群組）廣告網路帳戶名稱。

**[!UICONTROL Campaign]：** （僅限新產品群組）行銷活動。

**[!UICONTROL Ad Group]：** （僅限新產品群組）廣告群組。

**[!UICONTROL Condition]**&#x200B;或&#x200B;**[!UICONTROL Condition Type]：** （唯讀）所有產品

**[!UICONTROL Condition Value]：** （僅限現有產品群組）  

**[!UICONTROL Bid]**&#x200B;或&#x200B;**[!UICONTROL Max CPC]：** （僅包含產品群組）每次點按成本上限(CPC)，這是廣告點按的最高金額。 此值僅用於沒有子項產品群組的單位，並且將用來取代廣告群組層級值。

{{$include /help/_includes/tracking-template-google.md}}

此範本會覆寫較高層級的範本，且僅用於沒有子產品群組的單位。 不包括為帳戶或行銷活動指定的任何附加引數。 不包括為帳戶或行銷活動指定的任何附加引數。

### 所有其他產品群組

**[!UICONTROL Condition Type]**&#x200B;和&#x200B;**[!UICONTROL Condition Value]：** （現有產品群組的唯讀）要鎖定的產品維度。 針對新產品群組，輸入產品目標定位所依據的維度，以及所選資訊類別的合格屬性（例如，依品牌進行定位時為「Acme」，或依條件進行定位時為「New」）。

一旦您為特定產品維度（即「所有產品」以外的維度）建立產品群組，搜尋、社交和Commerce就會自動為「其他所有專案」建立產品群組。

如需可用產品維度的清單，請參閱&quot;[產品篩選器](#product-filters)&quot;。 根據行銷活動的[!UICONTROL Inventory Filter]設定，您的維度清單可能會受到限制。

**[!UICONTROL Excluded]：** （新產品群組為選用；現有產品群組為唯讀）排除相符產品廣告的競標。

**[!UICONTROL Max CPC]：** （僅包含產品群組）每次點按成本上限(CPC)，這是支付廣告點按的最高金額。 此值僅用於沒有子項產品群組的單位，並且將用來取代廣告群組層級值。

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

此範本會覆寫較高層級的範本，且僅用於沒有子產品群組的單位。

## [!DNL Microsoft Advertising]產品群組設定 {#microsoft-advertising-product-group-settings}

### 「所有產品」產品群組

**[!UICONTROL Network]：** （僅限新產品群組）廣告網路。

**[!UICONTROL Account]：** （僅限新產品群組）廣告網路帳戶名稱。

**[!UICONTROL Campaign]：** （僅限新產品群組）行銷活動。

**[!UICONTROL Ad Group]：** （僅限新產品群組）廣告群組。

**[!UICONTROL Condition]**&#x200B;或&#x200B;**[!UICONTROL Condition Type]：** （唯讀）所有產品

**[!UICONTROL Condition Value]：** （僅限現有產品群組）  

**[!UICONTROL Bid]**&#x200B;或&#x200B;**[!UICONTROL Max CPC]：** （僅包含產品群組）每次點按成本上限(CPC)，這是廣告點按的最高金額。 此值僅用於沒有子項產品群組的單位，並且將用來取代廣告群組層級值。

**[!UICONTROL Base URL]：** （僅限新產品群組）未使用<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

此範本會覆寫較高層級的範本，且僅用於沒有子產品群組的單位。

### 所有其他產品群組

**[!UICONTROL Condition Type]**&#x200B;和&#x200B;**[!UICONTROL Condition Value]：** （現有產品群組的唯讀）要鎖定的產品維度。 針對新產品群組，輸入產品定位所依據的維度，以及所選資訊類別的合格屬性（例如，依品牌定位時為「Acme」，或依條件定位時為「New」）。

一旦您為特定產品維度（即「所有產品」以外的維度）建立產品群組，搜尋、社交和Commerce就會自動為「其他所有專案」建立產品群組。

如需可用產品維度的清單，請參閱&quot;[產品篩選器](#product-filters)&quot;。 根據行銷活動的[!UICONTROL Inventory Filter]設定，您的維度清單可能會受到限制。

**[!UICONTROL Excluded]：** （新產品群組為選用；現有產品群組為唯讀）排除相符產品廣告的競標。

**[!UICONTROL Max CPC]：** （僅包含產品群組）每次點按成本上限(CPC)，這是支付廣告點按的最高金額。 此值僅用於沒有子項產品群組的單位，並且將用來取代廣告群組層級值。

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

此範本會覆寫較高層級的範本，且僅用於沒有子產品群組的單位。

>[!MORELIKETHIS]
>
>* [實作 [!DNL Google Ads] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [實作 [!DNL Microsoft Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [該[!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
