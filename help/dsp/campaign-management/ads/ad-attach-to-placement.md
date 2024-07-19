---
title: 將廣告附加至刊登版位
description: 瞭解如何將廣告附加至刊登版位。
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# 將廣告附加至刊登版位

使用[!UICONTROL Ad Tools]檢視將廣告附加至位置、將協力廠商追蹤畫素附加至廣告，以及將現有的協力廠商追蹤畫素與廣告分離。

>[!NOTE]
>
>通用視訊廣告只能附加至通用視訊位置。

## 開啟[!UICONTROL Ad Tools]檢視 {#ad-tools-open}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 以下列任一方式開啟[!UICONTROL Ad Tools]檢視：

   * （從[!UICONTROL Packages] 、 [!UICONTROL Placements]或[!UICONTROL Ads]檢視）按一下右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**。

   * （從[!UICONTROL Placements]檢視）按一下位置名稱旁的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * （從[!UICONTROL Ads]檢視）在廣告名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**」。

   預設會選取[!UICONTROL Attach Ads]標籤。

## 將廣告附加至刊登版位 {#attach-ads-campaign}

1. [開啟[!UICONTROL Ad Tools]檢視](#ad-tools-open)。

1. 在[!UICONTROL Edit]子檢視中，針對您想要附加至刊登版位的每個廣告群組執行下列動作：

   1. （選用）透過下列任一方式找出特定版位和廣告：

      * 在左方表格上方，按一下![篩選器](/help/dsp/assets/filter.png)，並依套件、版位型別、版位狀態、廣告型別或廣告狀態來篩選清單。

      * 在右側和左側表格上方，搜尋版位和廣告名稱中的特定文字字串。

   1. 在左側表格中，選取要附加廣告的每個位置旁的核取方塊。

   1. 在右側表格中，選取您要附加至所選版位的每個廣告旁的核取方塊。

      只有適用於版位型別且尚未附加至所選版位的廣告才可供選取。

   1. 按一下右下角的&#x200B;**[!UICONTROL Attach]**。

1. （選擇性）若要返回行銷活動詳細檢視，請按一下![返回資料夾](/help/dsp/assets/breadcrumb-return.png "返回資料夾[!UICONTROL Ad Tools]左邊的資料夾")並選取行銷活動名稱。

## 檢視附加至刊登版位的廣告 {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [開啟[!UICONTROL Ad Tools]檢視](#ad-tools-open)。

1. 切換至右上角的&#x200B;**[!UICONTROL View]**&#x200B;選項。

1. （選用）視需要尋找特定版位和廣告：

   * 在左方表格上方，按一下![篩選器](/help/dsp/assets/filter.png)，並依套件、版位型別、版位狀態、廣告型別或廣告狀態來篩選清單。

   * 在右側和左側表格中，搜尋位置或廣告名稱中的特定文字字串。

1. 按一下左側表格中的任何位置列，檢視右側表格中的附加廣告。

1. （選用）若要在行銷活動的版位中附加更多廣告，請切換至右上角的&#x200B;**[!UICONTROL Edit]**&#x200B;檢視。 如需指示，請參閱先前程式中的步驟2 &quot;[將廣告附加至刊登版位](#attach-ads-campaign)&quot;。

## 將協力廠商追蹤畫素附加至位置中的廣告 {#attach-pixels-ads}

1. [開啟[!UICONTROL Ad Tools]檢視](#ad-tools-open)。

1. 按一下「**[!UICONTROL Attach Pixels]**」標籤。

1. 在[!UICONTROL Edit]子檢視中：

   1. （選用）以下列任一方式找出廣告和協力廠商畫素：

      * 在左方表格上方，按一下![篩選](/help/dsp/assets/filter.png)，然後依廣告狀態、廣告型別、畫素整合事件或畫素型別來篩選清單。

      * 在右側和左側表格上方，搜尋廣告名稱和畫素名稱中的特定文字字串。

   1. （如果行銷活動不存在協力廠商追蹤畫素）建立畫素：

      1. 在右表中，按一下&#x200B;**[!UICONTROL Create pixel]**。

      1. 指定設定：

         **[!UICONTROL Integration Event]：**&#x200B;觸發畫素引發的事件，例如&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*。

         **[!UICONTROL Pixel Type]：**&#x200B;畫素是&#x200B;*[!UICONTROL IMG URL]* （1x1畫素影像檔）、*[!UICONTROL HTML]*&#x200B;或&#x200B;*[!UICONTROL JavaScript URL]*。

         **[!UICONTROL Pixel URL or Code]：**&#x200B;畫素影像的URL，使用指定畫素型別的適當格式。

         **[!UICONTROL Pixel Name]：**&#x200B;畫素名稱。 使用有助於您輕鬆識別畫素的名稱。

         **[!UICONTROL Pixel Provider]：**&#x200B;畫素提供者： *[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

      1. 按一下&#x200B;**[!UICONTROL Save]**。

   1. 在左側表格中，選取您要附加協力廠商追蹤畫素的每個廣告旁的核取方塊。

   1. 在右側表格中，選取您要附加至所選廣告的每個協力廠商追蹤畫素旁的核取方塊。

      只有尚未附加至所選取廣告的畫素才可供選取。

   1. 按一下右下角的&#x200B;**[!UICONTROL Attach]**。

1. （選擇性）若要返回行銷活動詳細檢視，請按一下![返回資料夾](/help/dsp/assets/breadcrumb-return.png "返回資料夾[!UICONTROL Ad Tools]左邊的資料夾")並選取行銷活動名稱。

## 將第三方追蹤畫素與位置中的廣告分離 {#detach-pixels-ads}

1. [開啟[!UICONTROL Ad Tools]檢視](#ad-tools-open)。

1. 按一下「**[!UICONTROL Attach Pixels]**」標籤。

1. 在[!UICONTROL Edit]子檢視中：

   1. （選用）以下列任一方式找出廣告和協力廠商畫素：

      * 在左方表格上方，按一下![篩選](/help/dsp/assets/filter.png)，然後依廣告狀態、廣告型別、畫素整合事件或畫素型別來篩選清單。

      * 在右側和左側表格上方，搜尋廣告名稱和畫素名稱中的特定文字字串。

   1. 在左側表格中，選取每個您要中斷協力廠商追蹤畫素連線的廣告旁的核取方塊。

   1. 在右側表格中，選取您要從所選廣告分離的每個協力廠商追蹤畫素旁的核取方塊。

      只有附加到所有選取廣告的畫素是可選的。

   1. 按一下右下角的&#x200B;**[!UICONTROL Detach]**。

1. （選擇性）若要返回行銷活動詳細檢視，請按一下![返回資料夾](/help/dsp/assets/breadcrumb-return.png "返回資料夾[!UICONTROL Ad Tools]左邊的資料夾")並選取行銷活動名稱。

## 檢視附加至廣告的畫素 {#view-pixels-ads}

1. [開啟[!UICONTROL Ad Tools]檢視](#ad-tools-open)。

1. 按一下「**[!UICONTROL Attach Pixels]**」標籤。

1. 切換至右上角的&#x200B;**[!UICONTROL View]**&#x200B;選項。

1. （選用）視需要尋找廣告和協力廠商畫素：

   * 在左方表格上方，按一下![篩選](/help/dsp/assets/filter.png)，然後依廣告狀態、廣告型別、畫素整合事件或畫素型別來篩選清單。

   * 在右側和左側表格上方，搜尋廣告名稱和畫素名稱中的特定文字字串。

1. 按一下左側表格中的任何廣告列，可檢視右側表格中附加的畫素。

1. （選擇性）若要在廣告上附加更多畫素，請切換至右上角的&#x200B;**[!UICONTROL Edit]**&#x200B;檢視。 如需指示，請參閱先前程式中的步驟3，「[將協力廠商追蹤畫素附加至位置](#attach-pixels-ads)中的廣告」。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [建立多個協力廠商廣告](ad-create-multiple.md)
>* [編輯廣告](ad-edit.md)
>* [列出與廣告](ad-list-placements.md)關聯的版位
>* [編輯刊登版位的廣告排程](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* 關於通用視訊的[常見問題集](/help/dsp/campaign-management/faq-universal-video.md)
