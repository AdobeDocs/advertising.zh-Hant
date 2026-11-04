---
title: 在Creative Studio中管理動態創意內容
description: 瞭解如何在Adobe Advertising Creative Studio中建置、品質檢查、編輯、複製和刪除目錄驅動的動態創意內容。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 88fead9ffc4eaa572be090877790422e67831036
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 0%
---
# 在[!UICONTROL Creative Studio]中管理動態創意內容

[!UICONTROL Creative Studio]中的&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤會依程式庫列出您的動態創意。 您可以在此處建立新的目錄驅動動態創意、使用AI檢查創意品質、編輯現有創意的詳細資訊和屬性對應、檢視變更記錄、複製創意以及刪除創意。

## 建立動態創意 {#build-dynamic-creative}

使用此工作流程來建立目錄驅動的動態創意。 四步驟引導式精靈會逐步引導您選取範本、連線目錄以及將目錄欄位對應至範本元素。 安裝之後，[!UICONTROL AI Assistant]可協助您預覽和品質檢查從目錄資料產生的每個廣告組合。

動態創意內容與標準廣告有一個關鍵差異：AI代理程式無法修改目錄來源內容。 它可以篩選、分析和標幟問題，但若要變更廣告內容，您必須從QA畫面或來源目錄中手動更新目錄值。

### 先決條件

* 您的範本程式庫中必須至少存在一個使用者建立的顯示廣告範本（不是系統範本）。
* 您的帳戶提供產品或內容目錄（摘要）。

### 步驟1：開啟[!UICONTROL Build Dynamic Creative]精靈 {#open-wizard}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Build dynamic creatives from catalog data]**&#x200B;快速動作卡片中的&#x200B;**[!UICONTROL Build]**。

   四個步驟的&#x200B;**[!UICONTROL Build Dynamic Creative]**&#x200B;對話方塊開啟。

### 步驟2：選取範本 {#select-template}

>[!NOTE]
>
>範本庫僅列出您建立的顯示廣告範本。 系統範本和視訊廣告範本無法當作動態創意的起點。

1. 在範本庫中，按一下範本以選取它。

   在選取範本之前，**[!UICONTROL Next]**&#x200B;按鈕為停用狀態。

1. 按一下&#x200B;**[!UICONTROL Use this template]**。

### 步驟3：選取目錄 {#select-catalog}

1. 設定創意設定：

   * **[!UICONTROL Ad Library]：**&#x200B;選取要儲存創意的創意檔案庫。
   * **[!UICONTROL Dynamic creative name]：**&#x200B;輸入動態創意的名稱。
   * **[!UICONTROL Number of cards]：**&#x200B;輸入要包含在每個廣告組合中的目錄選件數目(1-50)。
   * **[!UICONTROL Assign dynamic creative to a bundle]：** （選擇性）啟用時，儲存的創意會附加至套件組合。 從資料庫中選取束。

1. 選取一或多個目錄：

   1. （選擇性）使用&#x200B;**[!UICONTROL Catalog template]**&#x200B;將目錄清單篩選為特定範本系列。 若要選擇下載範本檔案以進行檢閱，請按一下&#x200B;**[!UICONTROL Download feed template]**。

   1. 搜尋並從清單中選取目錄。 所有選取的目錄必須屬於相同的目錄範本系列；如果您嘗試混合系列，會出現警告。

   1. （選擇性）若要上傳新的目錄檔案，請將檔案拖放至上傳區域，或按一下&#x200B;**[!UICONTROL Browse Files]**。 支援的格式：JPG、PNG、JPEG、XLS、XLSX、CSV、TSV、ZIP和MP4。 檔案大小上限： 25 MB。 您可以一次上傳一個檔案。 上傳的目錄會出現在晶片清單中，標示為&#x200B;**（已上傳）**。

1. 按一下&#x200B;**[!UICONTROL Continue]**。

### 步驟4：將目錄欄位對應至範本元素 {#attribute-mapping}

將每個目錄欄位對應至範本中對應的元素。 例如，將目錄的產品名稱欄位對應到範本的標題元素，並將產品影像欄位對應到背景影像元素。

1. 在&#x200B;**[!UICONTROL Targeting]**&#x200B;底下，選取至少一個資料來源以個人化創意： **[!UICONTROL Profile data]**、**[!UICONTROL Geographic data]**、**[!UICONTROL Data pass]**&#x200B;或&#x200B;**[!UICONTROL Audience Segment]**。

1. 對於每個範本元素，從下拉式清單中選取相符的目錄欄位。

1. 按一下&#x200B;**[!UICONTROL Continue]**。

### 步驟5：使用AI預覽和QA {#qa}

1. 選擇要&#x200B;*[!UICONTROL Save Dynamic Creative & Skip QA]*&#x200B;還是&#x200B;*[!UICONTROL Continue to QA]*。

   如果您繼續QA，**[!UICONTROL Dynamic Creative QA]**&#x200B;畫面會以預覽畫布和&#x200B;**[!UICONTROL AI Assistant]**&#x200B;聊天面板開啟。

1. 如果您繼續進行QA，請依照&quot;[品質檢查](#qa-dynamic-creative)&quot;中的程式來[分析和篩選廣告](#analyze-ads)、[檢閱預覽和警示](#review-previews)，並選擇性[修正目錄值](#correct-catalog-values)。 完成後，[儲存動態創意](#save-or-exit)。

## 編輯動態創意 {#edit-dynamic-creative}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

   全熒幕編輯器隨即開啟，左側顯示廣告預覽，右側顯示設定面板。

1. 使用&#x200B;**[!UICONTROL Details]**&#x200B;和&#x200B;**[!UICONTROL Attribute Mapping]**&#x200B;索引標籤編輯創意設定：

   **[!UICONTROL Details]**&#x200B;標籤：

   * **[!UICONTROL Advertiser]**、**[!UICONTROL Ad Library]**&#x200B;和&#x200B;**[!UICONTROL Ad template]**&#x200B;為唯讀。
   * **[!UICONTROL Dynamic creative name]：**&#x200B;創意內容的顯示名稱。
   * **[!UICONTROL Number of cards]：**&#x200B;每個廣告組合中包含的目錄選件數目(1-50)。
   * （選擇性）在&#x200B;**[!UICONTROL Catalogs]**&#x200B;下，更新目錄選擇：
     * 使用&#x200B;**[!UICONTROL Catalog template]**&#x200B;篩選可用的目錄。 若要選擇下載範本檔案，請按一下&#x200B;**[!UICONTROL Download feed template]**。
     * 從清單中搜尋並選取目錄，或透過將新目錄檔案拖曳至上傳區域或按一下&#x200B;**[!UICONTROL Browse Files]**&#x200B;以上傳新目錄檔案（支援的格式：JPG、PNG、JPEG、XLS、XLSX、CSV、TSV、ZIP、MP4；最大25 MB；一次一個檔案）。 上傳的目錄在晶片清單中標示為&#x200B;**（已上傳）**。

     所有目錄都必須屬於相同的目錄範本系列。

   **[!UICONTROL Attribute Mapping]**&#x200B;標籤：

   * 在&#x200B;**[!UICONTROL Targeting]**&#x200B;底下，選取至少一個資料來源： **[!UICONTROL Profile data]**、**[!UICONTROL Geographic data]**、**[!UICONTROL Data pass]**&#x200B;或&#x200B;**[!UICONTROL Audience Segment]**。
   * 在&#x200B;**[!UICONTROL Attribute Mapping]**&#x200B;底下，更新每個範本圖層名稱到對應目錄欄標籤的對應。

1. 按一下&#x200B;**[!UICONTROL Update Creative]**。

## 對動態創意內容進行品質檢查 {#qa-dynamic-creative}

使用QA代理程式，對照動態創意內容的範本分析目錄列、預覽產生的廣告，並識別潛在的內容問題。 您可以使用&#x200B;**[!UICONTROL AI Assistant]**&#x200B;來篩選及分組廣告、檢閱目錄警示，以及手動修正目錄值後再發佈變更。

代理程式會從[!UICONTROL Creative Libraries]或[!UICONTROL Creative Studio]開啟&#x200B;**[!UICONTROL Dynamic Creative QA]**&#x200B;畫面。 雖然功能表標籤不同，但兩個進入點提供相同的QA功能。 分析取決於所選的創意、目錄和請求。

>[!NOTE]
>
>QA代理程式適用於動態顯示創意，而非標準創意或動態視訊創意。 在[!UICONTROL Creative Libraries]中，動作僅適用於以動態範本為基礎的動態創意內容。

### 開啟QA代理 {#open-qa-agent}

1. 透過下列任一種方式開啟已儲存的動態創意內容，以供QA使用：

   * **來自[!UICONTROL Creative Libraries]：**

     1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

     1. 按一下程式庫名稱以開啟程式庫。

     1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下動態創意名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL QA Agent]**。

   * **來自[!UICONTROL Creative Studio]：**

     1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**。

     1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，在[!UICONTROL Generate or Build Creatives]區段下方的創意程式庫中找出動態創意。

     1. 將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**。

   **[!UICONTROL Dynamic Creative QA]**&#x200B;畫面會以預覽畫布和&#x200B;**[!UICONTROL AI Assistant]**&#x200B;聊天面板開啟。

1. 如果創意內容使用多個目錄，請從標題中的&#x200B;**[!UICONTROL Catalog]**&#x200B;選取要檢閱的目錄。

   助理會分析選取的目錄。 當創意僅使用一個目錄時，目錄選擇器會停用。

### 使用AI分析和篩選廣告 {#analyze-ads}

1. 在&#x200B;**[!UICONTROL AI Assistant]**&#x200B;面板中，在&#x200B;**[!UICONTROL Ask anything]**&#x200B;中輸入請求並按&#x200B;**[!UICONTROL Enter]**，或按一下其中一個建議的提示：

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   助理會在聊天面板中回應，並將相符的目錄列顯示為畫布上的廣告預覽。 在您提交請求之前，畫布會提示您要求助理分析目錄。

1. 透過後續追蹤要求繼續精簡檢視。 助理可以協助您：

   * 依對象區段、語言、地理或郵遞區號篩選廣告。
   * 使用您指定的臨界值檢查字元長度。
   * 檢查摘要錯誤、缺少內容以及可疑內容。
   * 檢閱翻譯狀態。
   * 比較A/B測試變體。
   * 將廣告分組以供審閱，例如依產品或問題分組。

   驗證助理的回應並在儲存變更前檢查預覽。

### 檢閱預覽和警示 {#review-previews}

* 使用畫布工具列可以：

  * 調整縮放。
  * 在&#x200B;**[!UICONTROL Thumbnail view]**&#x200B;和&#x200B;**[!UICONTROL Actual size]**&#x200B;之間切換。
  * 按一下&#x200B;**[!UICONTROL Replay animations]**&#x200B;以重播預覽。
  * 選取每頁的列數、選取頁碼，或使用&#x200B;**[!UICONTROL Previous page]**&#x200B;和&#x200B;**[!UICONTROL Next page]**。

* 當助理群組結果時，按一下連結即可檢視群組中的所有創意內容。 使用&#x200B;**[!UICONTROL Back to groups]**&#x200B;返回群組結果，或使用&#x200B;**[!UICONTROL Catalog Rows]**&#x200B;離開群組檢視。

* 預覽顯示&#x200B;**[!UICONTROL Issues detected]**&#x200B;時，將游標停留在指標上可檢視問題詳細資訊。

* 當目錄警示可用時，按一下&#x200B;**[!UICONTROL View Alerts]**。 **[!UICONTROL Alerts]**&#x200B;對話方塊列出每個問題的目錄、列號、欄和錯誤訊息。 按一下&#x200B;**[!UICONTROL Close]**&#x200B;以返回畫布。

### 正確的目錄值 {#correct-catalog-values}

您無需離開QA畫面，即可手動編輯廣告預覽的目錄值。

1. 在您要修正的預覽上，按一下&#x200B;**[!UICONTROL Edit]**。

1. 在編輯對話方塊中，選取要在&#x200B;**[!UICONTROL Catalog columns to edit]**&#x200B;下變更的欄。 若要尋找欄，請使用&#x200B;**[!UICONTROL Search columns]**。

1. 在&#x200B;**[!UICONTROL Columns content]**&#x200B;底下，更新選取的欄位值。

1. 按一下&#x200B;**[!UICONTROL Update]**。

   預覽會重新整理以反映更新的值。 除非您儲存動態創意，否則目錄變更不會發佈。

>[!IMPORTANT]
>
>這些編輯會更新目錄資料，而不僅僅是廣告預覽。 請先檢閱值，然後再發佈。

### 儲存變更或退出 {#save-or-exit}

* 若要儲存動態創意內容並發佈任何目錄編輯：

  1. 按一下標頭中的&#x200B;**[!UICONTROL Save Dynamic Creative]**。

  1. 確認儲存：

     * 對於新創意，在&#x200B;**[!UICONTROL Create Dynamic Creative]**&#x200B;確認對話方塊中，按一下&#x200B;**[!UICONTROL Create]**。
     * 針對現有的創意，在&#x200B;**[!UICONTROL Update Dynamic Creative]**&#x200B;確認對話方塊中，按一下&#x200B;**[!UICONTROL Update]**。

     您會根據開啟QA畫面的位置，返回創意程式庫或[!UICONTROL Creative Studio]。

* 若要離開而不發佈擱置的目錄編輯，請按一下頁面標頭中的&#x200B;**[!UICONTROL Cancel]**。

## 檢視動態創意內容的變更記錄 {#view-change-log}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Change Log]**。

## 複製動態創意 {#duplicate-dynamic-creative}

複製動態創意內容，以使用相同設定將新創意內容新增至程式庫。 您稍後可重新命名新的創意內容，並視需要編輯設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

   新創意命名為`<original name> (copy)`。

## 刪除動態創意 {#delete-dynamic-creative}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [關於Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理標準廣告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理範本](creative-studio-manage-templates.md)
