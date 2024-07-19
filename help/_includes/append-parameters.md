---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# 在帳戶和行銷活動設定中附加引數欄位

**[!UICONTROL Append Parameters]：** （選用）要附加至基底URL的任何其他追蹤引數。<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->。 預設情況下，廣告商層級的附加引數會包含在帳戶層級和促銷活動層級，但您也可以覆寫任一層級。

您可以使用任何靜態文字字串，包括協力廠商追蹤引數，或任何[支援的追蹤引數](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md)，在基本URL中插入適當的資料值。

請使用逗號或&amp;符號分隔多個引數。 不支援巢狀括弧。

**附註：**

* 對附加引數的變更不受[!UICONTROL Auto Upload]選項控制。 如果您變更現有基底URL的附加引數，則不會自動產生新URL。 下載帳戶或行銷活動的大量表單檔案、更新[!UICONTROL Base URL/Final URL]欄位，然後上傳和張貼大量表單，以新增引數。

* （具有平行追蹤的廣告網路）避免使用巨集，巨集不會取代啟用平行追蹤之來源的點選。 如果廣告商必須使用巨集，則Adobe帳戶團隊應與客戶支援或實作團隊合作以新增它們。

* (具有Adobe Advertising-Adobe Analytics整合的廣告商)若要包含AMO ID引數以將搜尋、社交和Commerce資料傳送至[!DNL Analytics]，請參閱[廣告網路特定格式](/help/integrations/analytics/ids.md#amo-id-formats)。 不需要手動為具有伺服器端AMO ID實作的[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶新增引數。
