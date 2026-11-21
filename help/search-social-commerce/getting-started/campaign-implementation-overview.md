---
title: 設定廣告網路帳戶和行銷活動
description: 請依照廣告網路連線、行銷活動、追蹤、轉換量度和選用產品組合最佳化的設定工作流程操作。
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# 設定廣告網路帳戶和行銷活動

*Beta功能*

[!DNL Adobe]和您的代理商會與您合作，以連線您的廣告網路帳戶、準備行銷活動、設定追蹤及驗證績效資料。 如果您希望Search、Social和Commerce最佳化合格的行銷活動，工作流程也包含產品組合設定。

此檢查清單提供更廣泛的[實作工作流程](implemention-overview.md)的帳戶和行銷活動詳細資料。 您可以執行的工作取決於您的許可權以及每個廣告網路和行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)支援的[功能。

## 設定工作流程

1. **確認存取和帳戶需求。**

   與您的管理員合作，確認對適當廣告商的存取權以及您任務所需的許可權。 請參閱[搜尋、社交和Commerce的使用者管理](/help/search-social-commerce/user-administration.md)。

   如有必要，請在廣告網路的網站上建立實際的廣告網路帳戶。 在Search、Social和Commerce中建立帳戶記錄時，不會在廣告網路上建立帳戶。

1. **連線或註冊每個廣告網路帳戶。**

   在[!UICONTROL Manage] > [!UICONTROL Accounts]中，使用[帳戶型別](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)的工作流程：

   * **API連線：** [建立帳戶詳細資料](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account)、完成網路特定驗證、設定追蹤選項，以及啟用帳戶。 驗證其[驗證及存取狀態](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status)；成功的驗證不一定表示已授與所有必要的許可權。

   * **資料上傳：** [建立帳戶詳細資料，並上傳行銷活動和績效資料](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md)。 這些帳戶不會與廣告網路同步，或支援組合最佳化。

   * **[!DNL Naver]僅限追蹤：**&#x200B;請遵循[僅限追蹤的帳戶工作流程](/help/search-social-commerce/manage/accounts/template-account-manage.md)。 使用大量表單來產生追蹤URL，並在廣告網路的編輯器中套用；該帳戶不會同步或支援組合最佳化。

1. **檢閱或建立行銷活動結構。**

   針對API連線的帳戶，請檢閱已同步的行銷活動及其元件。 [必要時要求手動同步](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md)。

   對於支援的行銷活動型別，請使用[!UICONTROL Manage] > [!UICONTROL Campaigns]來[建立或編輯行銷活動](/help/search-social-commerce/manage/campaigns/campaign-manage.md)。 建立必要的[廣告群組](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md)、[廣告](/help/search-social-commerce/manage/ads/ad-manage.md)和其他支援的元件。 您也可以使用[Bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md)進行支援的大量作業。

   在啟動行銷活動之前，完成任何必要的網路專屬設定。 管理廣告網路本身介面中不支援的元件。

1. **啟動前設定及驗證追蹤。**

   Select符合您實作的[轉換追蹤方法](/help/search-social-commerce/tracking/conversion-tracking-about.md)。 必要時，[產生並套用點選追蹤URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)和[產生轉換追蹤標籤](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md)。

   設定任何必要的[整合](/help/integrations/home.md)或[轉換摘要](/help/search-social-commerce/tracking/tracking-about.md)，並驗證轉換可如預期般歸因。 若是僅限追蹤的行銷活動，請在廣告網路的編輯器中套用產生的追蹤URL。

1. **檢閱轉換量度。**

   在[!UICONTROL Goals] > [!UICONTROL Conversions]中，[檢閱追蹤的量度，並讓必要的量度在管理檢視、報告和目標中可見](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available)。 必要時變更顯示名稱，以區分量度。

1. **（選擇性）準備產品組合最佳化。**

   確認行銷活動及其競標策略是[適用於產品組合最佳化](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)。

   [建立或選取使用適當轉換量度的目標](/help/search-social-commerce/goals/objectives/objective-about.md)。 在[!UICONTROL Manage] > [!UICONTROL Portfolios]中，[建立投資組合](/help/search-social-commerce/manage/portfolios/portfolio-create.md)或[編輯具有所需目標、支出策略和最佳化設定的現有投資組合](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)。

   [將行銷活動指派給投資組合](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)。 每個行銷活動只能屬於一個產品組合，且產品組合中的所有行銷活動必須使用相同的貨幣。

1. **驗證行銷活動資料並建立效能基準。**

   確認成本、點選和轉換資料可用於每個行銷活動。 比較轉換資料與適當的來源，包括[!DNL Google Ads]與[!DNL Microsoft Advertising] （如果適用）。 比較報表時，請使用一致的日期範圍和歸因設定。

   若為新投資組合，[啟動它](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)以收集資料並建立資料模型。 在啟用最佳化之前驗證資料和產品組合設定。

1. **（選擇性）啟動組合最佳化。**

   產品組合準備就緒時，[將其狀態變更為最佳化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)，檢閱先決條件和確認訊息。 然後搜尋、Social和Commerce會根據其設定和支援的促銷活動競標策略來最佳化產品組合。

1. **設定持續監視與報告。**

   [自訂您的資料檢視](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)、[設定自訂警示](/help/search-social-commerce/common-tasks/alerts-manage.md)以及[產生排程報告](/help/search-social-commerce/reports/management/report-manage.md)。 必要時，使用[報告範本](/help/search-social-commerce/reports/report-templates-manage.md)和[試算表摘要](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md)自動報告。

   啟動後繼續[監視和調整行銷活動和產品組合](/help/search-social-commerce/manage/manage-about.md#monitor-performance)。

>[!MORELIKETHIS]
>
>* [實作搜尋、社交和Commerce概觀](implemention-overview.md)
>* [關於管理行銷活動和產品組合](/help/search-social-commerce/manage/manage-about.md)
>* [[!DNL Google Ads] 搜尋、社交和Commerce中的轉換資料](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] 搜尋、社交和Commerce中的轉換資料](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
