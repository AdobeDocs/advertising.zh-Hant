---
title: 關於深入分析
description: 瞭解視覺效果的效能深入分析。
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
source-git-commit: a098e99f26a4e7d472d4a391d2cd465fc8d4255b
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---

# 關於深入分析

*Beta功能*

透過視覺效果的高層級效能深入分析，為您提供有效最佳化行銷活動並發現提升效能的新機會所需的資訊。 您可以檢視指定廣告商的各個促銷活動的資料，或向下展開至較低層級。

使用效能分析來：

* 追蹤策略規劃與明智決策的長期趨勢。

* 找出取得更佳結果的機會。

* 減少從取得原始資料到取得可操作的深入分析所花費的時間，進而提高效率。

您可以將標籤的所有視覺效果匯出至PDF檔案，或下載特定insight的資料，而不使用Microsoft Excel試算表(XLSX)格式的視覺效果。

您也可以[變更日期範圍、設定檢視並儲存自訂檢視](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"}，就像促銷活動管理檢視一樣。

## 深入分析型別

### [!UICONTROL Home]索引標籤

[!UICONTROL Home]索引標籤會針對廣告商的所有行銷活動，提供關鍵標準、績效和可見度量度。 依預設，會顯示特定廣告商和自訂目標的跨位置資料。 您可以選擇設定篩選條件，以顯示不同廣告商、不同自訂目標或特定位置的資料。 <!-- I don't see campaigns or packages anymore:  You can optionally configure filters to show data for a different advertiser or data for only specific campaigns, packages, custom goals, and placements. -->深入分析包括：

* **[!UICONTROL Trends]：**&#x200B;三個客戶指定量度（預設為[!UICONTROL Net Spend]、[!UICONTROL Impressions]和[!UICONTROL Net CPM]）的趨勢圖。

* **[!UICONTROL Delivery Breakdown]：**&#x200B;依三個客戶指定的維度（例如依促銷活動、發行者和媒體型別）劃分特定量度的資料。 您可以為每個維度劃分選擇不同的量度。

### [!UICONTROL Household Reach]索引標籤

[!UICONTROL Household Reach]標籤跨廣告商的所有行銷活動提供住戶觸及度量。 依預設，會顯示跨行銷活動的資料。 您可以選擇設定篩選器，以顯示不同廣告商、特定行銷活動、跨套件或位置，或特定套件或位置的資料。 這些見解包括：

* **[!UICONTROL Trends]：**&#x200B;三個客戶指定量度（預設為[!UICONTROL Net Spend]、[!UICONTROL Unique Reach]和[!UICONTROL Net CPM]）的趨勢圖（依日或依周）。

* **[!UICONTROL Incremental Household Reach]：**&#x200B;環圈圖，顯示[!UICONTROL Media Type]、[!UICONTROL Device Type]或[!UICONTROL Inventory Type]的遞增家庭觸及率。 *遞增式住戶觸及率*&#x200B;定義為僅透過單一媒體、裝置或詳細目錄型別觸及的住戶。

* **[!UICONTROL Reach Breakdown]：**&#x200B;遞增不重複家庭觸及與重疊家庭觸及的比較，由[!UICONTROL Media Type]、[!UICONTROL Device Type]或[!UICONTROL Inventory Type]決定。

  *遞增式住戶觸及率*&#x200B;定義為僅透過單一媒體、裝置或詳細目錄型別觸及的住戶。 *重疊的家庭範圍*&#x200B;定義為透過多種媒體、裝置或詳細目錄型別觸及的家庭。

* **[!UICONTROL Top Performers]：** [!UICONTROL Unique Reach]、[!UICONTROL Net Spend]和[!UICONTROL Cost per Reach]在行銷活動、位置、套件、發行者、網站/應用程式、媒體型別、詳細目錄型別或裝置型別方面表現最佳的行銷活動。

* **[!UICONTROL Performance Analysis]：**&#x200B;封裝、發行者或網站/應用程式所使用的[!UICONTROL Cost per Reach]和[!UICONTROL Net Spend]。 使用此insight可檢視哪些套件、發佈者或網站/應用程式顯示有大幅增加觸及的潛力。

  每個泡泡的大小表示遞增觸及分數，較大的泡泡表示平均遞增觸及較高。 若要檢視任何泡泡的完整實體名稱和關鍵量度，請將游標停留在泡泡上。

  影響的層級包括：

   * **高影響：**&#x200B;請考慮增加預算。
   * **中等影響**
   * **有限影響：**&#x200B;需要注意

### [!UICONTROL Household Conversion]索引標籤

[!UICONTROL Household Conversion]索引標籤會針對廣告商的所有行銷活動<!-- active only? -->提供家庭轉換量度。 依預設，會顯示特定廣告商的跨促銷活動資料以及特定的轉換量度。 您可以選擇設定篩選器，以顯示不同廣告商或轉換量度、特定行銷活動、跨套件或位置，或特定套件或位置的資料。 這些見解包括：

* **[!UICONTROL Trends]：**&#x200B;三個客戶指定量度（預設為[!UICONTROL Net Spend]、[!UICONTROL Conversions]和[!UICONTROL Net CPM]）的趨勢圖（依日或依周）。

* **[!UICONTROL Conversion Participation Overview]：**&#x200B;條狀圖顯示哪些媒體型別、詳細目錄型別和裝置型別導致大部分的家庭轉換。

  在回顧期間（30天）內傳送的曝光次數會視為適用於轉換參與率。

* **[!UICONTROL Top Performers]：**&#x200B;促銷活動、套件、位置、發佈者、網站/應用程式、媒體型別和詳細目錄型別的表格，可提升三個客戶指定量度（預設為[!UICONTROL Net Spend]、[!UICONTROL CPA]和[!UICONTROL Conversions]）的效能。 首先列出績效最高的人。

* **[!UICONTROL Performance Analysis]：**&#x200B;封裝、發行者或網站/應用程式所使用的[!UICONTROL CPA]和[!UICONTROL Net Spend]。 使用此insight可檢視哪些套件、發佈者或網站/應用程式顯示有大幅增加觸及的潛力。

  每個泡泡的大小表示遞增觸及分數，較大的泡泡表示平均遞增觸及較高。 若要檢視任何泡泡的完整實體名稱和關鍵量度，請將游標停留在泡泡上。

  影響的層級包括：

   * **高影響：**&#x200B;請考慮增加預算。
   * **中等影響**
   * **有限影響：**&#x200B;需要注意

## 開啟效能分析

* （若要開啟所有行銷活動的深入分析）在主功能表中，按一下&#x200B;**[!UICONTROL Insights BETA]**。

* （若要開啟特定行銷活動、封裝或位置的深入分析），請在[!UICONTROL Campaigns]、[!UICONTROL Packages]或[!UICONTROL Placements]檢視中的實體名稱旁，按一下「**[!UICONTROL ...]**」>「**[!UICONTROL Insights]**」。

## 將篩選器套用至索引標籤

1. 在索引標籤頂端的工具列中按一下![篩選按鈕](/help/dsp/assets/filter.png)。

1. 在左欄中選取維度，然後在右欄中選取一或多個值（如適用）。

   您一次只能選取一個廣告商。

1. 按一下&#x200B;**[!UICONTROL Apply]**。

1. （可選）若要進一步縮小資料範圍，請在工具列中選取實體型別，然後選取特定實體值（單一行銷活動、套件或位置）。

## 變更為Insight報告的Dimension

* 從insight左上方的下拉式功能表中選取維度。

## 變更Insight的回報量度

對於轉換量度，可同時支援Adobe Advertising追蹤和Adobe Analytics追蹤的轉換。

1. 在insight的右上角，按一下![量度設定](/help/dsp/assets/metric-settings.png "量度設定")。

1. 選取度量，然後按一下&#x200B;**[!UICONTROL Apply]**。

## 將索引標籤的所有視覺效果匯出至PDF檔案

* 在索引標籤上方，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Export]**。

  檔案會儲存至瀏覽器的預設「下載」資料夾。

## 將特定的Insight下載至XLSX檔案

* 在insight的右上角，按一下![下載](/help/creative/assets/download.png "下載")。

  檔案會儲存至瀏覽器的預設「下載」資料夾。

>[!MORELIKETHIS]
>
>* [關於自訂報告](/help/dsp/reports/report-about.md)
>* 行銷活動管理檢視中的[效能報表型別](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用的報告欄](/help/dsp/reports/report-columns.md)
>* [管理您的行銷活動資料檢視](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
