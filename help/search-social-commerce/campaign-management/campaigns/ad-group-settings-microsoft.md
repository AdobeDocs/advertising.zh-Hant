---
title: '"[!DNL Microsoft Advertising] 廣告群組設定」'
description: 參考設定 [!DNL Microsoft Advertising] 廣告群組。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 廣告群組設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：** 促銷活動內唯一的廣告群組名稱。 長度上限為128個字元。

**[!UICONTROL Status]：** 廣告群組的顯示狀態： *作用中* 或 *已暫停*. 新廣告群組的預設為 *作用中*.

**[!UICONTROL Ad Language]：** 廣告的目標語言。<!-- Which campaign types? Not there for audience image-based ad groups. -->

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]：** 如何在廣告群組中放置廣告以及放置廣告的位置：

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* （預設）：對搜尋網路上的廣告進行競標。

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]：* 若要在銀團化合作夥伴網站上對廣告投標。

* *[!UICONTROL Content network]：* 已棄用

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]：** 已棄用

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** （對象廣告群組）是否：

* *[!UICONTROL Target and Bid]：* 只向與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。

* *[!UICONTROL Bid Only]：* 即使未與目標對象相關聯的人，只要他們滿足其他廣告群組層級目標，也能顯示廣告。 不過，您可以針對特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

對象 [!DNL Microsoft Advertising] 對象網路中的廣告群組，位置目標的競標修飾詞並未在具有「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]：** （對象廣告群組；選用）要包含或排除作為目標的特定性別： *[!UICONTROL Male]*， *[!UICONTROL Female]*、和 *[!UICONTROL Unknown]*. 依預設，會鎖定所有性別。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓圈一次，以使用藍色勾號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可以選擇針對每個性別目標依指定的百分比增加或減少競標。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以使用紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

**[!UICONTROL Age]：** （對象廣告群組；選用）要包含或排除作為目標的特定年齡類別： *[!UICONTROL 18-24]*， *[!UICONTROL 25-34]*， *[!UICONTROL 35-49]*， *[!UICONTROL 50-64]*， *[!UICONTROL 65+]*、和 *[!UICONTROL Unknown]*. 依預設，會鎖定所有年齡。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓圈一次，以使用藍色勾號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可以選擇針對每個目標年齡，以指定的百分比增加或減少出價。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以使用紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

**[!UICONTROL Industry]：** （對象廣告群組；選用）要納入或排除作為目標的特定產業。 依預設，會鎖定所有產業。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓圈一次，以使用藍色勾號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可選擇針對每個目標產業，以指定的百分比增加或減少競標。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以使用紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

**[!UICONTROL Job Function Targets]：** （對象廣告群組；選用）要納入或排除為目標的特定工作職能。 依預設，所有工作功能都是鎖定目標。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓圈一次，以使用藍色勾號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可以選擇針對每個目標工作功能，以指定的百分比增加或減少競標。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以使用紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]：** （僅限顯示器/原生網路上的行銷活動；選用）您不想要顯示廣告的顯示網路上的網站。 輸入有效的URL，例如www.example.com。 若要指定多個字串，請以逗號分隔字串，或在個別行中輸入字串。

Microsoft如需可用性相關資訊，請參閱「[防止廣告出現在特定網站上](https://help.ads.microsoft.com/#apex/bae/en/14061/0).」

>[!MORELIKETHIS]
>
>* [管理廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

