---
title: （新UI）管理報表範本
description: 瞭解如何建立、檢視、編輯和刪除排程和隨選報告的可重複使用報告範本。
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# （新UI）管理報表範本

報表範本是預先定義的報表版面配置，可在產生大部分報表時重複使用。 如果您想要使用非預設引數、執行相同報表的變數，或根據定期排程執行相同報表，則使用範本可節省您的時間。 已儲存的範本可在&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;的&#x200B;**[!UICONTROL Templates]**&#x200B;索引標籤中使用。

您一次最多可以維護100個範本。

檢視資料需要[!UICONTROL View Scheduled Reports]許可權。 建立、複製、編輯、執行和刪除範本，以及複製資料列資料，需要[!UICONTROL Edit Scheduled Reports]許可權。 您只能編輯您建立的範本。

## 可用動作

* [建立報表範本](#template-create)作為新範本或根據現有範本。

* [檢視報表範本的設定，而不變更原始的](#template-view)。

* [編輯報表範本](#template-edit)，包括其排程。

* [依需求執行指定範本的報告](#template-run)。

* [刪除報表範本](#template-delete)。

* [將選取資料列中的所有資料複製到剪貼簿](#copy-to-clipboard)。

## 建立報表範本 {#template-create}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 執行下列任一項作業：

   * 若要建立新範本，請按一下&#x200B;**[!UICONTROL Create Template]**。 在&#x200B;**[!UICONTROL Create a New Template]**&#x200B;面板中，選取報表類別與報表型別，然後按一下&#x200B;**[!UICONTROL Proceed]**。

   * 若要根據現有的範本建立範本，請將游標停留在範本列上，然後按一下![範本設定](/help/search-social-commerce/assets/settings-new.png "範本設定") **[!UICONTROL Template Settings]**&#x200B;或&#x200B;**[!UICONTROL ...]>[!UICONTROL Duplicate]**。

1. 輸入範本的唯一&#x200B;**[!UICONTROL Report Name]**，並確認已啟用&#x200B;**[!UICONTROL Save as Template]**。

   以&#x200B;**[!UICONTROL Create Template]**&#x200B;開頭時，預設會啟用此設定。 如果停用，最終動作會變更為&#x200B;**[!UICONTROL Run Report]**，這會產生報表而非儲存範本。

1. 設定[基本與進階報告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)、[協助報告](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md)、[模型正確性報告](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md)或[專業報告](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md)的報告設定。

   按一下&#x200B;**[!UICONTROL Next]**&#x200B;在設定區段之間移動。

1. （選擇性）若要自動產生報表，請在&#x200B;**[!UICONTROL Scheduling]**&#x200B;中設定&#x200B;**[!UICONTROL Frequency]**&#x200B;和傳遞設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

您也可以在從[最新報告]索引標籤[&#128279;](/help/search-social-commerce/new-ui/reports/management/report-manage.md)建立報告時儲存範本，方法是在提交報告設定之前啟用&#x200B;**[!UICONTROL Save as Template]**。

## 檢視報表範本的設定 {#template-view}

若要在不變更原始範本的情況下檢查設定，請開啟重複專案。 這需要[!UICONTROL Edit Scheduled Reports]許可權。 開啟復本不會儲存新範本。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 將游標停留在範本列上，然後按一下![範本設定](/help/search-social-commerce/assets/settings-new.png "範本設定") **[!UICONTROL Template Settings]**。

1. 檢閱報表設定。

1. 完成後，請按一下「**[!UICONTROL Cancel]**」。 如果系統提示您放棄安裝，請按一下&#x200B;**[!UICONTROL Discard]**。

若要儲存副本，請依照[範本建立程式](#template-create)操作。

## 編輯報表範本 {#template-edit}

您可以變更您建立的任何範本的設定和排程。 變更會套用至日後從範本產生的報表。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 選取您所建立之範本旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

   選取多個範本或選取的範本是由其他使用者建立時，[!UICONTROL Edit]無法使用。

1. 變更報表設定。 若要新增、變更或移除排程，請在&#x200B;**[!UICONTROL Scheduling]**&#x200B;中編輯&#x200B;**[!UICONTROL Frequency]**。

   選取排程報告的每日、每週或每月頻率。 若要移除週期性排程，請選取&#x200B;**[!UICONTROL Now]**。

   編輯現有範本時，**[!UICONTROL Save as Template]**&#x200B;和&#x200B;**[!UICONTROL Type]**&#x200B;為唯讀。 您不需要再次啟用[!UICONTROL Save as Template]。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 依需求執行指定樣版的報表 {#template-run}

您可以隨時執行一或多個範本的報告。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 執行下列任一項作業：

   * （若要執行單一範本）：

     1. 開啟範本列的功能表並選取&#x200B;**[!UICONTROL Run]**。

     1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

   * （若要執行一或多個範本）：

     1. 選取每個要執行的範本旁的核取方塊。

     1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Run]**。

     1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

您也可以在編輯範本時按一下&#x200B;**[!UICONTROL Run Report]**，然後再按&#x200B;**[!UICONTROL Confirm]**，以執行範本。 請先儲存任何變更；此動作會執行儲存的範本。

## 刪除報表範本 {#template-delete}

您可以刪除任何可用的報表範本。 當您刪除包含排程的範本時，未來不會產生該報表。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 按一下「**[!UICONTROL Templates]**」標籤。

1. 執行下列任一項作業：

   * （若要刪除單一範本）：

     1. 開啟範本列的功能表並選取&#x200B;**[!UICONTROL Delete]**。

     1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

   * （若要刪除一或多個範本）：

     1. 選取要刪除的每個範本旁的核取方塊。

     1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

     1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。
