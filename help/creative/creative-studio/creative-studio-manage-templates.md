---
title: 在Creative Studio中管理廣告範本
description: 瞭解如何在Adobe Advertising Creative中建立、匯入、整理及管理廣告範本。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8fa8d6c66228d3a0af1de2514dd016d8f50262e8
workflow-type: tm+mt
source-wordcount: '3702'
ht-degree: 1%
---
# 在[!UICONTROL Creative Studio]中管理廣告範本

建立、匯入和管理顯示和視訊廣告範本，以用於廣告產生工作階段。

## [!UICONTROL Creative Studio] > [!UICONTROL Templates]檢視

**[!UICONTROL Templates]**&#x200B;索引標籤提供建立或匯入新廣告範本的快速動作。

[!UICONTROL Templates]索引標籤也會在頁面<!-- Only in the Templates tab -->底部將您現有的廣告範本列為[個別卡片（預設）或表格/清單](/help/creative/introduction/customize-data-views.md)。 廣告範本清單包含[!UICONTROL All]、[!UICONTROL System Templates] （您的Adobe帳戶團隊上傳至您的帳戶）和[!UICONTROL User Templates]的標籤。 依預設，會顯示所有廣告商的廣告範本。 若只要檢視特定廣告商的廣告範本，請從頁面頂端的廣告商清單中選取。

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### 可用動作

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

建立：

* [使用AI產生廣告範本](#template-generate)

* [手動建立廣告範本](#template-create)

* [匯入HTML5廣告範本](#templates-import)

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

## 使用AI產生廣告範本 {#template-generate}

*Beta功能*

在[!UICONTROL Creative Studio]中使用AI將現有的靜態顯示廣告影像轉換為可編輯的顯示廣告範本。 三步驟精靈可協助您產生及檢閱範本、使用自然語言請求變更，以及開啟範本編輯器以手動變更並儲存範本。

### 先決條件

您需要Creative資料庫中的靜態影像廣告。 此工作流程會從您的程式庫選取廣告；但不會直接在產生對話方塊中上傳新影像。

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### 步驟1：產生並檢閱範本

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. （可選）從頁面頂端的廣告商清單中選取一個廣告商，以檢視該廣告商的資料庫。

1. 在&#x200B;**[!UICONTROL Use AI to Generate a New Display Ad Template]**&#x200B;方塊中，按一下&#x200B;**[!UICONTROL Generate]**。

1. 在&#x200B;**[!UICONTROL Generate New Ad Template]**&#x200B;對話方塊中，選取&#x200B;**[!UICONTROL Generate from Existing Standard Ad Image]** （如果尚未選取）。

1. 從&#x200B;**[!UICONTROL Ad Library]**&#x200B;清單中選取包含影像廣告的資料庫。

1. 將游標停留在影像廣告卡上，然後按一下&#x200B;**[!UICONTROL Use this Standard Ad]**。

   使用選取的廣告寬度和高度，產生程式會自動開始。

<!--

Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [檢閱並調整產生的範本](#template-review)。

### 步驟2：檢閱並調整範本 {#template-review}

1. 等待產生完成，然後檢閱範本預覽和&#x200B;**[!UICONTROL Layers]**&#x200B;面板（如果可用）。

   在使用範本之前，請檢查文字、影像和版面配置。 這裡顯示的圖層可供檢閱；請在範本編輯器中手動變更。

1. （選用）要求變更產生的範本：

   1. 在&#x200B;**[!UICONTROL Ask the AI for any changes]**&#x200B;欄位中，說明您想要的變更。 例如，輸入`Change the headline to "Limited Time Offer" and the button text to "Shop Now"`。

   1. 按一下&#x200B;**[!UICONTROL Regenerate]**。

   1. 檢閱更新的預覽。 視需要重複。

1. 當您準備好要繼續時，請按一下&#x200B;**[!UICONTROL Use this Ad Template]**。

   產生的範本會在顯示範本編輯器中開啟。

### 步驟3：編輯並儲存範本 {#template-save}

>[!TIP]
>
> AI助理使用開放原始碼字型庫來尋找廣告中字型的相近相符專案。 若要使用您自己的字型，請將其上傳至[!UICONTROL Assets]標籤或從範本編輯器，然後在編輯器中取代產生的字型。
>
> 為達到最佳效果，請在範本編輯器中將AI產生的標誌取代為您原始的完美畫素標誌。

1. 在範本編輯器中，檢閱產生的元素，並使用[範本編輯器控制項](#template-controls)進行任何剩餘的變更。

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 在&#x200B;**[!UICONTROL Update Template]**&#x200B;對話方塊中，輸入或更新&#x200B;**[!UICONTROL Template name]**、選取&#x200B;**[!UICONTROL Advertiser]**，並選擇性地新增標籤。

1. 按一下&#x200B;**[!UICONTROL Update]**&#x200B;儲存範本並返回&#x200B;**[!UICONTROL Templates]**&#x200B;檢視。

   若要儲存個別復本，請按一下&#x200B;**[!UICONTROL Save As New]**。

然後您可以使用範本來[產生廣告變化](#ad-variations-generate)。

### 如果您無法產生範本 {#troubleshooting}

| 問題 | 該做什麼 |
| --- | --- |
| 從影像產生時，不會列出任何程式庫或影像廣告 | 檢查選取的廣告商和&#x200B;**[!UICONTROL Ad Library]**。 如果媒體櫃沒有標準廣告影像，請選取包含現有靜態影像廣告的其他媒體櫃。 |
| 以影像為基礎的產生失敗，或無法轉換影像 | 檢閱顯示的訊息，按一下&#x200B;**[!UICONTROL Back to library]**，然後選取影像廣告再試一次。 |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

## 手動建立廣告範本 {#template-create}

使用範本編輯器建立空白顯示區或視訊範本。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 在&#x200B;**[!UICONTROL Create New Ad Template]**&#x200B;方塊中，按一下&#x200B;**[!UICONTROL Create]**，然後選取&#x200B;**[!UICONTROL Display Ad Template]**&#x200B;或&#x200B;**[!UICONTROL Video Ad Template]**。

1. （顯示廣告）選取廣告範本大小，然後按一下&#x200B;**[!UICONTROL Continue]**。

1. 使用範本編輯器[&#128279;](#template-controls)中的控制項來設定範本設定。

1. （選擇性）若要下載已定義的範本復本，請按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   檔案會依照瀏覽器的正常程式下載。

1. 儲存範本：

   1. 執行下列任一項作業：

      * 按一下&#x200B;**[!UICONTROL Save]**。

      * 若要將範本儲存為草稿，請按一下「**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**」。

   1. 輸入&#x200B;**[!UICONTROL Template name]**、選取&#x200B;**[!UICONTROL Advertiser]**、選擇性地選取現有標籤或新增標籤至範本，然後按一下&#x200B;**[!UICONTROL Save]**。

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

## 編輯廣告範本 {#template-edit}

*僅顯示廣告範本。*

>[!IMPORTANT]
>
>AI代理程式無法變更範本版面、元素位置、間距或印刷樣式。 在產生內容之前，在範本編輯器中進行任何結構性變更。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Template]**。

1. 在範本編輯器[&#128279;](#template-controls)中使用控制項來編輯範本配置或元素。

1. （選擇性）若要下載已定義的範本復本，請按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   檔案會依照瀏覽器的正常程式下載。

1. 儲存範本：

   * 按一下&#x200B;**[!UICONTROL Save]**。

   * 若要將範本儲存為草稿，請按一下「**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**」。 輸入&#x200B;**[!UICONTROL Template name]**、選取&#x200B;**[!UICONTROL Advertiser]**、選擇性地選取現有標籤或新增標籤至範本，然後按一下&#x200B;**[!UICONTROL Save]**。

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## 從顯示廣告範本產生廣告變化 {#ad-variations-generate}

*僅顯示廣告範本。*

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**。

   [!UICONTROL Ad Variations Generator]會開啟，並預先載入範本。

1. 使用AI聊天介面來產生和調整廣告內容。 如需完整工作流程，請參閱「在Creative Studio中管理標準廣告[&#128279;](creative-studio-manage-standard-ads.md)」。

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

   * 若要將範本新增為我的最愛，請按一下[我的最愛] ![&#128279;](/help/creative/assets/favorite-null.png " [我的最愛] ")。

   * 若要移除範本作為我的最愛，請按一下[我的最愛] ![](/help/creative/assets/favorite.png "[我的最愛] ")。

## 刪除廣告範本 {#template-delete}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio].**

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本卡片或表格列上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

## 範本編輯器控制項 {#template-controls}

顯示和視訊範本編輯器都會在畫布上方提供一個工具列，用來復原變更和調整檢視、在左側提供面板來新增資產和元素，在右側提供[!UICONTROL Layers]面板來管理圖層。 用於編輯所選元素以及控制時間與播放的工具，在顯示範本與視訊範本之間有所不同。

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

### 復原變更並調整畫布檢視

一般動作工具列位於廣告範本編輯器的編輯畫布上方，並分成兩部分（左和右）。

#### 顯示廣告範本

| 控制 | 說明 |
| --- | --- |
| **[!UICONTROL Undo]** | 復原上一個動作。 |
| ![取消復原](/help/creative/assets/cs-icon-redo.png "取消復原") **[!UICONTROL Redo]** | 重新執行上一個復原的動作。 |
| **[!UICONTROL Links]** | 開啟面板以管理附加至範本中元素的點進URL。 |
| 縮放控制項 | 按一下&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;以調整畫布放大率（10%-150%，以10%為增量）。 按一下縮放等級標籤（當畫布自動符合時顯示&#x200B;**[!UICONTROL Auto]**，或手動設定時顯示百分比）以開啟具有下列選項的功能表： **[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**。 |
| 廣告大小 | 顯示目前的廣告維度（例如300 × 250）。 按一下以開啟大小選擇器，選擇器提供六種常用的IAB標準大小作為卡片，以及包含所有19個標準IAB顯示廣告大小的下拉式清單。 新範本的預設大小為300 × 250 （Medium矩形）。 |
| ![開啟圖層面板](/help/creative/assets/layers-panel-open.png "開啟圖層面板") | 開啟[!UICONTROL Layers]面板。 僅在[!UICONTROL Layers]面板關閉時顯示。 |

#### 影片廣告範本

| 控制 | 說明 |
| --- | --- |
| **[!UICONTROL Undo]** / ![取消復原](/help/creative/assets/cs-icon-redo.png "取消復原") **[!UICONTROL Redo]** | 復原或重新復原上一個動作。 |
| 縮放控制項 | 按一下&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;以調整畫布放大比例。 按一下縮放等級以開啟包含下列選項的功能表： **[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**。 |
| ![開啟圖層面板](/help/creative/assets/layers-panel-open.png "開啟圖層面板") | 開啟[!UICONTROL Layers]面板。 僅在[!UICONTROL Layers]面板關閉時顯示。 |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### 新增資產和元素

左側面板可讓您將廣告資產和元素新增到範本。 按一下圖示以開啟其內容面板；再按一下相同圖示以將其關閉。

#### 顯示廣告範本

| 圖示 | 說明 |
| --- | --- |
| **[!UICONTROL Search]** | 在您的資料庫中搜尋所有資產型別。 |
| **[!UICONTROL Upload]** | 將影像或字型檔案上傳到編輯器以用於目前的範本。 您一次最多可上傳20個檔案。 |
| **[!UICONTROL Templates]** | 從您的Creative Studio資料庫瀏覽廣告範本，以用作基礎圖層或參考元素。 |
| **[!UICONTROL My Assets]** | 瀏覽您在Creative Studio [!UICONTROL Assets]索引標籤中上傳的所有資產。 |
| **[!UICONTROL Images]** | 僅瀏覽您已在Creative Studio [!UICONTROL Assets]索引標籤中上傳的影像資產。 |
| **[!UICONTROL Text]** | 將文字元素新增至畫布，包括您已上傳的任何自訂字型。 |
| **[!UICONTROL Elements]** | 新增形狀和版面配置元素，例如按鈕和矩形。 |

您可以從任何面板將專案直接拖曳到畫布上，或按一下專案以將其置於預設位置。

#### 影片廣告範本

| 圖示 | 說明 |
| --- | --- |
| **[!UICONTROL Search]** | 在您的資料庫中搜尋所有資產型別。 |
| **[!UICONTROL Upload]** | 將影像、視訊、音訊或字型檔案(TTF、OTF、WOFF、WOFF2)上傳到編輯器，以便在目前的範本中使用。 您一次最多可上傳20個檔案。 |
| **[!UICONTROL Templates]** | 從您的Creative Studio資料庫瀏覽廣告範本。 |
| **[!UICONTROL My Assets]** | 瀏覽您在Creative Studio [!UICONTROL Assets]索引標籤中上傳的所有資產。 |
| **[!UICONTROL Images]** | 僅瀏覽您已在Creative Studio [!UICONTROL Assets]索引標籤中上傳的影像資產。 |
| **[!UICONTROL Video]** | 僅瀏覽您在Creative Studio [!UICONTROL Assets]索引標籤中上傳的視訊資產。 |
| **[!UICONTROL Audio]** | 僅瀏覽您已在Creative Studio [!UICONTROL Assets]索引標籤中上傳的音訊資產。 |
| **[!UICONTROL Text]** | 將文字元素新增至畫布，包括您已上傳的任何自訂字型。 |
| **[!UICONTROL Elements]** | 新增形狀與向量元素。 |

您可以從任何面板將專案直接拖曳到畫布上，或按一下專案以將其置於預設位置。

### 編輯選取的元素

按一下編輯畫布上的元素以選取它。 視範本型別而定，會顯示一或多個包含該元素控制項的工具列。

控制項會因元素型別而異。

<!-- From inspectorbar.ts -->

#### 顯示範本編輯工具列

| 控制 | 元素型別 | 說明 |
| --- | --- | --- |
| **[!UICONTROL Properties]** | 全部 | 開啟面板以編輯圖層名稱；將圖層標示為動態（在廣告產生期間可交換）；並設定點進URL （僅限連結）。 在它下方，選擇&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;狀態以設定該互動狀態的元素樣式，然後根據元素型別調整樣式 — 印刷樣式（僅限文字和連結）、裝飾（填色、邊框、圓角半徑）、維度、位置。 |
| **[!UICONTROL Effects]** | 全部 | 開啟一個面板，您可在其中選擇要針對該互動狀態套用效果的&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;狀態，然後調整&#x200B;**[!UICONTROL Transform]**、**[!UICONTROL Transition]**、**[!UICONTROL Box Shadow]**、**[!UICONTROL Filter]**、**[!UICONTROL Blend Mode]**&#x200B;和&#x200B;**[!UICONTROL Cursor]**&#x200B;區段。 文字元素也包含&#x200B;**[!UICONTROL Text Shadow]**&#x200B;區段。 |
| **[!UICONTROL Animations]** | 全部 | 開啟面板以設定圖層在時間軸上的進入和退出時間，並設定&#x200B;**[!UICONTROL Entrance Animation]**、**[!UICONTROL Loop Animation]**&#x200B;和&#x200B;**[!UICONTROL Exit Animation]**&#x200B;預設集具有持續期間和緩動。 包含&#x200B;**[!UICONTROL Copy]**、**[!UICONTROL Paste]**&#x200B;和&#x200B;**[!UICONTROL Reset]**&#x200B;動作。 |
| **[!UICONTROL Crop]** | 影像 | 開啟工具列以裁切影像。 選取&#x200B;**[!UICONTROL Aspect Ratio]**&#x200B;預設集（或&#x200B;**[!UICONTROL Free]**），然後按一下&#x200B;**[!UICONTROL Apply]**&#x200B;或&#x200B;**[!UICONTROL Cancel]**。 |
| **[!UICONTROL Position]** | 全部 | 開啟包含&#x200B;**[!UICONTROL Move]**&#x200B;選項(**[!UICONTROL Forward]**、**[!UICONTROL Backward]**、**[!UICONTROL To front]**、**[!UICONTROL To back]**)、**[!UICONTROL Align to Page]**&#x200B;選項(**[!UICONTROL Top]**、**[!UICONTROL Left]**、**[!UICONTROL Middle]**、**[!UICONTROL Center]**、**[!UICONTROL Bottom]**、**[!UICONTROL Right]**、**[!UICONTROL Fit Vertically]**、**[!UICONTROL Fit Horizontally]**、**[!UICONTROL Fit to Page]**)的功能表，非影像元素則開啟&#x200B;**[!UICONTROL Layer Level Alignment]**&#x200B;選項（相同的六個對齊選項，加上&#x200B;**[!UICONTROL Fit to Content]**）。 |

#### 視訊範本編輯工具列

| 控制 | 元素型別 | 說明 |
| --- | --- | --- |
| **[!UICONTROL Shape]** | 形狀 | 設定形狀特定的選項。 |
| 挖剪控制項 | 影像 | 調整切除型別、位移和平滑。 |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | 多個選取的元素或群組 | 將選取的元素群組在一起，或取消選取群組的群組。 |
| **[!UICONTROL Combine]** | 相容的形狀 | 將選取的形狀組合成單一形狀。 |
| **[!UICONTROL Audio replace]** | 音訊和視訊 | 以資產庫中的檔案取代音訊。 |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | 文字 | 調整字型系列、粗細、大小、水準對齊方式及其他進階印刷樣式設定。 |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | 影像和視訊 | 設定元素的填色影像或視訊來源。 |
| **[!UICONTROL Trim]** | 視訊與音訊 | 開啟裁剪模式以設定剪輯的起點和終點。 |
| ![磁碟區](/help/creative/assets/volume.png "磁碟區") ([!UICONTROL Volume]) | 視訊與音訊 | 調整音訊等級。 |
| ![播放速度](/help/creative/assets/speed.png "播放速度") ([!UICONTROL Playback speed]) | 視訊與音訊 | 調整播放速率。 |
| ![裁切](/help/creative/assets/crop.png "裁切") ([!UICONTROL Crop]) | 全部 | 裁切元素至自訂區域。 |
| 旋轉與翻轉控制項 | 全部 | 旋轉或翻轉所選元素。 |
| ![筆畫](/help/creative/assets/stroke.png "筆畫") ([!UICONTROL Stroke]) | 全部 | 設定框線顏色和寬度。 |
| **[!UICONTROL Text Background]** | 文字 | 在文字後面新增背景顏色。 |
| **[!UICONTROL Animations]** | 全部 | 新增或編輯輸入、結束或回圈動畫。 |
| **[!UICONTROL Style]** | 全部 | 開啟包含&#x200B;**[!UICONTROL Adjustments]**、**[!UICONTROL Filter]**、**[!UICONTROL Effect]**&#x200B;和&#x200B;**[!UICONTROL Blur]**&#x200B;選項的功能表。 |
| **[!UICONTROL Shadow]** | 全部 | 新增或編輯陰影。 |
| **[!UICONTROL Opacity]** | 全部 | 設定元素的透明度等級。 |
| **[!UICONTROL Position]** | 全部 | 以數值方式調整元素的大小、位置和旋轉。 |
| ![正在編輯面板](/help/creative/assets/cs-template-video-editing-panel.png "正在編輯面板") | 全部 | 開啟或關閉具有更多編輯功能的所選元素的[編輯面板](#detailed-element-properties-for-video-templates)。 |

#### 視訊範本的詳細元素屬性

在視訊範本編輯器中，按一下工具列中的「編輯面板」![](/help/creative/assets/cs-template-video-editing-panel.png "「編輯面板」")，以開啟所選元素的編輯面板，該面板具有更多編輯功能。 編輯面板會顯示在畫布的左側，與列出範本中圖層的[!UICONTROL Layers]面板不同。

##### 個別元素

當您選取單一影像、視訊、形狀或文字元素時，編輯面板會在下方顯示適用的區段。

| 面板區段 | 工具 | 控制項 |
| --- | --- | --- |
| [!UICONTROL Layer] | 對齊與圖層定位 | 將選取的圖層對齊左側、水準中心、右側、頂端、垂直中心或底部。 排列功能表會變更其前後棧疊順序。 這些控制項會定點陣圖層本身；它們不會對齊圖層內的文字。 |
| | [!UICONTROL Rotate & Flip] | 輸入旋轉角度（以度為單位）。 使用![水準翻轉](/help/creative/assets/cs-template-video-flip.png "水準翻轉")可水準映象圖層，或使用![垂直翻轉](/help/creative/assets/cs-template-video-flip-vertical.png "垂直翻轉")可垂直映象圖層。 |
| | ![不透明度](/help/creative/assets/cs-template-video-opacity.png "不透明度") [!UICONTROL Opacity] | 讓選取的圖層或多或少透明。 |
| | ![混合模式](/help/creative/assets/cs-template-video-blend-mode.png "混合模式") [!UICONTROL Blend Mode] | 變更選取圖層的顏色與其背後的圖層結合的方式。 |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | 開啟圖層位置和尺寸的其他控制項。 可用性取決於所選圖層的轉換許可權。 |
| [!UICONTROL Shape] | ![形狀選項](/help/creative/assets/cs-template-video-shape-options.png "形狀選項") [!UICONTROL Shape]和形狀特定屬性 | 變更形狀及其可用屬性，例如點、側、內徑、線寬或圓角半徑。 控制項取決於選取的形狀。 |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | 進入向量編輯模式以編輯形狀的路徑（如果可用）。 |
| [!UICONTROL Character] | ![字型](/help/creative/assets/cs-template-video-typeface.png "字型")字型，![文字樣式](/help/creative/assets/cs-template-video-text-style.png "文字樣式")文字樣式，![粗體](/help/creative/assets/cs-template-video-text-bold.png "粗體")粗體，![斜體](/help/creative/assets/cs-template-video-text-italic.png "斜體")斜體，以及![字型大小](/help/creative/assets/cs-template-video-font-size.png "字型大小")字型大小 | （文字圖層）變更所選文字的字型系列、字型樣式和大小。 |
| | ![靠左對齊](/help/creative/assets/cs-template-video-text-align-l.png "靠左對齊") / ![置中對齊](/help/creative/assets/cs-template-video-text-align-c.png "置中對齊") / ![靠右對齊](/help/creative/assets/cs-template-video-text-align-r.png "靠右對齊")文字對齊 | （文字圖層）將框架中的文字對齊左側、中央或右側，或自動偵測對齊方式。 |
| | ![進階文字設定](/help/creative/assets/cs-template-video-advanced-text.png "進階文字設定")進階文字設定 | （文字圖層）開啟其他印刷樣式設定。 |
| [!UICONTROL Fill] | ![填](/help/creative/assets/cs-template-video-fill.png "填")填色控制項 | 變更所選圖層的色彩、影像或視訊填色。 控制項會反映目前的填色型別，並開啟其設定。 針對文字，變更文字顏色。 |
| [!UICONTROL Stroke] | ![筆畫](/help/creative/assets/cs-template-video-stroke.png "筆畫")筆畫控制項 | 啟用或停用外框，並變更其顏色、寬度、樣式和位置。 啟用筆畫時，會出現其他控制項。 |
| [!UICONTROL Text Background] | ![文字背景](/help/creative/assets/cs-template-video-text-bg.png "文字背景")背景控制項 | （文字圖層）新增或變更文字後的背景。 |
| [!UICONTROL Animations] | ![動畫](/help/creative/assets/cs-template-video-animation.png "動畫") [!UICONTROL Presets] | 開啟所選圖層的動畫預設集，包括入口、出口和回圈動畫。 |
| [!UICONTROL Appearance] | ![調整](/help/creative/assets/cs-template-video-adjustments.png "調整") [!UICONTROL Adjustments] | 變更所選圖層的視覺屬性。 |
| | ![篩選器](/help/creative/assets/cs-template-video-filter.png "篩選器") [!UICONTROL Filter] | 將視覺化濾鏡套用至選取的圖層。 |
| | ![效果](/help/creative/assets/cs-template-video-effects.png "效果") [!UICONTROL Effect] | 將效果套用至選取的圖層。 |
| | ![模糊](/help/creative/assets/cs-template-video-blur.png "模糊") [!UICONTROL Blur] | 將模糊套用到選取的圖層。 |
| | ![陰影](/help/creative/assets/cs-template-video-shadow.png "陰影") [!UICONTROL Shadow] | 增加或變更所選圖層的陰影。 |

##### 多個選取範圍和專用元素

當您選取多個元素、群組、剪下元素或音訊片段時，編輯面板會在下方顯示選取範圍特定的區段。 多個元素、群組和切除也會保留[!UICONTROL Layer]區段。

| 面板區段 | 工具 | 控制項 |
| --- | --- | --- |
| [!UICONTROL Layer] | 對齊與圖層定位 | 對齊多個選取的元素或群組。 排列功能表會變更其前後棧疊順序。 |
| | [!UICONTROL Rotate & Flip] | 旋轉或翻轉所選元素或群組。 |
| | ![不透明度](/help/creative/assets/cs-template-video-opacity.png "不透明度") [!UICONTROL Opacity] | 使選取的元素或群組或多或少透明。 |
| | ![混合模式](/help/creative/assets/cs-template-video-blend-mode.png "混合模式") [!UICONTROL Blend Mode] | 變更所選元素或群組的顏色與其背後的圖層結合的方式。 |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | 開啟所選元素或群組位置與尺寸的控制項。 可用的控制項取決於選取的元素。 |
| [!UICONTROL Selection] | ![群組](/help/creative/assets/cs-template-video-group.png "群組")群組/ ![取消群組](/help/creative/assets/cs-template-video-ungroup.png "取消群組")取消群組 | 針對多個選取的圖層或選取的群組，顯示在[!UICONTROL Layer]下方。 將選取的圖層分組，以便一起管理，或將群組分割為個別圖層。 |
| [!UICONTROL Settings] | ![剪裁剪輯](/help/creative/assets/cs-template-video-cutout-clip.png "剪裁剪輯") / ![剪裁覆蓋圖](/help/creative/assets/cs-template-video-cutout-overlay.png "剪裁覆蓋圖")剪裁控制項 | （挖剪圖層）顯示在[!UICONTROL Layer]下方。 選取切除型別並調整其位移和邊平滑化。 |
| [!UICONTROL Audio Properties] | ![Trim](/help/creative/assets/cs-template-video-trim.png "Trim")Trim，![磁碟區](/help/creative/assets/cs-template-video-volume.png "磁碟區")磁碟區，以及![播放速度](/help/creative/assets/cs-template-video-playback-speed.png "播放速度")播放速度 | （音訊圖層）設定剪輯的起點和終點、音訊等級以及播放速度。 |

#### 直接在畫布上編輯元素

##### 顯示廣告範本

| 動作 | 說明 |
| --- | --- |
| **[!UICONTROL Replace]** | （僅限影像元素）開啟「影像」面板，讓您可以使用資產庫中的影像來取代影像。 |
| ![前進](/help/creative/assets/cs-icon-move-forward.png "前進") **[!UICONTROL Move forward]** | 以棧疊順序將元素向前移動一步（向前）。 |
| ![向後移動](/help/creative/assets/cs-icon-move-backward.png "向後移動") **[!UICONTROL Move backward]** | 以棧疊順序向後移動元素一步（向後）。 |
| ![重複](/help/creative/assets/cs-icon-duplicate.png "重複") **[!UICONTROL Duplicate]** | 建立元素的復本。 |
| ![刪除](/help/creative/assets/cs-icon-delete.png "刪除") **[!UICONTROL Delete]** | 從畫布移除元素。 |
| 旋轉控點 | 按一下並拖曳所選元素上方的操作框以旋轉它。 在拖曳時按住&#x200B;**[!UICONTROL Shift]**，將旋轉跳接至15度增量。 |

您也可以按一下並拖曳選取的元素來重新定位它，然後按一下並拖曳其周圍的控點來調整其大小。

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

您也可以按一下並拖曳選取的元素來重新定位它，然後按一下並拖曳其周圍的控點來調整其大小。

### 控制時間與播放

顯示和視訊編輯器都會在畫布底部顯示時間軸面板。

#### 顯示廣告範本

時間軸會顯示畫布上每個圖層的軌跡，根據圖層進入和結束的動畫時間，跨越圖層可見的時間範圍。 拖曳軌跡的開始或結束操作框以調整其進入或結束時間，或拖曳軌跡以重新排序圖層。 按一下尺標或拖曳播放點以移動到時間點。

時間軸工具列包含&#x200B;**[!UICONTROL Duration]**&#x200B;欄位（0-60秒）、**[!UICONTROL Play]**/**[!UICONTROL Pause]**、目前時間/總持續時間顯示、回圈切換、**[!UICONTROL Timeline Scale]**&#x200B;縮放控制項、**[!UICONTROL Fit View]**&#x200B;按鈕以及摺疊/展開切換。

#### 影片廣告範本

時間軸會顯示範本中的所有視訊和音訊片段。 使用時間軸來檢視剪輯的及時排列方式，並透過拖曳剪輯的開始和結束操作框來裁剪剪剪輯。 您不能直接在時間軸上新增剪輯；請改為從左側面板或畫布新增剪輯，然後它就會在時間軸上顯示為剪輯。

### 管理圖層

畫布右側的[!UICONTROL Layers]面板會列出範本中的所有元素，並讓您管理其順序、可見度和屬性。 針對顯示範本，按一下畫布工具列中的&#x200B;**[!UICONTROL Open Layers]**&#x200B;以開啟它。 對於視訊範本，預設會開啟面板。

按一下任何圖層來選取畫布上的對應元素。

**標籤（僅限顯示廣告範本）**

顯示範本在[!UICONTROL Layers]面板頂端有兩個標籤：

* **[!UICONTROL Dynamic]** — 僅列出在廣告產生期間可以交換的圖層，例如AI代理程式可以取代的影像和文字。 這是產生廣告變異的預設檢視。
* **[!UICONTROL All]** — 顯示範本的完整圖層階層，包括結構容器。 使用此檢視來檢查或重新組織元素的巢狀方式。

視訊範本會在沒有標籤的單一清單中顯示所有圖層。

**每層動作**

將游標停留在圖層上可檢視下列動作。

| 動作 | 說明 |
| --- | --- |
| ![重新命名圖層](/help/creative/assets/edit.png "重新命名圖層") **[!UICONTROL Rename layer]** | 可讓您在面板中輸入新的圖層名稱。 |
| ![鎖定圖層](/help/creative/assets/cs-icon-lock.png "鎖定圖層") **[!UICONTROL Lock layer]** / ![解鎖圖層](/help/creative/assets/cs-icon-unlock.png "解鎖圖層") **[!UICONTROL Unlock layer]** | 防止或允許移動、編輯或重新排序圖層。 |
| ![隱藏圖層](/help/creative/assets/cs-icon-hidden.png "隱藏圖層") **[!UICONTROL Hide layer]** / ![顯示圖層](/help/creative/assets/cs-icon-visible.png "顯示圖層") **[!UICONTROL Show layer]** | 隱藏或顯示畫布上的圖層。 隱藏的圖層會保留在範本中，但不會在範本彩現時顯示。 |
| ![拖曳以重新排序](/help/creative/assets/cs-icon-drag.png "拖曳以重新排序")拖曳以重新排序 | （僅限顯示廣告範本）拖曳重新排序圖示，以變更圖層在棧疊順序中的位置。 必須解除鎖定圖層才能重新排序。 |

**面板頁尾**

| 動作 | 說明 |
| --- | --- |
| ![複製選取的圖層](/help/creative/assets/cs-icon-duplicate.png "複製選取的圖層") **[!UICONTROL Duplicate selected layer]** | 建立所選圖層的復本。 |
| ![刪除選取的圖層](/help/creative/assets/cs-icon-delete.png "刪除選取的圖層") **[!UICONTROL Delete selected layer]** | 刪除選取的圖層。 |
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

>[!MORELIKETHIS]
>
>* [關於Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理資產](creative-studio-manage-assets.md)
>* [在Creative Studio中管理標準廣告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理動態創意內容](creative-studio-manage-dynamic-ads.md)
