---
title: 檢視從摘要產生的資料
description: 瞭解如何檢視從詳細目錄資料摘要產生的資料。
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# 檢視從摘要產生的資料

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

當您傳播摘要資料而不將其同時張貼至廣告網路時，可以使用下列其中一種方式預覽資料。 您稍後可以選擇從任一位置[張貼資料](propagated-data-post.md)至相關廣告網路。

* 如果您使用&quot;[!UICONTROL Propagate and Preview]&quot;的選項，請從[!UICONTROL Bulksheets]檢視中檢視產生的Bulksheet （名為&quot;`<feed file name>_<template name>`&quot;）。 [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤上未包含任何資料。 此選項可讓您在張貼資料之前[驗證與廣告和關鍵字相關聯的登入頁面](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)。

* 如果您使用「[!UICONTROL Propagate only]」選項，請在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤中，檢視促銷活動階層檢視內產生的資料。

  行銷活動階層檢視只會顯示摘要檔案產生的資料，不會顯示現有的帳戶元件。 元件及其所有子元件的資料發佈至廣告網路後，即不再列於行銷活動階層檢視中。

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

   1. （選用）若只要顯示針對特定範本建立的行銷活動元件：

      1. 按一下範本名稱。

      1. 在左側導覽窗格的[!UICONTROL Accounts]功能表中，展開廣告網路節點和廣告網路帳戶節點，然後選取範本名稱旁的核取方塊。

   1. 視您要檢視的元件而定，按一下「**[!UICONTROL Campaigns]**」、「**[!UICONTROL Ad Groups]**」、「**[!UICONTROL Keywords]**」或「**[!UICONTROL Ads]**」標籤。

      >[!NOTE]
      >
      >* 除非您檢視特定範本的資料，[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]索引標籤會列出所有範本和摘要檔案中建立的所有廣告群組、關鍵字和廣告。 用於[!DNL Google Ads]購物廣告的產品群組列在[!UICONTROL Keywords]索引標籤上。
      >* 若只要檢視特定行銷活動的子元件，請先檢視[!UICONTROL Campaigns]標籤。 同樣地，若要只檢視特定廣告群組的子元件，請先檢視[!UICONTROL Ad Groups]標籤。

   1. （選擇性）若要檢視進一步資訊，請執行下列任一項作業：

      * 若要檢視任何促銷活動、廣告群組、關鍵字或廣告的設定，請按一下名稱旁的[檢視/編輯設定圖示](/help/search-social-commerce/assets/settings.png "檢視/編輯設定圖示")。

      * 若要檢視行銷活動或廣告群組的子元件，請執行以下操作：

         * 若要列出行銷活動中的所有廣告群組，請按一下行銷活動名稱。

         * 若要列出廣告群組中的所有關鍵字或產品目標，請按一下廣告群組名稱。

         * 若要列出廣告群組中的所有廣告，請按一下廣告群組名稱，然後按一下「[!UICONTROL Ads]」標籤。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [從摘要產生的貼文行銷活動資料到廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
