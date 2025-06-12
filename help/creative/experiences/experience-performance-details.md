---
title: 體驗層級效能報表
description: 瞭解如何檢視體驗層級的效能報表。
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 118838e0236c0e40aea797edb1b2f8fb0efb2a79
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# 體驗層級效能報表

*已關閉的Beta*

您可以檢視任何體驗的詳細效能資料。

## 體驗層級效能報表中的資料

「報表」檢視包含下列資料：

* **總覽**&#x200B;標籤：整個體驗<!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." -->所有轉換量度的效能總覽，包括：

   * **整體效能**&#x200B;區段：

      * **整體效能**：曝光總數、點按、點進率(CTR)、檢視轉換和點進轉換。

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

      * **預設率**： （僅具有決策樹定位的體驗）從目標創意內容、沒有目標的一般創意內容或目標為「其他所有人」的一般創意內容，以及體驗的預設創意內容所產生的曝光次數。

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **效能劃分**&#x200B;區段：

      * **地區績效：*：依地理位置區分的個別量度。

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **裝置效能：**&#x200B;依裝置型別、作業系統和瀏覽器區分的個別量度。 可選擇按一下任何裝置類別的值，以檢視與該條件搭配使用的前<!-- NN -->個創意內容清單。

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Creative效能**&#x200B;索引標籤*：依創意和套裝或廣告標籤區分的效能概觀，包括：

   * **創意內容**&#x200B;子標籤：體驗中每個創意內容的曝光數、點按數和CTR總數。<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

   * **組合/標籤**&#x200B;子標籤：體驗中的個別組合（具有決策樹鎖定目標的體驗）或廣告標籤（沒有決策樹鎖定目標的體驗）的曝光、點按和CTR總數。

## 檢視體驗的效能報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定體驗。

1. 選取體驗：

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Reports]**。

   * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Reports]**。

   [!UICONTROL Overview]索引標籤隨即開啟。

1. （可選）在右上角工具列中指定日期範圍、轉換歸因規則，以及在所有效能報表中報告的轉換：

   * （選擇性）若要變更效能資料的日期範圍，請在日期功能表中選擇選項：

      * 若要指定預設期間，請選取報表： (*[!UICONTROL Last Month-to-date]，* *[!UICONTROL Last 7 days]，* *[!UICONTROL Last 30 days]，* *[!UICONTROL Last 7 days]，* *[!UICONTROL Last 30 days]，* *[!UICONTROL Today]，*&#x200B;或&#x200B;*[!UICONTROL Yesterday]*。

      * 若要指定自訂日期範圍，請輸入開始日期和結束日期，或按一下欄位旁的![行事曆圖示](/help/search-social-commerce/assets/calendar.png)並選取日期。

   * （選擇性）若要變更用於在一連串導致轉換的事件中歸因轉換資料的規則，請按一下![設定](/help/creative/assets/settings.png)並變更&#x200B;**[!UICONTROL Attribution Rule]**。

     如需歸因規則的詳細資訊，請參閱[歸因規則的計算方式](/help/search-social-commerce/reports/attribution-rules.md)。

   * （選擇性）若要變更報告的轉換，請按一下![設定](/help/creative/assets/settings.png)，然後在&#x200B;**[!UICONTROL Conversions]**&#x200B;功能表中選取轉換名稱。 目前，唯一可用的量度是「全選」，以包含所有轉換量度。

     可用的轉換欄包括Advertising Search、Social和Commerce中可用的轉換，無論您是否為Search、Social和Commerce客戶。 當廣告商具有[an [!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)時，清單可包含從Adobe Analytics同步的轉換和網站參與量度。 [!DNL Analytics]個計算量度和進階計算量度無法使用。 如需將收集的轉換納入報表的相關資訊，請參閱搜尋、社交和Commerce指南主題&quot;[關於管理廣告商的轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)&quot;。

1. （在[!UICONTROL Overview]索引標籤上）：

   * （選擇性）在[!UICONTROL Overall Regional Performance]區段中，將游標停留在圖表中的某個點上可檢視該點的資料。

   * （選用）在[!UICONTROL Regional Performance]區段中，執行下列任一項作業：

      * 按一下量度名稱（例如[!UICONTROL Impressions]）以檢視該量度。

      * 在[!UICONTROL Region]功能表中選取地區。

      * 將游標停留在國家或州上以檢視該區域的資料。

   * （選用）在[!UICONTROL Device Performance]區段中，執行下列任一項作業：

      * 將游標放在任何裝置類別的值上，即可檢視該條件的資料。

      * 按一下任何裝置類別的值，即可檢視與該條件搭配使用的前<!-- NN-->個創意內容清單。

1. （選擇性）若要依創意、組合或廣告標籤檢視資料，請按一下&#x200B;**[!UICONTROL Creative Performance]**&#x200B;標籤。

   * 在[!UICONTROL Creatives]子標籤上，您可以執行下列任一動作：

      * （選擇性）若要在圖表檢視和格線檢視之間切換，請分別按一下![圖表](/help/creative/assets/chart-view-button.png "圖表")和![格線](/help/creative/assets/table-view-button.png "格線")。

      * （選擇性）在圖表檢視中，將游標停留在圖表中的某個點上可檢視該點的資料。

      * （只有決策樹定位的體驗；選擇性）若要針對每個套用的廣告目標中斷效能，請啟用&#x200B;**[!UICONTROL Split targeting]**。

1. 若要依組合（具有決策樹定位的體驗）或廣告標籤（沒有決策樹定位的體驗）檢視資料，請按一下&#x200B;**[!UICONTROL Bundles]**&#x200B;子標籤。 您可以執行下列任一項作業：

   * （選擇性）若要在圖表檢視和格線檢視之間切換，請分別按一下![圖表](/help/creative/assets/chart-view-button.png "圖表")和![格線](/help/creative/assets/table-view-button.png "格線")。

   * （選擇性）在圖表檢視中，將游標停留在圖表中的某個點上可檢視該點的資料。

   * （只有決策樹定位的體驗；選擇性）若要針對每個套用的廣告目標中斷效能，請啟用&#x200B;**[!UICONTROL Split targeting]**。

## 下載體驗的效能報表

* 在效能報表頂端的工具列中按一下![下載](/help/creative/assets/download.png "下載")。

  根據瀏覽器的正常程式，檔案會以[!DNL Microsoft Excel]檔案的試算表(XLSX)格式下載。

>[!MORELIKETHIS]
>
>* [自訂Creative報告](/help/creative/report-custom-creative.md)
>* [下載檢視中的所有體驗](/help/creative/experiences/experience-download-view.md)
>* [關於Advertising Creative中的體驗](/help/creative/experiences/experience-about.md)
