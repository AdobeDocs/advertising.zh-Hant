---
title: 管理行銷活動的限制指派
description: 瞭解如何將限制指派給行銷活動。
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: d886a228-24d7-4d8e-b68a-76e56b4304ed
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# （新UI）管理行銷活動的限制指派

*Beta功能*

您可以為下列搜尋實體指派及移除競標限制：行銷活動、廣告群組、關鍵字、位置、單位層級產品群組，以及動態搜尋目標。 每個圖元只能有一個限制。

限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體指派限制。

取消指定限制會移除與帳號元件及其所有子元件的關聯，且這些元件無法再使用該限制的報表資料。 取消指定限制並不會刪除限制或帳戶元件本身。

>[!NOTE]
>
>* 如果您稍後編輯廣告的關鍵字或廣告復本（因而建立新的關鍵字或廣告），則限制不會指派給新實體。
>* 作用中限制僅限制最佳化舊關鍵字層級產品組合中已指派競標單位的競標。 若競標單位位於作用中產品組合、混合產品組合或不在產品組合中，則會忽略這些專案。

## 從新[!UICONTROL Campaigns]檢視指派限制給選取的行銷活動

您可以將單一限制指派給一或多個行銷活動。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取您要指派單一限制之每個行銷活動旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

## 從舊版[!UICONTROL Campaigns]檢視指派限制給選取的搜尋競標單位

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，選取帳戶元件檢視。

1. 選取每個相關列旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取適用的限制。

1. （選擇性）輸入其他詳細資料：

   1. 在[!UICONTROL Additional Details]旁邊，按一下&#x200B;**[!UICONTROL Open]**&#x200B;以展開詳細資料。

   1. 輸入選用的&#x200B;**[!UICONTROL Project Name]**&#x200B;和/或選用的&#x200B;**[!UICONTROL Description]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 從新[!UICONTROL Campaigns]檢視取消指派所選行銷活動的限制

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 選取每個行銷活動旁的核取方塊，您會從中取消指派限制。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

## 從舊版[!UICONTROL Campaigns]檢視取消指派搜尋競標單位的限制

>[!NOTE]
>
>若要刪除限制，使其無法用於未來用途，請參閱「競標限制」上「最佳化指南」一章中的「刪除搜尋競標單位的限制」，可於搜尋、社交和Commerce中使用。<!-- verify convention for referencing Optimization Guide here -->

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，選取帳戶元件檢視。

1. 選取要從中移除限制之每個元件旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 在確認對話方塊中，選取&#x200B;**[!UICONTROL Yes, Unassign]**。

>[!MORELIKETHIS]
>
>* [管理廣告群組的限制指派](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
