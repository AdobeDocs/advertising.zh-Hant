---
title: 檢視刊登版位的網站、廣告、頻率和詳細目錄資訊
description: 瞭解如何檢視刊登版位的目標網站、廣告、頻率和詳細目錄資料。
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# 檢視刊登版位的網站、廣告、頻率和詳細目錄資訊

對於每個位置，您可以 [開啟（詳細資料檢視） [!UICONTROL Inspector])](placement-details-view.md)，會列出位置中的所有目標網站、廣告和交易。 其中也包含投放位置的頻率資料。 您可以選擇從任何索引標籤匯出資料。

![位置檢測器](/help/dsp/assets/placement-inspector.png)

## 位置中的資訊 [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]：** 此版位曾有曝光的所有網站。

  此 [!UICONTROL Sites] 索引標籤包含搜尋和篩選功能、在主要頁面上可用的相同標準和自訂欄檢視選項，以及 [!UICONTROL Exclude] 按鈕來快速排除位置。

* **[!UICONTROL Ads]：** 位置中的所有廣告。

  此 [!UICONTROL Ads] 索引標籤包括搜尋和篩選功能、主要頁面上可用的相同標準和自訂欄檢視選項，以及每列中的快速動作按鈕，例如 [!UICONTROL Pause] （讓您可以快速暫停廣告）。

* **[!UICONTROL Frequency]：** 此投放位置的每個廣告頻率層級的資料，包括：
   * 廣告頻率層級（例如「1」，適用於使用者看過一次廣告的所有例項）
   * 裝置/瀏覽器或人員的預估不重複數量(視指定的 [!UICONTROL Cross Device Level] （適用於促銷活動）在指定頻率層級收到曝光數
   * 指定頻率層級的預估曝光次數
   * 指定頻率等級的預估平均頻率。 此值等於（預估曝光次數）/（預估不重複值）。

* **[!UICONTROL Inventory]：** 此位置所定位之所有交易的資訊。

  此 [!UICONTROL Inventory] 索引標籤可讓您透過顯示效能統計資料來快速進行疑難排解，例如 [!UICONTROL Auctions]， [!UICONTROL Bids]、和 [!UICONTROL Win Rate]. 索引標籤包括搜尋和篩選功能、主要頁面上可用的相同標準和自訂欄檢視選項，以及每列中的快速動作按鈕，包括 [!UICONTROL Edit]， [!UICONTROL View Report]、和 [[!UICONTROL Auction Insights] 以取得進一步的疑難排解](/help/dsp/inventory/private-deal-auction-insights.md).

## 開啟 [!UICONTROL Placement Inspector]

1. 開啟父行銷活動或套件的版位檢視：

   * 檢視上層行銷活動內的所有版位：

      1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

      1. 按一下行銷活動的名稱。

      1. 按一下 **[!UICONTROL Placements]** 標籤。

   * 檢視上層封裝內的所有版位：

      1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

      1. 按一下行銷活動的名稱。

      1. 按一下 **[!UICONTROL Packages]** 標籤。

      1. 按一下父套件的名稱。

1. 將游標停留在放置列上，按一下 **[!UICONTROL More]**，然後按一下選項：

   * 若要檢視位置所瞄準的所有網站，請按一下 **[!UICONTROL Sites]**.

   * 若要檢視刊登版位中的所有廣告，請按一下 **[!UICONTROL Ads]**.

   * 若要檢視位置的頻率資料，請按一下 **[!UICONTROL Frequency]**.

   * 若要檢視位置所目標的所有交易，請按一下 **[!UICONTROL Inventory]**.

1. （可選） [變更欄檢視](campaign-data-views-manage.md#column-view-change) 視需要檢視所需量度。

1. （可選）若要匯出任何標籤上的資料，請按一下 ![更多](/help/search-social-commerce/assets/more.png "更多") 圖示，然後按一下 **[!UICONTROL Export]**.

   資料會以XLSM格式儲存至瀏覽器的預設下載資料夾作為報表。

## 疑難排解詳細目錄

| 問題 | 可能的原因 | 要採取的動作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 發佈者尚未開始傳送競標要求。 | 請連絡發佈商以啟動交易。 |
| | 交易設定不正確，例如輸入不正確的外部交易ID。 | 確認交易詳細資料並編輯交易。 |
| [!UICONTROL Auctions but no Bids] | 位置鎖定目標不符合交易的傳入競標要求。 <br><br> 例如，刊登版位可能會將目標定位為不符合交易資格的地理位置。 | 視需要編輯位置目標，以避免目標錯配。 |
| | 投放位置沒有有效的廣告，且該廣告具有交易所需的媒體型別。 | 建立並附加具有正確媒體型別的廣告至投放位置。 |
| | 位置沒有足夠的預算。 | 增加版位預算以允許對傳入的請求投標。 |
| | 刊登投放日期與交易的曝光傳送日期不重疊。 | 視需要編輯位置的投放日期。 |
| [!UICONTROL Low Win Rate] | 位置的最高出價（下限或固定）低於交易要求的最低出價。 | 增加投放位置的 [!UICONTROL Max Bid] 視需要。 |
| | 此位置使用限制競標的競標前篩選條件。 | 降低競標前篩選器的臨界值，以允許更多競標。 |
| | 此位置的對象鎖定目標太嚴格。 | 檢查指定的對象目標是否有足夠的活躍使用者，並儘可能展開對象。 |

>[!MORELIKETHIS]
>
>* [Campaign Management檢視中的效能報表型別](campaign-reports-about.md)
>* [管理您的Campaign資料檢視](campaign-data-views-manage.md)
