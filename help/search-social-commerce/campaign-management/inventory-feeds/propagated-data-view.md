---
title: 檢視從摘要產生的資料
description: 瞭解如何檢視從詳細目錄資料摘要產生的資料。
exl-id: 961155ac-a9d3-42e4-904b-b968e9f3383b
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# 檢視從摘要產生的資料

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

當您傳播摘要資料而不將其同時張貼至廣告網路時，可以使用下列其中一種方式預覽資料。 您稍後可以選擇使用 [張貼資料](propagated-data-post.md) 從任一位置連線到相關的廣告網路。

* 如果您使用「[!UICONTROL Propagate and Preview]，」然後檢視產生的大量表單(名為「`<feed file name>_<template name>`&quot;)從 [!UICONTROL Bulksheets] 檢視。 上不含任何資料 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。 此選項可讓您 [驗證登入頁面](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) 在張貼資料之前，與廣告和關鍵字相關聯。

* 如果您使用「[!UICONTROL Propagate only]，」然後從檢視行銷活動階層檢視中產生的資料 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。

  行銷活動階層檢視只會顯示摘要檔案產生的資料，不會顯示現有的帳戶元件。 元件及其所有子元件的資料發佈至廣告網路後，即不再列於行銷活動階層檢視中。

   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

   1. （選用）若只要顯示針對特定範本建立的行銷活動元件：

      1. 按一下範本名稱。

      1. 在 [!UICONTROL Accounts] 在左側導覽窗格中展開廣告網路節點和廣告網路帳戶節點，然後選取範本名稱旁的核取方塊。

   1. 按一下 **[!UICONTROL Campaigns]**， **[!UICONTROL Ad Groups]**， **[!UICONTROL Keywords]**，或 **[!UICONTROL Ads]** 標籤，視您要檢視的元件而定。

      >[!NOTE]
      >
      >* 除非您檢視特定範本的資料， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤會列出從所有範本和摘要檔案建立的所有廣告群組、關鍵字和廣告。 使用的產品群組 [!DNL Google Ads] 購物廣告會列於 [!UICONTROL Keywords] 標籤。
      >* 若只要檢視特定行銷活動的子元件，請先檢視 [!UICONTROL Campaigns] 標籤。 同樣地，若只要檢視特定廣告群組的子元件，請先檢視 [!UICONTROL Ad Groups] 標籤。

   1. （選擇性）若要檢視進一步資訊，請執行下列任一項作業：

      * 若要檢視任何促銷活動、廣告群組、關鍵字或廣告的設定，請按一下 [檢視/編輯設定圖示](/help/search-social-commerce/assets/settings.png "檢視/編輯設定圖示") 位於名稱旁。

      * 若要檢視行銷活動或廣告群組的子元件，請執行以下操作：

         * 若要列出行銷活動中的所有廣告群組，請按一下行銷活動名稱。

         * 若要列出廣告群組中的所有關鍵字或產品目標，請按一下廣告群組名稱。

         * 若要列出廣告群組中的所有廣告，請按一下廣告群組名稱，然後按一下 [!UICONTROL Ads] 標籤。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [從摘要產生的行銷活動資料張貼至廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
