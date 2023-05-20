---
title: 通用視頻廣告設定
description: 請參閱通用視頻廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 0c9e9c8d2a3444c623568d25262421be53c0c846
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# 通用視頻廣告設定

*開放測試版功能*

>[!NOTE]
>
>通用視頻廣告只能附在通用視頻放映上。

## [!UICONTROL Insert Ad Tag]

*僅新廣告*

**[!UICONTROL URL]:** VAST標籤URL。

**[!UICONTROL Title]:** 檔案的標題，位於 [!UICONTROL Ads] 查看和報告。

>[!TIP]
>
> 要檢查VAST標籤的有效性，請將其貼上到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 按鈕 如果標籤有效，您將看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 使用將廣告附加到位置時容易找到的名稱， [!UICONTROL Ads] 視圖和報表中。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：30秒通用視頻」)。

**[!UICONTROL Show Controls]:** 廣告的視頻控制項包括的位置： *[!UICONTROL Under]*。 *[!UICONTROL Over]*。 *[!UICONTROL Bottom]*&#x200B;或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留視頻的寬度和高度比例(*[!UICONTROL Yes]*)或拉伸視頻以填充可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；只讀)作為廣告源輸入的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；只讀)作為廣告源輸入的第三方VAST標籤 [廣告DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Wmode]:** 窗口模式： *[!UICONTROL window]*。 *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*。 如果此設定不適用，則將其留空。

**[!UICONTROL Video Format]:** 潛在清單的廣告播放器的格式： *[!UICONTROL VPAID]*。 *[!UICONTROL VPAID & VAST]*&#x200B;或 *[!UICONTROL VAST]*。 可視性始終為 [!UICONTROL VPAID]但 [!UICONTROL VPAID & VAST] 包括不允許可查看性度量的庫存。 如果可視性指標對您的市場活動很重要，請考慮這一區別。

使用 [!UICONTROL VAST]當您瞄準僅嚴格要求VAST格式的連接電視或清單(通常來自諸如Google廣告經理、Appnexus、SpotX和Freewheel等供應源)時，不允許查看性測量。 此選項還用於以前與標準預卷(VAST)或電話+平板電腦標準預卷(VAST)放置/廣告相容的庫存。

**[!UICONTROL Clock Number]**:(僅在聯合王國使用；僅對具有權限的用戶可用)用於確保廣播正確廣告的唯一標識符。 如果此設定不適用，則將其留空。

### [!UICONTROL Pixel]

位置的所有現有事件跟蹤像素都會自動附加。 您可以根據對單個廣告的跟蹤需求分離現有像素並根據需要建立新像素。

以下設定適用於您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素觸發的事件。 對於此廣告類型，使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*。

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，格式與指定的 [!UICONTROL Pixel Type]。

**[!UICONTROL Pixel Name]:** 像素名稱。 使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供器： *[!UICONTROL None]*。 *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [關於通用視頻的常見問題](/help/dsp/campaign-management/faq-universal-video.md)
>* [關於廣告管理](ad-about.md)
>* [建立單個廣告](ad-create.md)
>* [列出與廣告關聯的放置](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [宏DSP](/help/dsp/campaign-management/macros.md)

