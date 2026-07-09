---
title: 可用於追蹤URL的巨集
description: 參考您可新增至登陸頁面URL、追蹤URL和協力廠商創意的巨集。
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
TQID: https://experienceleague.adobe.com/J5jfIECrL29NngVOulEgHKZBHYqBmoz4680HzEzhIng
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 3c3bffe0c28bb24c0df9385f9cc91be1376a66d2
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 0%

---

# 可用於追蹤URL的巨集

<!-- More feature metadata???  -->

您可以在協力廠商創意內容、體驗的協力廠商追蹤URL以及自用的登陸頁面URL中加入下列任何巨集。

有些可用的巨集或它們的對等巨集會自動包含在體驗標籤中。

<!--
 Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |
| `${TC_1}` | Custom tracking code 1. | &mdash; | &mdash; |
| `${TC_2}` | Custom tracking code 2. | &mdash; | &mdash; |
| `${TC_3}` | Custom tracking code 3. | &mdash; | &mdash; |
| `${TC_4}` | Custom tracking code 4. | &mdash; | &mdash; |
| `${TC_5}` | Custom tracking code 5. | &mdash; | &mdash; |
| `${GDPR_ENFORCED}` | Whether GDPR enforcement is required for the bid request. Values: **1** = GDPR should be enforced, **0** = GDPR should not be enforced. | &mdash; | &mdash; |
| `${GDPR_CONSENT}` | The GDPR consent value received from the supply partner in the bid request. Typically: **1** = consent provided, **0** = no consent provided. | &mdash; | &mdash; |
-->

| 巨集 | 說明 | 自動在Advertising DSP的Experience Tags中？ |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | 從DSP追蹤及報告行銷活動ID | 是 |
| `${TM_SITE_ID_NUM}` | 從DSP追蹤及報告網站ID | 是 |
| `${TM_PLACEMENT_ID_NUM}` | 從DSP追蹤並報告位置ID | 是 |
| `${TM_AD_ID_NUM}` | 從DSP追蹤及報告廣告ID | 是 |
| `${TM_CREATIVE_ID_NUM}` | 從DSP追蹤及報告創作ID | 不適用 |
| `${TM_SESSION_ID}` | 追蹤並報告與廣告請求關聯的工作階段ID。 如果未傳回值，則Advertising Creative會產生一個值。 | 是 |
| `${TM_ACC_EXPERIENCE_ID}` | 追蹤及報告Advertising Creative體驗ID | — |
| `${TM_ACC_CREATIVE_ID}` | 追蹤並報告Advertising Creative創作ID | — |
| `${TM_RANDOM}` | 隨機產生的數字，介於1到1,000,000之間。 常用於快取破產。 | — |
| `${TM_TIMESTAMP}` | UNIX®時間戳記（以秒為單位） | — |
| `${TM_CLICK_URL_URLENC}` | （適用於來自需要URL編碼的廠商的第三方廣告）經過編碼的點選重新導向URL，可讓廣告伺服器追蹤及計算廣告點選次數。 當使用者按一下廣告時，會啟用巨集，且會記錄該點按並計算在內，以用於報表用途。 | 是 |
| `${TC_1}` | 自訂追蹤代碼1。 | — |
| `${TC_2}` | 自訂追蹤代碼2. | — |
| `${TC_3}` | 自訂追蹤代碼3. | — |
| `${TC_4}` | 自訂追蹤代碼4. | — |
| `${TC_5}` | 自訂追蹤代碼5。 | — |
| `${GDPR_ENFORCED}` | 投標要求是否需要GDPR強制執行。 值： **1** =應強制執行GDPR，**0** =不應強制執行GDPR。 | — |
| `${GDPR_CONSENT}` | 從競標要求中的供應合作夥伴接收的GDPR同意值。 通常： **1** =已提供同意，**0** =未提供同意。 | — |

>[!MORELIKETHIS]
>
>* [將標準創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [標準創意設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [目標體驗設定*[非目標體驗設定](/help/creative/experiences/experience-settings-no-targeting.md)
