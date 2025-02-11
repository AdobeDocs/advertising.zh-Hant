---
title: Advertising DSP巨集
description: 參考一般追蹤的可用巨集，以及追蹤第三方顯示廣告的點按次數。
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Advertising DSP巨集

巨集是指令的簡短指令或簡稱，通常遵循格式`${MACRO_NAME}`。 創意程式碼或點進URL中包含的巨集會展開為廣告伺服器可理解的較長程式碼字串。 DSP廣告伺服器會在投放或點按廣告時執行巨集。

廣告伺服器巨集可用來將重要資訊傳送至DSP或協力廠商廣告伺服器。 巨集最常用於販運協力廠商和自訂創意程式碼或中繼資料（例如協力廠商畫素）。

您可以在任何位置手動插入巨集，例如在VAST標籤、任何URL中，或在DSP或第三方事件畫素中。 不過，每個DSP使用者端和合作夥伴都有不同的廣告標籤格式，因此應將巨集插入標籤的不同位置。 每次您與新客戶或合作夥伴合作時，請要求他們提供檔案，說明要將巨集插入其DSP流量的廣告標籤中。

## 一般追蹤巨集

您可以視需要使用涵蓋所有廣告和標籤型別的一般追蹤巨集，以傳回特定資料。

| 巨集 | 替代說明 | 型別 |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | 帳戶ID。 | 整數 |
| `${TM_AD_ID}` | 廣告金鑰(adKey)。 | 字串 |
| `${TM_AD_ID_NUM}` | 廣告ID。 | 整數 |
| `${TM_ADVERTISER_ID}` | 廣告商ID。 | 整數 |
| `${TM_CAMPAIGN_ID}` | 促銷活動金鑰。 | 字串 |
| `${TM_CAMPAIGN_ID_NUM}` | 行銷活動ID。 | 整數 |
| ` ${TM_CLICK_URL}` | 重新導向URL，可讓廣告伺服器追蹤及計算廣告點按次數。 當播放廣告時，如果使用者按一下該廣告，就會啟動巨集，且會記錄該點按並計算在內，以用於報表用途。 | 字串 |
| ` ${TM_CLICK_URL_URLENC}` | 編碼的重新導向URL，可讓廣告伺服器追蹤及計算廣告點按次數。 當播放廣告時，如果使用者按一下該廣告，就會啟動巨集，且會記錄該點按並計算在內，以用於報表用途。 除非您正在建立協力廠商廣告，且您的廠商需要URL編碼，否則請勿使用此巨集。 | 字串 |
| `${TM_FEED_ID}` | 媒體刊登的索引鍵(feedKey)。 | 字串 |
| `${TM_FEED_ID_NUM}` | 媒體刊登的ID。 | 整數 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | 此位置的網站索引鍵。 需要[!DNL AppsFlyer]個行動應用程式安裝廣告的點選追蹤器。<!-- should map to placement_site_key column of placement_site table --> | 字串 |
| `${TM_PLACEMENT_ID}` | 位置索引鍵(cpKey)。 | 字串 |
| `${TM_PLACEMENT_ID_NUM}` | 位置ID。 | 整數 |
| `${TM_RANDOM}` | Cachebuster：介於1到1000000之間的隨機數字。 | 長 |
| `${TM_SESSION_ID}` | 工作階段的ID，對應於廣告標籤的單一擷取。 | 字串 |
| `${TM_SITE_DOMAIN_URLENC}` | 從競標要求中的URL剖析的頁面子網域；以URL編碼。 不支援橫幅內即點即用廣告。 | 字串 |
| ` ${TM_SITE_NAME}` | 位置的網站名稱。 | 字串 |
| `${TM_SITE_URL_URLENC}` | 在競標要求中傳遞的URL；以URL編碼。 不支援橫幅內即點即用廣告。 | 字串 |
| `${TM_SITE_ID_NUM}` | 位置的網站ID。 | 整數 |
| `${TM_TIMESTAMP}` | Unix時間戳記表示自1970年1月1日午夜(00:00 UTC)以來經過的秒數。 | 長 |
| ` ${TM_VIDEO_DURATION}` | 廣告視訊的持續時間（秒數）。 | 整數 |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## 行動專用巨集

| 巨集 | 替代說明 | 型別 |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore])對應到裝置作業系統的平台識別碼：<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>當平台不是上述任何專案時`other`</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore])裝置模型名稱，以URL編碼。 | 字串 |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore])提供廣告的環境：<ul><li>`a` =行動應用程式</li><li>`b` =行動網站</li></ul> | 字串（`a`或`b`） |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen])對應到裝置作業系統的平台識別碼：<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>當平台不是上述任何專案時`other`</li></ul> | 字串 |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen])廣告為檢視器的裝置型別：<ul><li>`TAB` =平板電腦</li><li>`PHN` =行動</li><li>`computer` =電腦</li></ul> | 字串 |
| `${UOO}` | ([!DNL Nielsen])使用者是否已選擇退出廣告追蹤：<ul><li>`1` （DNT旗標= 1） =使用者已選擇退出廣告追蹤</li><li>`0` （DNT標幟= 0） =使用者已選擇加入廣告追蹤</li></ul> | 整數（`0`或`1`） |
| `${TM_BUNDLE}` | [!DNL iOS]或[!DNL Android]應用程式商店套件組合識別碼。 範例： com.zynga.wwf2.free或id804379658 | 字串 |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}`指出出價者是否確定出價要求來自歐盟，且要求GDPR強制執行：<ul><li>`1` =應強制執行GDPR</li><li>`0` =不應強制執行GDPR</li></ul>`gdpr_consent=${GDPR_CONSENT}`是傳入競標要求中從供應合作夥伴傳遞的同意值：<ul><li>在大多數情況下，這是base64url編碼的同意字串，或daisybit （範例： BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA）</li><li>`0` =不同意</li><li>`1` =同意</li></ul> | Daisybit或整數 |

{style="table-layout:auto"}

## 按一下協力廠商顯示廣告的巨集

若要使用協力廠商顯示標籤精確追蹤廣告點按次數，DSP需要顯示點按巨集。 只需要一個巨集版本；相關的巨集視標籤型別而定。

| 巨集 | 替代說明 | 型別 |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 可讓廣告伺服器追蹤及計算平台中廣告點按次數的重新導向URL。 | 字串 |
| `${TM_CLICK_URL_URLENC}` | 此重新導向URL可讓需要URL編碼的廣告伺服器追蹤及計算平台中的廣告點按次數。 | 字串 |

{style="table-layout:auto"}

DSP會在下列情況下，自動在協力廠商顯示標籤中插入顯示點選巨集：

* 從廣告伺服器夥伴<!-- [Needs PM confirmation.] -->匯出廣告標籤
* 直接在DSP中大量上傳[!DNL Flashtalking]或[!DNL Google DoubleClick for Advertisers]廣告標籤

如果您在建置顯示廣告時遺失點按巨集，DSP會顯示警告訊息，提示您手動在標籤的正確區域中插入適當的顯示點按巨集。

## [!DNL Analytics for Advertising]個巨集

如需[[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)客戶特別可用的其他巨集，請參閱&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)&quot;及&quot;[附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;。

## 疑難排解巨集錯誤

將巨集新增至程式碼時，請確定您使用巨集的確切語法。 驗證巨集時，DSP會檢查巨集是否與其中一個有效的巨集完全相符。

如果巨集名稱的開頭或結尾缺少字元，則會產生錯誤。 例如，如果出現下列情況，則會顯示錯誤訊息：

* 您忘記巨集名稱開頭的一或多個字元，例如`${`。 如果未包含完整語法，則無法將專案辨識為有效的巨集。
* 巨集的結尾不是有效的字元集，例如`}`。

>[!MORELIKETHIS]
>
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [連線電視廣告設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [顯示廣告設定](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [行動廣告設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [原生廣告設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [前段廣告設定](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [通用視訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
