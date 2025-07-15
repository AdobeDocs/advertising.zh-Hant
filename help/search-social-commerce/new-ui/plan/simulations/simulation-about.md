---
title: 關於模擬
description: 瞭解產品組合模擬。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# 關於模擬

*Beta功能*

模擬報表顯示預估邊際成本與目標值、成本、點按次數，以及不同支出（成本）層次的產品組合所預期的目標值，以及對應的每日預算或其他目標。 您可以選擇自訂檢視<!-- add link -->，以檢視其他流量量度、模擬設定，以及僅特定模擬型別（[!UICONTROL Weekly]或[!UICONTROL Custom]）。

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## 模擬型別

* **每週自動模擬：**&#x200B;每週都會使用目前的產品組合設定自動執行模擬報告。 每週自動模擬僅適用於投資組合為[最佳化或作用中](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)的期間。

  每個下載的每週模擬都包含一個活頁簿。 每個活頁簿包含20個步驟層級中每個步驟層的目標，以及目標中包含的預計成本、點按次數、加權收入（目標值）和轉換量度（根據對應目標）。 對於前20個資料列，未套用限制；對於其餘資料列，已套用限制。

* **自訂、使用者產生的模擬：**&#x200B;您可以使用目前的產品組合設定，或使用自訂產品組合設定，為單一[最佳化或作用中](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)產品組合建立自訂模擬報告，以檢視這些設定產生的結果，而不會實際變更這些結果。 例如，您可以建立自訂模擬，以檢視使用不同支出策略或學習預算<!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->的效果。 您可以在產品組合、行銷活動、競標單位和裝置層級檢視預估效能。 自訂模擬會繼承產品組合中的限制支出設定。

  >[!NOTE]
  >
  > 新的自訂模擬表單使用與舊版表單相同的設定，只是它繼承了產品組合設定的競標單位限制資訊。 您沒有選項可忽略競標單位限制，就像您在舊的自訂模擬設定頁面中所做的那樣。

  每個下載的自訂模擬都包含一個活頁簿。 每個活頁簿都包含一個工作表，供模擬的每個指定實體層級（產品組合、行銷活動、廣告群組、競標單位）使用（當該層級有資料可用時）。 當您指定裝置層級資料時，每個工作表都會包含[!UICONTROL Device]欄。 每個工作表都包含一列，內含每個適用實體的資料，以及20個步驟中每個步驟的裝置型別（例如每個促銷活動各一列）（若為報表指定此列）。 每列中的資料包含目標中所包含的根據對應目標的預測邊際成本對收入、成本、點選、加權收入（目標值）、裝置型別和轉換量度。 產品組合層次工作表也包含步驟層次的目標，而實體層次工作表則包含廣告網路、帳戶、促銷活動及（若適用）廣告群組。   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## [!UICONTROL Simulations]檢視

[!UICONTROL Simulations]檢視會列出每週模擬和自訂模擬。 管理員和其他使用者型別<!-- Verify which -->可以看到其他使用者建立的自訂模擬。 所有其他使用者只能看到他們建立的自訂模擬。

資料表包含每個模擬的進度；每一列填入的[!UICONTROL Target Midpoint]欄；以及成本/曝光數/點選數/目標值預測、實際值和準確度的欄。 您可以選擇新增其他自訂欄（包括提升度量度，例如實際目標值除以成本）。

### 可用動作 {#simulations-actions}

* [自訂檢視表](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)以包含其他量度，包括預估曝光數；實際成本、點按次數、曝光數和目標值；成本對目標的值；成本準確度、點按準確度、目標值準確度；以及預測與實際目標值與成本對目標值之間的差異（差異）。 您也可以包含大部分模擬設定和模擬型別（[!UICONTROL Custom]或[!UICONTROL Weekly]）的欄。

* [產生或重新執行單一投資組合的自訂模擬](simulation-create.md)。 您可以建立新的模擬，或是重新產生清單中現有的模擬。

* [每週下載和自訂模擬](simulation-download.md)，以ZIP檔案下載[!DNL Microsoft Excel]活頁簿。

* 使用[!UICONTROL Spend Planner]按鈕，開啟舊版支出建議工具，協助您識別產品組合間的最佳支出分配。

## 最佳實務

在下列情況下監視模擬報告：

* 在您啟動產品組合以透過對應的產品組合設定來預估可預期的效能之前，請至少使用兩週的資料。 如果模擬結果顯示效能低於您根據所包含行銷活動的歷史資料所預期的效能，請在啟動產品組合之前調查並解決問題。

* 在投資組合發生任何重大變更後（例如新增行銷活動或變更目標）。 如果您變更投資組合的模型開始日期、轉換量度的權重，或目標的點按值，則等到第二天17:00 PST之後再執行模擬，此時有更新的成本和收入模型可用。

* 定期監視轉換量度層級的效能趨勢。

>[!MORELIKETHIS]
>
>* [執行或重新執行模擬](simulation-create.md)
>* [下載模擬](simulation-download.md)
