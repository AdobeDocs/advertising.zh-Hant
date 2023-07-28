---
title: 透過範本傳播詳細目錄摘要資料
description: 瞭解如何透過廣告範本從您的詳細目錄摘要傳播資料，以管理帳戶結構並傳遞動態廣告。
exl-id: 40de75e8-8440-48f4-9fa7-1aeb2ae392c5
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# 透過範本傳播詳細目錄摘要資料

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

在您建立廣告網路專屬摘要範本，並關聯摘要檔案或 [!DNL Google] 或 [!DNL Microsoft®] 商家中心帳戶可透過根據以下範本傳播摘要資料，動態建立廣告： [摘要資料設定](feed-settings-manage.md). 在傳播期間，範本中的欄名稱會由摘要中的資料值取代，而除非範本另有指定，否則產生的行銷活動及其元件會具有預設設定。 根據範本選項， Search、Social和Commerce會為廣告建立新的帳戶結構（促銷活動、廣告群組、關鍵字），或將廣告對應至現有的帳戶結構。

當新的摘要資料包含專案的新資料值，或範本已變更時，現有廣告將被刪除並建立新的廣告。 如果唯一變更是指定了 [!DNL Google Ads] Param 1和Param 2，則只會更新這些值。 絕對不會建立重複的廣告（相同的廣告文案和登陸頁面）。

當您傳播資料時，您可以選擇在行銷活動階層檢視中預覽產生的資料、產生大量表單檔案以供檢閱，或產生大量表單檔案以供立即張貼至廣告網路。 每個傳輸動作完成時，傳輸摘要會新增至「傳輸」頁簽，指出根據傳輸建立、暫停或刪除的每個實體型別數目。 如果您未立即張貼資料，則可預覽資料並於稍後張貼。

## 從傳播摘要檔案 [!UICONTROL Templates] 標籤

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 選取要傳播的範本旁的核取方塊。

1. 在工具列中，按一下 **[!UICONTROL Propagate]**，然後選取下列其中一個選項：

   * **[!UICONTROL Propagate Only]：** 若要顯示傳播資料於 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。 您稍後仍可從發佈任何元件及其子元件的資料。 [!UICONTROL Templates] 標籤。

   * **[!UICONTROL Propagate and Preview]：** 建立大量表單檔案(名為&quot;`<feed file name>_<template name>`&quot;)，此頁面位於 [!UICONTROL Bulksheets] 檢視以供檢閱(但不會在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 標籤)。 您稍後可以從以下位置張貼大量表單檔案： [!UICONTROL Bulksheets] 檢視。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。 您不需要解壓縮檔案即可發佈。

   * **[!UICONTROL Propagate and Post to SE]：** 建立大量表單檔案(名為&quot;`<feed file name>_<template name>`&quot;)已排入佇列，等候張貼至廣告網路。 Bulksheet檔案可在 [!UICONTROL Bulksheets] 檢視，但無法在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。

   「最後一個Prop」。 「狀態」欄會顯示適用範本的工作狀態。

   完成每個傳輸動作後，傳輸摘要會新增至 [!UICONTROL Propagations] 索引標籤，表示根據傳輸建立、暫停或刪除的每個實體型別數目。 預估費用不包括從廣告網路本身的廣告編輯器中進行的變更。

## 從傳播摘要檔案 [!UICONTROL Feeds] 清單

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Feeds]**.

1. 選取摘要檔案旁的核取方塊。

1. 在資料表格上方，按一下 **[!UICONTROL Propagate/Post Feed Data]**，然後選取下列其中一個選項：

   * **[!UICONTROL Propagate Only]：** 若要顯示傳播資料於 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。 您稍後仍可從發佈任何元件及其子元件的資料。 [!UICONTROL Templates] 標籤。

   * **[!UICONTROL Propagate and Preview]：** 建立大量表單檔案(名為&quot;`<feed file name>_<template name>`&quot;)，此頁面位於 [!UICONTROL Bulksheets] 檢視以供檢閱(但不會在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 標籤)。 您稍後可以從以下位置張貼大量表單檔案： [!UICONTROL Bulksheets] 檢視。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。 您不需要解壓縮檔案即可發佈。

   * **[!UICONTROL Propagate and Post to SE]：** 建立大量表單檔案(名為&quot;`<feed file name>_<template name>`&quot;)已排入佇列，等候張貼至廣告網路。 Bulksheet檔案可在 [!UICONTROL Bulksheets] 檢視，但無法在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。

1. 在快顯視窗中，選取每個範本旁的核取方塊，以便從摘要檔案傳輸資料，然後按一下 **[!UICONTROL Propagate Feed]**.

   會列出與檔案相關的所有範本。

此 [!UICONTROL Templates] 標籤隨即開啟，且「[!UICONTROL Last Prop. Status]「欄」會顯示適用範本的工作狀態。

完成每個傳輸動作後，傳輸摘要會新增至 [!UICONTROL Propagations] 索引標籤，表示根據傳輸建立、暫停或刪除的每個實體型別數目。 預估費用不包括從廣告網路本身的廣告編輯器中進行的變更。

## 檢視傳輸摘要

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 按一下 **[!UICONTROL Propagations]** 標籤。

1. 在範本名稱旁，按一下 ![檢視/編輯設定圖示](/help/search-social-commerce/assets/settings.png "檢視/編輯設定圖示") .

## 停止傳播工作

您可以在工作仍在佇列時，停止清查摘要資料的傳播工作。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 在&quot;[!UICONTROL Last Prop. Status]」欄，按一下 **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [管理詳細目錄摘要的廣告範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [從摘要產生的行銷活動資料張貼至廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
