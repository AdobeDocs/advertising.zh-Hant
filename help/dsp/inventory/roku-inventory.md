---
title: 使用 [!DNL Roku] 詳細目錄
description: 瞭解DSP與的合作關係 [!DNL Roku]，包括詳細目錄選項、核准的第三方追蹤廠商，以及 [!DNL Roku] — 特定位置。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 使用 [!DNL Roku] 詳細目錄

Advertising DSP為的廣告提供獨特功能 [!DNL Roku].

## DSP和 [!DNL Roku] 合作關係

Roku與DSP擁有獨特的合作關係，可符合您的 [!DNL DSP] 對象至 [!DNL Roku] 1:1確定性對象目標定位的ID [!DNL Roku] 詳細目錄。

在Roku自己的DSP (OneView)之外，Advertising DSP可以單獨存取這些鎖定目標功能。 Advertising DSP也是唯一有權測量的DSP [!DNL Roku] 在所有其他連線電視(CTV)清查專案旁的供給。 因為 [!DNL Roku] 不會共用所有標準RTB和曝光畫素訊號，其他DSP無法跨Roku銷售的CTV供應專案鎖定目標或測量。

## [!DNL Roku] 詳細目錄選項

您可以a)直接透過設定私人交易ID [!DNL Roku] 然後輸入交易ID資料至DSP或b)造訪 [!DNL On Demand] 要訂閱的收藏館 [!DNL Roku] 設定檔：

>[!NOTE]
>
>[!DNL Roku] 開放市場與交換中無法使用詳細目錄。

* 針對您的私人交易， [在DSP中設定交易ID的相關資訊](/help/dsp/inventory/deal-id-create.md) 然後定位」[!UICONTROL Roku Network – Audience]「和」[!UICONTROL The Roku Channel – Audience]「 within [!DNL Roku] 版位。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 您可以 [訂閱以下內容 [!DNL Roku] 內的詳細目錄 [!DNL On Demand] 相簿](/help/dsp/inventory/on-demand-inventory-subscribe.md)，然後在中鎖定任何已核准的交易 [!DNL Roku] 版位：

   * &quot;[!UICONTROL Roku Network – Audience]」用於整個的詳細目錄 [!DNL Roku] 與優質內容合作夥伴的生態系統，例如 [!DNL The CW]， [!DNL ABC]、和 [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]「 for [!DNL Roku] 自有及營運(O&amp;O)應用程式內容。

### 使用自訂私人市場的好處 [!DNL Roku]

私人交易可讓您根據自己的需求自訂交易引數。

* **議價訂價：** 使用 [!DNL Roku] 銷售團隊商議並安排符合行銷活動需求的交易。

* **縮放優先順序：** 私人市場(PMP)的優先順序高於永遠開啟的交易(例如 [!DNL On Demand] 交易)。

* **頻率管理：** 此 [!DNL Roku] 預設頻率上限是每個使用者每30分鐘一(1)個廣告，但您可以按小時、日、周、月或整個飛行期間自訂上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]資料目標定位：** [!DNL Roku] 建立對象的來源 [!DNL Roku] 裝置和電視訊號，資料追蹤者： [!DNL The Roku Channel] （例如電視型別相似性、串流電視行為以及有線電視訂閱狀態），以及來自 [!DNL Roku] 客戶關係管理(CRM)系統。

* **[!DNL Roku]內容目標定位：** 私人交易可以依型別、應用程式封鎖清單、季節和主要事件來鎖定應用程式，並顯示在 [!DNL The Roku Channel] 僅限。

## [!DNL Roku] 版位

在DSP行銷活動中， [建立 [!DNL Roku] — 特定位置](/help/dsp/campaign-management/placements/placement-create.md) 使用位置型別»[!UICONTROL Connected TV (Roku)].」 包含 [!DNL Roku] 中的位置 [!DNL Roku] — 具有已定義目標的特定套件。

每個 [!DNL Roku] 位置必須至少指向一個 [!DNL Roku] 交易或來源。 若要搭配使用DSP不重複對象比對 [!DNL Roku]，包含一或多個可與比對的對象區段 [!DNL Roku] （選擇加入）確定性資料集。

### [!DNL Roku] — 核准的第三方追蹤廠商

[!DNL Roku] 刊登版位可包含來自下列廠商的第三方事件畫素和轉換畫素：  [!DNL Acxiom]， [!DNL Comscore]， [!DNL Data Plus Math]， [!DNL Experian]， [!DNL Factual]， [!DNL Kantar]， [!DNL Marketing Evolution]， [!DNL Neustar]， [!DNL Nielsen]， [!DNL Nielsen Catalina Solutions]， [!DNL NinthDecimal]， [!DNL Oracle]， [!DNL Placed]， [!DNL Polk]、和 [!DNL Research Now].

### 各放置策略的最佳實務

以下是建議作法 [!DNL Roku] — 特定位置。

若要最大化遞增範圍：

* 隱藏公開的對象 [!DNL Roku O&O] 排除您已使用觸及的對象 [!DNL The Roku Channel].

* 隱藏公開的對象 [!DNL All Roku] 排除您跨系統已觸及的對象 [!DNL Roku] 平台。

最快速的設定：

* 鎖定現有的隨時待處理交易 [!DNL The Roku Channel] 在 [[!DNL On Demand] 詳細目錄](/help/dsp/inventory/on-demand-inventory-subscribe.md) 以快速存取 [!DNL Roku] 自有及營運存貨。
* 鎖定現有的隨時待處理交易 [!DNL Roku Network] 在 [[!DNL On Demand] 詳細目錄](/help/dsp/inventory/on-demand-inventory-subscribe.md) 以快速跨以下專案達成規模： [!DNL Roku] 平台。

至最大比例：

* 自訂 [!DNL Roku] 優先存取的私人市場 [!DNL Roku] 以議定價格供應。

>[!MORELIKETHIS]
>
>* [手動建立交易識別碼詳細資料](/help/dsp/inventory/deal-id-create.md)
> * [訂閱並請求存取許可權 [!DNL On Demand] 進階存貨交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [建立位置](/help/dsp/campaign-management/placements/placement-create.md)
