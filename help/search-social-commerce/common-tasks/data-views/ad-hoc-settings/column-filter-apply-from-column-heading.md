---
title: 從欄標題功能表套用資料篩選器
description: 瞭解如何從欄標題選單篩選頁面資料。
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# 從欄標題功能表套用資料篩選

<!-- The same in new UI and legacy CM views -->

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

您可以對欄套用任意數量的篩選器，一次一個。<!-- True only for entity names, I think: All filters are joined using the AND operator. -->若要使用所有可用的量度一次新增多個篩選器，請參閱[從工具列套用資料篩選器](column-filter-apply-from-toolbar.md)。

1. 在欄標題的右側，按一下![向下箭頭](/help/search-social-commerce/assets/arrow-down-dropdown.png "向下箭頭")，然後按一下&#x200B;**[!UICONTROL Add Filter]**。

1. 在欄上定義篩選器：

   * （沒有輸入欄位的篩選器）選取每個要包含的值旁的核取方塊，然後按一下![更新篩選器](/help/search-social-commerce/assets/select.png "新增")。

   * （具有輸入欄位的篩選器）從第二個功能表選取運運算元，輸入適用的值，然後按一下![更新篩選器](/help/search-social-commerce/assets/select.png "新增")。

     例如，如果您已選取&#39;&#39;[!UICONTROL Clicks]&#39;&#39;資料行且只想傳回超過100次點按的資料列，則選取&#x200B;*[!UICONTROL greater than]*&#39;並在輸入欄位中輸入`100`根據資料型別，可用的運運算元可能包括&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;或&#x200B;*[!UICONTROL no date]。*

     >[!NOTE]
     >
     >* 文字值不區分大小寫。 例如，如果您依名稱含有「貸款」的行銷活動進行篩選，結果會包含「消費者貸款」和「貸款申請」。
     >* 每個欄只能套用一個簡單數值篩選（例如[!UICONTROL Impressions] \> 100）。

>[!MORELIKETHIS]
>
>* [從工具列套用資料篩選](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [編輯欄篩選器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [移除欄篩選器]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
