---
title: 關於管理行銷活動和產品組合
description: 瞭解廣告網路帳戶、行銷活動、追蹤和產品組合最佳化如何搭配運作，以及如何監控和改善效能。
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# 關於管理行銷活動和產品組合

*Beta功能*

搜尋、Social和Commerce將行銷活動管理、效能報告和產品組合最佳化整合到一個介面中。 您可以根據廣告網路和行銷活動型別，同步行銷活動資料、建立和編輯行銷活動元件、追蹤轉換，以及最佳化出價、預算或競標策略目標。 如需每個廣告網路可用的功能，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

[!UICONTROL Manage]功能表可讓您存取您的帳戶、行銷活動、廣告群組、廣告、關鍵字、產品群組和產品組合。 您的許可權會決定可用的檢視和動作。 如需完整的功能表組織，請參閱[使用者介面的組織方式](/help/search-social-commerce/getting-started/user-interface.md)。

## 帳戶、行銷活動和產品組合如何組合

* **廣告網路帳戶**&#x200B;將您的廣告商資料連結至Search、Social和Commerce。 [帳戶型別](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)包含透過API連線同步處理的帳戶、您上傳資料的帳戶，以及僅以範本追蹤的帳戶。 帳戶型別會決定您是否可以同步資料、管理行銷活動，或使用產品組合最佳化。

* **行銷活動**&#x200B;包含用來傳遞廣告的廣告和其他元件。 對於支援的行銷活動型別，您可以從[!UICONTROL Manage]檢視[建立和管理行銷活動](/help/search-social-commerce/manage/campaigns/campaign-manage.md)及其元件。 您也可以使用[Bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md)進行支援的大量作業。

* **產品組合**&#x200B;將符合資格的行銷活動分組，以針對共同的業務目標及預算或績效目標進行最佳化。 行銷活動只能屬於一個產品組合，且產品組合中的所有行銷活動必須使用相同的貨幣。 請參閱&quot;[關於投資組合](/help/search-social-commerce/manage/portfolios/portfolio-about.md)&quot;。

Portfolio指派為選用。 您可以追蹤並報告行銷活動，而無需將行銷活動指派給產品組合。 並非所有廣告網路、行銷活動型別或競標策略都支援產品組合最佳化。

## 同步化行銷活動資料

對於透過API連線的帳戶，搜尋、Social和Commerce會從廣告網路擷取支援的促銷活動結構和績效資料。 您對「搜尋」、「社交」和「Commerce」中支援的行銷活動元件所進行的變更會傳送至廣告網路。

必要時，您可以[要求手動同步](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md)。 如果帳戶停止同步處理，請檢閱其[驗證與存取狀態](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status)。

資料上傳帳戶和僅限追蹤的帳戶不會與廣告網路同步。 遵循[帳戶型別](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)的工作流程，以提供行銷活動和績效資料。

## 設定追蹤和最佳化

[追蹤](/help/search-social-commerce/tracking/tracking-about.md)會將行銷活動連結至對您的業務重要的轉換。 根據您的實作，轉換資料可能來自Adobe Advertising標籤、Adobe Analytics整合、廣告網路追蹤或資料摘要。 根據實作需要設定點選追蹤和轉換追蹤，並在使用資料進行最佳化前驗證資料。

在[!UICONTROL Goals] > [!UICONTROL Conversions]中，您可以[檢閱為廣告商追蹤的轉換量度，並控制其可見度](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md)。 在您的[目標](/help/search-social-commerce/goals/objectives/objective-about.md)中使用適當的量度。

若要啟用產品組合最佳化，請[建立產品組合](/help/search-social-commerce/manage/portfolios/portfolio-create.md)、指派目標且合格的行銷活動，以及設定其支出與最佳化設定。 有效的產品組合可收集績效資料並建立模型。 當資料與設定就緒時，[將投資組合狀態變更為最佳化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)以開始最佳化。 執行的動作取決於投資組合型別和[行銷活動競標策略](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)。

如需詳細的設定順序，請參閱&quot;[設定廣告網路帳戶和行銷活動](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)&quot;。

## 監視行銷活動和產品組合績效 {#monitor-performance}

客戶團隊、代理或廣告商負責根據服務合約條款監控績效及進行調整。 日常：

* 在[!UICONTROL Manage]檢視中檢閱行銷活動和帳戶績效。 [自訂欄、篩選器和日期範圍](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)，以聚焦於重要的量度和實體。

* 使用[!UICONTROL Dashboard] > [!UICONTROL Overview]來[監視投資組合趨勢和效能變化](/help/search-social-commerce/dashboard/dashboard-overview.md)。

* 檢閱[自訂警示](/help/search-social-commerce/common-tasks/alerts-manage.md)是否有需要調查的情況。

* [產生行銷活動、關鍵字、廣告和組合績效的報告](/help/search-social-commerce/reports/management/report-manage.md)。 針對產品組合，[檢閱效能詳細資料](/help/search-social-commerce/manage/portfolios/portfolio-details.md)，包括實際效能和模型準確性。

* 使用[模擬](/help/search-social-commerce/plan/simulations/simulation-about.md) （如果可用）來評估不同花費等級的預測效果。

* 調查您報告的轉換和來源資料之間的差異。 請參閱相關連結中[!DNL Google Ads]與[!DNL Microsoft Advertising]轉換資料的指引。

## 調整行銷活動和產品組合

根據效能和業務目標的變更，您可能需要：

* 編輯行銷活動設定、建立或暫停行銷活動元件、調整關鍵字集或測試不同的廣告。 可用動作取決於廣告網路和行銷活動型別。

* 使用相關的管理檢視和報表，檢閱地理、對象和位置鎖定目標。

* [當行銷活動應該使用不同的投資組合最佳化時，請變更行銷活動指派](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)。 將行銷活動指派給另一個產品組合，會將其從先前的產品組合中移除。

* [編輯產品組合設定](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)，包括目標、支出策略、限制或最佳化控制項，如您的產品設定檔所允許。

* 檢閱調查效能變更時的[變更記錄](/help/search-social-commerce/reports/history-logs.md)。

>[!MORELIKETHIS]
>
>* [設定廣告網路帳戶與行銷活動](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)
>* [[!DNL Google Ads] 搜尋、社交和Commerce中的轉換資料](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] 搜尋、社交和Commerce中的轉換資料](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
