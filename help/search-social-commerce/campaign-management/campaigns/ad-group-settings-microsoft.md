---
title: 『[!DNL Microsoft® Advertising] 廣告群組設定
description: 參考設定 [!DNL Microsoft® Advertising] 廣告群組。
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 7339af39250f0328bc6e8d530a2d7f04286132e5
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] 廣告群組設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：** 促銷活動中的唯一廣告群組名稱。 長度上限為128個字元。

**[!UICONTROL Status]：** 廣告群組的顯示狀態： *作用中* 或 *已暫停*. 新廣告群組的預設為 *作用中*.

**[!UICONTROL Ad Language]：** （搜尋行銷活動）廣告的目標語言。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]：** （搜尋廣告）在廣告群組中放置廣告的方式和位置：

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! websites]* （預設）：對搜尋網路上的廣告進行競標。

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! syndicated search partners]：* 若要在財團合作網站刊登廣告競標，請執行下列步驟：

* *[!UICONTROL Content network]：* 已棄用

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]：** 已棄用

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** （對象廣告群組）是否：

* *[!UICONTROL Target and Bid]：* 只對與目標對象相關聯且滿足廣告群組任何其他目標的使用者顯示廣告。

* *[!UICONTROL Bid Only]：* 即使是不與目標對象相關聯的人，只要他們滿足其他廣告群組層級目標，也能顯示廣告。 不過，您可以為特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

的 [!DNL Microsoft® Advertising] 在對象網路中的廣告群組，位置目標的競標修飾詞並未在具有「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定。

**[!UICONTROL Genre]：** (廣告群組位於 [!UICONTROL Audience CTV Video] 促銷活動；適用於美國、CA、BR、MX、UK、DE、ES、FR、IT、AU、MY和TH<!-- should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->)目標型別，這會決定您的廣告出現的顯示和頻道：

* *[!UICONTROL All genres]：* （預設）鎖定所有型別。

* *[!UICONTROL Select From Below List]：* 鎖定選取的流派。 從所有可用型別的清單中選取。

連線電視(CTV)廣告投放視您的視訊品質和競標金額而定。 請參閱 [CTV廣告的技術需求](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]：** （對象廣告群組；選用）要納入或排除作為目標的特定性別： *[!UICONTROL Male]*， *[!UICONTROL Female]*、和 *[!UICONTROL Unknown]*. 依預設，會鎖定所有性別。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓形，使藍色核取記號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可以選擇按每個性別目標的指定百分比增加或減少競標。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以便顯示紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

**[!UICONTROL Age]：** （對象廣告群組；選用）要納入或排除作為目標的特定年齡類別： *[!UICONTROL 18-24]*， *[!UICONTROL 25-34]*， *[!UICONTROL 35-49]*， *[!UICONTROL 50-64]*， *[!UICONTROL 65+]*、和 *[!UICONTROL Unknown]*. 依預設，會定位所有年齡。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓形，使藍色核取記號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可以選擇為每個目標年齡增加或減少競標，增加或減少指定的百分比。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以便顯示紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

**[!UICONTROL Industry]：** （對象廣告群組；選用）要納入或排除作為目標的特定產業。 依預設，會鎖定所有產業。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓形，使藍色核取記號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可以選擇針對每個目標產業，依指定百分比提高或降低競標。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以便顯示紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

**[!UICONTROL Job Function Targets]：** （對象廣告群組；選用）要納入或排除作為目標的特定工作職能。 依預設，所有工作功能都是鎖定目標。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下旁邊的圓形，使藍色核取記號(![包含](/help/search-social-commerce/assets/include.png "包含"))顯示。 您可以選擇針對每個目標工作功能，依指定的百分比增加或減少競標。

* 若要排除某個值，請按一下它旁邊的圓圈兩次，以便顯示紅色核取記號(![排除](/help/search-social-commerce/assets/exclude.png "排除"))顯示。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]：** （選用）從廣告群組向客戶提供廣告的次數。 輸入值並選取時間單位(*[!UICONTROL Hour]*， *[!UICONTROL Day]*，或 *[!UICONTROL Week]*)。

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]：** （僅限顯示/原生網路上的行銷活動；選用）顯示網路上的網站（您不想要顯示廣告）。 請輸入有效的URL，例如www.example.com。 若要指定多個字串，請以逗號分隔字串，或在個別行中輸入字串。

如需有關可用性的資訊，請參閱 [!DNL Microsoft® Advertising] 「的說明[防止廣告出現在特定網站上](https://help.ads.microsoft.com/#apex/bae/en/14061/0).」

>[!MORELIKETHIS]
>
>* [管理廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
