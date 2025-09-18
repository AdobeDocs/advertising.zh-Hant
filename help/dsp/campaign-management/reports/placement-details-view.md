---
title: 檢視刊登版位的網站、廣告、頻率和詳細目錄資訊
description: 瞭解如何檢視刊登版位的目標網站、廣告、頻率和詳細目錄資料。
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 0f022babeab6c044949760cedc103323eb0cc950
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# 檢視刊登版位的網站、廣告、頻率和詳細目錄資訊

對於每個位置，您可以[開啟（詳細資料檢視[!UICONTROL Inspector]）](placement-details-view.md)，其中列出位置中的所有目標網站、廣告和交易。 其中也包含投放位置的頻率資料。 您可以選擇從任何索引標籤匯出資料。

![位置檢視窗](/help/dsp/assets/placement-inspector.png)

## 位置[!UICONTROL Inspector]中的資訊 {#placement-inspector}

* **[!UICONTROL Sites]：**&#x200B;此位置有曝光的所有網站。

  [!UICONTROL Sites]索引標籤包含搜尋和篩選功能、主要頁面上可用的相同標準和自訂欄檢視選項，以及每列的[!UICONTROL Exclude]按鈕，以便您能夠從位置快速排除網站。

* **[!UICONTROL Ads]：**&#x200B;位置中的所有廣告。

  [!UICONTROL Ads]索引標籤包含搜尋和篩選功能、主要頁面上可用的相同標準和自訂欄檢視選項，以及每一列中的快速動作按鈕，例如[!UICONTROL View Ad Approvals]。

* **[!UICONTROL Frequency]：**&#x200B;位置之每個廣告頻率層級的資料，包括：
   * 廣告頻率層級（例如「1」，適用於使用者看過一次廣告的所有例項）
   * 以指定頻率層級接收曝光的裝置/瀏覽器或人員預估不重複數量（視促銷活動指定的[!UICONTROL Cross Device Level]而定）
   * 指定頻率層級的預估曝光次數
   * 指定頻率等級的預估平均頻率。 此值等於（預估曝光次數）/（預估不重複值）。

* **[!UICONTROL Inventory]：**&#x200B;此位置所鎖定之所有交易的資訊。

  [!UICONTROL Inventory]索引標籤可顯示效能統計資料，例如[!UICONTROL Auctions]、[!UICONTROL Bids]和[!UICONTROL Win Rate]，以啟用快速疑難排解。 索引標籤包含搜尋和篩選功能、首頁面上可用的相同標準和自訂欄檢視選項，以及每一列的快速動作按鈕，包括[!UICONTROL Edit]、[!UICONTROL View Report]和[[!UICONTROL Auction Insights]，以供進一步疑難排解](/help/dsp/inventory/private-deal-auction-insights.md)。

## 開啟[!UICONTROL Placement Inspector] {#inspector-open}

1. 開啟父行銷活動或套件的版位檢視：

   * 檢視上層行銷活動內的所有版位：

      1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

      1. 按一下行銷活動的名稱。

      1. 按一下「**[!UICONTROL Placements]**」標籤。

   * 檢視上層封裝內的所有版位：

      1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

      1. 按一下行銷活動的名稱。

      1. 按一下「**[!UICONTROL Packages]**」標籤。

      1. 按一下父套件的名稱。

1. 將游標停留在位置列上，按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Inspector]**。

1. （選擇性） [視需要變更資料行檢視](campaign-data-views-manage.md#column-view-change)，以檢視必要的量度。

1. （選擇性）若要匯出任何標籤上的資料，請按一下右上方的![更多](/help/search-social-commerce/assets/more.png "更多")，然後按一下&#x200B;**[!UICONTROL Export]**。

   資料會以XLSM格式儲存至瀏覽器的預設下載資料夾作為報表。

## 從[!UICONTROL Placement Inspector]移除刊登版位的廣告 {#remove-ads-placement-inspector}

1. [開啟[!UICONTROL Placement Inspector]](#inspector-open)。

1. 按一下「**[!UICONTROL Ads]**」標籤。

1. 在廣告名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Detach]**」。

## 疑難排解詳細目錄

| 問題 | 可能的原因 | 要採取的動作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 發佈者尚未開始傳送競標要求。 | 請連絡發佈商以啟動交易。 |
| | 交易設定不正確，例如輸入不正確的外部交易ID。 | 確認交易詳細資料並編輯交易。 |
| [!UICONTROL Auctions but no Bids] | 位置鎖定目標不符合交易的傳入競標要求。 <br><br>例如，位置可能以不符合交易條件的地理位置為目標。 | 視需要編輯位置目標，以避免目標錯配。 |
| | 投放位置沒有有效的廣告，且該廣告具有交易所需的媒體型別。 | 建立並附加具有正確媒體型別的廣告至投放位置。 |
| | 位置沒有足夠的預算。 | 增加版位預算以允許對傳入的請求投標。 |
| | 刊登投放日期與交易的曝光傳送日期不重疊。 | 視需要編輯位置的投放日期。 |
| [!UICONTROL Low Win Rate] | 位置的最高出價（下限或固定）低於交易要求的最低出價。 | 視需要增加位置的[!UICONTROL Max Bid]。 |
| | 此位置使用限制競標的競標前篩選條件。 | 降低競標前篩選器的臨界值，以允許更多競標。 |
| | 此位置的對象鎖定目標太嚴格。 | 檢查指定的對象目標是否有足夠的活躍使用者，並儘可能展開對象。 |

>[!MORELIKETHIS]
>
>* 行銷活動管理檢視中的[效能報表型別](campaign-reports-about.md)
>* [管理您的行銷活動資料檢視](campaign-data-views-manage.md)
