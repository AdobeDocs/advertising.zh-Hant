---
title: 從欄標題功能表套用資料篩選器
description: 瞭解如何從欄標題選單篩選頁面資料。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 從欄標題功能表套用資料篩選

您可以對欄套用任意數目的篩選器，一次一個篩選器。 所有篩選器皆使用AND運運算元連結。 若要使用所有可用量度一次新增多個篩選器，請參閱&quot;[從工具列套用資料篩選器](column-filter-apply-from-toolbar.md).」

1. 在欄標題的右側，按一下 ![向下鍵](/help/search-social-commerce/assets/arrow-down-dropdown.png "向下鍵")，然後按一下 **[!UICONTROL Add Filter]**.

1. 在欄上定義篩選器：

   * （沒有輸入欄位的篩選器）選取要包含的每個值旁的核取方塊，然後按一下 ![更新篩選器](/help/search-social-commerce/assets/select.png "更新篩選器").

   * （具有輸入欄位的篩選器）從第二個選單中選取運運算元，輸入適用的值，然後按一下 ![更新篩選器](/help/search-social-commerce/assets/select.png "更新篩選器").

      例如，如果您已選取&quot;[!UICONTROL Clicks]」欄，而只想傳回點按超過100次的列，然後選取 *[!UICONTROL greater than]*」並輸入 `100` 在輸入欄位中，根據資料型別，可用的運運算元可能包括 *[!UICONTROL greater than]*， *[!UICONTROL less than]*， *[!UICONTROL equals]*， *[!UICONTROL contains]*， *[!UICONTROL doesn't contain]*， *[!UICONTROL starts with]*， *[!UICONTROL ends with]*， *[!UICONTROL no value]*， *[!UICONTROL has value]*， *[!UICONTROL before]*， *[!UICONTROL after]*，或 *[!UICONTROL no date].*

      >[!NOTE]
      >
      >* 文字值不區分大小寫。 例如，如果您依名稱中包含「loan」的行銷活動進行篩選，結果會包含「Consumer Loans」和「loan applications」。
      >* 您只能套用一個簡單數值篩選器(例如 [!UICONTROL Impressions] \> 100)。

