---
title: 顯示廣告設定
description: 請參閱顯示廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# 顯示廣告設定

下列設定適用於標準顯示廣告。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。 預設為&#x200B;*[!UICONTROL Display]*。

**[!UICONTROL Ad Name]：**&#x200B;廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 使用當您在位置、[!UICONTROL Ads]檢視和報告中附加廣告時容易找到的名稱。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 300x250 Gamer」）。

**\[Ad Source\]**： （唯讀） *[!UICONTROL 3rd party]*。

**[!UICONTROL This is an expandable Banner]：** （僅限協力廠商廣告）指出廣告是可展開的橫幅廣告。 相關的擴充設定會決定要購買哪個詳細目錄，因此請確定它們反映了廣告行為。

**[!UICONTROL Expansion Method]：** （僅限協力廠商可展開的橫幅廣告）橫幅是否展開至&#x200B;*[!UICONTROL Click]*&#x200B;或&#x200B;*[!UICONTROL Rollover]*。

**[!UICONTROL Expansion Directions]：** （僅限協力廠商可展開的橫幅廣告）廣告展開的方向： *[!UICONTROL Up]*、*[!UICONTROL Down]*、*[!UICONTROL Left]*&#x200B;或&#x200B;*[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]：** （僅限協力廠商可展開的橫幅廣告）廣告可用的認證廠商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])、*[!UICONTROL Flashtalking]*、*[!UICONTROL Sizmek]*&#x200B;或&#x200B;*[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]：** （僅限第三方廣告）第三方創意資產的URL。 任何[timestamp]和[[timestamp]]引數都會被實際值取代。

**[!UICONTROL Final Display Code]：** （僅限協力廠商廣告）插入協力廠商創意資產的URL，並插入必要的[Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) （如果適用）。

**[!UICONTROL Ad Size]：**&#x200B;廣告的寬度和高度。 它必須是[支援的標準顯示廣告大小](ad-specs.md)。 您可以在上傳廣告前手動輸入廣告大小或輸入[!UICONTROL Display Code]。 如果您未輸入廣告大小，上傳的廣告或廣告標籤的維度會自動輸入為唯讀。

>[!IMPORTANT]
>
> 在寬度和高度欄位中宣告的廣告大小會與傳入的競標要求相符。 如果廣告的維度與宣告的廣告大小不符，您可能會遇到傳送問題。

### [!UICONTROL Pixel]

系統會自動附加位置的所有現有事件追蹤畫素。 您可以根據個別廣告的追蹤需求，分離現有畫素並視需要建立新畫素。 **秘訣：**&#x200B;若要使用[!UICONTROL Ad Tools]檢視一次編輯一個位置中多個廣告的第三方追蹤畫素，請參閱[將第三方追蹤畫素附加至位置中的廣告](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)。

下列設定會套用至您建立或編輯的每個畫素。

**[!UICONTROL Integration Event]：**&#x200B;觸發畫素引發的事件。 對於此廣告型別，請使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上引發的畫素。

**[!UICONTROL Pixel Type]：**&#x200B;畫素是&#x200B;*[!UICONTROL IMG URL]* （1x1畫素影像檔）、*[!UICONTROL HTML]*&#x200B;或&#x200B;*[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]：**&#x200B;畫素影像的URL，以指定[!UICONTROL Pixel Type]的適當格式顯示。

**[!UICONTROL Pixel Name]：**&#x200B;畫素名稱。 使用有助於您輕鬆識別畫素的名稱。

**[!UICONTROL Pixel Provider]：**&#x200B;畫素提供者： *[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告](ad-list-placements.md)關聯的版位
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)
