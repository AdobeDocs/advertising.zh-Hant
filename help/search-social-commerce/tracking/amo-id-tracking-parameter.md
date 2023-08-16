---
title: AMO ID (s_kwcid)追蹤引數
description: 瞭解用來與Adobe Analytics共用Adobe Advertising資料的追蹤引數。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# AMO ID (s_kwcid)追蹤引數

*僅具有Adobe Advertising-Adobe Analytics整合的廣告商*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe AdvertisingAdobe Analytics會使用AMO ID附加引數(也稱為 `s_kwcid` 引數，包含廣告頻道和廣告網路專用元素。

引數會透過下列其中一種方式新增至您的追蹤URL：

* （建議）已實作伺服器端插入功能。

   * DSP客戶：當一般使用者檢視含有Adobe Advertising畫素的顯示廣告時，畫素伺服器會自動將s_kwcid引數附加至您的登入頁面尾碼。

   * 搜尋、社交和商務客戶：

      * 的 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 帳戶與 [!UICONTROL Auto Upload] 若設定為已啟用帳戶或促銷活動，當一般使用者按一下包含Adobe Advertising畫素的廣告時，畫素伺服器會自動將s_kwcid引數附加至您的登陸頁面尾碼。

      * 針對其他廣告網路，或 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 帳戶與 [!UICONTROL Auto Upload] 設定為停用，手動將引數新增至您的帳戶層級附加引數，以便將其附加至您的基本URL。

* 未實作伺服器端插入功能：

   * DSP客戶：

      * 的 [!DNL Flashtalking] 新增標籤，手動插入其他巨集(根據&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md).」

      * 的 [!DNL Google Campaign Manager 360] 新增標籤，手動插入其他巨集(根據&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md).」

  <!--  * For all other ads, XXXX. -->

   * 搜尋、社交和商務客戶：

      * 針對([!DNL Google Ads] 和 [!DNL Microsoft® Advertising])廣告，手動新增AMO ID引數至您的登陸頁面尾碼。

      * 針對所有其他廣告網路上的廣告，手動將AMO ID引數新增至您的帳戶層級附加引數，以便將其附加至您的基本URL。

若要實施伺服器端插入功能，或決定最適合您企業的選項，請洽詢您的Adobe帳戶團隊。

如需DSP和Search， Social， &amp; Commerce的AMO ID格式，請參閱&quot;[使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).」

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* （搜尋、社交和商務） [管理廣告網路帳戶](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* （搜尋、社交和商務） [百度行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* （搜尋、社交和商務） [Google Ads行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* （搜尋、社交和商務） [Microsoft® Advertising campaign設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* （搜尋、社交和商務） [Yahoo！ Japan Ads促銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* （搜尋、社交和商務） [Yandex行銷活動設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
