---
title: 將標準創意內容新增至創意內容庫
description: 瞭解如何將標準（非動態）創意內容新增至創意內容庫。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: d68c8c31a047c4615224e9ab19654e56b5e8c8f9
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# 將標準創意內容新增至創意內容庫

*已關閉的Beta*

將創意內容新增至您的[創意資料庫](creative-library-manage.md)，以搭配[廣告體驗](/help/creative/experiences/experience-about.md)使用。

>[!NOTE]
>
> 您可以直接在廣告體驗中加入沒有定義使用者目標的個別創意內容。 您也可以將創意內容分組到[組合](bundle-manage.md)中，將其包含在鎖定目標的廣告體驗中。

## 將彈性的HTML廣告新增至創意內容庫 {#flexible-creative-add}

<!-- Later:
You can do either of the following: 

* Upload your own flexible creatives in ZIP files.

* Use any of the predefined flexible creative templates as a starting point for your own flexible creative.

### Upload your own flexible creatives {#flexible-creative-upload}

-->

您可以上傳多個彈性的創意單位。 彈性的創意內容必須採用ZIP格式，最大可達2 MB。 如需檔案需求，請參閱[HTML5創意規格](html5-creative-specification.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子標籤。

1. 按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**。

1. 按一下&#x200B;**[!UICONTROL Upload New]**。

1. 以下列任一方式指定ZIP檔案：

   * 將裝置或網路上的檔案拖放至方塊中。

   * 按一下&#x200B;**[!UICONTROL select a file]**&#x200B;以找出裝置或網路上的檔案。

   檢視[彈性廣告規格](#flexible-ad-spec)。

1. 新增或移除彈性的創意檔案：

   * 若要新增檔案，請按一下左上方的![新增](/help/creative/assets/create.png "新增")，然後在您的裝置或網路上找到檔案。

   * 若要移除檔案，請取消選取檔案旁邊的核取方塊。

1. 指定[彈性的HTML5廣告設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)。

   依預設，會選取您剛上傳的所有創意內容。 任何只有一個值的設定皆適用於所有選取的創意；對於某些設定，您可以指定個別值。 若要輸入特定創意的設定，請取消選取每個不適用創意旁的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Create]**

<!-- In a later phase:

### Add flexible creatives using a template {#flexible-creative-use-template}

You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads. Once you select a template to use, you'll edit the click tags and attributes.<!-- Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).>

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click the **[!UICONTROL Standard Ads]** subtab.

1. Click **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Click **[!UICONTROL Browse System Flexible Templates]**.



[The following are old instructions; see how this works in the new UI]


1. In the left panel, select the creative size to see all available templates for that size.

1. Under the template name, click **[!UICONTROL Use This Creative]**.

1. Edit the [flexible HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) to include your own click tags, images, and other attributes.

   The maximum file size of the creative, once it's zipped, is 2 MB.[Will saving the creative zip it??]

1. (Optional) Once you've made your changes, click []()[add image] to preview the new creative. 

1. Click **[!UICONTROL Save]**.

-->

## 將HTML5創意內容新增至創意內容庫

您可以一次新增單一型別的多個HTML5創意（簡單或靜態）。

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>您也可以[新增彈性的HTML5創意](#flexible-creative-add)，這些創意是HTML5創意，具有作為標準HTML標籤的所有屬性，您可以直接在[!DNL Creative]中編輯。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子標籤。

1. 按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL HTML5]**。

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. 以下列其中一種方式指定檔案：

   * 將裝置或網路上的檔案拖放至方塊中。

   * 按一下&#x200B;**[!UICONTROL select a file]**&#x200B;在您的裝置或網路上尋找檔案。

   請參閱[HTML5廣告規格](/help/creative/creative-libraries/html5-creative-specification.md)。

1. 指定[HTML5廣告設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)。

依預設，會選取您剛上傳的所有創意內容。 任何只有一個值的設定皆適用於所有選取的創意；對於某些設定，您可以指定個別值。 若要輸入特定創意的設定，請取消選取每個不適用創意旁的核取方塊。

1. 按一下&#x200B;**[!UICONTROL Create]**

## 將影像創意內容新增至創意內容庫

影像創意內容可以是GIF、JPEG、JPG或PNG格式。 檔案大小上限為兩(2) MB。 檢視[支援的創意大小](/help/creative/creative-libraries/creative-sizes.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子標籤。

1. 按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Image]**。

1. 指定影像：

   * 針對本機影像資產，請執行下列其中一項作業：

      * 將裝置或網路上的檔案拖放至方塊中。

      * 按一下&#x200B;**[!UICONTROL select a file]**&#x200B;在您的裝置或網路上尋找檔案。

   * 針對Adobe Experience Manager資料庫中的影像，請執行下列動作：

      1. 按一下&#x200B;**[!UICONTROL AEM Asset Library]**。

      1. 登入您的Experience Manager帳戶。

      1. 在您的[!UICONTROL Assets]或[!UICONTROL Collections]檢視中尋找並選取檔案，然後按一下右上角的&#x200B;**[!UICONTROL Select]**。

1. 新增或移除影像：

   * 若要新增影像，請按一下左上方的![新增](/help/creative/assets/create.png "新增")，在您的裝置或網路上找到檔案。

   * 若要移除影像，請取消選取影像旁邊的核取方塊。

1. 指定[影像創意設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)。

   依預設，會選取您剛上傳的所有創意內容，而您指定的任何設定會套用至所有選取的創意內容。 任何只有一個值的設定皆適用於所有選取的創意。 若要輸入特定創意的設定，請取消選取每個不適用的創意內容。

1. 按一下&#x200B;**[!UICONTROL Create]**

## 將協力廠商創意內容新增至創意內容庫 {#creative-add-third-party}

[!DNL Creative]支援大多數協力廠商廣告伺服器上託管的創意內容的JavaScript追蹤標籤。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 按一下程式庫名稱。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子標籤。

1. 按一下&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL 3rd Party]**。

1. 在[協力廠商創意設定](#creative-settings-third-party)中指定創意的JavaScript標籤和其他設定。

   您可以將任何[可用的巨集](/help/creative/creative-macros.md)複製並貼到JavaScript標籤中。

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
