---
title: 管理詳細目錄資料摘要檔案
description: 瞭解如何設定控制摘要資料處理方式的設定。
source-git-commit: a0cdc0de763feeafdea57e4233b48a2c39449e1f
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# 管理詳細目錄資料摘要檔案

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （僅刪除動作），以及 [!DNL Yandex] 僅限帳戶*

如果您提交自己的摘要資料，則必須上傳包含您產品資料的檔案，以根據您的產品資料動態建立行銷活動結構、廣告和關鍵字。 然後，您可以將其與廣告網路特定的廣告範本建立關聯，並透過範本處理資料，最終將資料發佈到相關的廣告網路。 您可以將多個範本與一個摘要檔案相關聯，但每個範本只能與一個摘要檔案相關聯。

>[!NOTE]
>
>如果您直接使用商戶中心帳戶中的資料，請勿上傳檔案。

您可以透過下列其中一種方式來上傳及處理資料摘要檔案：

* **自動使用FTP：** 您可以直接將檔案上傳至FTP目錄；摘要服務每兩小時會檢查一次新檔案。 第一次上傳檔案後，您可以將其與廣告網路專用範本建立關聯。 稍後，您上傳的所有同名檔案都會自動關聯至相同的範本。 視您的方式而定 [設定摘要資料設定](feed-settings-manage.md)、Search、Social和Commerce可自動透過所有適用的範本傳播摘要資料，並可選擇將產生的行銷活動和廣告資料發佈到相關的廣告網路。

   若要設定FTP目錄以儲存及自動處理資料檔案，請聯絡您的Adobe帳戶團隊。

* **手動處理：** 您可以手動 [上傳摘要檔案](#feed-file-upload) 從 [!UICONTROL Advanced] (ACM)檢視。 將摘要檔案與一個或多個特定廣告網路建立關聯之後 [範本](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)，您可以透過以下方式產生行銷活動和廣告資料： [透過範本傳播摘要資料](feed-data-propagate.md) 根據 [摘要資料設定](feed-settings-manage.md). 您可以選擇在行銷活動階層檢視中預覽產生的資料、產生大量表單檔案以供稽核，或產生大量表單檔案以供立即張貼至廣告網路。 如果您未立即發佈資料，則可以 [預覽](propagated-data-view.md) 和 [張貼](propagated-data-post.md) 稍後。 您可以稍後再試 [以新檔案取代現有的摘要檔案](#feed-file-replace) 不會失去任何現有的範本關聯。

## 摘要檔案需求

個別檔案中不需要特定資料欄位，但每個檔案都需要以下內容：

* 檔案中的第一行必須包含欄名稱(也稱為 *標頭*)，此引數會對應至關聯範本中的動態引數。 其餘行必須包含與欄名稱相對應的資料。 每個資料行（列）都必須只與一個帳戶元件相關，例如一個行銷活動或一個廣告。 所有行上的值必須以定位字元或逗號分隔。 請參閱 [CSV範例檔案](#example-csv-feed-file) 和 [TSV範例檔案](#example-tsv-feed-file) 下方的。

* 檔案大小不限，但必須具備下列其中一種副檔名： `.tsv` （以定位點分隔的值）， `.txt` (適用於 [!DNL Unicode] — 相容的ASCII文字)、 `.csv` （逗號分隔值），或 `.zip` （適用於壓縮ZIP格式的單一檔案，會解壓縮成TSV檔案）。

* 檔案名稱會區分大小寫，且不能包含以下字元： `# % & * | \ : " < > . ? /`

* 如果您將檔案儲存在FTP目錄中，則每個檔案版本都必須使用相同的檔案名稱。

* ([!DNL Google Ads] （僅限範本）如果您的範本在文字廣告中使用Param2或Param2廣告引數，則摘要檔案中的對應資料欄位必須包含數值資料，且不含貨幣符號。

* 若要更新現有帳戶元件，請包含現有行銷活動的名稱（及其相關元件）。 如果未指定現有結構，則會建立新元件。

### 以逗號分隔的摘要檔案範例 {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### 以Tab分隔的摘要檔案範例 {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## 最佳實務

* 若資料包含國際字元，請使用TSV或TXT格式的檔案。

* 若要透過有限的手動稽核或編輯達到可重複流程，請依照以下方式設定摘要檔案及其帳戶結構資料：

   * 包含足以建立帳戶結構或對映至現有帳戶結構的資料欄和資料列。 理想情況下，請使用與產品分類法緊密相連的現有帳戶結構，且摘要資料可輕鬆對應至該結構。

   * 包括簡短到足以在廣告文案中使用的說明。

   * 跨產品列使用一致的資料模式和命名慣例。

   * 移除所有前面空格和結尾空格。

   * 移除任何亂碼字元。

## 檢視或下載摘要檔案

您可以開啟或下載手動或使用FTP上傳的任何摘要檔案。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 找到摘要檔案：

1. 在範本清單中，找到使用摘要檔案的範本。

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Feeds]** 以開啟所有摘要檔案的清單。

1. 按一下摘要檔案名稱。

1. 依照瀏覽器的正常程式開啟或儲存檔案。

如需詳細資訊，請參閱瀏覽器的線上說明。

## 手動上傳摘要檔案 {#feed-file-upload}

>[!NOTE]
> 如果您將範本與手動上傳的檔案相關聯，但接著透過FTP上傳另一個具有相同名稱、副檔名和文法大小寫的檔案，則當您透過範本傳播資料時會使用FTP檔案。 例如，myfile.csv會取代myfile.csv，但Myfile.CSV則不會。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Feeds]**.

1. 在資料表格上方，按一下 **[!UICONTROL Upload]**.

1. 輸入完整路徑和檔案名稱，或按一下「 」，指定要上傳的檔案 **[!UICONTROL Browse]** 以找出裝置或網路上的檔案。

1. 按一下 **[!UICONTROL Upload].

將會驗證檔案中的所有欄位。 在更正值之前，您稍後無法張貼具有無效欄位長度的專案。 檔案中的所有欄名稱在範本中會成為動態引數。

## 取代摘要檔案 {#feed-file-replace}

當您取代摘要檔案時，即使新檔案具有不同的檔案名稱或副檔名，所有現有的範本關聯仍會保留。 當您透過最初與先前檔案相關聯的所有範本傳播資料時，會使用新檔案。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 執行下列任一項作業：

   * 在 [!UICONTROL Feed] 欄，按一下 ![更多選項](/help/search-social-commerce/assets/options.png "更多選項") 並選取 **[!UICONTROL Re-upload]**.

   * 在資料表格上方的工具列中，按一下 **[!UICONTROL Feeds]**. 在摘要檔案清單中，選取現有檔案名稱旁的核取方塊。 在資料表格上方，按一下 **[!UICONTROL Upload]**.
   >[!NOTE]
   >
   >摘要檔案的來源(&quot;[!UICONTROL FTP]手動上傳檔案的「&amp;mdash」或「&amp;mdash」會包含在 [!UICONTROL Source] 欄。

1. 輸入完整路徑和檔案名稱，或按一下「 」，指定要上傳的檔案 **[!UICONTROL Browse]** 以找出裝置或網路上的檔案。

即使新檔案具有不同的檔案名稱或副檔名，現有檔案仍會以新檔案覆寫。

1. 按一下 **[!UICONTROL Re-Upload]**.

將會驗證檔案中的所有欄位。 在更正值之前，您稍後無法張貼具有無效欄位長度的專案。 檔案中的所有欄名稱在範本中會成為動態引數。

## 刪除摘要檔案

您可以刪除任何手動或透過FTP上傳的摘要檔案。 當您刪除摘要檔案時，它不再與任何範本相關聯。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，隨即開啟以 [!UICONTROL Templates] 標籤。

1. 在資料表格上方的工具列中，按一下 **[!UICONTROL Feeds]**.

1. 選取要刪除的每個檔案旁的核取方塊。

1. 在資料表格上方，按一下 **[!UICONTROL Delete]**.

1. 在確認訊息中，按一下 **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [關於詳細目錄摘要](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [透過範本傳播摘要資料](feed-data-propagate.md)
>* [檢視從摘要產生的資料](propagated-data-view.md)
>* [編輯從摘要產生的資料](propagated-data-edit.md)
>* [從摘要產生的行銷活動資料張貼至廣告網路](propagated-data-post.md)
>* [停止庫存摘要資料的張貼工作](stop-job.md)
>* [從摘要產生的資料狀態](propagated-data-status.md)

