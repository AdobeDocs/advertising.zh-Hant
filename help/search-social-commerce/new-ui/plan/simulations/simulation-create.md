---
title: 執行或重新執行自訂模擬
description: 瞭解如何執行或重新執行投資組合的自訂模擬。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
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
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%
---
# 執行或重新執行自訂模擬

*Beta功能*

您可以產生[最佳化或作用中](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status)投資組合的自訂模擬。 您也可以在清單中選取模擬，以針對相同的投資組合執行新的模擬，或使用現有的設定重新執行模擬。

建立自訂模擬需要[!UICONTROL Create Simulation]許可權。 選取投資組合需要[!UICONTROL View Portfolios]許可權。

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin]和[!UICONTROL Account Manager]使用者可以看到其他使用者建立的模擬。 所有其他使用者只能看到他們建立的自訂模擬。

## 建立新的模擬 {#simulation-create}

您可以從[!UICONTROL Simulations]檢視開始，或從[!UICONTROL Portfolios]檢視](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation)執行[自訂模擬。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 清除所有選取的模擬列，然後按一下&#x200B;**[!UICONTROL Run Simulation]**。

1. 選取投資組合：

   1. 按一下&#x200B;**[!UICONTROL Select Portfolio]**。

   1. 選取投資組合。

      若要搜尋包含特定文字字串的產品組合，請開始在搜尋欄位中輸入文字字串。 值不區分大小寫。

   1. 按一下&#x200B;**[!UICONTROL Proceed]**。

1. 指定[自訂模擬設定](#custom-simulation-settings)：

   1. （選擇性）若要變更用於模擬的投資組合，請按一下投資組合名稱旁的&#x200B;**[!UICONTROL Change Portfolio]**、選取投資組合，然後按一下&#x200B;**[!UICONTROL Proceed]**。

   1. 在[!UICONTROL Basic Settings]索引標籤上：

      1. 輸入唯一的&#x200B;**[!UICONTROL Simulation Name]**。

      1. （選用）變更模擬的基本引數。

   1. （選擇性）在[!UICONTROL Advanced Settings]標籤上，變更模擬的進階引數。

   依預設會指定所選投資組合的現有引數。 變更值將顯示不同引數產生的結果，而不會變更投資組合的現有引數。

1. 按一下&#x200B;**[!UICONTROL Next]**。

1. 檢閱設定，並視需要編輯設定。

1. 按一下&#x200B;**[!UICONTROL Submit & Run]**。

已提交要求，並開啟[!UICONTROL Simulations]檢視。 當模擬報告可用時，您和任何其他指定的電子郵件收件者都會收到附有下載連結的通知。 您也可以[從[!UICONTROL Simulations]檢視](simulation-download.md)下載模擬。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 使用現有設定重新執行模擬 {#rerun-a-simulation-with-the-existing-settings}

您可以使用現有的設定，一次最多可重新執行10個模擬。 無法重新執行狀態為[!UICONTROL Queued]或[!UICONTROL In Progress]的模擬。 如果您的選取範圍包括這些模擬，則會略過這些模擬，而會提交其餘的模擬。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 選取您要重新執行的模擬旁的核取方塊。

1. 在資料表上方的工具列或大量動作工具列中，按一下&#x200B;**[!UICONTROL Re-Run Simulation]**。

請求已提交，且檢視會重新整理。

## 對清單中的投資組合執行新的模擬 {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

在您按一下[!UICONTROL Run Simulation]之前選取模擬，會選取其投資組合以進行新的模擬。 表單使用投資組合的目前設定，而不是所選模擬的設定。 此動作不會編輯現有的模擬。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 選取您要使用之投資組合的模擬旁的核取方塊。

   如果您選取多個模擬，它們都必須使用相同的投資組合。 產品組合必須為作用中或最佳化。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Run Simulation]**。

1. 指定[自訂模擬設定](#custom-simulation-settings)，包括唯一的&#x200B;**[!UICONTROL Simulation Name]**。 視需要變更&#x200B;**[!UICONTROL Basic Settings]**&#x200B;和&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;標籤上的引數。

1. 按一下&#x200B;**[!UICONTROL Next]**。

1. 檢閱設定，並視需要編輯設定。

1. 按一下&#x200B;**[!UICONTROL Submit & Run]**。

已提交要求，並開啟[!UICONTROL Simulations]檢視。 模擬成功完成之後，您可以[下載模擬](simulation-download.md)。

## 自訂模擬設定 {#custom-simulation-settings}

如需自訂模擬設定的詳細資訊，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。

>[!MORELIKETHIS]
>
>* [關於模擬](simulation-about.md)
>* [檢視模擬詳細資料](simulation-view.md)
>* [下載模擬](simulation-download.md)
