---
title: 變更管理檢視和報告中的可用轉換量度
description: 瞭解如何在管理檢視和報告中使用轉換量度。
feature: Conversions
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# 變更管理檢視和報告中的可用轉換量度

當Adobe Advertising追蹤 [轉換](/help/search-social-commerce/glossary.md#c-d) 廣告商的量度最初會排除在產品組合目標、報表和管理檢視之外。 若要顯示轉換量度，您必須明確使其可用，然後選擇性變更預設顯示名稱（即顯示的名稱）。 唯一的例外是所追蹤的轉換 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] 通用事件追蹤標籤會自動開放使用並顯示。

同樣地，您可以在投資組合目標、報表和管理檢視中隱藏轉換量度。 當您隱藏先前可見的轉換量度時，它會從包含轉換量度的任何衍生量度中移除。

從可用的轉換量度清單中，可存取廣告商資料的每位使用者都可以自訂他們看到的管理檢視和報表量度，包括或省略他們選擇的特定量度。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   已針對廣告商收集的所有轉換量度，以及已針對顯示指定的任何不同名稱都會列示。

1. （選用）篩選清單：

   * 若要搜尋特定的量度名稱或顯示名稱，請按一下 ![搜尋](/help/search-social-commerce/assets/search.png "搜尋")，在輸入欄位中輸入單字或字串，然後按下 **[!DNL Enter]** 機碼。

     您可以搜尋出現在片語中任何位置的字串（例如第一個字母或最後三個字母），而搜尋詞則否 [區分大小寫](/help/search-social-commerce/glossary.md#c-d).

   * 若要依管理檢視和報告中的使用狀態來搜尋轉換量度，請按一下 ![篩選](/help/search-social-commerce/assets/filter.png "篩選")，並選取篩選器 **[!UICONTROL Show in UI and Reports]**. 然後選取 **[!UICONTROL Show]** （檢視可納入報表和管理檢視中的轉換量度）或 **[!UICONTROL Hide]** （以檢視在報表和管理檢視中無法使用的轉換量度）。

1. 變更管理檢視和報告可用的轉換量度：

   * 若要顯示或隱藏單一量度，請按一下 **[!UICONTROL Show in UI and Reports]** 欄以變更設定。

   * 若要顯示或隱藏多個量度，請執行下列動作：

      1. 選取每個轉換量度旁的核取方塊。

         如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

      1. 在資料表格上方的工具列中，按一下 ![顯示](/help/search-social-commerce/assets/show.png "顯示") 顯示量度或 ![隱藏](/help/search-social-commerce/assets/hide.png "隱藏") 以隱藏量度。

      1. （若要隱藏量度）在確認訊息中，按一下 **[!UICONTROL Yes]** 以隱藏量度，包括從任何包含量度的衍生量度中移除量度。

1. （可選） [變更顯示在欄標題中的名稱](conversion-metric-edit-display-name.md) 用於任何轉換量度。

   每個可見轉換量度的預設顯示名稱是擷取資料中拼寫的量度名稱。

>[!NOTE]
>
>如果Adobe Advertising收集新轉換量度的資料，則新量度 — 由追蹤的轉換除外 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] universal event tracking tags — 會自動從「管理檢視」和「報表」中排除，直到您將其納入為止。 由追蹤的新轉換 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] 通用事件追蹤標籤一律會自動提供。

>[!MORELIKETHIS]
>
* [關於管理廣告商的轉換量度](conversion-metric-about.md)
* [檢視為廣告商追蹤的轉換量度](conversion-metric-view-tracked.md)
* [變更轉換量度的顯示名稱](conversion-metric-edit-display-name.md)
