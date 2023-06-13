---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---
# Google Ads實體的追蹤範本欄位

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]：** （可選）追蹤範本或追蹤URL，這會指定所有離登陸網域重新導向和追蹤引數，也會將最終/登陸頁面URL內嵌在 [!DNL ValueTrack] 引數。 範例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重新導向。

針對Adobe廣告轉換追蹤，此追蹤會在行銷活動設定包含時套用&quot;[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search、Social和Commerce會自動為自己的重新導向和追蹤程式碼加上前置詞。

* 如需支援的內嵌最終URL的引數，請參閱 [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] 格式](https://support.google.com/google-ads/answer/6305348). (前往「可用」一節中的「僅限追蹤範本」引數 [!DNL ValueTrack] 引數。」)

* 您可以選擇加入URL引數及為促銷活動定義的任何自訂引數，以&amp;分隔，例如 {lpurl}？matchtype={matchtype}裝置(&amp;D){device}.

* 您可以選擇新增協力廠商重新導向和追蹤。

>[!NOTE]
>
>* 避免使用巨集，因為巨集不會取代來自啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，則Adobe帳戶團隊應與客戶支援或實作團隊合作來新增它們。
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 如果您在廣告、網站連結或關鍵字層級更新追蹤範本，則會重新提交相關廣告以供審閱。 您可以在帳戶、行銷活動或廣告群組層級更新追蹤範本，無需重新提交廣告進行核准。
