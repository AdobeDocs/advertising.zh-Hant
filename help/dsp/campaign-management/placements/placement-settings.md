---
title: 位置設定
description: 請參閱可用位置設定的說明。
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: caab8c3163a7ffdbc0b5ef28176b2ee73f83b6e8
workflow-type: tm+mt
source-wordcount: '3540'
ht-degree: 0%

---

# 位置設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 位置名稱。

>[!TIP]
>使用適合您情況的命名慣例。 一個建議的命名慣例是「*\&lt;campaign name=&quot;&quot;>： \&lt;ad unit=&quot;&quot;>： \&lt;duration>： \&lt;targeting>*.」

**[!UICONTROL Status]：** 位置狀態： *[!UICONTROL Active]* （預設）或 *[!UICONTROL Paused]*.

>[!TIP]
>最佳實務是暫停位置，直到準備好啟動為止。

**[!UICONTROL Details]：** （唯讀）適用的廣告型別、建立或建立刊登版位的帳戶以及父級行銷活動。 若要檢視詳細資訊，請按一下 **[!UICONTROL Show more]**.

**[!UICONTROL Templates]：** 開啟現有版位範本的清單。 若要從範本自動填入鎖定目標設定：

1. 執行下列任一項作業：

   * 若要重複使用範本中的所有目標，請選取範本名稱旁的核取方塊。

   * 若要重複使用範本中的個別目標型別，請展開範本名稱並選取您要重複使用的目標型別旁的核取方塊。

1. 按一下 **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]：** （僅限視訊廣告格式）廣告持續時間及/或廣告規格，用於計算右側的「預測」預測。 欄位會依廣告型別而異。

**[!UICONTROL Environment]：** （僅限通用視訊廣告格式）要當作目標包含在位置中的裝置環境（桌上型電腦、行動裝置、連線電視）。 請至少指定一個。

在自訂報表中，位置層級維度「裝置環境」會指出目標環境。

**[!UICONTROL Placement tags]：** （選擇性）關鍵字或暱稱可協助您找到此位置。

## 目標

**[!UICONTROL Package]：** （選用）位置指派到的套件。 按一下 ![編輯](/help/dsp/assets/edit.png) 以選取現有封裝或建立封裝。 將位置指派給封裝時， [!UICONTROL Goals] 區段會以套件中的投放日期、傳遞目標和預算更新。

**[!UICONTROL Flight Dates]：** 刊登的開始日期和結束日期。 當版位處於作用中狀態並指派給作用中的套件或行銷活動時，核准的廣告即符合在飛行期間執行的資格。

套件（如適用）或促銷活動的日期預設為自動填入。

>[!NOTE]
>
>* 投放日期必須包含在行銷活動投放日期和套件投放日期中。

### 指派給具有封裝層級步調之封裝的版位

**[!UICONTROL Placement Funding]：** 如何為位置編列預算：

* *[!UICONTROL Optimize based on performance]：* 控制封裝層級的預算。
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]：* 可讓您設定最小和/或最大版位預算。 至少指定一種預算型別：

   * *[!UICONTROL Maximum Budget]*：輸入值和持續時間(*[!UICONTROL All time]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*)。

   * *[!UICONTROL Minimum Budget]*：最小預算（以套件預算的百分比表示）。 指定間隔上限時，最小預算值一律會計算為間隔上限的百分比。 否則，會以套件預算的百分比計算。

**[!UICONTROL Max Bid]：** 1000次曝光最多付費。

**[!UICONTROL Placement Pre-bid Filters]：** 最多需要達到五個KPI臨界值（例如最低可檢視度量度或點進率），才能進行競標。 您可以將競標前篩選器作為最佳化策略，但瞭解每個規則可能會限制此位置競標的機會。 若要新增或編輯篩選器：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一項作業：
   * 若要新增篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 旁邊 **[!UICONTROL Only bid if]**，選取量度，然後輸入值。
   * 若要移除篩選器，請按一下 **[!UICONTROL X]** 在篩選列中。
1. 按一下 **[!UICONTROL Save]**.

如需各個競標前篩選器的說明，請參閱「[位置層級競標前篩選器及其使用方式](/help/dsp/optimization/optimization-pre-bid-filters.md).」

### 所有其他版位

**[!UICONTROL Budget Goal]：** 總預算上限與預算間隔(*[!UICONTROL All time]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]：** （僅具有利潤管理的行銷活動中的位置）總預算上限和預算間隔(*[!UICONTROL All time]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]：**  套件的最佳化目標。 如需各個最佳化目標的說明，請參閱「[最佳化目標及使用方式](/help/dsp/optimization/optimization-goals.md)「。

**[!UICONTROL Target Goal]：** 用於追蹤效能的目標目標。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Pace on]：** 步調的基礎：

* **[!UICONTROL Budget goal]：** （預設）此選項會在配置的預算內儘可能多地提供曝光數。

* **[!UICONTROL Impressions]：** 此選項會傳送曝光次數，直到在指定間隔內達到指定數量為止。 選取此選項時，請指定曝光次數和間隔： *[!UICONTROL All time]，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]：** 1000次曝光最多付費。

**[!UICONTROL Flight pacing]：** （只有具有刊登版位層級步調的刊登版位）如何調整廣告投放步調：

* *[!UICONTROL Even]：* （預設）以每次飛行各50%的目標為準進行均勻進度傳送。

* *[!UICONTROL Slightly Ahead]：* （預設）加速傳遞，使其在飛行期間的中途完成55-65%。

* *[!UICONTROL Frontload]：* 加速傳遞，使其在飛行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：* 加速傳遞，使其在飛行中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （僅具有刊登版位層級步調的刊登版位）如何在飛行中每天進行廣告投放步調：

* *[!UICONTROL Even]：* （預設）根據存貨可用性調整交貨規模。 一般而言，拍賣量較大時，白天每小時會傳送更多廣告，而早上和晚上傳送的廣告會較少。

* *[!UICONTROL ASAP]：* （預設）將傳送速度加快一倍 *平均*.

  >[!CAUTION]
  >
  >此選項可能對效能造成負面影響。 只有在您完全排定傳送的優先順序，且花費在效能最佳化上時，才使用它。

**[!UICONTROL Placement Pre-bid Filters]：** （選用）最多必須符合五個篩選器，才能進行競標。 您可以使用競標前篩選器作為最佳化策略，但請記住，每個規則可能會限制此位置競標的機會。 若要新增或編輯篩選器：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一項作業：
   * 若要新增篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 旁邊 **[!UICONTROL Only bid if]**，選取量度，然後輸入值。
   * 若要移除篩選器，請按一下 **[!UICONTROL X]** 在篩選列中。
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]：** （選用）在版位中包含或排除廣告的特定位置。 如果您未指定任何位置，則會鎖定所有位置。

>[!NOTE]
>
>Roku位置無法使用城市和DMA位置。

若要指定位置，請執行下列動作：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一項作業：
   * 若要包含或排除國家、州、市、DMA、聯邦立法區或州立法區，請執行下列動作：
      1. 在左欄中選取位置型別。
      1. （視需要）按一下位置以展開它。
      1. 在位置旁邊，按一下 *[!UICONTROL Include]* 將其加入為目標或 *[!UICONTROL Exclude]* 以將其排除為目標。
   * 若要搜尋郵遞區號，並包含或排除所有選取的結果，請執行下列動作：
      1. 按一下 **[!UICONTROL Search Postal Code]**.
      1. 選取國家/地區。
      1. 輸入城市名稱，然後按一下 ![編輯](/help/dsp/assets/search.png).
      1. 按一下正確的搜尋結果。
      1. 按一下 *[!UICONTROL Include All]* 若要將所有位置納入目標或 *[!UICONTROL Exclude All]* 以排除所有位置作為目標。
   * 若要輸入或貼上郵遞區號，並包含或排除所有郵遞區號：
      1. 按一下 **[!UICONTROL Paste Postal Code]**.
      1. 選取國家/地區。
      1. 輸入或貼上最多1000個郵遞區號。
每行包含一個郵遞區號，或輸入多個值，並以逗號或定位點分隔。
      1. 按一下 *[!UICONTROL Include All]* 若要將所有位置納入目標或 *[!UICONTROL Exclude All]* 以排除所有位置作為目標。
   * 若要從移除位置 [!UICONTROL Included] 或 [!UICONTROL Excluded] 清單，按一下 **[!UICONTROL X]** 位於右欄中的位置旁。
1. 按一下 **[!UICONTROL Done]**.

>[!NOTE]
>
>* 並非所有國家/地區都有州、城市或郵遞區號位置。
>* DMA （指定市場區域）、聯邦立法區和州立法區僅適用於美國地點。

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]：** 要納入或排除作為目標的詳細目錄來源。 對於大多數版位型態，預設會包含所有存貨型態及每種型態的所有來源。 的 [!DNL Roku] 版位，您必須指定存貨型態與來源。 您可以從下列存貨型態中選擇：

* [!UICONTROL Public]：（除Roku外的所有放置型別）DSP有權存取的所有未結交換存取。 您可以包含和排除公開詳細目錄。

  您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要索引鍵或選取的特徵標籤進行搜尋。

* [!UICONTROL Private] | [!UICONTROL Roku Private]：您現有的私人交易（或現有的私人交易） [!DNL Roku] 交易： [!DNL Roku] 位置)，以及您已在DSP中設定的發佈者。 您可以包含（但不排除）公用詳細目錄。

  您可以依關鍵字、金鑰、交易ID或自訂標籤來搜尋清單。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*：（選擇性）覆寫競標價演演算法，至少以交易的固定與最低價格投標。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]：全部 [溢價，不保證 [!UICONTROL On Demand] 詳細目錄](/help/dsp/inventory/on-demand-inventory-about.md) (或 [!UICONTROL On Demand] [!DNL Roku] 交易： [!DNL Roku] 個位置)，您已訂閱此位置 [!DNL DSP]. 您可以包含和排除 [!UICONTROL On Demand] 詳細目錄。

  您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要金鑰或選取的發佈者區域、類別標籤或特性標籤進行搜尋。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*：（選擇性）覆寫競標價演演算法，至少以交易的固定與最低價格投標。

若要指定詳細目錄目標定位：

* 若要排除清查型別，請清除名稱旁的核取方塊。
* 若要鎖定存貨型態，請執行下列步驟：
   1. 選取存貨型別名稱旁的核取方塊。
   1. （可選）變更來源以包含：
      1. 按一下 ![編輯](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] 和 [!UICONTROL On Demand] 詳細目錄)按一下 **[!UICONTROL View by Source]** 或 **[!UICONTROL View by Feed]** 以變更來源的列出方式。
      1. （適用時）視需要篩選詳細目錄。
      1. 指定要包含和排除的來源：
         * 若要包含 [!UICONTROL Public] 或 [!UICONTROL On Demand] 來源，按一下 **[!UICONTROL Include]** 在來源名稱旁邊。
         * 要包含 [!UICONTROL Private] 來源：
            * 若要在交易中包含所有詳細目錄，請按一下 **[!UICONTROL Include all]** 位於交易名稱旁。
            * 若要包含個別存貨來源，請展開交易名稱，然後按一下來源名稱旁的核取方塊。
         * 若要排除 [!UICONTROL Public] 或 [!UICONTROL On source]，按一下 **[!UICONTROL Exclude]** 在來源名稱旁邊。
   1. （選用）若要將包含目標資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Save & Export]**.
   1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>如果您訂閱 [!UICONTROL On Demand] 詳細目錄，但找不到要鎖定的發佈者或交易，然後檢查交易的狀態。 如需有關狀態的詳細資訊，請參閱 [關於 [!DNL On Demand] 進階詳細目錄](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]：** （僅限視訊位置）排除輸出流量。

串流廣告通常以快顯視窗或填入內容（在原生體驗中）的形式出現在內容上，而不是在視訊播放器中一般視訊廣告。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]：** 要鎖定的流量型別。 選項包括 **[!UICONTROL Websites]** 和 **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]：** (可用時機 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)目標網站的品質。 第1層至第3層均符合品牌安全標準，並經DSP對應團隊審查及核准。

* *[!UICONTROL Tier 1]：* 具全國知名度的優質網站和應用程式。

* *[!UICONTROL Tier 2]：* 鎖定第1級以及知名度低於第1級的高品質網站和應用程式。

* *[!UICONTROL Tier 3]：* 鎖定第1層至第2層，外加符合細分受眾需求且符合品牌安全要求的合法網站和應用程式。 使用第3層進行觸及或資料目標定位購買。

* *[!UICONTROL All Sites]：* 鎖定第1層至第3層以及尚未篩選或分類的新詳細目錄，您可將其用於觸及範圍。

>[!NOTE]
>
>詳細目錄專屬於刊登版位中的廣告單位。

>[!TIP]
>
>針對效能行銷活動，最佳實務是選取 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]：** (選用；適用時機 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)在選取的網站層級中納入或排除（但不是兩者）作為目標的網站類別。 從DSP已根據主旨對應的垂直網站清單中選擇：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要包含或排除的網站類別：
   * 若要包含網站類別，請執行下列動作：
      1. 按一下 **[!UICONTROL Include categories]**.
      1. 選取每個要定位的類別旁的核取方塊。
   * 若要排除網站類別，請執行下列動作：
      1. 按一下 **[!UICONTROL Exclude categories]**.
      1. 選取每個要排除的類別旁的核取方塊。
1. （選用）若要將包含目標資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]：** (選用；適用時機 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)要排除的網站。 您可以搜尋及選取網站，或輸入或貼上網域名稱：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定網站：
   * 若要搜尋網站：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選取網站層，以及/或選取網站類別。
      1. 在搜尋結果中，選取要排除的網站：
         * 若要排除個別網站，請選取它旁邊的核取方塊。
         * （可用結果超過50個時）若要排除前50個結果，請按一下 **[!UICONTROL Exclude these 50]**. 若要排除所有搜尋結果，請按一下 **[!UICONTROL Exclude these \<*NN *\>]**.
   * 若要輸入網域名稱，請執行下列動作：
      1. 按一下 **[!UICONTROL Paste]**.
      1. 在不同行中輸入一或多個網域名稱。
      1. 按一下 **[!UICONTROL Exclude All]**.
1. 按一下 **[!UICONTROL Done]** 完成時。

>[!NOTE]
>
>* 除了DSP之外，也會套用帳戶層級和廣告商層級的封鎖網站清單 [全域封鎖的網站清單](/help/dsp/introduction/features/brand-safety-media-quality.md)，其中包含不安全的廣告網站。
>* 封鎖的網站清單一律會覆寫目標網站清單。 如果位置同時排除並包含廣告的相同目標，則會排除目標。

**[!UICONTROL Language]：** （選用）單一目標語言。

**[!UICONTROL Site List Preview]：** （唯讀）此位置的所有鎖定和封鎖網站。

您可以選擇將目標網站和封鎖網站的清單匯出為逗號分隔值(CSV)檔案。 若要匯出清單，請按一下 **[!UICONTROL Export full site list]**，然後依照瀏覽器的正常程式開啟或儲存檔案。

**[!UICONTROL Allow unscreened sites]：** （僅限標準顯示位置）啟用未稽核網站上的廣告傳遞。 當此版位鎖定私人詳細目錄時，此選項可能會在封鎖的網站上傳送廣告。

**[!UICONTROL Paste list of targeted sites]：** 僅允許您鎖定特定網站。 啟用此選項時，其他網站鎖定目標選項會停用。

**[!UICONTROL Sites]：** (可用時機 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL On]*)要定位的網站。 您可以搜尋及選取網站，或輸入或貼上網域名稱：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定網站：
   * 若要搜尋網站：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選取網站層，以及/或選取網站類別。
      1. 在搜尋結果中，選取要包含的網站：
         * 若要排除個別網站，請選取它旁邊的核取方塊。
         * （可用結果超過50個時）若要包含前50個結果，請按一下 **[!UICONTROL Include these 50]**. 若要包含所有搜尋結果，請按一下 **[!UICONTROL Include these \<*NN *\>]**.
   * 若要輸入網域名稱，請執行下列動作：
      1. 按一下 **[!UICONTROL Paste]**.
      1. 在不同行中輸入一或多個網域名稱。
      1. 按一下 **[!UICONTROL Include All]**.
1. 按一下 **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]：** 此位置的任何對象目標，包括 [第三方區段、第一方區段、Adobe區段、自訂區段和儲存的對象](/help/dsp/audiences/audience-settings.md). 也會顯示所有所選區段和已儲存對象的作用中重複資料刪除對象人數總計。 您可以選取現有對象、建立可稍後重複使用的對象，或選取特定對象區段：

* 若要選取現有對象，請按一下 ![選取](/help/dsp/assets/chevron-down.png) 旁邊 [!UICONTROL Included Audiences]，然後選取對象。
* 若要建立對象，請按一下 ![選取](/help/dsp/assets/chevron-down.png) 旁邊 [!UICONTROL Included Audiences]，然後選取 **[!UICONTROL + Create Audience]**. 如需指示，請參閱 [建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)，從步驟3開始。
* 若要選取特定受眾區段，請按一下 **[!UICONTROL Select segments for this placement only]**. 選取區段邏輯；如需指示，請參閱&quot;[建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md).」 完成後，按一下 **儲存**.

**[!UICONTROL Excluded Audiences]：** 要針對此位置排除的任何對象，包括具有下列專案的對象： [第三方區段、第一方區段、Adobe區段、自訂區段和儲存的對象](/help/dsp/audiences/audience-settings.md). 也會顯示所有排除對象中的總計和作用中重複資料刪除對象人數。 您可以選取現有對象或建立新對象，以便稍後重複使用：

* 若要選取現有對象，請按一下 ![選取](/help/dsp/assets/chevron-down.png) 旁邊 [!UICONTROL Excluded Audiences]，然後選取對象。
* 若要建立對象，請按一下 ![選取](/help/dsp/assets/chevron-down.png) 旁邊 [!UICONTROL Excluded Audiences]，然後選取 **+建立對象**. 如需指示，請參閱 [建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)，從步驟3開始。
* 若要選取特定受眾區段，請按一下 **[!UICONTROL Select segments for this placement only]**. 選取區段邏輯；如需指示，請參閱&quot;[建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md).」 完成後，按一下 **儲存**.

**[!UICONTROL Cross Device Targeting]：** (至少選取一個區段或對象，然後 [行銷活動已設定為以人物為基礎的跨裝置目標定位](/help/dsp/campaign-management/campaigns/campaign-settings.md). 可讓您將目標延伸至所有人的所有已知裝置（根據促銷活動設定中指定的裝置圖表），甚至不在指定區段中的裝置。 費用可能會根據為行銷活動指定的圖表而套用。 裝置圖表資料僅在北美提供。

**[!UICONTROL Placement Cap]：** （選用）不重複裝置或個人的次數(取決於指定的 [!UICONTROL Cross Device Level] （適用於促銷活動），則會從版位提供廣告。 選項包括 *[!UICONTROL Unlimited]* 或每日、周或月的特定金額。

>[!NOTE]
>
> 您可以在行銷活動、封裝和位置層級設定頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Secondary Cap]：** (選擇性；當您包含數值時可用 [!UICONTROL Placement Cap])主要位置上限範圍內的附加限制。 選取曝光次數和時段（例如每12小時3次）。

**[!UICONTROL Day Parting]：** （選用）一週中的特定日數以及廣告可能在一天中的哪個時間執行。 若要指定日時段間隔：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 選取適用的時區。
1. 指定間隔：
   * 若要選取預設間隔，請按一下其中一個間隔按鈕。 選項包括*[!UICONTROL Weekends]**， *[!UICONTROL Weekdays]*， *[!UICONTROL Morning]*， *[!UICONTROL Lunch]*， *[!UICONTROL Dinner]*，或 *[!UICONTROL Prime]* (primetime)。
   * 若要手動選取間隔，請在儲存格內按一下，並選擇拖曳以選取間隔。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]：** (選用；可供設定了下列專案的廣告商使用： [!DNL Comscore] 和 [!DNL Grapeshot] 區段)來自的特定區段名稱或ID [!DNL Comscore] 和 [!DNL Grapeshot] 以包含為目標。 此功能可能需支付額外費用。 若要啟用此功能及設定主題區段，請聯絡您的Adobe客戶團隊。

若要指定主題目標定位：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要定位的區段：
   1. 在左欄中，選取合作夥伴(*[!UICONTROL Comscore]* 或 *[!UICONTROL Grapeshot]*)。
   1. 在輸入欄位中輸入區段名稱或區段ID。
1. （選用）若要將包含主題資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>* 主題鎖定目標會限制位置可出價的詳細目錄，因此主題鎖定目標僅佔整體購買的一小部分。
>
>* 在上設定任何負面目標定位 [!DNL Comscore] 或 [!DNL Grapeshot].

**[!UICONTROL Device Targeting]：** （選擇性）特定裝置資訊，包括裝置型別、製造商、作業系統、瀏覽器和連線型別，以納入和排除作為目標。 若要指定裝置目標定位：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要包含和排除的裝置詳細資料：
   1. 在左欄中選取類別。
   1. 指定目標：
      * 若要包含值，請按一下 **[!UICONTROL Include]** 值名稱旁。
      * 若要排除值，請按一下 **[!UICONTROL Exclude]** 值名稱旁。
1. （選用）若要將內含裝置目標定位資訊的CSV檔案下載至瀏覽器的下載位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]：** （選擇性）要納入或排除（但不是兩者都包括）為目標的特定網際網路服務提供者(ISP)。 若要指定ISP目標定位：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要包含或排除的ISP：
   * 納入ISP：
      1. 按一下 **[!UICONTROL Include ISPs]**.
      1. （選用）依關鍵字篩選清單。
      1. 選取每個要鎖定的ISP旁的核取方塊。
   * 排除ISP：
      1. 按一下 **[!UICONTROL Exclude ISPs]**.
      1. （選用）依關鍵字篩選清單。
      1. 選取每個要排除的ISP旁的核取方塊。
1. （選用）若要將含有ISP目標定位資訊的CSV檔案下載至瀏覽器的下載位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]：** 型別 [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39] 要套用的內容篩選器。 針對新版位選取廣告商層級預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]：

   * **[!UICONTROL Block sites that are]：** （選用）預設要封鎖的一或多個存貨內容型別。 可能需支付額外費用。

* [!UICONTROL Peer 39]：

   * **目標網站為：** （選用）預設要鎖定的一或多個存貨屬性型別。 可能需支付額外費用。

* [!UICONTROL ComScore]：

   * **封鎖符合以下條件的網站：** （選擇性）預設要封鎖的一或多個存貨屬性型別。 可能需支付額外費用。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]：** （選用）預設封鎖廣告的成人內容程度： *[!UICONTROL Do Not Block]* （預設）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

   * **[!UICONTROL Alcohol Content]：** （選用）預設封鎖廣告的酒精含量等級： *[!UICONTROL Do Not Block]* （預設）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

**[!UICONTROL Pre-bid fraud blocking]：** 根據詐騙流量和透過測量的可疑活動封鎖的網站型別 [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39]. 針對新版位選取廣告商層級預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]：

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：** 依預設，會針對新位置封鎖所有100%無效的流量，包括被劫持裝置上的流量。 可能需支付額外費用。

   * **[!UICONTROL Also block sites with]：** （選用）額外的詐騙和無效流量層級，導致DSP依預設封鎖廣告：  *[!UICONTROL None]* （預設值，不會封鎖其他流量）， *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*， *[!UICONTROL >4% Average Fraud/IVT levels]*， *[!UICONTROL >6% Average Fraud/IVT levels]*， *[!UICONTROL >10% Average Fraud/IVT levels]*，或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需支付額外費用。

* [!UICONTROL Peer 39]：

   * **[!UICONTROL Block sites that are]：** （選用）一或多個詐騙型別，預設會導致DSP封鎖廣告： *[!UICONTROL Fraud]* （會封鎖所有詐騙網站）、 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需支付額外費用。

* [!UICONTROL Integral Ad Science]：

   * **[!UICONTROL Block sites that are]：** （選用）一種可疑DSP網站或應用程式活動，預設會封鎖廣告： *[!UICONTROL None]* （預設值，不會根據可疑活動封鎖廣告）， *[!UICONTROL Suspicious Activity - High Risk]*，或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需支付額外費用。

**[!UICONTROL Ads.txt filtering]：**

哪個層級 [Ads.txt](https://iabtechlab.com/ads-txt-about/) 要透過套用每個發佈者的「授權數位賣家」清單來使用的競標前篩選。 針對新刊登版位選取廣告商層級的預設值，但您可以變更設定：

* *[!UICONTROL Opt out of ads.txt (default)]*：從所有賣家購買詳細目錄。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：優先從網域的授權直接銷售者和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：僅向網域的授權直接銷售者和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：僅從網域的授權直接銷售者購買詳細目錄。

**[!UICONTROL DoubleVerify Authentic Brand Safety]：** (廣告商設定了 [!UICONTROL DoubleVerify Authentic Brand Safety] option)啟用 [!DNL DoubleVerify Authentic Brand Safety]，會使用針對指定區段ID設定的自訂品牌安全規則，封鎖競標後的曝光數。 DSP會針對廣告商設定中所指定的區段ID向您的帳戶開立帳單。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] 位置)核准的第三方追蹤廠商 [!DNL Roku] 包含 [!DNL Acxiom]， [!DNL comScore]， [!DNL Data Plus Math]， [!DNL Experian]， [!DNL Factual]， [!DNL Kantar]， [!DNL Marketing Evolution]， [!DNL Neustar]， [!DNL Nielsen]， [!DNL Nielsen Catalina Solutions]， [!DNL NinthDecimal]， [!DNL Oracle]， [!DNL Placed]， [!DNL Polk]、和 [!DNL Research Now].

**[!UICONTROL Event Pixels]：** （選用）預設要附加至位置中所有新廣告的第三方事件追蹤畫素。 若要指定事件畫素：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一項作業：
   * 若要選取現有畫素，請選取畫素列中的核取方塊。
   * 若要建立畫素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入下列資訊：
         * **[!UICONTROL Pixel name]：** 畫素名稱；長度上限為500個字元。 使用有助於您輕鬆識別畫素的名稱。
         * **[!UICONTROL Pixel event fires on]：** 觸發畫素引發的事件。 可用的事件因廣告型別而異。
         * **[!UICONTROL Pixel type]：** 畫素是否為 *[!UICONTROL IMG URL]* （1x1畫素影像檔案）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]：** 畫素影像的URL。
      1. 按一下 **[!UICONTROL Create and attach]**.
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]：** （選用）依預設要附加至位置中所有新廣告的轉換追蹤畫素。 若要指定轉換畫素：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一項作業：
   * 若要選取現有畫素，請選取畫素列中的核取方塊。
   * 若要建立畫素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入下列資訊：
         * **[!UICONTROL Conversion pixel name]：** 畫素名稱；長度上限為500個字元。 使用有助於您輕鬆識別畫素的名稱。
         * **[!UICONTROL Conversion category]：** 轉換型別。
         * **[!UICONTROL Impression conversion window]：** 廣告曝光發生後，曝光可歸因於轉換的天數。 預設值為30天。
         * **[!UICONTROL Click conversion window]：** 廣告點選發生後的天數，該點選可歸因於轉換。 預設值為30天。
         * **[!UICONTROL Notes]：** （選用）畫素的描述或其他資訊。
      1. 按一下 **[!UICONTROL Create and attach]**.
      1. 在相關網頁上實作轉換畫素：
         1. 在主功能表中，前往 **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. 在畫素列中，按一下 **[!UICONTROL edit]**.
         1. 將值複製到 [!UICONTROL HTML Tag] 和 [!UICONTROL Flash Tag] 視需要提供給廣告商或網站連絡人的欄位。

            廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]：** （選用）要以每1000次曝光的不可計費成本追蹤的靜態第三方費率。 若適用，套裝程式層級預設會自動套用至新位置，除非您輸入其他值。

>[!NOTE]
>
>可記帳費用會反映在 [!UICONTROL Net CPM] 量度。

>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [建立位置](placement-create.md)
>* [編輯位置](placement-edit.md)
>* [管理位置的競標乘數](placement-manage-bid-multipliers.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [鍵盤快速鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Campaign Management常見問題集](/help/dsp/campaign-management/faq-campaign-management.md)
