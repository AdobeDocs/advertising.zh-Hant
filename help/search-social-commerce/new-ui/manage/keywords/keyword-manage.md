---
title: 管理關鍵字
description: 瞭解如何建立及管理可競標和負面的關鍵字，以及將限制指派給關鍵字。
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 0%
---
# 管理關鍵字

*Beta功能*

僅&#x200B;*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]和現有[!DNL Baidu]帳戶*

關鍵字是與廣告相關聯的字詞或片語。 關鍵字設定包括關鍵字比對型別、關鍵字觸發廣告時可使用的最高競標，以及（針對某些廣告網路）可選的追蹤引數。 關鍵字層級設定會覆寫廣告群組或促銷活動設定。 負關鍵字會防止針對相符搜尋顯示廣告。

當您[透過API連線存取廣告網路帳戶](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)，且Search、Social和Commerce已同步處理帳戶資料與廣告網路時，您可以在[支援的促銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)中建立搜尋廣告群組的關鍵字。 您也可以編輯和變更關鍵字的狀態，以及建立和刪除負關鍵字。

如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

## 關於[!UICONTROL Keywords]檢視 {#keyword-view-about}

[!UICONTROL Manage] > [!UICONTROL Keywords]檢視包含所選廣告商帳戶的兩個標籤：

* [!UICONTROL Keywords]索引標籤會列出篩選檢視中的所有可競標關鍵字。

* [!UICONTROL Negatives]索引標籤會列出篩選檢視中的所有負面關鍵字。

### 可用動作

* [建立關鍵字](#keyword-create)

* [建立負面關鍵字](#keyword-negative-create)

* [編輯關鍵字設定](#keyword-edit)

* [變更關鍵字和負關鍵字的狀態或將其刪除](#keyword-status)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

* [將限制指派給關鍵字，並從關鍵字取消指派限制](#keyword-constraints)

* [指派標籤分類](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)給關鍵字

## 建立關鍵字 {#keyword-create}

>[!TIP]
>
>若要一次建立大量關鍵字，請使用[行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;索引標籤上，按一下&#x200B;**[!UICONTROL Create Keywords]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步驟中，選取網路、帳戶、行銷活動和廣告群組。

1. 輸入[[!DNL Baidu] 關鍵字設定](keyword-settings-baidu.md)、[[!DNL Google Ads] 關鍵字設定](keyword-settings-google.md)、[[!DNL LY Ads] 關鍵字設定](keyword-settings-yahoo-japan.md)、[[!DNL Microsoft Advertising] 關鍵字設定](keyword-settings-microsoft.md)或[[!DNL Yandex] 關鍵字設定](keyword-settings-yandex.md)。

   您最多可以在一個作業中輸入或貼上2000個關鍵字。 請使用逗號分隔多個關鍵字，或在不同的行中輸入這些關鍵字。

   >[!NOTE]
   >
   >如果帳戶或行銷活動設定僅在廣告層級指定追蹤，則Search、Social和Commerce不會產生關鍵字的追蹤。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯] ![ ](/help/search-social-commerce/assets/edit-new.png " [編輯] ") **[!UICONTROL Edit]**&#x200B;並變更實體和/或關鍵字設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 編輯關鍵字設定 {#keyword-edit}

視廣告網路而定，變更關鍵字文字或比對型別可以刪除現有關鍵字並建立新關鍵字。 如需詳細資訊，請參閱廣告網路的關鍵字設定。

>[!TIP]
>
>若要一次編輯大量關鍵字資料，包括不同廣告網路上的關鍵字，請使用[行銷活動大量工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;索引標籤上，選取要編輯的每個關鍵字旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[[!DNL Baidu] 關鍵字設定](keyword-settings-baidu.md)、[[!DNL Google Ads] 關鍵字設定](keyword-settings-google.md)、[[!DNL LY Ads] 關鍵字設定](keyword-settings-yahoo-japan.md)、[[!DNL Microsoft Advertising] 關鍵字設定](keyword-settings-microsoft.md)或[[!DNL Yandex] 關鍵字設定](keyword-settings-yandex.md)。

   對於多個關鍵字，您只能編輯所有選定關鍵字的共同欄位，並且您的變更會套用到所有選定的關鍵字。 對於某些英數字元欄位，您可以將現有值變更為指定值、將現有字串取代為指定字串、新增首碼或附加尾碼。 對於某些貨幣欄位，您可以將現有值變更為指定值，或透過指定百分比或貨幣金額來增加或減少金額，但有限制。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯]。![](/help/search-social-commerce/assets/edit-new.png "[編輯]。")**[!UICONTROL Edit]**，然後變更關鍵字設定。

1. 按一下&#x200B;**[!UICONTROL Update]**。

## 建立負面關鍵字 {#keyword-negative-create}

僅&#x200B;*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]和現有[!DNL Baidu]帳戶*

您可以針對搜尋或顯示/原生網路，為搜尋廣告群組或行銷活動建立負關鍵字。

>[!NOTE]
>
>您也可以在[廣告群組設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)和[行銷活動設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)中建立和編輯負關鍵字。

>[!TIP]
>
>若要一次建立大量負面關鍵字，請使用[行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Negatives]**&#x200B;索引標籤上，按一下&#x200B;**[!UICONTROL Create Negatives]**，然後按&#x200B;**[!UICONTROL Campaign Negative Keyword]**&#x200B;或&#x200B;**[!UICONTROL Ad Group Negative Keyword]**。

1. 選取網路、帳戶、促銷活動，以及（針對廣告群組層級的負面關鍵字）廣告群組。

1. 輸入負關鍵字。 請使用下列語法，不含減號(`-`)：

   * 負值廣泛比對： `keyword` （不受[!DNL Microsoft Advertising]支援）

   * 負面字詞相符： `"keyword"`

   * 完全相符的負值： `[keyword]`

   請使用逗號分隔多個值，或在不同的行中輸入這些值。 您最多可以在一個作業中輸入或貼上2000個負關鍵字。 以下是適用的需求和限制：

   * 最大字元長度： [!DNL Baidu]： 30個單位元組或15個雙位元組； [!DNL Microsoft Advertising]： 100個單位元組或50個雙位元組； [!DNL Google Ads]和[!DNL LY Ads]： 80個單位元組或40個雙位元組。

   * [!DNL Baidu]僅允許每個廣告群組的每個關鍵字有一個符合型別。 例如，廣告群組1不能同時包含`"keyword"`和`[keyword]`。

   * [!DNL Google Ads]：每個關鍵字最多只能包含10個字詞，而且只能包含字母、數字和下列特殊字元：空格`# $ & _ - " [ ] ' + . / :`

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯] ![ ](/help/search-social-commerce/assets/edit-new.png " [編輯] ") **[!UICONTROL Edit]**，然後變更實體和/或負面的關鍵字。

1. 按一下&#x200B;**[!UICONTROL Create]**。

## 變更關鍵字和負關鍵字的狀態 {#keyword-status}

您可以暫停作用中、可競標的搜尋關鍵字，以停用其競標。 您稍後可以透過將狀態變回作用中來繼續競標。

您也可以刪除作用中或暫停的搜尋關鍵字或負關鍵字。 已刪除的關鍵字會從廣告網路中刪除。 當您將其納入資料篩選器時，仍可顯示這些值，但您無法加以變更。

### 啟動或暫停關鍵字

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;索引標籤上，選擇性地篩選清單，然後選取您要變更其狀態之每個關鍵字旁的核取方塊。

1. 在大量動作工具列中，變更狀態：

   * 若要啟用暫停的關鍵字，請按一下&#x200B;**[!UICONTROL Activate]**。

   * 若要暫停使用中的關鍵字，請按一下&#x200B;**[!UICONTROL Pause]**。

### 刪除關鍵字或負關鍵字

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;或&#x200B;**[!UICONTROL Negatives]**&#x200B;索引標籤上，選擇性地篩選清單，然後選取要刪除的每個關鍵字或負關鍵字旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

## 管理關鍵字的限制指派 {#keyword-constraints}

您可以為行銷活動、廣告群組、關鍵字、位置、單位層級產品群組及動態搜尋目標指派及移除競標限制。 每個圖元只能有一個限制。

限制由子實體繼承，因此除非您想要覆寫繼承的值，否則不需要為子實體指派限制。

取消指定限制會移除與帳號元件及其所有子元件的關聯，且這些元件無法再使用該限制的報表資料。 取消指定限制並不會刪除限制或帳戶元件本身。

>[!NOTE]
>
>* 如果您稍後編輯非可變廣告的關鍵字或廣告復本（因此建立新的關鍵字或廣告），則限制不會指派給新圖元。
>* 作用中限制僅限制最佳化舊關鍵字層級產品組合中已指派競標單位的競標。 若競標單位位於作用中產品組合、混合產品組合或不在產品組合中，則會忽略這些專案。

### 為關鍵字指派限制 {#keyword-constraint-assign}

您可以將單一限制指定給一或多個關鍵字。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;索引標籤上，選取您要指派單一限制的每個關鍵字旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

### 從關鍵字取消指派限制 {#keyword-constraint-unassign}

取消指派限制並不會刪除它。 若要刪除限制，使其無法用於未來用途，請參閱「競標限制」上「最佳化指南」一章中的「刪除搜尋競標單位的限制」，可於搜尋、社交和Commerce中使用。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;索引標籤上，選取每個要取消指派限制之關鍵字旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] 關鍵字設定](keyword-settings-baidu.md)
>* [[!DNL Google Ads] 關鍵字設定](keyword-settings-google.md)
>* [[!DNL LY Ads] 關鍵字設定](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] 關鍵字設定](keyword-settings-microsoft.md)
>* [[!DNL Yandex] 關鍵字設定](keyword-settings-yandex.md)
>* [管理搜尋競標單位的限制](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理標籤分類](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
