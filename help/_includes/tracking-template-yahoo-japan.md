---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Yahoo！的追蹤範本欄位 日本廣告實體

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]：** （選用）追蹤範本或追蹤URL，可指定所有離登陸網域重新導向和追蹤引數，並將最終/登陸頁面URL內嵌在引數中。 使用引數`!{lpurl}`指示登陸頁面URL。 範例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重新導向。

您可以選擇新增第三方重新導向和追蹤。

針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動為其自己的重新導向和追蹤代碼加上前置詞。

>[!NOTE]
>
>* 最精細層級的追蹤範本會覆寫所有較高層級的值。 例如，如果帳戶設定和關鍵字設定都包含值，則會套用關鍵字值。
>* 您可以在任何層級更新追蹤範本，無需重新提交廣告進行核准。
