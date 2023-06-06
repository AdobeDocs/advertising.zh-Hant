---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---
# 代碼片段

## Google Ads實體的追蹤範本欄位 {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]：** （可選）追蹤範本或追蹤URL，這會指定所有離登陸網域重新導向和追蹤引數，也會將最終/登陸頁面URL內嵌在 [!DNL ValueTrack] 引數。 範例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重新導向。

針對Adobe廣告轉換追蹤，此追蹤會在行銷活動設定包含時套用&quot;[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search、Social和Commerce會自動為自己的重新導向和追蹤程式碼加上前置詞。

* 如需支援的內嵌最終URL的引數，請參閱 [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] 格式](https://support.google.com/google-ads/answer/6305348). （前往「可用ValueTrack引數」一節中的「僅限追蹤範本」引數。）

* 您可以選擇性地包含URL引數以及針對促銷活動定義的任何自訂引數（以&amp;分隔），例如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以選擇新增協力廠商重新導向和追蹤。

>[!NOTE]
>
>* 避免使用巨集，因為巨集不會取代來自啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，則Adobe帳戶團隊應與客戶支援或實作團隊合作來新增它們。
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 如果您在廣告、網站連結或關鍵字層級更新追蹤範本，則會重新提交相關廣告以供審閱。 您可以在帳戶、行銷活動或廣告群組層級更新追蹤範本，無需重新提交廣告進行核准。


## Microsoft Advertising實體的追蹤範本欄位 {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：** （可選）追蹤範本或追蹤URL，這會指定所有離登陸網域重新導向和追蹤引數，也會將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重新導向。

針對Adobe廣告轉換追蹤，此追蹤會在行銷活動設定包含時套用&quot;[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search、Social和Commerce會自動為自己的重新導向和追蹤程式碼加上前置詞。

* 如需支援的內嵌最終URL的引數，請參閱 [[!DNL Microsoft Advertising] 指示最終URL之引數的相關檔案](https://help.ads.microsoft.com/#apex/3/en/56799).

* 您可以選擇性地包含URL引數以及針對促銷活動定義的任何自訂引數（以&amp;分隔），例如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以選擇新增協力廠商重新導向和追蹤。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 您可以在任何層級更新追蹤範本，而無需重新提交廣告進行核准。


## 文字和範本 — 說明如何插入動態引數的附註 {#inventory-feed-template-insert-dynamic-parameter}

若要將欄名稱或修飾元群組插入為動態引數，請在輸入欄位中按一下，然後按一下欄清單中的欄名稱或 [修飾元名稱](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) 在修飾詞清單中。 若要插入 [!DNL Param1] 或 [!DNL Param2] 變數，輸入值 `{param1:default text}` 或 `{param2:default text}`，其中「預設文字」是當摘要檔案中的引數欄對於廣告列而言為空時所使用的文字。

## 文字廣告範本 — 說明如何插入廣告自訂程式的附註 {#inventory-feed-template-insert-ad-customizer}

若要插入廣告自訂程式，請使用以下格式，其中 `Default text` 是當摘要檔案未包含有效值時要插入的選用值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`
