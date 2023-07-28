---
title: 使用複製並貼上大量建立和編輯行銷活動資料
description: 瞭解如何使用複製並貼上功能大量管理行銷活動資料。
exl-id: 09454f19-221b-43bb-ac74-f2c121329422
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# 使用複製並貼上大量建立和編輯行銷活動資料

*[!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex] 僅限帳戶*

*[!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 檢視*

您最多可以複製10,000列 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 檢視，並將它們貼到 [!DNL Microsoft Excel] 或其他編輯器以編輯任何非ID欄位。 接著，您就可以複製 [!DNL Excel] 列，並將它們以定位點分隔的資料貼回檢視以進行變更。 此功能使用您電腦的剪貼簿。

您可以使用此功能編輯現有的促銷活動物件（包含ID欄位），並建立不含ID欄位的新促銷活動物件。

## 複製資料列

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. 選取要複製的每一列旁的核取方塊。

   您最多可以複製10,000列。

1. 在資料表格上方的工具列中，按一下 ![更多](/help/search-social-commerce/assets/more.png "更多")，然後按一下 **[!UICONTROL Copy]**.

   或者，您可以使用作業系統的「複製」鍵盤指令，例如 **[!DNL Ctrl+C]** 的 [!DNL Microsoft Windows] 或 **[!DNL Command-C]** 的 [!DNL Apple Mac].

1. 在 [!UICONTROL Copy to Clipboard] 對話方塊，按一下 **[!UICONTROL Continue]**. 當資料準備複製時，請按一下 **[!UICONTROL Copy]**.

1. 將列貼入 [!DNL Excel] 或其他編輯者。

## 編輯和建立資料列

1. 根據下列要求編輯資料：

   * 貼上的資料必須包含標題列和必要的行銷活動物件值；請參閱 [百度](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)， [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)， [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)， [導覽](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)， [Yahoo！ 顯示網路](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)， [Yahoo！ 日本](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)、和 [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). 欄順序並不重要。

      * 對於要編輯的現有物件，您必須包含所有相關的ID欄、實體名稱以及要編輯的屬性。 請勿編輯物件的數值ID。

      * 對於新的促銷活動物件，請包括所有相關的實體名稱和屬性，但不包括物件ID （自動產生）。 例如，若您建立新廣告，請將 [!UICONTROL Ad ID] 欄位空白。 當您張貼物件時，廣告網路會自動建立ID。

   * 任何非必要欄中的值可能為Null （空白），但每一列必須具有相同數目的定位字元分隔值。

1. 將資料儲存為定位字元分隔的值。

## 將資料列貼入行銷活動管理檢視

>[!NOTE]
>
>如果貼上的列包含與現有實體相同或重複現有實體的任何資料，則會忽略重複資料。

1. 在 [!DNL Excel] 或其他編輯器，複製相關的定位點分隔列。

1. 在「搜尋、社交和商務」主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 開啟要貼上資料的檢視(**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**)。

1. 在資料表格上方的工具列中，按一下 ![更多](/help/search-social-commerce/assets/more.png "更多")，然後按一下 **[!UICONTROL Paste]**.

   或者，您可以使用作業系統的「貼上」鍵盤指令，例如 **[!DNL Ctrl+V]** 的 [!DNL Microsoft Windows] 或 **[!DNL Command-V]** 的 [!DNL Apple Mac].

1. 將資料貼入輸入方塊，然後按一下 **[!UICONTROL Process]**.

1. （選擇性）輸入其他詳細資料：

   * (如果 **[!UICONTROL Additional Details]** 已壓縮)按一下 ![開啟](/help/search-social-commerce/assets/chevron-up.png "開啟") 以展開詳細資訊。

   * 輸入選擇性的 **[!UICONTROL Job Name]** 和/或選填 **[!UICONTROL Job Description]**.

1. 按一下 **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [直接在列中編輯設定](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [管理行銷活動](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [管理廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [管理關鍵字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [管理廣告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
