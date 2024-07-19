---
title: 關於通知
description: 瞭解通知，包括不同的型別和類別。
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 49dc6a4a18966bbf68402d70aec9574ed11e1886
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# 關於通知

*Beta功能*

您可以設定通知設定，以訂閱或取消訂閱不同型別的警示。 您可以透過下列任何方式檢視通知：

* 從[!UICONTROL Notifications]面板（可從位於![通知](/help/search-social-commerce/assets/notifications-panel.png "通知")的主功能表取得）。

* 從[!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta]。

* 從[!UICONTROL Notification Center]網頁應用程式，它會在Search、Social和Commerce以外的個別視窗中開啟[!UICONTROL Notification Center]。

  應用程式的載入速度比一般瀏覽器版本更快，而且會自動更新。 您可以安裝應用程式，並使用瀏覽器的應用程式管理員來管理它。

* 從推播通知到您的瀏覽器。

  啟用推播通知時，會根據瀏覽器的通知慣例顯示。

您可以檢視通知、將通知標示為已讀取或未讀取，以及刪除通知。

## 通知型別

* **[!UICONTROL Notices]**：版本、停機時間和其他變更管理通知。

* **[!UICONTROL Recommendations]**：發現可改善效能、實作最佳實務等機會。

* **[!UICONTROL Warnings]**：需要注意但對最佳化或管理無關緊要的問題。

* **[!UICONTROL Issues]**：需要立即注意的重大問題。 包含帳戶授權錯誤通知。

## 通知類別

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**： [大量工作表作業](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)已完成或失敗的通知。

   * **[!UICONTROL Manager Account Missing]**： Search、Social和Commerce缺少[廣告網路管理員帳戶](/help/search-social-commerce/admin/manager-accounts.md)的認證的通知，這些認證是正確設定重要功能所必需的。

   * **[!UICONTROL UI Actions]**：關於在背景執行的作業已完成或失敗的通知。 工作型別包含[大量工作表工作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)、大量編輯資料表中的工作，或使用工具列、實體指派工作或使用者介面中的其他動作（例如與廣告網路同步、貼上列或重新命名實體）。 實體指派包括指派或取消指派給任何實體的[標籤分類值](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md)、指派行銷活動給投資組合，以及指派或取消指派給投資組合的限制。<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**：用於已關閉的測試版

      * **[!UICONTROL File Upload to Cloud Storage]**：用於已關閉的測試版

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**：通知Search、Social和Commerce無法存取[廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)，因為認證無效或授權權杖無效或過期。

      * **[!UICONTROL Account Missing]**： Search、Social和Commerce缺少[廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)之認證的通知。

      * **[!UICONTROL Manager Account Auth Error]**：通知Search、Social和Commerce無法與[廣告網路管理員帳戶](/help/search-social-commerce/admin/manager-accounts.md)同步，因為認證無效或授權權杖無效或過期。

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**： [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md)已完成或失敗的通知。

   * **[!UICONTROL Custom Alerts]**：已針對警示範本觸發[警示執行個體](/help/search-social-commerce/alerts/alert-about.md)的通知。

   * **[!UICONTROL Reports]**： [自訂或排程報告](/help/search-social-commerce/reports/report-about.md)已完成或失敗的通知。

   * **[!UICONTROL Spreadsheet Feeds]**： [試算表摘要](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)完成或失敗的通知。

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: 

-->

<!--
* [!UICONTROL Portfolio Management]

  * **[!UICONTROL Simulation Report]**: 

-->

<!--
* [!UICONTROL System]

  * **[!UICONTROL Change Management]**: 

-->

>[!MORELIKETHIS]
>
>* [檢視您的通知](notification-view.md)
>* [將通知標示為已讀取或未讀取](notification-mark-read-unread.md)
>* [刪除通知](notification-delete.md)
>* [編輯您的通知設定](notification-edit.md)
>* [啟用和停用來自[!UICONTROL Notification Center]](notifications-push-enable-disable.md)的推播通知
>* [安裝及解除安裝[!UICONTROL Notification Center] Web應用程式](notification-app-install-uninstall.md)
