---
title: 實施搜尋、社交和Commerce概觀
description: 瞭解啟動和維護投資組合的一般工作流程。
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%
---
# 實施搜尋、社交和Commerce概觀

[!DNL Adobe]或其其中一個附屬代理與每個廣告商合作，以推出其線上廣告產品組合併追蹤任何其他廣告行銷活動。 初次啟動後，其他持續性工作可確保繼續達成廣告商的目標。

以下是實作及使用「搜尋」、「社交」和「Commerce」的一般工作流程。

## 初始啟動

[!DNL Adobe]和/或您的機構與您合作時，請完成下列工作：

1. 評估高階業務目標並設計策略以達成目標：

   1. 識別您的業務模式和行銷目標。

   1. 識別您的轉換追蹤需求

   1. 分析您現有的線上廣告帳戶結構。

   1. 識別產品組合最佳化和報告的量度。

1. （管理員或帳戶管理員使用者）設定管理帳戶：

   1. 設定廣告商的帳戶。 如果代理商管理廣告商的資料，則廣告商的帳戶必須與代理商帳戶相關聯。

   1. （如有必要）為廣告商建立使用者帳戶，以檢視和管理其行銷活動資料並產生報表。

   與您的管理員合作，使用Adobe Admin Console和適當的產品設定檔來設定存取權。 請參閱[搜尋、社交和Commerce的使用者管理](/help/search-social-commerce/user-administration.md)。

1. 同步處理或建立每個廣告網路帳戶的行銷活動：

   * 針對API連線的帳戶，[在[!UICONTROL Manage] > [!UICONTROL Accounts]中建立帳戶詳細資料](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account)、完成網路特定驗證、設定追蹤選項，以及啟用帳戶。

   * 對於沒有API支援的帳戶，請依照適用的[資料上傳](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md)或[僅限追蹤的帳戶](/help/search-social-commerce/manage/accounts/template-account-manage.md)工作流程進行。 這些帳戶不會與廣告網路同步，或支援組合最佳化。

   * 如果帳戶尚未包含行銷活動資料，請從Search、Social和Commerce內或廣告網路內新增行銷活動、廣告群組、關鍵字、廣告和版位。

     如需詳細的設定檢查清單，請參閱&quot;[設定廣告網路帳戶與行銷活動](campaign-implementation-overview.md)&quot;。 對於支援的行銷活動型別，請使用[!UICONTROL Manage] > [!UICONTROL Campaigns]來[建立和管理行銷活動](/help/search-social-commerce/manage/campaigns/campaign-manage.md)。

1. 設定您希望Adobe Advertising追蹤轉換之所有廣告的追蹤：

   1. （如有必要） [透過產生及上傳點選追蹤URL，為廣告、關鍵字、[!DNL Google Ads]位置及[!DNL Google Ads]副檔名設定點選追蹤](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)。

      使用Adobe Advertising畫素式轉換追蹤服務的廣告商點選追蹤URL包含重新導向至[!DNL Adobe]伺服器。

   1. [設定轉換追蹤](/help/search-social-commerce/tracking/conversion-tracking-about.md)。 根據實作，這可能需要將轉換追蹤標籤新增到適當的網頁，和/或為您使用自己的方法收集的轉換資料設定每日摘要拖放功能。 您可以從[!UICONTROL Goals] > [!UICONTROL Conversions] [產生Adobe Advertising轉換追蹤標籤](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md)。

      如需詳細資訊，請參閱[關於搜尋、社交和Commerce的追蹤](/help/search-social-commerce/tracking/tracking-about.md)。

1. 設定與其他產品的整合：

   1. （使用Adobe Analytics和/或Adobe Audience Manager的廣告商）設定各種帳戶之間的整合，讓Adobe Advertising可以與他們交換資料。

      請參閱「[與CX Enterprise](/help/integrations/home.md)的整合」指南。

   1. （具有[!DNL Google Analytics]的廣告商）同步[!DNL Google Analytics]帳戶、屬性和檢視組合的轉換量度，以進行最佳化和報告。

      此設定使用舊版使用者介面。 請參閱「[關於同步 [!DNL Google Analytics] 轉換量度](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)」，並在必要時切換至舊版介面[&#128279;](ui-switch.md)。

1. （選用）設定和啟動產品組合：

   1. 在[!UICONTROL Goals] > [!UICONTROL Conversions]中，[檢閱轉換量度，並將必要的量度設定為可見](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available)。 在[!UICONTROL Goals] > [!UICONTROL Objectives]中，[建立或選取最佳化目標](/help/search-social-commerce/goals/objectives/objective-about.md)。

   1. 在[!UICONTROL Manage] > [!UICONTROL Portfolios]中，[&#128279;](/help/search-social-commerce/manage/portfolios/portfolio-create.md)使用適當的[合格行銷活動](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)，建立已設定成符合您目標與業務目標的產品組合。 [啟動投資組合](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)以收集資料並建立資料模型。 接下來，實作團隊會收集並驗證點按和收入資料至少14天，並驗證產品組合設定。

      >[!NOTE]
      >
      >搜尋、Social和Commerce仍會追蹤和報告未指派給產品組合的促銷活動的資料，但不會為他們提供最佳化。

   1. 在足夠的資料可用來建立基準後，團隊可以[將產品組合狀態變更為最佳化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) — 讓Search、Social和Commerce根據產品組合型別和行銷活動競標策略，將產品組合的競標、預算和/或競標策略目標最佳化。

   如需最佳化支援和產品組合狀態，請參閱&quot;[關於產品組合](/help/search-social-commerce/manage/portfolios/portfolio-about.md)&quot;。

1. 監控您的產品組合績效：

   1. 使用[!UICONTROL Dashboard] > [!UICONTROL Overview]來[檢閱投資組合趨勢](/help/search-social-commerce/dashboard/dashboard-overview.md)，並[檢視投資組合績效詳細資料](/help/search-social-commerce/manage/portfolios/portfolio-details.md)以調查結果和模型準確性。

   1. [設定自訂警報](/help/search-social-commerce/common-tasks/alerts-manage.md)和[產生自訂報告](/help/search-social-commerce/reports/management/report-manage.md)以進行效能監視。 必要時，使用[報告範本](/help/search-social-commerce/reports/report-templates-manage.md)和[試算表摘要](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md)自動報告。

   如需詳細資訊，請參閱&quot;[監視行銷活動和產品組合績效](/help/search-social-commerce/manage/manage-about.md#monitor-performance)&quot;。

1. （選擇性）設定您的[效能資料檢視](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)，以顯示您要檢視的資料。

## 進行中的任務

初次啟動後，需要下列持續性工作。 根據您的參與條款，[!DNL Adobe]、附屬機構或廣告商會執行下列工作：

* 檢視警報、每個產品組合及其元件行銷活動的效能資料、可自訂的報表，以及（某些角色）模擬，繼續監視和分析每個產品組合的效能。

* 視需要，根據產品組合的實際和預測績效以及成長機會，調整用於管理產品組合的各種策略和設定：

  * 調整投資組合預算、目標和其他設定。

  * 調整帳戶/行銷活動結構，以配合行銷策略的變更。

  * 新增/暫停/刪除行銷活動元件。 這可能包括根據搜尋字詞分析擴展關鍵字集，以及測試廣告文案和登陸頁面。

  * 根據進階效能報告更新地理和網站目標定位策略。

  * （選用）將競標限制新增至個別搜尋關鍵字或廣告群組、行銷活動或產品組合中的所有關鍵字。

  * 新增投資組合。

如需監視行銷活動和產品組合以及調整其設定的指示，請參閱&quot;[關於管理行銷活動和產品組合](/help/search-social-commerce/manage/manage-about.md)&quot;和&quot;[編輯產品組合詳細資料](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)&quot;。
