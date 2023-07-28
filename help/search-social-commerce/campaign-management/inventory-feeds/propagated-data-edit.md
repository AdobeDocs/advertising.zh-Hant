---
title: 編輯從摘要產生的資料
description: 瞭解如何編輯從詳細目錄資料摘要產生的資料。
exl-id: 5f866557-e44b-4fd9-9683-f7fbaf6d308b
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# 編輯從摘要產生的資料

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

當您傳播摘要資料而不將其同時張貼至廣告網路時，您可以透過下列其中一種方式來編輯資料。 您稍後可以選擇使用 [張貼資料](propagated-data-post.md) 從任一位置到相關廣告網路：

* 如果您使用「[!UICONTROL Propagate and Preview]，」然後您可以編輯產生的Bulksheet檔案(名為「`<feed file name>_<template name>`&quot;)，從下載 [!UICONTROL Bulksheets] 檢視、編輯檔案，然後再次上傳檔案。 上不含任何資料 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。

* 如果您使用「[!UICONTROL Propagate only]，」然後您就可以使用為元件編輯產生的資料 [[!UICONTROL New] 狀態](propagated-data-status.md) 在行銷活動階層檢視中 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤。

  行銷活動階層檢視只會顯示摘要檔案產生的資料，不會顯示現有的帳戶元件。 元件及其所有子元件的資料發佈至廣告網路後，即不再列於行銷活動階層中。

   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

   1. （選用）若只要顯示針對特定範本建立的行銷活動元件：

      1. 按一下範本名稱。

      1. 在 [!UICONTROL Accounts] 在左側導覽窗格中展開廣告網路節點和廣告網路帳戶節點，然後選取範本名稱旁的核取方塊。

   1. 按一下 **[!UICONTROL Campaigns]**， **[!UICONTROL Ad Groups]**， **[!UICONTROL Keywords]**，或 **[!UICONTROL Ads]** 標籤，視您要檢視的元件而定。

      >[!NOTE]
      >
      >* 除非您檢視特定範本的資料， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 索引標籤會列出從所有範本和摘要檔案建立的所有廣告群組、關鍵字和廣告。 使用的產品群組 [!DNL Google Ads] 購物廣告會列於 [!UICONTROL Keywords] 標籤。
      >* 若只要檢視特定行銷活動的子元件，請先檢視 [!UICONTROL Campaigns] 標籤。 同樣地，若只要檢視特定廣告群組的子元件，請先檢視 [!UICONTROL Ad Groups] 標籤。

   1. （選用；若要編輯僅限廣告群組、關鍵字或廣告）請篩選清單以僅包含特定促銷活動或廣告群組的子元件：

      * 若要列出行銷活動中的所有廣告群組，請按一下行銷活動名稱。

      * 若要列出廣告群組中的所有關鍵字，請按一下廣告群組名稱。

      * 若要將所有內容以廣告群組的形式列出，請按一下廣告群組名稱，然後按一下 [!UICONTROL Ads] 標籤。

   1. 按一下 [檢視/編輯設定圖示](/help/search-social-commerce/assets/settings.png "檢視/編輯設定圖示") 位於促銷活動、廣告群組、關鍵字或廣告名稱旁。

   1. 編輯設定，然後按一下 **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [從摘要產生的行銷活動資料張貼至廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
