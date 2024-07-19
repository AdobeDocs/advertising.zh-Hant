---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Microsoft Advertising實體的追蹤範本欄位

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：** （選用；不適用於所有實體）追蹤範本或追蹤URL，這會指定所有離登陸網域重新導向和追蹤引數，並將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重新導向。

針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動為其自己的重新導向和追蹤代碼加上前置詞。

* 如需支援嵌入最終URL的引數，請參閱有關引數的[[!DNL Microsoft Advertising] 檔案，以指示最終URL](https://help.ads.microsoft.com/#apex/3/en/56799)。

* 您可以選擇加入URL引數以及針對促銷活動定義的任何自訂引數（以&amp;分隔），例如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以選擇新增第三方重新導向和追蹤。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 您可以在任何層級更新追蹤範本，無需重新提交廣告進行核准。
