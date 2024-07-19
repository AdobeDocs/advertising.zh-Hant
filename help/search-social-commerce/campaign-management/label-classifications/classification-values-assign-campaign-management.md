---
title: 從行銷活動管理檢視將分類值指派給帳戶元件
description: 瞭解如何將分類值指派給帳戶元件。
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 從行銷活動管理檢視將分類值指派給帳戶元件

您可以從行銷活動管理檢視中指派及移除下列搜尋實體的分類值：行銷活動、廣告群組、關鍵字、廣告、位置、單位層級產品群組及動態搜尋目標。 如有需要，您可以在指派程式期間建立分類和分類值。 每個標籤分類最多可以有2000個值。

每個實體在每個分類中可以有一個標籤值。 例如，Shoes_Campaign的「顏色」值可以是「紅色」，而「地理」值可以是「洛杉磯」，但無法有多個「顏色」或「地理」值。

標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

>[!NOTE]
>
>您某些廣告網路和行銷活動型別的關鍵字和廣告復本是[不可變動](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，這表示編輯它們會刪除現有實體並建立新的實體。 以這種方式刪除現有實體時，不會將標籤分類指派給新實體。

1. 按一下「**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**」，然後選取帳戶元件檢視。

1. 執行下列任一項作業：

   * （若要指派值給單一實體）將游標停留在實體名稱上，按一下![功能表按鈕](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表按鈕")，然後選取&#x200B;**[!UICONTROL Classification]**。

   * （若要將值指定給一或多個實體），請執行下列動作：

      * 選取每個相關列旁的核取方塊。

        如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

      * 在資料表上方的工具列中，按一下![更多](/help/search-social-commerce/assets/more.png "更多")，然後按一下&#x200B;**[!UICONTROL Classification]**。

1. 在[!UICONTROL Assignment Details]中，執行下列任一項作業：

   * 若要將任何現有分類值變更為新值，請選取&#x200B;**[!UICONTROL Set To]**。

     每個值的長度上限為100個字元，可包含ASCII和非ASCII字元。

   * 若要指派指定的分類值而不移除現有值，請選取&#x200B;**[!UICONTROL Assign]**。

   * 若要移除目前指派的特定分類值，請選取&#x200B;**[!UICONTROL Remove]**。

     移除分類值時，指定帳戶元件將無法再使用該值的報表資料。

   * 若要刪除指定的分類值，請選取&#x200B;**[!UICONTROL Delete]**。

     刪除分類值會使該值日後無法使用，且報表資料不再可用於該值。 會移除值與特定帳戶元件之間的所有指定，但不會刪除帳戶元件。

1. 請針對每個適用的分類值，執行下列動作：

   1. 在&#x200B;**[!UICONTROL Classification]**&#x200B;欄中指定分類名稱：

      * 若要使用現有的分類，請按一下分類名稱將其展開。

      * 若要建立分類，請按一下[!UICONTROL +]。 在輸入欄位中輸入分類名稱，然後按一下[儲存] ![ ](/help/search-social-commerce/assets/select.png " [儲存] ")，立即儲存分類。

        名稱必須包含[ASCII字元32-126](https://www.asciitable.com/)，最大長度為27個單位元組字元。

   1. 在&#x200B;**[!UICONTROL Value Name]**&#x200B;欄中，指定值的名稱：

      * 若要使用現有值，請按一下值名稱以選取它。

      * 若要建立值，請按一下[!UICONTROL +]。 在輸入欄位中輸入值，然後按一下[儲存]。![](/help/search-social-commerce/assets/select.png "")，立即儲存值。

        長度上限為100個字元，可包含ASCII和非ASCII字元。

1. （選擇性）輸入其他詳細資料：

   1. 在&#x200B;**[!UICONTROL Additional Details]**&#x200B;旁邊，按一下![開啟](/help/search-social-commerce/assets/chevron-up.png "開啟")以展開詳細資料。

   1. 輸入選用的&#x200B;**[!UICONTROL Project Name]**&#x200B;和/或選用的&#x200B;**[!UICONTROL Description]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [關於標籤分類](classification-about.md)
>* [建立標籤分類](classification-create.md)
>* [使用大量表單指派分類值給帳戶元件](classification-values-assign-bulksheets.md)
>* [從帳戶元件移除標籤分類值](classification-values-remove.md)
>* [刪除標籤分類值](classification-values-delete.md)
>* [刪除標籤分類](classification-delete.md)
