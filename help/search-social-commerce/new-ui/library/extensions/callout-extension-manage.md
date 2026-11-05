---
title: 管理Google Ads共用圖說文字擴充功能
description: 瞭解如何建立、編輯和刪除Google Ads共用的圖說文字擴充功能。
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
source-wordcount: '685'
ht-degree: 0%
---
# 管理[!DNL Google Ads]共用圖說文字延伸

僅&#x200B;*[!DNL Google Ads]個帳戶*

圖說文字擴充功能是有關您網站提供的產品、服務或促銷活動的資訊文字，會以文字廣告顯示。 廣告網路可能會顯示2-4個含有廣告的圖說文字。

您在帳戶層級為[同步的Google廣告帳戶](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)建立共用的圖說文字和設定。 資料庫中的圖說文字不會與廣告搭配使用，直到您將它們與搜尋網路上的支援行銷活動或廣告群組建立關聯為止。

若要讓您的廣告符合顯示圖說文字的資格，請為每個行銷活動或廣告群組至少指派兩個圖說文字。 廣告群組層級的編號說明會覆寫行銷活動層級的編號說明。

## 關於[!UICONTROL Callouts]和[!UICONTROL Associations]檢視 {#callout-view-about}

在&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;中，**[!UICONTROL Callouts]**&#x200B;索引標籤會列出您的帳戶層級共用圖說文字。 **[!UICONTROL Associations]**&#x200B;索引標籤會列出擴充功能與帳戶實體之間的關聯。

檢視這些標籤需要[!UICONTROL View Extensions]許可權。 建立、編輯和刪除編號說明以及建立或刪除關聯需要[!UICONTROL Edit Extensions]許可權。

如需每個帳戶的副檔名數目上限，請參閱[Google Ads帳戶限制](https://support.google.com/google-ads/answer/6372658)檔案。

### 可用動作

* [建立共用圖說文字](#callout-create)

* [編輯共用的圖說文字設定](#callout-edit)

* [刪除共用圖說文字](#callout-delete)

* [將共用圖說文字與行銷活動和廣告群組建立關聯](ad-extension-association-manage.md#callout-associate)

* [刪除擴充功能關聯](ad-extension-association-manage.md#association-delete)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

## 建立共用圖說文字 {#callout-create}

1. 在主功能表中，按一下「**[!UICONTROL Library]>[!UICONTROL Extensions]**」，然後按一下「**[!UICONTROL Callouts]**」標籤。

1. 按一下&#x200B;**[!UICONTROL Create Callout]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;中，選取[!DNL Google Ads]和帳戶。

1. 輸入[共用圖說文字設定](#shared-callout-settings)。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 檢閱設定。 若要變更設定，請按一下適用區段中的&#x200B;**[!UICONTROL Edit]**。

1. 按一下&#x200B;**[!UICONTROL Create]**。

建立圖說文字之後，[請將其與行銷活動或廣告群組建立關聯](ad-extension-association-manage.md#callout-associate)。

## 編輯共用的圖說文字設定 {#callout-edit}

您可以一次編輯一個共用圖說文字。 建立開始日期後即無法變更。

1. 在主功能表中，按一下「**[!UICONTROL Library]>[!UICONTROL Extensions]**」，然後按一下「**[!UICONTROL Callouts]**」標籤。

1. 選取一個編號說明旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[共用圖說文字設定](#shared-callout-settings)。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**，檢閱設定，然後按一下&#x200B;**[!UICONTROL Update]**。

## 刪除共用圖說文字 {#callout-delete}

1. 在主功能表中，按一下「**[!UICONTROL Library]>[!UICONTROL Extensions]**」，然後按一下「**[!UICONTROL Callouts]**」標籤。

1. 選取要刪除的每個共用編號說明旁的核取方塊。

   如需選取多個列的資訊，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

若要移除關聯而不刪除資料庫中的共用圖說文字，請改為刪除[關聯](ad-extension-association-manage.md#association-delete)。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

## 共用圖說文字設定 {#shared-callout-settings}

如需圖說文字不核准的其他原則和原因，請參閱[Google廣告圖說文字需求](https://support.google.com/adspolicy/answer/1054212)。

**[!UICONTROL Callout Text]：**&#x200B;要顯示的文字。 它最多可包含25個單位元組或12個雙位元組字元。 它不能在文字開頭包含驚歎號或標點符號。

**[!UICONTROL Start Date]：** （選擇性；僅建立）編號說明可能顯示的第一個日期。 預設為當天。 若要指定未來日期，請以YYYY/MM/DD格式輸入，或使用日期選擇器。 現有圖說文字的開始日期是唯讀的。

**[!UICONTROL End Date]：** （選用）編號說明可能顯示的最後日期。 依預設，編號說明可能會無限期顯示。 若要指定結束日期，請以YYYY/MM/DD格式輸入，或使用日期選擇器。

**[!UICONTROL Mobile Preference]：** （選擇性）允許[!DNL Google Ads]嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示擴充功能。 否則，擴充功能會出現在任何裝置型別上。 [!DNL Google Ads]不保證會在偏好的裝置型別上顯示副檔名。

## 圖說文字的效能資料 {#callout-performance}

搜尋、Social和Commerce對應廣告擴充功能上的點選次數，並將結果轉換為與擴充功能顯示所在廣告相關聯的關鍵字。 「搜尋」、「社交」和「Commerce」不提供擴充功能層級的成本和點選資料。

您可以在[!DNL Google Ads]介面中檢視擴充功能層級的成本並點選資料。

>[!MORELIKETHIS]
>
>* [管理共用的網站連結延伸模組](sitelink-extension-manage.md)
>* [管理廣告延伸關聯](ad-extension-association-manage.md)
