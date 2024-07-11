---
title: 封裝設定
description: 請參閱可用封裝設定的說明。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 9a7d73a281dba1331f00dd9ff75fafdc057413d0
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# 封裝設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]：** 封裝名稱。 長度上限為60個字元。

**[!UICONTROL Description]：** （選用）封裝的說明。

**[!UICONTROL 3rd Party Billed Fees]：** （選用）要以不可開立帳單成本追蹤的靜態第三方費用：

* **[!UICONTROL CPM]：** 每1000次曝光的成本(CPM)。

* **[!UICONTROL Description]：** CPM費用的說明。

>[!NOTE]
>
>可記帳費用會反映在 [!UICONTROL Net CPM] 量度。

您可以在以下位置覆寫套件層級設定： [位置層級](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]：** （現有套裝程式的唯讀）套裝程式中位置間距和上限的層級：

* **[!UICONTROL Package level pacing]：** 此步調策略的運作方式是透過為所有包含的版位設定步調和上限，如 *群組*. 此策略可確保指定封裝內的所有版位都經過整體最佳化，根據效能和規模將支出分配到選定的關鍵效能指標(KPI)。

* **[!UICONTROL Placement level pacing]：**  此步調策略的運作方式是透過為所有包含的位置設定步調和上限 *個別*. 最佳實務是僅將此策略用於執行保證的私人市場交易。

**[!UICONTROL Flight Dates]：** 套件的整體開始日期和結束日期。 投放日期必須包含在行銷活動投放日期中。

>[!NOTE]
>
>* 指派給此封裝的所有刊登版位的投放日期必須包含在這些日期中。
> * 啟用自訂照明時，您無法編輯封裝開始日期。

**[!UICONTROL *Activate Custom Flighting]：** 可讓您在中為套件建立非偶數步調航班 [!UICONTROL Flighting] 一節。 啟用自訂燈光並儲存封裝後，您就無法停用自訂燈光或編輯封裝開始日期。

**[!UICONTROL Budget]：** （僅具有套件層級步調的套件）總預算上限和預算間隔。

對於具有自訂飛行的套件，預算間隔一律為 *[!UICONTROL All time]*. 對於沒有自訂燈光的封裝，請指定預算間隔： *[!UICONTROL All time]，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]：** （僅具有套件層級步調和動態利潤管理的套件）套件期間的毛預算上限。

**[!UICONTROL Optimization Goal]：** （僅具有套件層級步調的套件）套件的最佳化目標。 如需各個最佳化目標的說明，請參閱： [最佳化目標及使用方式](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]：** (具有&quot;[!UICONTROL Highest Return on Ad Spend]「和」[!UICONTROL Lowest Cost per Acquisition]「僅限最佳化目標) A [自訂目標](/help/dsp/optimization/custom-goal.md) 包括用來計算CPA或ROAS量度的收入或轉換事件。 自訂目標可選擇性地包含其他加權的上層漏斗事件（例如頁面造訪和購物車新增），以用於除了封裝最佳化的CPA或ROAS量度之外的其他用途。 如需自訂目標的詳細資訊，包括建立自訂目標的最佳實務，以及使用這些目標的促銷活動，請參閱&quot;[自訂目標](/help/dsp/optimization/custom-goal.md)「和」[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md).」<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]：** (選用；套件包含&quot;[!UICONTROL Highest Return on Ad Spend]「和」[!UICONTROL Lowest Cost per Acquisition]「僅限最佳化目標)告訴最佳化模型只從點選型轉換學習。 否則，最佳化模型會同時學習點按和曝光轉換的機制。

**[!UICONTROL Conversion Metric]：** (選用；套件包含&quot;[!UICONTROL Highest Return on Ad Spend]「和」[!UICONTROL Lowest Cost per Acquisition]「僅限最佳化目標)最終轉換事件（例如註冊）或收入事件/銷售金額（例如購買和購買值），用於計算廣告支出回報或每次收購成本。 從對應至所選自訂目標的所有主要事件（「目標量度」）清單中選取。 如果清單是空的，請編輯自訂目標，以納入至少一個基礎事件作為目標量度。

**[!UICONTROL Package Goal Type]：** （僅具有自訂最佳化目標的套件）套件的用途。 此設定有助於判斷如何最佳化套件：

* *[!UICONTROL Prospecting]：* 潛在客戶套件著重於爭取新客戶。

* *[!UICONTROL Retargeting]：* 重新目標定位套件著重於重新公開先前的訪客或客戶。

* *[!UICONTROL Other]：* 所有其他用途。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]：** （僅限具有自訂最佳化目標的套件）其歷史資料會作為最佳化套件的輸入的其他套件。

**[!UICONTROL Target]：** （僅限具有套件層級步調的套件）目標目標，用於追蹤效能。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Frequency Cap]：** （僅限具有套件層級步調的套件）不重複裝置、通用ID或人員(視指定的 [!UICONTROL Cross Device Level] 用於行銷活動和版位的 [!UICONTROL Targeting] 設定)，即可從套件中提供廣告。 選項包括 *[!UICONTROL Unlimited]* 或每日、周或月的特定金額。

>[!NOTE]
>
>* 您可以在行銷活動、封裝和位置層級設定頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。
>* 最佳實務是在封裝層級設定潛在客戶與重新目標定位的頻率上限。
> * 較高的頻率上限會導致較高的花費和印象，但觸及率較低。 較低的頻率上限會導致較低的花費和曝光數，但觸及率較高。

**[!UICONTROL Pace on]：** （僅限套件層級步調的套件）步調基準：

* *[!UICONTROL Budget]：* （預設）此選項會在配置的套件預算內儘可能多地提供曝光數。

* *[!UICONTROL Impressions]：* 此選項會傳送曝光次數，直到在指定間隔內達到指定數量為止。 選取此選項時，請指定曝光次數和間隔： *所有時間，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]：** （僅具有套件層級步調的套件）如何在整個航班上調整廣告傳送的步調：

* *[!UICONTROL Even]：* 每個航班的傳送進度都相同，目標為上半段航班的50%傳送。

* *[!UICONTROL Slightly Ahead]：* （預設）加速傳遞，使其在飛行期間的中途完成55-65%。

* *[!UICONTROL Frontload]：* 加速傳遞，讓整個行程完成65-75%。

* *[!UICONTROL Aggressive Frontload]：* 加速傳遞，讓整個行程完成75-85%。

**[!UICONTROL Intraday pacing]：** （僅含套件層級步調的套件）如何在飛行中每天進行廣告投放步調：

* *[!UICONTROL Even]：* （預設）根據存貨可用性調整交貨規模。 一般而言，拍賣量較大時，白天每小時會傳送更多廣告，而早上和晚上傳送的廣告會較少。

* *[!UICONTROL ASAP]：* 將傳送速度加快一倍 *平均*.

  >[!CAUTION]
  >
  >此選項可能對效能造成負面影響。 只有在您完全排定傳送的優先順序，且花費在效能最佳化上時，才使用它。

## [!UICONTROL Flighting]

（具有套件層級步調的套件）套件的投放期間，包括整體中的任何自訂投放期間 [!UICONTROL Flight Dates] 適用於此套件。 您只能在下列情況下設定自訂航班： [!UICONTROL Activate Custom Flighting] 選項已啟用於 [!UICONTROL Goals & Budget] 區段。

**[!DNL Flight N]：** (僅適用於 [!UICONTROL Activate Custom Flighting] 選項已啟用)針對每個航班，指定開始日期、結束日期以及目標支出目標。 若要新增其他航班，請按一下 **[!UICONTROL Add Flight]**.

對於現有的套裝程式，您可以選擇在 [!UICONTROL Rollover] 欄中列出的任何航班，可將潛在的未花費預算新增至下一個航班。 中的投影值 [!UICONTROL Adjusted Goal (Goal + Rollover)] 欄會隨之變更。<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [關於封裝管理](package-about.md)
>* [建立封裝](package-create.md)
>* [編輯套裝](package-edit.md)
>* [將位置附加至封裝](package-attach-placement.md)
>* [檢視封裝的變更記錄](package-change-log.md)
>* [Campaign Management常見問題集](/help/dsp/campaign-management/faq-campaign-management.md)
