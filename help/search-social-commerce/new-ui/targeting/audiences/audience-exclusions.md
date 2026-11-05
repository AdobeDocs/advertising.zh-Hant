---
title: 管理行銷活動和廣告群組的對象排除
description: 瞭解Google Ads和Microsoft Advertising對象排除，包括如何刪除Google Ads排除。
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
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%
---
# 管理行銷活動和廣告群組的對象排除

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶*

對象排除可防止行銷活動或廣告群組中的廣告向特定[對象](audience-manage.md)中的使用者顯示。

對於[!DNL Google Ads]帳戶，您可以排除任何對象型別。 對於[!DNL Microsoft Advertising]帳戶，您只能排除動態再行銷對象。

>[!NOTE]
>
>排除專案一律會覆寫[對象目標](audience-targets-manage.md)。

## 關於[!UICONTROL Exclusions]檢視 {#audience-exclusions-view-about}

「[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions]」檢視會在所選廣告商的篩選檢視中列出對象排除。

檢視資料需要[!UICONTROL View Audiences]許可權。 選取資料列和刪除支援的排除專案需要[!UICONTROL Edit Audience Exclusions]許可權。

### 可用動作

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [刪除對象排除專案](#audience-exclusions-delete)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## 刪除對象排除專案 {#audience-exclusions-delete}

僅&#x200B;*[!DNL Google Ads]個排除專案*

您可以刪除一或多個[!DNL Google Ads]對象排除。 此檢視中不支援刪除[!DNL Microsoft Advertising]排除專案。

1. 在主功能表中，按一下「**[!UICONTROL Targeting]>[!UICONTROL Audiences]**」，然後按一下「**[!UICONTROL Exclusions]**」標籤。

1. （選用）篩選清單以包含特定對象排除專案。

1. 選取要刪除的每個[!DNL Google Ads]排除專案旁的核取方塊。 請勿在選取範圍中包含其他廣告網路的排除專案。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

>[!MORELIKETHIS]
>
>* [管理對象](audience-manage.md)
>* [管理行銷活動和廣告群組的對象目標](audience-targets-manage.md)
