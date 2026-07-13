---
title: 在Creative Studio中管理廣告範本
description: 瞭解如何在Adobe Advertising Creative的「Creative Studio範本」索引標籤中建立、匯入、整理及管理廣告範本。
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d4a041529615006a79093dccb8690f3b9f5e8cba
workflow-type: tm+mt
source-wordcount: 2512
ht-degree: 2%

---

# 在[!UICONTROL Creative Studio]中管理廣告範本

*Beta功能*

建立、匯入和管理顯示和視訊廣告範本，以用於廣告產生工作階段。

## [!UICONTROL Creative Studio] > [!UICONTROL Templates]檢視

**[!UICONTROL Templates]**&#x200B;索引標籤提供建立或匯入新廣告範本的快速動作。

此索引標籤也會在頁面<!-- Only in the Templates tab -->底部將您現有的廣告範本列為[個別卡片（預設）或表格/清單](/help/creative/introduction/customize-data-views.md)。 廣告範本清單包含[!UICONTROL All]、[!UICONTROL System Templates] （由您的Adobe帳戶團隊上傳至您的帳戶）和[!UICONTROL User Templates]的標籤。 依預設，會顯示所有廣告商的廣告範本。 若只要檢視特定廣告商的廣告範本，請從頁面頂端的廣告商清單中選取。

<!-- 
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### 可用動作

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

建立：

* [匯入HTML5廣告範本](#templates-import)

* [手動建立廣告範本](#template-create)

對現有範本的動作：

* [從顯示廣告範本產生廣告變化](#ad-variations-generate)

* [編輯廣告範本](#template-edit)

* [新增或移除廣告範本的標籤](#template-labels)

* [預覽廣告範本](#template-preview)

* [下載廣告範本](#template-download)

* [將廣告範本新增或移除為最愛](#template-favorite)

* [刪除廣告範本](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## 匯入HTML5廣告範本 {#templates-import}

上傳一或多個預先建立的HTML5範本（這些範本會封裝為ZIP檔案）。 匯入時會驗證範本；如果HTML超過200,000個字元、CSS超過60,000個字元、範本包含超過5,000個DOM元素，或範本包含不支援的指令碼標籤，則匯入會失敗。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 選取頁面頂端的廣告商。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 在&#x200B;**[!UICONTROL Upload HTML5 Templates]**&#x200B;方塊中，按一下&#x200B;**[!UICONTROL Upload]**，然後選取&#x200B;**[!UICONTROL Display Ad Template]**&#x200B;或&#x200B;**[!UICONTROL Video Ad Template]**。

1. 從您的裝置或網路選取一或多個ZIP檔案。

1. 在&#x200B;**[!UICONTROL Import Templates]**&#x200B;對話方塊：

   1. 選取&#x200B;**[!UICONTROL Advertiser]**。

      如果您已在頁面頂端選取特定廣告商，則會預先選取該廣告商。

   1. （選擇性）針對每個檔案，編輯&#x200B;**[!UICONTROL Template Name]**。

      預設會使用檔案名稱。

   1. （選擇性）若要新增更多檔案，請按一下&#x200B;**[!UICONTROL Add more]**&#x200B;並選取其他ZIP檔案。 指定每個額外檔案的&#x200B;**[!UICONTROL Template Name]**。

1. 按一下&#x200B;**[!UICONTROL Import Templates]**。

>[!NOTE]
>
>如果匯入失敗，請簡化範本或聯絡您的Adobe客戶團隊。

## 手動建立廣告範本 {#template-create}

使用範本編輯器建立空白顯示區或視訊範本。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 在&#x200B;**[!UICONTROL Create New Ad Template]**&#x200B;方塊中，按一下&#x200B;**[!UICONTROL Create]**，然後選取&#x200B;**[!UICONTROL Display Ad Template]**&#x200B;或&#x200B;**[!UICONTROL Video Ad Template]**。

1. （顯示廣告）選取廣告範本大小，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 使用範本編輯器](#template-controls)中的[控制項來設定範本設定。

1. （選擇性）若要下載已定義的範本復本，請按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   檔案會依照瀏覽器的正常程式下載。

1. 儲存範本：

   1. 執行下列任一項作業：

      * 按一下&#x200B;**[!UICONTROL Save]**。

      * 若要將範本儲存為草稿，請按一下「**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**」。

   1. 輸入&#x200B;**[!UICONTROL Template name]**、選取&#x200B;**[!UICONTROL Advertiser]**、選擇性地選取現有標籤或新增標籤至範本，然後按一下&#x200B;**[!UICONTROL Save]**。

## 編輯廣告範本 {#template-edit}

*僅顯示廣告範本。*

>[!IMPORTANT]
>
>AI代理程式無法變更範本版面、元素位置、間距或印刷樣式。 在產生內容之前，在範本編輯器中進行任何結構性變更。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Template]**。

1. 在範本編輯器](#template-controls)中使用[控制項來編輯範本配置或元素。

1. （選擇性）若要下載已定義的範本復本，請按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   檔案會依照瀏覽器的正常程式下載。

1. 儲存範本：

   * 按一下&#x200B;**[!UICONTROL Save]**。

   * 若要將範本儲存為草稿，請按一下「**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**」。 輸入&#x200B;**[!UICONTROL Template name]**、選取&#x200B;**[!UICONTROL Advertiser]**、選擇性地選取現有標籤或新增標籤至範本，然後按一下&#x200B;**[!UICONTROL Save]**。

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## 範本編輯器控制項 {#template-controls}

顯示和視訊範本編輯器共用編輯畫布和右側[!UICONTROL Layers]面板上方的一般動作工具列。 左側面板、廣告範本編輯控制項，以及時間軸在顯示和視訊範本之間有所不同。

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### 一般動作工具列

一般動作工具列位於廣告範本編輯器的編輯畫布上方，並分成兩部分（左和右）。

#### 顯示廣告範本

| 控制 | 說明 |
| --- | --- |
| **[!UICONTROL Undo]** | 復原上一個動作。 |
| ![取消復原](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | 重新執行上一個復原的動作。 |
| **[!UICONTROL Links]** | 開啟面板以管理附加至範本中元素的點進URL。 |
| 縮放控制項 | 按一下&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;以調整畫布放大率（10%-150%，以10%為增量）。 按一下縮放等級標籤（當畫布自動符合時顯示&#x200B;**[!UICONTROL Auto]**，或手動設定時顯示百分比）以開啟具有下列選項的功能表： **[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**。 |
| 廣告大小 | 顯示目前的廣告維度（例如300 × 250）。 按一下以開啟大小選擇器，選擇器提供六種常用的IAB標準大小作為卡片，以及包含所有19個標準IAB顯示廣告大小的下拉式清單。 新範本的預設大小為300 × 250 （Medium矩形）。 |
| ![開啟圖層面板](/help/creative/assets/layers-panel-open.png "開啟圖層面板") | 開啟[!UICONTROL Layers]面板。 僅在[!UICONTROL Layers]面板關閉時顯示。 |

#### 影片廣告範本

| 控制 | 說明 |
| --- | --- |
| **[!UICONTROL Undo]** / ![取消復原](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | 復原或重新復原上一個動作。 |
| 縮放控制項 | 按一下&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;以調整畫布放大比例。 按一下縮放等級以開啟包含下列選項的功能表： **[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**。 |
| ![開啟圖層面板](/help/creative/assets/layers-panel-open.png "開啟圖層面板") | 開啟[!UICONTROL Layers]面板。 僅在[!UICONTROL Layers]面板關閉時顯示。 |

<!-- Not there as of 7/10:  | **[!UICONTROL Preview]** | Opens a preview of the video template. | -->

### 左側面板

左側面板包含一欄圖示。 按一下圖示以開啟其內容面板；再按一下相同圖示以將其關閉。

#### 顯示廣告範本

| 圖示 | 說明 |
| --- | --- |
| **[!UICONTROL Search]** | 在您的資料庫中搜尋所有資產型別。 |
| **[!UICONTROL Upload]** | 將影像或字型檔案上傳到編輯器以用於目前的範本。 您一次最多可上傳20個檔案。 |
| **[!UICONTROL Templates]** | 從您的Creative Studio資料庫瀏覽廣告範本，以用作基礎圖層或參考元素。 |
| **[!UICONTROL My Assets]** | 在Creative Studio Assets索引標籤中瀏覽您已上傳的所有資產。 |
| **[!UICONTROL Images]** | 僅瀏覽您在Creative Studio Assets標籤中上傳的影像資產。 |
| **[!UICONTROL Text]** | 將文字元素新增至畫布，包括您已上傳的任何自訂字型。 |
| **[!UICONTROL Elements]** | 新增形狀和版面配置元素，例如按鈕和矩形。 |

您可以從任何面板將專案直接拖曳到畫布上，或按一下專案以將其置於預設位置。

#### 影片廣告範本

| 圖示 | 說明 |
| --- | --- |
| **[!UICONTROL Search]** | 在您的資料庫中搜尋所有資產型別。 |
| **[!UICONTROL Upload]** | 將影像、視訊、音訊或字型檔案(TTF、OTF、WOFF、WOFF2)上傳到編輯器，以便在目前的範本中使用。 您一次最多可上傳20個檔案。 |
| **[!UICONTROL Templates]** | 從您的Creative Studio資料庫瀏覽廣告範本。 |
| **[!UICONTROL My Assets]** | 在Creative Studio Assets索引標籤中瀏覽您已上傳的所有資產。 |
| **[!UICONTROL Images]** | 僅瀏覽您在Creative Studio Assets標籤中上傳的影像資產。 |
| **[!UICONTROL Video]** | 僅瀏覽您在Creative Studio Assets標籤中上傳的視訊資產。 |
| **[!UICONTROL Audio]** | 僅瀏覽您在Creative Studio Assets索引標籤中上傳的音訊資產。 |
| **[!UICONTROL Text]** | 將文字元素新增至畫布，包括您已上傳的任何自訂字型。 |
| **[!UICONTROL Elements]** | 新增形狀與向量元素。 |

您可以從任何面板將專案直接拖曳到畫布上，或按一下專案以將其置於預設位置。

### 廣告範本編輯控制項

按一下編輯畫布上的元素以選取它。 視範本型別而定，會顯示一或多個包含該元素控制項的工具列。

#### 檢視窗工具列和面板

控制項會因元素型別而異。

<!-- From inspectorbar.ts -->

##### 顯示廣告範本

| 控制 | 元素型別 | 說明 |
| --- | --- | --- |
| **[!UICONTROL Properties]** | 全部 | 開啟面板以編輯圖層名稱；將圖層標示為動態（在廣告產生期間可交換）；並設定點進URL （僅限連結）。 在它下方，選擇&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;狀態以設定該互動狀態的元素樣式，然後根據元素型別調整樣式 — 印刷樣式（僅限文字和連結）、裝飾（填色、邊框、圓角半徑）、維度、位置。 |
| **[!UICONTROL Effects]** | 全部 | 開啟一個面板，您可在其中選擇要針對該互動狀態套用效果的&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;狀態，然後調整&#x200B;**[!UICONTROL Transform]**、**[!UICONTROL Transition]**、**[!UICONTROL Box Shadow]**、**[!UICONTROL Filter]**、**[!UICONTROL Blend Mode]**&#x200B;和&#x200B;**[!UICONTROL Cursor]**&#x200B;區段。 文字元素也包含&#x200B;**[!UICONTROL Text Shadow]**&#x200B;區段。 |
| **[!UICONTROL Animations]** | 全部 | 開啟面板以設定圖層在時間軸上的進入和退出時間，並設定&#x200B;**[!UICONTROL Entrance Animation]**、**[!UICONTROL Loop Animation]**&#x200B;和&#x200B;**[!UICONTROL Exit Animation]**&#x200B;預設集具有持續期間和緩動。 包含&#x200B;**[!UICONTROL Copy]**、**[!UICONTROL Paste]**&#x200B;和&#x200B;**[!UICONTROL Reset]**&#x200B;動作。 |
| **[!UICONTROL Crop]** | 影像 | 開啟工具列以裁切影像。 選取&#x200B;**[!UICONTROL Aspect Ratio]**&#x200B;預設集（或&#x200B;**[!UICONTROL Free]**），然後按一下&#x200B;**[!UICONTROL Apply]**&#x200B;或&#x200B;**[!UICONTROL Cancel]**。 |
| **[!UICONTROL Position]** | 全部 | 開啟包含&#x200B;**[!UICONTROL Move]**&#x200B;選項(**[!UICONTROL Forward]**、**[!UICONTROL Backward]**、**[!UICONTROL To front]**、**[!UICONTROL To back]**)、**[!UICONTROL Align to Page]**&#x200B;選項(**[!UICONTROL Top]**、**[!UICONTROL Left]**、**[!UICONTROL Middle]**、**[!UICONTROL Center]**、**[!UICONTROL Bottom]**、**[!UICONTROL Right]**、**[!UICONTROL Fit Vertically]**、**[!UICONTROL Fit Horizontally]**、**[!UICONTROL Fit to Page]**)的功能表，非影像元素則開啟&#x200B;**[!UICONTROL Layer Level Alignment]**&#x200B;選項（相同的六個對齊選項，加上&#x200B;**[!UICONTROL Fit to Content]**）。 |

##### 影片廣告範本

| 控制 | 元素型別 | 說明 |
| --- | --- | --- |
| **[!UICONTROL Shape]** | 形狀 | 設定形狀特定的選項。 |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | 多個選取的元素或群組 | 將選取的元素群組在一起，或取消選取群組的群組。 |
| **[!UICONTROL Combine]** | 相容的形狀 | 將選取的形狀組合成單一形狀。 |
| **[!UICONTROL Audio replace]** | 音訊和視訊 | 以資產庫中的檔案取代音訊。 |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | 文字 | 調整字型系列、粗細、大小、水準對齊方式及其他進階印刷樣式設定。 |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | 影像和視訊 | 設定元素的填色影像或視訊來源。 |
| **[!UICONTROL Trim]** | 視訊與音訊 | 開啟裁剪模式以設定剪輯的起點和終點。 |
| ![磁碟區](/help/creative/assets/volume.png "磁碟區") ([!UICONTROL Volume]) | 視訊與音訊 | 調整音訊等級。 |
| ![播放速度](/help/creative/assets/speed.png "播放速度") ([!UICONTROL Playback speed]) | 視訊與音訊 | 調整播放速率。 |
| ![裁切](/help/creative/assets/crop.png "裁切") ([!UICONTROL Crop]) | 全部 | 裁切元素至自訂區域。 |
| ![筆畫](/help/creative/assets/stroke.png "筆畫") ([!UICONTROL Stroke]) | 全部 | 設定框線顏色和寬度。 |
| **[!UICONTROL Text Background]** | 文字 | 在文字後面新增背景顏色。 |
| **[!UICONTROL Animations]** | 全部 | 新增或編輯輸入、結束或回圈動畫。 |
| **[!UICONTROL Style]** | 全部 | 開啟包含&#x200B;**[!UICONTROL Adjustments]**、**[!UICONTROL Filter]**、**[!UICONTROL Effect]**&#x200B;和&#x200B;**[!UICONTROL Blur]**&#x200B;選項的功能表。 |
| **[!UICONTROL Shadow]** | 全部 | 新增或編輯陰影。 |
| **[!UICONTROL Opacity]** | 全部 | 設定元素的透明度等級。 |
| **[!UICONTROL Position]** | 全部 | 以數值方式調整元素的大小、位置和旋轉。 |

#### 一般編輯控制項

##### 顯示廣告範本

| 動作 | 說明 |
| --- | --- |
| **[!UICONTROL Replace]** | （僅限影像元素）開啟「影像」面板，讓您可以使用資產庫中的影像來取代影像。 |
| ![前進](/help/creative/assets/cs-icon-move-forward.png) **[!UICONTROL Move forward]** | 以棧疊順序將元素向前移動一步（向前）。 |
| ![向後移動](/help/creative/assets/cs-icon-move-backward.png) **[!UICONTROL Move backward]** | 以棧疊順序向後移動元素一步（向後）。 |
| ![重複](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate]** | 建立元素的復本。 |
| ![刪除](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete]** | 從畫布移除元素。 |

您也可以拖曳選取的元素來重新定位它，並拖曳它周圍的控點來調整它的大小。

##### 影片廣告範本

| 動作 | 說明 |
| --- | --- |
| **[!UICONTROL Edit text]** | （僅限文字元素）切換到文字編輯模式，以便您可以直接在畫布上輸入文字並設定文字格式。 在文字編輯模式中，次要功能表會提供&#x200B;**[!UICONTROL Text color]**、**[!UICONTROL Bold]**、**[!UICONTROL Italic]**&#x200B;和&#x200B;**[!UICONTROL Text variables]** （範本預留位置）。 |
| **[!UICONTROL Replace]** | （僅限影像元素）開啟資產庫以便交換影像。 |
| **[!UICONTROL Bring forward]** | 以棧疊順序將元素向前移動一步。 |
| **[!UICONTROL Send backward]** | 以棧疊順序向後移動元素一步。 |
| **[!UICONTROL Duplicate]** | 建立元素的復本。 |
| **[!UICONTROL Delete]** | 從畫布移除元素。 |
| **... >[!UICONTROL Flip horizontal]** | 將元素水準翻轉180度。 |
| **... >[!UICONTROL Flip vertical]** | 將元素垂直翻轉180度。 |
| **... >[!UICONTROL Copy Element]** | 將元素複製到畫布剪貼簿。 |
| **... >[!UICONTROL Pastes Element]** | 貼上複製的元素。 |

您也可以拖曳選取的元素來重新定位它，並拖曳它周圍的控點來調整它的大小。

### 時間軸

顯示和視訊編輯器都會在畫布底部顯示時間軸面板。

#### 顯示廣告範本

時間軸會顯示畫布上每個圖層的軌跡，根據圖層進入和結束的動畫時間，跨越圖層可見的時間範圍。 拖曳軌跡的開始或結束操作框以調整其進入或結束時間，或拖曳軌跡以重新排序圖層。 按一下尺標或拖曳播放點以移動到時間點。

時間軸工具列包含&#x200B;**[!UICONTROL Duration]**&#x200B;欄位（0-60秒）、**[!UICONTROL Play]**/**[!UICONTROL Pause]**、目前時間/總持續時間顯示、回圈切換、**[!UICONTROL Timeline Scale]**&#x200B;縮放控制項、**[!UICONTROL Fit View]**&#x200B;按鈕以及摺疊/展開切換。

#### 影片廣告範本

時間軸會顯示範本中的所有視訊和音訊片段。 使用時間軸來檢視剪輯的及時排列方式，並透過拖曳剪輯的開始和結束操作框來裁剪剪剪輯。 您不能直接在時間軸上新增剪輯；請改為從左側面板或畫布新增剪輯，然後它就會在時間軸上顯示為剪輯。

### [!UICONTROL Layers]面板

畫布右側的[!UICONTROL Layers]面板會列出範本中的所有元素，並讓您管理其順序、可見度和屬性。 針對顯示範本，按一下畫布工具列中的&#x200B;**[!UICONTROL Open Layers]**&#x200B;以開啟它。 對於視訊範本，預設會開啟面板。

按一下任何圖層來選取畫布上的對應元素。

**標籤（僅限顯示廣告範本）**

顯示範本在[!UICONTROL Layers]面板頂端有兩個標籤：

* **[!UICONTROL Dynamic]** — 僅列出在廣告產生期間可以交換的圖層，例如AI代理程式可以取代的影像和文字。 這是產生廣告變異的預設檢視。
* **[!UICONTROL All]** — 顯示範本的完整圖層階層，包括結構容器。 使用此檢視來檢查或重新組織元素的巢狀方式。

視訊範本會在沒有標籤的單一清單中顯示所有圖層。

**每層動作**

將游標停留在圖層上可檢視下列動作：

| 動作 | 說明 |
| --- | --- |
| ![重新命名圖層](/help/creative/assets/edit.png) **[!UICONTROL Rename layer]** | 可讓您在面板中輸入新的圖層名稱。 |
| ![鎖定圖層](/help/creative/assets/cs-icon-lock.png) **[!UICONTROL Lock layer]** / ![解除鎖定圖層](/help/creative/assets/cs-icon-unlock.png) **[!UICONTROL Unlock layer]** | 防止或允許移動、編輯或重新排序圖層。 |
| ![隱藏圖層](/help/creative/assets/cs-icon-hidden.png) **[!UICONTROL Hide layer]** / ![顯示圖層](/help/creative/assets/cs-icon-visible.png) **[!UICONTROL Show layer]** | 隱藏或顯示畫布上的圖層。 隱藏的圖層會保留在範本中，但不會在範本彩現時顯示。 |
| ![拖曳以重新排序](/help/creative/assets/cs-icon-drag.png)拖曳以重新排序 | （僅限顯示廣告範本）拖曳重新排序圖示，以變更圖層在棧疊順序中的位置。 必須解除鎖定圖層才能重新排序。 |

**面板頁尾**

| 動作 | 說明 |
| --- | --- |
| ![複製選取的圖層](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate selected layer]** | 建立所選圖層的復本。 |
| ![刪除選取的圖層](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete selected layer]** | 刪除選取的圖層。 |
| **[!UICONTROL Group selected layers]** （僅限視訊範本） | 將兩個或多個選取的圖層群組為單一群組。 只有在選取兩個或多個圖層時才會出現。 您可以使用群組列上的控制項，取消群組群組圖層或從群組中移除個別圖層。 |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

## 從顯示廣告範本產生廣告變化 {#ad-variations-generate}

*僅顯示廣告範本。*

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**。

   [!UICONTROL Ad Variations Generator]會開啟，並預先載入範本。

1. 使用AI聊天介面來產生和調整廣告內容。 如需完整工作流程，請參閱「在Creative Studio中管理標準廣告](creative-studio-manage-standard-ads.md)」。[

## 新增或移除廣告範本的標籤 {#template-labels}

*僅顯示廣告範本。*

標籤可幫助您組織和篩選使用者範本。 您無法將標籤新增至系統範本。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**。

1. 在&#x200B;**[!UICONTROL Edit Labels]**&#x200B;對話方塊：

   * 若要新增標籤，請選取現有的標籤，或在輸入欄位中輸入名稱，然後按一下&#x200B;**[!UICONTROL Add Tag]**。

   * 若要移除標籤，請按一下標籤標籤標籤旁的&#x200B;**[!UICONTROL X]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 預覽廣告範本 {#template-preview}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片上。

1. 執行下列任一項作業：

   * （卡片檢視）按一下&#x200B;**[!UICONTROL Preview template]**&#x200B;圖示，或按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Preview]**。

   * （表格檢視）按一下「**[!UICONTROL ...]** > **[!UICONTROL Preview]**」。

1. 若是視訊範本，請按一下![播放](/help/creative/assets/play.png "播放")。

## 下載廣告範本 {#template-download}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   範本會根據瀏覽器的正常程式下載為ZIP檔案。

## 將廣告範本新增或移除為最愛 {#template-favorite}

*僅卡片檢視*

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片上。

1. 執行下列任一項作業：

   * 若要將範本新增為我的最愛，請按一下![我的最愛](/help/creative/assets/favorite-null.png)。

   * 若要移除範本作為我的最愛，請按一下[我的最愛]。![](/help/creative/assets/favorite.png)

## 刪除廣告範本 {#template-delete}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [關於Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理資產](creative-studio-manage-assets.md)
>* [在Creative Studio中管理標準廣告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理動態創意內容](creative-studio-manage-dynamic-ads.md)

