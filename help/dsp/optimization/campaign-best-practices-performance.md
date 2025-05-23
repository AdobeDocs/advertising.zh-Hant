---
title: 設定效能行銷活動的最佳實務
description: 瞭解設定以效能為中心的行銷活動的最佳實務，包括針對最低CPA或最高ROAS最佳化的位置。
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# 設定效能行銷活動的最佳實務

DSP可最佳化以效能為中心的行銷活動。 請參閱下列效能行銷活動的最佳實務：

* 步驟1 — 定義目標
* 步驟2 — 定義策略
* 步驟3 — 建立套件
* 步驟4 — 建立位置結構
* 步驟5 — 使用正確的Creative Assets

## 步驟1 — 定義您的目標

瞭解行銷活動的目標很重要，例如達成最高可能的ROAS或最低可能的CPA。 效能行銷活動具有[最佳化目標](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;。 請為行銷活動中的每個套件相應地指定最佳化目標。

![最佳化目標](/help/dsp/assets/optimization-goals.png)

您也需要判斷導致整體目標的成功事件，並據此建立自訂目標。 針對每個封裝，指定要與整體最佳化目標搭配使用的自訂目標，以使用[!DNL Adobe Sensei]進行報告和演演算法最佳化。 如需建立自訂目標（包括最佳實務）的詳細資訊，請參閱[自訂目標](custom-goal.md)。

## 步驟2 — 定義策略

### 潛在客戶策略

上層漏斗套件包含具有非常廣泛目標定位的位置，以觸及淨新消費者。

#### 建議的潛在客戶放置策略

* 使用下列策略尋找可能轉換的新對象：

   * 從資料管理平台(DMP) (例如Adobe Audience Manager)進行相似建模。
   * 使用第三方資料的行為目標定位。
   * 內容鎖定。
   * 網站/類別目標定位。

* 使用執行網路(RON)鎖定目標：一定要包含執行網路放置而不使用對象鎖定目標，以及廣泛的詳細目錄鎖定目標。 這可讓[!DNL Adobe Sensei]演演算法找出有價值的使用者，這些使用者可能擁有尚未分類到受眾的較新Cookie。

### 重新目標定位策略

下層漏斗套件包括定位已造訪過廣告商網頁或廣告商擁有CRM資料之使用者的位置。

#### 重新目標定位的建議放置策略

* 如果廣告商為Adobe Analytics或Adobe Audience Manager客戶，您就可以建立第一方區段（例如首頁訪客、產品頁面或購物車放棄者），並將他們用作DSP中的位置目標。

* 避免針對以對象為目標的位置指派過多預算。 一般來說，每個月每1,000位使用者預算為$30。

## 步驟3 — 建立套件

最佳實務是建立個別套件，以用於上層漏斗的探勘和下層漏斗的重新目標定位。 最佳化會在封裝層級進行，因此封裝內所有位置的效能資料都會集中在一起。 因此，請將位置分組到具有類似預期效能的套件中。

![個別封裝的範例，用於尋找及重新目標定位](/help/dsp/assets/p-r.png)

此外，請使用下列設定。

### 目標與預算

* **步調和上限：**&#x200B;若要選取CPA或ROAS最佳化目標，封裝必須使用封裝層級的步調。 這可確保套件中的所有版位都已最佳化，以根據效能和規模分配支出至所選的目標。

* **投放日期：** （潛在客戶套件）當您的行銷活動執行超過25天時，請使用[!UICONTROL Activate Custom Flighting]功能。 首先，將前10天的自訂航班設定為所需每日預算的大約75%，以減少&#x200B;*學習階段*&#x200B;期間的支出。 然後，為剩餘預算設定第二個自訂航班。

  例如，如果您在30天內有$100,000的支出，則請將「航班1」（第1-10天）的預算設定為$25,000 （75% x $100,000/30天=每天$2,500）。 使用剩餘預算$75,000用於「航班2」（第11至30天）。

* **預算：** DSP一律會嘗試將100%的套件預算平均分配給封裝中的所有位置。 如果刊登版位花費很少或沒有支出，我們建議為刊登版位設定預算上限，以允許更多預算依規模分配給刊登版位。 允許24到48小時校準預算變更。

* **最佳化目標：**&#x200B;根據封裝目標，使用兩個效能最佳化目標之一： *[!UICONTROL Highest Return on Ad Spend]*&#x200B;或&#x200B;*[!UICONTROL Lowest Cost per Acquisition]*。 這些目標會分別針對最高ROAS或最低CPA位置自動最佳化套件。

* **自訂目標：**
   * 如果新封裝與現有封裝具有相同的目標，您可以選擇連結現有封裝，讓演演算法可以使用現有的機器學習資料。
   * 輸入適當的[!UICONTROL Target CPA]或[!UICONTROL Target ROAS]。

* **Flight Pacing和Intraday Pacing：**&#x200B;針對這兩種型別的步調，選取&#x200B;*[!UICONTROL Even]*，透過在每一天和整個飛行期間都統一步調，將您的效能目標最大化。

  >[!CAUTION]
  >
  >僅當您完全排定傳遞的優先順序並花費超過效能最佳化時，才使用&#x200B;*[!UICONTROL FrontLoad]*&#x200B;和&#x200B;*[!UICONTROL Aggressive Front Load]*&#x200B;進行航班步調和&#x200B;*[!UICONTROL ASAP]*&#x200B;進行當天步調，因為這些策略可能會對您想要的效能KPI產生負面影響。

## 步驟4 — 建立位置結構

越少越好。 如果您在每個套件中設定的版位少於六個，則可用的預算可以最輕鬆地動態轉移到績效最佳的版位。

此外，請務必視情況將每個位置新增至封裝目標型別為&#x200B;*[!UICONTROL Prospecting]*&#x200B;或&#x200B;*[!UICONTROL Retargeting]*&#x200B;的封裝。

以下是建議用於效能行銷活動的版位設定。

### 目標

您必須在套件層級設定CPA或ROAS最佳化（請參閱步驟3 — 建立套件），但您可以新增其他位置層級設定。

* **最高出價：**
   * 對於潛在客戶位置，請使用最低最高出價($5)。
   * 若是重新定位版位，請使用最高出價($12)。

* **競標前篩選條件：**&#x200B;最小化或最好避免設定嚴格的競標前篩選條件，以防止位置達到規模。 最佳作法包括下列各項：

   * 每個位置使用一(1)個競標前篩選器。 使用多個競標前篩選器需要同時符合兩個條件，這會減少規模。

   * 若套用了其他鎖定目標（例如對象、地理和網站鎖定目標），請考慮設定較寬鬆的競標前篩選器。

檢視何時在[位置層級競標前篩選器中使用每個競標前篩選器的說明，以及如何使用它們](/help/dsp/optimization/optimization-pre-bid-filters.md)。

### 詳細目錄

若要最大化規模，請使用[!UICONTROL Public] (Open Exchange)和[!UICONTROL On Demand]詳細目錄。

### 網站目標定位

* **[!UICONTROL Traffic Type]**：僅[!UICONTROL Websites]
* **[!UICONTROL Site Tier]**： [!UICONTROL All sites]

### 對象目標定位

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]：**
   * 對於潛在位置，請將類似的對象類別和類似的對象大小分組到一個位置中。 然後，根據效能，執行下列任一項作業：
      * 從現有版位中移除表現不佳的對象。
      * 將表現最佳的對象移至另一個位置，以更能控制預算。
   * 若要重新定位位置，您最好在每個位置包含一個對象區段，以輕鬆控制競標和預算。

>[!NOTE]
>
>如果使用者只能透過一個位置聯絡，您的廣告會表現最好。 使用者在各個位置之間大幅重疊可能會導致競爭，進而產生持續增加出價的週期，從而提高每位使用者的成本。 因此，如果您包含多個對象，請確定這些對象並非由重疊的使用者/對象成員組成。
>
> 您可以在層級中建立您的對象，以避免重疊的對象，如此一來，您就可以視需求在位置中隱藏更高、包含性更強的層。

* **[!UICONTROL Frequency Capping]：**
   * 對於潛在位置，請使用嚴格的頻率上限（每天一次曝光）。
   * 對於重新定位版位，請將主要版位上限設定為每天6-10次曝光次數，並將次要版位上限設定為每小時一次曝光次數。

* **[!UICONTROL Device Targeting]**：
   * 包含[!UICONTROL Computer]、[!UICONTROL Mobile]和[!UICONTROL Tablet]。
   * 由於定位和測量限制，請勿以[!UICONTROL Firefox]和[!UICONTROL Safari]為目標。 如需有關[!DNL Safari ITP]的[!DNL Adobe]支援的詳細資訊，請聯絡您的Adobe客戶團隊。
   * 如果您鎖定行動網站流量，請停用除[!UICONTROL Chrome]和[!UICONTROL Edge]之外的所有行動瀏覽器。

### 品牌安全與媒體品質

使用內容篩選、競標前詐騙封鎖及/或[!UICONTROL Ads.txt]篩選功能會限制您的刊登版位規模，但如有需要請加以使用。

## 步驟5 — 使用正確的Creative Assets

* 最佳實務是納入儘可能多的獨特廣告大小，以最大化觸及率。 通用顯示範本可讓您上傳任何標準顯示廣告大小。
* 請確定所有版位都至少包含&#x200B;*1&rbrace;所有主要顯示廣告大小（300x250、728x90、160x600、300x600、320x50和300x50）。*
* 經常更新創意內容以防止創意疲勞。

>[!MORELIKETHIS]
>
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [位置層級競標前篩選及使用方式](optimization-pre-bid-filters.md)
>* [行銷活動啟動檢查清單](/help/dsp/campaign-management/campaign-launch-checklist.md)
