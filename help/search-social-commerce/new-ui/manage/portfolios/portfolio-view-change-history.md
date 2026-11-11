---
title: （新UI）檢視產品組合的變更記錄和競標變更記錄
description: 瞭解如何在Adobe Advertising Search、Social和Commerce中檢視產品組合變更和競標變更歷史記錄、變更日期範圍、篩選產品組合變更，以及產生、下載和刪除歷史記錄報告。
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
source-git-commit: e7e0221adbb72127a9e6d2354b6a235b233a4a76
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---
# （新UI）檢視產品組合的變更記錄和競標變更記錄

*Beta功能*

您可以檢視在任何日期範圍內對投資組合進行的變更記錄。 記錄的動作包括投資組合建立、投資組合設定的所有變更、投資組合指派或未指派的所有行銷活動、投資組合中競標單位套用或移除的所有限制、投資組合中已過期競標單位的所有限制，以及影響投資組合的其他動作。

[!UICONTROL Change History]對話方塊包含用於投資組合變更的[!UICONTROL Portfolio Change History]索引標籤和用於競標歷程記錄的[!UICONTROL Portfolio Bid Change History]索引標籤。 依預設，這兩個索引標籤都會顯示最近180天，昨天結束。

您可以依類別篩選產品組合變更，並變更任一索引標籤的日期範圍。 您也可以將資料下載至試算表檔案。

## 檢視投資組合的變更記錄 {#portfolio-change-history}

每個變更的資訊包括[!UICONTROL Change Date]、[!UICONTROL Changed By]、[!UICONTROL Change Type]和[!UICONTROL Description]。 變更會從最新到最舊列出。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 將游標停留在投資組合列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Change History]**。

1. 在[!UICONTROL Change History]對話方塊中，檢視&#x200B;**[!UICONTROL Portfolio Change History]**&#x200B;索引標籤。

1. （可選）變更顯示的資訊：

   * 按一下![行事曆](/help/search-social-commerce/assets/calendar-new.png "行事曆")以變更報告的日期範圍。

   * 按一下![篩選](/help/search-social-commerce/assets/filter-new.png "篩選")以依類別篩選資料： [!UICONTROL All]、[!UICONTROL Objective]、[!UICONTROL Campaign]、[!UICONTROL Target]、[!UICONTROL Constraints]、[!UICONTROL Optimization Levers]或[!UICONTROL Others]。

## 檢視投資組合的競標變更記錄 {#portfolio-bid-change-history}

1. [開啟投資組合的變更記錄](#portfolio-change-history)。

1. 按一下「**[!UICONTROL Portfolio Bid Change History]**」標籤。

1. （選擇性）按一下![行事曆](/help/search-social-commerce/assets/calendar-new.png "行事曆")以變更日期範圍。

1. （選用）按一下日期欄標題，依日期遞增或遞減順序排序清單。

若要檢視個別競標單位的歷程記錄，請[從投資組合的效能詳細資料](portfolio-details.md#bid-unit-history)開啟競標單位詳細資料。 當[!UICONTROL Bid Unit ID]資料行可用時，您也可以[從[!UICONTROL Keywords]檢視](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history)開啟競標單位歷史記錄。

## 管理投資組合變更歷史的報告

您可以將投資組合變更記錄的額外資訊下載到[!DNL Microsoft Excel]活頁簿（XLSX檔案）格式的檔案中。 報表包含數值變更ID、舊值和新值、變更型別（例如「已新增」或「已修改」）、動作型別（例如「預算」或「Portfolio名稱」）和子型別（如果適用）、時間和使用者名稱。

您也可以從[!UICONTROL Portfolio Bid Change History]索引標籤產生、下載和刪除報告。 報表設定標題為[!UICONTROL Portfolio History]代表投資組合變更，標題為[!UICONTROL Portfolio Bid History]代表競標歷史記錄。

### 產生含有已篩選資料列的報表

1. [開啟投資組合的變更記錄](#portfolio-change-history)，然後按一下您要下載其資料的標籤。

1. 按一下右上角的![下載報表](/help/search-social-commerce/assets/download.png "下載報表")。

1. 在[!UICONTROL Portfolio History]或[!UICONTROL Portfolio Bid History]設定中，接受預設報告名稱或輸入唯一報告名稱，然後按一下&#x200B;**[!UICONTROL Generate]**。

   依預設，報表名稱包含歷史記錄型別以及日期和時間，格式為`YYYYMMDD_HHmm`，例如&quot;portfolioChangeHistory_20260402_1326&quot;。 如果名稱已存在，則會新增數值尾碼。

   檔案已新增至[!UICONTROL Recently Generated]清單。

1. （選擇性）若要在檔案完成後下載檔案，請按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 下載完成的報表

1. [開啟投資組合的變更記錄](#portfolio-change-history)，然後按一下您產生報表的標籤。

1. 按一下右上角的![下載報表](/help/search-social-commerce/assets/download.png "下載報表")。

1. 在[!UICONTROL Portfolio History]或[!UICONTROL Portfolio Bid History]設定的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 刪除已完成的報告

1. [開啟投資組合的變更記錄](#portfolio-change-history)，然後按一下您產生報表的標籤。

1. 按一下右上角的![下載報表](/help/search-social-commerce/assets/download.png "下載報表")。

1. 在[!UICONTROL Portfolio History]或[!UICONTROL Portfolio Bid History]設定的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![刪除](/help/search-social-commerce/assets/delete-new.png "刪除")。

>[!MORELIKETHIS]
>
>* [建立投資組合](portfolio-create.md)
>* [&#x200B; （新使用者介面）編輯投資組合](portfolio-edit.md)
>* [（新使用者介面）檢視投資組合效能詳細資料](portfolio-details.md)
>* [&#x200B; （新UI）在[!UICONTROL Portfolios]檢視中下載資料](portfolio-view-report.md)
>* [關於投資組合](portfolio-about.md)
