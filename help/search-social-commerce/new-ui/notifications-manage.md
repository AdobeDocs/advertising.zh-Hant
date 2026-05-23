---
title: （新UI）管理通知
description: 瞭解如何檢視、設定和管理搜尋、社交和Commerce通知，包括推播通知和通知中心Web應用程式。
feature: Search Notifications
source-git-commit: 000ed245b2ea3381e4ca8fcbdd2d6075d50f4b09
workflow-type: tm+mt
source-wordcount: '1710'
ht-degree: 0%

---

# （新UI）管理通知

*Beta功能*

您可以設定通知設定，以訂閱或取消訂閱不同型別的警示。 您可以透過下列任何方式檢視通知：

* 從[!UICONTROL Notifications]面板（可在右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")取得）。 您可以從面板篩選清單、編輯通知設定或開啟[!UICONTROL Notification Center]。

* 從[!UICONTROL Notification Center] （在Search、Social和Commerce以外的個別視窗中開啟）。 若要從[!UICONTROL Notifications]面板開啟[!UICONTROL Notification Center]，請按一下&#x200B;**[!UICONTROL View All]**。

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

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**： [大量工作表作業](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)已完成或失敗的通知。<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]**： Search、Social和Commerce遺失[廣告網路管理員帳戶](/help/search-social-commerce/admin/manager-accounts.md)之認證的通知，這些是正確設定重要功能所需的認證。<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]**：關於在背景執行的作業已完成或失敗的通知。 工作型別包含[大量工作表工作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->、大量編輯資料表中的工作，或使用工具列、實體指派工作或使用者介面中的其他動作（例如與廣告網路同步、貼上列或重新命名實體）。 實體指派包括指派或取消指派給任何實體的[標籤分類值](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)、指派行銷活動給投資組合，以及指派或取消指派給投資組合的限制。

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**：通知已透過[手動帳戶資料上傳](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md)上傳帳戶資料檔案，或帳戶資料上傳失敗。<!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]**：通知已透過[帳戶資料上傳至 [!DNL Amazon] [!DNL S3]儲存貯體](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md)上傳帳戶資料檔案，或帳戶資料上傳失敗。<!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**：通知Search、Social和Commerce無法存取[廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，因為認證無效或授權權杖無效或過期。

      * **[!UICONTROL Account Missing]**： Search、Social和Commerce缺少[廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)之認證的通知。

      * **[!UICONTROL Manager Account Auth Error]**：通知Search、Social和Commerce無法與[廣告網路管理員帳戶](/help/search-social-commerce/admin/manager-accounts.md)同步，因為認證無效或授權權杖無效或過期。<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**： [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md)已完成或失敗的通知。

   * **[!UICONTROL Custom Alerts]**：已針對警示範本觸發[警示執行個體](/help/search-social-commerce/new-ui/alerts-manage.md)的通知。

   * **[!UICONTROL Spreadsheet Feeds]**： [試算表摘要](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md)完成或失敗的通知。

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]**：通知特定檢視的資料檢視報告（例如[!UICONTROL Camapigns]檢視中的資料表內容）已完成或失敗。

      * **[!UICONTROL Reports]**： [自訂或排程報告](/help/search-social-commerce/new-ui/reports/management/report-manage.md)已完成或失敗的通知。

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]**：當當天最佳化停用時通知。

      * **[!UICONTROL Simulation Report]**：關於[模擬工作](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md)的通知。

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**：廣告商層級關於成功和失敗自動指派行銷活動轉換目標的通知。

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**：產品組合層級關於成功和失敗自動指派行銷活動轉換目標的通知。

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**：關於[產品組合大量編輯工作（透過Bulksheets）](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md)的通知。

         * **[!UICONTROL Portfolio Settings]**：有關[投資組合設定](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md)變更的通知。

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## 可用動作

* [檢視您的通知](#notification-view)

* [編輯您的通知設定](#notification-edit)

* [將通知標示為已讀取或未讀取](#notification-mark-read-unread)

* [刪除通知](#notification-delete)

* [啟用和停用推播通知](#notification-push-enable-disable)

* [安裝及解除安裝[!UICONTROL Notification Center]網頁應用程式](#notification-app-install-uninstall)

## 檢視您的通知 {#notification-view}

當您[訂閱有關帳戶驗證錯誤、觸發的自訂警示以及產生的[!UICONTROL Advertising Insights]的通知](#notification-edit)時，您可以在[!UICONTROL Notifications]面板或[!UICONTROL Notification Center]中檢視您的通知。

### 在[!UICONTROL Notifications]面板中檢視通知

1. 按一下任何頁面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. （可選）執行下列任一項作業：

   * 若要檢視任何通知的詳細資訊，請按一下通知名稱。

     在某些通知中，[!UICONTROL Action Recommended]區段可能包含連結，以開啟受影響或負責的實體的篩選檢視。

   * 若要將通知標示為&#x200B;*已讀取*&#x200B;或&#x200B;*未讀取*，請將游標停留在警示名稱上，然後按一下![標示為已讀取或未讀取](/help/search-social-commerce/assets/notifications-read-unread.png "標示為已讀取或未讀取")。

     標示為&#x200B;*已讀取*&#x200B;的通知以較淺的文字顯示，但在您刪除之前仍可繼續使用。

     ![已讀取和未讀取的通知](/help/search-social-commerce/assets/notifications-read-vs-unread.png "已讀取和未讀取的通知")

   * 若要變更通知型別的訂閱偏好設定，請按一下通知旁的![設定](/help/search-social-commerce/assets/settings-nc.png "設定")，變更您的設定，然後按一下&#x200B;**[!UICONTROL Save]**。

   * 若要刪除通知，請按一下通知旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

   * 若要開啟[!UICONTROL Notification Center]，請按一下&#x200B;**[!UICONTROL View All]**。

### 在[!UICONTROL Notification Center]中檢視通知

1. 按一下任何頁面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 按一下&#x200B;**[!UICONTROL View All]**。

1. （選擇性）若要依型別篩選通知，請按一下&#x200B;*[!UICONTROL Notices]、[!UICONTROL Recommendations]、[!UICONTROL Warnings]或[!UICONTROL Issues]*。

1. （可選）執行下列任一項作業：

   * 若要檢視任何通知的詳細資訊，請按一下通知名稱。

     在某些通知中，[!UICONTROL Action Recommended]區段可能包含連結，以開啟受影響或負責的實體的篩選檢視。

   * 若要將通知標示為&#x200B;*已讀取*&#x200B;或&#x200B;*未讀取*，請將游標停留在警示名稱上，然後按一下![標示為已讀取或未讀取](/help/search-social-commerce/assets/notifications-read-unread.png "標示為已讀取或未讀取")。

     標示為&#x200B;*已讀取*&#x200B;的通知以較淺的文字顯示，但在您刪除之前仍可繼續使用。

   * 若要變更通知型別的訂閱偏好設定，請按一下通知旁的![設定](/help/search-social-commerce/assets/settings-nc.png "設定")，變更您的設定，然後按一下&#x200B;**[!UICONTROL Save]**。

   * 若要刪除通知，請按一下通知旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

## 編輯您的通知設定 {#notification-edit}

您可以選擇訂閱或取消訂閱有關帳戶驗證錯誤、觸發的所有自訂警示以及完成您產生的[!UICONTROL Advertising Insights]的電子郵件和網頁通知。

1. 以下列其中一種方式開啟通知設定：

   * 在任何頁面的右上方，按一下![通知](/help/search-social-commerce/assets/notifications.png "通知")以開啟[!UICONTROL Notifications]面板。 按一下右上角的![設定](/help/search-social-commerce/assets/settings-nc.png "設定")。

   * 在任何頁面的右上方，按一下![通知](/help/search-social-commerce/assets/notifications.png "通知")，按一下&#x200B;**[!UICONTROL View All]**&#x200B;以開啟[!UICONTROL Notification Center]，然後在左側功能表中按一下![設定](/help/search-social-commerce/assets/settings-nc.png "設定")。

1. 變更上述任何通知類別的設定：

   * 若要訂閱或取消訂閱通知，請移動[!UICONTROL Subscribe]欄中的滑桿：

      * 若要取消訂閱所有通知型別，請將滑桿向左移動（已停用）。

      * 若要訂閱一或多個通知型別，請將滑桿移至右側（已啟用）。

   * （啟用[!UICONTROL Subscribe]時）若要訂閱電子郵件通知，請選取&#x200B;**[!UICONTROL Email]**&#x200B;欄中的核取方塊。

   * （停用[!UICONTROL Subscribe]時）若要在Search、Social和Commerce中訂閱Web通知，並在瀏覽器啟用推播通知時，選取&#x200B;**[!UICONTROL Web]**&#x200B;欄中的核取方塊。

     Web通知只有在您[啟用推播通知](#notification-push-enable-disable)至瀏覽器時才會傳送。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 將通知標示為已讀取或未讀取 {#notification-mark-read-unread}

將通知標示為&#x200B;*已讀取*&#x200B;或&#x200B;*未讀取*&#x200B;會變更每頁頂端[!UICONTROL Notifications]連結中指示的未讀取通知數目（例如![含有未讀取通知計數器的通知圖示](/help/search-social-commerce/assets/notifications-unread.png "含有未讀取通知計數器的通知圖示")）。

標示為&#x200B;*已讀取*&#x200B;的通知以較淺的文字顯示，但在您刪除之前仍可繼續使用。

![已讀取和未讀取的通知](/help/search-social-commerce/assets/notifications-read-vs-unread.png "已讀取和未讀取的通知")

1. [開啟通知面板或通知中心](#notification-view)。

1. 將游標停留在警示名稱上，然後按一下![標籤為已讀或未讀](/help/search-social-commerce/assets/notifications-read-unread.png "標籤為已讀或未讀")。

## 刪除通知 {#notification-delete}

### 刪除[!UICONTROL Notifications]面板中的通知

1. 按一下任何頁面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 按一下通知旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

### 刪除[!UICONTROL Notification Center]中的通知

1. 按一下任何頁面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 按一下&#x200B;**[!UICONTROL View All]**。

1. （選擇性）若要依型別篩選通知，請按一下&#x200B;*[!UICONTROL Notices]*、*[!UICONTROL Recommendations]*、*[!UICONTROL Warnings]*&#x200B;或&#x200B;*[!UICONTROL Issues]*。

1. 按一下通知旁的![刪除](/help/search-social-commerce/assets/delete.png "刪除")。

## 啟用和停用推播通知 {#notification-push-enable-disable}

您可以在Search、Social和Commerce中啟用通知，通知會根據瀏覽器的通知慣例顯示。 在使用[!DNL Microsoft Windows]的裝置上，通知會顯示在熒幕右下方（系統匣）。 在[!DNL Apple Mac]個裝置上，通知會顯示在右側功能表中。

推播通知可在下列瀏覽器中使用：

* [!DNL Google Chrome] 40以上

* [!DNL Microsoft Edge] 17和更高版本

* [!DNL Mozilla Firefox] 44和更高版本

您可以根據瀏覽器的標準程式停用推播通知。

### 啟用推播通知

1. 按一下任何頁面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 按一下&#x200B;**[!UICONTROL View All]**。

1. 在右下方，按一下![啟用推播通知](/help/search-social-commerce/assets/notifications-push.png "啟用推播通知")。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Enable]**。

1. 設定瀏覽器以允許來自[!UICONTROL Notification Center] （在`https://alert-center-ui-na.efrontier.com`）的通知。

   預設通知設定因瀏覽器而異，您可以a)自動顯示允許來自[!UICONTROL Notification Center]的通知的選項，或b)需要手動管理通知設定。 例如，在[!DNL Microsoft Edge]中，您可以從瀏覽器工具列允許來自[!UICONTROL Notification Center]的通知。 請參閱瀏覽器說明中的指示。

   ![在Microsoft Edge中管理通知設定的位置](/help/search-social-commerce/assets/notifications-blocked-dialog.png "在Microsoft Edge中管理通知設定的位置")

1. 在您的[通知設定](#notification-edit)中，啟用您要推送之警示型別的[!UICONTROL Web]通知。

### 停用推播通知

在瀏覽器的通知管理員中，從`https://alert-center-ui-na.efrontier.com`移除通知。 例如，在[!DNL Google Chrome]中，您可以從位於`chrome://settings/content/notifications`的指定網站移除或封鎖通知。

請參閱瀏覽器說明中的指示。

## 安裝及解除安裝[!UICONTROL Notification Center]網頁應用程式 {#notification-app-install-uninstall}

您可以透過安裝[!UICONTROL Notification Center] Web應用程式，在瀏覽器外部接收和管理通知。 應用程式看起來與Search、Social和Commerce中的[!UICONTROL Notification Center]相同，且具有相同的功能。 應用程式適用於[!DNL Google Chrome] 40和更高版本或[!DNL Microsoft Edge] 17和更高版本。

安裝[!UICONTROL Notification Center]應用程式後，它會在瀏覽器的應用程式管理員中自動啟用，並載入為單獨的視窗，其版面配置會根據視窗大小動態排列。 您可以從瀏覽器的應用程式管理員開啟和關閉應用程式，或將其釘選到作業系統的工作列或固定。 應用程式會自動更新。

![Microsoft Windows工作列中的「通知中心」圖示](/help/search-social-commerce/assets/windows-taskbar.png "Microsoft Windows工作列中的「通知中心」圖示")

您可以從瀏覽器的應用程式管理員停用或解除安裝應用程式。 如需有關管理Web應用程式的詳細資訊，請參閱瀏覽器的說明。

### 安裝[!DNL Google Chrome]的[!UICONTROL Notification Center]網頁應用程式

1. 按一下任何頁面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 按一下&#x200B;**[!UICONTROL View All]**。

1. 按一下右下角的![安裝通知中心Web應用程式](/help/search-social-commerce/assets/notifications-install-app.png "安裝通知中心Web應用程式")。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Add]**。

1. 在安裝應用程式中？ 訊息，按一下&#x200B;**[!UICONTROL Install]**。

### 安裝[!DNL Microsoft Edge]的[!UICONTROL Notification Center]網頁應用程式

* 從「搜尋」、「社交」和「Commerce」中：

   1. 按一下任何頁面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

   1. 按一下&#x200B;**[!UICONTROL View All]**。

   1. 按一下右下角的![安裝通知中心Web應用程式](/help/search-social-commerce/assets/notifications-install-app.png "安裝通知中心Web應用程式")。

   1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Add]**。

   1. 在[!UICONTROL Install Notification Center]應用程式訊息中，按一下&#x200B;**[!UICONTROL Install]**。

* 從[!DNL Edge]主功能表：

   1. 在瀏覽器工具列中按一下&#x200B;**...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**。

   1. 在[!UICONTROL Install Notification Center]應用程式訊息中，按一下&#x200B;**[!UICONTROL Install]**。

### 解除安裝[!DNL Google Chrome]的[!UICONTROL Notification Center]網頁應用程式

* 在[!DNL Chrome]中，移至`chrome://apps`，用滑鼠右鍵按一下&#x200B;**[!UICONTROL notification-center]**，然後按一下&#x200B;**[!UICONTROL Remove from Chrome]**。

### 解除安裝[!DNL Microsoft Edge]的[!UICONTROL Notification Center]網頁應用程式

1. 在[!DNL Edge]瀏覽器工具列中按一下&#x200B;**...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**。 或者，移至`edge://apps`。

1. 用滑鼠右鍵按一下&#x200B;**[!UICONTROL Notification Center]**，然後按一下&#x200B;**[!UICONTROL Uninstall]**。
