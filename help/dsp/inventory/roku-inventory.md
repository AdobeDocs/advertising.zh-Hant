---
title: 使用 [!DNL Roku] 詳細目錄
description: 瞭解DSP與 [!DNL Roku]的合作關係，包括詳細目錄選項、核准的第三方追蹤廠商，以及 [!DNL Roku]特定位置的最佳實務。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 使用[!DNL Roku]詳細目錄

Advertising DSP提供[!DNL Roku]上的廣告功能。

## 對象比對

[!DNL Roku]與DSP合作關係將您的[!DNL DSP]對象與[!DNL Roku]詳細目錄上1:1確定性對象目標的[!DNL Roku] ID配對。

## [!DNL Roku]詳細目錄選項

您可以a)直接使用[!DNL Roku]設定私人交易識別碼，然後將交易識別碼資料輸入DSP或b)造訪[!DNL On Demand]相簿以訂閱[!DNL Roku]設定檔：

>[!NOTE]
>
>[!DNL Roku]詳細目錄不適用於開放市場與交換。

* 針對您的私人交易，[在DSP](/help/dsp/inventory/deal-id-create.md)中設定交易ID的相關資訊，然後在[!DNL Roku]位置中鎖定&quot;[!UICONTROL Roku Network - Audience]&quot;和&quot;[!UICONTROL The Roku Channel - Audience]&quot;。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 您可以[在 [!DNL On Demand] 相簿](/help/dsp/inventory/on-demand-inventory-subscribe.md)中訂閱下列 [!DNL Roku] 詳細目錄，然後在[!DNL Roku]版位中鎖定任何已核准的交易：

   * [!UICONTROL Roku Network - Audience]，適用於擁有優質內容合作夥伴（例如[!DNL The CW]、[!DNL ABC]和[!DNL ESPN]）的[!DNL Roku]生態系統中的詳細目錄。
   * 針對[!DNL Roku]所擁有且營運的(O&amp;O)應用程式內容的&quot;[!UICONTROL The Roku Channel - Audience]&quot;。

### 使用[!DNL Roku]自訂私人市場的優點

私人交易可讓您根據自己的需求自訂交易引數。

* **議價價格：**&#x200B;與[!DNL Roku]銷售團隊合作，商議並安排符合行銷活動需求的交易。

* **規模優先順序：**&#x200B;私人行銷場所(PMP)的優先順序高於永遠開啟的交易（例如[!DNL On Demand]筆交易）。

* **頻率管理：** [!DNL Roku]預設頻率上限是每個使用者每30分鐘一個(1)廣告，但您可以按小時、日、周、月或整個航班期間自訂上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]資料鎖定目標：** [!DNL Roku]對象是從[!DNL Roku]裝置和電視訊號建置的，[!DNL The Roku Channel]追蹤的資料（例如電視型別相似性、串流電視行為以及有線訂閱狀態），以及來自[!DNL Roku]客戶關係管理(CRM)系統的其他資料。

* **[!DNL Roku]內容鎖定目標：**&#x200B;私人交易可以依型別、應用程式封鎖清單、季節和尖峰事件來鎖定應用程式，並僅在[!DNL The Roku Channel]內顯示。

## [!DNL Roku]個位置

在DSP行銷活動中，[使用版位型別&quot;[!UICONTROL Connected TV (Roku)]&quot;建立 [!DNL Roku]專屬版位](/help/dsp/campaign-management/placements/placement-create.md)。 將[!DNL Roku]個版位包含在具有已定義目標的[!DNL Roku]特定套件中。

每個[!DNL Roku]位置都必須至少鎖定一個[!DNL Roku]交易或來源。 若要使用符合[!DNL Roku]的DSP對象，請包含一或多個可與[!DNL Roku] （選擇加入）確定性資料集相符的對象區段。

### [!DNL Roku]個已核准的第三方追蹤廠商

[!DNL Roku]版位可包含來自下列廠商的第三方事件畫素和轉換畫素： [!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。

### 各放置策略的最佳實務

下列是[!DNL Roku]特定位置的建議作法。

若要最大化遞增範圍：

* 透過排除您已使用[!DNL The Roku Channel]觸及的對象，隱藏[!DNL Roku O&O]上公開的對象。

* 排除您透過[!DNL Roku]平台已觸及的對象，以隱藏[!DNL All Roku]上公開的對象。

最快速的設定：

* 鎖定[[!DNL On Demand] 詳細目錄](/help/dsp/inventory/on-demand-inventory-subscribe.md)中[!DNL The Roku Channel]的現有、永遠開啟的交易，以快速存取[!DNL Roku]擁有且運作的詳細目錄。
* 鎖定[[!DNL On Demand] 詳細目錄](/help/dsp/inventory/on-demand-inventory-subscribe.md)中[!DNL Roku Network]的現有、永遠開啟的交易，以快速在[!DNL Roku]平台上達成規模。

至最大比例：

* 自訂[!DNL Roku]私人市集，以議定價格優先存取[!DNL Roku]供給。

>[!MORELIKETHIS]
>
>* [手動建立交易識別碼詳細資料](/help/dsp/inventory/deal-id-create.md)
> * [訂閱及要求存取 [!DNL On Demand] 進階詳細目錄交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [建立位置](/help/dsp/campaign-management/placements/placement-create.md)
