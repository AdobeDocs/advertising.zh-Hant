---
title: 位置設定
description: 請參閱可用位置設定的說明。
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 07ecb613c49e27e1a1e82d7082b1715040b82610
workflow-type: tm+mt
source-wordcount: '3915'
ht-degree: 0%

---

# 位置設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]**&#x200B;位置名稱。

>[!TIP]
>使用適合您情況的命名慣例。 一個建議的命名慣例是&quot;*\&lt;行銷活動名稱\>： \&lt;廣告單位\>： \&lt;持續時間\>： \&lt;目標定位\>*&quot;。

**[!UICONTROL Status]：**&#x200B;位置狀態： *[!UICONTROL Active]* （預設）或&#x200B;*[!UICONTROL Paused]*。

>[!TIP]
>最佳實務是暫停位置，直到準備好啟動為止。

**[!UICONTROL Details]：** （唯讀）適用的廣告型別、建立或建立刊登版位的帳戶以及父級行銷活動。 若要檢視更多詳細資料，請按一下&#x200B;**[!UICONTROL Show more]**。

**[!UICONTROL Templates]：**&#x200B;開啟現有的位置範本清單。 若要從範本自動填入鎖定目標設定：

1. 執行下列任一項作業：

   * 若要重複使用範本中的所有目標，請選取範本名稱旁的核取方塊。

   * 若要重複使用範本中的個別目標型別，請展開範本名稱並選取您要重複使用的目標型別旁的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Apply]**。

**[!UICONTROL Ad specs for forecast]：** （僅限視訊廣告格式）用來計算右側預測預測的廣告持續時間和/或廣告規格。 欄位會依廣告型別而異。

**[!UICONTROL Environment]：** （僅限通用視訊廣告格式）要當作目標包含在位置中的裝置環境（桌上型電腦、行動裝置、連線電視）。 請至少指定一個。

在自訂報表中，位置層級維度「裝置環境」會指出目標環境。

**[!UICONTROL Placement tags]：** （選擇性）關鍵字或暱稱可協助您尋找此位置。

## 目標

**[!UICONTROL Package]：** （選用）指派位置的套件。 按一下![編輯](/help/dsp/assets/edit.png)以選取現有封裝或建立封裝。 將位置指派給封裝時，[!UICONTROL Goals]區段會以封裝的投放日期、傳遞目標和預算更新。

**[!UICONTROL Flight Dates]：**&#x200B;置入的開始日期和結束日期。 當版位處於作用中狀態並指派給作用中的套件或行銷活動時，核准的廣告即符合在飛行期間執行的資格。

套件（如適用）或促銷活動的日期預設為自動填入。

>[!NOTE]
>
>* 投放日期必須包含在行銷活動投放日期和套件投放日期中。

### 指派給具有封裝層級步調之封裝的版位

**[!UICONTROL Placement Funding]：**&#x200B;如何為位置編列預算：

* *[!UICONTROL Optimize based on performance]：*&#x200B;控制封裝層級的預算。
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]：*&#x200B;可讓您設定最小和/或最大版位預算。 至少指定一種預算型別：

   * *[!UICONTROL Maximum Budget]*：輸入值和持續時間(*[!UICONTROL All time]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*)。

   * *[!UICONTROL Minimum Budget]*：最小預算佔套件預算的百分比。 指定間隔上限時，最小預算值一律會計算為間隔上限的百分比。 否則，會以套件預算的百分比計算。

**[!UICONTROL Max Bid]：**&#x200B;為1000次曝光需支付的最大金額。

**[!UICONTROL Placement Pre-bid Filters]：**&#x200B;最多必須達到五個KPI臨界值（例如最低可檢視度量度或點進率），才能進行競標。 您可以將競標前篩選器作為最佳化策略，但瞭解每個規則可能會限制此位置競標的機會。 若要新增或編輯篩選器：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一項作業：
   * 若要新增篩選器：
      1. 按一下&#x200B;**[!UICONTROL Add Filter]**。
      1. 在&#x200B;**[!UICONTROL Only bid if]**&#x200B;旁邊，選取量度，然後輸入值。
   * 若要移除篩選器，請按一下篩選器列中的&#x200B;**[!UICONTROL X]**。
1. 按一下&#x200B;**[!UICONTROL Save]**。

請參閱「[位置層級競標前篩選器」處各競標前篩選器的說明及使用方式](/help/dsp/optimization/optimization-pre-bid-filters.md)。

### 所有其他版位

**[!UICONTROL Budget Goal]：**&#x200B;總預算上限與預算間隔(*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]：** （僅具有利潤管理的行銷活動中的刊登版位）總預算上限和預算間隔(*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]：**&#x200B;封裝的最佳化目標。 請在「[最佳化目標及使用方法](/help/dsp/optimization/optimization-goals.md)」檢視每個最佳化目標的說明。

**[!UICONTROL Target Goal]：**&#x200B;用來追蹤效能的目標目標。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Pace on]：**&#x200B;步調的基礎：

* **[!UICONTROL Budget goal]：** （預設）此選項會在配置的預算內儘可能多地提供曝光數。

* **[!UICONTROL Impressions]：**&#x200B;此選項會傳送曝光數，直到在指定的間隔內達到指定的數量為止。 選取此選項時，請指定曝光次數和間隔： *[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Max Bid]：**&#x200B;為1000次曝光需支付的最大金額。

**[!UICONTROL Flight pacing]：** （只有具有刊登版位層級步調的刊登版位）如何安排廣告傳送的步調：

* *[!UICONTROL Even]：* （預設） Paces會在每個航班中均勻地傳遞，目標是航班前半段的50%傳遞。

* *[!UICONTROL Slightly Ahead]：* （預設）加速傳遞，使其在飛行期間的中途完成55-65%。

* *[!UICONTROL Frontload]：*&#x200B;加速傳遞，使其在飛行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：*&#x200B;加速傳遞，使其在飛行中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （僅具有刊登版位層級步調的刊登版位）如何在航班內的每一天安排廣告傳送的步調：

* *[!UICONTROL Even]：* （預設）根據庫存可用性調整傳遞。 一般而言，拍賣量較大時，白天每小時會傳送更多廣告，而早上和晚上傳送的廣告會較少。

* *[!UICONTROL ASAP]：* （預設值）將傳遞速度加速到&#x200B;*Even*&#x200B;的兩倍。

  >[!CAUTION]
  >
  >此選項可能對效能造成負面影響。 只有在您完全排定傳送的優先順序，且花費在效能最佳化上時，才使用它。

**[!UICONTROL Placement Pre-bid Filters]：** （選擇性）最多必須符合五個篩選器，才能進行競標。 您可以使用競標前篩選器作為最佳化策略，但請記住，每個規則可能會限制此位置競標的機會。 若要新增或編輯篩選器：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一項作業：
   * 若要新增篩選器：
      1. 按一下&#x200B;**[!UICONTROL Add Filter]**。
      1. 在&#x200B;**[!UICONTROL Only bid if]**&#x200B;旁邊，選取量度，然後輸入值。
   * 若要移除篩選器，請按一下篩選器列中的&#x200B;**[!UICONTROL X]**。
1. 按一下&#x200B;**[!UICONTROL Save]**。

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]：** （選用）在版位中包含或排除廣告的特定位置。 如果您未指定任何位置，則會鎖定所有位置。

>[!NOTE]
>
>Roku位置無法使用城市和DMA位置。

若要指定位置，請執行下列動作：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一項作業：
   * 若要包含或排除國家、州、市、DMA、聯邦立法區或州立法區，請執行下列動作：
      1. 在左欄中選取位置型別。
      1. （視需要）按一下位置以展開它。
      1. 在位置旁邊，按一下&#x200B;*[!UICONTROL Include]*&#x200B;以將其納入為目標，或按一下&#x200B;*[!UICONTROL Exclude]*&#x200B;以將其排除為目標。
   * 若要搜尋郵遞區號，並包含或排除所有選取的結果，請執行下列動作：
      1. 按一下&#x200B;**[!UICONTROL Search Postal Code]**。
      1. 選取國家/地區。
      1. 輸入城市名稱，然後按一下[編輯]。![](/help/dsp/assets/search.png)
      1. 按一下正確的搜尋結果。
      1. 按一下&#x200B;*[!UICONTROL Include All]*&#x200B;以包含所有位置作為目標，或按一下&#x200B;*[!UICONTROL Exclude All]*&#x200B;以排除所有位置作為目標。
   * 若要輸入或貼上郵遞區號，並包含或排除所有郵遞區號：
      1. 按一下&#x200B;**[!UICONTROL Paste Postal Code]**。
      1. 選取國家/地區。
      1. 輸入或貼上最多1000個郵遞區號。
每行包含一個郵遞區號，或輸入多個值，並以逗號或定位點分隔。
      1. 按一下&#x200B;*[!UICONTROL Include All]*&#x200B;以包含所有位置作為目標，或按一下&#x200B;*[!UICONTROL Exclude All]*&#x200B;以排除所有位置作為目標。
   * 若要從[!UICONTROL Included]或[!UICONTROL Excluded]清單中移除位置，請按一下右側欄中位置旁的&#x200B;**[!UICONTROL X]**。
1. 按一下&#x200B;**[!UICONTROL Done]**。

>[!NOTE]
>
>* 並非所有國家/地區都有州、城市或郵遞區號位置。
>* DMA （指定市場區域）、聯邦立法區和州立法區僅適用於美國地點。

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]：**&#x200B;要納入或排除作為目標的詳細目錄來源。 對於大多數版位型態，預設會包含所有存貨型態及每種型態的所有來源。 對於[!DNL Roku]個位置，您必須指定詳細目錄型別和來源。 您可以從下列存貨型態中選擇：

* [!UICONTROL Public]： （除Roku以外的所有位置型別）DSP有權存取的所有未結交換詳細目錄。 您可以包含和排除公開詳細目錄。

  您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要索引鍵或選取的特徵標籤進行搜尋。

* [!UICONTROL Private] | [!UICONTROL Roku Private]：您與已在DSP中設定的發行者之間的現有私人交易（或[!DNL Roku]個刊登版位的現有私人[!DNL Roku]交易）。 您可以包含（但不排除）公用詳細目錄。

  您可以依關鍵字、金鑰、交易ID或自訂標籤來搜尋清單。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*： （選擇性）覆寫競標價演演算法，以至少對交易的固定與最低價格出價。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]：您已在[!DNL DSP]中訂閱的所有[優質、不保證的[!UICONTROL On Demand]詳細目錄](/help/dsp/inventory/on-demand-inventory-about.md) （或[!DNL Roku]個位置的[!UICONTROL On Demand] [!DNL Roku]交易）。 您可以包含和排除[!UICONTROL On Demand]詳細目錄。

  您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要金鑰或選取的發佈者區域、類別標籤或特性標籤進行搜尋。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*： （選擇性）覆寫競標價演演算法，以至少對交易的固定與最低價格出價。

若要指定詳細目錄目標定位：

* 若要排除清查型別，請清除名稱旁的核取方塊。
* 若要鎖定存貨型態，請執行下列步驟：
   1. 選取存貨型別名稱旁的核取方塊。
   1. （可選）變更來源以包含：
      1. 按一下![編輯](/help/dsp/assets/edit.png)。
      1. （[!UICONTROL Public]和[!UICONTROL On Demand]詳細目錄）按一下&#x200B;**[!UICONTROL View by Source]**&#x200B;或&#x200B;**[!UICONTROL View by Feed]**&#x200B;以變更來源的列示方式。
      1. （適用時）視需要篩選詳細目錄。
      1. 指定要包含和排除的來源：
         * 若要包含[!UICONTROL Public]或[!UICONTROL On Demand]來源，請按一下來源名稱旁的&#x200B;**[!UICONTROL Include]**。
         * 若要包含[!UICONTROL Private]來源：
            * 若要在交易中包含所有詳細目錄，請按一下交易名稱旁的&#x200B;**[!UICONTROL Include all]**。
            * 若要包含個別存貨來源，請展開交易名稱，然後按一下來源名稱旁的核取方塊。
         * 若要排除[!UICONTROL Public]或[!UICONTROL On source]，請按一下來源名稱旁的&#x200B;**[!UICONTROL Exclude]**。
   1. （選擇性）若要將包含目標資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下&#x200B;**[!UICONTROL Save & Export]**。
   1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!TIP]
>
>如果您已訂閱[!UICONTROL On Demand]詳細目錄，但找不到要鎖定的發行者或交易，請檢查交易的狀態。 如需有關狀態的詳細資訊，請參閱[關於 [!DNL On Demand] 進階詳細目錄](/help/dsp/inventory/on-demand-inventory-about.md)。

**[!UICONTROL Exclude out-stream]：** （僅限視訊位置）排除輸出流量。

串流廣告通常以快顯視窗或填入內容（在原生體驗中）的形式出現在內容上，而不是在視訊播放器中一般視訊廣告。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]：**&#x200B;目標流量的型別。 選項包括&#x200B;**[!UICONTROL Websites]**&#x200B;和&#x200B;**[!UICONTROL Apps]**。

**[!UICONTROL Site tier]：** （當&#x200B;**[!UICONTROL Paste list of targeted sites]**&#x200B;為&#x200B;*[!UICONTROL Off]*&#x200B;時可用）要定位的網站品質。 第1層至第3層皆符合品牌安全規範，並已獲得DSP對應團隊的核准。

* *[!UICONTROL Tier 1]：*&#x200B;全國可辨識的高階網站和應用程式。

* *[!UICONTROL Tier 2]：*&#x200B;目標為第1層，以及較第1層知之甚少的品質網站和應用程式。

* *[!UICONTROL Tier 3]：*&#x200B;鎖定第1層至第2層，加上符合細分對象需求且符合品牌安全規範的合法網站和應用程式。 使用第3層進行觸及或資料目標定位購買。

* *[!UICONTROL All Sites]：*&#x200B;目標層級1-3和尚未篩選或分類的新詳細目錄，您可以將其用於觸及範圍。

>[!NOTE]
>
>詳細目錄專屬於刊登版位中的廣告單位。

>[!TIP]
>
>針對效能行銷活動，最佳實務是選取&#x200B;*[!UICONTROL All Sites]*。

**[!UICONTROL Site Categories]：** （選擇性；當&#x200B;**[!UICONTROL Paste list of targeted sites]**&#x200B;為&#x200B;*[!UICONTROL Off]*&#x200B;時可用）所選網站層級中的網站類別要包含或排除（但不能同時包含和排除）為目標。 從DSP已根據主旨對應的垂直網站清單中選擇：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 指定要包含或排除的網站類別：
   * 若要包含網站類別，請執行下列動作：
      1. 按一下&#x200B;**[!UICONTROL Include categories]**。
      1. 選取每個要定位的類別旁的核取方塊。
   * 若要排除網站類別，請執行下列動作：
      1. 按一下&#x200B;**[!UICONTROL Exclude categories]**。
      1. 選取每個要排除的類別旁的核取方塊。
1. （選擇性）若要將包含目標資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下&#x200B;**[!UICONTROL Export]**。
1. 按一下&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL Exclude Sites]：** （選擇性；當&#x200B;**[!UICONTROL Paste list of targeted sites]**&#x200B;為&#x200B;*[!UICONTROL Off]*&#x200B;時可用）要排除的網站。 您可以搜尋及選取網站，或輸入或貼上網域名稱：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 指定網站：
   * 若要搜尋網站：
      1. 按一下&#x200B;**[!UICONTROL Search]**。
      1. 輸入關鍵字、選取網站層，以及/或選取網站類別。
      1. 在搜尋結果中，選取要排除的網站：
         * 若要排除個別場地，請選取相鄰的核取方塊。
         * （可用結果超過50個時）若要排除前50個結果，請按一下&#x200B;**[!UICONTROL Exclude these 50]**。 若要排除所有搜尋結果，請按一下&#x200B;**[!UICONTROL Exclude these \<*NN *\>]**。
   * 若要輸入網域名稱，請執行下列動作：
      1. 按一下&#x200B;**[!UICONTROL Paste]**。
      1. 在不同行中輸入一或多個網域名稱。
      1. 按一下&#x200B;**[!UICONTROL Exclude All]**。
1. 完成後，請按一下「**[!UICONTROL Done]**」。

>[!NOTE]
>
>* 除了套用DSP [全域封鎖的網站清單](/help/dsp/introduction/features/brand-safety-media-quality.md)之外，也會套用帳戶層級和廣告商層級的封鎖網站清單，此清單包含被視為不安全的廣告網站。
>* 封鎖的網站清單一律會覆寫目標網站清單。 如果位置同時排除並包含廣告的相同目標，則會排除目標。

**[!UICONTROL Language]：** （選擇性）目標單一語言。

**[!UICONTROL Site List Preview]：** （唯讀）此位置的所有鎖定和封鎖網站。

您可以選擇將目標網站和封鎖網站的清單匯出為逗號分隔值(CSV)檔案。 若要匯出清單，請按一下&#x200B;**[!UICONTROL Export full site list]**，然後依照瀏覽器的正常程式開啟或儲存檔案。

**[!UICONTROL Allow unscreened sites]：** （僅限標準顯示位置）啟用未稽核網站上的廣告傳遞。 當此版位鎖定私人詳細目錄時，此選項可能會在封鎖的網站上傳送廣告。

**[!UICONTROL Paste list of targeted sites]：**&#x200B;僅允許您鎖定特定網站。 啟用此選項時，其他網站鎖定目標選項會停用。

**[!UICONTROL Sites]：** （當&#x200B;**[!UICONTROL Paste list of targeted sites]**&#x200B;是&#x200B;*[!UICONTROL On]*&#x200B;時可用）要定位的網站。 您可以搜尋及選取網站，或輸入或貼上網域名稱：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 指定網站：
   * 若要搜尋網站：
      1. 按一下&#x200B;**[!UICONTROL Search]**。
      1. 輸入關鍵字、選取網站層，以及/或選取網站類別。
      1. 在搜尋結果中，選取要包含的網站：
         * 若要排除個別場地，請選取相鄰的核取方塊。
         * （可用結果超過50個時）若要包含前50個結果，請按一下&#x200B;**[!UICONTROL Include these 50]**。 若要包含所有搜尋結果，請按一下&#x200B;**[!UICONTROL Include these \<*NN *\>]**。
   * 若要輸入網域名稱，請執行下列動作：
      1. 按一下&#x200B;**[!UICONTROL Paste]**。
      1. 在不同行中輸入一或多個網域名稱。
      1. 按一下&#x200B;**[!UICONTROL Include All]**。
1. 按一下&#x200B;**[!UICONTROL Done]**。

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]：**&#x200B;此位置的任何對象目標，包括[第三方區段、第一方區段、Adobe區段、自訂區段和儲存的對象](/help/dsp/audiences/audience-settings.md)。 也會顯示所有所選區段和已儲存對象的作用中重複資料刪除對象人數總計。 您可以選取現有對象、建立可稍後重複使用的對象，或選取特定對象區段：

* 若要選取現有對象，請按一下[!UICONTROL Included Audiences]旁的![選取](/help/dsp/assets/chevron-down.png)，然後選取對象。
* 若要建立對象，請按一下[!UICONTROL Included Audiences]旁的![選取](/help/dsp/assets/chevron-down.png)，然後選取&#x200B;**[!UICONTROL + Create Audience]**。 如需指示，請參閱[從步驟3開始建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)。
* 若要選取特定對象區段，請按一下&#x200B;**[!UICONTROL Select segments for this placement only]**。 選取區段邏輯；如需指示，請參閱&quot;[建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)&quot;中的步驟6。 完成時，按一下&#x200B;**儲存**。

**[!UICONTROL Excluded Audiences]：**&#x200B;要排除以進行位置的任何對象，包括具有[第三方區段、第一方區段、Adobe區段、自訂區段和已儲存對象的對象](/help/dsp/audiences/audience-settings.md)。 也會顯示所有排除對象中的總計和作用中重複資料刪除對象人數。 您可以選取現有對象或建立新對象，以便稍後重複使用：

* 若要選取現有對象，請按一下[!UICONTROL Excluded Audiences]旁的![選取](/help/dsp/assets/chevron-down.png)，然後選取對象。

* 若要建立對象，請按一下[!UICONTROL Excluded Audiences]旁的![選取](/help/dsp/assets/chevron-down.png)，然後選取&#x200B;**+建立對象**。 如需指示，請參閱[從步驟3開始建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)。

**[!UICONTROL Targeting]：**&#x200B;要鎖定的使用者識別碼型別。 在投放位置上線後（即航班開始後），您無法變更此設定。

當您同時選取舊有ID和通用ID時，會為通用ID指定競標偏好設定。

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*： （預設）根據使用者的Cookie、行動廣告ID或連線電視(CTV) ID鎖定使用者。 系統會根據瀏覽器、應用程式內或CTV詳細目錄來選取ID。

* *[!UICONTROL Universal ID Beta]*：鎖定以使用者隱私權為主的ID；選取一種ID型別。 可用的選項由[!UICONTROL Geo-Targeting]區段中選取的地理目標決定。 搭配直接匯入至DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md)的[[!DNL RampID] 區段、DSP將您的PII轉換為通用ID的[區段](/help/dsp/audiences/sources/source-about.md)或追蹤通用ID的[自訂區段](/help/dsp/audiences/custom-segment-create.md)使用。

   * *[!UICONTROL ID5]*：目標[!DNL ID5] ID是依概率從電子郵件地址和其他訊號建立的。<!-- What countries/geos are these available for? Everywhere?--> ID5 ID免費提供。 **注意：**&#x200B;來自[!DNL Eyeota]的第三方區段可能包含ID5 ID。

   * *[!UICONTROL RampID]*：目標[!DNL LiveRamp] [!DNL RampIDs]使用電子郵件地址登入您網站的使用者。<!-- Verify --> [!DNL RampIDs]適用於北美、澳洲和紐西蘭的使用者。

   * *[!UICONTROL Unified ID2.0]*：使用使用者電子郵件地址登入您網站之使用者的目標[!DNL Unified ID2.0] (UID2) ID。<!-- Verify -->[!DNL UID2 IDs]不適用於歐洲經濟區和其他國家/地區的使用者。 檢視禁止的國家[清單](/help/policies/universal-id-policy.md#prohibited-countries-uid2)。

  **[!UICONTROL Terms of service]**：使用通用ID的服務合約條款。 您或DSP帳戶中的其他使用者必須接受條款一次，才能將資料轉換為新的ID型別。 若客戶擁有受管理的服務合約，您的Adobe客戶團隊將取得您的同意，並代表貴組織接受條款。 若要閱讀條款，請按一下&#x200B;**>**。 若要接受條款，請捲動至條款底部，然後按一下&#x200B;**[!UICONTROL Accept]**。

**[!UICONTROL Cross Device Targeting]：** (將[行銷活動設定為以人物為基礎的跨裝置目標定位](/help/dsp/campaign-management/campaigns/campaign-settings.md)時，即可使用；您只會目標定位舊有ID （非通用ID），而且至少要選取一個區段或對象。 可讓您將目標延伸至所有人的所有已知裝置（根據促銷活動設定中指定的裝置圖表），甚至不在指定區段中的裝置。 費用可能會根據為行銷活動指定的圖表而套用。 裝置圖表資料僅在北美提供。

**[!UICONTROL Placement Cap]：** （選用）從刊登版位提供不重複裝置、通用ID或人員（視指定的行銷活動[!UICONTROL Cross Device Level]和刊登版位的[!UICONTROL Targeting]設定而定）的次數。 選項包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每日、每週或每月的特定金額。

>[!NOTE]
>
> 您可以在行銷活動、封裝和位置層級設定頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Secondary Cap]：** （選擇性；當您包含數值[!UICONTROL Placement Cap]時可用）主要位置上限範圍內的額外限制。 選取曝光次數和時段（例如每12小時3次）。

**[!UICONTROL Day Parting]：** （選擇性）廣告可以在一週中的特定日和一天中的某個時間執行。 若要指定日時段間隔：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 選取適用的時區。
1. 指定間隔：
   * 若要選取預設間隔，請按一下其中一個間隔按鈕。 選項包括*[!UICONTROL Weekends]**、*[!UICONTROL Weekdays]*、*[!UICONTROL Morning]*、*[!UICONTROL Lunch]*、*[!UICONTROL Dinner]*&#x200B;或&#x200B;*[!UICONTROL Prime]* (primetime)。
   * 若要手動選取間隔，請在儲存格內按一下，並選擇拖曳以選取間隔。
1. 按一下&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL Topic Targeting]：** （選擇性；可供設定了[!DNL Proximic by Comscore]和[!DNL Oracle Data Cloud]區段的廣告商使用）要納入為目標的[!DNL Proximic by Comscore]和[!DNL Oracle Data Cloud] （原為[!DNL Grapeshot]）的特定區段名稱或ID。 此功能可能需支付額外費用。 若要啟用此功能及設定主題區段，請聯絡您的Adobe客戶團隊。

**注意：** [!DNL Oracle]將於2024年9月30日前淘汰其廣告業務，包括[!DNL Oracle Data Cloud] （先前稱為[!DNL Grapeshot]）的所有服務。

若要指定主題目標定位：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 指定要定位的區段：
   1. 在左欄中，選取夥伴（*[!UICONTROL Comscore]*&#x200B;或&#x200B;*[!UICONTROL Grapeshot]*）。
   1. 在輸入欄位中輸入區段名稱或區段ID。
1. （選擇性）若要將包含主題資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下&#x200B;**[!UICONTROL Export]**。
1. 按一下&#x200B;**[!UICONTROL Save]**。

>[!TIP]
>
>* 主題鎖定目標會限制位置可出價的詳細目錄，因此主題鎖定目標僅佔整體購買的一小部分。
>
>* 在[!DNL Proximic by Comscore]或[!DNL Oracle Data Cloud] （先前為[!DNL Grapeshot]）的區段內設定任何負面目標定位。

**[!UICONTROL Device Targeting]：** （選擇性）特定裝置資訊，包括裝置型別、製造商、作業系統、瀏覽器和連線型別，以包含和排除作為目標。 若要指定裝置目標定位：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 指定要包含和排除的裝置詳細資料：
   1. 在左欄中選取類別。
   1. 指定目標：
      * 若要包含值，請按一下值名稱旁的&#x200B;**[!UICONTROL Include]**。
      * 若要排除值，請按一下值名稱旁的&#x200B;**[!UICONTROL Exclude]**。
1. （選擇性）若要將包含裝置目標定位資訊的CSV檔案下載至瀏覽器的下載位置，請按一下&#x200B;**[!UICONTROL Export]**。
1. 按一下&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL ISP Targeting]：** （選擇性）要包含或排除（但不是兩者都包含）為目標的特定網際網路服務提供者(ISP)。 若要指定ISP目標定位：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 指定要包含或排除的ISP：
   * 納入ISP：
      1. 按一下&#x200B;**[!UICONTROL Include ISPs]**。
      1. （選用）依關鍵字篩選清單。
      1. 選取每個要鎖定的ISP旁的核取方塊。
   * 排除ISP：
      1. 按一下&#x200B;**[!UICONTROL Exclude ISPs]**。
      1. （選用）依關鍵字篩選清單。
      1. 選取每個要排除的ISP旁的核取方塊。
1. （選擇性）若要將包含ISP目標定位資訊的CSV檔案下載至瀏覽器的下載位置，請按一下&#x200B;**[!UICONTROL Export]**。
1. 按一下&#x200B;**[!UICONTROL Save]**。

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]：**&#x200B;要套用的[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]內容篩選器的型別。 針對新版位選取廣告商層級預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]：

   * **[!UICONTROL Block sites that are]：** （選擇性）一或多個預設要封鎖的詳細目錄內容型別。 可能需支付額外費用。

* [!UICONTROL Peer 39]：

   * **目標網站：** （選擇性）預設要定位的一或多個清查屬性型別。 可能需支付額外費用。

* [!UICONTROL ComScore]：

   * **封鎖下列網站：** （選擇性）預設會封鎖一或多個型別的詳細目錄屬性。 可能需支付額外費用。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]：** （選擇性）預設要封鎖廣告的成人內容程度： *[!UICONTROL Do Not Block]* （預設）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需支付額外費用。

   * **[!UICONTROL Alcohol Content]：** （選擇性）預設要封鎖廣告的酒精內容程度： *[!UICONTROL Do Not Block]* （預設）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需支付額外費用。

**[!UICONTROL Pre-bid fraud blocking]：**&#x200B;根據透過[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]測量的詐騙流量和可疑活動而封鎖的網站型別。 針對新版位選取廣告商層級預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]：

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：**&#x200B;依預設，會封鎖所有100%無效的流量（包括被劫持裝置上的流量），以供新位置使用。 可能需支付額外費用。

   * **[!UICONTROL Also block sites with]：** （選擇性）額外的詐騙和無效流量等級會導致DSP依預設封鎖廣告： *[!UICONTROL None]* （預設值，不會封鎖額外的流量）、*[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、*[!UICONTROL >4% Average Fraud/IVT levels]*、*[!UICONTROL >6% Average Fraud/IVT levels]*、*[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或&#x200B;*[!UICONTROL >25% Average Fraud/IVT levels]*。 可能需支付額外費用。

* [!UICONTROL Peer 39]：

   * **[!UICONTROL Block sites that are]：** （選擇性）一或多種型別的詐騙，預設會導致DSP封鎖廣告： *[!UICONTROL Fraud]* （會封鎖所有有欺詐的網站）、*[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;及/或&#x200B;*[!UICONTROL Fraud: Zero Ads]*。 可能需支付額外費用。

* [!UICONTROL Integral Ad Science]：

   * **[!UICONTROL Block sites that are]：** （選用）可疑DSP網站或應用程式活動的型別，依預設會封鎖廣告： *[!UICONTROL None]* （預設，不會封鎖基於可疑活動的廣告）、*[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或&#x200B;*[!UICONTROL Suspicious Activity - High or Moderate Risk]*。 可能需支付額外費用。

**[!UICONTROL Pre-bid viewability]：**

要套用至此位置的[!DNL DoubleVerify]、[!DNL Oracle Advertising] ([!DNL Moat])和[!DNL Integral Ad Science]的競標前可檢視度篩選器。 系統已為新版位選取廣告商層級的預設值，但您可以變更設定。 可能需支付額外費用。

>[!NOTE]
>
>[!DNL Oracle]將在2024年9月30日前停止其廣告業務，包括[!DNL MOAT]的所有服務。

**[!UICONTROL Ads.txt filtering]：**

套用每個發佈者的「授權數位賣家」清單，以使用哪個層級的[Ads.txt](https://iabtechlab.com/ads-txt-about/)競標前篩選。 針對新刊登版位選取廣告商層級的預設值，但您可以變更設定：

* *[!UICONTROL Opt out of ads.txt (default)]*：向所有賣家購買詳細目錄。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：優先從網域的授權直銷商和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：僅從網域的授權直接銷售者和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：只從網域的授權直銷商購買詳細目錄。

**[!UICONTROL Attention Targeting]：** （顯示器、視訊、行動裝置和標準連線電視位置）根據指定的網站、格式和廣告大小，鎖定具有特定關注等級（高、中或低）的[!DNL Adelaide]競標前區段。 區段每週都會更新。 **注意：**&#x200B;使用[!DNL Adelaide]區段進行目標定位，將會針對每個含有[!DNL Adelaide]關注目標定位的曝光產生CPM費用；此費用與[關注測量](/help/dsp/campaign-management/campaigns/campaign-settings.md)的費用不同。 對於互動式前段位置，您只需支付VAST曝光數的費用。

**[!UICONTROL DoubleVerify Authentic Brand Safety]：** （使用[!UICONTROL DoubleVerify Authentic Brand Safety]選項設定的廣告商）啟用[!DNL DoubleVerify Authentic Brand Safety]，這會封鎖使用針對指定區段ID設定的自訂品牌安全規則在競標後的曝光數。 DSP會針對廣告商設定中所指定的區段ID向您的帳戶開立帳單。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>（[!DNL Roku]位置） [!DNL Roku]核准的第三方追蹤廠商包括[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。

**[!UICONTROL Event Pixels]：** （選用）預設要附加至位置中所有新廣告的協力廠商事件追蹤畫素。 若要指定事件畫素：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一項作業：
   * 若要選取現有畫素，請選取畫素列中的核取方塊。
   * 若要建立畫素：
      1. 按一下&#x200B;**[!UICONTROL Create]**。
      1. 輸入下列資訊：
         * **[!UICONTROL Pixel name]：**&#x200B;畫素名稱；長度上限為500個字元。 使用有助於您輕鬆識別畫素的名稱。
         * **[!UICONTROL Pixel event fires on]：**&#x200B;觸發畫素引發的事件。 可用的事件因廣告型別而異。
         * **[!UICONTROL Pixel type]：**&#x200B;畫素是&#x200B;*[!UICONTROL IMG URL]* （1x1畫素影像檔）、*[!UICONTROL HTML]*&#x200B;或&#x200B;*[!UICONTROL JavaScript URL]*。
         * **[!UICONTROL Pixel URL]：**&#x200B;畫素影像的URL。
      1. 按一下&#x200B;**[!UICONTROL Create and attach]**。
   1. 按一下&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL Conversion Pixels]：** （選用）依預設要附加至位置中所有新廣告的轉換追蹤畫素。 若要指定轉換畫素：

1. 按一下![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一項作業：
   * 若要選取現有畫素，請選取畫素列中的核取方塊。
   * 若要建立畫素：
      1. 按一下&#x200B;**[!UICONTROL Create]**。
      1. 輸入下列資訊：
         * **[!UICONTROL Conversion pixel name]：**&#x200B;畫素名稱；長度上限為500個字元。 使用有助於您輕鬆識別畫素的名稱。
         * **[!UICONTROL Conversion category]：**&#x200B;轉換型別。
         * **[!UICONTROL Impression conversion window]：**&#x200B;廣告曝光發生後，該曝光可歸因於轉換的天數。 預設值為30天。
         * **[!UICONTROL Click conversion window]：**&#x200B;廣告點選發生後的天數，在此期間點選可歸因於轉換。 預設值為30天。
         * **[!UICONTROL Notes]：** （選擇性）畫素的描述或其他資訊。
      1. 按一下&#x200B;**[!UICONTROL Create and attach]**。
      1. 在相關網頁上實作轉換畫素：
         1. 在主功能表中，移至&#x200B;**[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**。
         1. 在畫素列中，按一下&#x200B;**[!UICONTROL edit]**。
         1. 視需要複製[!UICONTROL HTML Tag]和[!UICONTROL Flash Tag]欄位中的值，以提供給廣告商或網站連絡人。

            廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。
   1. 按一下&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL 3rd-party Fees]：** （選用）要以每1000次曝光的不可記帳成本追蹤的靜態第三方費率。 若適用，套裝程式層級預設會自動套用至新位置，除非您輸入其他值。

>[!NOTE]
>
>可記帳費用會反映在[!UICONTROL Net CPM]量度中。

>[!MORELIKETHIS]
>
>* [關於位置管理](placement-about.md)
>* [建立位置](placement-create.md)
>* [編輯版位](placement-edit.md)
>* [管理刊登版位的競標乘數](placement-manage-bid-multipliers.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [鍵盤快速鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* 有關Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)的[常見問題集
