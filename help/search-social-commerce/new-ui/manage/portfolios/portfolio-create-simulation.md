---
title: 從[!UICONTROL Portfolios]檢視執行並下載模擬
description: 瞭解如何執行自訂模擬，以及從「產品組合」檢視下載每週模擬。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# 從[!UICONTROL Portfolios]檢視執行並下載模擬

*Beta功能*

您可以針對單一[最佳化或作用中](portfolio-about.md#portfolio-status)產品組合執行自訂模擬，並從[!UICONTROL Portfolios]檢視下載最多100個產品組合的每週自動模擬。

執行自訂模擬需要[!UICONTROL Create Simulation]許可權。 下載每週模擬需要[!UICONTROL View Simulation]許可權。

>[!NOTE]
>
>您也可以[從[!UICONTROL Simulations]檢視](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)建立或重新執行自訂模擬。

## 執行自訂模擬 {#run-simulation}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 執行下列任一項作業：

   * 將游標停留在投資組合列上。 在投資組合名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**」。

   * 選取投資組合旁的核取方塊。 在大量動作工具列中，按一下&#x200B;**[!UICONTROL More]>[!UICONTROL Run Simulation]**。

1. 指定[自訂模擬設定](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md#custom-simulation-settings)：

   1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;索引標籤上，輸入唯一的&#x200B;**[!UICONTROL Simulation Name]**&#x200B;並根據需要變更基本引數。

   1. （選用）在&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;標籤上，變更進階引數。

   所選投資組合的目前設定會用作預設值。 變更模擬設定不會變更投資組合的設定。

1. 按一下&#x200B;**[!UICONTROL Next]**。

1. 檢閱設定，並視需要進行變更。

1. 按一下&#x200B;**[!UICONTROL Submit & Run]**。

已提交要求，並開啟[!UICONTROL Simulations]檢視。 模擬成功完成之後，您可以[下載模擬](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)。

## 下載每週模擬 {#download-simulations}

您可以一次下載一個執行日期的每週模擬，做為[!DNL Microsoft Excel]活頁簿（XLSX檔案）。 僅包含有效及最佳化的產品組合，以及該日期的可用模擬報告。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 選取您要下載其每週模擬的每個投資組合旁的核取方塊。 最多選取100個投資組合。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL More]>[!UICONTROL Download Simulation]**。

1. 在&#x200B;**[!UICONTROL Weekly Simulation]**&#x200B;中，選取執行日期。

   依預設，會選取最近可用的日期。 如果某些選取的投資組合無法提供報表，對話方塊會顯示將排除的投資組合數量。 視需要選取其他日期。 當所選投資組合中沒有該日期的可用模擬時，您無法下載報表。

1. 按一下「下載」按鈕，其標籤包含具有可用報表的產品組合數目（例如，**[!UICONTROL Download 2 portfolios]**）。

   檔案會依照瀏覽器的正常程式下載。 完成訊息會指出包含的投資組合數量。

若要下載自訂模擬或選取個別的每週模擬，請使用[[!UICONTROL Simulations]檢視](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)。

>[!MORELIKETHIS]
>
>* [（新使用者介面）檢視投資組合效能詳細資料](portfolio-details.md)
>* [關於投資組合](portfolio-about.md)
>* [執行或重新執行自訂模擬](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [下載模擬](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
