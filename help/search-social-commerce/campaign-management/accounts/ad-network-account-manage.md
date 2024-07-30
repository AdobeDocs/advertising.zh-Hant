---
title: 管理廣告網路帳戶
description: 瞭解如何設定及管理廣告網路帳戶的帳戶詳細資料。
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 68efad8ad3bc2985ac75a0f9437a2eafb194e4b6
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# 管理廣告網路帳戶

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

以下為建立和編輯廣告網路帳戶詳細資料、重新整理帳戶的[!DNL oAuth]權杖以及停用帳戶的指示。

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

## 建立廣告網路帳戶詳細資料 {#create-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員及系統管理員使用者角色*

若要啟用帳戶的同步或追蹤，您必須建立包含帳戶存取認證和追蹤選項且狀態為&#x200B;*作用中*&#x200B;的對應帳戶記錄。

>[!NOTE]
>
>* 新[!DNL Baidu]帳戶不提供支援。
>* 若要在廣告網路上建立實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 在資料表上方的工具列中，按一下![建立](/help/search-social-commerce/assets/add.png "建立")。

1. 指定[帳戶設定](#account-settings)：

   1. 按一下廣告網路的名稱，然後按一下&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;區段中，輸入帳戶詳細資料。

      針對使用登入授權型別&quot;[!UICONTROL oAuth]&quot;的廣告網路，允許Search、Social和Commerce使用[OAuth授權通訊協定](https://oauth.net/2/)存取帳戶：

      1. 輸入帳戶的&#x200B;**[!UICONTROL Login]**&#x200B;值，選擇性地輸入密碼，然後按一下&#x200B;**[!UICONTROL Authenticate]**。

         最佳實務是使用登入對帳戶進行API存取。 當您想要加密並儲存密碼時，請輸入密碼，以便Adobe帳戶團隊可視需要重新整理權杖。

      1. （如果您未登入廣告商的帳戶）登入廣告商的廣告帳戶。 最佳實務是使用認證來存取帳戶的API。

      1. 在許可權請求/存取畫面中，按一下按鈕以確認許可權。

      1. 在開啟的快顯視窗中複製驗證字串，並將該字串貼到&#x200B;**[!UICONTROL oAuth Token]**&#x200B;欄位中。

      1. 指定剩餘的帳戶詳細資料。

   1. 按一下&#x200B;**[!UICONTROL Set Account Tracking]**，然後輸入追蹤設定。

1. 按一下&#x200B;**[!UICONTROL Post]**。

   帳戶中所有促銷活動的最近成本和點選資料，可在大約24小時內從Search、Social和Commerce取得。 依預設，可使用過去5至10天的資料，視廣告網路而定。 不過，如有必要，專案啟動團隊最多可以擷取過去60天的資料。

## 編輯廣告網路帳戶詳細資料 {#edit-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員及系統管理員使用者角色*

如果帳戶認證變更，您想要變更整個帳戶的預設追蹤引數，或想要啟用或停用帳戶的活動，然後編輯帳戶詳細資料。

>[!NOTE]
>
>若要編輯廣告網路上的實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 將游標放在帳戶名稱上，按一下![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然後選取&#x200B;**[!UICONTROL Edit]**。

1. 編輯[帳戶設定](#account-settings)：

   1. （選用）編輯帳戶詳細資料。

   1. （選用）按一下「**[!UICONTROL Set Account Tracking]**」並編輯追蹤設定。

1. 按一下&#x200B;**[!UICONTROL Post]**。

   >[!NOTE]
   >
   >搜尋、社交和Commerce必須將新帳戶資料與廣告網路上的資料同步。 這會每天自動發生一次，或在Search、Social和Commerce偵測到廣告網路上的變更時更頻繁。

## 重新整理搜尋帳戶的oAuth存取權杖 {#refresh-oauth-tokens}

*僅限代理商帳戶管理員、Adobe帳戶管理員及系統管理員使用者角色*

如果「搜尋」、「社交」和「Commerce」使用[OAuth授權通訊協定](https://oauth.net/2/)存取帳戶，且帳戶認證變更，或需要其他存取權來支援「搜尋」、「社交」和「Commerce」的新功能，則您必須取得帳戶的新存取權杖。

如果您的新功能需要新的Token，您的Adobe帳戶團隊將會通知您。

1. （如果您為同一瀏覽器應用程式中的相同廣告網路登入其他帳戶），請登出廣告商帳戶以外的任何帳戶。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 將游標放在帳戶名稱上，按一下![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然後選取&#x200B;**[!UICONTROL Edit]**。

1. 取得新的存取Token：

   1. 按一下&#x200B;**[!UICONTROL Get oAuth Token]**。

   1. （如果您未登入廣告商的帳戶）登入廣告商的廣告帳戶。 最佳實務是使用認證來存取帳戶的API。

   1. 在許可權請求/存取畫面中，按一下按鈕以確認許可權。

   1. 在開啟的快顯視窗中複製驗證字串，並將該字串貼到&#x200B;**[!UICONTROL oAuth Token]**&#x200B;欄位中。

1. 按一下&#x200B;**[!UICONTROL Post]**。

## 啟用或停用廣告網路帳戶 {#enable-disable-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員及系統管理員使用者角色*

當您啟用廣告網路帳戶時，搜尋、社交和Commerce會與帳戶同步促銷活動資料（若有支援），並針對產品組合中的促銷活動推送自動競標和/或促銷活動預算。當您停用廣告網路帳戶時，搜尋、社交和Commerce會停止帳戶上的所有活動。 系統會儲存帳戶作用中時收集的資料，但行銷活動管理檢視和報告不會包含帳戶停用期間的資料。 您稍後可以重新啟用帳戶，以繼續使用該帳戶的活動。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 執行下列任一項作業：

   * （若要變更單一帳戶的狀態）將游標放在帳戶名稱上，按一下![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然後選取&#x200B;**[!UICONTROL Edit]**。 將&#x200B;**[!UICONTROL Status]**&#x200B;變更為&#x200B;*已啟用*&#x200B;或&#x200B;*已停用*，然後按一下&#x200B;**[!UICONTROL Post]**。

   * （若要變更一或多個帳戶的狀態），請執行下列動作：

      1. 選取每個帳戶旁的核取方塊。

         如需選取多個列的秘訣，請參閱[選取多個列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)。

      1. 在資料表上方的工具列中，按一下![啟動圖示](/help/search-social-commerce/assets/activate.png "啟動圖示")以啟用帳戶，或按一下![「停用」圖示](/help/search-social-commerce/assets/disable.png "「停用」圖示")以停用帳戶。

## 廣告網路帳戶設定 {#account-settings}

>[!NOTE]
>
>只有機構帳戶管理員、[!DNL Adobe]帳戶管理員和管理員使用者可以設定帳戶設定。

### 帳戶詳細資料

**[!UICONTROL SE Account ID]：** （除[!DNL Naver]和[!DNL Yandex]帳戶以外的所有帳戶；僅可針對新帳戶編輯）廣告網路所指派的帳戶ID。

>[!NOTE]
>
>這裡不支援廣告網路管理員帳戶。 若要識別[!DNL Microsoft Advertising]或[!DNL Yandex]的管理員帳戶，請分別使用主要帳戶ID或MCC帳戶欄位。 若要[設定 [!DNL Google Ads] 管理員帳戶](/help/search-social-commerce/admin/manager-accounts.md)的認證，請移至[!UICONTROL Admin] \> [!UICONTROL Manager Accounts]。

**[!UICONTROL Account Name]：**&#x200B;要顯示在Search、Social和Commerce中的帳戶名稱。

>[!NOTE]
>
>如果您已整合「搜尋」、「社交」和「Commerce-Adobe Analytics」，並變更搜尋帳戶的名稱，然後通知您的Adobe帳戶團隊，讓他們可以更新對應。

**[!UICONTROL Login Details]： \[登入型別\]** - （僅限[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center]）是否授權使用下列專案登入帳戶：

* *[!UICONTROL oAuth]* （預設值）：若要使用[[!DNL OAuth] 授權通訊協定](https://oauth.net/2/)。

* *[!UICONTROL Password]：*&#x200B;若要使用使用者端的密碼。

對於[!DNL Microsoft Advertising]帳戶，只能使用[!DNL oAuth]授權的登入。

**[!UICONTROL Login Details]： [!UICONTROL Login]：** （除[!DNL Naver]以外的所有廣告網路）可啟用帳戶API存取的登入名稱或ID。

**[!UICONTROL Login Details]： [!UICONTROL OAuth Token]：** （[!DNL Microsoft Advertising] [!DNL oAuth]已啟用，以及[!DNL Meta]和[!DNL Yandex]以外的所有其他網路）使用[[!DNL OAuth] 授權通訊協定](https://oauth.net/2/)授權登入的帳戶權杖。

**[!UICONTROL Login Details]： [!UICONTROL Password]：** （除[!DNL Naver]以外的所有廣告網路）帳戶的密碼。 對於[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]和[!DNL Yandex]上啟用密碼的帳戶，此欄位是必要的。 對於已啟用[!DNL oAuth]的帳戶，此欄位是選擇性的；當您想要加密並儲存密碼以便帳戶管理員視需要重新整理權杖時，請使用它。

**[!UICONTROL Login Details]： [!UICONTROL Access Key]：** （僅限[!DNL Yandex]個帳戶）要使用的開發人員帳戶的存取金鑰。

**[!UICONTROL Currency]：**&#x200B;帳戶所用貨幣的縮寫。 此欄位可供新[!DNL Naver]帳戶編輯。 對於所有其他搜尋網路，當您儲存記錄後，系統會以廣告網路上為帳戶設定的貨幣自動填入值。

**[!UICONTROL Landing Page Suffix]** （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶；選擇性）任何要附加至要追蹤資訊之最終URL結尾的引數；包含您的企業必須追蹤的所有引數。

範例： `param1=value1&param2=value2`

使用Adobe Advertising點選追蹤的帳戶必須在尾碼中包含廣告網路的點選識別碼([!DNL Microsoft Advertising]為`msclkid`； Google為`gclid`)。 具有Adobe Analytics整合的帳戶必須使用AMO ID引數（以`s_kwcid`開頭）。 如果帳戶具有伺服器端AMO ID實作，則當使用者按一下廣告時，引數會自動新增；否則，您必須在此處手動新增。 檢視 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)的[必要尾碼格式和 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)的[必要尾碼格式。

>[!NOTE]
>
>* [!UICONTROL Auto Upload]追蹤設定未更新此欄位。
>* 較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。

**時區：** （除[!DNL Baidu]和[!DNL Yahoo! Display Network]以外的所有廣告網路）廣告商的時區。 此欄位可供新[!DNL Naver]帳戶編輯及選用。 對於所有其他搜尋網路，當您儲存記錄後，系統會以廣告商的搜尋、社交和Commerce帳戶設定的時區自動填入值。

**狀態：**&#x200B;搜尋、社交和Commerce中的帳戶狀態：

* *已啟用：*&#x200B;搜尋、社交和Commerce會與帳戶同步行銷活動資料（若有支援），並針對產品組合中的行銷活動推送自動競標和/或行銷活動預算。
* *已停用：*&#x200B;搜尋、社交和Commerce已停止帳戶上的所有活動。 系統會儲存帳戶作用中時收集的資料，但行銷活動管理檢視和報告不會包含帳戶暫停期間的資料。 您稍後可以重新啟用帳戶，以繼續使用該帳戶的活動。

**追蹤範本** - （僅限[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]帳戶；選擇性）帳戶的預設追蹤範本，會指定所有離登陸網域重新導向和追蹤引數，並將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重新導向。

* 若要內嵌最終URL：

   * （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）如需表示追蹤範本中最終URL的引數清單，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348)中「可用的[!DNL ValueTrack]引數」一節中的（[!DNL Microsoft Advertising]僅限） [[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799)或（[!DNL Google Ads]僅限）「追蹤範本」引數。

   * （僅限[!DNL Yahoo! Japan Ads]）使用引數`!{lpurl}`來指示登陸頁面URL。

* 您可以選擇加入URL引數以及針對促銷活動定義的任何自訂引數，以&amp;分隔，例如`{lpurl}?matchtype={matchtype}&device={device}`。

* 您可以選擇新增第三方重新導向和追蹤。

* 當行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時，搜尋、社交和Commerce會在您儲存記錄時自動為其自己的重新導向和追蹤代碼加上前置詞。

>[!NOTE]
>
>* 對於[!DNL Google Ads]，請避免使用巨集，這些巨集不會取代來自啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，Adobe帳戶團隊應與客戶支援或實作團隊合作以新增巨集。
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 如果您在廣告、網站連結或關鍵字層級更新追蹤範本，則會重新提交相關廣告以供檢閱。 您可以在帳戶、行銷活動或廣告群組層級更新追蹤範本，無需重新提交廣告進行核准。

**[!UICONTROL Master Account ID]：** （僅限[!DNL Microsoft Advertising]個帳戶）與帳戶關聯的機構/管理帳戶識別碼。

**[!UICONTROL MCC Account]：** （僅限[!DNL Yandex]個帳戶；選擇性）與該帳戶關聯的機構/管理帳戶。 若要移除現有的關聯，請選取&quot;[!UICONTROL No MCC Account]&quot;。

**[!UICONTROL Application ID]：** （僅限[!DNL Yandex]個帳戶）要用於帳戶的開發人員權杖。 所有[!DNL Yandex]帳戶都使用相同的權杖。

**[!UICONTROL Purse Campaign ID]：** （僅停用[!DNL Yandex]個共用帳戶設定的帳戶；選擇性）促銷活動的數值ID，用於支付帳戶中所有廣告促銷活動。

**[!UICONTROL Finance Token]：** （[!DNL Yandex]個共用帳戶設定的帳戶僅停用；選擇性）用於財務相關API呼叫的開發人員權杖，例如，根據組合最佳化的需要，在廣告商的促銷活動之間重新配置錢包中的金額。

### 帳戶追蹤

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]：** （僅適用於[!UICONTROL EF Redirect]）未實作

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid格式：** (現有[!DNL Google Ads]帳戶是具有Adobe Advertising-Adobe Analytics整合且尚未移轉AMO ID (s_kwcid)的廣告商)

此帳戶使用舊版的AMO ID追蹤程式碼格式，可讓Adobe Advertising與Adobe Analytics共用帳戶的相關資料。 [最新格式](/help/integrations/analytics/ids.md#amo-id-formats)包含行銷活動ID和廣告群組ID的引數，這些引數對於在Analytics中[!DNL Google Ads]最高成效行銷活動以及草稿和實驗行銷活動的行銷活動和廣告群組層級進行準確報告是必要的：

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

如果此帳戶需要在行銷活動和廣告群組層級報告，請按一下[!UICONTROL Edit] （鉛筆）圖示，然後再按一下&#x200B;**[!UICONTROL Migrate to new s_kwcid format]**&#x200B;以變更為新格式。 對於不包含這些行銷活動型別的帳戶，可選擇性移轉至新格式，但建議這麼做。

如需完整指示，請參閱[更新 [!DNL Google Ads] 帳戶](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)的AMO ID追蹤代碼。

**報表套裝名稱：** (僅適用於具有權杖的EF重新導向；具有Adobe Advertising-Adobe Analytics整合的廣告商；選用)一或多個Analytics報表套裝，Search、Social和Commerce會將其從廣告網路收集到的資料（包括帳戶的實體分類和點選資料）傳送至這些報表套裝。 此功能僅適用於支援的廣告網路。

若要讓資料顯示在報表套裝中，(a)必須為帳戶設定伺服器端AMO ID功能，或(b)必須啟用&quot;[!UICONTROL Enable tracking for SAINT feeds]&quot;的廣告商層級設定。 此外，廣告商的Analytics帳戶必須設定為可從Search、Social和Commerce接收資料。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

>[!MORELIKETHIS]
>
>* [關於廣告網路帳戶](ad-network-account-about.md)
>* [管理商家中心帳戶](merchant-account-manage.md)
>* [更新 [!DNL Google Ads] 帳戶的s_kwcid追蹤代碼](update-amo-id-google.md)
