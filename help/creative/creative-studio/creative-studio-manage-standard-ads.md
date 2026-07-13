---
title: 在Creative Studio中管理標準廣告
description: 瞭解如何在Creative Studio創意內容庫中建立、編輯、複製、下載和刪除標準顯示廣告。
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# 在[!UICONTROL Creative Studio]中管理標準廣告

*Beta功能*

[!UICONTROL Creative Studio]中的&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤是從範本產生的標準顯示廣告資料庫。 從這裡，您可以使用[!UICONTROL Ad Variations Generator]建立廣告、編輯已儲存的廣告、從現有廣告產生新的變化、檢視變更記錄、複製、下載和刪除。

## 建立標準廣告 {#create-standard-ads}

使用[!UICONTROL Ad Variations Generator]從範本產生顯示廣告內容。 AI助理會產生並精簡標題、CTA、影像、顏色等，並可在單一工作階段中建立新的大小變體。

>[!NOTE]
>
>標準廣告產生目前僅支援顯示廣告範本。 視訊廣告範本無法從&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤或&#x200B;**[!UICONTROL Templates]**&#x200B;標籤當作起點。

### 先決條件

您的範本資料庫中必須至少存在一個顯示廣告範本。

### 產生標準廣告

1. 以下列其中一種方式開啟[!UICONTROL Ad Variations Generator]：

   * **從[!UICONTROL Creatives]索引標籤：**

      1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

      1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Generate standard ads from templates]**&#x200B;快速動作卡片中的&#x200B;**[!UICONTROL Generate]**。

      1. 在範本選取對話方塊中，按一下範本以選取它，然後按一下&#x200B;**[!UICONTROL Use this template]**。

   * （僅限顯示廣告） **從[!UICONTROL Templates]標籤：**

      1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

      1. 按一下「**[!UICONTROL Templates]**」標籤。

      1. 將游標停留在範本卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**。

   [!UICONTROL Ad Variations Generator]隨即開啟。 畫布會顯示包含範本可用廣告格式的&#x200B;**[!UICONTROL Template Sizes]**&#x200B;區段，以及將顯示所產生內容的&#x200B;**[!UICONTROL Ad Concepts]**&#x200B;區段。

1. （選用）若要將品牌設定檔套用至廣告，請在畫布工具列中選取&#x200B;**[!UICONTROL Brand Profile]**。

   AI助理在產生內容時，會使用您品牌的標誌、調色盤、語音准則、影像標準和管道准則。

1. 使用[!UICONTROL AI Assistant]建立廣告變化：

   1. 在&#x200B;**[!UICONTROL Ask AI to generate ad variations…]**&#x200B;欄位中，輸入要求並按&#x200B;**[!UICONTROL Enter]**，或按一下其中一個精選提示：

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      AI會在畫布上產生結果，並將結果組織成&#x200B;*概念*，每個概念代表不同的內容變數。 **[!UICONTROL Ad Concepts]**&#x200B;區段中的概念計數器會追蹤有多少概念存在(例如，**(2/10)**)。 每個工作階段最多允許10個概念。

   1. 傳送後續訊息以繼續精簡。 範例：

      * 「讓所有文案變得更好玩，更少企業化。」
      * 「將標誌變更為白色版本。」
      * 「將CTA設定為『立即購買』所有概念。」
      * 「將此廣告大小調整為全部6個IAB標準顯示大小。」
      * 「提供3個不同的標題概念，每個概念都有相符的背景影像。」

      >[!NOTE]
      >
      >AI Assistant可以產生及修改文字（標題、副標題、CTA、內文）、交換背景影像、套用品牌顏色、切換標誌版本，以及建立新大小的範本。 它無法變更範本結構：元素位置、版面、間距、邊框間距、字型系列、字型大小或框線。 在啟動工作階段之前，在範本編輯器中執行結構變更。 請參閱[編輯範本](creative-studio-manage-templates.md#edit-template)。

   1. （選擇性）若要在要求中包含視覺參考，請按一下聊天輸入區域中的&#x200B;**[!UICONTROL +]**&#x200B;按鈕。 在&#x200B;**[!UICONTROL Select from Asset Library]**&#x200B;對話方塊：

      * 若要在資產庫中使用資產，請按一下資產，然後按一下&#x200B;**[!UICONTROL Add to chat]**。 提交您的訊息，將資產加入為內容。

      * 若要上傳一或多個資產，請按一下&#x200B;**[!UICONTROL Upload Assets]**&#x200B;並選取裝置或網路上的檔案。

1. （可選）使用畫布工具列來檢閱產生的廣告：

   * **[!UICONTROL Brand]：**&#x200B;選取或變更套用至工作階段的品牌設定檔。
   * **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]：**&#x200B;調整畫布縮放等級。
   * **[!UICONTROL Fit to screen]：**&#x200B;重設檢視以顯示所有大小。
   * **[!UICONTROL Replay animations]：**&#x200B;重播範本動畫。

   當AI建立新大小時，**[!UICONTROL Adjust]**、**[!UICONTROL Keep]**&#x200B;和刪除控制項會出現在新大小卡片上。 按一下&#x200B;**[!UICONTROL Keep]**&#x200B;接受目前的大小，按一下&#x200B;**[!UICONTROL Adjust]**&#x200B;在顯示編輯器中開啟範本（您可以在其中進行結構變更），然後按一下&#x200B;**[!UICONTROL Update Ad Format]**&#x200B;儲存，或按一下刪除圖示移除新大小。

1. （選用）管理概念和變數：

   * 若要管理概念，請將游標停留在概念標籤上（例如&#x200B;**[!UICONTROL Concept 3]**），按一下&#x200B;**[!UICONTROL ...]**，然後選取選項：

      * **[!UICONTROL Add to chat]：**&#x200B;在下一個提示中參考概念。
      * **[!UICONTROL Delete]：**&#x200B;移除概念。

   * 若要管理個別的變數，請將游標放在變數卡片上，按一下&#x200B;**[!UICONTROL ...]**，然後選取一個選項：

      * **[!UICONTROL Add to Chat]：**&#x200B;在下一個提示中參考變數。 您也可以直接按一下變化卡片內文，切換提及內容。
      * **[!UICONTROL Edit Data]：**&#x200B;開啟對話方塊，您可以在其中更新變數&#x200B;**[!UICONTROL Name]**&#x200B;以及範本中定義之每個點按標籤的點進URL。 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以套用。
      * **[!UICONTROL Delete]：**&#x200B;移除變數。

1. 當您對產生的概念感到滿意時，請按一下標題中的&#x200B;**[!UICONTROL Save Standard Ads]**。

   在至少存在一個概念之前，按鈕會停用。

1. 在&#x200B;**[!UICONTROL Save Standard Ads]**&#x200B;對話方塊中，指定下列設定，然後按一下&#x200B;**[!UICONTROL Save Standard Ads]**。

   **[!UICONTROL Advertiser]：** （必要）要儲存創意的廣告商。

   **[!UICONTROL Creative Library]：** （必要）要將創意內容儲存到的創意內容庫。 在您選取廣告商後，資料庫選擇器便會啟用。

   **[!UICONTROL Attach to Bundles]：** （選擇性）啟用時，儲存的創意會附加至一或多個組合。 針對每個廣告變化，選取組合或輸入新的組合名稱。

   **\[每個廣告的設定\]：**&#x200B;對於每個廣告變數，您可以檢視並選擇變更&#x200B;**[!UICONTROL Name]、**、**[!UICONTROL Language]、**&#x200B;和&#x200B;**[!UICONTROL click URL]。**

## 編輯標準廣告 {#edit-standard-ad}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

   全熒幕編輯器隨即開啟，左側顯示即時廣告預覽，右側顯示設定面板。

1. 使用&#x200B;**[!UICONTROL Details]**&#x200B;和&#x200B;**[!UICONTROL Attributes]**&#x200B;標籤編輯廣告設定：

   **[!UICONTROL Details]**&#x200B;標籤：

   * **[!UICONTROL Creative Name]：** （必要）創意內容的顯示名稱。
   * **[!UICONTROL Language]：** （必要）廣告內容的語言。
   * **[!UICONTROL Creative Size]：** （唯讀）廣告維度。
   * **點按標籤：**&#x200B;如果範本定義了點按標籤，則每個點按標籤都會顯示為標示標籤名稱的必填欄位。 輸入每個標籤的點進目的地URL。
   * **[!UICONTROL Label]：** （選用）用於組織創意的標籤。 選取現有標籤，或輸入新標籤並按一下&#x200B;**[!UICONTROL Add tag].**

   **[!UICONTROL Attributes]**&#x200B;標籤：

   即時預覽會在您編輯時即時更新。 載入預覽時，**[!UICONTROL Attributes]**&#x200B;索引標籤無法使用。

   * **文字屬性：**&#x200B;輸入範本中定義的每個可編輯文字圖層的文字值。
   * **影像屬性：**&#x200B;顯示目前影像的縮圖。 按一下&#x200B;**[!UICONTROL Replace Image]**&#x200B;以上傳替代專案（PNG、JPEG、GIF、WebP或SVG）。

1. 按一下&#x200B;**[!UICONTROL Update Creative]**。

## 產生標準廣告的廣告變化 {#generate-ad-variations}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**。

   [!UICONTROL Ad Variations Generator]會開啟，並預先載入所選的廣告。

1. 使用AI聊天介面來產生和調整其他變化。 如需完整工作流程，請參閱&quot;[建立標準廣告](#create-standard-ads)&quot;。

## 複製標準廣告 {#duplicate-standard-ad}

複製標準廣告，以使用相同設定將新創意內容新增到媒體櫃。 您稍後可重新命名新的創意內容，並視需要編輯設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

   新創意命名為`<original name> (copy)`。

## 檢視標準廣告的變更記錄 {#view-change-log}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Change Log]**。

   隨即開啟對話方塊，顯示廣告變更的表格。

## 下載標準廣告 {#download-standard-ad}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   創意內容會根據瀏覽器的正常程式下載。

## 刪除標準廣告 {#delete-standard-ad}

>[!NOTE]
>
>此動作無法復原。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;索引標籤上，將游標停留在創意卡片上，然後按一下&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [關於Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理動態創意內容](creative-studio-manage-dynamic-ads.md)
>* [在Creative Studio中管理範本](creative-studio-manage-templates.md)
>* [在Advertising Creative中管理品牌設定檔](/help/creative/brands/brand-manage.md)

