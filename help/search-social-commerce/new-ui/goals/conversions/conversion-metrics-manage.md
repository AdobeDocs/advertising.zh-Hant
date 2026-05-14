---
title: 管理廣告商的轉換量度
description: 瞭解如何將Adobe Advertising追蹤的轉換量度用於廣告商。
feature: Conversions
source-git-commit: 3272a0d3e5766a22c2ff761b84f1774cafe153bd
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 0%

---

# （新UI）管理和檢視廣告商轉換量度的績效資料

*Beta功能*

廣告商的[轉換](/help/search-social-commerce/glossary.md#c-d)量度在整個Adobe Advertising中使用：

* 在「搜尋」、「社交」和「Commerce」中，轉換量度的資料可顯示在行銷活動、投資組合和目標管理檢視及報表中的欄中。 具有足夠存取許可權的使用者也可以使用轉換量度來建立目標，這些目標是用來最佳化產品組合。

* （使用Advertising DSP的廣告商）在DSP中，您可以在行銷活動管理檢視、自訂目標和自訂報表中包含轉換量度。 您也可以使用轉換量度來建立[自訂目標](/help/dsp/admin/custom-objectives-manage.md)，這些目標用於最佳化封裝。

可用的量度包括：

* Adobe Advertising追蹤廣告商的轉換量度。

* [從Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md)同步的轉換和網站參與量度。

* [網站事件已從Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md)同步。

* 由[!DNL Google Ads]追蹤的轉換，以及由[!DNL Microsoft Advertising]通用事件追蹤標籤追蹤的轉換。

* （當[您已設定特定 [!DNL Google Analytics] 帳戶、屬性和檢視組合作為搜尋、社交和Commerce的資料來源](/help/search-social-commerce/admin/data-sources/data-source-about.md)時） [!DNL Google Analytics]所追蹤的轉換。

* 來自自訂摘要的轉換。

從可用的轉換量度清單中，有權存取廣告商資料的每位使用者都可以自訂他們看到的可用於管理檢視和報表的量度，包括或省略他們選擇的特定量度。 您可以使用與擷取資料中拼字完全相同的量度名稱，或是變更欄標題中所顯示的名稱，以提高可讀性。

>[!IMPORTANT]
>
>依預設，廣告商的轉換量度（除了[!DNL Google Ads]、[!DNL Google Analytics]和[!DNL Microsoft Advertising]通用事件追蹤標籤所追蹤的轉換之外）無法納入行銷活動和產品組合管理檢視、目標和報告中。 若要讓轉換量度可供使用，您必須明確提供該量度。
>
>由[!DNL Google Ads]、[!DNL Google Analytics]和[!DNL Microsoft Advertising]通用事件追蹤標籤追蹤的新轉換一律會自動提供。

>[!TIP]
>
>當廣告商（或廣告網路）停止收集轉換量度後，[在管理檢視和報告中隱藏它](#conversion-metrics-change-available)，除非您想要用它來檢視歷史資料。

## 檢視為廣告商追蹤的轉換量度

* 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

會列出為廣告商收集的所有轉換量度，以及指派給他們的任何不同顯示名稱。 每個量度列都包含量度的來源。

## 變更轉換量度的顯示名稱

例如，如果您使用名為&#x200B;*reg*&#x200B;的轉換量度來收集註冊資料，那麼您可以選擇變更顯示名稱，使其顯示為「註冊」。

您無法刪除現有的顯示名稱。

>[!NOTE]
>
>對於來自 [!DNL Google Analytics][&#128279;](/help/search-social-commerce/admin/data-sources/data-source-about.md)的量度，如果您更新或重新驗證整合，則會覆寫對顯示名稱所做的任何手動變更。 同樣地，除非您[更新](/help/search-social-commerce/admin/data-sources/data-source-edit.md)或[重新驗證](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md)整合，否則會忽略[!DNL Google Analytics]內的任何名稱變更。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

1. 從工具列[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[欄標題](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)篩選清單。

1. 在度量的&#x200B;**[!UICONTROL Conversion Display Name]**&#x200B;欄中，將游標放在度量名稱上，然後按一下&#x200B;**...** > **[!UICONTROL Rename]**。

1. 輸入應顯示的名稱，然後按一下&#x200B;**[!UICONTROL Apply]**。

   顯示名稱必須是唯一的，而且不能包括下列特殊字元： `\"<'>&`

## 變更管理檢視、目標和報告中可用的轉換量度 {#conversion-metrics-change-available}

>[!NOTE]
>
>當您隱藏先前可用的轉換量度時，該量度會從任何包含該轉換量度的衍生量度中移除。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

   已針對廣告商收集的所有轉換量度，以及已針對顯示指定的任何不同名稱都會列示。

1. （選擇性）從工具列[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[欄標題](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)篩選清單。

1. 變更管理檢視和報告可用的轉換量度：

   * 若要顯示或隱藏單一量度，請按一下&#x200B;**[!UICONTROL Visibility]**&#x200B;欄中的切換以變更設定。

   * 若要顯示或隱藏多個量度，請執行下列動作：

      1. 選取每個轉換量度旁的核取方塊。

         如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

      1. 在大量動作工具列中，按一下![可見度](/help/search-social-commerce/assets/visible.png "可見度")以顯示度量，或按一下![可見度關閉](/help/search-social-commerce/assets/visibility-off.png "可見度關閉")隱藏度量。

      1. （若要隱藏量度）在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**&#x200B;以隱藏量度，包括從包含量度的任何衍生量度中移除量度。

## 管理轉換的效能資料報表

您可以下載下列有關追蹤的轉換的資訊：同步的量度名稱，「搜尋」、「社交」和「Commerce」管理檢視與報表中量度的顯示名稱，量度是否顯示在管理檢視與報表中，轉換ID以及量度來源。 將資料下載至[!DNL Microsoft Excel]活頁簿（XLSX檔案）格式的檔案。

### 產生含有已篩選資料列的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

1. 指定要下載其資料的轉換：

   * 若要下載特定列的資料，請選取列旁的核取方塊。

   * 若要下載所有列的資料，您不需要選取任何核取方塊。 預設會包含所有列。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]設定中，輸入唯一的報告名稱，然後按一下&#x200B;**[!UICONTROL Generate]**。

   依預設，該檔案的名稱為「conversionsReport_YYYYYMMDD_NNNN」，其中「NNNN」為循序工作編號（例如「conversionsReport_20260402_1326）。

   檔案已新增至[!UICONTROL Recently Generated]清單。

1. （選擇性）若要在檔案完成後下載檔案，請按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 下載完成的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 刪除已完成的報告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

1. 在資料表上方的工具列中，按一下![下載](/help/search-social-commerce/assets/download.png "下載") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![刪除](/help/search-social-commerce/assets/delete-new.png "刪除")。

<!--
>[!MORELIKETHIS]
>
>* 
-->
