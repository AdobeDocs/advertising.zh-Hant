---
title: （新UI）管理廣告網路帳戶
description: 瞭解如何透過廣告網路API同步的廣告網路在新UI中設定和管理帳戶詳細資訊。
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# （新UI）透過API連線管理廣告網路帳戶

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Beta功能*

<!-- Move out info about Naver into a separate page -->

以下是使用廣告網路的API來管理搜尋、社交和Commerce同步的廣告網路帳戶指示。

<!-- Move out info about Naver into a separate page -->

如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

## 建立廣告網路帳戶詳細資料 {#create-account}

若要啟用帳戶同步，您必須建立包含帳戶存取認證和追蹤選項且狀態為&#x200B;*已啟用*&#x200B;的對應帳戶記錄。

>[!NOTE]
>
>若要在廣告網路上建立實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 按一下&#x200B;**[!UICONTROL Create Account]**。

1. 按一下廣告網路的名稱，然後按一下&#x200B;**[!UICONTROL Next]**。

1. （除[!DNL Yandex]以外的所有廣告網路）使用廣告商的認證登入廣告網路。 選取「此帳戶的帳戶追蹤」選項。 然後，按一下右上角的&#x200B;**[!UICONTROL Next]**。

1. 指定[帳戶設定](#account-settings-api)：

   1. 在&#x200B;**[!UICONTROL Select Accounts]**&#x200B;標籤上，指定一般帳戶設定。 請為[!DNL Yandex]帳戶指定帳戶認證。

   1. 按一下「**[!UICONTROL Setup Tracking]**」標籤，然後輸入追蹤設定。

   1. （具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商）按一下「**[!UICONTROL Set up Adobe Analytics]**」標籤，然後選取所有[!DNL Analytics]報告套裝以用於追蹤和報告行銷活動活動。

1. 按一下&#x200B;**[!UICONTROL Save]**。

   帳戶中所有促銷活動的最近成本和點選資料，會每小時在「搜尋」、「社交」和「Commerce」中更新。 依預設，可使用過去5至10天的資料，視廣告網路而定。 不過，如有必要，專案啟動團隊最多可以擷取過去60天的資料。

## 編輯廣告網路帳戶詳細資料 {#edit-account}

若要重新驗證帳戶設定以重新整理連線或更新許可權、啟用或停用帳戶上的活動、變更帳戶上的預設追蹤引數，或變更[!DNL Analytics]報表套裝以用於追蹤和報告，然後編輯帳戶詳細資料。

>[!NOTE]
>
>若要編輯廣告網路上的實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 以下列任一方式選取該帳戶：

   * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

   * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 編輯[帳戶設定](#account-settings-api)：

   1. （選擇性）在&#x200B;**[!UICONTROL Account Details]**&#x200B;索引標籤上，編輯帳戶詳細資料。

   1. （選用）按一下「**[!UICONTROL Setup Tracking]**」標籤，然後編輯追蹤設定。

   1. （選用；具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商）按一下「**[!UICONTROL Set up Adobe Analytics]**」標籤，然後編輯[!DNL Analytics]報告套裝，以用於追蹤和報告行銷活動活動。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 按一下&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >搜尋、社交和Commerce必須將新帳戶資料與廣告網路上的資料同步。 這會每天自動發生一次，或在Search、Social和Commerce偵測到廣告網路上的變更時更頻繁。

## 重新驗證廣告網路帳戶 {#reauthenticate}

若要重新整理廣告網路連線或更新帳戶的許可權，請重新驗證帳戶。

1. （如果您為同一瀏覽器應用程式中的相同廣告網路登入其他帳戶），請登出廣告商帳戶以外的任何帳戶。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. 以下列任一方式選取該帳戶：

   * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

   * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;標籤上，按一下&#x200B;**[!UICONTROL Re authenticate]**&#x200B;並使用廣告商的認證登入廣告網路。

1. 按一下&#x200B;**[!UICONTROL Save]**。

## 啟用或停用廣告網路帳戶 {#enable-disable-account}

當您啟用廣告網路帳戶時，搜尋、社交和Commerce會與帳戶同步行銷活動資料（若有支援），並針對產品組合中的行銷活動推送自動競標和/或行銷活動預算。 當您停用廣告網路帳戶時，搜尋、社交和Commerce會停止該帳戶上的所有活動。 系統會儲存帳戶作用中時收集的資料，但行銷活動管理檢視和報告不會包含帳戶停用期間的資料。 您稍後可以重新啟用帳戶，以繼續使用該帳戶的活動。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 執行下列任一項作業：

   * （從[!UICONTROL Accounts]檢視）：

      * （若要啟用帳戶）選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Activate]**。

      * （若要停用帳戶）選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Pause]**。

   * （從帳戶設定）：

      1. 以下列任一方式選取該帳戶：

         * 將游標放在帳戶名稱上，按一下&#x200B;**...**，然後按一下&#x200B;**[!UICONTROL Edit]**。

         * 選取帳戶名稱旁的核取方塊，然後按一下大量動作工具列中的&#x200B;**[!UICONTROL Edit]**。

      1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;標籤上，關閉&#x200B;**[!UICONTROL Account enabled]**。

      1. 按一下&#x200B;**[!UICONTROL Save]**。

## 廣告網路帳戶設定 {#account-settings-api}

帳戶設定會依廣告網路而有所不同。 您可能無法看見下列所有設定。

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### [!UICONTROL Select Accounts]/[!UICONTROL Account Details]索引標籤

**[!UICONTROL Account Name]：**&#x200B;要顯示在Search、Social和Commerce中的帳戶名稱。

>[!NOTE]
>
>如果您已整合「搜尋」、「社交」和「Commerce-Adobe Analytics」，並變更搜尋帳戶的名稱，請要求您的Adobe帳戶團隊更新對應。

**[！DNL [廣告網路]帳戶]：** （建立帳戶時可見）要同步的廣告網路帳戶。

**[登入詳細資料]：** （僅限Yandex帳戶）要使用的帳戶認證：

* **[!UICONTROL Login]：**&#x200B;啟用帳戶API存取權的登入名稱或ID。

* **[!UICONTROL Password]：**&#x200B;帳戶的密碼。

* **[!UICONTROL Access Key]：**&#x200B;要使用的開發人員帳戶的存取金鑰。

* **[!UICONTROL Application ID]：**&#x200B;要用於帳戶的開發人員權杖。 所有[!DNL Yandex]帳戶都使用相同的權杖。

* **[!UICONTROL Purse Campaign ID]：** （僅停用[!DNL Yandex]個共用帳戶設定的帳戶；選擇性）促銷活動的數值ID，用於支付帳戶中所有廣告促銷活動。

* **[!UICONTROL Finance Token]：** （[!DNL Yandex]個共用帳戶設定的帳戶僅停用；選擇性）用於財務相關API呼叫的開發人員權杖，例如，根據組合最佳化的需要，在廣告商的促銷活動之間重新配置錢包中的金額。

**[!UICONTROL Network Account ID]：** (除[!DNL Yandex]以外的所有廣告網路廣告網路所指派的帳戶ID。

>[!NOTE]
>
>這裡不支援廣告網路管理員帳戶。 若要識別[!DNL Microsoft Advertising]的管理員帳戶，請分別使用主要帳戶ID或MCC帳戶欄位。 若要[設定 [!DNL Google Ads] 管理員帳戶](/help/search-social-commerce/admin/manager-accounts.md)的認證，請移至[!UICONTROL Admin] \> [!UICONTROL Manager Accounts]。

**[!UICONTROL Currency]：** （唯讀）帳戶所用貨幣的縮寫。 儲存記錄後，此值會自動以廣告網路上的帳戶所設定的貨幣填入。

**[!UICONTROL Time Zone]：**&#x200B;廣告商的時區。 儲存記錄後，此值會自動填入為廣告商的Search、Social和Commerce帳戶設定的時區。

**[!UICONTROL Login]：** （唯讀）用來登入帳戶的使用者帳戶。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]：**&#x200B;搜尋、Social和Commerce會與帳戶同步行銷活動資料（若有支援），並針對產品組合中的行銷活動推送自動競標和/或行銷活動預算。

## [!UICONTROL Setup Tracking]索引標籤

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]：**&#x200B;是否使用Adobe Advertising轉換追蹤服務來啟用追蹤。 此方法會產生唯一的點選追蹤ID，並將使用者重新導向至Adobe Advertising伺服器以供追蹤，然後再傳送至使用者端的登陸頁面。 此方法有預設的追蹤選項，您可以選擇性地加以自訂，您也可以指定要附加至每個URL的引數。

若要啟用此功能，請開啟&#x200B;**[啟用追蹤]**。

>[!NOTE]
>
>* 如果您變更此設定，則必須重新產生帳戶的追蹤URL。
>* 行銷活動層級追蹤選項會覆寫帳戶層級設定。

**[!UICONTROL Tracking Type]：** (啟用搜尋、社交和Commerce追蹤時)將一般使用者重新導向至最終URL或目的地URL的方法。 選取的選項適用於帳戶或行銷活動中的所有競標單位。 預設帳戶層級設定繼承自廣告商的追蹤設定，而預設行銷活動層級設定繼承自帳戶設定。

* *[!UICONTROL Standard]：*&#x200B;若要將一般使用者重新導向至指定的URL。

* *[!UICONTROL Token]：*&#x200B;若要將一般使用者重新導向至URL，並將點選(`ef_id`)的搜尋、社交和Commerce ID記錄為查詢字串引數（用作Token）。 如果您要報告離線交易、希望Search、Social和Commerce與Adobe Analytics交換資料，或希望追蹤[!DNL Apple Safari]瀏覽器內發生的所有轉換，請選擇此選項。

>[!NOTE]
>
>* 如果您從[!UICONTROL Standard]切換至[!UICONTROL Token] （或反之），則必須重新產生帳戶的追蹤URL。
>* 您可以在行銷活動層級覆寫帳戶層級設定。

**[!UICONTROL Auto Update]：** (啟用搜尋、社交和Commerce追蹤時)將追蹤URL標準化，以便跨瀏覽器和伺服器相容。 搜尋、Social和Commerce會在下次同步期間自動將以下內容上傳到廣告網路：(a)追蹤範本的搜尋、Social和Commerce追蹤引數，以及附加至最終URL的相同引數，或(b)內嵌搜尋、Social和Commerce追蹤程式碼的新目的地URL。 對於具有[Adobe Advertising-Adobe Analytics整合](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)和伺服器端AMO ID (s_kwcid)設定的廣告商，上傳也包含您[和](/help/integrations/analytics/ids.md#amo-id)帳戶的[!DNL Google Ads]AMO ID引數[!DNL Microsoft Advertising]。 預設帳戶層級設定繼承自廣告商的追蹤設定。 您可以在行銷活動層級覆寫帳戶層級設定。

追蹤URL只會每天針對不同步的實體更新（亦即已新增的新實體和屬性已變更的現有實體）。 因此，如果您將現有廣告商/帳戶/促銷活動的此設定從「停用」變更為「啟用」，則不會為已同步的現有實體更新追蹤URL。 若要將追蹤新增至現有非同步實體的URL，請連絡您的Adobe客戶團隊，申請一次性手動同步程式。 自動上傳程式將處理未來的變更。

**[!UICONTROL URL Encoding]：** (啟用搜尋、社交和Commerce追蹤時；帳戶僅具有目的地URL)編碼一般使用者瀏覽器位址列中的基底URL （例如`%3D`而非`=`）：

**[!UICONTROL Tracking Level]：** (當搜尋、社交和Commerce追蹤已啟用時；可在帳戶和促銷活動層級使用；不適用於已啟用平行追蹤的廣告網路)應透過新增重新導向（如適用）並將引數附加至相關URL來追蹤點選和收入的層級：

* *[!UICONTROL Keyword]：*&#x200B;只追蹤關鍵字層級的資料。 [!DNL Yandex]無法使用。

* *[!UICONTROL Ad]：*&#x200B;只追蹤廣告層級的資料。 [!DNL Naver]無法使用。

* *[!UICONTROL Keyword and Ad]：*&#x200B;若要同時追蹤關鍵字和廣告層級的資料。 [!DNL Naver]和[!DNL Yandex]無法使用。

**[!UICONTROL Landing Page Suffix]** （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶；選擇性）任何要附加至要追蹤資訊之最終URL結尾的引數；包含您的企業必須追蹤的所有引數。

範例： `param1=value1&param2=value2`

使用Adobe Advertising點選追蹤的帳戶必須在尾碼中包含廣告網路的點選識別碼(`msclkid`為[!DNL Microsoft Advertising]； Google為`gclid`)。 具有Adobe Analytics整合的帳戶必須使用AMO ID引數（以`s_kwcid`開頭）。 如果帳戶具有伺服器端AMO ID實作，則當使用者按一下廣告時，引數會自動新增；否則，您必須在此處手動新增。 檢視[的 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)必要尾碼格式和[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)必要尾碼格式。

>[!NOTE]
>
>* [!UICONTROL Auto Update]追蹤設定未更新此欄位。
>* 較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。

**帳戶追蹤URL**： （僅限[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]帳戶；選擇性）帳戶的預設追蹤範本，會指定所有離登陸網域重新導向和追蹤引數，並將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重新導向。

* 若要內嵌最終URL：

   * （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）如需表示追蹤範本中最終URL的引數清單，請參閱[!DNL Microsoft Advertising]檔案[[!DNL Microsoft Advertising] 中「可用的](https://help.ads.microsoft.com/#apex/3/en/56799)引數」一節中的（[!DNL Google Ads]僅限） [!DNL ValueTrack]檔案[[!DNL Google Ads] 或（](https://support.google.com/google-ads/answer/6305348)僅限）「追蹤範本」引數。

   * （僅限[!DNL Yahoo! Japan Ads]）使用引數`!{lpurl}`來指示登陸頁面URL。

* 您可以選擇加入URL引數以及針對促銷活動定義的任何自訂引數，以&amp;分隔，例如`{lpurl}?matchtype={matchtype}&device={device}`。

* 您可以選擇新增第三方重新導向和追蹤。

* 當行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時，搜尋、社交和Commerce會在您儲存記錄時自動為其自己的重新導向和追蹤代碼加上前置詞。

>[!NOTE]
>
>* 對於[!DNL Google Ads]，請避免使用巨集，這些巨集不會取代來自啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，Adobe帳戶團隊應與客戶支援或實作團隊合作，以新增巨集。
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 如果您在廣告、網站連結或關鍵字層級更新追蹤範本，則會重新提交相關廣告以供檢閱。 您可以在帳戶、行銷活動或廣告群組層級更新追蹤範本，無需重新提交廣告進行核准。

## [!UICONTROL Setup Analytics]索引標籤

**[!UICONTROL Adobe Analytics Report Suite]：** （具有[[!DNL Adobe Analytics for Advertising] 整合](/help/integrations/analytics/overview.md)的廣告商；選用）一或多個Analytics報表套裝，Search、Social和Commerce會將其從廣告網路收集到的資料（包括帳戶的實體分類和點按資料）傳送至這些報表套裝。 此功能僅適用於支援的廣告網路。

若要讓資料顯示在報表套裝中，(a)必須為帳戶設定伺服器端AMO ID功能，或(b)必須啟用&quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot;的廣告商層級設定。 此外，廣告商的[!DNL Analytics]帳戶必須設定為從Search、Social和Commerce接收資料。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

>[!MORELIKETHIS]
>
>* [關於廣告網路帳戶](../ad-network-account-about.md)
>* [管理商家中心帳戶](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [更新 [!DNL Google Ads] 帳戶的s_kwcid追蹤代碼](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
