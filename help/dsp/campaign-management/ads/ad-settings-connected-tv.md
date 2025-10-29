---
title: 連線電視廣告設定
description: 請參閱連線電視廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 連線電視廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限新廣告*

**[!UICONTROL URL]**： VAST標籤URL。

**[!UICONTROL Title]**：用於「廣告」檢視和報告中的檔案名稱。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後按一下&#x200B;**[!UICONTROL Enter]**&#x200B;索引鍵。 如果標籤有效，您會在頂端附近看到包含`<VAST>`的XML檔案。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。

**[!UICONTROL Ad Name]：**&#x200B;廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 使用當您在位置、[!UICONTROL Ads]檢視和報告中附加廣告時容易找到的名稱。 例如，說明單位型別和某些關鍵屬性（例如「假日產品預覽：30秒CTV」）。

**[!UICONTROL Width | Ad Unit Width]：**&#x200B;整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位型別而鎖定。

**[!UICONTROL Height | Ad Unit Height]：**&#x200B;整個廣告單位的高度。 此選項可能會根據您選取的廣告單位型別而鎖定。

**[!UICONTROL Player X]：**&#x200B;廣告單位的X座標。 保留預設設定。

**[!UICONTROL Player Y]：**&#x200B;廣告單位的Y座標。 保留預設設定。

**[!UICONTROL Player Width]：**&#x200B;整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位型別而鎖定。

這與&#x200B;**[!UICONTROL Width]**&#x200B;欄位相同。

**[!UICONTROL Player Height]：**&#x200B;整個廣告單位的高度。 此選項可能會根據您選取的廣告單位型別而鎖定。

這與&#x200B;**[!UICONTROL Height]**&#x200B;欄位相同。

**[!UICONTROL Show Controls]：**&#x200B;在何處加入廣告的視訊控制項： *[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]*&#x200B;或&#x200B;*[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]：**&#x200B;是保留視訊的寬度和高度比例(*[!UICONTROL Yes]*)，還是延伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入做為廣告來源的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入的協力廠商VAST標籤作為廣告來源，並插入必要的[Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) （如果適用）。

**[!UICONTROL Clock Number]**： （僅用於英國；僅供具有許可權的使用者使用）唯一識別碼，用於確保廣播正確的廣告。 如果此設定不適用，請保留空白。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告](/help/dsp/campaign-management/ads/ad-list-placements.md)關聯的版位
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)
