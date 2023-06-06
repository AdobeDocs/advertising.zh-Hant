---
title: 從工具列套用資料篩選器
description: 瞭解如何從工具列篩選頁面資料。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 從工具列套用資料篩選器

您可以依需要套用多少篩選器至檢視。 所有篩選器皆使用AND運運算元連結。

1. 在工具列中，按一下 ![篩選](/help/search-social-commerce/assets/filter.png "篩選").

1. 在篩選設定中，執行下列任一項作業：

   * 若要新增篩選器，請按一下 ![新增篩選器](/help/search-social-commerce/assets/add.png "新增篩選器") **[!UICONTROL ADD FILTER]**，然後執行下列動作：

      1. （可選）若要依文字字串篩選欄名稱，請在 **[!UICONTROL ADD FILTER]** 輸入欄位。

      1. 從欄功能表中選取欄名稱。

      1. 在欄上定義篩選器：

         * （沒有輸入欄位的篩選器）按一下 ![向下鍵](/help/search-social-commerce/assets/arrow-down-expand.png "向下鍵") ，然後選取要包含的每個值旁的核取方塊。

         * （具有輸入欄位的篩選器）從第二個功能表選取運運算元，然後輸入適用的值。

            例如，如果您已選取&quot;[!UICONTROL Clicks]」欄，而只想傳回點按超過100次的列，然後選取 *[!UICONTROL greater than]*」並輸入 `100` 在輸入欄位中。

            根據資料型別，可用的運運算元可能包括 *[!UICONTROL greater than]*， *[!UICONTROL less than]*， *[!UICONTROL equals]*， *[!UICONTROL contains]*， *[!UICONTROL doesn't contain]*， *[!UICONTROL starts with]*， *[!UICONTROL ends with]*， *[!UICONTROL no value]*， *[!UICONTROL has value]*， *[!UICONTROL before]*， *[!UICONTROL after]*，或 *[!UICONTROL no date].*

            **注意：** 文字值不區分大小寫。 例如，如果您依名稱中包含「loan」的行銷活動進行篩選，則結果將包含「Consumer Loans」和「loan applications」。

         * ([!UICONTROL Ad Groups]， [!UICONTROL Keywords]， [!UICONTROL Product Groups]， [!UICONTROL Placements]、和 [!UICONTROL Auto Targets] 僅限檢視；選用)將設定變更為&quot;[!UICONTROL Include rows with performance data only].」

            **警告：** 如果您取消選取選項，且檢視包含許多沒有效能資料的實體，則顯示資料的時間會更長。
   * 若要編輯現有篩選器，請按一下該篩選器，變更篩選器定義，然後按一下 ![更新篩選器](/help/search-social-commerce/assets/select.png "更新篩選器").

   * 若要移除現有篩選器，請按一下 **[!UICONTROL X]** 位於篩選定義旁。


1. 按一下 **[!UICONTROL Apply]**.
