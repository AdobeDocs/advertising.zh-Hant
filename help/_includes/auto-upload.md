---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---
# 帳戶和行銷活動設定中的自動上傳欄位

**[!UICONTROL Auto Upload]：** （僅適用於具有[!UICONTROL EF Redirect]的同步行銷活動）下次Search、Social和Commerce與其同步時，會自動將下列內容上傳至廣告網路： (a)追蹤範本的搜尋、Social和Commerce追蹤引數以及附加至最終URL的相同引數，或(b)內嵌搜尋、Social和Commerce追蹤程式碼的新目的地URL。 對於具有[Adobe Advertising-Adobe Analytics整合](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)和伺服器端AMO ID (s_kwcid)組態的廣告商，上傳也包含您[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶的[AMO ID引數](/help/integrations/analytics/ids.md#amo-id)。 預設帳戶層級設定繼承自廣告商的追蹤設定。 您可以在行銷活動層級覆寫帳戶層級設定。

**注意：**&#x200B;只有不同步的實體（亦即新增的實體和屬性已變更的現有實體）才會每天更新追蹤URL。 因此，如果您將現有廣告商/帳戶/促銷活動的此設定從「停用」變更為「啟用」，則不會為已同步的現有實體更新追蹤URL。 若要將追蹤新增至現有非同步實體的URL，請連絡您的Adobe帳戶團隊，要求執行一次性的手動同步程式。 自動上傳程式將處理未來的變更。
