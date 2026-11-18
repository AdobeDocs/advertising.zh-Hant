---
title: （全新UI） Advertising深入分析
description: 瞭解如何設定和檢視Advertising insight儀表板的模型準確度、效能、模擬、預算上限和轉換。
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 54920f5e0e08c1bf6f960b4d96aa4161dfa11143
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# （全新UI） Advertising深入分析

Advertising深入分析提供可操作的視覺資料，協助您評估產品組合績效、找出最佳化問題並比較轉換資料。 每個insight都會隨選產生，並顯示為熒幕上的控制面板。

**[!UICONTROL Reports]>[!UICONTROL Insights]**&#x200B;檢視會在&#x200B;**[!UICONTROL Dashboards]**&#x200B;下顯示可用的深入分析。 頁面標題為&#x200B;**[!UICONTROL Advertising Insights]**。

>[!NOTE]
>
>本頁說明Beta版新使用者介面中的insight控制面板。 可用性取決於您的存取權以及所選廣告商可用的深入分析。 [舊版Advertising Insights](/help/search-social-commerce/advertising-insights/insight-about.md)針對產生的檔案包含一組不同的分析和程式。

## 深入分析型別 {#insight-types}

| insight | 說明 |
| --- | --- |
| [!UICONTROL Model Accuracy] | 識別Search、Social和Commerce預測產品組合成本和收入的程度。 您可以在產品組合、廣告網路和促銷活動層級檢閱模型準確性。 |
| [!UICONTROL Performance Insights] | 比較最佳化狀態變更、目標變更或指定日期前後的投資組合績效。 控制面板包括績效摘要、影響最佳化的變更稽核、行銷活動比較、趨勢和目標值分析。 |
| [!UICONTROL Portfolio Simulation Analysis] | 比較現有的自訂模擬與實際效能。 您可以檢閱產品組合和行銷活動資料、分析模擬準確性，以及探索不同目標支出等級的預估成效。 |
| [!UICONTROL Campaign Budget Cap Analysis] | 指出產品組合的支出是否受限於行銷活動預算上限。 儀表板包括限定支出、受影響的行銷活動、預估的曝光數損失、每日和一週中的某天趨勢，以及產品組合設定的建議。 |
| [!UICONTROL Modeled Conversions] | 比較Adobe轉換值與廣告網路報告的值，包括模型資料。 您可以分析帳戶、產品組合或行銷活動，並將Adobe測量和Adobe測量及模型化的值與發佈者報告的值比較。 |
| [!UICONTROL Delayed Revenue Analysis] | 測量轉換延遲（從廣告點按或閱覽到後續轉換的經過時間），並顯示其對目標值、投資報酬率(ROI)和模型準確性的影響。 該分析僅適用於具有點按式或瀏覽式收入歸因的產品組合。 |

## 產生insight {#insight-generate}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Insights]**。

1. 按一下您要產生的insight。

1. 在&#x200B;**[!UICONTROL Configure]**&#x200B;面板中，指定[insight設定](#insight-settings)。

1. 按一下&#x200B;**[!UICONTROL Generate Insight]**。

   配置面板關閉，儀表板顯示分析。

1. 檢閱[insight結果](#insight-results)。

若要變更設定，請按一下&#x200B;**[!UICONTROL Configure]**、變更值，然後再次按一下&#x200B;**[!UICONTROL Generate Insight]**。 若要返回insight清單，請按一下階層連結中的&#x200B;**[!UICONTROL Analysis List]**。

## insight設定 {#insight-settings}

### 模型精確度 {#model-accuracy-settings}

* **[!UICONTROL Portfolios]：** Select one投資組合。

* **[!UICONTROL Choose Revenue Type]：** Select **[!UICONTROL Actual Revenue]** （預設）或&#x200B;**[!UICONTROL Delayed Revenue]**。

* **[!UICONTROL Date Range]：** Select要分析的日期。 請參閱[日期範圍設定](#date-range-settings)。

### 效能分析 {#performance-insights-settings}

* **[!UICONTROL Portfolios]：** Select one投資組合。

* **[!UICONTROL Revenue Type]：** Select **[!UICONTROL Actual Revenue]** （預設）或&#x200B;**[!UICONTROL Delayed Revenue]**。

* **事件日期：** Select要比較績效的日期型別：

  * **[!UICONTROL Optimization Status Change (last 90 days)]** （預設值）： Select投資組合的可用最佳化狀態變更日期。

  * **[!UICONTROL Objective Change Date (last 90 days)]：** Select是投資組合可用的目標變更日期。

  * **[!UICONTROL Specific Date]：**&#x200B;使用日期選擇器指定日期。

  在設定比較期間之前，先設定事件日期的Select。 如果選取的投資組合沒有可用的事件日期，您可以使用&#x200B;**[!UICONTROL Specific Date]**。

* **[!UICONTROL Pre Days]：**&#x200B;指定事件日期之前的期間：

  * Select **[!UICONTROL 7]** （預設）、**[!UICONTROL 14]**&#x200B;或&#x200B;**[!UICONTROL 30]**。

  * Select **[!UICONTROL Pre Start Date]**&#x200B;並指定&#x200B;**[!UICONTROL Custom Pre Date]**。

  * Select **[!UICONTROL Custom Pre Days]**&#x200B;並輸入正數天數。

* **[!UICONTROL Post Days]：**&#x200B;指定事件日期之後的期間：

  * Select **[!UICONTROL 7]** （預設）、**[!UICONTROL 14]**&#x200B;或&#x200B;**[!UICONTROL 30]**。

  * Select **[!UICONTROL Post End Date]**&#x200B;並指定&#x200B;**[!UICONTROL Custom Post Date]**。

  * Select **[!UICONTROL Custom Post Days]**&#x200B;並輸入正數天數。

  兩個比較期間均不包含事件日期本身。

* **[!UICONTROL Date Exclusion]：** （選用）從分析中排除日期：

  1. 按一下&#x200B;**[!UICONTROL Select Dates]**。

  1. Select要排除的日期：

     * 按一下個別日期，加以選取或取消選取。

     * 按一下以選取範圍時按住&#x200B;**[!UICONTROL Shift]**。

     * 若要移除所有排除專案，請按一下&#x200B;**[!UICONTROL Clear All]**。

  1. 完成後，請按一下「**[!UICONTROL Done]**」。

### Portfolio模擬分析 {#simulation-settings}

* **[!UICONTROL Portfolios]：** Select one產品組合具有現有的自訂模擬。

* **[!UICONTROL Simulation Date]：** Select要分析的模擬日期。 如果該日期有多個可用的模擬，請依名稱選取模擬。

  如果沒有可用的自訂模擬，請在使用此insight之前[產生自訂模擬](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md)。

* **[!UICONTROL Actual Days]：** Select **[!UICONTROL 7]** （預設）、**[!UICONTROL 14]**&#x200B;或&#x200B;**[!UICONTROL 30]**&#x200B;天的實際效能資料。 若要指定其他數字，請選取&#x200B;**[!UICONTROL Enter Actual Days]**&#x200B;並輸入1-90的值。

* **[!UICONTROL Type]：**&#x200B;轉換歸因的Select **[!UICONTROL Transaction Date]** （預設）或&#x200B;**[!UICONTROL Click Date]**。

### 行銷活動預算上限分析 {#budget-cap-settings}

* **[!UICONTROL Portfolio]：** Select one投資組合。

* **[!UICONTROL Date Range]：** Select要分析的日期。 請參閱[日期範圍設定](#date-range-settings)。

### 模型化轉換 {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]：** Select **[!UICONTROL Account]**、**[!UICONTROL Portfolio]** （預設）或&#x200B;**[!UICONTROL Campaign]**。

* **[!UICONTROL Accounts]**、**[!UICONTROL Portfolios]**&#x200B;或&#x200B;**[!UICONTROL Campaigns]：** Select分析層級的適用實體。 您可以選取多個圖元。

* **[!UICONTROL Date Range]：** Select要分析的日期。 請參閱[日期範圍設定](#date-range-settings)。

* **[!UICONTROL Adobe Conversion]：** Select要比較的Adobe轉換屬性。

* **[!UICONTROL Publisher Conversion]：** Select要比較的發行者轉換屬性。

  可用的轉換屬性取決於分析層級、選取的圖元和日期範圍。 比較需要兩個轉換屬性。

### 延遲收入分析 {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]：** Select one產品組合具有點按式或瀏覽式收入歸因。

* **[!UICONTROL Date Range]：** Select要分析的日期。 請參閱[日期範圍設定](#date-range-settings)。

### 日期範圍設定 {#date-range-settings}

針對具有&#x200B;**[!UICONTROL Date Range]**&#x200B;設定的深入分析，請選取&#x200B;**[!UICONTROL Last 7 days]** （預設）、**[!UICONTROL Last 14 days]**&#x200B;或&#x200B;**[!UICONTROL Last 30 days]**。

若要指定其他句號，請選取&#x200B;**[!UICONTROL Custom Date]**&#x200B;並輸入&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**。 您可以選取從目前日期到最近90天內的日期。

## 檢視insight結果 {#insight-results}

### 模型精確度 {#model-accuracy-results}

檢閱投資組合詳細資訊，並使用下列標籤：

* **[!UICONTROL Portfolio]：**&#x200B;檢閱投資組合層級的模型正確性和預算比較。

* **[!UICONTROL Ad Network]：**&#x200B;依廣告網路檢閱模型正確性和預算比較。

* **[!UICONTROL Campaigns]：**&#x200B;檢閱行銷活動層級模型的正確性以及目標與實際績效的比較。

* **[!UICONTROL Playground Beta]：**&#x200B;比較多個行銷活動的模型準確度。

若要取得行銷活動正確性圖表，請選取&#x200B;**[!UICONTROL Comparison Options]**&#x200B;和&#x200B;**[!UICONTROL Campaign]**。 在&#x200B;**[!UICONTROL Playground Beta]**&#x200B;中，您可以選取多個行銷活動。 按一下&#x200B;**[!UICONTROL Table View]**&#x200B;在圖表與其基礎資料之間切換。

### 效能分析 {#performance-insights-results}

儀表板會顯示&#x200B;**[!UICONTROL Pre Period]**&#x200B;和&#x200B;**[!UICONTROL Post Period]**、兩個時段的彙總績效量度，以及投資組合詳細資訊。

**[!UICONTROL Audit Trail]**&#x200B;總結了影響最佳化的因素變更，包括產品組合預算、支出策略、最低行銷活動支出和支出限制倍數。 當變更有詳細資料可用時，按一下&#x200B;**[!UICONTROL View Details]**&#x200B;進行檢查。

使用&#x200B;**[!UICONTROL Comparative Overview]**、**[!UICONTROL Campaigns Comparison]**、**[!UICONTROL Trends & Patterns]**、**[!UICONTROL Deep Analysis]**&#x200B;和&#x200B;**[!UICONTROL Objective Value And Analysis]**&#x200B;索引標籤來探索比較。

### Portfolio模擬分析 {#simulation-results}

複查模擬詳細資訊，並使用下列頁標：

* **[!UICONTROL Portfolio]：**&#x200B;檢閱投資組合層級的模擬資料。 在此標籤中：

  * **[!UICONTROL Simulation Data]**&#x200B;顯示模擬量度和目標支出績效。

  * **[!UICONTROL Simulation Vs Actual]**&#x200B;比較模擬效能和實際效能。

  * **[!UICONTROL Try New Target]**&#x200B;可讓您在&#x200B;**[!UICONTROL Explore Target Spend]**&#x200B;中輸入目標支出，以檢視預估的點按次數、成本和收入。 這是對預估績效的分析；它不會改變產品組合的支出目標。

* **[!UICONTROL Campaigns]：**&#x200B;檢閱行銷活動層級的模擬比較。

* **[!UICONTROL Accuracy Analysis]：**&#x200B;檢閱模擬準確性。

### 行銷活動預算上限分析 {#budget-cap-results}

檢閱投資組合詳細資料和摘要量度：

* **[!UICONTROL Total Capped Spend]：**&#x200B;達到行銷活動預算時的日支出百分比。

* **[!UICONTROL Capped Campaigns]：**&#x200B;至少達到其預算一次的行銷活動數。

* **[!UICONTROL Est. Lost Impressions]：**&#x200B;預估曝光因預算限制而遺失。

* **[!UICONTROL Peak Capping Day]：**&#x200B;一週中支出上限最多的日子。

**[!UICONTROL Spend on Capped Campaigns by Day]**&#x200B;和&#x200B;**[!UICONTROL Capped Spend by Weekday]**&#x200B;圖表顯示上限趨勢。 請檢閱&#x200B;**[!UICONTROL Capped Campaign Performance]**&#x200B;以取得行銷活動詳細資料，並檢閱&#x200B;**[!UICONTROL Portfolio Settings Recommendations]**&#x200B;以取得建議的設定變更。

### 模型化轉換 {#modeled-conversions-results}

檢閱所選實體和日期範圍的下清單格：

* **[!UICONTROL Adobe Measured vs Publisher Conversions]：**&#x200B;將Adobe直接測量的轉換值與發佈者報告的值（包含測量與模型化的資料）進行比較。

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]：**&#x200B;比較Adobe測量與模型化的轉換值與發佈者報告的值。

這兩個表格都包含實體名稱和ID、Adobe值、發佈者報告的值、絕對差異和百分比差異。

如果沒有可用的資料，請確認您已選取轉換屬性，且選取的實體和日期範圍均有資料。

### 延遲收入分析 {#delayed-revenue-results}

**[!UICONTROL Key Insights Summary]**&#x200B;顯示預期的加權收入（現在稱為「[目標值](/help/search-social-commerce/glossary.md#o-p)」）、ROI和模型正確性資訊。

**[!UICONTROL Conversion Lag Breakdown by Revenue Property]**&#x200B;區段顯示每個收入屬性在第0天以及第3、7、14和28天實現的轉換百分比。

在&#x200B;**[!UICONTROL Performance Over Time]**&#x200B;中，選取&#x200B;**[!UICONTROL Objective Value]**、**[!UICONTROL ROI]**&#x200B;或&#x200B;**[!UICONTROL Model Accuracy]**&#x200B;以比較點按日期、交易日期和預期績效。 按一下&#x200B;**[!UICONTROL Table View]**&#x200B;在圖表與其基礎資料之間切換。

在&#x200B;**[!UICONTROL Metrics Definitions]**&#x200B;中，按一下&#x200B;**[!UICONTROL Show]**&#x200B;以取得分析中所使用日期和量度的說明，或按一下&#x200B;**[!UICONTROL Hide]**&#x200B;以摺疊它們。

如果分析不適用，請選取具有點按式或瀏覽式收入歸因的投資組合。 如果沒有可用的資料，請確認資料存在於選取的投資組合和日期範圍。
