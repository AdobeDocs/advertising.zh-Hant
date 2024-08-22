---
title: 使用試算表檢閱和編輯封裝設定
description: 瞭解如何使用試算表檢閱和編輯重要套件設定。
feature: DSP Packages
source-git-commit: ad00092c4ef5d44c364ab0593826220054f715c3
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# 使用試算表檢閱和編輯封裝設定

您可以以XLSX （[!DNL Microsoft Excel]試算表）格式下載一或多個套件的設定以供檢閱。 試算表內含獨立的索引標籤，內含航班資訊。 然後，您可以進行變更以選取兩個標籤中的欄位，並一次將資料上傳回DSP。 可編輯欄位包含大部分通常可編輯的設定。

>[!TIP]
>
>若要編輯一或多個套件的多個欄位，請參閱&quot;[編輯套裝](/help/dsp/campaign-management/packages/package-edit.md)&quot;。

## 一或多個套件的下載設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下&#x200B;**[!UICONTROL Packages]**。

1. 選取您要下載其設定的每個封裝旁的核取方塊。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**。

檔案會自動儲存至瀏覽器的「下載」資料夾。 如需所包含欄的清單，請參閱[已下載/已上傳試算表中的封裝欄](#qa-sheet-columns-packages)。

## 上傳一個或多個套件的設定

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下&#x200B;**[!UICONTROL Packages]**。

1. 選取每個要上傳其設定的封裝旁的核取方塊。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**。

1. 在[!UICONTROL Edit in Excel]對話方塊：

   1. 將檔案拖放至方塊中，或按一下方塊內部，從您的裝置或網路選取檔案。

   1. 按一下&#x200B;**[!UICONTROL Upload]**。

1. （選擇性）若要確認已處理更新，請按一下頂端功能表列右側的![工作](/help/dsp/assets/downloads.png)。

## 套件設定已下載/已上傳試算表中的欄{#qa-sheet-columns-packages}

>[!TIP]
>
> 在下載的試算表中，所有可編輯的欄都會以藍色反白顯示。

### [!UICONTROL Package]索引標籤

| 章節 | 欄 | 說明 | 可編輯嗎？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | 套件的數值ID。 | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | 封裝的名稱。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL Status] | 封裝狀態： *[!UICONTROL active]*&#x200B;或&#x200B;*[!UICONTROL inactive]*。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL Description] | 套件的說明（選用）。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | 要以每1000次曝光的不可記帳成本追蹤的靜態第三方費用率（如適用）。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | 第三方費用比率的選擇性說明（如適用）。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | 封裝的開始日期。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | 封裝的結束日期。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | 封裝中要放置和限制位置的層級： *[!UICONTROL Package]*&#x200B;或&#x200B;*[!UICONTROL Placement]*。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | 套件預算。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | 預算間隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | 選擇性預算間隔上限。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | 選擇性預算間隔上限的間隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | 套件的目標。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | 目標的目標值。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | （僅具有&quot;[!UICONTROL Highest Return on Ad Spend]&quot;和&quot;[!UICONTROL Lowest Cost per Acquisition]&quot;最佳化目標的套件）包含用於計算CPA或ROAS量度的收入或轉換事件的[自訂目標](/help/dsp/optimization/custom-goal.md)。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | （選用；僅具有最佳化目標「[!UICONTROL Highest Return on Ad Spend]」和「[!UICONTROL Lowest Cost per Acquisition]」的套件）最終轉換事件或收入事件/銷售金額，用於計算廣告支出回報或每次收購成本。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | （僅限具有自訂最佳化目標的封裝）封裝的目的，有助於判斷如何最佳化封裝： *[!UICONTROL Prospecting]*、*[!UICONTROL Retargeting]*&#x200B;或&#x200B;*[!UICONTROL Other]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | （僅限具有自訂最佳化目標的套件）另一個套件的套件ID，其歷史資料會用作最佳化套件的輸入。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | （僅限具有自訂最佳化目標的套件）其歷史資料會作為最佳化套件的輸入的其他套件。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | 套件是否朝著&#x200B;*[!UICONTROL budget]*&#x200B;或&#x200B;*[!UICONTROL primary_goal]*&#x200B;步調（針對曝光數）。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | （當您在曝光數上調整封裝時）指定時間間隔內的目標曝光數。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | （當您在曝光數上排列封裝時）目標曝光數的時間間隔。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | 封裝的航班步調策略： *[!UICONTROL Even]*、*[!UICONTROL slightly ahead]*、*[!UICONTROL frontload]*&#x200B;或&#x200B;*[!UICONTROL aggressive frontload]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | 封裝的當天步調策略： *[!UICONTROL Even]*&#x200B;或&#x200B;*[!UICONTROL ASAP]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | 在指定的[!UICONTROL Frequency Cap Interval]期間封裝的主要頻率上限。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | 主要頻率上限的間隔： *[!UICONTROL Day]*、*[!UICONTROL Week]*&#x200B;或&#x200B;*[!UICONTROL Month]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | 主要[!UICONTROL Frequency Cap]適用的周數、天數、小時數或分鐘數。 例如，如果主要上限是每月12次曝光，則這裡的值將是`12`。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | 在指定的[!UICONTROL Secondary Frequency Cap Interval]期間封裝的次要頻率上限 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | 次要頻率上限的間隔型別： *[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*&#x200B;或&#x200B;*[!UICONTROL Minute]*。 [!UICONTROL Secondary Frequency Cap Interval Value]會指出適用的周數、天數、小時數或分鐘數。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]適用的周數、天數、小時或分鐘。 例如，如果次要曝光次數上限為每六小時三次曝光，則這裡的值將是`6`。 | 是 |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | 是否要為套件&#x200B;*T* (true)或&#x200B;*F* (false)建立非偶數步調航班。 啟用自訂燈光並儲存封裝後，您就無法停用自訂燈光或編輯封裝開始日期。 | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | （只有啟用[!UICONTROL Activate Custom Flighting]選項時才能使用）是否要將上一個航班的任何剩餘預算自動新增到下一個航班的現有預算： *T* (true)或&#x200B;*F* (false)。 | 是 |
| [!UICONTROL Error] | [!UICONTROL Error] | 任何相關錯誤。 | — |

### [!UICONTROL Package_Flights]索引標籤

| 章節 | 欄 | 說明 | 可編輯嗎？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | 套件的數值ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | 航班的數值ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | 航班的第一個日期。 | 是 |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | 航班的最後日期。 | 是 |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | 航班的目標支出目標。 | 是 |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | （未啟用&quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot;選項的現有套件）要新增至下一個航班的潛在未花費預算金額。 | 是 |

>[!MORELIKETHIS]
>
>* [編輯封裝](/help/dsp/campaign-management/packages/package-edit.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
