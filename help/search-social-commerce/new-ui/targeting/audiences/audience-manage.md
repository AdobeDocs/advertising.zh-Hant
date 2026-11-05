---
title: 管理對象
description: 瞭解對象庫，以及如何管理Google Ads和Microsoft Advertising支援的對象。
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
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%
---
# 管理對象

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶*

對象是使用者群組，您可以將其用作[目標](audience-targets-manage.md)或相同廣告網路上受支援行銷活動和廣告群組的[排除專案](audience-exclusions.md)。 廣告網路會決定要鎖定目標對象的大小。

## 關於[!UICONTROL Library]檢視 {#audience-view-about}

[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Library]檢視會列出所選廣告商的對象。 若要檢視[!DNL Google Ads]和[!DNL Microsoft Advertising]對象，請從&#x200B;**[!UICONTROL Network]**&#x200B;功能表選取&#x200B;**[!UICONTROL All Other Network]**。

資料庫包含[!DNL Google Ads]個以客戶資料為基礎、市場內和類似的對象，以及[!DNL Microsoft Advertising]個再行銷、動態再行銷、自訂、客戶比對、市場內和類似的對象。

檢視資料需要[!UICONTROL View Audiences]許可權。 選取列和刪除支援的對象需要[!UICONTROL Edit Audience Library]許可權。

### 可用動作

<!--
Restricted to internal beta users:

* [Create a customer match audience from a customer data list](#audience-customer-list-create)

* [Create a Google Ads audience from Adobe audiences](#audience-adobe-create)

* [Create a Microsoft Advertising dynamic remarketing audience](#audience-dynamic-create)

* [Update a customer match audience using a customer data list](#audience-customer-list-edit)

* [Edit a dynamic remarketing audience](#audience-dynamic-edit)
-->

* [刪除動態再行銷對象](#audience-delete)

* [將選取列中的所有資料複製到剪貼簿](#copy-to-clipboard)

## 對象資料來源 {#audience-data-sources}

您可以根據下列資料來源使用對象：

* **Adobe對象區段：**&#x200B;選擇加入Adobe Audience Manager或Adobe Analytics帳戶的廣告商可以根據其現有的[!DNL Adobe]區段使用[!DNL Google Ads]個客戶比對對象。

  * 對於沒有Audience Manager且擁有[!DNL Analytics]帳戶之廣告商，對象會使用與Adobe CX Enterprise共用之[!DNL Analytics]區段中的使用者ID。

  * 對於具有Audience Manager帳戶的廣告商，受眾會使用來自Audience Manager區段的使用者ID，這些區段將「搜尋」、「社交」和「Commerce」當作目的地。 這些可能包括發佈至Adobe CX Enterprise的[!DNL Analytics]區段，以及使用Adobe CX Enterprise對象庫建立的區段。

  [!DNL Google Ads]帳戶必須[符合客戶符合](https://support.google.com/adspolicy/answer/6299717)的資格，並且已選擇加入[使用者ID區段](https://support.google.com/google-ads/answer/9199250)。 搜尋、社交和Commerce中的廣告商帳戶也必須設定為允許建立客戶相符對象。 請聯絡您的Adobe客戶團隊以啟用此功能。

  客戶資料型對象的[!DNL Adobe]區段資料和Cookie同步檔案每天都會同步至[!DNL Google Ads]。

* **Adobe Campaign電子郵件清單：**&#x200B;您的Adobe客戶團隊可以協助您設定工作流程，以從[!DNL Campaign]的電子郵件清單建立和更新[!DNL Google Ads]個客戶相符對象。 工作流程是在[!DNL Campaign]中設定，而不是在對象庫中設定。 請參閱&quot;[從Adobe Campaign電子郵件清單](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)建立客戶比對對象。&quot;

* **客戶資料清單：**&#x200B;具有合格[!DNL Google Ads]或[!DNL Microsoft Advertising]帳戶的廣告商，可依據包含其客戶關係管理(CRM)系統之主要識別碼的CSV檔案，使用符合客戶條件的對象。

* **動態再行銷清單：**&#x200B;擁有[!DNL Microsoft Advertising]帳戶的廣告商可以根據最近與其產品互動的使用者來使用對象，例如產品檢視者或過去的購買者。 這些對象需要在相關網頁上使用廣告網路的JavaScript轉換和對象追蹤標籤。

  動態再行銷對象可搭配搜尋和對象網路上的購物行銷活動，以使用產品廣告重新鎖定使用者，並搭配搜尋行銷活動，以使用文字廣告和動態搜尋廣告重新鎖定使用者。

  >[!NOTE]
  >
  >動態再行銷對象目標的競標修飾詞未在具有[!UICONTROL Auto-optimize Bid Adjustment Values]設定的組合中進行最佳化。

>[!NOTE]
>
>搜尋、Social和Commerce不會儲存您上傳的客戶資料，或用來建立或編輯對象的[!DNL Adobe]區段中的客戶資料。

<!--
Restricted to internal beta users: audience creation and library editing.

## Create a customer match audience from a customer data list {#audience-customer-list-create}

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts that are eligible for customer match only*

For [!DNL Microsoft Advertising], the file can include email addresses. For [!DNL Google Ads], the file can include email addresses, mailing addresses, telephone numbers, user IDs, or mobile device IDs.

Creating and editing library audiences requires the [!UICONTROL Edit Audience Library] permission in addition to internal beta access.

1. Prepare a CSV file with the customer data in the required format.

   First and last names, email addresses, and telephone numbers must be hashed using SHA-256. Follow the network's formatting requirements for the selected identifier type. See the [Google Ads formatting guidelines](https://support.google.com/google-ads/answer/7476159) or the [Microsoft Advertising instructions for preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. In **[!UICONTROL Data Source]**, select the customer-list option.

1. Enter the **[!UICONTROL Audience Name]** and select the **[!UICONTROL Data Upload Type]**:

   * ([!DNL Microsoft Advertising]) **[!UICONTROL Emails]**.

   * ([!DNL Google Ads]) **[!UICONTROL Emails, Phones, and/or Mailing Addresses]**, **[!UICONTROL User IDs]**, or **[!UICONTROL Mobile Device IDs]**.

     User ID lists are available only to eligible [!DNL Google Ads] advertisers in the U.S. who are opted in for user ID segments.

1. (Mobile device ID lists only) Select the **[!UICONTROL OS Type]** and enter the **[!UICONTROL App ID]**.

   For an Android app, use its package name in [!DNL Google Play], such as `com.example.game` from `https://play.google.com/store/apps/details?id=com.example.game`. For an iOS app, use its application ID from the [!DNL App Store], such as `id284882215`. Your development team can provide the ID.

1. In **[!UICONTROL Select File]**, select the CSV file from your device or network.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. ([!DNL Google Ads]; optional) If you do business in the European Economic Area (EEA) or United Kingdom (UK) and have collected all required user consents, select the consent check box to send the consent status as **[!UICONTROL GRANTED]** for advertising and ad personalization.

   If you leave the check box unselected, the consent status is sent as **[!UICONTROL UNSPECIFIED]**. [!DNL Google Ads] ignores data for EEA and UK users with an unspecified consent status, which can cause data discrepancies and performance issues.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Membership days specify how long a user's cookie stays in the audience. Use the length of time for which you expect the ad to remain relevant. Customer lists don't expire unless you enter a value.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

The ad network may take up to 24 hours to process the file. See the [Google Ads documentation on customer match and its limitations](https://support.google.com/displayvideo/answer/9539301).

## Create Google Ads customer match audiences from Adobe audiences {#audience-adobe-create}

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

Each [!DNL Adobe] audience can be used for only one [!DNL Google Ads] audience. Each new audience has the same name as the original [!DNL Adobe] audience.

1. Complete the prerequisites:

   1. Ask an [!DNL Adobe] administrator or account manager to enable customer match audiences for the advertiser.

   1. Implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html){target="_blank"} version 2.0 or higher.

   1. Deploy the following tag as high as possible on the advertiser's webpages from which the audience should be tracked:

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      Replace `Advertising_Cloud_UserID` with the advertiser's unique numeric user ID.

   1. Have an authorized user [configure synchronization with the advertiser's organization account in Adobe CX Enterprise](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Google Ads] and the account.

1. In **[!UICONTROL Data Source]**, select the Adobe audience option.

1. In **[!UICONTROL Adobe Audience]**, select one or more available segments. You can search the list.

   Segments already used for another [!DNL Google Ads] audience aren't available. If you select multiple segments, a separate audience is created for each segment.

1. Select the available customer list user ID option in **[!UICONTROL Audience Type]**.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Remarketing lists have a maximum duration of 540 days. Customer lists don't have a maximum duration; enter 10000 to indicate that the cookie never expires.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Search, Social, & Commerce automatically pushes a [!DNL Google] tracking URL back to each source segment so that [!DNL Google] can track the audience. [!DNL Google] may take up to 24 hours to process the audience.

>[!TIP]
>
>For real-time segmentation, use Audience Manager-created audiences. [!DNL Analytics] segments synced to Adobe CX Enterprise may have smaller populations because they're synced daily. Users who qualify for a segment may not be included until the next day.

## Create a Microsoft Advertising dynamic remarketing audience {#audience-dynamic-create}

You can create multiple dynamic remarketing audiences using the same tracking tag.

1. Implement the [Microsoft Advertising universal event tracking (UET) tag with the required product ID and page type parameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) on the relevant webpages. Identify the tag's name.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Microsoft Advertising] and the account.

1. In **[!UICONTROL Data Source]**, select the dynamic remarketing list option.

1. Enter the **[!UICONTROL Audience Name]**.

1. In **[!UICONTROL Tag Name]**, select the UET tag on the webpages whose users comprise the audience.

1. In **[!UICONTROL Whom to add to your audience]**, select **[!UICONTROL General Visitors]**, **[!UICONTROL Product Searchers]**, **[!UICONTROL Product Viewers]**, **[!UICONTROL Past Buyers]**, or **[!UICONTROL Shopping Cart Abandoners]**.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available. For dynamic remarketing audiences, membership can range from 1-180 days.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Dynamic remarketing audiences are eligible for targeting once they include at least 300 users.

## Update a customer match audience using a customer data list {#audience-customer-list-edit}

You can update customer match audiences created from data files, but not [!DNL Google Ads] audiences created from [!DNL Adobe] audiences. You can add or delete members, or replace all existing members. You can't edit multiple library audiences at once.

1. Prepare a CSV file in the required format, using the same data type as the original list. For mobile device IDs, use the same app and operating system.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. In **[!UICONTROL Select Action]**, select:

   * **[!UICONTROL Add]:** Add members from the uploaded file who aren't already in the audience.

   * **[!UICONTROL Delete]:** Remove members in the uploaded file from the audience.

   * **[!UICONTROL Replace]:** Replace all existing audience members with the uploaded data.

1. In **[!UICONTROL Select File]**, select the CSV file, accept the privacy policies, and configure the applicable consent setting.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

The ad network may take a while to process audience updates.

## Edit a dynamic remarketing audience {#audience-dynamic-edit}

You can change a [!DNL Microsoft Advertising] dynamic remarketing audience's name, UET tag, and visitor type. You can't change its membership duration or edit multiple library audiences at once.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one dynamic remarketing audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. Edit the **[!UICONTROL Audience Name]**, **[!UICONTROL Tag Name]**, or **[!UICONTROL Whom to add to your audience]**.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.
-->

## 刪除動態再行銷對象 {#audience-delete}

您可以一次刪除一個[!DNL Microsoft Advertising]動態再行銷對象。 您無法從資料庫中刪除其他[!DNL Google Ads]或[!DNL Microsoft Advertising]對象型別。

1. 在主功能表中，按一下「**[!UICONTROL Targeting]>[!UICONTROL Audiences]**」，然後按一下「**[!UICONTROL Library]**」標籤。

1. 從&#x200B;**[!UICONTROL Network]**&#x200B;功能表選取&#x200B;**[!UICONTROL All Other Network]**。

1. 選取一個動態再行銷對象旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 將選取列中的所有資料複製到剪貼簿 {#copy-to-clipboard}

根據已套用的篩選條件和在檢視中可見的欄，複製所選列中的可見資訊。 資訊會儲存為定位點分隔值(TSV)。

1. 選取要複製其資料的每一列旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Copy]**。

>[!MORELIKETHIS]
>
>* [管理行銷活動和廣告群組的對象目標](audience-targets-manage.md)
>* [管理行銷活動和廣告群組的對象排除](audience-exclusions.md)
