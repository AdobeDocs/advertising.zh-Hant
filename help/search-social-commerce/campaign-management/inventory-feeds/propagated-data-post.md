---
title: 從摘要產生的行銷活動資料張貼至廣告網路
description: 瞭解如何將詳細目錄資料摘要產生的資料發佈到廣告網路。
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# 從摘要產生的行銷活動資料張貼至廣告網路

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

您可以在透過相關範本傳播資料時，或以個別程式發佈從摘要產生的促銷活動資料。 一旦您張貼資料，任何現有的傳播資料都會從[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]清單中移除。

為了張貼成功，所有廣告群組都必須指派給促銷活動，所有關鍵字和廣告都必須指派給廣告群組，並且必須包括所有必要的資訊，不得有任何長度違規。

* 如果您使用選項「[!UICONTROL Propagate and Preview]」，則[從[!UICONTROL Bulksheets]檢視張貼產生的Bulksheet檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) （名為「`<feed file name>_<template name>`」）。

  如果您先前未[驗證登入頁面](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)，您可以在張貼檔案之前先進行驗證。

* 如果您使用「[!UICONTROL Propagate only]」選項，則可以從[!UICONTROL Templates]索引標籤在行銷活動階層檢視中張貼具有[[!UICONTROL New]狀態](propagated-data-status.md)之元件的已產生資料。

  >[!NOTE]
  >
  >作用中或刪除的元件可能包含新的子元件，如果資料有效，則可張貼子元件。

  >[!TIP]
  >
  >如果您先前未驗證登入頁面，但想要驗證，請[傳播資料並從[!UICONTROL Bulksheets]檢視預覽](feed-data-propagate.md)，而非張貼至廣告網路。 您可以[先驗證URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)，再手動將檔案張貼至廣告網路。

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

   1. 選取範本旁的核取方塊。

   1. 在工具列中按一下&#x200B;**[!UICONTROL Post]**。

   1. 在張貼設定中，在欄位中輸入或選取資訊，然後按一下&#x200B;**[!UICONTROL Post]**。

      * **[!UICONTROL Selection]：**&#x200B;已過帳的帳戶元件。

      * **[!UICONTROL Scheduling]：**&#x200B;何時發佈檔案：

         * *[!UICONTROL Post to search engine now]* （預設值）：從傳播摘要資料建立大量工作表檔案，並立即開始張貼。

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]：*&#x200B;建立Bulksheet檔案並於稍後發佈。 指定下列專案：

            * **[!UICONTROL Start Time]：**&#x200B;將來應該將Bulksheet檔案張貼至廣告網路的日期和時間。 預設情況下，檔案會在隔天的00:00 (12:00 a.m.)傳送。 **注意：**&#x200B;對於需要較長處理時間的大型檔案，已發佈的資料無法立即在行銷活動管理檢視或網路的廣告管理員中使用。

            * **[!UICONTROL End Time]：**&#x200B;根據「[!UICONTROL When the Scheduled End Date is reached]」的[摘要資料設定](feed-settings-manage.md#feed-data-settings)，未來可能會暫停或刪除已張貼廣告的日期和時間。 預設的結束時間是從今天開始的00:00 （上午12:00） 30天。 選取「**[!UICONTROL None]**」以無限期地讓資料保持作用中（或直到您為範本傳播新資料為止），或指定日期和時間。

              若要指定日期，請使用DD/MM/YYYY或D/M/YYYY格式，或按一下![行事曆](/help/search-social-commerce/assets/calendar.png "行事曆")開啟行事曆，然後[選取日期](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md)。 若要變更時間，請以24小時格式（HH/MM或H/M）輸入時間，或從清單中選取時間（以30分鐘為間隔）。

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]：**&#x200B;建立可從[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets]檢視取得的大量工作表檔案。 您可以選擇從那裡發佈檔案。

           當產生的大量表單檔案超過2 MB時，該檔案會採用ZIP格式。 您不需要解壓縮檔案即可發佈。

      * **[!UICONTROL Generate Tracking URLs]：**&#x200B;是否要在大量表單檔案中包含關鍵字和廣告變數的追蹤URL： *[!UICONTROL Yes]* （預設）或&#x200B;*[!UICONTROL No]*。

        如果您選取&#x200B;*[!UICONTROL Yes]*，則會根據[帳戶設定](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)中的[!UICONTROL Tracking Methods]引數，或如果您要將資料對應到現有的促銷活動，則將資料對應到現有[促銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)中的[!UICONTROL Tracking Methods]引數，從關鍵字和廣告的基本URL產生URL。

        如果相關專案存在追蹤URL，則不會重新產生，除非需要新專案（例如如果關鍵字元合型別、創意文字或帳戶的追蹤引數已變更）。

      * **[!UICONTROL Bulksheet Name]：**&#x200B;要從傳播摘要資料建立的Bulksheet檔案名稱。 依預設，檔案名稱為`<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`。 您可以視需要重新命名檔案，但檔案的結尾必須是下列其中一個副檔名： `.tsv` （以Tab分隔的值）、`.txt` （以ASCII文字表示）、`.csv` （以逗號分隔的值）或`.zip` （以壓縮的TSV檔案表示）。 若資料包含國際字元，請使用TSV或TXT格式。

        張貼的檔案可在[!UICONTROL Bulksheets]檢視中使用30天，無論您是否張貼至廣告網路。

「[!UICONTROL Last Prop. Status]」欄顯示適用範本的工作狀態。

建立大量表單時，它會列在[!UICONTROL Bulksheets]檢視中。 發佈檔案時，會傳送包含檔案連結的電子郵件通知。 但是，如果無法張貼全部或部分資料，則會在[!UICONTROL Bulksheets]檢視中列出錯誤檔案，並傳送包含錯誤檔案連結的電子郵件通知。

>[!NOTE]
>
>* 無論您選取的排程選項為何，指定的資料都會從[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]清單中移除。
>* 處理大量資料需要更長的時間。 您可以在過程中追蹤檔案的進度。
>* 所有張貼的資料都受限於網路的編輯程式。
>* 在張貼Bulksheet檔案之前，您可以[取消張貼](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md)。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](inventory-feeds-about.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
