---
title: '[!DNL Google Ads]廣告群組設定'
description: 參考 [!DNL Google Ads] 廣告群組的設定。
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# [!DNL Google Ads]廣告群組設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：**&#x200B;促銷活動中的唯一廣告群組名稱。 長度上限為255個雙位元組字元。

**[!UICONTROL Status]：**&#x200B;廣告群組的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新廣告群組的預設值為&#x200B;*作用中*。

**[!UICONTROL Ad Group Type]：** （僅展開動態搜尋廣告行銷活動）廣告群組的型別：

* *[!UICONTROL Search Standard]* （預設）：適用於標準廣告。

* *[!UICONTROL Search Dynamic]：*&#x200B;適用於動態搜尋廣告。

**[!UICONTROL Ad Rotation Mode]：** [!DNL Google Ads]在廣告群組中相互關聯地傳遞您作用中廣告的頻率：

* *[!UICONTROL Optimize]：* Google廣告偏愛其預期表現優於廣告群組中其他廣告的廣告。 這些廣告更常進入廣告拍賣，一段時間過後，系統會偏好使用單一廣告。 這可能與您的業務和最佳化目標不一致。

* *[!UICONTROL Rotate forever]：*   您的每個廣告進入廣告拍賣的次數都比較平均，這使得Search、Social和Commerce不僅可根據點進率，也可根據轉換為您的廣告評分。

* *[!UICONTROL Use campaign setting]* （新廣告群組的預設值）：使用現有的行銷活動層級廣告輪換設定。 **注意：**&#x200B;行銷活動層級設定在「搜尋」、「社交」和「Commerce」中不可見。

如果行銷活動使用智慧出價策略（例如[!UICONTROL Target CPA]、[!UICONTROL Target ROAS]或[!UICONTROL Enhanced CPC]），則[!DNL Google Ads]會自動將選項設為&quot;[!UICONTROL Optimize]&quot;。

**[!UICONTROL Custom Bid Level]：** （僅針對顯示網路的行銷活動）競標方式：由&#x200B;*[!UICONTROL Ad Group]* （預設值）、*[!UICONTROL Age]*、*[!UICONTROL Gender]*、*[!UICONTROL Interest and List]* (Google Ads中的興趣與再行銷)、*[!UICONTROL Keyword]*、*[!UICONTROL Placement]* （網站）、*[!UICONTROL Unknown]*&#x200B;或&#x200B;*[!UICONTROL Vertical]*。

>[!NOTE]
>
>* 當您依據關鍵字競標時，請在關鍵字層級建立追蹤範本。 同樣地，當您依版位競標時，請在版位層級建立追蹤範本。 針對所有其他維度，在廣告層級建立追蹤範本。
>* 當您針對產品組合中的行銷活動依年齡、性別、興趣和清單或垂直方式競標時，最佳化功能不會將維度的競標最佳化。 此外，所有歸因都會套用至廣告群組。
>* 搜尋網路上的廣告一律會使用關鍵字競標。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]：** （具有[!UICONTROL Target CPA]競標的行銷活動；選用）廣告群組的每次贏取目標成本(CPA)。 此值會覆寫行銷活動層級目標。

**[!UICONTROL Target ROAS]：** （具有[!UICONTROL Target ROAS]競標的行銷活動；選用）廣告群組的目標廣告支出(ROAS)回報百分比。 此值會覆寫行銷活動層級目標。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** （僅搜尋網路上的行銷活動，以及顯示網路上的現有唯讀[!DNL Gmail]行銷活動）是否：

* *[!UICONTROL Target and Bid]：*&#x200B;若要只對與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。

* *[!UICONTROL Bid Only]：*&#x200B;若要顯示廣告，即使是未與目標對象相關聯的使用者，只要他們符合其他廣告群組層級的目標即可。 不過，您可以為特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。

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
