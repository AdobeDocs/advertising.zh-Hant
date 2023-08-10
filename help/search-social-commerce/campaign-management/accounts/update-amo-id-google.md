---
title: 更新的AMO ID (s\_kwcid)追蹤程式碼 [!DNL Google Ads] 帳戶
description: 瞭解如何切換到的最新AMO ID追蹤程式碼 [!DNL Google Ads] 帳戶。
exl-id: 82168ee6-43bb-4b8d-882d-5254a1abcb09
feature: Search Campaign Management
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# 更新的s_kwcid追蹤程式碼 [!DNL Google Ads] 帳戶

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

*[!DNL Google Ads]僅限帳戶*

現有之s\_kwcid追蹤程式碼的舊版格式 [!DNL Google Ads] 帳戶不支援Analytics的某些功能，例如行銷活動和廣告群組層級的報表 [!DNL Google Ads] 最大成效行銷活動、草稿和實驗行銷活動，以及其他在多個行銷活動中存在相同廣告+關鍵字+比對型別組合的使用案例。

最新格式包含行銷活動ID和廣告群組ID的引數：

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

您可以個別變更任何或所有現有帳戶的新格式。 如果您沒有最高成效的行銷活動或草稿和實驗行銷活動，則移轉至新格式為選用。

所有新增 [!DNL Google Ads] 帳戶會自動使用新的s\_kwcid格式。

>[!NOTE]
>
>在您移轉帳戶後，所有點按、成本和曝光資料都會在變更後正確報告，但在移轉前發生的任何點進仍會根據舊的s\_kwcid格式歸因於轉換資料。

1. 在主功能表中，按一下 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. 將游標放在帳戶名稱上，按一下 ![箭頭下拉式圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png)，然後選取 **[!UICONTROL Edit]**.
1. 按一下 **[!UICONTROL Set Account Tracking]**.
1. 開始移轉：

   1. 旁邊 **[!UICONTROL S_KWCID FORMAT]** ，按一下 **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. 按一下 **[!UICONTROL Migrate to new s_kwcid format]**.
   1. 在確認訊息中，選取核取方塊，然後按一下 **[!UICONTROL Continue]**.
   1. 在帳戶設定中，按一下 **[!UICONTROL Post]**.

   行銷活動的中繼資料會在幾天內在Analytics中更新。 追蹤會持續進行，不會遺失任何資料，但在Analytics收到所有中繼資料之前，報表可能不會反映新的追蹤代碼。

   >[!NOTE]
   >
   >移轉前發生的所有點進仍會根據舊格式報告轉換資料。

1. 開始移轉後，請視需要更新登陸頁面尾碼設定（在某些廣告網路中稱為「最終URL尾碼」）：

   * 當 [!UICONTROL Auto Upload]「功能」已在追蹤設定中啟用，搜尋、社交和商務會自動更新此帳戶及其促銷活動之登陸頁面尾碼中的追蹤程式碼。 您不必執行任何動作。
   * 當 [!UICONTROL Auto Upload]「功能未啟用，而且您沒有使用伺服器端s-kwcid，則必須在登陸頁面尾碼設定中手動更新s\_kwcid引數。 您可以在帳戶和行銷活動設定中手動變更帳戶和行銷活動層級的尾碼，或透過在大量表單中上傳變更來進行。 若要在廣告群組層級或更低層級設定尾碼，請使用 [!DNL Google Ads] 編輯者。
   * 如果您將s\_kwcid納入任何促銷活動元件的基本URL設定中，請將其移至相關的登陸頁面尾碼設定。

1. （建議）移轉其他帳戶之前，請先在Analytics中驗證此帳戶的資料。

>[!MORELIKETHIS]
>
>* [管理廣告網路帳戶](ad-network-account-manage.md)
>* [AMO ID追蹤引數](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [概觀 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
