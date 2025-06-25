---
title: 管理詳細目錄資料摘要檔案
description: 瞭解如何進行設定，以控制摘要資料的處理方式。
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# 管理詳細目錄資料摘要檔案

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

如果您提交自己的摘要資料，則必須上傳包含產品資料的檔案，以根據產品資料動態建立行銷活動結構、廣告和關鍵字。 然後，您可以將其與廣告網路特定的廣告範本建立關聯，並透過範本處理資料，最終將資料發佈到相關的廣告網路。 您可以將多個範本與一個摘要檔案相關聯，但每個範本只能與一個摘要檔案相關聯。

>[!NOTE]
>
>如果您直接從商戶中心帳戶使用資料，請勿上傳檔案。

您可以透過下列其中一種方式來上傳及處理資料摘要檔案：

* **自動使用FTP：**&#x200B;您可以直接將檔案上傳到FTP目錄；摘要服務每兩小時會檢查一次新檔案。 第一次上傳檔案後，您可以將其與廣告網路專用範本建立關聯。 稍後，您上傳的所有同名檔案會自動與相同範本建立關聯。 根據您[設定摘要資料設定的方式](feed-settings-manage.md)，搜尋、社交和Commerce可能會透過所有適用的範本自動傳播摘要資料，並選擇性地將產生的行銷活動和廣告資料發佈到相關的廣告網路。

  若要設定FTP目錄以儲存及自動處理資料檔案，請聯絡您的Adobe客戶團隊。

* **手動處理：**&#x200B;您可以從[!UICONTROL Advanced] (ACM)檢視手動[上傳摘要檔案](#feed-file-upload)。 將摘要檔案與一個或多個廣告網路特定的[範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)產生關聯後，您就可以根據[摘要資料設定](feed-settings-manage.md)，透過範本[傳播摘要資料](feed-data-propagate.md)來產生行銷活動和廣告資料。 您可以選擇在行銷活動階層檢視中預覽產生的資料、產生大量表單檔案以供檢閱，或產生大量表單檔案以供立即張貼至廣告網路。 如果您未立即張貼資料，則可以[預覽](propagated-data-view.md)並在稍後[張貼](propagated-data-post.md)。 您可以稍後[以新檔案](#feed-file-replace)取代現有的摘要檔案，而不會失去任何現有的範本關聯。

## 摘要檔案需求

個別檔案不需要特定資料欄位，但每個檔案都需要以下內容：

* 檔案中的第一行必須包含資料行名稱（也稱為&#x200B;*標題*），這些名稱會對應到關聯範本中的動態引數。 其餘行必須包含與欄名稱相對應的資料。 每個資料行（列）都必須只與一個帳戶元件有關，例如一個行銷活動或一個廣告。 所有行的值必須以定位字元或逗號分隔。 請參閱下面的[CSV範例檔案](#example-csv-feed-file)和[TSV範例檔案](#example-tsv-feed-file)。

* 檔案大小不限，但必須有下列其中一個副檔名： `.tsv` （用於定位點分隔值）、`.txt` （用於符合[!DNL Unicode]的ASCII文字）、`.csv` （用於逗號分隔值）或`.zip` （用於壓縮的ZIP格式單一檔案，這會解壓縮成TSV檔案）。

* 檔案名稱區分大小寫，且不能包含以下字元： `# % & * | \ : " < > . ? /`

* 如果您將檔案儲存在FTP目錄中，則每個檔案版本都必須使用相同的檔案名稱。

* （僅限[!DNL Google Ads]範本）如果您的範本在文字廣告中使用Param2或Param2廣告引數，則摘要檔案中的對應資料欄位必須包含數值資料，且不含貨幣符號。

* 若要更新現有帳戶元件，請包含現有行銷活動的名稱（及其元件，如果相關）。 如果未指定現有結構，則會建立新元件。

### 以逗號分隔的摘要檔案範例 {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### 以定位點分隔的摘要檔案範例 {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## 最佳實務

* 若資料包含國際字元，請使用TSV或TXT格式的檔案。

* 若要以有限的手動檢閱或編輯達到可重複的流程，請依照下列方式設定摘要檔案及其帳戶結構資料：

   * 包含足夠資料的欄和列，以建立帳戶結構或對映至現有的帳戶結構。 理想情況下，請使用與產品分類法密切相關的現有帳戶結構，且摘要資料可輕鬆對應至該結構。

   * 包括短到可在廣告復本中使用的說明。

   * 跨產品列使用一致的資料模式和命名慣例。

   * 移除所有前面空格和結尾空格。

   * 移除任何亂碼字元。

## 檢視或下載摘要檔案

您可以開啟或下載手動或使用FTP上傳的任何摘要檔案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

1. 找到摘要檔案：

1. 在範本清單中，找出使用摘要檔案的範本。

1. 在資料表格上方的工具列中，按一下&#x200B;**[!UICONTROL Feeds]**&#x200B;以開啟所有摘要檔案的清單。

1. 按一下摘要檔案名稱。

1. 依照瀏覽器的正常程式開啟或儲存檔案。

如需詳細資訊，請參閱瀏覽器的線上說明。

## 手動上傳摘要檔案 {#feed-file-upload}

>[!NOTE]
> 如果您將範本與手動上傳的檔案相關聯，但接著透過FTP上傳另一個具有相同名稱、副檔名和文法大小寫的檔案，則當您透過範本傳播資料時會使用FTP檔案。 例如，myfile.csv會取代myfile.csv，但Myfile.CSV則不會。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Feeds]**。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Upload]**。

1. 輸入完整路徑和檔案名稱，或按一下&#x200B;**[!UICONTROL Browse]**&#x200B;在您的裝置或網路上尋找檔案，以指定要上傳的檔案。

1. 按一下**[!UICONTROL Upload]。

將會驗證檔案中的所有欄位。 在更正值之前，您無法在稍後張貼欄位長度無效的專案。 檔案中的所有欄名稱都會在範本中成為動態引數。

## 取代摘要檔案 {#feed-file-replace}

當您取代摘要檔案時，即使新檔案具有不同的檔案名稱或副檔名，所有現有的範本關聯仍會保留。 當您透過最初與先前檔案相關聯的所有範本傳播資料時，會使用新檔案。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

1. 執行下列任一項作業：

   * 在任何適用範本的[!UICONTROL Feed]欄中，按一下![更多選項](/help/search-social-commerce/assets/options.png "更多選項")並選取&#x200B;**[!UICONTROL Re-upload]**。

   * 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Feeds]**。 在摘要檔案清單中，選取現有檔案名稱旁的核取方塊。 按一下資料表上方的&#x200B;**[!UICONTROL Upload]**。

   >[!NOTE]
   >
   >摘要檔案的來源（&quot;[!UICONTROL FTP]&quot;或手動上傳檔案的&quot;&amp;mdash&quot;）包含在[!UICONTROL Source]欄中。

1. 輸入完整路徑和檔案名稱，或按一下&#x200B;**[!UICONTROL Browse]**&#x200B;在您的裝置或網路上尋找檔案，以指定要上傳的檔案。

即使新檔案具有不同的檔案名稱或副檔名，現有的檔案也會被新檔案覆寫。

1. 按一下&#x200B;**[!UICONTROL Re-Upload]**。

將會驗證檔案中的所有欄位。 在更正值之前，您無法在稍後張貼欄位長度無效的專案。 檔案中的所有欄名稱都會在範本中成為動態引數。

## 刪除摘要檔案

您可以刪除任何手動或透過FTP上傳的摘要檔案。 當您刪除摘要檔案時，該檔案不再與任何範本相關聯。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，這會開啟至[!UICONTROL Templates]索引標籤。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Feeds]**。

1. 選取要刪除的每個檔案旁的核取方塊。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Yes]**。

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [透過範本傳播摘要資料](feed-data-propagate.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [從摘要產生的貼文行銷活動資料到廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)
