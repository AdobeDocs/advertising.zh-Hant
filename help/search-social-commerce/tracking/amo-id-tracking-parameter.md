---
title: AMO ID (s_kwcid)追蹤引數
description: 瞭解用來與Adobe Analytics共用Adobe Advertising資料的追蹤引數。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# AMO ID (s_kwcid)追蹤引數

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe AdvertisingAdobe Analytics會使用AMO ID附加引數(也稱為 `s_kwcid` 引數，包含廣告頻道和廣告網路專用元素。

<!-- add everything below to IDs page -->

引數會透過下列其中一種方式新增至您的追蹤URL：

* （建議）已實作伺服器端插入功能。

  的 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帳戶與 [!UICONTROL Auto Upload] 若設定已啟用帳戶或促銷活動，當一般使用者點按廣告時，畫素伺服器會自動將AMO ID引數附加至您的登陸頁面尾碼 <!-- click a search ad or views a display ad --> 與Adobe Advertising畫素。

  針對其他廣告網路，或 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帳戶與 [!UICONTROL Auto Upload] 設定已停用，手動將AMO ID引數新增至您的帳戶層級附加引數，這會將其附加至您的基本URL。

* <!-- (Search, Social, & Commerce only) -->未實施伺服器端插入功能，您必須手動將AMO ID引數新增至([!DNL Google Ads] 和 [!DNL Microsoft Advertising])登陸頁面尾碼或（其他廣告網路）帳戶層級的附加引數。

若要實施伺服器端插入功能，或決定最適合您企業的選項，請洽詢您的Adobe帳戶團隊。

如需DSP和Search， Social， &amp; Commerce的AMO ID格式，請參閱&quot;[使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).」

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [管理廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [百度行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising促銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo！ Japan Ads促銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
