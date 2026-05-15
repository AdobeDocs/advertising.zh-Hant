---
title: 執行或重新執行自訂模擬
description: 瞭解如何執行或重新執行投資組合的自訂模擬。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: d8170c2bbeab003339472d03033f1741014d6c4b
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 0%

---

# 執行或重新執行自訂模擬

*Beta功能*

您可以產生[最佳化或作用中](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)投資組合的自訂模擬。 您也可以變更現有模擬的引數並重新產生模擬，或使用現有引數重新執行現有模擬。

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin]和[!UICONTROL Account Manager]使用者可以看到其他使用者建立的模擬。 所有其他使用者只能看到他們建立的自訂模擬。

## 建立新的模擬

1. 執行下列任一項作業：

* 從[!UICONTROL Simulations]檢視：

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

   1. 按一下資料表上方的&#x200B;**[!UICONTROL Run Simulation]**。

   1. 選取投資組合：

      1. 按一下&#x200B;**[!UICONTROL Select Portfolio]**。

      1. 選取投資組合。

         若要搜尋包含特定文字字串的產品組合，請開始在搜尋欄位中輸入文字字串。 值不區分大小寫。

      1. 按一下&#x200B;**[!UICONTROL Proceed]**。

* 從[!UICONTROL Portfolios]檢視：

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

   1. 執行下列任一項作業：

      * 將游標停留在投資組合列上。 在投資組合名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**」。

      * 選取投資組合旁的核取方塊。 在大量動作工具列中按一下&#x200B;**[!UICONTROL Run Simulation]**。

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

當模擬報告可用時，您和任何其他指定的電子郵件收件者會收到通知，其中包含下載資料的ZIP檔案(包含一個活頁簿（XLSX檔案）連結。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 使用現有設定重新執行模擬

您可以重新執行目前未排入佇列的模擬。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 選取您要重新執行的模擬旁的核取方塊。

1. 在資料表上方的工具列中，按一下![重新執行](/help/search-social-commerce/assets/rerun.png "重新執行")。

## 編輯現有模擬的設定並重新執行

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 選取要再生的模擬旁的核取方塊。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Run Simulation]**。

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

當模擬報告可用時，您和任何其他指定的電子郵件收件者會收到通知，其中包含下載資料的ZIP檔案(包含一個活頁簿（XLSX檔案）連結。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 自訂模擬設定 {#custom-simulation-settings}

如需自訂模擬設定的詳細資訊，請參閱最佳化指南，此指南可在Search、Social和Commerce中取得。

>[!MORELIKETHIS]
>
>* [關於模擬](simulation-about.md)
>* [檢視模擬詳細資料](simulation-view.md)
>* [下載模擬](simulation-download.md)
