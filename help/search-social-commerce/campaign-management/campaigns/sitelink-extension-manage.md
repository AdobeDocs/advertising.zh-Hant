---
title: 管理共用的網站連結
description: 瞭解如何建立和管理共用網站連結擴充功能。
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# 管理共用的網站連結

*[!DNL Google Ads]和 [!DNL Microsoft Advertising] 僅限*

為任何已同步處理專案建立及管理帳戶層級的共用網站連結 [!DNL Google Ads] 或 [!DNL Microsoft Advertising] 帳戶來自 [!UICONTROL Extensions] > [!UICONTROL Sitelinks] 資料庫。

## 建立共用的網站連結

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 在資料表格上方的工具列中，按一下 ![建立](/help/search-social-commerce/assets/add.png "建立").

1. 選取廣告網路和帳戶名稱，然後按一下 **[!UICONTROL Continue]**.

1. 輸入 [共用網站連結設定](#shared-sitelink-settings).

1. 按一下 **[!UICONTROL Post]**.

建立網站連結後，您可以 [將其指派給帳戶、行銷活動或廣告群組](sitelink-extension-associate.md).

## 編輯共用的網站連結設定

您可以一次編輯一個共用網站連結。

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 選取要編輯的網站連結旁的核取方塊。

1. 在資料表格上方的工具列中，按一下 ![編輯](/help/search-social-commerce/assets/edit.png "編輯").

1. 編輯 [共用網站連結設定](#shared-sitelink-settings).

1. 按一下 **[!UICONTROL Post]**.

## 刪除共用的網站連結

1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 選取要刪除的每個共用網站連結旁的核取方塊。

   如需選取多個列的秘訣，請參閱「[選取多列](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」

1. 在工具列中，按一下 ![更多](/help/search-social-commerce/assets/more.png "更多") 並選取 **[!UICONTROL Delete]**.

1. 在確認訊息中，按一下 **[!UICONTROL Delete]**.

## 共用網站連結設定 {#shared-sitelink-settings}

如需網站連結不核准的其他原則和原因，請參閱 [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) 和 [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) sitelink擴充功能需求。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]：** 為連結顯示的文字。 最多可包含25個單位元組或12個雙位元組字元。 連結文字在帳戶或行銷活動中必須是唯一的。

>[!NOTE]
>
>([!DNL Google Ads])現有35個字元的文字會顯示在桌上型電腦和平板電腦的廣告中，但不會顯示在行動裝置上。

**[!UICONTROL Status]：** 網站連結的顯示狀態：  *[!UICONTROL Active]* 或 *[!UICONTROL Deleted]* （僅限現有網站連結）。 新網站連結的預設值為 *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1]， [!UICONTROL Description Line 2]：** 搜尋引擎可能顯示在連結文字下方的額外文字。 若要包含說明，請在兩個說明欄位中輸入值。 每個說明欄位最多可包含35個單位元組或17個雙位元組字元。

**[!UICONTROL Start Date]：** （僅具有現有舊版網站連結或無網站連結的行銷活動；選用）網站連結可能在行銷活動中與廣告一起顯示的第一個日期。 新網站連結的預設值為當天。 若要指定未來的開始日期，請以YYYY/MM/DD或M/D/YYYY的格式輸入日期，或按一下並選取日期。

**[!UICONTROL End Date]：** （選用）網站連結在行銷活動中可能連同廣告一起顯示的最後日期。 依預設，網站連結可能會無限期地顯示。 若要指定結束日期，請以YYYY/MM/DD或M/D/YYYY格式輸入日期，或按一下並選取日期。

**[!UICONTROL Mobile Preference]：** （選用）讓網路嘗試向行動裝置使用者（而非桌上型電腦或平板電腦使用者）顯示廣告擴充功能。 預設不會啟用選項，且廣告擴充功能會出現在任何裝置型別上。

>[!NOTE]
>
>網路不保證會在偏好的裝置型別上顯示廣告擴充功能。

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** 搜尋引擎使用者在按一下您的廣告時所前往的登陸頁面URL。 包含任何決定頁面內容的引數。 如果您輸入值，該值會覆寫廣告的基本URL。

儲存記錄後，基本URL會包含為行銷活動或帳戶設定的任何附加引數。

>[!NOTE]
>
>* （具有最終URL的帳戶）基礎URL可能包含登陸頁面網域或子網域內的重新導向，但登陸頁面網域外不得重新導向。 廣告網路會從此URL擷取網域，並為廣告新增任何選用顯示路徑，以建立廣告的顯示URL。
>* ([!DNL Google Ads])行銷活動或廣告群組中的每個網站連結都必須有唯一的登陸頁面，而每個網站連結登陸頁面的內容必須有大約80%的唯一內容。 例如，同一頁面中不能有含有多個錨點連結的網站連結。
>* ([!DNL Google Ads])避免使用巨集，巨集不會取代啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，則Adobe帳戶團隊應與客戶支援或實作團隊合作來新增它們。

**[!UICONTROL Tracking Template]：** （可選）追蹤範本或追蹤URL，這會指定所有離登陸網域重新導向和追蹤引數，也會將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重新導向。

* 針對Adobe廣告轉換追蹤，此追蹤會在行銷活動設定包含時套用&quot;[!UICONTROL EF Redirect]&quot;和&quot;自動上傳&quot;、Search、Social和Commerce會在您儲存記錄時自動為其自己的點選追蹤程式碼加上前置詞。

* 如需支援的內嵌最終URL的引數，請參閱([!DNL Microsoft Advertising] 僅限) [[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799) 或([!DNL Google Ads] 僅限) 「可用」一節中的「僅限追蹤範本」引數 [!DNL ValueTrack] 引數」(在 [[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348).

* 您可以選擇加入URL引數及為促銷活動定義的任何自訂引數，以&amp;分隔，例如 `{lpurl}?matchtype={matchtype}&device={device}`.

* 您可以選擇新增協力廠商重新導向和追蹤。

>[!NOTE]
>
>* 當行銷活動設定包含「[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search、Social和Commerce會自動為自己的重新導向和追蹤程式碼加上前置詞。
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* ([!DNL Google Ads])如果您在網站連結或關鍵字層級更新追蹤範本，則會重新提交相關廣告以供稽核。 您可以在帳戶、行銷活動或廣告群組層級更新追蹤範本，無需重新提交廣告進行核准。
>* ([!DNL Microsoft Advertising])您可以在任何層級更新追蹤範本，無需重新提交廣告進行核准。
>* 對象 [!DNL Google Ads]，請避免使用巨集，這類巨集不會取代來自啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，Adobe帳戶團隊應與客戶支援或實作團隊合作來新增巨集。

>[!MORELIKETHIS]
>
>* [關於網站連結擴充功能](sitelink-extension-about.md)
>* [將共用網站連結與帳戶、行銷活動和廣告群組建立關聯](sitelink-extension-associate.md)
