---
title: 更新 [!DNL Google Ads] 帳戶的AMO ID (s_kwcid)追蹤代碼
description: 瞭解如何切換至 [!DNL Google Ads] 帳戶的最新AMO ID追蹤代碼。
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: edb46265c6977a1e2c1b352f41fedcfc3a9e3bbf
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# 更新[!DNL Google Ads]帳戶的AMO ID (s_kwcid)追蹤代碼

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

僅&#x200B;*[!DNL Google Ads]個帳戶*

現有[!DNL Google Ads]帳戶的[AMO ID追蹤代碼](/help/integrations/analytics/ids.md#amo-id-formats)的舊版（2019年10月之前）格式不支援Analytics中的某些功能，例如[!DNL Google Ads]最高成效行銷活動的行銷活動和廣告群組層級報告、草稿和實驗行銷活動，以及其他在多個行銷活動中存在相同廣告+關鍵字+相符型別組合的使用案例。

目前的格式包含行銷活動ID和廣告群組ID的引數：

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

對於使用舊版格式的現有帳戶，您可以變更為目前格式。 如果您沒有最高成效的行銷活動或草稿和實驗行銷活動，則移轉至新格式為選用。

所有新[!DNL Google Ads]帳戶都會自動使用目前的AMO ID格式。

>[!NOTE]
>
>此選項僅適用於未使用目前格式的帳戶。
>
>在您移轉帳戶後，所有點按、成本和曝光資料都會在變更後正確報告，但在移轉前發生的任何點進仍會根據舊AMO ID格式歸因於轉換資料。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 將游標放在帳戶名稱上，按一下![箭頭下拉式圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png)，然後選取&#x200B;**[!UICONTROL Edit]**。

1. 按一下&#x200B;**[!UICONTROL Set Account Tracking]**。

1. 開始移轉：

   1. 在[!UICONTROL Account Tracking]設定中的&#x200B;**[!UICONTROL S_KWCID FORMAT]**&#x200B;旁邊，按一下&#x200B;**[!UICONTROL LEGACY S_KWCID FORMAT]**。

   1. 按一下&#x200B;**[!UICONTROL Migrate to new s_kwcid format]**。

   1. 在確認訊息中，選取核取方塊，然後按一下&#x200B;**[!UICONTROL Continue]**。

   1. 在帳戶設定中，按一下&#x200B;**[!UICONTROL Post]**。

   行銷活動的中繼資料會在幾天內於[!DNL Analytics]中更新。 追蹤會繼續進行，不會遺失任何資料，但報告可能要到[!DNL Analytics]收到所有中繼資料後，才會反映新的追蹤代碼。

   >[!NOTE]
   >
   >移轉前發生的所有點進仍會根據舊格式報告轉換資料。

1. 開始移轉後，請視需要更新登陸頁面尾碼設定（在某些廣告網路中稱為「最終URL尾碼」）：

   * 在追蹤設定中啟用「[!UICONTROL Auto Upload]」功能後，搜尋、社交和Commerce會自動更新此帳戶及其促銷活動之登陸頁面尾碼中的追蹤代碼。 您不必執行任何動作。

   * 當[!UICONTROL Auto Upload]功能未啟用，而且您沒有使用[伺服器端AMO ID功能](/help/integrations/analytics/ids.md#amo-id-formats)時，您必須手動更新登陸頁面尾碼設定中的AMO ID引數。 您可以在[帳戶設定](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)和[行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)中手動變更帳戶和行銷活動層級的尾碼，或透過[在大量表單中上傳變更](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)來手動變更帳戶和行銷活動層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用[!DNL Google Ads]編輯器。

   * 如果您在任何促銷活動元件的基本URL設定中包含AMO ID，請將其移至相關的登陸頁面尾碼設定。

1. （建議）移轉其他帳戶之前，請先在[!DNL Analytics]中驗證此帳戶的資料。

>[!MORELIKETHIS]
>
>* [管理廣告網路帳戶](ad-network-account-manage.md)
>* [Adobe AdvertisingID已由 [!DNL Analytics]](/help/integrations/analytics/ids.md)使用
>* [總覽 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
