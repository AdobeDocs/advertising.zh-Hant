---
title: 管理 [!DNL Google Ads] 動態搜尋目標
description: 瞭解如何建立和管理 [!DNL Google Ads] 動態搜尋目標。
exl-id: 85b1455a-dda1-4bb9-b4be-d6e0a837fd9d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 動態搜尋目標

*[!DNL Google Ads]僅限帳戶*

您可以針對使用搜尋網路的行銷活動，建立、編輯和變更動態搜尋目標的狀態。

>[!NOTE]
>
>您可以透過上傳一次建立和編輯大量目標資料 [大量工作表檔案](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 並張貼至廣告網路。

## 建立 [!DNL Google Ads] 動態搜尋目標

您可以建立動態搜尋目標，以定義網站中的頁面（即廣告顯示URL中使用的網域），其內容是用來鎖定相同廣告群組中的動態搜尋廣告。

您可以鎖定所有條件或最多三個個別條件。

>[!NOTE]
>
>若要取得最佳追蹤效能，請建立&quot;[!UICONTROL All Targets]「每個行銷活動僅定位一個廣告群組。

>[!TIP]
>
>若要同時建立多個帳戶元件，請使用 [行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路、帳戶、行銷活動和廣告群組，然後按一下 **[!UICONTROL Continue]**.

1. 指定 [動態搜尋目標設定](#dynamic-search-target-settings).

1. 按一下 **[!UICONTROL Post]**.

## 編輯 [!DNL Google Ads] 動態搜尋目標設定

您可以編輯的狀態或最高競標 [!DNL Google Ads] 動態搜尋目標。 您無法變更已鎖定目標的條件。

>[!TIP]
>
>若要一次編輯大量資料，請使用 [行銷活動大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. 選取要編輯之每一列旁的核取方塊。

   如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

1. 指定 [動態搜尋目標設定](#dynamic-search-target-settings).

   若為多個目標，您的變更會套用至所有選取的目標。 對於 [!UICONTROL Bid field]，您可以選擇將現有值變更為指定值，或透過指定百分比或貨幣金額（具有限制）來增加或減少金額。

1. 儲存資料：

   * （單一目標）按一下 **[!UICONTROL Post]**.

   * （多個廣告群組）按一下 **[!UICONTROL Post Now]**.

## 變更狀態 [!DNL Google Ads] 動態搜尋目標

您可以暫停支援之行銷活動型別中的任何作用中動態搜尋目標，以停止將其用於相同廣告群組中的動態搜尋廣告。 您稍後可以將廣告狀態變更回「作用中」，以使用這些廣告作為目標。

您也可以刪除任何動態目標。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. （選擇性）篩選清單以包含特定的動態目標。

1. 執行下列任一項作業：

   * 若要變更一個動態目標的狀態，請按一下 **[!UICONTROL Status]** 欄並變更狀態。

   * 若要刪除一或多個動態目標，請執行下列動作：

      1. 選取要刪除的每個動態目標旁的核取方塊。

     如需選取多個列的秘訣，請參閱&quot;[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

      1. 在工具列中，按一下 ![更多](/help/search-social-commerce/assets/more.png "更多") 並選取 **[!UICONTROL Delete]**.

      1. 在確認訊息中，按一下 **[!UICONTROL Delete]**.

## [!DNL Google Ads] 動態搜尋目標設定 {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]：** (若您未在行銷活動的欄位中指定網站網域和語言，則此為必要專案。 [!UICONTROL DSA Options] 區段；現有目標為唯讀)廣告群組的動態搜尋目標：

* *[!UICONTROL All Targets]* （預設值）：鎖定所有已編制索引的頁面。

* *\[特定目標\]：* 索引頁面的目標設定為最多三個條件。 選取此專案時，您必須指定資訊類別和特定值，以指定條件，針對此資訊類別和特定值來鎖定廣告（例如「URL包含shoes.example.com」）。 若要指定多個條件，請按一下 **[!UICONTROL + And]**. 目標條件包括：

   * *[!UICONTROL Category]：* 若要針對具有特定索引的頁面顯示廣告 [!DNL Google Ads] 內容類別。

   * *[!UICONTROL URL]：* 顯示具有特定URL之索引頁面的廣告，其中值可能包含在URL中的任何位置。

   * *[!UICONTROL Page Title]：* 若要顯示索引頁面的廣告，並在頁面標題中顯示特定文字。

   * *[!UICONTROL Page Content]：* 顯示具有特定內容之索引頁面的廣告。

**狀態：** 目標設定的狀態：

* *[!UICONTROL Active]* （預設）：啟用競標。

* *[!UICONTROL Paused]：* 停用競標。

* *[!UICONTROL Deleted]* （僅限現有目標）：刪除目標設定。

### [!UICONTROL Bids]

**[!UICONTROL Bid]：** 廣告的最大每次點按成本(CPC)或廣告的每1000次曝光成本(CPM)，適用於廣告網路和促銷活動定價模型。 此值會覆寫廣告群組層級值。

>[!NOTE]
>
>如果目標在最佳化的產品組合中，則會套用一天特定的CPC競標。 之後，最佳化功能會根據自己的計算來放置競標。

>[!MORELIKETHIS]
>
>* [關於 [!DNL Google Ads] 動態搜尋目標](dynamic-search-target-about.md)
