---
title: 從工具列套用資料篩選
description: 瞭解如何從工具列篩選頁面資料。
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# 從工具列套用資料篩選

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

您可以套用任意數目的篩選器來檢視。<!-- True only for entity names, I think: All filters are joined using the AND operator. -->

## （新UI）從管理檢視的工具列套用資料篩選器

1. 在工具列中按一下![篩選器](/help/search-social-commerce/assets/filter-new.png "篩選器")。

1. 在篩選設定中，執行下列任一項作業：

   * 若要新增篩選器，請按一下&#x200B;**[!UICONTROL ADD FILTER]**，然後執行下列動作：

      1. （選擇性）若要依文字字串篩選欄名稱，請在&#x200B;**[!UICONTROL ADD FILTER]**&#x200B;輸入欄位中輸入搜尋字串。

      1. 從欄功能表中選取欄名稱。

      1. 在欄上定義篩選器：

         * （沒有輸入欄位的篩選器）按一下第二個功能表旁的![向下箭頭](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭頭")，然後選取要包含的每個值旁的核取方塊。

         * （具有輸入欄位的篩選器）從第二個功能表選取運運算元，然後輸入適用的值。

           例如，如果您已選取&quot;[!UICONTROL Clicks]&quot;欄，且只想傳回點按超過100次的列，則選取「*[!UICONTROL greater than]*」並在輸入欄位中輸入`100`。

           根據資料型別，可用的運運算元可能包括&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;或&#x200B;*[!UICONTROL no date]。*

           **注意：**&#x200B;文字值不區分大小寫。 例如，如果您依名稱含有「貸款」的行銷活動進行篩選，結果會包含「消費者貸款」和「貸款申請」。

   * 若要編輯現有篩選器，請按一下該篩選器，然後變更篩選器定義。

   * 若要移除現有的篩選器，請按一下篩選器定義旁的&#x200B;**[!UICONTROL -]**。

## （舊版UI）從行銷活動管理檢視的工具列套用資料篩選器

1. 在工具列中按一下![篩選器](/help/search-social-commerce/assets/filter.png "篩選器")。

1. 在篩選設定中，執行下列任一項作業：

   * 若要新增篩選器，請按一下![新增篩選器](/help/search-social-commerce/assets/add.png "新增篩選器") **[!UICONTROL ADD FILTER]**，然後執行下列動作：

      1. （選擇性）若要依文字字串篩選欄名稱，請在&#x200B;**[!UICONTROL ADD FILTER]**&#x200B;輸入欄位中輸入搜尋字串。

      1. 從欄功能表中選取欄名稱。

      1. 在欄上定義篩選器：

         * （沒有輸入欄位的篩選器）按一下第二個功能表旁的![向下箭頭](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭頭")，然後選取要包含的每個值旁的核取方塊。

         * （具有輸入欄位的篩選器）從第二個功能表選取運運算元，然後輸入適用的值。

           例如，如果您已選取&quot;[!UICONTROL Clicks]&quot;欄，且只想傳回點按超過100次的列，則選取「*[!UICONTROL greater than]*」並在輸入欄位中輸入`100`。

           根據資料型別，可用的運運算元可能包括&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;或&#x200B;*[!UICONTROL no date]。*

           **注意：**&#x200B;文字值不區分大小寫。 例如，如果您依名稱含有「貸款」的行銷活動進行篩選，結果會包含「消費者貸款」和「貸款申請」。

         * （[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Product Groups]、[!UICONTROL Placements]和[!UICONTROL Auto Targets]檢視；選擇性）將設定變更為&quot;[!UICONTROL Include rows with performance data only]&quot;。

           **警告：**&#x200B;如果您取消選取選項，而檢視包含許多沒有效能資料的實體，則需要較長時間才能顯示資料。

   * 若要編輯現有篩選器，請按一下該篩選器，然後變更篩選器定義。

   * 若要移除現有的篩選器，請按一下篩選器定義旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

1. 按一下&#x200B;**[!UICONTROL Apply]**。

>[!MORELIKETHIS]
>
>* [從欄標題功能表套用資料篩選](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [編輯欄篩選器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [移除欄篩選器]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
