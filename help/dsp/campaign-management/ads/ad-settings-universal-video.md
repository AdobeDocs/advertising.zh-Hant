---
title: 通用視訊廣告設定
description: 請參閱通用視訊廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# 通用視訊廣告設定

>[!NOTE]
>
>通用視訊廣告只能附加至通用視訊位置。

## [!UICONTROL Insert Ad Tag]

*僅限新廣告*

**[!UICONTROL URL]：** VAST標籤URL。

**[!UICONTROL Title]：**&#x200B;檔案的標題，它在[!UICONTROL Ads]檢視和報告中。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後按一下&#x200B;**[!UICONTROL Enter]**&#x200B;索引鍵。 如果標籤有效，您會在頂端附近看到包含`<VAST>`的XML檔案。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。

**[!UICONTROL Ad Name]：**&#x200B;廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 使用當您在位置、[!UICONTROL Ads]檢視和報告中附加廣告時容易找到的名稱。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 30sec Universal Video）。

**[!UICONTROL Show Controls]：**&#x200B;在何處加入廣告的視訊控制項： *[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]*&#x200B;或&#x200B;*[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]：**&#x200B;是保留視訊的寬度和高度比例(*[!UICONTROL Yes]*)，還是延伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入做為廣告來源的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入的協力廠商VAST標籤作為廣告來源，並插入必要的[Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) （如果適用）。

**[!UICONTROL Wmode]：**&#x200B;視窗模式： *[!UICONTROL window]*、*[!UICONTROL transparent]*&#x200B;或&#x200B;*[!UICONTROL opaque]*。 如果此設定不適用，請保留空白。

**[!UICONTROL Video Format]：**&#x200B;潛在詳細目錄之廣告播放器的格式： *[!UICONTROL VPAID]*、*[!UICONTROL VPAID & VAST]*&#x200B;或&#x200B;*[!UICONTROL VAST]*。 可檢視度一律針對[!UICONTROL VPAID]測量，但[!UICONTROL VPAID & VAST]包含不允許可檢視度測量的詳細目錄。 如果可檢視度量度對您的行銷活動很重要，請考慮此區別。

當您目標為只嚴格要求VAST格式的連線電視或詳細目錄時(通常來自Google Ad Manager、Appnexus、SpotX和Freewheel等供應來源)，請使用[!UICONTROL VAST] （不允許可檢視度測量）。 也請將此選項用於先前與標準前段廣告(VAST)或手機+平板電腦標準前段廣告(VAST)版位/廣告相容的詳細目錄。

**[!UICONTROL Clock Number]**： （僅用於英國；僅供具有許可權的使用者使用）唯一識別碼，用於確保廣播正確的廣告。 如果此設定不適用，請保留空白。

### [!UICONTROL Pixel]

系統會自動附加位置的所有現有事件追蹤畫素。 您可以根據個別廣告的追蹤需求，分離現有畫素並視需要建立新畫素。 **秘訣：**&#x200B;若要使用[!UICONTROL Ad Tools]檢視一次編輯一個位置中多個廣告的第三方追蹤畫素，請參閱[將第三方追蹤畫素附加至位置中的廣告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)。

下列設定會套用至您建立或編輯的每個畫素。

**[!UICONTROL Integration Event]：**&#x200B;觸發畫素引發的事件。 對於此廣告型別，請使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上引發的畫素。

**[!UICONTROL Pixel Type]：**&#x200B;畫素是&#x200B;*[!UICONTROL IMG URL]* （1x1畫素影像檔）、*[!UICONTROL HTML]*&#x200B;或&#x200B;*[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]：**&#x200B;畫素影像的URL，以指定[!UICONTROL Pixel Type]的適當格式顯示。

**[!UICONTROL Pixel Name]：**&#x200B;畫素名稱。 使用有助於您輕鬆識別畫素的名稱。

**[!UICONTROL Pixel Provider]：**&#x200B;畫素提供者： *[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* 關於通用視訊的[常見問題集](/help/dsp/campaign-management/faq-universal-video.md)
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告](/help/dsp/campaign-management/ads/ad-list-placements.md)關聯的版位
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)
