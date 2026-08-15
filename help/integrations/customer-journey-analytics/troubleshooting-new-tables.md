---
title: 疑難排解Customer Journey Analytics中的Adobe Advertising資料
description: 瞭解如何疑難排解及解決Customer Journey Analytics中的Adobe Advertising資料問題。
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: c3ffa88d5df4fa2ff7e52813503c10b67d7c6eb7
workflow-type: tm+mt
source-wordcount: 3290
ht-degree: 0%

---

# 疑難排解Customer Journey Analytics中的Adobe Advertising資料

以下是潛在問題、其可能原因和解決方案。

## 所有潛在問題的清單

| 問題 | 更多資訊 |
| ------- | ---------------- |
| 在瀏覽器的程式碼檢查工具的[!DNL Network]標籤中看不到alloy()呼叫 | 請參閱「[安裝和設定問題](#issues-installation-setup)」>「[WebSDK擴充功能未初始化](#websdk-extension-doesn't-initialize)」一節 |
| 主控台錯誤：未定義alloy | 請參閱&quot;[安裝和設定問題](#issues-installation-setup)&quot; > &quot;[WebSDK擴充功能未初始化](#websdk-extension-doesn't-initialize)&quot; |
| 沒有向edge.adobedc.net互動或收集請求 | 請參閱&quot;[安裝和設定問題](#issues-installation-setup)&quot; > &quot;[WebSDK擴充功能未初始化](#websdk-extension-doesn't-initialize)&quot; |
| 要求會到達Adobe Experience Platform Edge Network但傳回400或500錯誤 | 請參閱「[安裝及設定問題](#issues-installation-setup)」>「[資料流未設定或設定錯誤](#datastream-not-configured-or-misconfigured)」一節 |
| Adobe Analytics或Adobe Advertising報表中不會出現任何資料 | 請參閱「[安裝及設定問題](#issues-installation-setup)」>「[資料流未設定或設定錯誤](#datastream-not-configured-or-misconfigured)」一節 |
| 網路回應中的錯誤：「找不到資料流」 | 請參閱「[安裝及設定問題](#issues-installation-setup)」>「[資料流未設定或設定錯誤](#datastream-not-configured-or-misconfigured)」一節 |
| 不會針對網頁記錄任何瀏覽轉換或點進轉換 | 請參閱&quot;[Advertising擴充功能設定問題](#advertising-extension-setup-issues)&quot;一節 |
| 點進的Experience Data Model (XDM)承載中缺少`_experience.adcloud` | 請參閱&quot;[Advertising擴充功能設定問題](#advertising-extension-setup-issues)&quot;一節 |
| 轉換會在除錯工具中確認，但不會出現在Adobe Advertising報表中 | 請參閱&quot;[Advertising擴充功能設定問題](#advertising-extension-setup-issues)&quot;一節 |
| 訪客ID在不同頁面之間變更 | 請參閱&quot;[身分和ECID問題](#identity-and-ecid-issues)&quot;一節 |
| Advertising受眾區段不相符 | 請參閱&quot;[身分和ECID問題](#identity-and-ecid-issues)&quot;一節 |
| 除錯程式會顯示不符合規則條件 | 請參閱&quot;[規則或事件未引發](#rules-or-events-don't-fire)&quot;一節 |
| [!UICONTROL Send Event]動作永遠不會執行 | 請參閱&quot;[規則或事件未引發](#rules-or-events-don't-fire)&quot;一節 |
| 在[!DNL Tags]中所做的變更未反映在已上線的網站上 | 請參閱&quot;[程式庫建置和發佈問題](#library-build-and-publishing-issues)&quot;一節 |
| 已套用擴充功能更新，但舊行為仍持續存在 | 請參閱&quot;[程式庫建置和發佈問題](#library-build-and-publishing-issues)&quot;一節 |
| `alloy()`傳送事件呼叫成功（回應為200個），但報表中缺少Adobe Advertising轉換資料 | 請參閱「[Advertising欄位的結構描述驗證問題](#schema-validation-for-advertising-fields)」一節 |
| 偵錯工具中的XDM承載未顯示`_experience.adcloud`物件 | 請參閱「[Advertising欄位的結構描述驗證問題](#schema-validation-for-advertising-fields)」一節 |
| Customer Journey Analytics中沒有摘要報表資料可用於Advertising DSP或Advertising Search、Social和Commerce。 | 請參閱「[報告問題](#reporting-issues)」>「[摘要報告](#summary-reporting)」一節 |
| 廣告商1的Customer Journey Analytics中有摘要報表資料可以使用，但廣告商2則沒有。 | 請參閱「[報告問題](#reporting-issues)」>「[摘要報告](#summary-reporting)」一節 |
| （搜尋、社交和Commerce使用者） Customer Journey Analytics中的摘要報表資料可用於一個[!DNL Google Ads]、[!DNL Meta Ads]或[!DNL Microsoft Advertising]帳戶，但不能用於另一個帳戶。 | 請參閱「[報告問題](#reporting-issues)」>「[摘要報告](#summary-reporting)」一節 |
| Customer Journey Analytics Workspace中的摘要報表資料與Advertising DSP或Advertising Search、Social和Commerce中的資料不同，或是某些行銷活動和行銷活動實體缺少摘要資料。 | 請參閱「[報告問題](#reporting-issues)」>「[摘要報告](#summary-reporting)」一節 |
| CJA Customer Journey Analytics Workspace中的轉換資料（例如`Page Views`）不適用於報表維度（例如`Campaign`）。 | 請參閱「[報告問題](#reporting-issues)」>「[事件層級報告](#event-level-reporting)」一節 |

## 安裝和設定問題 {#issues-installation-setup}

### WebSDK擴充功能未初始化#websdk-extension-doesn&#39;t-initialize

#### 問題：

* 在瀏覽器的程式碼檢查工具的[!DNL Network]標籤中看不到alloy()呼叫
* 主控台錯誤：未定義alloy
* 沒有向edge.adobedc.net互動或收集請求

#### 可能的原因和驗證/解決方案

| 原因 | 修正 |
| ----- | --- |
| 資料庫未發佈或處於草稿狀態 | 移至[發佈流程](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)，並確認包含WebSDK擴充功能的程式庫處於已核准/發佈狀態。 |
| 內嵌程式碼遺失或錯誤的環境 | 確認網頁上的[!DNL Tags]內嵌程式碼參考了正確的環境(Dev/Stage/Prod)。 在`<head>`標籤中尋找`//assets.adobedtm.com/...`指令碼標籤的環境。 |
| 非同步與同步載入衝突 | 確定每個網頁僅有一個[!DNL Tags]內嵌程式碼。 重複的內嵌程式碼會導致競爭條件。 |
| 內容安全性原則(CSP)封鎖 | 將`edge.adobedc.net` `and assets.adobedtm.com`新增至您的CSP `connect-src`和`script-src`指示。 |

### 資料流未設定或設定錯誤 {#datastream-not-configured-or-misconfigured}

#### 問題：

* 要求會到達Adobe Experience Platform Edge Network但傳回400或500錯誤
* Adobe Analytics或Adobe Advertising報表中未出現任何資料<!-- It's not useful to organize this info by cause, not symptom -->
* 網路回應中的錯誤：「找不到資料流」

#### 可能的原因和驗證/解決方案

| 原因 | 修正 |
| ----- | --- |
| 標籤屬性的資料串流ID遺失或不正確。 | <ol><li>在[!DNL Tags]中，開啟標籤屬性的[資料流組態設定](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)。</li><li>確認[!UICONTROL Datastream]欄位指向每個環境（開發、測試和生產）的正確資料流，以及正確的結構和資料集。<br><br>除非您在所有三個環境中明確共用一個資料流，否則每個環境都應該有自己的資料流。</li></ol> |
| 標籤屬性未啟用資料流服務。 | [開啟資料流設定](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)，並確認下列服務已啟用：<ul><li>Adobe Advertising （用於轉換/對象同步）</li><li>Adobe Experience Platform （用於設定檔擷取）</li></ul> |
| 沙箱不符 | 確認資料串流與您的結構描述和資料集屬於相同的Adobe Experience Platform沙箱。 常見的錯誤是在生產沙箱中建立資料串流，但將結構描述指向開發沙箱。 |

### [!UICONTROL Advertising]擴充功能設定問題 {#advertising-extension-setup-issues}

#### 問題：

* 不會針對網頁記錄任何瀏覽轉換或點進轉換。

  若要驗證是否已記錄轉換：

  1. 開啟網頁並附加`ef_id=test&s_kwcid=test`至URL。
  1. 開啟瀏覽器的程式碼檢查工具（通常稱為[!DNL Inspect]），開啟[!DNL Network]標籤，並從Adobe Experience Platform尋找event_type=&quot;advertising.enrichment_ct&quot;的互動呼叫。
  1. 在資料收集介面中，[開啟您要收集之網站資料的結構描述定義](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas)，並確認`xdm->_experience->adcloud->conversionDetails->trackingCode`和`trackingIdentities`包含`ef_id`和`s_kwcid`。

* 點進的Experience Data Model (XDM)承載中缺少`_experience.adcloud`。

* 轉換會在除錯工具中確認，但不會出現在Adobe Advertising報表中

#### 可能的原因和驗證/解決方案

| 原因 | 修正 |
| ----- | --- |
| 未針對資料流啟用`Adobe Advertising`服務 | <ol><li>在[!DNL Tags]中，開啟標籤屬性的[資料流組態設定](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)。</li><li>啟用下列服務並儲存設定：<ul><li>Adobe Advertising （用於轉換/對象同步）</li><li>Adobe Experience Platform （用於設定檔擷取）</li></ul></ol> |
| 未針對[!UICONTROL WebSDK]延伸啟用`Adobe Advertising`元件 | WebSDK擴充功能中的`Adobe Advertising`元件預設為停用，且無論XDM結構描述或規則如何設定，在Adobe Advertising點進或檢視的追蹤運作之前，必須先明確啟用。<ol><li>在[!DNL Tags]中，開啟Adobe Experience Platform Web SDK組態設定[&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components)中屬性的組建選項。</li><li>啟用&#x200B;**Advertising**&#x200B;元件，並儲存設定。</li><li>重建並重新發佈程式庫。</li></ol> |
| 僅記錄點進轉換；檢視轉換不會出現 | 這是預期的預設行為。 啟用`Adobe Advertising`元件後，點進追蹤會使用`s_kwcid`和`ef_id` URL查詢引數自動啟用。 瀏覽追蹤預設為停用，且需要其他設定 — 請參閱下一列。 |
| 未啟用或設定閱覽追蹤 | <ol><li>為資料流啟用Adobe Advertising服務</li><ol><li>前往Adobe Experience Platform中的[!UICONTROL Data Collection] > [!UICONTROL Datastreams]，並開啟[!DNL Tags]屬性使用的資料流。</li><li>選取「**新增服務**」，選取「**Adobe Advertising**」和「**Adobe Experience Platform**」，然後選取「**儲存**」。</li></ol><li>在Adobe Advertising DSP中設定廣告商</li><ol><li>在[!DNL Tags]中，移至[!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure]。</li><li>在[!UICONTROL Advertiser]區段下，從下拉式清單中選取並啟用一個廣告商。 若要設定多個廣告商，請選取&#x200B;**新增廣告商**。</li></ol><li>確認正在引發檢視轉換畫素</li><ol><li>在Adobe Experience Platform Debugger中，確認互動呼叫包含`xdm.query`欄位下的`stitchId`。</li><li>在瀏覽器程式碼檢查工具的[!DNL Network]標籤上，確認已引發型別為`advertising.enrichment`的事件，且包含`xdm.query`下的`stitchId`。</li></ol></ol> 檢視轉換無論造訪次數為何，都只會每30分鐘引發一次。 如果您沒有看到互動呼叫，請清除瀏覽器快取，然後再試一次。 |
| （如果導覽互動呼叫觸發後，Experience Platform中沒有檢視事件）廣告商是手動輸入，而不是從下拉式清單中選取 | 從[!UICONTROL Advertiser]下拉式清單重新選取廣告商，而非手動輸入。 |
| （如果導覽互動呼叫觸發後，Experience Platform中沒有檢視事件）。導覽互動呼叫不會傳送任何廣告商ID | 確認已在WebSDK擴充功能設定的[!UICONTROL Advertiser]區段下設定並啟用廣告商，然後重建並重新發佈程式庫。 |

在開啟[!UICONTROL Advertising]擴充功能設定問題的支援票證之前，請先確認下列事項：

* **Adobe Advertising**&#x200B;和&#x200B;**Adobe Experience Platform**&#x200B;服務已新增至資料流。
* 已在WebSDK擴充功能組態中啟用&#x200B;**Adobe Advertising**&#x200B;元件。
* 啟用元件後，已重建及重新發佈程式庫。
* 針對點進追蹤，登陸頁面URL在廣告點按上包含`s_kwcid`和`ef_id`。
* 針對閱覽追蹤，廣告商在Adobe Advertising DSP中設定為使用正確的廣告商ID。
* WebSDK擴充功能的版本為2.36.0或更新版本。

### 身分和ECID問題 {#identity-and-ecid-issues}

#### 問題：

* 訪客ID在不同頁面之間變更
* Advertising受眾區段不相符

#### 可能的原因和驗證/解決方案

| 原因 | 修正 |
| ----- | --- |
| 第三方Cookie已封鎖 | 在資料流的Edge Network設定中設定第一方網域，以移轉至第一方CNAME資料收集。 |
| 存在舊版`s_ecid` Cookie時，`idMigrationEnabled`設為`false` | 在WebSDK基底組態中設定`idMigrationEnabled: true`，以從`s_ecid`或`AMCV_` Cookie移轉現有的ECID。 |

### 規則或事件不會觸發#rules-or-events-don&#39;t-fire

#### 問題：

* 除錯程式會顯示不符合規則條件
* [!UICONTROL Send Event]動作永遠不會執行

#### 驗證與解析

請確認下列專案：

* 規則會儲存並包含在作用中的程式庫組建中。
* 事件型別符合實際的頁面行為（例如，[!UICONTROL Library Loaded]與[!UICONTROL DOM Ready]的比較與[!UICONTROL Window Loaded]的比較）。
* 規則的條件限制不太嚴格。 暫時移除條件以隔離問題以進行測試。
* 規則順序正確。 如果多個規則共用相同事件，請檢查規則順序。
* 頁面上先前沒有停止執行的JavaScript錯誤。 檢查瀏覽器主控台是否有未攔截到的例外狀況。

### 程式庫建置和發佈問題 {#library-build-and-publishing-issues}

#### 問題：

* 在[!DNL Tags]中所做的變更未反映在已上線的網站上
* 已套用擴充功能更新，但舊行為仍持續存在

#### 可能的原因和驗證/解決方案

| 原因 | 修正 |
| ----- | --- |
| 變更未新增至程式庫 | 在[!UICONTROL Publishing Flow]中，確認您的變更已新增至開發環境中的程式庫。 移至[!UICONTROL Libraries]，開啟工作程式庫，選取&#x200B;**新增所有變更的資源**，然後選取&#x200B;**儲存並建置**。 |
| 瀏覽器正在快取舊程式庫 | 執行硬式重新整理（Ctrl+Shift+R或Cmd+Shift+R），或在無痕視窗/私人視窗中開啟頁面。 如果問題仍然存在，請完全清除瀏覽器快取。 |
| 內嵌程式碼適用於錯誤的環境 | 如果您要測試生產行為，請確認頁面上的內嵌程式碼是生產內嵌程式碼。 |
| 程式庫建置無訊息地失敗 | 移至[!UICONTROL Publishing Flow]並檢查程式庫是否顯示[!UICONTROL Build Failed]狀態。 開啟程式庫並檢閱組建記錄 — 常見原因是規則設定無效或擴充功能版本衝突。 |

### Advertising欄位的結構描述驗證問題 {#schema-validation-for-advertising-fields}

#### 問題：

* `alloy()`傳送事件呼叫成功（回應為200個），但報表中缺少Adobe Advertising轉換資料
* 偵錯工具中的XDM承載未顯示`_experience.adcloud`物件

#### 可能的原因和驗證/解決方案

| 原因 | 修正 |
| ----- | --- |
| 結構描述中缺少[!UICONTROL Advertising]欄位群組 | <ol><li>前往Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas]。</li><li>開啟資料流使用的結構描述。</li><li>在[!UICONTROL Field Groups]面板中，確認已列出&#x200B;**Adobe Advertising Cloud ExperienceEvent完整擴充功能**。</li><li>如果遺失，請選取「**新增**」，搜尋&#x200B;**Adobe Advertising Cloud**，選取「**Adobe Advertising Cloud ExperienceEvent完整擴充功能**」，然後儲存設定。</li></ol>結構描述變更不需要單獨重新發佈您的[!DNL Tags]資料庫，但如果新增新欄位，則必須重新對應[!DNL Tags]中的XDM資料元素。 |
| 結構描述中缺少必要的Adobe Advertising欄位 | 請確定`_experience.adcloud.conversionDetails`下的結構描述中存在必要的Adobe Advertising欄位。 請參閱[參考：必要的結構描述欄位](#required-schema-fields)。<br><br>如果缺少任一欄位，請確認&#x200B;**Adobe Advertising Cloud ExperienceEvent完整擴充功能**&#x200B;欄位群組已儲存至結構描述，然後重新整理結構描述編輯器。 |
| 登陸頁面URL不包含必要的查詢引數 | 請確定登入頁面URL包含必要的查詢引數。 在廣告點進上，登入頁面URL必須包含兩個查詢引數，例如`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`。 請參閱&quot;[參考：遺漏查詢引數](#missing-query-parameters)&quot;以取得可能的原因。 |
| XDM承載中有些引數遺失或空白 | 若要驗證傳出XDM裝載，請開啟Adobe Experience Platform Debugger或瀏覽器程式碼檢查工具的[!DNL Network]標籤、篩選`edge.adobedc.net`，並檢查互動要求內文（請參閱下列範例裝載）。<br><br>如果`trackingCode`或`trackingIdentity`空白或遺失：觸發規則時，頁面上未出現查詢引數（檢查URL和規則的事件時間），或結構描述中缺少欄位群組（請重新造訪上面的第一列）。 |

##### 參考：必要的結構描述欄位 {#required-schema-fields}

| 欄位路徑 | 型別 | 說明 |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | 字串 | 將轉換對應至原始廣告點選。 從登陸頁面URL上的`s_kwcid`查詢引數填入。 |
| `_experience.adcloud.conversionDetails.trackingIdentity` | 字串 | 儲存追蹤的閱覽或點進轉換事件的唯一身分和其他詳細資訊。 從登陸頁面URL上的`ef_id`查詢引數填入。 |

##### 參考：缺少查詢引數 {#missing-query-parameters}

| 缺少引數 | 可能的原因 |
| ----- | --- |
| `s_kwcid` | Adobe Advertising搜尋或DSP促銷活動設定中不會啟用自動標籤。 |
| `ef_id` | 登陸頁面URL未使用Adobe Advertising追蹤的重新導向，或促銷活動設定中未啟用EF ID附加。 |

**範例點進承載**

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

## Customer Journey Analytics Workspace中的報告問題

### 摘要報告

| 問題 | 驗證與解析 |
| ----- | --- |
| Customer Journey Analytics中沒有摘要報表資料可用於Advertising DSP或Advertising Search、Social和Commerce。 | <ol><li>確認Customer Journey Analytics Workspace所參照的資料檢視是否正確。</li><li>確認從Adobe Advertising到Customer Journey Analytics的摘要已啟用。 請洽詢您的Adobe客戶團隊。</li><li>確認您的Adobe Advertising維度/分類/查詢資料集和摘要資料集已包含在Customer Journey Analytics連線中。</li><li>確認您的Adobe Advertising維度和摘要量度已包含在Customer Journey Analytics資料檢視中。</li></ol>如果您已驗證上述所有設定，但仍看不到摘要資料，請為您的組織開啟[支援票證](https://experienceleague.adobe.com/home?support-tab=home#support)。 |
| 廣告商1的Customer Journey Analytics中有摘要報表資料可以使用，但廣告商2則沒有。 | <ol><li>確認從Adobe Advertising到Customer Journey Analytics的摘要已為廣告商2啟用。 請洽詢您的Adobe客戶團隊。</li><li>確認在Customer Journey Analytics連線中，已為您的三個資料集（維度/分類/查詢、摘要和事件量度）啟用設定&quot;[!UICONTROL Backfill all existing data]&quot;。</li></ol>如果您已驗證上述所有條件，但仍看不到摘要資料，請為您的組織開啟[支援票證](https://experienceleague.adobe.com/home?support-tab=home#support)。 |
| （搜尋、社交和Commerce使用者） Customer Journey Analytics中的摘要報表資料可用於一個[!DNL Google Ads]、[!DNL Meta Ads]或[!DNL Microsoft Advertising]帳戶，但不能用於另一個帳戶。 | 確認特定廣告網路帳戶已啟用從Adobe Advertising到Customer Journey Analytics的摘要。 請洽詢您的Adobe帳戶團隊。<br><br>如果帳戶已啟用摘要，但您仍然看不到摘要資料，請為您的組織開啟[支援票證](https://experienceleague.adobe.com/home?support-tab=home#support)。 包含廣告網路帳戶的[!UICONTROL Account ID]。 |
| Customer Journey Analytics Workspace中的摘要報表資料與Advertising DSP或Advertising Search、Social和Commerce中的資料不同，或是某些行銷活動和行銷活動實體缺少摘要資料。 | <ol><li>確認您在[!DNL Workspace]和Adobe Advertising報表中使用相同的日期範圍。</li><li>確認[!DNL Workspace]和Adobe Advertising報表中套用的任何篩選器和區段不會造成資料差異。</li><li>確認您Customer Journey Analytics資料檢視的[!UICONTROL Time Zone]符合您[Advertising DSP帳戶](/help/dsp/admin/user-own-profile-edit.md)的[!UICONTROL Default Timezone]。</li><li>確認在Customer Journey Analytics連線中，已為您的三個資料集（維度/分類/查詢、摘要和事件量度）啟用設定&quot;[!UICONTROL Backfill all existing data]&quot;。</li></ol>如果您確定資料不一致，請為您的組織開啟[支援票證](https://experienceleague.adobe.com/home?support-tab=home#support)。 包含廣告網路帳戶的[!UICONTROL Account ID]。 若要顯示差異的證據，請包含熒幕擷取畫面和電子表格。 您的Adobe客戶團隊可回溯修正資料摘要，以視需要解決差異。 |

### 事件層級報表

| 問題 | 驗證與解析 |
| ----- | --- |
| Customer Journey Analytics Workspace中的轉換資料（例如`Page Views`）不適用於報表維度（例如`Campaign`）。 | 從驗證障礙最少的專案開始，驗證以下內容：<ul><li>確認您使用正確的資料檢視。</li><li>確認適用的轉換量度為網頁/線上事件，Adobe Advertising可將其歸因於維度。</li><li>確認Adobe Advertising正在追蹤適用網站上的點進和檢視點進。</li><li>在分類資料集的Customer Journey Analytics連線中，確認[!DNL Key]和[!DNL Matching Key]設定的值是否正確： [!DNL Key]： `Tracking Code` (_customername.adLens2.trackingCode)， [!DNL Matching Key]： `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)。</li><li>確認[!DNL Adobe Advertising]服務已新增至Adobe Experience Platform資料流、資料流的對應結構描述是`XDM ExperienceEvent Schema`，以及欄位群組`Adobe Advertising Cloud ExperienceEvent Full Extension`已新增至`XDM ExperienceEvent`結構描述。</li><li>確認Adobe Advertising設定已在WebSDK擴充功能中正確設定並發佈。</li></ul>如果您已驗證上述所有設定，但仍看不到轉換資料，請為您的組織開啟[支援票證](https://experienceleague.adobe.com/home?support-tab=home#support)。 包含廣告網路帳戶的[!UICONTROL Account ID]。 |

## 實用的驗證和偵錯工具

### Adobe Experience Platform Debugger

安裝[!DNL Chrome]的[!DNL Adobe Experience Platform Debugger]延伸模組：

* 所有WebSDK `alloy()`呼叫的即時檢視
* 資料串流ID和環境驗證
* XDM裝載檢查
* Edge Network要求和回應詳細資料

偵錯工具中的金鑰檢查：

| 標籤 | 檢查內容 |
| ----- | --- |
| [!UICONTROL Summary] | 確認偵測到WebSDK並顯示安裝的版本。 |
| [!UICONTROL Adobe Experience Platform WebSDK] | 顯示每個引發的事件、完整XDM裝載及Edge Network回應。 |
| [!UICONTROL Adobe Advertising] | 確認AMO ID擷取和XDM與`advertising.enrichment`事件型別的互動呼叫。 |

### 瀏覽器程式碼檢查工具的[!DNL Network]標籤

使用瀏覽器程式碼檢查工具的[!DNL Network]標籤（通常稱為「[!DNL Inspect]」）執行下列動作：

依`edge.adobedc.net`篩選以檢查原始Edge Network請求：

* 要求URL： `https://[org-id].data.adobedc.net/ee/v2/interact`
* 方法： `POST`
* 狀態： `200` （狀況良好）、`400` （裝載錯誤）或`500` （伺服器或資料流錯誤）

檢查要求裝載：

* 正確的`dataStreamId`
* 具有預期欄位的`xdm`物件是否存在
* 已填入ECID的`identityMap`

### 主控台驗證

檢查已安裝的WebSDK版本：

```js
window.alloy.version
```

手動觸發測試事件：

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## 請求支援前的快速參考檢查清單

開啟支援票證之前，請先確認下列事項：

* WebSDK擴充功能是最新版本。
* 程式庫已發佈，且內嵌程式碼適用於正確的環境。
* 資料串流ID已針對開發、測試和生產正確設定。
* 已啟用所有必要的資料流服務。
* [!UICONTROL Advertising]元件已在WebSDK擴充功能設定中啟用，且已設定DSP廣告商ID。
* XDM結構描述包含[!UICONTROL Advertising]欄位群組。
* [!UICONTROL Send Event]規則包含識別對應，並在正確的事件上引發。
* 沒有CSP或瀏覽器隱私設定會封鎖Edge Network請求。
* Adobe Experience Platform Debugger會確認事件已送達Edge Network。
* 瀏覽器主控台中沒有停止執行的JavaScript錯誤。
* `Adobe Advertising Cloud ExperienceEvent Full Extension`欄位群組已新增至結構描述。
* 結構描述中存在`_experience.adcloud.conversionDetails.trackingCode`。
* 結構描述中存在`_experience.adcloud.conversionDetails.trackingIdentity`。
* 登陸頁面URL同時包含點進時的`s_kwcid`和`ef_id`引數。
* Adobe Experience Platform Debugger會確認輸出承載中已填入`conversionDetails`。

## 何時將問題升級

在下列情況下，請聯絡您的Adobe客戶團隊或工程團隊：

* 資料流驗證後，Edge Network請求傳回持續性`500`錯誤。
* 已在Debugger中確認[!UICONTROL Advertising]次轉換，但24-48小時後不會出現在報表中。
* WebSDK版本更新引進了舊版中不存在的回歸。 在支援票證中包含特定版本號碼。

>[!MORELIKETHIS]
>
>* [總覽](overview.md)
>* [由 [!DNL Customer Journey Analytics]](ids.md)使用的Adobe Advertising ID
>* [必要條件](prerequisites.md)
>* [設定資料收集、資料傳輸及報告](set-up.md)
>* Customer Journey Analytics中的[Adobe Advertising量度和維度](advertising-data-in-cja.md)
>* （Adobe Analytics使用者） [收集AMO ID和EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
