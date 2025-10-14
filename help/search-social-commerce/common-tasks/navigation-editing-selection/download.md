---
title: 從行銷活動管理檢視下載資料
description: 瞭解如何從大多數的行銷活動管理檢視下載資料。
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 723d50d11cd76471ac41d3bb007af4f5d1bfa32f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# （舊版UI）從行銷活動管理檢視下載資料

*舊版使用者介面*

您可以從[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]檢視下載資料，但[!UICONTROL Keywords] - [!UICONTROL Keyword Negatives]、[!UICONTROL Placements] - [!UICONTROL Placement Negatives]、[!UICONTROL Audiences]和[!UICONTROL Extensions]檢視除外。 您可以下載：

* [!DNL XLSM] （啟用巨集的[!DNL Microsoft Excel]試算表）格式的報告。 如果您在檢視中選取特定列，則報表會為每個選取的列包含一個列。 如果您未選取任何列，則會為檢視中的每一列建立一個列。

* TXT格式的區塊工作表檔案，包含所有相關的子圖元。 如果您為多個廣告網路上的實體選取列，則會為每個相關廣告網路建立一個檔案。 如果您未選取任何列，則會針對檢視中顯示的每個廣告網路建立一個檔案。 為不同廣告網路產生的大量表單檔案包含不同的資料欄。

  如果您產生多個行銷活動的資料，且合併的資料包含超過500,000列，則行銷活動會視需要將資料進一步分割為兩個或多個檔案（名為`<bulksheet name>_1.txt`、`<bulksheet name>_2.txt`等）。

  [!UICONTROL Downloads]面板中的每個Bulksheet檔案也會列在[!UICONTROL Bulksheets]檢視中。 建立檔案時，您會收到電子郵件通知，其中包含下載檔案的連結；根據編譯的資料量，通知可能需要幾分鐘或更長時間。 但是，如果檔案產生失敗，則「大量表單」檢視中會列出錯誤檔案，而您會收到電子郵件通知，其中包含錯誤檔案的連結。 從[!UICONTROL Download]面板或[!UICONTROL Bulksheets]索引標籤刪除Bulksheet檔案時，會將它從這兩個位置刪除。

>[!NOTE]
>
>另請參閱從&quot;[[!UICONTROL Portfolios]檢視](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)&quot;、&quot;[[!UICONTROL Campaigns]檢視](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)&quot;和&quot;[[!UICONTROL Ad Groups]檢視](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md)&quot;下載新使用者介面中的資料的相關說明。

1. （可選）選取要包含在檔案中的個別列。

   否則，檢視中的所有資料都會包括在內。

1. 按一下工具列右側的![報告下載](/help/search-social-commerce/assets/download.png "報告下載")。

1. 按一下[建立] ![&#x200B; &#x200B;](/help/search-social-commerce/assets/add.png " [建立] ") **[!UICONTROL Create]**，可選擇新增檔案名稱，然後按一下[建立] **[!UICONTROL Report]**&#x200B;或[建立] **[!UICONTROL Bulksheet]**。

1. （選擇性）報告工作完成後，按一下![報告下載](/help/search-social-commerce/assets/download.png "報告下載")以檢視[!UICONTROL Available Reports]面板，然後下載或刪除報告：

   * 若要依照瀏覽器的正常程式開啟或儲存檔案，請按一下![下載試算表](/help/search-social-commerce/assets/download-spreadsheet.png "下載試算表")。

     如需有關瀏覽器程式的詳細資訊，請參閱瀏覽器的線上說明。

   * 若要刪除檔案，請按一下![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

>[!MORELIKETHIS]
>
>* [（舊版UI）從[!UICONTROL Downloads]功能表刪除效能資料報告或大量表單檔案](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [（新UI）從[!UICONTROL Portfolios]檢視管理資料檢視報告](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)
>* [（新UI）從[!UICONTROL Campaigns]檢視管理資料檢視報告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)
>* [（新UI）從[!UICONTROL Ad Groups]檢視管理資料檢視報告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md)
