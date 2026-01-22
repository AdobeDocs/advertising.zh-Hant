---
title: 使用大量工作表檔案大量編輯投資組合設定
description: 瞭解如何使用Bulksheet檔案編輯多個投資組合的設定。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 8b63f697278b5dc4ecbb720af44053fbc771273f
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# 使用大量工作表檔案大量編輯投資組合設定

*Beta功能*

產品組合大量表單是包含特定格式的產品組合設定的檔案，可用來快速檢閱和修改設定。 您可以使用一或多個投資組合的設定來產生（下載）大量表單。 檔案下載為[!DNL Excel]活頁簿，內含兩個工作表（XLSX格式）。 活頁簿包含：

* 含有編輯欄位相關資訊的唯讀[!UICONTROL Instructions]工作表。

* [!UICONTROL Portfolio Settings Edit]索引標籤，每個包含的組合各有一列。 您可以選擇視需要編輯欄位，將檔案儲存在本機，然後[將編輯後的檔案](#portfolio-bulksheet-upload)上傳至Search、Social和Commerce。 可編輯欄位會以顏色反白顯示。

## 下載包含投資組合設定的大量表單檔案

1. （選擇性）選取每個投資組合旁的核取方塊，以包含在Bulksheet中。

   如果您未選取特定產品組合，則可下載所有產品組合的設定。

1. 在資料表格上方的工具列中，按一下：

   * （適用於所有投資組合） **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export All Portfolios]**。

   * （針對選取的投資組合） **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**。

1. 輸入要建立的Bulksheet檔案名稱，然後按一下&#x200B;**[!UICONTROL Export Now]**。

   檔案會儲存至瀏覽器的預設「下載」資料夾。

## 上傳包含更新後產品組合設定的大量表單檔案 {#portfolio-bulksheet-upload}

檔案必須是XLSX格式。

1. 在資料表上方的工具列中，按一下&#x200B;**[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**。

1. 在[!UICONTROL Import Portfolio Details File]對話方塊：

   1. 將檔案拖放至方塊中，或按一下&#x200B;**[!UICONTROL Browse File]**&#x200B;從您的裝置或網路選取檔案。

   1. 按一下&#x200B;**[!UICONTROL Import]**。

您可以從日期範圍選取器旁的[!UICONTROL Global Sync Status]按鈕（![全域同步狀態](/help/search-social-commerce/assets/global-sync-status.png "全域同步狀態")）檢查上傳狀態。 如果有任何變更未成功，您可以下載顯示失敗內容的錯誤檔案。

通知也會新增至通知中心，您可以從![按鈕(](/help/search-social-commerce/assets/notifications-new.png ")旁的")通知[!UICONTROL Global Sync Status]通知![全域同步狀態](/help/search-social-commerce/assets/global-sync-status.png "全域同步狀態")圖示開啟「通知」窗格。

## 已上傳大量工作表檔案的資料需求

所有Bulksheet檔案都必須包含資料行[!UICONTROL Portfolio ID]，而且每個資料列都必須包含[!UICONTROL Portfolio ID]的值才能執行。 如需資料需求的詳細資訊，請參閱已下載Bulksheet檔案上的[!UICONTROL Instructions]標籤。

如需[!UICONTROL Portfolio Settings Edit]標籤上產品組合設定欄的解釋，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [&#x200B; （新使用者介面）編輯投資組合](portfolio-edit.md)
>* [建立投資組合](portfolio-create.md)
>* [（新UI）關於投資組合](portfolio-about.md)
