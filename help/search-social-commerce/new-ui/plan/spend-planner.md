---
title: 使用[!UICONTROL Spend Planner]
description: 瞭解如何產生、下載和套用產品組合預算建議，以幫助您在產品組合中達成最佳的支出分配。
feature: Search Optimization, Search Portfolios
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
TQID: https://experienceleague.adobe.com/8BAQij06MRhxYoCoFNjhHsgC4o38lQnj9vpmTzYyqGg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4126848d8192a1d4a23406dfeb5b643788670689
workflow-type: tm+mt
source-wordcount: 801
ht-degree: 0%

---

# 使用[!UICONTROL Spend Planner]

[!UICONTROL Spend Planner] （在舊版使用者介面中稱為「[!UICONTROL Spend Recommendation Tool]」）會識別具有相同目標與貨幣之最佳化與使用中投資組合的最佳支出分配，因此您可以最大化投資組合集的收入或目標目標。

檢視具有每日預算之產品組合的支出建議報告時，您可以將任何產品組合的預算變更為建議預算。

## [!UICONTROL Spend Planner]報表中的資料

針對具有目標[!UICONTROL Maximize Clicks]的投資組合，報告包含支出建議和點選預測。 對於所有其他目標，此報表包含支出建議及收入預測。

支出建議報表包含下列資料：

* 散佈線圖顯示當個別支出目標設為最佳化時，投資組合在指定總成本下可達到的預測最大收入或點按次數。 每個收入點或點按點的預測成本都會計算在內。

* 兩個環圈圖，顯示支出與預期收入，或按投資組合的點按分佈1\)目前支出目標及2\)提議支出目標。

* 每個產品組合的長條圖，顯示當您維護所有選定產品組合或建議的總支出目標的目前總每日支出目標時，建議的每日支出（成本）和預測的收入分佈或點按分佈。 您可以選擇將建議的支出目標套用至選取的投資組合，這會影響下一個競標執行週期的競標。

## 可用動作

* 從[新使用者介面](#spend-recommendations-generate)或[舊使用者介面](#spend-recommendations-generate-legacy)產生[!UICONTROL Spend Planner]報告

* [套用支出建議](#spend-recommendations-apply)至對應的投資組合。

* [開啟或儲存支出建議報表資料至檔案](#spend-recommendations-download)

## （新UI）產生[!UICONTROL Spend Planner]報表 {#spend-recommendations-generate}

1. 執行下列任一項作業：

   * 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Spend Planner]**。

   * 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。 在資料表上方的工具列中，按一下![支出規劃工具](/help/search-social-commerce/assets/spend-planner-icon.png "支出規劃工具")。

   [!UICONTROL Spend Recommendation]工具會在舊版使用者介面中開啟。

1. 使用所選產品組合的目前合併預算檢視資料：

   1. 選取投資組合目標。

   1. 選取貨幣。

   1. （選用）選取產品組合支出策略以進一步篩選產品組合清單。

   1. 選取每個要包含的投資組合旁的核取方塊。 若要選取所有投資組合，請選取[!UICONTROL Portfolios]旁的核取方塊。

      只會列出具有所選引數的已最佳化和作用中產品組合。

   1. 按一下&#x200B;**[!UICONTROL Update]**。

   1. （選擇性）若要檢視圖表上任一點的成本和收入，請將游標停留在點上。

1. （選用）若要檢視使用不同總支出目標的每個產品組合的建議每日支出目標和預期收入，請在[!UICONTROL Total Spend Target]欄位中輸入所有產品組合的建議每日總支出目標。 然後按&#x200B;**Enter**&#x200B;鍵。

   支出建議工具會使用每週模擬的資料，因此建議支出總計會與您提議的支出目標最相符，並提供理想的支出組合。

<!--

New UI; validate post-Update steps once I get it to generate a report:

## Generate a spend recommendation report {#spend-recommendations-generate}

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Spend Planner]**.

1. View data using the current, combined budgets for the selected portfolios:

   1. Click **[!UICONTROL Select Objective]**.

   1. Select the portfolio objective.

   1. Select the currency.

   1. (Optional) Select a portfolio spend strategy to further filter the portfolios list.

   1. Select the check box next to each portfolio to include.

      Only optimized and active portfolios with the selected parameters are listed.

   1. Click **[!UICONTROL Update]**.

   1. (Optional) To see the cost and revenue for any point on the chart, hold the cursor over the point.

1. (Optional) To download the proposed allocation and expected revenue per portfolio, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download") next to [!UICONTROL Portfolio Allocation] in the right column.

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

1. (Optional) To view the recommended daily spend and expected revenue for each of the portfolios using a different total spend target, enter a proposed total daily spend target across all portfolios in the [!UICONTROL Total Spend Target] field. Then press the **Enter** key.

   The spend recommendation tool uses data from weekly simulations, so the total recommended spend is the closest match to your proposed spend target with the ideal spend mix.

-->

## （舊版UI）從[!UICONTROL Optimization] > [!UICONTROL Spend Recommendation]檢視產生[!UICONTROL Spend Recommendation]報告 {#spend-recommendations-generate-legacy}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]**。

1. 使用所選產品組合的目前合併預算檢視資料：

   1. 選取投資組合目標。

   1. 選取貨幣。

   1. （選用）選取產品組合支出策略以進一步篩選產品組合清單。

   1. 選取每個要包含的投資組合旁的核取方塊。 若要選取所有投資組合，請選取[!UICONTROL Portfolios]旁的核取方塊。

      只會列出具有所選引數的已最佳化和作用中產品組合。

   1. 按一下&#x200B;**[!UICONTROL Update]**。

   1. （選擇性）若要檢視圖表上任一點的成本和收入，請將游標停留在點上。

1. （選用）若要檢視使用新總支出目標的每個產品組合的建議每日支出和預測收入，請在[!UICONTROL Total Spend Target]欄位中輸入所有產品組合的建議每日支出總目標。 然後按&#x200B;**Enter**&#x200B;鍵。

   支出建議工具會使用每週模擬的資料，因此建議支出總計會與您提議的支出目標最相符，並提供理想的支出組合。

<!--
## (New UI) Apply spend recommendations {#spend-recommendations-apply}

*Portfolios with daily budgets only*

>[!NOTE]
>
>* If the applied changes will increase or decrease the spend target of any portfolio by more than 20%, you must approve the change.
>* When the spend target for a portfolio changes by more than 20%, Search, Social, & Commerce takes up to 3-4 days to adjust its models and achieve the new target.

1. [Generate a spend recommendation report](#spend-recommendations-generate) for one or more portfolios with daily budgets.

1. Select the check box next to each portfolio for which you want to apply the recommended spend target. To select all portfolios, select the check box next to **[!UICONTROL Select All Recommendations]**.

1. Click **[!UICONTROL Apply Selected Recommendations]**.

1. (If any of the budgets will change by more than 20%) In the confirmation message, click **[!UICONTROL Confirm]** to approve the changes.

-->

## &#x200B;<!--(Legacy UI) -->套用支出建議 {#spend-recommendations-apply-legacy}

*僅含每日預算的產品組合*

>[!NOTE]
>
>* 如果套用的變更將導致任何產品組合的支出目標增加或減少超過20%，則您必須核准變更。
>* 當產品組合的支出目標變更超過20%時，搜尋、社交和Commerce最多需要3-4天才能調整其模型並達成新目標。

1. [針對一或多個具有每日預算的產品組合產生支出建議報告](#spend-recommendations-generate-legacy)。

1. 選取您要套用建議支出目標之每個投資組合旁的核取方塊。 若要選取所有投資組合，請選取&#x200B;**[!UICONTROL Select All Recommendations]**&#x200B;旁的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Apply Selected Recommendations]**。

1. （如果任何預算變更超過20%）在確認訊息中，按一下&#x200B;**[!UICONTROL Yes]**&#x200B;以核准變更。

<!--

## (New UI) Open or save data as a [!DNL Microsoft Excel] workbook file {#spend-recommendations-download}

You can open or save data from either a) the line chart showing cost points and the expected revenue for each cost and b) the donut charts of the current and proposed media mix. [This seems to be identical to the Portfolio Allocation report -- how should these be different?]

1. [Generate a spend recommendation report](#spend-recommendations-generate) for selected portfolios.

1. Above the report, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download").

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

-->

## &#x200B;<!--(Legacy UI) -->開啟資料或將資料儲存為[!DNL Microsoft Excel]活頁簿檔案 {#spend-recommendations-download-legacy}

1. 產生所選投資組合的支出建議報告。

1. 在報告的右上角，按一下![下載](/help/search-social-commerce/assets/download-spend-recommendation.png "下載")。

   依照瀏覽器的正常程式開啟或儲存檔案。 如需詳細資訊，請參閱瀏覽器的線上說明。
