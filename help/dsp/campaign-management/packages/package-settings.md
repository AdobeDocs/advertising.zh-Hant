---
title: 封裝設定
description: 請參閱可用封裝設定的說明。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: ab3118901b7cd88776f7c0ce8038b928118a7555
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# 封裝設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]：**&#x200B;封裝名稱。 長度上限為60個字元。

**[!UICONTROL Description]：** （選擇性）封裝的說明。

**[!UICONTROL 3rd Party Billed Fees]：** （選擇性）要作為不可記帳成本追蹤的靜態協力廠商費用：

* **[!UICONTROL CPM]：**&#x200B;每1000次曝光的成本(CPM)。

* **[!UICONTROL Description]：** CPM費用的說明。

>[!NOTE]
>
>可記帳費用會反映在[!UICONTROL Net CPM]量度中。

您可以在[位置層級](/help/dsp/campaign-management/placements/placement-settings.md)覆寫封裝層級設定。

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]：** （現有封裝為唯讀）封裝中要放置和限制位置的層級：

* **[!UICONTROL Package level pacing]：**&#x200B;此步調策略的運作方式是以&#x200B;*群組*&#x200B;的形式來步調及限定所有包含的版位。 此策略可確保指定封裝內的所有版位都經過整體最佳化，根據效能和規模將支出分配到選定的關鍵效能指標(KPI)。

* **[!UICONTROL Placement level pacing]：**&#x200B;此步調策略的運作方式是依步調及限定所有包含的版位&#x200B;*個別*。 最佳實務是僅將此策略用於執行保證的私人市場交易。

**[!UICONTROL Flight Dates]：**&#x200B;封裝的整體開始日期和結束日期。 投放日期必須包含在行銷活動投放日期中。

>[!NOTE]
>
>* 指派給此封裝的所有刊登版位的投放日期必須包含在這些日期中。
> * 啟用自訂照明時，您無法編輯封裝開始日期。

**[!UICONTROL Activate Custom Flighting]：**&#x200B;可讓您在下方[!UICONTROL Flighting]區段中建立封裝的非偶數步調航班。 啟用自訂燈光並儲存封裝後，您就無法停用自訂燈光或編輯封裝開始日期。

**[!UICONTROL Budget]：** （僅具有封裝層級步調的封裝）總預算上限和預算間隔。

對於具有自訂訊號的封裝，預算間隔一律為&#x200B;*[!UICONTROL All time]*。 對於沒有自訂燈光的封裝，請指定預算間隔： *[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Gross Budget]：** （僅具有封裝層級步調與動態利潤管理的封裝）封裝期間的毛預算上限。

**[!UICONTROL Optimization Goal]：** （僅具有封裝層級步調的封裝）封裝的最佳化目標。 在[最佳化目標及使用方式](/help/dsp/optimization/optimization-goals.md)檢視每個最佳化目標的說明。

**[!UICONTROL Custom Goal for Model Learning]：** （僅具有&quot;[!UICONTROL Highest Return on Ad Spend]&quot;和&quot;[!UICONTROL Lowest Cost per Acquisition]&quot;最佳化目標的套件）包含用來計算CPA或ROAS量度的收入或轉換事件的[自訂目標](/help/dsp/optimization/custom-goal.md)。 自訂目標可選擇性地包含其他加權的上層漏斗事件（例如頁面造訪和購物車新增），以用於除了封裝最佳化的CPA或ROAS量度之外的其他用途。 如需自訂目標的詳細資訊，包括建立自訂目標的最佳實務和使用這些目標的行銷活動，請參閱&quot;[自訂目標](/help/dsp/optimization/custom-goal.md)&quot;和&quot;[設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]：** （選擇性；僅具有&quot;[!UICONTROL Highest Return on Ad Spend]&quot;和&quot;[!UICONTROL Lowest Cost per Acquisition]&quot;最佳化目標的套件）告訴最佳化模型只從點按式轉換中學習。 否則，最佳化模型會同時學習點按和曝光轉換的機制。

**[!UICONTROL Conversion Metric]：** （選擇性；僅套件具有&quot;[!UICONTROL Highest Return on Ad Spend]&quot;和&quot;[!UICONTROL Lowest Cost per Acquisition]&quot;最佳化目標）最終轉換事件（例如註冊）或收入事件/銷售金額（例如購買和購買值），用於計算廣告支出回報或每次收購成本。 從對應至所選自訂目標的所有主要事件（「目標量度」）清單中選取。 如果清單是空的，請編輯自訂目標，以納入至少一個基礎事件作為目標量度。

**[!UICONTROL Package Goal Type]：** （僅具有自訂最佳化目標的封裝）封裝的目的。 此設定有助於判斷如何最佳化套件：

* *[!UICONTROL Prospecting]：*&#x200B;潛在客戶套件著重於取得新客戶。

* *[!UICONTROL Retargeting]：*&#x200B;重新目標定位套件著重於重新公開先前的訪客或客戶。

* *[!UICONTROL Other]：*&#x200B;所有其他用途。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]：** （僅具有自訂最佳化目標的套件）另一個套件，其歷史資料已用來作為最佳化套件的輸入。

**[!UICONTROL Target]：** （僅具有封裝層級步調的封裝）用來追蹤效能的目標目標。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Frequency Cap]：** （僅具有套件層級步調的套件）可從套件提供不重複裝置、通用ID或人員（取決於為行銷活動指定的[!UICONTROL Cross Device Level]和位置的[!UICONTROL Targeting]設定）的廣告次數。 選項包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每日、每週或每月的特定金額。

>[!NOTE]
>
>* 您可以在行銷活動、封裝和位置層級設定頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。
>* 最佳實務是在封裝層級設定潛在客戶與重新目標定位的頻率上限。
> * 較高的頻率上限會導致較高的花費和印象，但觸及率較低。 較低的頻率上限會導致較低的花費和曝光數，但觸及率較高。

**[!UICONTROL Pace on]：** （僅包含封裝層級步調的封裝）步調所根據的封裝：

* *[!UICONTROL Budget]：* （預設）此選項會在配置的套件預算內儘可能多地提供曝光數。

* *[!UICONTROL Impressions]：*&#x200B;此選項會傳送曝光數，直到在指定的間隔內達到指定的數量為止。 選取此選項時，請指定曝光次數和間隔： *所有時間，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Flight pacing]：** （僅具有封裝層級步調的封裝）如何在整個航班上調整廣告傳送的步調：

* *[!UICONTROL Even]：*&#x200B;在每個航班上均勻地安排傳遞，目標是在航班的前半段傳遞50%的傳遞。

* *[!UICONTROL Slightly Ahead]：* （預設）加速傳遞，使其在飛行期間的中途完成55-65%。

* *[!UICONTROL Frontload]：*&#x200B;加速傳遞，使其在飛行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：*&#x200B;加速傳遞，使其在飛行中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （僅具有封裝層級步調的封裝）如何在航班內的每一天安排廣告傳送的步調：

* *[!UICONTROL Even]：* （預設）根據庫存可用性調整傳遞。 一般而言，拍賣量較大時，白天每小時會傳送更多廣告，而早上和晚上傳送的廣告會較少。

* *[!UICONTROL ASAP]：*&#x200B;將傳遞速度加速到&#x200B;*平均*&#x200B;的兩倍。

  >[!CAUTION]
  >
  >此選項可能對效能造成負面影響。 只有在您完全排定傳送的優先順序，且花費在效能最佳化上時，才使用它。

## [!UICONTROL Flighting]

（具有套件層級步調的套件）套件的投放期間，包括套件整體[!UICONTROL Flight Dates]內的任何自訂投放期間。 您必須在[!UICONTROL Goals & Budget]區段中啟用[!UICONTROL Activate Custom Flighting]選項，才能設定自訂航班。

**[!DNL Flight N]：** （僅在啟用[!UICONTROL Activate Custom Flighting]選項時可用）針對每個航班，指定開始日期、結束日期以及目標支出目標。 若要新增其他航班，請按一下&#x200B;**[!UICONTROL Add Flight]**。

對於現有的套件，您可以選擇在任何航班的[!UICONTROL Rollover]欄中輸入值，以將潛在的未花費預算新增到下一個航班。 [!UICONTROL Adjusted Goal (Goal + Rollover)]資料行中的投影值已相應變更。<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [關於封裝管理](package-about.md)
>* [建立封裝](package-create.md)
>* [編輯封裝](package-edit.md)
>* [將位置附加至封裝](package-attach-placement.md)
>* [檢視封裝的變更記錄](package-change-log.md)
>* 有關Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)的[常見問題集
