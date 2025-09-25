---
title: 管理動態廣告範本
description: 瞭解xxxx。
feature: Creative Templates
source-git-commit: ed0fe4849c1db933f1c68a49fc848acd7c74af5b
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# 管理動態廣告範本

上傳具有所需廣告格式的壓縮HTML5檔案，為每個廣告型別(靜態HTML5或動態HTML5)和廣告大小的組合建立個別的廣告範本。 對於動態HTML5廣告，您也可以上傳包含廣告屬性<!-- more clarification? -->的檔案。

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## 建立動態廣告範本

>[!NOTE]
>
>當您[新增動態創意內容至創意內容庫](/help/creative/creative-libraries/creative-add-dynamic.md)時，您也可以上傳動態廣告範本。 您在此處建立的任何廣告範本都可以在[!UICONTROL Ad Templates]檢視中使用，以供日後使用。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Create Ad Template]**

1. 指定[廣告範本設定](#ad-template-settings)

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 編輯動態廣告範本

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 將游標停留在廣告範本列上，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[廣告範本設定](#ad-template-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 下載動態廣告範本

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 將游標停留在廣告範本列上，然後按一下&#x200B;**[!UICONTROL Download]**。

   檔案會依照瀏覽器的正常程式下載。

## 刪除動態廣告範本

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 將游標停留在廣告範本列上，然後按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Delete]**.<!-- Confirm -->

## 從廣告範本建立動態廣告

>[!NOTE]
>
>您也可以[將動態創意內容新增至創意資源庫](/help/creative/creative-libraries/creative-add-dynamic.md) （從創意資源庫）。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 將游標停留在廣告範本列上，然後按一下&#x200B;**[!UICONTROL Create Dynamic Ad]**。

   在[!UICONTROL New Dynamic Ad]畫面中，[!UICONTROL Ad Template Size]、[!UICONTROL Ad Template Type]及[!UICONTROL Ad Template]欄位會自動選取且為唯讀。

1. 指定動態廣告設定以[建立動態廣告](/help/creative/creative-libraries/creative-add-dynamic.md)。

## 廣告範本設定 {#ad-template-settings}

### 廣告範本詳細資料

**[!UICONTROL Advertiser]**： （現有範本為唯讀）將為其產生廣告的廣告商。

**[!UICONTROL Ad Template Name]**：廣告商的唯一廣告範本名稱。

**[!UICONTROL Ad Template Type]**： （現有範本為唯讀）廣告範本格式： *靜態HTML5*&#x200B;或&#x200B;*動態HTML5*。

**[!UICONTROL Ad Template Size]**： （現有範本為唯讀）範本建立的廣告維度。

**[!UICONTROL Description]**： （選用）對使用廣告範本的任何人有用的資訊。

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### HTML5 zip

具有所需廣告格式的壓縮HTML5檔案。 如果您已上傳檔案，則會列出檔案名稱。

請參閱[HTML5創意規格](/help/creative/creative-libraries/html5-creative-specification.md)。

若要上傳檔案：

1. 按一下&#x200B;**[!UICONTROL Upload HTML5 zip]**。

1. 在您的裝置或網路上尋找檔案。

### (動態HTML5廣告範本)屬性檔案

<!-- EXPLAIN -->包含廣告範本屬性的檔案。 如果您已上傳檔案，則會列出檔案名稱。

<!-- Add specs for this file type -->

若要上傳檔案：

1. 按一下&#x200B;**[!UICONTROL Upload Attributes File]**。

1. 在您的裝置或網路上尋找檔案。

>[!MORELIKETHIS]
>
>* [動態廣告的工作流程](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理資產檔案](/help/creative/feeds/asset-manage.md)
>* [管理摘要範本](/help/creative/feeds/feed-template-manage.md)
>* [管理目錄](/help/creative/feeds/catalog-manage.md)
>* [將動態創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-dynamic.md)

