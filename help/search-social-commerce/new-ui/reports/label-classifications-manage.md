---
title: 管理標籤分類
description: 瞭解如何使用標籤分類將您的帳戶元件分組。
feature: Search Label Classifications
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 0%

---

# 管理標籤分類

標籤分類可協助您將帳戶元件分組為有意義的集合。 例如，您可以建立名為「地理」的父標籤分類，並為分類內的每個地理區域（例如「英國」和「日本」）建立不同的標籤值，然後將標籤值指派給您的[競標單位](/help/search-social-commerce/glossary.md#a-b)或父促銷活動。 然後，您就可以在檢視和報表中加入任何標籤值，做為個別的欄，並按照不同的分類群組和值對報表進行子樞紐分析。

## 標籤分類的元件

### 標籤分類

每個廣告商最多可以有30個標籤分類，這是最上層的類別。 建立標籤分類後，您就可以為分類建立特定的標籤值。

### 標籤值

每個標籤分類最多可以有2000個值。 一旦您為分類建立特定標籤值，您就可以從行銷活動管理檢視](#classification-values-assign-campaign-management)或[使用大量表單](#classification-values-assign-bulksheets)，將其指派給行銷活動、廣告群組、關鍵字、廣告、位置及產品群組[。

每個符合資格的實體都可以有多個分類的標籤值，但每個分類只有一個標籤值。 標籤值由子實體繼承，但可以覆寫。 在最低層次指定的值一律會覆寫在父層次指定的值。

## 標籤分類檢視

[!UICONTROL Reports] > [!UICONTROL Labels Classifications]檢視包含[!UICONTROL Classifications]和[!UICONTROL Label Values]個子檢視。 預設會顯示關鍵字層級標籤分類和值的資料，但您可以選擇檢視廣告層級分類和值的資料。

## 可用動作

* 檢視標籤分類的資料。

* 檢視標籤分類值的資料。

* [建立標籤分類](#classification-create)。

* 從行銷活動管理檢視](#classification-values-assign-campaign-management)或使用Bulksheets](#classification-values-assign-bulksheets)將分類值指派給帳戶元件[。[

* [從帳戶元件](#classification-values-remove)移除標籤分類值。

* [刪除標籤分類值](#classification-values-delete)。

* [刪除標籤分類](#classification-delete)。

## 建立標籤分類 {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. 按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Label Classifications]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Create Classification]**。

1. 輸入唯一的標籤分類名稱，然後按一下&#x200B;**[!UICONTROL Create]**。

   廣告商帳戶的名稱必須是唯一的，且包含[ASCII字元32-126](https://www.asciitable.com/)，最大長度為27個單位元組字元。 名稱不能與現有報表欄或現有Bulksheet欄的名稱相同。 檢視[百度](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)、[Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)、[LY Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)、[Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)、[Yahoo！的大量表單欄名稱 顯示網路](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)和[Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)。

## 從行銷活動管理檢視將分類值指派給帳戶元件 {#classification-values-assign-campaign-management}

您可以從行銷活動管理檢視中指派及移除下列搜尋實體的分類值：行銷活動、廣告群組、關鍵字、廣告、位置、單位層級產品群組及動態搜尋目標。 如有需要，您可以在指派程式期間建立分類和分類值。 每個標籤分類最多可以有2000個值。

每個實體在每個分類中可以有一個標籤值。 例如，Shoes_Campaign的「顏色」值可以是「紅色」，而「地理」值可以是「洛杉磯」，但無法有多個「顏色」或「地理」值。

標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

>[!NOTE]
>
>您某些廣告網路和行銷活動型別的關鍵字和廣告復本是[不可變動](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，這表示編輯它們會刪除現有實體並建立新的實體。 以這種方式刪除現有實體時，不會將標籤分類指派給新實體。

1. 從&#x200B;**[!UICONTROL Manage]**&#x200B;或&#x200B;**[!UICONTROL Target]**&#x200B;功能表開啟實體檢視。

1. 選取每個相關列旁的核取方塊。

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

## 使用大量表單指派分類值給帳戶元件 {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

您可以使用大量表單來將標籤分類與下列搜尋實體的值相關聯：行銷活動、廣告群組、關鍵字、廣告、位置、單位層級產品群組及動態搜尋目標。 每個標籤分類最多可以有2000個值。

每個實體在每個分類中可以有一個標籤值。 例如，Shoes_Campaign的「顏色」值可以是「紅色」，而「地理」值可以是「洛杉磯」，但無法有多個「顏色」或「地理」值。

標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

>[!NOTE]
>
>您某些廣告網路和行銷活動型別的關鍵字和廣告復本是[不可變動](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，這表示編輯它們會刪除現有實體並建立新的實體。 以這種方式刪除現有實體時，不會將標籤分類指派給新實體。

1. [下載大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)，其中包含您要指派標籤分類值的實體：

   * 在[!UICONTROL Rows and Columns]標籤上，展開[!UICONTROL Bulksheet Columns]窗格中的[!UICONTROL Campaign]清單。

   * 展開[!UICONTROL Label Classification]清單。

   * 選取每一個要在其大量表單檔案中包含欄的分類。

     例如，如果您包含標籤分類「顏色」和「地理」，則大量表單會包含「顏色」和「地理」欄。

1. 在編輯器中開啟檔案，並將標籤值新增至要與其產生關聯的實體的標籤分類欄。 每個值的長度上限為100個字元，可包含ASCII和非ASCII字元。

   請參閱下一節中的範例值。

   除了新增值之外，您也可以從相關列移除現有值以將其刪除。 若要從父項實體及其子項實體中移除值，請a)僅包含父項實體列，並移除現有的分類值，或b)同時包含父項實體及其子項實體，並從所有父項列與子項列移除現有的分類值。

1. [上傳檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)以建立關聯。<!-- Update once the new bulksheet UI is GA -->

上傳的標籤值會顯示在相關實體檢視中。

### 要在大量表單中上傳的標籤分類值範例

此範例包含標籤分類「顏色」和「地理」的欄。 針對您自己的大量表單，將欄取代您自己的標籤分類名稱。

| 帳戶 | Campaign | 廣告群組 | 關鍵字 | 廣告 | 產品建議放置環境 | 標籤 | 顏色 | 地理 |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | 綠色 | |
| Acct1 | C1 | AG1 | | | | | | |
| Acct1 | C1 | AG1 | K1 | | | | | UK |
| Acct1 | C1 | AG1 | K2 | | | | 紅色 | AU |
| Acct1 | C1 | AG1 | K3 | | | | 藍色 | DE |
| Acct1 | C1 | AG1 | | A1 | | | | |
| Acct1 | C1 | AG1 | | A1 | | | 紅色 | |
| Acct1 | C1 | AG1 | | | P1 | | 紅色 | AU |
| Acct1 | C1 | AG1 | | | P2 | | 藍色 | DE |

## 從帳戶元件中移除標籤分類值 {#classification-values-remove}

移除分類值會移除與帳戶元件及其所有子元件的關聯。 這些元件不再提供分類值的報表資料。 移除分類值不會刪除值或帳戶元件。

>[!NOTE]
>
>若要從標籤分類刪除值，請參閱&quot;[刪除標籤分類值](#classification-values-delete)&quot;。

1. 從&#x200B;**[!UICONTROL Manage]**&#x200B;或&#x200B;**[!UICONTROL Target]**&#x200B;功能表開啟實體檢視。

1. 選取每個相關列旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 選取每個分類值旁的核取方塊，以從選取的實體中移除。<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   若要選取所有指派的值，請按一下&#x200B;**[!UICONTROL Select All]**。 若要取消選取所有指派的值，請按一下&#x200B;**[!UICONTROL Deselect All]**。

1. 按一下&#x200B;**[!UICONTROL Unassign Selected]**。

## 刪除標籤分類值 {#classification-values-delete}

刪除標籤分類值會使這些值在日後無法使用，且報表資料不再適用於這些值。 會移除值及其上層標籤分類和特定帳戶元件之間的所有指派，但不會刪除上層標籤分類和促銷活動元件。

>[!NOTE]
>
>若要解除分類值與帳戶元件的關聯，請參閱&quot;[從帳戶元件移除標籤分類值](#classification-values-remove)&quot;。

1. 按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Label Classifications]**。

1. 按一下「**[!UICONTROL Label Values]**」標籤。

1. （選用）篩選清單以包含特定標籤值。

1. 選取要刪除的每個標籤值旁的核取方塊。

   您一次最多可以刪除200列。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 刪除標籤分類

刪除分類會移除其子值與帳戶元件之間的所有關聯。 已刪除的分類及其值無法供日後使用。 分類值的報表資料已無法使用。

>[!NOTE]
>
>若要解除分類值與帳戶元件的關聯，請參閱&quot;[從帳戶元件移除標籤分類值](#classification-values-remove)&quot;。

1. 按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Label Classifications]**。

1. （選用）篩選清單以包含特定標籤分類。

1. 選取要刪除的每個標籤分類旁的核取方塊。

   您一次最多可以刪除200列。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。
