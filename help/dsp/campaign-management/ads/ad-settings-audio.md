---
title: 音訊廣告設定
description: 請參閱音訊廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# 音訊廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限新廣告*

**[!UICONTROL URL]**： VAST標籤URL。

**[!UICONTROL Title]**：檔案的名稱，用於[!UICONTROL Ads]檢視和報告。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後按一下&#x200B;**[!UICONTROL Enter]**&#x200B;索引鍵。 如果標籤有效，您會在頂端附近看到包含`<VAST>`的XML檔案。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。 預設為&#x200B;*[!UICONTROL Audio]*。

**[!UICONTROL Ad Name]：**&#x200B;廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 使用當您在位置、[!UICONTROL Ads]檢視和報告中附加廣告時容易找到的名稱。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 30sec Audio）。

**[!UICONTROL Ad Duration]：**&#x200B;音訊檔案的長度。 視選取的廣告單位而定，此廣告會自動設為[!UICONTROL 15]或[!UICONTROL 30]。

此欄位不一定顯示，端視帳戶許可權而定。

**[!UICONTROL VAST Tag]：** （僅使用VAST標籤的廣告）協力廠商廣告來源的URL。 請確定VAST標籤僅包含音訊媒體檔案。

**[!UICONTROL Final VAST Tag]：** （僅使用VAST標籤的廣告）已插入第三方廣告來源的URL以及必要的[Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) （如果適用）。

**[!UICONTROL Select Rate]：** （僅具有許可權的使用者）透過Adobe計費的預先議定費率，或您已經議定且透過廠商計費的費率之一。 若要新增費率，請聯絡您的Adobe客戶團隊。

### [!UICONTROL Pixel]

系統會自動附加位置的所有現有事件追蹤畫素。 您可以根據個別廣告的追蹤需求，分離現有畫素並視需要建立新畫素。 **秘訣：**&#x200B;若要使用[!UICONTROL Ad Tools]檢視一次編輯一個位置中多個廣告的第三方追蹤畫素，請參閱[將第三方追蹤畫素附加至位置中的廣告](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)。

下列設定會套用至您建立或編輯的每個畫素。

**[!UICONTROL Integration Event]：**&#x200B;觸發畫素引發的事件。 對於此廣告型別，請使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上引發的畫素。

**[!UICONTROL Pixel Type]：**&#x200B;畫素是&#x200B;*[!UICONTROL IMG URL]* （1x1畫素影像檔）、*[!UICONTROL HTML]*&#x200B;或&#x200B;*[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]：**&#x200B;畫素影像的URL，使用指定畫素型別的適當格式。

**[!UICONTROL Pixel Name]：**&#x200B;畫素名稱。 使用有助於您輕鬆識別畫素的名稱。

**[!UICONTROL Pixel Provider]：**&#x200B;畫素提供者：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告](/help/dsp/campaign-management/ads/ad-list-placements.md)關聯的版位
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)
