---
title: 關於您的創意程式庫
description: 瞭解如何管理廣告體驗的創意內容。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 8d549853be10ebfbb71b14e013b04178466e87fe
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# 關於你的創意圖書館

您的創意程式庫可讓您管理將在廣告體驗中使用的創意內容。 您可以建立多個程式庫，每個程式庫都包含一組創意和&#x200B;*創意組合*，這些創意組合是您可以以單一單位新增到體驗中的創意群組。

您的程式庫可以包括：

* **個別創意：**&#x200B;您可以直接在廣告體驗中包含沒有定義使用者目標的個別創意。 您也可以使用您的創意內容來建立組合，這些組合可包含在鎖定的[廣告體驗](/help/creative/experiences/experience-about.md)中。

   * **標準創意：** 你可以上傳和管理各種 [格式](#creative-creative-formats)的創意。 針對每個創意，指定你關聯該創意的廣告預設語言，以及使用者點擊包含該創意的廣告時會開啟的預設登陸頁。 你可以選擇性地指定標籤，作為各種檢視中的[!DNL Creative]篩選條件，以及在使用該[!UICONTROL Custom Creative Report]維度時作為欄位值[!UICONTROL Creative Label]。

   * **動態創意：** 你可以透過將廣告範本中的動態變數映射到動態檔案中的數值來建立動態生成的創意。 所有使用者都可以預覽、複製並刪除現有的動態廣告。

* **創意套裝** ：將創意內容分組，用於多個體驗並設定明確的用戶目標。 您可以建立包含標準顯示廣告的&#x200B;*標準顯示組合*、包含標準視訊廣告的&#x200B;*標準視訊組合*，以及包含動態產生之顯示廣告的&#x200B;*動態顯示組合*。

## 支援的Creative格式 {#creative-creative-formats}

### 標準創意格式

你可以新增並管理以下符合 [支援創意大小](creative-sizes.md)的創意類型。

>[!IMPORTANT]
>
>* 即使你打算使用 HTML5、彈性 HTML5 或第三方創意來製作標準的展示廣告體驗，你也必須為每個創意尺寸加入圖片創意。
>* 每個標準展示體驗都需要為該體驗分配的每個創意尺寸預設一個圖片創意。 預設圖片創意用於瀏覽器未啟用 JavaScript，或廣告伺服器因延遲無法個人化廣告時。
>* 每個標準影片體驗都需要為該體驗指定的創意時長預設一個影片創意。<!-- when is it used? -->

#### 彈性 HTML5

彈性 HTML5 創意是 HTML5 創意，所有圖片和其他屬性都以標準 HTML 標籤形式呈現，你可以直接 [!DNL Creative]在其中編輯，無論是在創意庫內，還是在個人體驗中（創造原始創意的變體）。 在數位訊號處理（DSP）中，彈性的 HTML5 創意是針對單一特定廣告尺寸（以像素為單位）使用。 你可以選擇性地更改彈性 HTML5 創意中屬性的預設值。 之後，你可以在特定體驗中為屬性指定自訂值，這會產生一種與父創意不同的變化。

你可以選擇上傳彈性的 HTML5 創意檔案為 ZIP 檔，或是使用你帳號上可用的範本作為起點。 請參閱 [彈性 HTML5 創意](html5-creative-specification.md)的規格。

#### 標準展示創意

標準展示廣告包括：

* HTML5 創意素材可本地上傳或從 Adobe GenStudio 上傳，用於績效行銷。
* 圖片檔可上傳本地或 Adobe Experience Manager 上傳。

##### HTML5 創意

* **GenStudio 體驗：**&#x200B;你可以將 GenStudio 用於績效行銷[的展示廣告體驗](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/display-ad-experiences)[中，匯入所有廣告變體](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home)，作為 HTML5 創意。外部連結已轉換為當地參考資料。 HTML 內容可達 20 MB，單張圖片可達 50 MB。

  一旦你匯入了 GenStudio 體驗，你可以編輯匯入的創意內容的元資料（名稱、語言、標籤），但無法編輯創意內容。 如果你在 GenStudio 裡編輯 GenStudio 體驗，然後重新匯入 [!DNL Creative] 體驗以使用最新版本。

  >[!NOTE]
  >
  >要使用此功能，GenStudio 帳號與 Advertising Creative 帳號必須共用相同的組織 ID，且使用者必須擁有存取 GenStudio 的權限。

* **上傳檔案：** 您也可以上傳簡單或靜態的 HTML5 創意，並標明所有屬性與圖片，格式為 ZIP 檔案。 你無法編輯任何屬性或新增圖片;相反地，上傳一個新的 ZIP 檔來新增創意。 請參閱 [簡單與靜態HTML5創意](html5-creative-specification.md)的規範。

##### 形象創意團隊

你可以以 GIF、JPEG、JPG 或 PNG 格式加入圖片創意。 你可以從 Adobe Experience Manager 帳號上傳核准的圖片，或是從你的裝置或網路上傳圖片。

每個標準展示廣告體驗都需要為每個設定的創意大小預設一個圖片創意。

#### 第三方創意

輸入 JavaScript 追蹤標籤，適用於第三方廣告伺服器上的創意。 指令碼會依廣告伺服器而有所不同；範例如下：

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### 視訊創意 {#creative-video-specs}

您可以從您的裝置或網路上傳適用於Web、行動或連線電視的第一方視訊創意。 每個標準視訊廣告體驗都需要為指派給體驗的每個創意期間提供預設的視訊創意。 DSP會自動將所有視訊創意轉碼為VAST 2.0標籤，以便您預覽。 在[!UICONTROL Tag Manager]中，您可以選擇將DSP專屬的轉碼[套用至任何視訊廣告體驗標籤。](/help/creative/experiences/experience-tag-video-transcoding.md)

請參考以下影片創意要求。 **注意：**&#x200B;如果您要將視訊體驗上傳至Advertising DSP，請同時參閱DSP對高畫質視訊Assets的[需求](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets)，此需求可能會比較受限。

**檔案類型：** .mov、.mp4、.webm

**檔案大小：** 最大 512 MB

**影片畫面比例：** 16,4:9:3

**影片解析度：** 360p 為 640x360,720p 為 1280x720,1080p 為 1920x1080

**影片長度：** 最多90秒

**位元率：** 360p 為 600-1200 kbps，720p 為 1500-2500 kbps，1080p 為 3000-5000+ kbps

**影片幀率：** 23.98 FPS。 根據地區或發行商的要求，可能會接受額外的幀率

**視訊編碼：** H.264（產業標準）、AV1、H.265

**音訊格式：** ACC（產業標準/MP4）、Opus（WebM/AV1）

**音訊位元率：** 16-512 kbps

**音訊取樣速率：** 44100-48000 Hz

**音訊速率：** 44.1kHz或48 kHz

**其他音訊：**&#x200B;上傳的檔案必須為非交錯式、混合式且包含音軌。 可能沒有音效，但視訊檔案中必須包含音軌。

### 動態廣告的格式

你可以透過將廣告範本中的動態變數映射到動態檔案中的數值，動態產生靜態 HTML5 和動態 HTML5 格式的創意。 動態創意可能包括從您舊有的 Adobe 廣告動態創意優化（DCO）經驗遷移過來的創意。

## [!UICONTROL Creative Libraries]檢視

如需自訂每個檢視的詳細資訊，請參閱[自訂您的資料檢視](/help/creative/introduction/customize-data-views.md)。

### [!UICONTROL Creative Libraries]主要檢視

[!UICONTROL Creative Libraries]主要檢視會顯示您的所有創意程式庫。 每個資料庫的資料包含指派給資料庫套裝的體驗數量、套裝數量、創意內容數量、創意大小數量、預設語言目標數量、建立日期，以及資料庫任何元素的最後修改日期。 表格模式也包含廣告商欄。

當你進入卡片模式時，可以用按鈕在多個創意 &lt; and > 庫中瀏覽圖片。

#### 可用行動

* [建立一個新的函式庫](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* 每個創意圖書館：

   * [編輯程式庫名稱](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [開啟程式庫以檢視指派給程式庫的創意和組合](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [刪除函式庫](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### [!UICONTROL Creative Libraries] >[!UICONTROL Creatives]觀點

#### [!UICONTROL Standard Ads]

分頁會 [!UICONTROL Standard Ads] 顯示你所創建的所有標準創意。 每個創意的資料包括創意大小、創意類型及創作日期。 表格模式也包含預設語言欄位及預設登陸頁面。

##### 可用行動

* [將標準創意加入函式庫](creative-add-standard.md)

* [編輯標準創意](creative-edit-standard.md)

* [預覽標準創意](creative-preview.md)

* [將標準創意加入標準展示組合包，並將標準創意從標準展示組合中移除](creative-attach-detach-bundles.md)

* [將影片創意加入標準影片組合包，並將影片創意從標準影片組合中移除](creative-attach-detach-bundles.md)

* [重複標準創意](creative-duplicate.md)

* [下載標準創意](creative-download.md)

* [刪除標準創意](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

這個 [!UICONTROL Dynamic Ads] 分頁會顯示所有動態創作，這些都是你創意目錄中動態建立的，除了你 [手動刪除](creative-delete.md) 的 [!UICONTROL Dynamic Ads] 動態創意。 如果你 [手動複製](creative-duplicate.md) 了任何動態創意<!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed -->，那麼該目錄的創意清單也會包含重複的創意。

每個創意的資料包括創意類型、創意大小、該創意所屬的目錄數量，以及創作日期。 表格模式還包含產生創意的廣告範本欄位及優惠數量。

>[!NOTE]
>
>每次目錄被處理時，該目錄中現有動態創意的資料都會被刷新。<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### 可用行動

* [將動態創意加入函式庫](creative-add-dynamic.md)

* [編輯動態創意](creative-edit-dynamic.md)

* [預覽動態創意](creative-preview.md)

* [將動態創意加入動態展示套件，並將動態創意從動態展示套件中移除](creative-attach-detach-bundles.md)

* [重複動態創意](creative-duplicate.md)

* [刪除動態創意](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries] >[!UICONTROL Bundles]觀點

這個檢視會 [!UICONTROL Bundles] 顯示你所有的標準和動態組合容器。 你可以看到每個組合包中創意的名稱、創意尺寸和語言。 在卡片模式時，你可以用 &lt; and > 按鈕捲動圖片，裡面有多個創意。

#### 可用行動

* 將標準顯示、標準影像及動態顯示套件加入函式庫

* 在組合中列出並預覽創意作品

* 編輯組合名稱

* 將標準展示創意加入標準展示組合包，並將標準展示創意從標準展示組合中移除

* 將標準影片創意加入標準影片組合包，並將標準影片創意從標準影片組合中移除

* 重複組合包

* 刪除套件

>[!MORELIKETHIS]
>
>* [管理創意圖書館](/help/creative/creative-libraries/creative-library-manage.md)
>* [將標準創意作品加入創意庫](creative-add-standard.md)
>* [管理創意套件](bundle-manage.md)
>* [自訂你的資料檢視](/help/creative/introduction/customize-data-views.md)
