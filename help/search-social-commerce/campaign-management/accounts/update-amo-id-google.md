---
title: 更新的AMO ID (s_kwcid)追蹤代碼 [!DNL Google Ads] 帳戶
description: 瞭解如何切換至的最新AMO ID追蹤代碼 [!DNL Google Ads] 帳戶。
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: 515c049a45d795fd973b5fcead5f96e71dbf844a
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# 更新的AMO ID (s_kwcid)追蹤代碼 [!DNL Google Ads] 帳戶

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

*[!DNL Google Ads]僅限帳戶*

的舊版（2019年10月之前） [AMO ID追蹤代碼](/help/integrations/analytics/ids.md#amo-id-formats) 適用於現有 [!DNL Google Ads] 帳戶不支援Analytics的某些功能，例如行銷活動和廣告群組層級的報表 [!DNL Google Ads] 最大成效行銷活動、草稿和實驗行銷活動，以及其他在多個行銷活動中存在相同廣告+關鍵字+比對型別組合的使用案例。

目前的格式包含行銷活動ID和廣告群組ID的引數：

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

您可以個別將任何或所有現有帳戶變更為目前格式。 如果您沒有最高成效的行銷活動或草稿和實驗行銷活動，則移轉至新格式為選用。

所有新增 [!DNL Google Ads] 帳戶會自動使用目前的AMO ID格式。

>[!NOTE]
>
>在您移轉帳戶後，所有點按、成本和曝光資料都會在變更後正確報告，但在移轉前發生的任何點進仍會根據舊AMO ID格式歸因於轉換資料。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 將游標放在帳戶名稱上，按一下 ![箭頭下拉式圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png)，然後選取 **[!UICONTROL Edit]**.

1. 按一下 **[!UICONTROL Set Account Tracking]**.

1. 開始移轉：

   1. 旁邊 **[!UICONTROL S_KWCID FORMAT]** ，按一下 **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. 按一下 **[!UICONTROL Migrate to new s_kwcid format]**.

   1. 在確認訊息中，選取核取方塊，然後按一下 **[!UICONTROL Continue]**.

   1. 在帳戶設定中，按一下 **[!UICONTROL Post]**.

   行銷活動的中繼資料更新於 [!DNL Analytics] 幾天內。 追蹤會持續進行，不會遺失任何資料，但報告可能不會反映新的追蹤程式碼，直到 [!DNL Analytics] 接收所有中繼資料。

   >[!NOTE]
   >
   >移轉前發生的所有點進仍會根據舊格式報告轉換資料。

1. 開始移轉後，請視需要更新登陸頁面尾碼設定（在某些廣告網路中稱為「最終URL尾碼」）：

   * 當 [!UICONTROL Auto Upload]「功能」已在追蹤設定中啟用，搜尋、社交和商務會自動更新此帳戶及其促銷活動之登陸頁面尾碼中的追蹤程式碼。 您不必執行任何動作。

   * 當 [!UICONTROL Auto Upload]「功能未啟用，且您沒有使用 [伺服器端AMO ID功能](/help/integrations/analytics/ids.md#amo-id-formats)，則您必須在登陸頁面尾碼設定中手動更新AMO ID引數。 您可以在帳戶和行銷活動設定中手動變更帳戶和行銷活動層級的尾碼，或透過在大量表單中上傳變更來進行。 若要在廣告群組層級或更低層級設定尾碼，請使用 [!DNL Google Ads] 編輯者。

   * 如果您在任何促銷活動元件的基本URL設定中包含AMO ID，請將其移至相關的登陸頁面尾碼設定。

1. （建議）驗證此帳戶在中的資料 [!DNL Analytics] 移轉其他帳戶之前。

>[!MORELIKETHIS]
>
>* [管理廣告網路帳戶](ad-network-account-manage.md)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [概觀 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
