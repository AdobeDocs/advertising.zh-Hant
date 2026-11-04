---
title: 產生彈性HTML5創意專案的變體
description: 瞭解如何從創意資料庫產生並儲存彈性HTML5創意的AI輔助變體。
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# 產生彈性HTML5創意專案的變體

使用[!UICONTROL Ad Variations Generator]建立現有彈性HTML5創意內容的新變體。 AI助理會產生並精簡標題、CTA、影像、顏色等，並可在單一工作階段中建立新的大小變體。 將產生的變化儲存為創意資料庫中的新標準廣告。

>[!NOTE]
>
>您也可以從[!UICONTROL Creative Studio]產生廣告變化。 兩個進入點開啟相同的[!UICONTROL Ad Variations Generator]。 如需其他進入點，請參閱&quot;[在Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations)中產生標準廣告的廣告變化&quot;。

## 可用性 {#availability}

在新的[!UICONTROL Creative Libraries] UI中，**[!UICONTROL Generate Variations]**&#x200B;動作可用於彈性的HTML5創意，包括基於系統範本的創意。 它不適用於其他創意型別，包括動態創意內容。

當創意內容沒有產生器所需的內部父級廣告範本參考時，會停用動作。 此參考不是您可以編輯的設定；在創意的&#x200B;**[!UICONTROL Template]**&#x200B;索引標籤上傳或取代檔案時不會明確設定此參考。

## 開啟廣告變化產生器 {#open-generator}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 以下列其中一種方式開啟程式庫：

   * 按一下程式庫名稱。
   * 在程式庫名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Open]**」。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下彈性HTML5創意名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Generate Variations]**。

   [!UICONTROL Ad Variations Generator]會開啟，其中包含所選創意的內容。 畫布會顯示包含範本可用廣告格式的&#x200B;**[!UICONTROL Template Sizes]**&#x200B;區段，以及將顯示所產生內容的&#x200B;**[!UICONTROL Ad Concepts]**&#x200B;區段。

## 產生和調整變數 {#generate-variations}

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
      >AI Assistant可以產生及修改文字（標題、副標題、CTA、內文）、交換背景影像、套用品牌顏色、切換標誌版本，以及建立新大小的範本。 它無法變更範本結構：元素位置、版面、間距、邊框間距、字型系列、字型大小或框線。 在啟動工作階段之前，在範本編輯器中執行結構變更。 請參閱[編輯範本](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template)。

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

## 儲存變數 {#save-variations}

1. 當您對產生的概念感到滿意時，請按一下標題中的&#x200B;**[!UICONTROL Save Standard Ads]**。

   在至少存在一個概念之前，按鈕會停用。

1. 在&#x200B;**[!UICONTROL Save Standard Ads]**&#x200B;對話方塊中，檢閱下列設定，然後按一下&#x200B;**[!UICONTROL Save Standard Ads]**。

   **[!UICONTROL Advertiser]：**&#x200B;與來源創意程式庫關聯的廣告商。 您無法變更此值。

   **[!UICONTROL Creative Library]：**&#x200B;儲存新廣告的來源創意庫。 您無法變更此值。

   **[!UICONTROL Attach to Bundles]：** （選擇性）啟用時，儲存的創意會附加至一或多個組合。 針對每個廣告變化，選取組合或輸入新的組合名稱。

   **\[每個廣告的設定\]：**&#x200B;對於每個廣告變數，您可以檢視並選擇性地變更每個點按標籤的&#x200B;**[!UICONTROL Name]**、**[!UICONTROL Language]**&#x200B;和點進URL。

   您會回到創意內容庫。

>[!MORELIKETHIS]
>
>* [編輯標準創意](creative-edit-standard.md)
>* [在Creative Studio中管理標準廣告](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [在Advertising Creative中管理品牌設定檔](/help/creative/brands/brand-manage.md)
>* [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)中的[C2PA中繼資料
