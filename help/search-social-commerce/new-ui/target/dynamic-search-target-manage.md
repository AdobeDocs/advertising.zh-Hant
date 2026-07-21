---
title: 管理 [!DNL Google Ads] 動態搜尋目標
description: 瞭解如何建立和管理 [!DNL Google Ads] 動態搜尋目標。
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 702
ht-degree: 0%

---

# 管理[!DNL Google Ads]動態搜尋目標

僅&#x200B;*[!DNL Google Ads]個帳戶*

您可以建立、編輯和變更使用搜尋網路之[!DNL Google Ads]行銷活動的動態搜尋目標狀態。

## 什麼是動態搜尋目標？

動態搜尋目標會定義廣告網路是使用您網站中的所有頁面還是頁面子集，來鎖定您的動態搜尋廣告。 在廣告群組層級設定動態搜尋目標；這些目標會套用至相同廣告群組中的所有動態搜尋廣告。

根據您的行銷活動設定，動態搜尋目標可能是必要或選用的：

* 若未在行銷活動的&quot;[!UICONTROL DSA Options]&quot;區段中指定網站網域和語言，您必須建立動態搜尋目標。

* 當您在促銷活動的&quot;[!UICONTROL DSA Options]&quot;區段中指定網站網域和語言時，您可以選擇建立動態搜尋目標。

  [!DNL Google Ads]會根據這些設定所指定的網站內容，自動顯示您的動態搜尋廣告。

若要最佳追蹤效能，請為每個動態搜尋目標設定一個廣告群組的行銷活動，並包含以所有條件為目標的廣告群組。

如需[!DNL Google Ads]動態搜尋廣告的詳細資訊，請參閱https://support.google.com/google-ads/answer/2471185。

## [!UICONTROL Auto Targets]檢視

[!UICONTROL Target] > [!UICONTROL Auto Targets]檢視會列出所選廣告商帳戶之篩選檢視中的所有動態搜尋目標。 您也可以管理動態搜尋目標。

### 可用動作

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [將限制](#constraint-assign)指派給動態搜尋目標，以及[從動態搜尋目標移除限制](#constraint-unassign)

* [指派標籤分類](#classification-values-assign)給動態搜尋目標，以及[從動態搜尋目標移除標籤分類](#classification-values-remove)

>[!NOTE]
>
>您可以上傳[大量工作表檔案](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)並張貼至廣告網路，一次建立及編輯大量目標資料（包括標籤和限制指派）。

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## 從新的[!UICONTROL Auto Targets]檢視指派限制給選取的動態搜尋目標 {#constraint-assign}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Target]>[!UICONTROL Auto Targets]**。

1. 選取每個動態搜尋目標旁的核取方塊，您將為其指定單一限制。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 選取限制。

1. 按一下&#x200B;**[!UICONTROL Assign Now]**。

## 從新的[!UICONTROL Auto Targets]檢視移除所選動態搜尋目標的限制 {#constraint-unassign}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Auto Targets]**。

1. 選取每個動態搜尋目標旁的核取方塊，您會從中取消指派限制。

1. 在大量動作工具列中按一下&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 按一下&#x200B;**[!UICONTROL Confirm]**。

## 指派分類值給動態搜尋目標 {#classification-values-assign}

>[!NOTE]
>
>標籤值由子實體繼承，因此除非您想要覆寫繼承的值，否則請勿輸入子實體的值。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Target]>[!UICONTROL Auto Targets]**。

1. 選取您要指派標籤值的每個動態搜尋目標旁的核取方塊。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中按一下&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**。

1. 請針對每個適用的分類值，執行下列動作：

   1. 在&#x200B;**[!UICONTROL Classifications]**&#x200B;欄中指定分類：

      * 若要使用現有的分類，請按一下分類名稱將其展開。

      * 若要建立分類，請按一下欄標題中的[!UICONTROL +]。 在輸入欄位中輸入分類名稱，然後按一下[儲存] ![&#x200B; &#x200B;](/help/search-social-commerce/assets/save-checkmark.png " [儲存] ")，立即儲存分類。 若要使用新分類，請按一下分類名稱將其展開。

        名稱必須包含[ASCII字元32-126](https://www.asciitable.com/)，最大長度為27個單位元組字元。

   1. 在&#x200B;**[!UICONTROL Value Name]**&#x200B;欄中，指定所選分類的值：

      * 若要使用現有值，請選取該值。

      * 若要建立值，請按一下欄標題中的[!UICONTROL +]。 在輸入欄位中輸入值，然後按一下![儲存](/help/search-social-commerce/assets/save-checkmark.png "儲存")，立即儲存值並依預設選取。

        長度上限為100個字元，可包含ASCII和非ASCII字元。

1. 按一下&#x200B;**+[!UICONTROL Assign Now]**。

## 從動態搜尋目標中移除標籤分類值 {#classification-values-remove}

移除分類值會移除與帳戶元件及其所有子元件的關聯。 這些元件不再提供分類值的報表資料。 移除分類值不會刪除值或帳戶元件。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Target]>[!UICONTROL Auto Targets]**。

1. 選取每個動態搜尋目標旁的核取方塊，您會從其中移除標籤值。

   如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

1. 在大量動作工具列中，按一下&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 選取每個分類值旁的核取方塊，以從選取的實體中移除。

   若要選取所有指派的值，請按一下&#x200B;**[!UICONTROL Select All]**。 若要取消選取所有指派的值，請按一下&#x200B;**[!UICONTROL Deselect All]**。

1. 按一下&#x200B;**[!UICONTROL Unassign Selected]**。

>[!MORELIKETHIS]
>
>* [（新UI）管理搜尋競標單位的限制](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [&#x200B; （新UI）管理標籤分類](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
