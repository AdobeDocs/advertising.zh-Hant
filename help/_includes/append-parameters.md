---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---
# 在帳戶和行銷活動設定中附加引數欄位

**[!UICONTROL Append Parameters]：** （選用）附加至基本URL的任何其他追蹤引數。<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. 預設情況下，廣告商層級的附加引數會包含在帳戶層級和促銷活動層級，但您可以覆寫任一層級。

您可以使用任何靜態文字字串，包括協力廠商追蹤引數，或 [支援的追蹤引數](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md)，這會在基本URL中插入適當的資料值。

請使用逗號或&amp;符號來分隔多個引數。 不支援巢狀括弧。

**附註：**

* 附加引數的變更不受 [!UICONTROL Auto Upload] 選項。 如果您變更現有基本URL的附加引數，則不會自動產生新URL。 下載帳戶或促銷活動的Bulksheet檔案，更新 [!UICONTROL Base URL/Final URL] 欄位，然後上傳並張貼大量表單。

* （具有平行追蹤的廣告網路）避免使用巨集，巨集不會取代啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，則Adobe帳戶團隊應與客戶支援或實作團隊合作來新增它們。

* (使用AdobeAdvertising-Adobe Analytics整合的廣告商)加入 `s_kwcid` 將搜尋、社交和商務資料傳送到的引數 [!DNL Analytics]，請參閱 [廣告網路特定格式](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md). 不需要手動新增引數 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 具有伺服器端s\_kwcid實作的帳戶。
