---
title: 變更管理檢視和報告中的可用轉換量度
description: 瞭解如何在管理檢視和報告中使用轉換量度。
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# 變更管理檢視和報告中的可用轉換量度

當Adobe Advertising追蹤廣告商的[轉換](/help/search-social-commerce/glossary.md#c-d)量度時，它最初會從產品組合目標、報告和管理檢視中排除。 若要顯示轉換量度，您必須明確使其可用，然後選擇性變更預設顯示名稱（即顯示的名稱）。 唯一的例外是[!DNL Google Ads]、[!DNL Google Analytics]和[!DNL Microsoft Advertising]通用事件追蹤標籤所追蹤的轉換會自動提供並顯示。

同樣地，您可以在投資組合目標、報表和管理檢視中隱藏轉換量度。 當您隱藏先前可見的轉換量度時，它會從包含轉換量度的任何衍生量度中移除。

從可用的轉換量度清單中，可存取廣告商資料的每位使用者都可以自訂他們看到的管理檢視和報表量度，包括或省略他們選擇的特定量度。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**。

   已針對廣告商收集的所有轉換量度，以及已針對顯示指定的任何不同名稱都會列示。

1. （選用）篩選清單：

   * 若要搜尋特定的量度名稱或顯示名稱，請按一下![搜尋](/help/search-social-commerce/assets/search.png "搜尋")，在輸入欄位中輸入字詞或字串，然後按&#x200B;**[!DNL Enter]**&#x200B;鍵。

     您可以搜尋出現在片語中任何位置的字串（例如第一個字母或最後三個字母），而且搜尋字詞不會區分大小寫[&#128279;](/help/search-social-commerce/glossary.md#c-d)。

   * 若要依據轉換量度在管理檢視和報告中的可用性來搜尋轉換量度，請按一下![篩選器](/help/search-social-commerce/assets/filter.png "篩選器")，然後選取篩選器&#x200B;**[!UICONTROL Show in UI and Reports]**。 然後選取&#x200B;**[!UICONTROL Show]** （以檢視可包含在報告和管理檢視中的轉換量度）或&#x200B;**[!UICONTROL Hide]** （以檢視報告和管理檢視中不可用的轉換量度）。

1. 變更管理檢視和報告可用的轉換量度：

   * 若要顯示或隱藏單一量度，請按一下&#x200B;**[!UICONTROL Show in UI and Reports]**&#x200B;欄中的切換以變更設定。

   * 若要顯示或隱藏多個量度，請執行下列動作：

      1. 選取每個轉換量度旁的核取方塊。

         如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

      1. 在資料表上方的工具列中，按一下![顯示](/help/search-social-commerce/assets/show.png "顯示")以顯示度量，或按一下![隱藏](/help/search-social-commerce/assets/hide.png "隱藏")隱藏度量。

      1. （若要隱藏量度）在確認訊息中，按一下&#x200B;**[!UICONTROL Yes]**&#x200B;以隱藏量度，包括從包含量度的任何衍生量度中移除量度。

1. （選擇性） [針對任何轉換量度，變更顯示在欄標題](conversion-metric-edit-display-name.md)中的名稱。

   每個可見轉換量度的預設顯示名稱是擷取資料中拼寫的量度名稱。

>[!NOTE]
>
>如果Adobe Advertising收集新轉換量度的資料，則新量度（除了[!DNL Google Ads]、[!DNL Google Analytics]和[!DNL Microsoft Advertising]通用事件追蹤標籤所追蹤的轉換）會自動從管理檢視和報表中排除，直到您將其納入為止。 由[!DNL Google Ads]、[!DNL Google Analytics]和[!DNL Microsoft Advertising]通用事件追蹤標籤追蹤的新轉換一律會自動提供。

>[!MORELIKETHIS]
>
>* [關於管理廣告商的轉換量度](conversion-metric-about.md)
>* [檢視為廣告商追蹤的轉換量度](conversion-metric-view-tracked.md)
>* [變更轉換量度的顯示名稱](conversion-metric-edit-display-name.md)
