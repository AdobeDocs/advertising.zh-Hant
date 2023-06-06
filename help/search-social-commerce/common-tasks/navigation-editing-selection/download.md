---
title: 從行銷活動管理檢視下載資料
description: 瞭解如何從大多數的行銷活動管理檢視下載資料。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 從行銷活動管理檢視下載資料

您可以從以下位置下載資料： [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 檢視，但不包括 [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives]， [!UICONTROL Placements] - [!UICONTROL Placement Negatives]， [!UICONTROL Audiences]、和 [!UICONTROL Extensions] 檢視。 您可以下載：

* 中的報告 [!DNL XLSM] （啟用巨集） [!DNL Microsoft® Excel] 試算表)格式。 如果您在檢視中選取特定列，則報表會為每個選取的列包含一個列。 如果您未選取任何列，則會為檢視中的每一列建立一個列。

* TXT格式的Bulksheet檔案，包含所有相關的子圖元。 如果您為多個廣告網路上的實體選取列，則會為每個相關廣告網路建立一個檔案。 如果您未選取任何列，則會針對檢視中顯示的每個廣告網路建立一個檔案。 為不同廣告網路產生的大量表單檔案包含不同的資料欄。

   如果您產生多個行銷活動的資料，且合併的資料包含超過500,000列，則行銷活動會視需要將資料進一步分割為兩個或多個檔案，並命名為 `<bulksheet name>_1.txt`， `<bulksheet name>_2.txt`、等等。

   中的每個Bulksheet檔案 [!UICONTROL Downloads] 面板也會列於 [!UICONTROL Bulksheets] 檢視。 建立檔案後，您會收到電子郵件通知，其中包含下載檔案的連結；根據編譯的資料量，通知可能需要幾分鐘或更長時間。 但是，如果檔案產生失敗，則會在「大量表單」檢視中列出錯誤檔案，而您會收到電子郵件通知，其中包含錯誤檔案的連結。 從以下任一位置刪除大量工作表檔案： [!UICONTROL Download] 面板或 [!UICONTROL Bulksheets] tab會將其從兩個位置刪除。

1. （可選）選取要包含在檔案中的個別列。

   否則，會包含檢視中的所有資料。

1. 在工具列右側，按一下 ![報表下載](/help/search-social-commerce/assets/download.png "報表下載").

1. 按一下 ![建立](/help/search-social-commerce/assets/add.png "建立") **[!UICONTROL Create]**，並選擇性地新增檔案名稱，然後按一下 **[!UICONTROL Report]** 或 **[!UICONTROL Bulksheet]**.

1. （選用）報告工作完成後，請按一下 ![報表下載](/help/search-social-commerce/assets/download.png "報表下載") 若要檢視 [!UICONTROL Available Reports] 面板，然後下載或刪除報表：

   * 若要依照瀏覽器的正常程式開啟或儲存檔案，請按一下 ![下載試算表](/help/search-social-commerce/assets/download-spreadsheet.png "下載試算表").

      如需有關瀏覽器程式的詳細資訊，請參閱瀏覽器的線上說明。

   * 若要刪除檔案，請按一下 ![刪除](/help/search-social-commerce/assets/delete.png "刪除").

>[!MORELIKETHIS]
>
>[從刪除效能資料報表或Bulksheet檔案 [!UICONTROL Downloads] 功能表](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
