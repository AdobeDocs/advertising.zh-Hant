---
title: 動態創意設定
description: 參考動態創意作品的設定。
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 4e809ac18720f22f636b2df2ad4a5b1db355e729
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# 動態創意設定

<!-- add a description -->

## 動態廣告設定<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### 基本詳細資訊

**[!UICONTROL Creative Type]：**&#x200B;創意內容是&#x200B;*[!UICONTROL Display]*&#x200B;廣告(HTML5)或&#x200B;*[!UICONTROL Video]*&#x200B;廣告。

**[!UICONTROL Dynamic Display Ad Name]**&#x200B;或&#x200B;**[!UICONTROL Dynamic Video Ad Name]：**&#x200B;創意的唯一名稱。

**[!UICONTROL Advertiser]：**&#x200B;要為其建立廣告的廣告商。 如果您是從[!UICONTROL Creatives] > [!UICONTROL Creative Libraries]內建立廣告，則廣告商已選取且為唯讀。

**[!UICONTROL Library]：**&#x200B;要建立廣告的創意內容庫。 如果您是從[!UICONTROL Creatives] > [!UICONTROL Creative Libraries]內建立廣告，則資料庫名稱已經選取且是唯讀的。

**[!UICONTROL Ad Template Size]：** （僅限動態顯示廣告）要從中建立廣告之廣告範本的[廣告維度](/help/creative/creative-libraries/creative-sizes.md)。 如果您先選取特定[!UICONTROL Ad Template]，則會自動選取此值。

## 廣告範本

**[!UICONTROL Ad Template]：**&#x200B;用來建立廣告的廣告範本。 選取現有的廣告範本，或上傳新的廣告範本，然後選取範本型別（*靜態*&#x200B;或&#x200B;*動態*）。 範本必須是ZIP格式並包含：<!-- Need to add more specs for templates -->

* 顯示創意：具有所需廣告格式的HTML5檔案，以及具有廣告屬性(.tdf)的檔案(僅限動態HTML5廣告)

* 影片創意：具有所需廣告格式的.scene檔案。 ZIP檔案最大可達512 MB。

若要繼續，請按一下&#x200B;**[!UICONTROL Select Ad Template]**。

**[!UICONTROL Card Count (Max 50)]：** （僅限顯示廣告）轉盤中顯示的產品數量。

**[!UICONTROL Duration]：** （僅限視訊廣告；唯讀）從選取的廣告範本衍生的視訊持續時間。 每個視訊的持續時間必須介於1至90秒之間。

## 目錄

**[!UICONTROL Template]：**&#x200B;用來建立廣告的摘要範本。

**\[Catalogs\]**：要從中產生廣告的一或多個目錄。 選取現有目錄，或下載現有摘要範本並建立及上傳新目錄來建立新目錄。 按一下&#x200B;**[!UICONTROL Select Catalog]**。

上傳的目錄必須採用ZIP格式並包含以下專案：

* （動態顯示和視訊廣告）一或多個CSV、TSV或Microsoft Excel試算表(XLSX)格式的摘要檔案。 檔案大小上限為512 MB。<!-- Need to add more specs for the feed files -->

* （顯示廣告） GIF、JPEG、JPG或PNG格式的影像資產

* （影片廣告）MP4、MOV或WEBM格式的影片資產。 支援的廣告範本包括開始卡、結束卡、頂端覆蓋、底部覆蓋或L形。 每個視訊的持續時間必須介於1至90秒之間。

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**： <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->摘要檔案中必須有值才能建立廣告的欄型別： *[!UICONTROL Profile data]*、*[!UICONTROL Geographic data]、*[!UICONTROL Data pass]、*[!UICONTROL Audience Segment]*。  **注意：**&#x200B;這些設定與廣告體驗設定中的進階設定分開運作。<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]：**

將指定廣告範本中的每個屬性（動態廣告欄位）對應到指定目錄（目錄標籤）中的欄，或輸入靜態值。

>[!MORELIKETHIS]
>
>* [將動態創意內容新增至創意內容庫](creative-add-dynamic.md)
>* [在創意程式庫中編輯動態創意內容](creative-edit-dynamic.md)
>* [動態廣告的工作流程](/help/creative/introduction/workflow-dynamic-ads.md)
