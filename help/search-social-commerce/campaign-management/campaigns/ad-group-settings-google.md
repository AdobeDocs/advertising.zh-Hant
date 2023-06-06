---
title: '"[!DNL Google Ads] 廣告群組設定」'
description: 參考設定 [!DNL Google Ads] 廣告群組。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] 廣告群組設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：** 促銷活動內唯一的廣告群組名稱。 長度上限為255個雙位元組字元。

**[!UICONTROL Status]：** 廣告群組的顯示狀態： *作用中* 或 *已暫停*. 新廣告群組的預設為 *作用中*.

**[!UICONTROL Ad Group Type]：** （僅限展開的動態搜尋廣告行銷活動）廣告群組的型別：

* *[!UICONTROL Search Standard]* （預設值）：適用於標準廣告。

* *[!UICONTROL Search Dynamic]：* 適用於動態搜尋廣告。

**[!UICONTROL Ad Rotation Mode]：** 頻率 [!DNL Google Ads] 會在廣告群組中相互傳遞您的作用中廣告：

* *[!UICONTROL Optimize]：* Google廣告偏愛其預期表現優於廣告群組中其他廣告的廣告。 這些廣告更常進入廣告拍賣，一段時間後，會偏好使用單一廣告。 這可能與您的業務和最佳化目標不一致。

* *[!UICONTROL Rotate forever]：*   您的每個廣告進入廣告拍賣的次數都更為平均，可讓「搜尋、社交和商務」不僅依據點進率，也依據轉換為您的廣告評分。

* *[!UICONTROL Use campaign setting]*（新廣告群組的預設值）：使用現有的促銷活動層級廣告輪換設定。 **注意：** 行銷活動層級設定在「搜尋」、「社交」和「商務」中不可見。

如果行銷活動使用智慧競標策略(例如 [!UICONTROL Target CPA]， [!UICONTROL Target ROAS]，或 [!UICONTROL Enhanced CPC])，然後 [!DNL Google Ads] 自動將選項設為&quot;[!UICONTROL Optimize].」

**[!UICONTROL Custom Bid Level]：** （僅針對顯示網路的行銷活動）競標方式：依據 *[!UICONTROL Ad Group]* （預設）， *[!UICONTROL Age]*， *[!UICONTROL Gender]*， *[!UICONTROL Interest and List]* (Google Ads中的興趣與再行銷)， *[!UICONTROL Keyword]*， *[!UICONTROL Placement]* （網站）， *[!UICONTROL Unknown]*，或 *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* 當您依據關鍵字競標時，請在關鍵字層級建立追蹤範本。 同樣地，當您依版位競標時，請在版位層級建立追蹤範本。 針對所有其他維度，在廣告層級建立追蹤範本。
>* 當您針對產品組合中的行銷活動，依年齡、性別、興趣和清單或垂直專案競標時，最佳化功能不會將維度的競標最佳化。 此外，所有歸因都會套用至廣告群組。
>* 搜尋網路上的廣告一律會使用關鍵字競標。


## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]：** (行銷活動具有 [!UICONTROL Target CPA] 競標；選用)廣告群組的每次贏取目標成本(CPA)。 此值會覆寫行銷活動層級目標。

**[!UICONTROL Target ROAS]：** (行銷活動具有 [!UICONTROL Target ROAS] 競標；選用)廣告群組的目標廣告投資報酬率(ROAS)，以百分比表示。 此值會覆寫行銷活動層級目標。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** (僅限搜尋網路上的行銷活動，且現有行銷活動為唯讀 [!DNL Gmail] 行銷活動)是否：

* *[!UICONTROL Target and Bid]：* 只向與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。

* *[!UICONTROL Bid Only]：* 即使未與目標對象相關聯的人，只要他們滿足其他廣告群組層級目標，也能顯示廣告。 不過，您可以針對特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [管理廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

