---
title: 動態創意設定
description: 參考動態創意作品的設定。
feature: Creative Dynamic Creatives
source-git-commit: f0bbbfb528000babbcb2c4c6915b62e81f477bda
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# 動態創意設定

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## 動態廣告設定<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### 基本詳細資訊

**[!UICONTROL Dynamic Ad Name]：**&#x200B;創意的唯一名稱。

**[!UICONTROL Advertiser]：**&#x200B;要為其建立廣告的廣告商。

**[!UICONTROL Library]：**&#x200B;要建立廣告的創意內容庫。 如果您是從[!UICONTROL Creatives] > [!UICONTROL Creative Libraries]內建立廣告，則資料庫名稱已經選取且是唯讀的。

**[!UICONTROL Ad Template Size]：**&#x200B;要從中建立廣告之廣告範本的[廣告維度](/help/creative/creative-libraries/creative-sizes.md)。 如果您先選取特定[!UICONTROL Ad Template]，則會自動選取此值。

## 廣告範本

**[!UICONTROL Ad Template]：**&#x200B;用來建立廣告的廣告範本。 選取現有的廣告範本，或上傳新的廣告範本，然後選取範本型別（*靜態*&#x200B;或&#x200B;*動態*）。 上傳的範本必須是ZIP格式，並包含HTML5檔案和範本定義檔案(template.TDF)。<!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]：**&#x200B;要顯示在輪播中的產品數量。

## 目錄

**[!UICONTROL Template]：**&#x200B;用來建立廣告的摘要範本。

**\[Catalogs\]**：要從中產生廣告的一或多個目錄。 選取現有目錄，或下載現有摘要範本並建立及上傳新目錄來建立新目錄。

上傳的目錄必須採用ZIP格式並包含以下專案：

* 一或多個CSV、TSV或Microsoft Excel試算表(XLSX)格式的摘要檔案。<!-- Need to add more specs for that -->

* GIF、JPEG、JPG或PNG格式的影像資產

* （選用） MP4或WEBM格式的視訊資產

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**： <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->摘要檔案中必須有值才能建立廣告的欄型別： *[!UICONTROL Profile data]*、*[!UICONTROL Geographic data]、*[!UICONTROL Data pass]、*[!UICONTROL Audience Segment]*。  **注意：**&#x200B;這些設定與廣告體驗設定中的進階設定分開運作。<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]：**

將指定廣告範本中的每個屬性（動態廣告欄位）對應到指定目錄（目錄標籤）中的欄，或輸入靜態值。

>[!MORELIKETHIS]
>
>* [將動態創意內容新增至創意內容庫](creative-add-dynamic.md)
>* [在創意程式庫中編輯動態創意內容](creative-edit-dynamic.md)
>* [動態廣告的工作流程](/help/creative/introduction/workflow-dynamic-ads.md)
