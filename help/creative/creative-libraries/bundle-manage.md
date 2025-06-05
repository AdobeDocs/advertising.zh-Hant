---
title: 管理創意組合
description: 瞭解xxxx。
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: baba02d2537828f1ed0b5c7842d1f987a55f5ef0
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# 管理創意組合

*已關閉的Beta*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

組合是創意作品群組，您可以將其作為一個單元新增到體驗中。 建立束容器後，您可以將創意附加至束。 標準套件組合只能包含標準廣告，而動態套件組合只能包含動態廣告。 您可以覆寫套件中所有創意的登陸頁面、曝光追蹤標籤，以及點選追蹤標籤，這些創意會從體驗決策樹內指派給體驗，而不會影響基本創意內容。

[!DNL Creative]會依指派給組合的每個體驗之指定，在組合中旋轉創意。 您可以選擇允許[!DNL Creative]使用演演算法廣告輪換(由Adobe Sensei提供技術支援)，根據效能最佳化任何體驗的廣告元素。

若要在廣告體驗中跨套件組合最佳化廣告元素，每個套件組合只能包含每個\[創意大小+語言\]組合之一。 例如，如果套件中包含一個預設語言為「法文」的250x250創意內容，則您無法新增預設語言為「法文」的第二個250x250創意內容。 如果您有多個相同大小的創意專案使用相同的語言，請將其個別新增至體驗。

附加至組合的原創作品仍可作為個別原創作品使用。 您可以將單一創意內容新增至多個組合。 如果您編輯附加至束的創意內容的任何設定，則變更會傳播至束。 不過，為體驗中的創意設定的任何自訂登陸頁面、曝光追蹤標籤，以及點選追蹤標籤，一律會用於體驗。

<!-- multiselect only to duplicate and delete -->

## 為創意資源庫建立套件組合

您可以將創意內容附加至多個組合。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**。

1. 輸入唯一的&#x200B;**[!UICONTROL Bundle Name]**&#x200B;和&#x200B;**[!UICONTROL Bundle Type]：** *標準* （適用於標準創意）或&#x200B;*動態* (適用於動態創意。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 列出套件組合中的創意內容

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定資料庫。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 按一下束卡或列以檢視束中的所有創意。

## 複製組合

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定資料庫。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 選取要複製的組合：

   * 若要複製單一組合：

      * 在卡片檢視中，按一下組合名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Duplicate]**。

      * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Duplicate]**。

   * 若要複製一或多個束，請選取要複製的每個束的核取方塊。 在大量動作工具列中按一下&#x200B;**[!UICONTROL Duplicate].**

     若要選取所有列，請選取左上方的全域核取方塊。

   新組合命名為`<original name> (copy) # 1` （或序列中的下一個編號）。 例如，如果您製作「測試組合」的兩個重複專案，則這些重複專案會命名為「測試組合（副本） # 1」和「測試組合（副本） # 2」。

## 編輯套件組合名稱

對套件名稱的變更會傳播到所有關聯的體驗。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 選取束：

   * 在卡片檢視中，按一下資料庫名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Edit]**。

   * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯&#x200B;**[!UICONTROL Bundle Name]**。

   [!UICONTROL Bundle Name]必須是唯一的。

1. 按一下&#x200B;**[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## 將創意內容附加至組合

您可以將[現有的標準創意](/help/creative/creative-libraries/creative-libraries-about.md)附加至標準組合，並將現有的動態創意<!-- [existing dynamic creatives](creative-dynamic-manage.md) -->附加至動態組合。 將創意附加至搭售方案會讓創意內容可在指派給搭售方案的所有體驗中使用。 每個組合只能包含每個\[創意大小+語言\]組合中的一個。

>[!NOTE]
>
>您也可以[從標準廣告和動態廣告檢視](creative-attach-detach-bundles.md)將創意內容附加至組合。

### 從組合清單將創意附加至組合

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定資料庫。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 選取束：

   * 在卡片檢視中，按一下組合名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Attach Creatives]**。

   * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Attach Creatives]**。

   符合束型別資格的每個創意內容都會列在右方框架中。 已附加至該套裝的創意內容會列出，但無法選取。

1. （選擇性）按一下![卡片檢視](/help/creative/assets/card-view-button.png "卡片檢視")以開啟卡片檢視，或按一下![表格/清單檢視](/help/creative/assets/table-view-button.png "表格檢視")返回表格檢視，在預設表格檢視與可用套裝的卡片檢視之間切換。

1. 在右方框架中，選取每個要附加至搭售方案之創意內容旁的核取方塊，然後按一下&#x200B;**[!UICONTROL Attach Creative to Bundle]**。

### 從套裝的創意清單將創意內容附加至套裝

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定資料庫。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 按一下束卡或列以檢視束中的所有創意。

1. 按一下右上角的&#x200B;**[!UICONTROL Attach Creatives]**。

1. 在右側面板中，選取您要附加的每個創意內容的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Attach Creatives to Bundle]**。

## 將創意內容從套件中分離 {#bundle-detach-creatives}

將創意內容從套件分離會移除兩者之間的關聯，因此創意內容將不再用於鎖定套件為目標的體驗。

將創意內容從套件中分離，並不會將創意內容從創意內容庫中的「創意內容」索引標籤中刪除。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定資料庫。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 按一下束卡或列以檢視束中的所有創意。

1. 選取要從束分離的創意：

   * 若要分離單一創意內容：

      * 在卡片檢視中，按一下創意名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Detach]**。

      * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Detach]**。

   * 若要分離一或多個創意，請選取欲分離的每個創意的核取方塊。 在大量動作工具列中按一下&#x200B;**[!UICONTROL Detach]**。

     若要選取所有列，請選取左上方的全域核取方塊。

## 預覽套件組合中的單一創意

您可以在檢視者看到創意時加以預覽，包括超連結。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定資料庫。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 按一下束卡或列以檢視束中的所有創意。

1. 選取創意：

   * 在卡片檢視中，按一下創意名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Preview]**。

   * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Preview]**。

1. （選擇性）若要調整熒幕中的影像大小，請選取&#x200B;**[!UICONTROL Zoom]**&#x200B;清單中的選項，從影像大小的10%到100%。

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. （選用）若要開啟創意的登陸頁面，請按一下創意內容。

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. （選擇性）若要下載創意，請按一下![下載](/help/creative/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

## 預覽套件組合中的所有創意內容

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 選取束：

   * 在卡片檢視中，按一下組合名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Preview]**。

   * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Preview]**。

1. （選擇性）若要依語言篩選創意，請選取&#x200B;**[!UICONTROL Language]**&#x200B;清單中的選項，然後按一下預覽右上角的&#x200B;**[!UICONTROL Preview]**。

1. （選擇性）若要依大小篩選創意，請在&#x200B;**[!UICONTROL Size]**&#x200B;清單中選取選項，然後按一下預覽右上角的&#x200B;**[!UICONTROL Preview]**。

1. （選擇性）若要調整熒幕中影像的大小，請選取&#x200B;**[!UICONTROL Zoom]**&#x200B;清單中的選項，從影像大小的10%到100%。

1. （選用）若要開啟創意內容的登陸頁面，請按一下創意內容。

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. （選用）若要共用示範URL，讓未登入[!DNL Creative]的其他人可以預覽創意內容：

   1. 按一下預覽右上角的![共用](/help/creative/assets/share.png "共用")。

   1. 在[!UICONTROL Share Demo URL]對話方塊中，按一下&#x200B;**[!UICONTROL Copy]**&#x200B;將URL複製到剪貼簿，以便與其他人共用。

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## 刪除組合

您可以刪除未指派給[即時](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses)體驗的組合。 如果將組合指派給即時體驗，請在繼續之前[從決策樹](/help/creative/experiences/experience-target-node-delete.md)移除該組合以供該體驗使用。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （選擇性） [自訂檢視](/help/creative/introduction/customize-data-views.md)以包含特定資料庫。

1. 按一下程式庫名稱。

1. 按一下「**[!UICONTROL Bundles]**」標籤。

1. 選取要刪除的組合：

   * 若要刪除單一組合：

      * 在卡片檢視中，按一下組合名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Delete]**。

      * 在表格檢視中，將游標停留在資料列上並按一下&#x200B;**[!UICONTROL Delete]**。

   * 若要刪除一個或多個束，請選取要刪除的每個束的核取方塊。 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete].**

     若要選取所有列，請選取左上方的全域核取方塊。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [指派和取消指派創意組合至體驗中的最終節點](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [預覽創意](/help/creative/creative-libraries/creative-preview.md)
>* [將標準創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-standard.md)
>* [管理創意內容庫](/help/creative/creative-libraries/creative-library-manage.md)
>* [關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)
