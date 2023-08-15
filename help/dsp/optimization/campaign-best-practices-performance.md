---
title: 設定效能行銷活動的最佳實務
description: 瞭解設定以效能為中心的行銷活動的最佳實務，包括針對最低CPA或最高ROAS最佳化的位置。
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: eda0459472c1e4a8297daf69454de0fcb3d4f8ca
workflow-type: tm+mt
source-wordcount: '1255'
ht-degree: 0%

---

# 設定效能行銷活動的最佳實務

DSP可以針對具有最低每次收購成本(CPA)或最高廣告投資報酬率(ROAS)的刊登版位，最佳化以效能為中心的行銷活動。

請參閱下列效能行銷活動的最佳實務：

* 步驟1 — 定義目標
* 步驟2 — 定義策略
* 步驟3 — 建立套件
* 步驟4 — 建立位置結構
* 步驟5 — 使用正確的創意資產

## 步驟1 — 定義您的目標

瞭解行銷活動的目標很重要，例如達成最高可能的ROAS或最低可能的CPA。 績效行銷活動具有 [最佳化目標](/help/dsp/optimization/optimization-goals.md) 結尾為&quot;[!UICONTROL - Custom Goal]&quot; (例如&quot;[!UICONTROL Highest ROAS - Custom Goal]「)。 對於行銷活動中的每個套件，您將會相應地指定目標目標。

![最佳化目標](/help/dsp/assets/optimization-goals.png)

您也需要判斷導致整體目標的成功事件，並據此建立自訂目標。 對於每個套件，您將指定自訂目標，以搭配報告和演演算法最佳化的整體最佳化目標使用 [!DNL Adobe Sensei]. 如需建立自訂目標的詳細資訊，請參閱 [建立自訂目標的最佳實務](custom-goal-best-practices.md).

![自訂目標](/help/dsp/assets/objective-goals.png)

## 步驟2 — 定義策略

### 潛在客戶策略

上層漏斗套件包含具有非常廣泛目標定位的位置，以觸及淨新消費者。

#### 建議的潛在客戶放置策略

* 使用下列策略尋找可能轉換的新對象：

   * 從資料管理平台(DMP) (例如Adobe Audience Manager)進行相似建模。
   * 使用第三方資料的行為目標定位。
   * 內容鎖定。
   * 網站/類別目標定位。

* 使用執行網路(RON)鎖定目標：一定要包含執行網路放置而不使用對象鎖定目標，以及廣泛的詳細目錄鎖定目標。 這允許 [!DNL Adobe Sensei] 此演演算法可尋找有價值的使用者，這些使用者可能擁有尚未分類到受眾的較新Cookie。

### 重新目標定位策略

下層漏斗套件包括定位已造訪過廣告商網頁或廣告商擁有CRM資料之使用者的位置。

#### 重新目標定位的建議放置策略

* 如果廣告商為Adobe Analytics或Adobe Audience Manager客戶，您就可以建立第一方區段（例如首頁訪客、產品頁面或購物車放棄者），並將他們用作DSP中的位置目標。

* 避免針對以對象為目標的位置指派過多預算。 一般來說，每個月每1,000位使用者預算為$30。

## 步驟3 — 建立套件

最佳實務是建立個別套件，以用於上層漏斗的探勘和下層漏斗的重新目標定位。 最佳化會在封裝層級進行，因此封裝內所有位置的效能資料都會集中在一起。 因此，請將位置分組到具有類似預期效能的套件中。

![用於探索和重新定位的獨立套件範例](/help/dsp/assets/p-r.png)

此外，請使用下列設定。

### 目標與預算

* **步調和上限：** 若要選取CPA或ROAS最佳化目標，套件必須使用套件層級的步調。 這可確保套件中的所有版位都已最佳化，以根據效能和規模分配支出至所選的目標。

* **投放日期：** （潛在客戶套件）當行銷活動執行超過25天時，請使用 [!UICONTROL Activate Custom Flighting] 功能。 首先，將前10天的自訂航班設定為所需每日預算的大約75%，以減少 *學習階段*. 然後，為剩餘預算設定第二個自訂航班。

  例如，如果您在30天內有$100,000的支出，則請將「航班1」（第1-10天）的預算設定為$25,000 （75% x $100,000/30天=每天$2,500）。 使用剩餘預算$75,000用於「航班2」（第11至30天）。

* **預算：** DSP一律會嘗試將100%的套件預算平均分配給套件中的所有版位。 如果刊登版位花費很少或沒有支出，我們建議為刊登版位設定預算上限，以允許更多預算依規模分配給刊登版位。 允許24到48小時校準預算變更。

* **最佳化目標：** 使用兩個效能最佳化目標之一， *[!UICONTROL Highest ROAS]* 或 *[!UICONTROL Lowest CPA]*，視套件目標而定。 這些目標會分別針對最高ROAS或最低CPA位置自動最佳化套件。

* **自訂目標：**
   * 如果新封裝與現有封裝具有相同的目標，您可以選擇連結現有封裝，讓演演算法可以使用現有的機器學習資料。
   * 輸入適當的 [!UICONTROL Target CPA] 或 [!UICONTROL Target ROAS].

* **Flight步調和Intraday步調：** 對於兩種型別的步調，選擇 *[!UICONTROL Even]* 藉由在每一天和整個飛行中均一的步調，將您的效能目標最大化。

  >[!CAUTION]
  >
  >使用 *[!UICONTROL FrontLoad]* 和 *[!UICONTROL Aggressive Front Load]* 適用於飛行步調和 *[!UICONTROL ASAP]* 只有當您將傳送和支出完全排在效能最佳化之前，才設定當天步調的步調，因為這些策略可能會對您想要的效能KPI產生負面影響。

## 步驟4 — 建立位置結構

越少越好。 如果您在每個套件中設定的版位少於六個，則可用的預算可以最輕鬆地動態轉移到績效最佳的版位。

此外，請務必將每個位置新增至套件目標型別為 *[!UICONTROL Prospecting]* 或 *[!UICONTROL Retargeting]*，視情況而定。

以下是建議用於效能行銷活動的版位設定。

### 目標

您將在封裝層級設定CPA或ROAS最佳化（請參閱步驟3 — 建立封裝），但您可以新增其他位置層級設定。

* **最高出價：**
   * 對於潛在客戶位置，請使用最低最高出價($5)。
   * 若是重新定位版位，請使用最高出價($12)。

* **競標前篩選：** 最小化或最好避免設定激進的競標前篩選器，這會使位置無法達到規模。 最佳作法包括下列各項：

   * 每個位置使用一(1)個競標前篩選器。 多個競標前篩選器需要同時符合兩個條件，這會減少規模。

   * 若套用了其他鎖定目標（例如對象、地理和網站鎖定目標），請考慮設定較寬鬆的競標前篩選器。

如需各個競標前篩選器的使用時機的說明，請參閱： [位置層級競標前篩選器及其使用方式](/help/dsp/optimization/optimization-pre-bid-filters.md).

### 詳細目錄

若要最大化規模，請使用 [!UICONTROL Public] （開啟Exchange）和 [!UICONTROL On Demand] 詳細目錄。

### 網站目標定位

* **[!UICONTROL Traffic Type]**： [!UICONTROL Websites] 僅限
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### 對象目標定位

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * 對於潛在位置，請將類似的對象類別和類似的對象大小分組到一個位置中。 然後，根據效能，執行下列任一項作業：
      * 從現有版位中移除表現不佳的對象。
      * 將表現最佳的對象移至另一個位置，以更能控制預算。
   * 若要重新定位位置，您最好在每個位置包含一個對象區段，以輕鬆控制競標和預算。

>[!NOTE]
>
>如果使用者只能透過一個位置聯絡，您的廣告將會表現最好。 使用者在各個位置之間大幅重疊可能會導致競爭，進而產生持續增加出價的週期，從而提高每位使用者的成本。 因此，如果您包含多個對象，請確定這些對象並非由重疊的使用者/對象成員組成。
>
> 您可以在層級中建立您的對象，以避免重疊的對象，如此一來，您就可以視需求在位置中隱藏更高、包含性更強的層。

* **[!UICONTROL Frequency Capping]:**
   * 對於潛在位置，請使用嚴格的頻率上限（每天一次曝光）。
   * 對於重新定位版位，請將主要版位上限設定為每天6-10次曝光次數，並將次要版位上限設定為每小時一次曝光次數。

* **[!UICONTROL Device Targeting]**:
   * 包含 [!UICONTROL Computer]， [!UICONTROL Mobile]、和 [!UICONTROL Tablet].
   * 不要鎖定目標 [!UICONTROL Firefox] 和 [!UICONTROL Safari] 因為鎖定目標和測量限制。 請聯絡您的Adobe客戶團隊，以取得更多關於 [!DNL Adobe] 支援 [!DNL Safari ITP].
   * 如果您鎖定行動網站流量，請停用除外的所有行動瀏覽器 [!UICONTROL Chrome] 和 [!UICONTROL Edge].

### 品牌安全與媒體品質

使用內容篩選、競標前詐騙封鎖，及/或 [!UICONTROL Ads.txt] 篩選會限制您的刊登版位規模，但必要時可加以使用。

## 步驟5 — 使用正確的創意資產

* 最佳實務是納入儘可能多的獨特廣告大小，以最大化觸及率。 通用顯示範本可讓您上傳任何標準顯示廣告大小。
* 請確定所有版位都包含 *至少* 所有主要顯示廣告大小（300x250、728x90、160x600、300x600、320x50及300x50）。
* 經常更新創意內容以防止創意疲勞。

>[!MORELIKETHIS]
>
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [位置層級競標前篩選器及其使用方式](optimization-pre-bid-filters.md)
>* [行銷活動啟動檢查清單](/help/dsp/campaign-management/campaign-launch-checklist.md)
