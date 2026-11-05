---
title: 管理行銷活動和廣告群組的對象目標
description: 瞭解如何針對Google Ads和Microsoft Advertising管理對象目標及其競標調整。
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
source-wordcount: '562'
ht-degree: 0%
---
# 管理行銷活動和廣告群組的對象目標

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶*

[!DNL Google Ads]行銷活動和廣告群組以及[!DNL Microsoft Advertising]廣告群組可以鎖定來自相同廣告網路的特定[對象](audience-manage.md)。 廣告網路會決定要鎖定目標對象的大小。

對象目標會將現有對象與行銷活動或廣告群組建立關聯。 您可以編輯現有目標的競標調整與狀態。

>[!NOTE]
>
>[對象排除](audience-exclusions.md)一律覆寫目標。

## 關於[!UICONTROL Targets]檢視 {#audience-targets-view-about}

「[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets]」檢視會列出所選廣告商之篩選檢視中的對象目標。

檢視資料需要[!UICONTROL View Audiences]許可權。 編輯、變更目標狀態及刪除目標需要[!UICONTROL Edit Audience Targets]許可權。

### 可用動作

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [編輯對象目標競標調整和狀態](#audience-targets-edit)

* [變更對象目標的狀態或刪除對象目標](#audience-targets-status)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## 編輯對象目標競標調整和狀態 {#audience-targets-edit}

您可以一次編輯一或多個對象目標。 您的變更會套用至所有選取的目標。

>[!NOTE]
>
>當父級行銷活動使用CPC競標策略，並且在設定為自動最佳化對象目標競標調整值的產品組合中，搜尋、Social和Commerce會自動最佳化競標修飾元。 未最佳化[!DNL Microsoft Advertising]動態再行銷對象目標的競標修飾詞。

1. 在主功能表中，按一下「**[!UICONTROL Targeting]>[!UICONTROL Audiences]**」，然後按一下「**[!UICONTROL Targets]**」標籤。

1. 選取每個要編輯的目標旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯&#x200B;**[!UICONTROL Bid Modifier]**&#x200B;或&#x200B;**[!UICONTROL Status]**，或兩者。 檢視[編輯設定](#audience-targets-edit-settings)。

   欄位保持不變，以保留現有值。

1. （選用）展開&#x200B;**[!UICONTROL ADDITIONAL DETAILS]**&#x200B;並輸入&#x200B;**[!UICONTROL Project Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**。

1. 按一下&#x200B;**[!UICONTROL Save]**。

您也可以按一下&#x200B;**[!UICONTROL Bid Adjustment]**&#x200B;欄中的單一目標值，直接在資料表中編輯其競標調整。

## 變更對象目標的狀態或刪除對象目標 {#audience-targets-status}

您可以暫停作用中的對象目標以停用該目標的競標，稍後再啟用它以繼續競標。 您也可以刪除作用中或暫停的目標。

1. 在主功能表中，按一下「**[!UICONTROL Targeting]>[!UICONTROL Audiences]**」，然後按一下「**[!UICONTROL Targets]**」標籤。

1. （選用）篩選清單以包含特定對象目標。

1. 選取每個要變更其狀態的目標旁的核取方塊。

1. 在大量動作工具列中，按一下下列其中一項：

   * **[!UICONTROL Activate]**&#x200B;以啟動選取的目標。

   * **[!UICONTROL Pause]**&#x200B;以暫停選取的目標。

   * **[!UICONTROL Delete]**&#x200B;刪除選取的目標。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

## 對象目標編輯設定 {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]：**&#x200B;如何變更對象競標調整：

* *[!UICONTROL Set To]：*&#x200B;以指定的百分比取代現有的競標調整。

* *[!UICONTROL Increase]：*&#x200B;將現有值增加指定的百分比。

* *[!UICONTROL Decrease]：*&#x200B;將現有值減少指定的百分比。

對於[!UICONTROL Increase]和[!UICONTROL Decrease]，請輸入非負值。

對於設定值，0%不會調整競標。 其他支援的值範圍介於–90%到900%。 例如，如果關鍵字層級的競標為1 USD，而對象競標調整為50%，則該對象的競標會增加到1.50 USD。

**[!UICONTROL Status]：**&#x200B;選取&#x200B;**[!UICONTROL Active]**&#x200B;以啟用競標，或選取&#x200B;**[!UICONTROL Paused]**&#x200B;停用目標的競標。

>[!MORELIKETHIS]
>
>* [管理對象](audience-manage.md)
>* [管理行銷活動和廣告群組的對象排除](audience-exclusions.md)
