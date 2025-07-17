---
title: 關於您的創意程式庫
description: 瞭解如何管理廣告體驗的創意內容。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 056502f8c634ee62b750d7c4c188dc248b836a5a
workflow-type: tm+mt
source-wordcount: '1412'
ht-degree: 0%

---

# 關於您的創意程式庫

*封閉Beta版功能*

您的創意程式庫可讓您管理將在廣告體驗中使用的創意內容。 您可以建立多個程式庫，每個程式庫都包含一組創意和&#x200B;*創意組合*，這些創意組合是您可以以單一單位新增到體驗中的創意群組。

您的程式庫可以包括：

* **個別創意：**&#x200B;您可以直接在廣告體驗中包含沒有定義使用者目標的個別創意。 您也可以使用您的創意內容來建立組合，這些組合可包含在鎖定的[廣告體驗](/help/creative/experiences/experience-about.md)中。

   * **標準創意：**&#x200B;您可以上傳和管理[各種格式的創意](#creative-creative-formats)。 對於每個創意，您為與創意相關的每個廣告指定預設語言，並指定當使用者按一下包含創意的廣告時開啟的預設登陸頁面。 您可以選擇指定標籤，以在[!DNL Creative]內的各種檢視中作為篩選器使用，並在包含使用[!UICONTROL Custom Creative Report]維度時作為[!UICONTROL Creative Label]中的欄值使用。

   * **動態創意：** (僅限現有Adobe Advertising DCO客戶)管理員使用者可以將廣告範本中的動態變數對應到摘要檔案中的值，以建立動態產生的創意。 所有使用者都可以預覽、複製和刪除現有的動態廣告。

* **創意組合：**&#x200B;將創意分組為組合，以搭配定義的使用者目標用於多個體驗。 您可以建立包含標準顯示廣告的&#x200B;*標準顯示組合*、包含標準視訊廣告的&#x200B;*標準視訊組合*，以及包含動態產生之顯示廣告的&#x200B;*動態顯示組合*。

## 支援的Creative格式 {#creative-creative-formats}

### 標準創作的格式

您可以在[支援的創意大小](creative-sizes.md)中新增和管理下列創意型別。

>[!IMPORTANT]
>
>* 即使您打算將HTML5、彈性HTML5或協力廠商創意內容用於標準顯示廣告體驗，您也必須為您使用的每個創意大小新增影像創意內容。
>* 每個標準顯示體驗都需要為指派給體驗的每個創意大小提供預設影像創意。 當瀏覽器未啟用JavaScript或廣告伺服器因延遲而無法個人化廣告時，就會使用預設影像創意。
>* 每個標準視訊體驗都需要為指派給體驗的每個創意期間提供預設的視訊創意。<!-- when is it used? -->

#### 彈性的HTML5

有彈性的HTML5創意人員是HTML5創意人員，擁有其所有影像和其他屬性做為標準HTML標籤，您可以直接在[!DNL Creative]中編輯，無論是在創意資料庫中或是在個別體驗中（這會建立原始創意的變體）。 在DSP中，彈性的HTML5創意內容適用於單一特定廣告大小（以畫素為單位）。 您可以選擇變更彈性HTML5創意內容中所指定屬性的預設值。 稍後，您可以為特定體驗中的屬性指定自訂值，這會建立父級創意內容的變體。

您可以上傳彈性的HTML5創意內容當作ZIP檔案，或使用其中一個範本作為起點。 檢視彈性HTML5創意的[規格](html5-creative-specification.md)。

#### HTML5創意

您可以上傳簡單或靜態的HTML5創作，並指定所有屬性和影像做為ZIP檔案。 您無法編輯任何屬性或新增影像；請改為上傳新的ZIP檔案以新增創意。 檢視簡單和靜態HTML5創意的[規格](html5-creative-specification.md)。

#### 影像創意

您可以在GIF、JPEG、JPG或PNG格式中包含影像創意。 您可以從您的Adobe Experience Manager帳戶上傳已核准的影像，或從您的裝置或網路上傳影像。

每個標準顯示廣告體驗都需要為指派給體驗的每個創意大小提供預設影像創意。

#### 協力廠商創意人員

輸入協力廠商廣告伺服器上託管創意內容的JavaScript追蹤標籤。 指令碼會依廣告伺服器而有所不同；範例如下：

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### 視訊創意 {#creative-video-specs}

您可以從您的裝置或網路上傳適用於Web、行動或連線電視的第一方視訊創意。 每個標準視訊廣告體驗都需要為指派給體驗的每個創意期間提供預設的視訊創意。 DSP會自動將所有影片創意內容轉碼為VAST 2.0標籤，以便您預覽。 在[!UICONTROL Tag Manager]中，您可以選擇將[發行者特定的轉碼](/help/creative/experiences/experience-tag-video-transcoding.md)套用至任何視訊廣告體驗標籤。

請參閱下列視訊創作需求。 **注意：**&#x200B;如果您要將視訊體驗上傳至Advertising DSP，請同時參閱DSP對高畫質視訊Assets的[需求](https://experienceleague.adobe.com/zh-hant/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets)，此需求可能會比較受限。

**檔案型別：** .mov、.mp4、.webm

**檔案大小：**&#x200B;最大512 MB

**視訊外觀比例：** 16:9、4:3

**視訊解析度：** 640x360 (360p)、1280x720 (720p)、1920x1080 (1080p)

**視訊長度：**&#x200B;最多90秒

**位元速率：** 600-1200 kbps (360p)、1500-2500 kbps (720p)、3000-5000+ kbps (1080p)

**視訊影格速率：** 23.98 FPS。 根據地區或發佈商的要求，可接受額外的影格速率

**視訊轉碼器：** H.264 （業界標準）、AV1、H.265

**音訊格式：** ACC （業界標準/MP4）、Opus (WebM/AV1)

**音訊位元速率：** 16-512 kbps

**音訊取樣速率：** 44100-48000 Hz

**音訊速率：** 44.1kHz或48 kHz

**其他音訊：**&#x200B;上傳的檔案必須為非交錯式、混合式且包含音軌。 可能沒有音效，但視訊檔案中必須包含音軌。

### 動態廣告的格式

管理員使用者可透過將廣告範本中的動態變數對應至摘要檔案中的值，以動態方式產生靜態HTML5和動態HTML5格式的創意。 動態創意內容可能包含來自舊版Adobe Advertising Dynamic Creative Optimization (DCO)體驗的創意內容。

## [!UICONTROL Creative Libraries]檢視

如需自訂每個檢視的詳細資訊，請參閱[自訂您的資料檢視](/help/creative/introduction/customize-data-views.md)。

### [!UICONTROL Creative Libraries]主要檢視

[!UICONTROL Creative Libraries]主要檢視會顯示您的所有創意程式庫。 每個資料庫的資料包含指派給資料庫套裝的體驗數量、套裝數量、創意內容數量、創意大小數量、預設語言目標數量、建立日期，以及資料庫任何元素的最後修改日期。 表格模式也包含廣告商欄。

當您處於卡片模式時，可以使用&lt;和>按鈕，捲動程式庫中多個創意部分的影像。

#### 可用動作

* [建立新程式庫](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* 對於每個創意內容庫：

   * [編輯程式庫名稱](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [開啟程式庫以檢視指派給程式庫的創意和組合](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [刪除程式庫](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]檢視

#### [!UICONTROL Standard Ads]

[!UICONTROL Standard Ads]索引標籤會顯示您已建立的所有標準創意。 每個創意的資料包括創意大小、創意型別和建立日期。 表格模式也包含預設語言和預設登陸頁面的欄。

##### 可用動作

* [將標準創意內容新增至程式庫](creative-add-standard.md)

* [編輯標準創意](creative-edit-standard.md)

* [預覽標準創意](creative-preview.md)

* [將標準創意加入標準顯示組合，並從標準顯示組合中移除標準創意](creative-attach-detach-bundles.md)

* [將視訊創意內容新增至標準視訊組合，並從標準視訊組合中移除視訊創意內容](creative-attach-detach-bundles.md)

* [複製標準創意](creative-duplicate.md)

* [下載標準創意內容](creative-download.md)

* [刪除標準創意](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

[!UICONTROL Dynamic Ads]索引標籤會顯示為您的創意目錄動態建立的所有動態創意，但您從[索引標籤](creative-delete.md)手動刪除[!UICONTROL Dynamic Ads]的任何動態創意除外。 如果您[手動複製](creative-duplicate.md)自上次處理目錄以來的任何動態創意，則該目錄的創意清單也包含重複的創意。

每個創意的資料包括創意型別、創意大小、創意所屬的目錄數量和建立日期。 表格模式也包含產生創意的範本欄和選件計數。

>[!NOTE]
>
>每次處理目錄時，該目錄的現有動態創意內容都會重新整理資料。

##### 可用動作

目前僅Adobe客戶團隊可建立及編輯動態創意內容。 不過，所有使用者都可以：

* [預覽動態創意內容](creative-preview.md)

* [將動態創意新增至動態顯示組合，並從動態顯示組合中移除動態創意](creative-attach-detach-bundles.md)

* [複製動態創意](creative-duplicate.md)

* [刪除動態創意](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]檢視

[!UICONTROL Bundles]檢視會顯示您的所有標準和動態套件組合容器。 您可以檢視每個套件組合中包含的創意內容名稱、創意大小和語言。 當您處於卡片模式時，可以使用&lt;和>按鈕捲動包含多個創意的套件組合中的影像。

#### 可用動作

* 新增標準顯示、標準視訊和動態顯示套件組合至程式庫

* 列出及預覽組合中的創意

* 編輯套件組合名稱

* 將標準顯示創意加入標準顯示組合，並從標準顯示組合中移除標準顯示創意

* 將標準視訊創意內容新增至標準視訊組合，並從標準視訊組合中移除標準視訊創意內容

* 複製組合

* 刪除組合

>[!MORELIKETHIS]
>
>* [管理創意內容庫](/help/creative/creative-libraries/creative-library-manage.md)
>* [將標準創意內容新增至創意內容庫](creative-add-standard.md)
>* [管理創意組合](bundle-manage.md)
>* [自訂您的資料檢視](/help/creative/introduction/customize-data-views.md)
