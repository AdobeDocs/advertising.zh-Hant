---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Microsoft Advertising實體的追蹤範本欄位

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：** （選用；不適用於所有實體）追蹤範本或追蹤URL，可指定所有離登陸網域重新導向和追蹤引數，也會將最終/登陸頁面URL內嵌在引數中。 範例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重新導向。

針對Adobe Advertising轉換追蹤，此專案會在行銷活動設定包含時套用」[!UICONTROL EF Redirect]「和」[!UICONTROL Auto Upload]，」當您儲存記錄時，Search， Social， &amp; Commerce會自動加上其重新導向與追蹤程式碼的前置詞。

* 如需可內嵌最終URL的支援引數，請參閱 [[!DNL Microsoft Advertising] 指示最終URL之引數的相關檔案](https://help.ads.microsoft.com/#apex/3/en/56799).

* 您可以選擇加入URL引數和為促銷活動定義的任何自訂引數，各個引數之間以&amp;分隔，例如 {lpurl}？matchtype={matchtype}裝置(&amp;D){device}.

* 您可以選擇新增第三方重新導向和追蹤。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 您可以在任何層級更新追蹤範本，無需重新提交廣告進行核准。
