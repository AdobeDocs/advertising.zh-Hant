---
title: 管理共用網站連結擴充功能
description: 瞭解如何建立、編輯和刪除共用網站連結擴充功能。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%
---
# 管理共用網站連結擴充功能

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶*

網站連結是文字廣告清單中的額外文字連結。 使用網站連結將使用者直接帶往您網站上的特定頁面。 廣告網路會根據網站連結與廣告的相關性來決定要顯示的網站連結。

您可以選擇加入每個網站連結的描述性文字。 當廣告網路與網站連結高度相關時，廣告網路也可能會顯示帳戶中現有廣告的復本。 [!DNL Google Ads]可能會在案頭廣告中顯示2到6個網站連結，在行動廣告中最多可顯示4個網站連結。 [!DNL Microsoft Advertising]可能會顯示兩個、四個或六個有說明的網站連結，或是4-6沒有說明。

您在帳戶層級為[已同步化的廣告網路帳戶](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)建立共用的網站連結文字和設定。 資料庫中的網站連結不會與廣告搭配使用，直到您將它們與帳戶實體建立關聯為止。

## 關於[!UICONTROL Sitelinks]和[!UICONTROL Associations]檢視 {#sitelink-view-about}

在&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;中，**[!UICONTROL Sitelinks]**&#x200B;索引標籤會列出您的帳戶層級共用網站連結。 **[!UICONTROL Associations]**&#x200B;索引標籤會列出擴充功能與帳戶實體之間的關聯。

檢視這些標籤需要[!UICONTROL View Extensions]許可權。 建立、編輯和刪除網站連結，以及建立或刪除關聯，需要[!UICONTROL Edit Extensions]許可權。

請參閱廣告網路說明，瞭解每個[Google Ads帳戶](https://support.google.com/google-ads/answer/6372658)和每個[Microsoft Advertising帳戶](https://help.ads.microsoft.com/#apex/3/en/52001)的副檔名數目上限。

### 可用動作

* [建立共用的網站連結](#sitelink-create)

* [編輯共用的網站連結設定](#sitelink-edit)

* [刪除共用的網站連結](#sitelink-delete)

* [將共用的網站連結與帳戶、行銷活動和廣告群組建立關聯](ad-extension-association-manage.md#sitelink-associate)

* [刪除擴充功能關聯](ad-extension-association-manage.md#association-delete)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

## 建立共用的網站連結 {#sitelink-create}

1. 在主功能表中，按一下「**[!UICONTROL Library]>[!UICONTROL Extensions]**」，然後按一下「**[!UICONTROL Sitelinks]**」標籤。

1. 按一下&#x200B;**[!UICONTROL Create Sitelink]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;中，選取廣告網路和帳戶。

1. 輸入[共用的網站連結設定](#shared-sitelink-settings)。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 檢閱設定。 若要變更設定，請按一下適用區段中的&#x200B;**[!UICONTROL Edit]**。

1. 按一下&#x200B;**[!UICONTROL Create]**。

建立網站連結後，[將其與帳戶、行銷活動或廣告群組建立關聯](ad-extension-association-manage.md#sitelink-associate)。

## 編輯共用的網站連結設定 {#sitelink-edit}

您可以一次編輯一個共用網站連結。 建立開始日期後即無法變更。

1. 在主功能表中，按一下「**[!UICONTROL Library]>[!UICONTROL Extensions]**」，然後按一下「**[!UICONTROL Sitelinks]**」標籤。

1. 選取一個網站連結旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[共用的網站連結設定](#shared-sitelink-settings)。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**，檢閱設定，然後按一下&#x200B;**[!UICONTROL Update]**。

您也可以按一下網站連結的值，直接在資料表中編輯網站連結的&#x200B;**[!UICONTROL Base URL]**&#x200B;或&#x200B;**[!UICONTROL Tracking Template]**。

## 刪除共用的網站連結 {#sitelink-delete}

1. 在主功能表中，按一下「**[!UICONTROL Library]>[!UICONTROL Extensions]**」，然後按一下「**[!UICONTROL Sitelinks]**」標籤。

1. 選取要刪除的每個共用網站連結旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

若要移除關聯而不從資料庫中刪除共用網站連結，請改為刪除[關聯](ad-extension-association-manage.md#association-delete)。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

## 共用的網站連結設定 {#shared-sitelink-settings}

如需網站連結未核准的其他原則和原因，請參閱[Google Ads網站連結需求](https://support.google.com/adspolicy/answer/1054210)和[Microsoft Advertising網站連結需求](https://help.ads.microsoft.com/#apex/ads/en/ext60206)。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]：**&#x200B;要針對連結顯示的文字。 它最多可包含25個單位元組或12個雙位元組字元。 連結文字在帳戶或行銷活動中必須是唯一的。

>[!NOTE]
>
>([!DNL Google Ads]) 35個字元的現有文字會顯示在桌上型電腦和平板電腦的廣告中，但不會顯示在行動裝置上。

**[!UICONTROL Status]：**&#x200B;網站連結的顯示狀態： **[!UICONTROL Active]**&#x200B;或現有網站連結的&#x200B;**[!UICONTROL Deleted]**。 新網站連結預設為作用中。

**[!UICONTROL Description Line 1]，[!UICONTROL Description Line 2]：**&#x200B;廣告網路可能顯示在連結文字下的額外文字。 若要包含說明，請輸入兩個欄位。 每個字元最多可包含35個單位元組或17個雙位元組字元。

**[!UICONTROL Start Date]：** （選擇性；僅建立）網站連結可能顯示的第一個日期。 預設為當天。 若要指定未來日期，請以YYYY/MM/DD格式輸入，或使用日期選擇器。 現有網站連結的開始日期是唯讀的。

**[!UICONTROL End Date]：** （選用）網站連結可能顯示的最後日期。 依預設，網站連結可能會無限期地顯示。 若要指定結束日期，請以YYYY/MM/DD格式輸入，或使用日期選擇器。

**[!UICONTROL Mobile Preference]：** （選擇性）允許網路嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示擴充功能。 依預設，此選項不會啟用，而且擴充功能可出現在任何裝置型別上。 網路不保證會在偏好的裝置型別上顯示擴充功能。

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]：** （選用）追蹤URL，包括離登陸網域重新導向與追蹤引數，而最終的登陸頁面URL內嵌在引數中。 例如，`https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`。

在此檢視中，為[!UICONTROL Base URL]和[!UICONTROL Tracking Template]輸入的值必須以`http://`或`https://`開頭，且不能包含空格。

* 當行銷活動設定包含&#x200B;**[!UICONTROL EF Redirect]**&#x200B;和&#x200B;**[!UICONTROL Auto Upload]**&#x200B;時，搜尋、社交和Commerce會在您儲存記錄時自動為其自己的重新導向和追蹤代碼加上前置詞。

* 如需內嵌最終URL的引數，請參閱[Microsoft Advertising檔案](https://help.ads.microsoft.com/#apex/3/en/56799)或[Google Ads ValueTrack檔案](https://support.google.com/google-ads/answer/6305348)中的「僅限追蹤範本」引數。

* 您可以包含URL引數和行銷活動層級自訂引數(以&amp;符號(`&`)分隔)，以及協力廠商重新導向與追蹤。

* 最精細層級的追蹤範本會覆寫較高層級的範本。

>[!NOTE]
>
>* 若為具有最終URL的帳戶，基本URL可能會在登陸頁面網域或子網域內包含重新導向，但不能在登陸頁面網域外。 廣告網路會擷取網域以建立顯示URL。
>* ([!DNL Google Ads])行銷活動或廣告群組中的每個網站連結必須具有約80%唯一內容的唯一登陸頁面。 請勿將相同頁面上多個錨點的連結作為個別網站連結登陸頁面使用。
>* ([!DNL Google Ads])在網站連結或關鍵字層級更新追蹤範本，會重新提交相關廣告以供稽核。 在帳戶、行銷活動或廣告群組層級更新它不會重新提交廣告。
>* ([!DNL Microsoft Advertising])您可以更新任何層級的追蹤範本，而無需重新提交廣告以供核准。
>* ([!DNL Google Ads])避免使用巨集，這些巨集不會取代來自啟用平行追蹤之來源的點按。 如果需要巨集，您的Adobe帳戶團隊會與客戶支援或實作團隊合作來新增它們。

## 網站連結的效能資料 {#sitelink-performance}

搜尋、Social和Commerce對應廣告擴充功能上的點選次數，並將結果轉換為與擴充功能顯示所在廣告相關聯的關鍵字。 「搜尋」、「社交」和「Commerce」無法使用擴充功能層級的成本和點選資料。

在[!UICONTROL Transaction Report]中，`sl:<Sitelink text>`的[!UICONTROL Link Type]值（例如`sl:See Current Offers`）會識別來自網站連結的交易，而非廣告本身。 請參閱[交易報告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)。

您可以在廣告網路的介面中檢視擴充功能層級的成本和點選資料。

>[!MORELIKETHIS]
>
>* [管理Google Ads共用圖說文字副檔名](callout-extension-manage.md)
>* [管理廣告延伸關聯](ad-extension-association-manage.md)
