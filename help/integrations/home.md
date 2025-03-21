---
title: 新增功能
description: 瞭解Adobe Advertising與Adobe Experience Cloud中其他產品和服務之間整合的更新。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: d933613a46dfde7529623d0b0ab62e01006cb53c
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# 新增功能

下列是新的或最近變更的功能。

| 日期 | 功能 | 說明 | 以取得詳細資訊 |
| ---- | ------- | ----------- | -------------------- |
| 2024年10月29日發行 | [!DNL Adobe Analytics for Advertising] | （具有[!DNL Adobe Analytics for Advertising]和[!DNL Microsoft Advertising]最高成效行銷活動的廣告商）現在，當您為最高成效行銷活動在追蹤URL中實作新的AMO ID ([!DNL s_kwcid])引數時（不包含廣告和關鍵字），您可在Adobe Analytics中使用最高成效行銷活動的資產群組層級資料。 對大多數具有最高成效行銷活動的帳戶的追蹤已移轉到新格式。 對於沒有[!UICONTROL Auto Upload]追蹤選項的具有最高成效行銷活動的帳戶，這些行銷活動尚未移轉到新格式，不過，您必須手動更新每個登陸頁面尾碼，以包含新的AMO ID格式。<br><br>您最高成效行銷活動的Adobe Analytics資料也可在Search、Social和Commerce中使用。 | 檢視新的[AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)和[何時以及如何新增引數至您的追蹤URL](/help/integrations/analytics/ids.md#amo-id-implement)。 |
| 2024年11月13日 | [!DNL Analytics for Advertising] | (具有[!DNL Analytics for Advertising]和Adobe Customer Journey Analytics的廣告商)如果您使用保留變數來擷取AMO ID和EF ID，那麼您可以透過儘快將您為AMO ID和EF ID保留的變數複製到標準[!DNL eVars]中，為Adobe Advertising和Adobe Customer Journey Analytics之間的未來整合做好準備。 這樣一來，當您完成工作時，即可立即收集AMO ID和EF ID的歷史資料，且這些歷史資料可供日後使用。 如果您使用保留的變數且需要完成此工作，Adobe客戶團隊會通知您。 | 請參閱&quot;[收集AMO ID與EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)&quot;。 |
| 2023年12月16日 | 說明 | 新檔案將說明如何在[!DNL Target]中為來自搜尋、社交和Commerce中廣告的點進流量設定A/B測試，以及如何在[!DNL Analytics]中測量和視覺化測試的秘訣。 | 請參閱&quot;[在Adobe Target中設定A/B測試以搜尋、社交和Commerce廣告](/help/integrations/target/ab-tests-search.md)&quot;。 |
| 2023年8月8日 | [!DNL Analytics for Advertising] | 有些[!DNL Analytics]成功事件量度（包括標準、自訂和保留的轉換量度及流量量度）可自動在DSP以及搜尋、社交和Commerce中使用。 現在，您可以將[!DNL eVar]和[!DNL prop]層級資料匯入自訂成功事件中，藉此根據現有的[!DNL Analytics] [!DNL eVars]和[!DNL props]設定自己的成功量度。 | 請參閱&quot;[從Adobe Analytics [!DNL eVars] 和 [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)建立轉換量度。&quot; |
| 2023年7月13日 | 報告 | (具有[!DNL Analytics for Advertising]的DSP使用者)連線電視(CTV)位置的瀏覽轉換現在包含在Adobe Analytics中可用的轉換資料中。 | 請參閱 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)的[概觀中的「如何使用整合的範例」一節。 |
| 2022年11月1日 | 說明 | 新檔案將說明如何在Advertising DSP和Adobe Target之間實作點進和檢視訊號共用、在[!DNL Target]中為您的DSP廣告設定A/B測試活動，以及如何設定Adobe Analytics Analysis Workspace以檢視測試資料。 | 請參閱&quot;[在Adobe Target中設定Advertising DSP Ads的A/B測試](/help/integrations/target/ab-tests-dsp.md)&quot;。 |
| 2022年8月17日 | 說明 | 新章節將說明Adobe Advertising與Adobe Audience Manager整合的所有方式。 | 請參閱「與Adobe Audience Manager整合」一章，包括「[Adobe Advertising與Adobe Audience Manager](/help/integrations/audience-manager/overview.md)整合」的概觀。 |
| 2021年4月27日 | [!DNL Analytics for Advertising] | 瞭解為何以及如何將[!DNL Analytics for Advertising]巨集新增至您的[!DNL Google Campaign Manager 360]廣告標籤，以將點按資料傳送至Adobe Analytics。 | 請參閱&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;。 |
| 2021年4月19日 | [!DNL Analytics for Advertising] | 瞭解為什麼以及如何將巨集附加至您的[!DNL Flashtalking]廣告標籤，以將點選資料傳送至Adobe Analytics。 | 請參閱&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)&quot;。 |
| 2021年10月27日 | [!DNL Analytics for Advertising] | 如果您的組織想從使用舊版Adobe Analytics `visitorAPI.js`資料庫切換到使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)資料庫(`alloy.js`)進行資料彙集，您必須進行一些變更以啟用識別碼拼接。 | 請參閱&quot;[搭配Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md)使用 [!DNL Last Event Service] JavaScript資料庫。&quot; |
| 2021年5月26日 | 說明 | 章節「[!DNL Analytics for Advertising]」現在包含有關「在[!DNL Analytics Marketing Channels]中工作」的子章節。 | 請參閱：「[行銷管道的基礎知識](/help/integrations/analytics/marketing-channels/mc-overview.md)」、「[使用Adobe Advertising ID建立 [!DNL Analytics Marketing Channels] 處理規則](/help/integrations/analytics/marketing-channels/mc-ids.md)」、「[搭配使用 [!DNL Analytics Marketing Channels] Adobe Advertising資料](/help/integrations/analytics/marketing-channels/mc-ac-data.md)」和「[為何管道資料在Adobe Advertising和 [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)之間可能有所差異。」 |
| 2021年5月26日 | 說明 | 已新增所有關於[!DNL Analytics for Advertising]的影片教學課程的連結。 | 請參閱： &quot;[Adobe Advertising整合的相關教學課程影片](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html)&quot;。 |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
