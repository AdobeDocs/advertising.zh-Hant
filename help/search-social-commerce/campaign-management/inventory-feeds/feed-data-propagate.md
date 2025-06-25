---
title: 透過範本傳播詳細目錄摘要資料
description: 瞭解如何透過廣告範本從您的詳細目錄摘要傳播資料，以管理帳戶結構並傳遞動態廣告。
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# 透過範本傳播詳細目錄摘要資料

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

在您建立廣告網路專屬摘要範本，並將摘要檔案或[!DNL Google]或[!DNL Microsoft]商家中心帳戶與其建立關聯後，您可以根據[摘要資料設定](feed-settings-manage.md)，透過範本傳播摘要資料，以動態建立廣告。 在傳播期間，範本中的欄名稱會由摘要中的資料值取代，而除非範本另有指定，否則產生的行銷活動及其元件會具有預設設定。 根據範本選項，搜尋、Social和Commerce會為廣告建立新的帳戶結構（促銷活動、廣告群組、關鍵字），或將廣告對應至現有的帳戶結構。

當新的摘要資料包含專案的新資料值，或範本已變更時，現有廣告將被刪除並建立新的廣告。 如果唯一變更是[!DNL Google Ads] Param 1和Param 2的指定，則只會更新這些值。 絕對不會建立重複的廣告（相同的廣告文案和登陸頁面）。

當您傳播資料時，您可以選擇在行銷活動階層檢視中預覽產生的資料、產生大量表單檔案以供檢閱，或產生大量表單檔案以供立即張貼至廣告網路。 每個傳輸動作完成時，傳輸摘要會新增至「傳輸」頁簽，指出根據傳輸建立、暫停或刪除的每個實體型別數目。 如果您未立即張貼資料，則可預覽資料並於稍後張貼。

## 從[!UICONTROL Templates]索引標籤傳播摘要檔案

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

1. 選取要傳播的範本旁的核取方塊。

1. 在工具列中按一下&#x200B;**[!UICONTROL Propagate]**，然後選取下列其中一個選項：

   * **[!UICONTROL Propagate Only]：**&#x200B;在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤上顯示傳播的資料。 您稍後仍可從[!UICONTROL Templates]標籤張貼任何元件及其子元件的資料。

   * **[!UICONTROL Propagate and Preview]：**&#x200B;若要建立Bulksheet檔案（名為&quot;`<feed file name>_<template name>`&quot;），可在[!UICONTROL Bulksheets]檢視中檢視（但不適用於[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤）。 您稍後可以從[!UICONTROL Bulksheets]檢視張貼Bulksheet檔案。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。 您不需要解壓縮檔案即可發佈。

   * **[!UICONTROL Propagate and Post to SE]：**&#x200B;若要建立立即排入佇列以張貼至廣告網路的Bulksheet檔案（名為&quot;`<feed file name>_<template name>`&quot;），請執行下列步驟： Bulksheet檔案可在[!UICONTROL Bulksheets]檢視中使用，但無法在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤中使用。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。

   「最後一個Prop」。 「狀態」欄會顯示適用範本的工作狀態。

   每個傳輸動作完成時，傳輸摘要會新增至[!UICONTROL Propagations]索引標籤，指出根據傳輸已經或將會建立、暫停或刪除的每個實體型別數目。 預估費用不包括從廣告網路本身的廣告編輯器中進行的變更。

## 從[!UICONTROL Feeds]清單傳播摘要檔案

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Feeds]**。

1. 選取摘要檔案旁的核取方塊。

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Propagate/Post Feed Data]**，然後選取下列其中一個選項：

   * **[!UICONTROL Propagate Only]：**&#x200B;在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤上顯示傳播的資料。 您稍後仍可從[!UICONTROL Templates]標籤張貼任何元件及其子元件的資料。

   * **[!UICONTROL Propagate and Preview]：**&#x200B;若要建立Bulksheet檔案（名為&quot;`<feed file name>_<template name>`&quot;），可在[!UICONTROL Bulksheets]檢視中檢視（但不適用於[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤）。 您稍後可以從[!UICONTROL Bulksheets]檢視張貼Bulksheet檔案。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。 您不需要解壓縮檔案即可發佈。

   * **[!UICONTROL Propagate and Post to SE]：**&#x200B;若要建立立即排入佇列以張貼至廣告網路的Bulksheet檔案（名為&quot;`<feed file name>_<template name>`&quot;），請執行下列步驟： Bulksheet檔案可在[!UICONTROL Bulksheets]檢視中使用，但無法在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤中使用。

     當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。

1. 在快顯視窗中，選取每個範本旁的核取方塊，以便從摘要檔案傳輸資料，然後按一下&#x200B;**[!UICONTROL Propagate Feed]**。

   會列出與檔案相關的所有範本。

「[!UICONTROL Templates]」索引標籤隨即開啟，「[!UICONTROL Last Prop. Status]」欄會顯示適用範本的工作狀態。

每個傳輸動作完成時，傳輸摘要會新增至[!UICONTROL Propagations]索引標籤，指出根據傳輸已經或將會建立、暫停或刪除的每個實體型別數目。 預估費用不包括從廣告網路本身的廣告編輯器中進行的變更。

## 檢視傳輸摘要

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 按一下「**[!UICONTROL Propagations]**」標籤。

1. 在範本名稱旁邊，按一下![檢視/編輯設定圖示](/help/search-social-commerce/assets/settings.png "檢視/編輯設定圖示") 。

## 停止傳播工作

您可以在工作仍在佇列時，停止清查摘要資料的傳播工作。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

1. 在範本名稱旁邊的&quot;[!UICONTROL Last Prop. Status]&quot;欄中，按一下&#x200B;**[!UICONTROL Cancel]**。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [管理詳細目錄摘要的廣告範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [從摘要產生的貼文行銷活動資料到廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
