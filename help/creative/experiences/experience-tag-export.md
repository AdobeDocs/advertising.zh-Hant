---
title: 匯出並實作即時體驗的廣告體驗標籤
description: 瞭解如何匯出廣告體驗標籤並可選擇上傳至Advertising DSP行銷活動。
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: f2bf245c13244cbcb76cead8b37f149b9b9bc24f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 匯出並實作即時體驗的廣告體驗標籤

*已關閉的Beta*

特定創意大小的廣告標籤可用於[即時](experience-about.md#experience-statuses)體驗後，您就可以在JavaScript和iframe格式中產生並複製該標籤，以在Advertising DSP或其他DSP上實作。 DSP的標籤包含DSP所需的所有巨集。

使用Advertising DSP的廣告商可選擇直接將標籤上傳至Advertising DSP行銷活動，作為廣告型別為「標準顯示」的廣告。

>[!NOTE]
>
>* 當您使用決策樹目標定位建立體驗時，[!DNL Creative]會自動為每個適用的創意大小建立廣告標籤。
>* 當您建立沒有決策樹定位的體驗時，您必須針對每個適用的創意大小[手動建立廣告標籤](experience-tag-create-manually.md)。
>* 體驗標籤是動態的。 如果您編輯體驗，則不需要更新標籤。
>* 請確定您將在其中實作廣告體驗的行銷活動包含與體驗相容的目標定位。 階層式鎖定目標行為可能因DSP而異。 在Advertising DSP中，廣告層級鎖定目標會套用在（而非）位置層級鎖定目標上方。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 執行下列任一項作業：<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * 在卡片檢視中，按一下體驗名稱旁的&#x200B;**[!UICONTROL ...]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格檢視中，將游標停留在資料列上，按一下&#x200B;**[!UICONTROL More]**，然後按一下&#x200B;**[!UICONTROL Tag Manager]**

1. 將游標停留在適用廣告標籤的列上，然後按一下![匯出廣告標籤](/help/creative/assets/export.png "匯出廣告標籤") **[!UICONTROL Export ad tags]**&#x200B;或&#x200B;**[!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]**。

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. （選擇性）在[!UICONTROL Macros]標籤上，指定最多五個要包含在標籤中的自訂巨集。 對於要包含的每個巨集：

   1. 選取核取方塊。<!-- Explain more -->

   1. 輸入自訂巨集。<!-- Explain more -->

1. 按一下右上角的&#x200B;**[!UICONTROL Next]**&#x200B;或按一下左側功能表中的&#x200B;**[!UICONTROL Generate ad tags]**。

1. 選取標籤型別： ** *JavaScript<!-- sic -->* **或** *IFRAME* ** <!-- sic -->。

1. 在[!UICONTROL Destinations]清單中，選取您將為體驗建立廣告的位置。

   * *一般：*&#x200B;對於您將在其他DSP中建立的廣告。 **注意：**&#x200B;您可能需要視需要手動加入[額外的巨集](/help/creative/creative-macros.md)。

   * *Adobe AdCloud：*&#x200B;針對您將在Advertising DSP中建立的廣告。

   * *Google CM360：*&#x200B;針對您將在[!DNL Google Campaign Manager 360]中建立的廣告。 **注意：**&#x200B;您可能需要視需要手動加入[額外的巨集](/help/creative/creative-macros.md)。

1. 按一下&#x200B;**[!UICONTROL Generate tags]**。

1. 複製或下載標籤：

   * 若要複製單一廣告大小的標籤，請展開標籤列，將游標停留在列上，然後按一下![複製](/help/creative/assets/copy.png "複製") **[!UICONTROL Copy]**。<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * 若要以檔案形式將所有產生的標籤下載至瀏覽器的預設下載位置，請按一下![下載標籤](/help/creative/assets/download.png "下載標籤")。

   您可以在文字編輯器中開啟檔案，以複製每個標籤。 對於JavaScript標籤，標籤包含在`<script></script>`和`<noscript></noscript>`標籤中。 若為iframe標籤，該標籤會包含在`<iframe></iframe>`標籤中。

1. 實施相關DSP的標籤：

   * 針對Advertising DSP以外的DSP，請為將在DSP中建立廣告的使用者提供標籤。

   * 若為Advertising DSP：

      1. 按一下右上角的&#x200B;**[!UICONTROL Next]**&#x200B;或按一下左側功能表中的&#x200B;**[!UICONTROL DSP link]**。

      1. 選取您要上傳廣告標籤的行銷活動。

      1. 按一下&#x200B;**[!UICONTROL Assign Tags]**。

         針對選取的行銷活動，DSP會開啟至[!UICONTROL Ads]檢視。

      1. 在[!UICONTROL Create ads]檢視中，檢閱廣告標籤，選取您要建立廣告的每個標籤，然後按一下&#x200B;**[!UICONTROL Create]**。


<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [手動建立適用創意大小的廣告標籤](experience-tag-create-manually.md)
>* [將創意內容指派給體驗的廣告標籤，而不需鎖定目標](experience-tag-assign-creatives.md)
>* [重新命名廣告標籤](experience-tag-rename.md)
