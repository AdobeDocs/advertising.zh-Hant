---
title: 變更管理檢視和報告中可用的交易屬性
description: 瞭解如何在管理檢視和報告中使用交易屬性。
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
feature: Search Admin, Search Transaction Properties
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# 變更管理檢視和報告中可用的交易屬性

當Adobe Advertising追蹤 [交易屬性](/help/search-social-commerce/glossary.md#s-t) 對於廣告商而言，它最初會被排除在產品組合目標、報表和管理檢視之外。 若要讓屬性可見，您必須明確讓屬性可用，然後視需要變更預設顯示名稱（即顯示的名稱）。 唯一的例外是所追蹤的轉換 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] 通用事件追蹤標籤會自動開放使用並顯示。

同樣地，您可以在投資組合目標、報表和管理檢視中隱藏屬性。 當您隱藏先前可見的屬性時，該屬性會從包含該屬性的任何衍生量度中移除。

從可用的屬性清單中，有權存取廣告商資料的每位使用者都可以自訂管理檢視和報表中看到的屬性，包括或省略他們選擇的特定屬性。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   已針對廣告商收集的所有交易屬性，以及已指定用於顯示的任何不同名稱都會列在清單中。

1. （選用）篩選清單：

   * 若要搜尋特定的屬性名稱或顯示名稱，請按一下 ![搜尋](/help/search-social-commerce/assets/search.png "搜尋")，在輸入欄位中輸入單字或字串，然後按下 **[!DNL Enter]** 機碼。

     您可以搜尋出現在片語中任何位置的字串（例如第一個字母或最後三個字母），而搜尋詞則否 [區分大小寫](/help/search-social-commerce/glossary.md#c-d).

   * 若要依照屬性在管理檢視和報表中的可用性來搜尋屬性，請按一下 ![篩選](/help/search-social-commerce/assets/filter.png "篩選")，並選取篩選器 **[!UICONTROL Show in UI and Reports]**. 然後選取 **[!UICONTROL Show]** （以檢視可包含在報表和管理檢視中的屬性）或 **[!UICONTROL Hide]** （以檢視報表和管理檢視中無法使用的屬性）。

1. 變更管理檢視和報告可用的屬性：

   * 若要顯示或隱藏單一屬性，請按一下 **[!UICONTROL Show in UI and Reports]** 欄以變更設定。

   * 若要顯示或隱藏多個屬性，請執行下列動作：

      1. 選取每個屬性旁的核取方塊。

         如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

      1. 在資料表格上方的工具列中，按一下 ![顯示](/help/search-social-commerce/assets/show.png "顯示") 顯示屬性或 ![隱藏](/help/search-social-commerce/assets/hide.png "隱藏") 以隱藏屬性。

      1. （若要隱藏屬性）在確認訊息中，按一下 **[!UICONTROL Yes]** 以隱藏屬性，包括從任何包含屬性的衍生量度中移除屬性。

1. （可選） [變更顯示在欄標題中的名稱](transaction-property-edit-display-name.md) 屬性使用。

   每個可見屬性的預設顯示名稱是屬性名稱，如擷取資料中所拼寫。

>[!NOTE]
>
>如果Adobe Advertising收集新屬性的資料，則會收集新屬性 — 所追蹤的轉換除外 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] universal event tracking tags — 會自動從「管理檢視」和「報表」中排除，直到您將其納入為止。 由追蹤的新轉換 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] 通用事件追蹤標籤一律會自動提供。

>[!MORELIKETHIS]
>
* [關於管理廣告商的交易屬性](transaction-property-about.md)
* [檢視為廣告商追蹤的交易屬性](transaction-property-view-tracked.md)
* [變更交易屬性的顯示名稱](transaction-property-edit-display-name.md)
