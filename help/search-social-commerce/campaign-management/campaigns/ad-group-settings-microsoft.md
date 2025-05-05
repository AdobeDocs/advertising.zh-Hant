---
title: '[!DNL Microsoft Advertising]廣告群組設定'
description: 參考 [!DNL Microsoft Advertising] 廣告群組的設定。
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]廣告群組設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：**&#x200B;促銷活動中的唯一廣告群組名稱。 長度上限為128個字元。

**[!UICONTROL Status]：**&#x200B;廣告群組的顯示狀態： *作用中*&#x200B;或&#x200B;*已暫停*。 新廣告群組的預設值為&#x200B;*作用中*。

**[!UICONTROL Ad Language]：** （搜尋行銷活動）廣告的目標語言。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]：** （搜尋廣告）在廣告群組中放置廣告的方式和位置：

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* （預設）：在搜尋網路上刊登廣告競標。

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]：*&#x200B;若要在聯合發行合作夥伴網站上對廣告投標。

* *[!UICONTROL Content network]：*&#x200B;已棄用

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]：**&#x200B;已棄用

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** （對象廣告群組）是否：

* *[!UICONTROL Target and Bid]：*&#x200B;若要只對與目標對象相關聯的使用者顯示廣告，這些使用者也滿足廣告群組的任何其他目標。

* *[!UICONTROL Bid Only]：*&#x200B;若要顯示廣告，即使是未與目標對象相關聯的使用者，只要他們符合其他廣告群組層級的目標即可。 不過，您可以為特定對象設定較高的競標，以增加向這些對象顯示廣告的機會。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

針對對象網路中的[!DNL Microsoft Advertising]個廣告群組，位置目標的競標修飾詞並未在具有「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定的標準產品組合中進行最佳化。

**[!UICONTROL Genre]：** （廣告群組位於[!UICONTROL Audience CTV Video]個行銷活動中；在美國、CA、BR、MX、UK、DE、ES、FR、IT、AU、MY和TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->提供）目標型別，其決定廣告出現的節目和頻道：

* *[!UICONTROL All genres]：* （預設）鎖定所有型別。

* *[!UICONTROL Select From Below List]：*&#x200B;目標選取的型別。 從所有可用型別的清單中選取。

連線電視(CTV)廣告投放視您的視訊品質和競標金額而定。 檢視CTV廣告[&#128279;](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements)的技術需求。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]：** （對象廣告群組；選用）要包含或排除為目標的特定性別： *[!UICONTROL Male]*、*[!UICONTROL Female]*&#x200B;和&#x200B;*[!UICONTROL Unknown]*。 依預設，會鎖定所有性別。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下相鄰的圓圈，以顯示藍色核取記號（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以選擇按每個性別目標的指定百分比增加或減少競標。

* 若要排除值，請按兩下相鄰的圓圈，以便出現紅色核取記號（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

**[!UICONTROL Age]：** （對象廣告群組；選用）要包含或排除為目標的特定年齡類別： *[!UICONTROL 18-24]*、*[!UICONTROL 25-34]*、*[!UICONTROL 35-49]*、*[!UICONTROL 50-64]*、*[!UICONTROL 65+]*&#x200B;和&#x200B;*[!UICONTROL Unknown]*。 依預設，會定位所有年齡。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下相鄰的圓圈，以顯示藍色核取記號（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以選擇為每個目標年齡增加或減少競標，增加或減少指定的百分比。

* 若要排除值，請按兩下相鄰的圓圈，以便出現紅色核取記號（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

**[!UICONTROL Industry]：** （對象廣告群組；選用）要納入或排除為目標的特定產業。 依預設，會鎖定所有產業。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下相鄰的圓圈，以顯示藍色核取記號（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以選擇針對每個目標產業，依指定百分比提高或降低競標。

* 若要排除值，請按兩下相鄰的圓圈，以便出現紅色核取記號（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

**[!UICONTROL Job Function Targets]：** （對象廣告群組；選擇性）要納入或排除為目標的特定工作職能。 依預設，所有工作功能都是鎖定目標。 排除專案一律會覆寫包含專案。

* 若要鎖定所有值，請勿選取任何值。

* 若要包含值，請按一下相鄰的圓圈，以顯示藍色核取記號（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以選擇針對每個目標工作功能，依指定的百分比增加或減少競標。

* 若要排除值，請按兩下相鄰的圓圈，以便出現紅色核取記號（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]：** （選擇性）可從廣告群組向客戶提供廣告的次數。 輸入值並選取時間單位（*[!UICONTROL Hour]*、*[!UICONTROL Day]*&#x200B;或&#x200B;*[!UICONTROL Week]*）。

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]：** （僅限顯示/原生網路的行銷活動；選擇性）您不想顯示廣告的顯示網路網站。 請輸入有效的URL，例如www.example.com。 若要指定多個字串，請以逗號分隔字串，或在個別行中輸入字串。

如需有關可用性的資訊，請參閱[!DNL Microsoft Advertising] 「防止廣告出現在特定網站[&#128279;](https://help.ads.microsoft.com/#apex/bae/en/14061/0)」的說明。

>[!MORELIKETHIS]
>
>* [管理廣告群組](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
