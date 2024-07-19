---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# 代碼片段

## Google Ads實體的追蹤範本欄位 {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]：** （選用）追蹤範本或追蹤URL，其會指定所有離登陸網域重新導向和追蹤引數，並將最終/登陸頁面URL內嵌於[!DNL ValueTrack]引數中。 範例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重新導向。

針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動為其自己的重新導向和追蹤代碼加上前置詞。

* 如需支援的引數以內嵌最終URL，請參閱支援的 [!DNL ValueTrack] 格式](https://support.google.com/google-ads/answer/6305348)的[[!DNL Google Ads] 檔案。 （前往「可用[!DNL ValueTrack]引數」一節中的「僅限追蹤範本」引數。）

* 您可以選擇加入URL引數以及針對促銷活動定義的任何自訂引數（以&amp;分隔），例如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以選擇新增第三方重新導向和追蹤。

>[!NOTE]
>
>* 避免使用巨集，因為巨集不會取代來自啟用平行追蹤之來源的點選。 如果廣告商必須使用巨集，則Adobe帳戶團隊應與客戶支援或實作團隊合作以新增它們。
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 如果您在廣告、網站連結或關鍵字層級更新追蹤範本，則會重新提交相關廣告以供檢閱。 您可以在帳戶、行銷活動或廣告群組層級更新追蹤範本，無需重新提交廣告進行核准。

## [!DNL Microsoft Advertising]個實體的追蹤範本欄位 {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：** （選用）追蹤範本或追蹤URL，可指定所有離登陸網域重新導向和追蹤引數，並將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重新導向。

針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動為其自己的重新導向和追蹤代碼加上前置詞。

* 如需支援嵌入最終URL的引數，請參閱有關引數的[[!DNL Microsoft Advertising] 檔案，以指示最終URL](https://help.ads.microsoft.com/#apex/3/en/56799)。

* 您可以選擇加入URL引數以及針對促銷活動定義的任何自訂引數（以&amp;分隔），例如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以選擇新增第三方重新導向和追蹤。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 您可以在任何層級更新追蹤範本，無需重新提交廣告進行核准。

## 文字廣告範本 — 說明如何插入動態引數的附註 {#inventory-feed-template-insert-dynamic-parameter}

若要將欄名稱或修飾元群組插入為動態引數，請在輸入欄位中按一下，然後按一下欄清單中的欄名稱或修飾元清單中的[修飾元名稱](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)。 若要插入[!DNL Param1]或[!DNL Param2]變數，請輸入值`{param1:default text}`或`{param2:default text}`，其中「預設文字」為當摘要檔案中的引數欄為廣告列空白時所使用的文字。

## 文字廣告範本 — 說明如何插入廣告自訂程式的附註 {#inventory-feed-template-insert-ad-customizer}

若要插入廣告自訂程式，請使用下列格式，其中`Default text`是當摘要檔案未包含有效值時要插入的選用值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}`，例如`{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}`，例如`{CUSTOMIZER.Discount:10%}`
