---
title: 可用於追蹤URL的巨集
description: 參考您可新增至登陸頁面URL、追蹤URL和協力廠商創意的巨集。
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: e966058f5fe3fe9eb039f74bda8ea950f717e123
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 可用於追蹤URL的巨集

*已關閉的Beta*

<!-- More feature metadata???  -->

您可以在協力廠商創意內容、體驗的協力廠商追蹤URL以及自用的登陸頁面URL中加入下列任何巨集。

有些可用的巨集或它們的對等巨集會自動包含在體驗標籤中。

<!-- Later: 

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

-->

| 巨集 | 說明 | 自動在Advertising DSP的Experience Tags中？ |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | 從DSP追蹤及報告行銷活動ID | 是 |
| `${TM_SITE_ID_NUM}` | 從DSP追蹤及報告網站ID | 是 |
| `${TM_PLACEMENT_ID_NUM}` | 從DSP追蹤並報告位置ID | 是 |
| `${TM_AD_ID_NUM}` | 從DSP追蹤及報告廣告ID | 是 |
| `${TM_CREATIVE_ID_NUM}` | 從DSP追蹤及報告創作ID | 不適用 |
| `${TM_SESSION_ID}` | 從DSP追蹤並報告曝光ID。 如果未傳回值，Advertising Creative會產生一個值。 | 是 |
| `${TM_ACC_EXPERIENCE_ID}` | 追蹤及報告Advertising Creative體驗ID | — |
| `${TM_ACC_CREATIVE_ID}` | 追蹤並報告Advertising Creative創作ID | — |
| `${TM_RANDOM}` | 介於1到1000000之間的隨機數字 | — |
| `${TM_TIMESTAMP}` | UNIX®時間戳記（以秒為單位） | — |
| `${TM_CLICK_URL_URLENC}` | （適用於來自需要URL編碼的廠商的第三方廣告）經過編碼的點選重新導向URL，可讓廣告伺服器追蹤及計算廣告點選次數。 當使用者按一下廣告時，就會啟用巨集，且會記錄該點按並計算在內，以用於報表用途。 | 是 |

>[!MORELIKETHIS]
>
>* [將標準創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [標準創意設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [目標體驗設定](/help/creative/experiences/experience-settings-targeting.md)
>*[非目標體驗設定](/help/creative/experiences/experience-settings-no-targeting.md)
