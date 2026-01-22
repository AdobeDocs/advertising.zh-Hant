---
title: 將標準創意內容新增至創意內容庫
description: 瞭解如何將標準（非動態）創意內容新增至創意內容庫。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: a1ca7815334b35de8f9ab5781e53e6b6aa5f4770
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---

# 將標準創意內容新增至創意內容庫

新增標準創意內容至您的[創意資料庫](creative-library-manage.md)，以搭配標準[廣告體驗](/help/creative/experiences/experience-about.md)使用。

>[!NOTE]
>
> 您可以直接在廣告體驗中加入沒有定義使用者目標的個別創意內容。 您也可以將創意內容分組到[組合](bundle-manage.md)中，將其包含在鎖定目標的廣告體驗中。

## 將彈性的HTML廣告新增至創意內容庫 {#flexible-creative-add}

您可以執行下列任一項作業：

* 在ZIP檔案中上傳您自己的彈性創意。

* 使用任何已上傳至您帳戶的預先定義彈性創意範本，作為您自己的彈性創意的起點。

### 上傳您自己的彈性創意 {#flexible-creative-upload}

您可以上傳多個彈性的創意單位。 彈性的創意內容必須採用ZIP格式，最大可達2 MB。 如需檔案需求，請參閱[HTML5創意規格](html5-creative-specification.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**。

1. 按一下&#x200B;**[!UICONTROL Upload New]**。

1. 以下列任一方式指定ZIP檔案：

   * 將裝置或網路上的檔案拖放至方塊中。

   * 按一下&#x200B;**[!UICONTROL Select a file]**&#x200B;以找出裝置或網路上的檔案。

   檢視[彈性廣告規格](#flexible-ad-spec)。

1. 新增或移除彈性的創意檔案：

   * 若要新增檔案，請按一下左上方的![新增](/help/creative/assets/create.png "新增")，然後在您的裝置或網路上找到檔案。

   * 若要移除檔案，請取消選取檔案旁邊的核取方塊。

1. （選擇性）若要預覽創意，請按一下影像上方的![預覽](/help/creative/assets/preview.png "預覽")。

1. 指定[彈性的HTML5廣告設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)。

   依預設，會選取您剛上傳的所有創意內容。 任何只有一個值的設定皆適用於所有選取的創意；對於某些設定，您可以指定個別值。 若要輸入特定創意的設定，請取消選取每個不適用創意旁的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Create]**

### 使用範本新增彈性創意 {#flexible-creative-use-template}

您可以使用任何上傳至您帳戶的彈性創意範本，建置預先定義大小的廣告。 選取要使用的範本後，您將會編輯點按標籤和屬性。&lt;！ — 如果我們將範本下載功能新增回，則將最後一句取代為：您可以a\)選取要使用的範本，然後編輯點按標籤和屬性；或b\) [將範本下載為ZIP檔](#download-flexible-creative-template)，離線編輯內容以建置您自己的創意，然後[將編輯後的檔案上傳為新的創意](flexible-creative-upload)。>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**。

1. 按一下&#x200B;**[!UICONTROL Browse System Flexible Templates]**。

1. （選擇性）若要預覽範本，請按一下範本名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Preview]**。

   您可以選擇下載範本：按一下範本名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Download]**。

1. 在範本名稱旁，按一下&#x200B;**[!UICONTROL ...]**，然後按&#x200B;**[!UICONTROL Use Selected]**。

1. 編輯[彈性的HTML5創意設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)以指定語言，並包含您自己的點按標籤、影像和其他屬性。

   壓縮後，創意的檔案大小上限為2 MB。<!-- Still true? -->

1. 新增或移除您自己的彈性創意檔案：

   * 若要從您的裝置或網路新增檔案，請按一下左上方的![[新增]](/help/creative/assets/create.png "[新增]")，然後找到檔案。 選取創意內容旁的核取方塊，並取消選取其他創意內容旁的核取方塊，然後編輯[彈性HTML5創意設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)，以指定語言並包含您自己的點按標籤、影像和其他屬性。

   * 若要移除檔案，請取消選取檔案旁邊的核取方塊。

1. （選擇性）若要預覽創意，請按一下影像上方的![預覽](/help/creative/assets/preview.png "預覽")。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 將標準顯示創意新增至創意資源庫

標準顯示創意包含影像和HTML5創意內容，包括從Adobe Experience Manager和Adobe GenStudio for Performance Marketing匯入的創意內容。

* 影像創意內容可以是GIF、JPEG、JPG或PNG格式。 檔案大小上限為兩(2) MB。 檢視[支援的創意大小](/help/creative/creative-libraries/creative-sizes.md)。

* 您可以一次新增多個Experience Manager資產、多個GenStudio體驗，或單一型別的多個本機HTML5創意（簡單或靜態）。 如需HTML5創意內容，請參閱[HTML5廣告規格](/help/creative/creative-libraries/html5-creative-specification.md)。

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>您也可以[新增彈性的HTML5創意](#flexible-creative-add)，這些創意是HTML5創意，具有作為標準HTML標籤的所有屬性，您可以直接在[!DNL Creative]中編輯。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Standard Display]**。

1. 指定創意：

   * 針對本機影像或HTML5資產，請執行下列其中一項作業：

      * 將裝置或網路上的檔案拖放至方塊中。

      * 按一下&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的裝置或網路上尋找檔案。

   * 針對連線至您DSP帳戶[的](/help/creative/creative-libraries/aem-assets-configure.md)Experience Manager資料庫中已核准的影像，請執行下列動作：

      1. 按一下&#x200B;**[!UICONTROL AEM Asset Library]**。

      1. (如果您尚未登入您的Experience Manager帳戶)請登入您的Experience Manager帳戶。

      1. 在您的[!UICONTROL Assets]或[!UICONTROL Collections]檢視中尋找並選取檔案，然後按一下右上角的&#x200B;**[!UICONTROL Select]**。

         <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * 針對GenStudio體驗，請執行以下作業：

      1. 按一下&#x200B;**[!UICONTROL GenStudio Library]**。

      1. (如果您尚未登入您的GenStudio帳戶)請登入您的GenStudio帳戶。

         預設會顯示您的顯示廣告體驗。 視需要選擇性依行銷活動或其他屬性篩選您的體驗。

      1. 找到並選取顯示廣告體驗，然後按一下右上角的&#x200B;**[!UICONTROL Select]**。

     所選體驗中的每個創意變體都將匯入為單獨的HTML5創意內容。

1. 新增或移除創意：

   * 若要新增影像，請按一下左上方的![新增](/help/creative/assets/create.png "新增")，在您的裝置或網路上找到檔案。

   * 若要移除影像，請取消選取影像旁邊的核取方塊。

1. 指定[HTML5創意設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)或[影像創意設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)。

   依預設，會選取您剛才上傳的所有創意內容或GenStudio體驗，而您指定的任何設定會套用至所有已選取的專案。 任何只有一個值的設定會套用至所有選取的專案。 若要輸入特定創意內容或GenStudio體驗的設定，請取消選取每個不適用的創意內容或體驗。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 將協力廠商創意內容新增至創意內容庫 {#creative-add-third-party}

[!DNL Creative]支援大多數協力廠商廣告伺服器上託管的創意內容的JavaScript追蹤標籤。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**。

1. 在[協力廠商創意設定](#creative-settings-third-party)中指定創意的JavaScript標籤和其他設定。

   您可以將任何[可用的巨集](/help/creative/creative-macros.md)複製並貼到JavaScript標籤中。

1. 按一下&#x200B;**[!UICONTROL Create]**

## 將視訊創意內容新增至創意內容庫

檢視[視訊創意規格](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs)和[支援的創意大小](/help/creative/creative-libraries/creative-sizes.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Video]**。

1. 以下列其中一種方式指定視訊檔案：

   * 將裝置或網路上的檔案拖放至方塊中。

   * 按一下&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的裝置或網路上尋找檔案。

1. 指定[視訊創作設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video)。

   預設會選取您剛上傳的創意，而您指定的任何設定會套用至選取的創意。<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. 按一下&#x200B;**[!UICONTROL Create]**

>[!MORELIKETHIS]
>
>* [編輯標準創意](/help/creative/creative-libraries/creative-edit-standard.md)
>* [標準創意設定](/help/creative/creative-libraries/creative-settings-standard.md)
>* [可用於追蹤URL的巨集](/help/creative/creative-macros.md)
>* [支援的創意大小](/help/creative/creative-libraries/creative-sizes.md)
>* [預覽創意](/help/creative/creative-libraries/creative-preview.md)
>* [從組合附加及分離創意](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)
>* [管理創意內容庫](/help/creative/creative-libraries/creative-library-manage.md)
