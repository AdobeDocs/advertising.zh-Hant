---
title: 編輯從摘要產生的資料
description: 瞭解如何編輯從詳細目錄資料摘要產生的資料。
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# 編輯從摘要產生的資料

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

當您傳播摘要資料而不將其同時張貼至廣告網路時，您可以透過下列其中一種方式來編輯資料。 您稍後可以選擇從任一位置[張貼資料](propagated-data-post.md)至相關廣告網路：

* 如果您使用&quot;[!UICONTROL Propagate and Preview]&quot;的選項，則您可以編輯產生的大量表單檔案（名為&quot;`<feed file name>_<template name>`&quot;），方法是從[!UICONTROL Bulksheets]檢視下載該檔案，編輯該檔案，然後再次上傳。 [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤上未包含任何資料。

* 如果您使用「[!UICONTROL Propagate only]」選項，則可以從[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤，編輯行銷活動階層檢視中[[!UICONTROL New]狀態為](propagated-data-status.md)之元件的已產生資料。

  行銷活動階層檢視只會顯示摘要檔案產生的資料，不會顯示現有的帳戶元件。 元件及其所有子元件的資料發佈至廣告網路後，即不再列於行銷活動階層中。

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

   1. （選用）若只要顯示針對特定範本建立的行銷活動元件：

      1. 按一下範本名稱。

      1. 在左側導覽窗格的[!UICONTROL Accounts]功能表中，展開廣告網路節點和廣告網路帳戶節點，然後選取範本名稱旁的核取方塊。

   1. 視您要檢視的元件而定，按一下「**[!UICONTROL Campaigns]**」、「**[!UICONTROL Ad Groups]**」、「**[!UICONTROL Keywords]**」或「**[!UICONTROL Ads]**」標籤。

      >[!NOTE]
      >
      >* 除非您檢視特定範本的資料，[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤會列出所有範本和摘要檔案中建立的所有廣告群組、關鍵字和廣告。 用於[!DNL Google Ads]購物廣告的產品群組列在[!UICONTROL Keywords]索引標籤上。
      >* 若只要檢視特定行銷活動的子元件，請先檢視[!UICONTROL Campaigns]標籤。 同樣地，若要只檢視特定廣告群組的子元件，請先檢視[!UICONTROL Ad Groups]標籤。

   1. （選用；若要編輯僅限廣告群組、關鍵字或廣告）請篩選清單以僅包含特定行銷活動或廣告群組的子元件：

      * 若要列出行銷活動中的所有廣告群組，請按一下行銷活動名稱。

      * 若要列出廣告群組中的所有關鍵字，請按一下廣告群組名稱。

      * 若要將所有內容以廣告群組的形式列出，請按一下廣告群組名稱，然後按一下「[!UICONTROL Ads]」標籤。

   1. 按一下行銷活動、廣告群組、關鍵字或廣告名稱旁的[檢視/編輯設定圖示](/help/search-social-commerce/assets/settings.png "檢視/編輯設定圖示")。

   1. 編輯設定，然後按一下&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [從摘要產生的貼文行銷活動資料到廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
