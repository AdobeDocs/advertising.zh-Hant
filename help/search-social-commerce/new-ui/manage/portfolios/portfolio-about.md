---
title: （新UI）關於投資組合
description: 瞭解投資組合。
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# （新UI）關於投資組合

*Beta功能*

您可以使用投資組合（類似於投資組合）集體管理廣告行銷活動。 產品組合是一組廣告行銷活動或廣告集，包括其相關聯的關鍵字和廣告，針對單一業務目標最佳化。 目標可能包括多重加權轉換及單一預算或績效目標（例如每月預算或目標ROI）。 由於個別行銷活動/廣告集、關鍵字和廣告的執行方式可能彼此不同（例如，它們可能會花費不同的金額或實現不同的ROI），因此最佳化功能會使用AI驅動模型來引導整個產品組合，以集體方式實現目標。 產品組合中的所有行銷活動都會使用相同的貨幣。

有些使用者角色可以建立和設定投資組合。 根據投資組合型別，投資組合設定可能包括投資組合目標、指派的行銷活動、花費策略、任何投資組合層級競標限制，以及建模和最佳化引數。 當您準備好進行搜尋、Social和Commerce以開始最佳化產品組合時，請將狀態變更為「已最佳化」。

您可以選擇將投資組合分組到投資組合群組中，以便檢視整個群組的複合點按和收入資料。 從[舊版UI](/help/search-social-commerce/getting-started/ui-switch.md)建立投資組合群組。

視您的角色而定，您或許可以產生效能模擬，使用預測模型來識別最佳花費點與詳細的預測準確度報表。<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## 依競標策略提供最佳化支援 {#optimization-by-bid-strategy}

行銷活動符合根據行銷活動或廣告群組競標策略進行最佳化的資格。

>[!NOTE]
>
>「智慧型競標」和「自動競標」經常互換使用，但兩者並不相同。 智慧型競標僅參考使用拍賣時間競標的[!DNL Google Ads]和[!DNL Microsoft Advertising]自動競標策略，這表示廣告網路會在每次拍賣時針對轉換或轉換值最佳化。

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| 競標策略 | 智慧型競標？ | 關鍵字 — /產品群組層級競標？ | 支援等級 | 目標型別 | 競標單位 | Adobe設定了哪些專案？ | 廣告網路設定了哪些專案？ |
|---|---|---|---|---|---|---|---|
| 手動CPC （僅限[!DNL Google Ads]選項） | — | 是 | 建立、編輯、最佳化 | 具有任何權重值的單一或多屬性目標 | 關鍵字+比對型別+促銷活動 | 關鍵字競標、行銷活動預算、競標調整值 | 不適用 |
| ECPC （增強型CPC） | 是 | 是 | 建立、編輯、最佳化 | 具有任何權重值的單一或多屬性目標 | 關鍵字+比對型別+促銷活動 | 關鍵字競標、行銷活動預算 | 即時調整競標 |
| 最大化點按次數[^1] | — | — | 建立、編輯、最佳化 | 無；僅針對點按次數最佳化 | Campaign | 行銷活動預算 | 即時調整競標，以在預算內最大化點按次數 |
| 將轉換次數最大化<br> （無論是否有TCPA） | 是 | — | 建立、編輯、最佳化 | 使用1的權數的單一屬性目標 | 行銷活動或廣告群組([!DNL Google Ads])<br>僅限行銷活動([!DNL Microsoft Advertising]) | 行銷活動預算，設定<br>TCPA時的目標CPA可以是[!DNL Microsoft Advertising]中的獨立競標策略) | 即時調整競標，以最大化預算內的訂單/銷售機會，在設定目標時達成CPA目標 |
| 最大化的轉換值<br> （無論是否有TROAS） | 是 | — | 建立、編輯、最佳化 | 具有任何權重值的多屬性目標，或權重值大於1的單一屬性目標（代表貨幣值） | 行銷活動或廣告群組([!DNL Google Ads])<br>僅限行銷活動([!DNL Microsoft Advertising]) | 行銷活動預算，設定<br>TROAS時的目標ROAS可以是[!DNL Microsoft Advertising]中的獨立競標策略) | 即時調整競標，以在預算內最大化收入/利潤，在設定目標時達成ROAS目標 |
| 目標曝光比重 | — | — | 建立、編輯 | 不適用 | 不適用 | 不適用 — 無法指派至投資組合 | 即時調整競標以符合曝光分享目標 |

[^1]：廣告網路上的[!UICONTROL Maximize Clicks]競標策略設定與搜尋、社交和Commerce目標[!UICONTROL Maximize Clicks]不同。 如果競標策略是[!UICONTROL Maximize Clicks]，則您應僅將其指派給具有行銷活動層級或廣告群組層級最佳化的產品組合，而不是具有關鍵字層級最佳化的產品組合。

## Portfolio狀態 {#portfolio-status}

投資組合可以有下列狀態：

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## [!UICONTROL Portfolios]檢視

[!UICONTROL Portfolios]檢視會列出您現有的產品組合，其中包含可自訂的效能資料。 您可以[自訂檢視表](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)中的欄，並從工具列[或](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)欄標題[篩選資料以包含特定投資組合](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)。

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### 可用動作

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [建立投資組合](portfolio-create.md)

* [複製投資組合](portfolio-duplicate.md)

* [編輯投資組合設定](portfolio-edit.md)

* [使用大量工作表檔案大量編輯投資組合設定](portfolio-bulksheets.md)

* [檢視投資組合績效詳細資料](portfolio-details.md)

* [在[!UICONTROL Portfolios]檢視中下載資料](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [建立投資組合](portfolio-create.md)
>* [複製投資組合](portfolio-duplicate.md)
>* [編輯投資組合](portfolio-edit.md)
>* [從[!UICONTROL Portfolios]檢視管理資料檢視報告](portfolio-view-report.md)
