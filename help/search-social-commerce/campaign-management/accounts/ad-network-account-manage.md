---
title: 管理廣告網路帳戶
description: 瞭解如何設定和管理廣告網路帳戶的帳戶詳細資料。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '2088'
ht-degree: 0%

---

# 管理廣告網路帳戶

以下是建立和編輯廣告網路帳戶詳細資料、重新整理 [!DNL oAuth] 帳號的代號，以及停用帳號。

## 建立廣告網路帳戶詳細資料 {#create-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員和管理員使用者角色*

若要啟用帳戶的同步或追蹤，您必須建立包含帳戶存取認證和追蹤選項以及狀態的對應帳戶記錄 *作用中*. 如需每個廣告網路可用功能的詳細資訊，請參閱「[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md).」

>[!NOTE]
>
>若要在廣告網路上建立實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 指定 [帳戶設定](#account-settings)：

   1. 按一下廣告網路的名稱，然後按一下 **[!UICONTROL Next]**.

   1. 在 **[!UICONTROL Account Details]** 區段，輸入帳戶詳細資料。

      對於使用登入授權型別的廣告網路」[!UICONTROL oAuth]，」允許Search、Social和Commerce使用存取帳戶 [Oauth授權通訊協定](http://tools.ietf.org/html/draft-ietf-oauth-v2-22)：

      1. 輸入 **[!UICONTROL Login]** 帳戶的值，選擇性地輸入密碼，然後按一下 **[!UICONTROL Authenticate]**.

         最佳實務是使用登入來存取帳戶的API。 輸入您想要加密並儲存的密碼，以便Adobe帳戶團隊可視需要重新整理Token。

      1. （如果您未登入廣告商的帳戶）登入廣告商的廣告帳戶。 最佳實務是使用帳戶的API存取憑證。

      1. 在許可權請求/存取畫面中，按一下按鈕以確認許可權。

      1. 在開啟的彈出式視窗中複製驗證字串，並將該字串貼到 **[!UICONTROL oAuth Token]** 欄位。

      1. 指定剩餘的帳戶詳細資料。
   1. 按一下 **[!UICONTROL Set Account Tracking]**，並輸入追蹤設定。


1. 按一下 **[!UICONTROL Post]**.

   Search、Social和Commerce可在約24小時內提供帳戶中所有促銷活動的最新成本和點選資料。 依預設，可使用過去5-10天的資料，視廣告網路而定。 不過，如有必要，專案啟動團隊最多可擷取過去60天的資料。

## 編輯廣告網路帳戶詳細資料 {#edit-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員和管理員使用者角色*

如果帳戶認證變更，您想要變更整個帳戶的預設追蹤引數，或者想要啟用或停用帳戶的活動，然後編輯帳戶詳細資料。

>[!NOTE]
>
>若要編輯廣告網路上的實際帳戶，請前往廣告網路的網站。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 將游標停留在帳戶名稱上，按一下 ![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然後選取 **[!UICONTROL Edit]**.

1. 編輯 [帳戶設定](#account-settings)：

   1. （選用）編輯帳戶詳細資料。

   1. （可選）按一下 **[!UICONTROL Set Account Tracking]**，並編輯追蹤設定。

1. 按一下 **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >搜尋、Social和Commerce必須將新帳戶資料與廣告網路上的資料同步。 這會每天自動發生一次，或在Search、Social和Commerce偵測到廣告網路上的變更時更常發生。

## 重新整理搜尋帳戶的oAuth存取權杖 {#refresh-oauth-tokens}

*僅限代理商帳戶管理員、Adobe帳戶管理員和管理員使用者角色*

如果Search、Social和Commerce使用存取該帳戶 [Oauth授權通訊協定](http://tools.ietf.org/html/draft-ietf-oauth-v2-22) 和帳戶認證變更，或需要其他存取權杖才能支援Search、Social和Commerce的新功能，則您必須取得帳戶的新存取權杖。

如果您的新功能需要新的Token，您的Adobe帳戶團隊將會通知您。

1. （如果您已登入相同瀏覽器應用程式中相同廣告網路的其他帳戶）登出廣告商帳戶以外的任何帳戶。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 將游標停留在帳戶名稱上，按一下 ![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然後選取 **[!UICONTROL Edit]**.

1. 取得新的存取Token：

   1. 按一下 **[!UICONTROL Get oAuth Token]**.

   1. （如果您未登入廣告商的帳戶）登入廣告商的廣告帳戶。 最佳實務是使用帳戶的API存取憑證。

   1. 在許可權請求/存取畫面中，按一下按鈕以確認許可權。

   1. 在開啟的彈出式視窗中複製驗證字串，並將該字串貼到 **[!UICONTROL oAuth Token]** 欄位。

1. 按一下 **[!UICONTROL Post]**.

## 啟用或停用廣告網路帳戶 {#enable-disable-account}

*僅限代理商帳戶管理員、Adobe帳戶管理員和管理員使用者角色*

當您啟用廣告網路帳戶時，Search、Social和Commerce會與帳戶同步促銷活動資料（若有支援），並針對產品組合中的促銷活動推送自動競標和/或促銷活動預算。當您停用廣告網路帳戶時，Search、Social和Commerce會停止該帳戶上的所有活動。 系統仍會儲存帳戶作用中時收集的資料，但行銷活動管理檢視和報告不包含帳戶停用期間的資料。 您稍後可以重新啟用帳戶，以繼續使用該帳戶的活動。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 執行下列任一項作業：

   * （若要變更單一帳戶的狀態）將游標停留在帳戶名稱上，請按一下 ![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然後選取 **[!UICONTROL Edit]**. 變更 **[!UICONTROL Status]** 至 *已啟用* 或 *已停用*，然後按一下 **[!UICONTROL Post]**.

   * （若要變更一或多個帳號的狀態），請執行下列動作：

      1. 選取每個帳戶旁的核取方塊。

         如需選取多個列的秘訣，請參閱「[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

      1. 在資料表格上方的工具列中，按一下 ![啟動圖示](/help/search-social-commerce/assets/activate.png "啟動圖示") 若要啟用帳戶或 ![停用圖示](/help/search-social-commerce/assets/disable.png "停用圖示") 以停用帳戶。

## 廣告網路帳戶設定 {#account-settings}

>[!NOTE]
>
>僅限代理商客戶經理， [!DNL Adobe] 帳戶管理員和管理員使用者可以設定帳戶設定。

### 帳戶詳細資料

**[!UICONTROL SE Account ID]：** (除以下專案外的所有帳戶： [!DNL Naver] 和 [!DNL Yandex] 帳戶；僅新帳戶可編輯)廣告網路所指派的帳戶ID。

>[!NOTE]
>
>此處不支援廣告網路管理員帳戶。 識別經理帳戶的方式 [!DNL Microsoft Advertising] 或 [!DNL Yandex]，分別使用主要帳戶ID或MCC帳戶欄位。 至 [設定認證 [!DNL Google Ads] 經理帳戶](/help/search-social-commerce/admin/manager-accounts.md)，前往 [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]：** 要在Search、Social和Commerce中為帳戶顯示的名稱。

>[!NOTE]
>
>如果您整合了Search、Social和Commerce-Adobe Analytics，並變更了搜尋帳戶的名稱，然後通知您的Adobe帳戶團隊，讓他們可以更新對應。

**[!UICONTROL Login Details]： \[登入型別\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] 僅限)是否授權以下使用者登入帳戶：

* *[!UICONTROL oAuth]* （預設）：若要使用 [[!DNL OAuth] 授權通訊協定](http://tools.ietf.org/html/draft-ietf-oauth-v2-22).

* *[!UICONTROL Password]：* 使用使用者端的密碼。

對象 [!DNL Microsoft Advertising] 帳戶，僅限 [!DNL oAuth]-authorized logins可以使用。

**[!UICONTROL Login Details]： [!UICONTROL Login]：** (所有廣告網路，除了 [!DNL Naver])可啟用帳戶API存取權的登入名稱或ID。

**[!UICONTROL Login Details]： [!UICONTROL OAuth Token]：** ([!DNL Microsoft Advertising] [!DNL oAuth]-enabled和其他所有網路，除了 [!DNL Baidu]， [!DNL Meta]、和 [!DNL Yandex])帳戶的Token，可授權使用 [[!DNL OAuth] 授權通訊協定](http://tools.ietf.org/html/draft-ietf-oauth-v2-22).

**[!UICONTROL Login Details]： [!UICONTROL Password]：** (所有廣告網路，除了 [!DNL Naver])帳戶的密碼。 對於上的啟用密碼的帳戶 [!DNL Baidu]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex]，此欄位為必填欄位。 對象 [!DNL oAuth]-enabled帳號，此欄位是選用欄位；當您想要加密並儲存密碼時，請使用該欄位，以便帳號管理員視需要重新整理Token。

**[!UICONTROL Login Details]： [!UICONTROL Access Key]：** ([!DNL Baidu] 和 [!DNL Yandex] 僅限帳戶)要使用的開發人員帳戶存取金鑰。

**[!UICONTROL Currency]：** 用於帳戶的貨幣縮寫。 此欄位可針對新欄位進行編輯 [!DNL Naver] 帳戶。 對於所有其他搜尋網路，當您儲存記錄後，系統會以廣告網路上為帳戶設定的貨幣自動填入值。

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] 僅限accounts；選用)任何要附加至最終URL結尾以追蹤資訊的引數；包含您的企業必須追蹤的所有引數。

範例： `param1=value1&param2=value2`

使用Adobe廣告點選追蹤的帳戶必須包含廣告網路的點選識別碼(`msclkid` 的 [!DNL Microsoft Advertising]； `gclid` (適用於Google)。 與Adobe Analytics整合的帳戶必須使用 `s_kwcid` 引數。 如果帳戶有伺服器端s\_kwcid實施，則當使用者按一下廣告時，引數會自動新增；否則，您必須在此處手動新增。 請參閱 [必要的字尾格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) 和 [必要的字尾格式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* 此欄位未由 [!UICONTROL Auto Upload] 追蹤設定。
>* 較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同的追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。


**時區：** (所有廣告網路，但不包括 [!DNL Baidu] 和 [!DNL Yahoo! Display Network])廣告商的時區。 此欄位可編輯，且是新欄位的選用欄位 [!DNL Naver] 帳戶。 對於所有其他搜尋網路，當您儲存記錄後，系統會以廣告商的搜尋、社交和商務帳戶設定的時區自動填入值。

**狀態：** Search、Social和Commerce中的帳戶狀態：

* *已啟用：* 搜尋、Social和Commerce會與帳戶同步促銷活動資料（若有支援），並針對產品組合中的促銷活動推送自動競標和/或促銷活動預算。
* *已停用：* 搜尋、社交和商務會停止帳戶上的所有活動。 系統仍會儲存帳戶作用中時收集的資料，但行銷活動管理檢視和報告不包含帳戶暫停期間的資料。 您稍後可以重新啟用帳戶，以繼續使用該帳戶的活動。

**追蹤範本** - ([!DNL Google Ads]， [!DNL Microsoft Advertising]、和 [!DNL Yahoo! Japan Ads] 僅限帳戶；選用)帳戶的預設追蹤範本，這會指定所有離登陸網域重新導向和追蹤引數，也會將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重新導向。

* 若要內嵌最終URL：

   * ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] 如需指出追蹤範本中最終URL的引數清單，請參閱([!DNL Microsoft Advertising] 僅限) [[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799) 或([!DNL Google Ads] 僅限) 「可用ValueTrack引數」一節中的「僅限追蹤範本」引數。 [[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] 僅限)使用引數 `!{lpurl}` 以指出登入頁面URL。

* 您可以選擇加入URL引數及為促銷活動定義的任何自訂引數，以&amp;分隔，例如 `{lpurl}?matchtype={matchtype}&device={device}`.

* 您可以選擇新增協力廠商重新導向和追蹤。

* 當行銷活動設定包含「[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search、Social和Commerce會自動為自己的重新導向和追蹤程式碼加上前置詞。

>[!NOTE]
>
>* 對象 [!DNL Google Ads]，請避免使用巨集，這類巨集不會取代來自啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，Adobe帳戶團隊應與客戶支援或實作團隊合作來新增巨集。
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 如果您在廣告、網站連結或關鍵字層級更新追蹤範本，則會重新提交相關廣告以供審閱。 您可以在帳戶、行銷活動或廣告群組層級更新追蹤範本，無需重新提交廣告進行核准。


**[!UICONTROL Master Account ID]：** ([!DNL Microsoft Advertising] 僅限帳戶)與帳戶相關聯之機構/管理帳戶的ID。

**[!UICONTROL MCC Account]：** ([!DNL Yandex] 僅限帳戶；選擇性)與帳戶相關聯的機構/管理帳戶。 若要移除現有的關聯，請選取「[!UICONTROL No MCC Account].」

**[!UICONTROL Application ID]：** ([!DNL Yandex] 僅限帳戶)用於帳戶的開發人員權杖。 相同的Token用於所有 [!DNL Yandex] 帳戶。

**[!UICONTROL Purse Campaign ID]：** ([!DNL Yandex] 僅限已停用「共用帳戶」設定的帳戶；選用)促銷活動的數值ID，將用於支付帳戶中所有廣告促銷活動的費用。

**[!UICONTROL Finance Token]：** ([!DNL Yandex] 僅停用「共用帳戶」設定的帳戶；選用)用於財務相關API呼叫的開發人員Token，例如，根據組合最佳化的需要，在廣告商的行銷活動之間重新分配錢包中的資金。

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

**[!UICONTROL Track Product Group]：** (適用於 [!UICONTROL EF Redirect] 僅限)未實作

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S\_kwcid格式** - (現有 [!DNL Google Ads] 具有Advertising-Adobe Analytics整合Adobe且尚未移轉s\_kwcid的廣告商帳戶)

此帳戶使用舊版的s\_kwcid追蹤程式碼格式，可讓Adobe廣告與Adobe Analytics共用帳戶的相關資料。 此 [最新格式](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) 包含行銷活動ID和廣告群組ID的引數，這些引數對於在行銷活動和廣告群組層級準確報告是必要的 [!DNL Google Ads] Analytics中的最高成效行銷活動，以及草稿和實驗行銷活動：

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

如果此帳戶需要在行銷活動和廣告群組層級報告，則按一下 [!UICONTROL Edit] （鉛筆）圖示然後 **[!UICONTROL Migrate to new s\_kwcid format]** 以變更為新格式。 對於不包含這些促銷活動型別的帳戶，可選擇性移轉至新格式，但建議這麼做。

如需完整指示，請參閱&quot;[更新的s\_kwcid追蹤程式碼 [!DNL Google Ads] 帳戶](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).」

**報表套裝名稱** - (僅適用於具有權杖的EF重新導向；具有AdobeAdvertising-Adobe Analytics整合的廣告商；選用)一或多個Analytics報表套裝，Search、Social和Commerce會將其從廣告網路收集到的資料（包括帳戶的實體分類和點選資料）傳送至這些報表套裝。 此功能僅適用於支援的廣告網路。

若要讓資料顯示在報表套裝中，(a)必須為帳戶設定伺服器端s\_kwcid，或(b)將廣告商層級設定為&quot;[!UICONTROL Enable tracking for SAINT feeds]必須啟用「」。 此外，廣告商的Analytics帳戶必須設定為從Search、Social和Commerce接收資料。 如需詳細資訊，請聯絡您的Adobe客戶經理。

>[!MORELIKETHIS]
>
>* [關於廣告網路帳戶](ad-network-account-about.md)
>* [管理商家中心帳戶](merchant-account-manage.md)
>* [更新的s\_kwcid追蹤程式碼 [!DNL Google Ads] 帳戶](update-skwcid-google.md)
