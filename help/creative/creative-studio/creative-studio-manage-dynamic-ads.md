---
title: 在Creative Studio中管理動態創意內容
description: 瞭解如何在Adobe Advertising Creative Studio中建置、編輯、複製和刪除目錄驅動的動態創意內容。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# 在[!UICONTROL Creative Studio]中管理動態創意內容

*Beta功能*

[!UICONTROL Creative Studio]中的&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤會依程式庫列出您的動態創意。 您可以在此處建立新的目錄驅動動態創意、編輯現有創意的詳細資訊和屬性對應、檢視變更記錄、複製創意以及刪除創意。

## 建立動態創意 {#build-dynamic-creative}

使用此工作流程來建立目錄驅動的動態創意。 四步驟引導式精靈會逐步引導您選取範本、連線目錄以及將目錄欄位對應至範本元素。 安裝之後，[!UICONTROL AI Assistant]可協助您預覽和品質檢查從目錄資料產生的每個廣告組合。

動態創意內容與標準廣告有一個關鍵差異：AI代理程式無法修改目錄來源內容。 它可以篩選、分析和標幟問題，但若要變更廣告內容，您必須更新來源目錄。

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

   如果您繼續QA，畫布會顯示從目錄產生的所有廣告組合，顯示為列並在範本中呈現每個目錄專案的預覽。

1. 如果您繼續QA：

   1. 執行下列任一項作業：

      * 使用&#x200B;**[!UICONTROL Zoom in]**&#x200B;和&#x200B;**[!UICONTROL Zoom out]**&#x200B;控制項來調整畫布檢視。

      * 使用分頁控制項(**X-Y / Z**)來分頁目錄列。

      * 若要編輯廣告組合：

         1. 將游標停留在目錄列上，然後按一下&#x200B;**[!UICONTROL Edit]**。

         1. 在&#x200B;**[!UICONTROL Edit Row]**&#x200B;對話方塊中，更新欄位值。

         1. 按一下&#x200B;**[!UICONTROL Save]**。

        畫布會重新整理以反映更新的值。

      * 使用&#x200B;**[!UICONTROL AI Assistant]**&#x200B;聊天面板來分析和篩選目錄組合。 在&#x200B;**[!UICONTROL Ask anything]**&#x200B;欄位中輸入您的要求，或按一下其中一個建議的提示：

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        AI代理程式可以：

         * 篩選畫布以顯示符合特定對象區段、地理、語言、類別或其他目錄欄位的廣告。
         * 檢查品質問題，例如，字元限制溢位、內容溢位或出血、影像連結損毀，以及免責宣告可見度。
         * 比較A/B測試分析的廣告組合
         * 將廣告組織成群組，以便並排檢閱。

        AI代理程式無法修改目錄來源的內容。 若要變更廣告內容，請更新來源目錄。

   1. 在標題中儲存&#x200B;**[!UICONTROL Save Dynamic Creative]**。

   1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Create]**。

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

## 重新開啟動態創意內容的QA助理 {#qa-dynamic-creative}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**。

   QA畫面隨即開啟。 請參閱&quot;[步驟5：使用AI](#qa)預覽和QA&quot;，以取得可用的畫布控制項和AI助理功能。

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

