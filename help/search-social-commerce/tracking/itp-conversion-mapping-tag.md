---
title: Adobe Advertising轉換對應標籤
description: 瞭解適用於ITP 2.2的JavaScript型轉換對應標籤，其可讓Adobe Advertising追蹤發生於非登陸頁面上的轉換事件。
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: 2c755eaa01f5bc7606074bb0fc276901c21ef807
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Adobe AdvertisingJavaScript轉換對應標籤

*僅追蹤Adobe Advertising轉換的廣告商*

Adobe AdvertisingJavaScript型轉換對應標籤與Adobe AdvertisingJavaScript v2或v3轉換追蹤標籤搭配使用時，可讓Adobe Advertising追蹤發生於非登陸頁面之頁面上的轉換事件。 ITP 2.2解決方案會將使用者的Cookie儲存在廣告商擁有的iFrame中的本機儲存空間中。 接著，本機儲存空間就能將Cookie值從點按下游保留至轉換頁面。

使用轉換對應標籤，確保Adobe Advertising可追蹤在Apple Safari和Mozilla Firefox瀏覽器內發生的所有轉換，進而限制第一方Cookie的持續性。<!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

使用轉換對應標籤：

1. [部署轉換對應標籤](#deploy-conversion-mapping-tag)。

1. 如果您的組織使用多個Adobe Experience Cloud Identity Service組織ID （先前稱為IMS組織ID），請[更新您的轉換標籤](#update-conversion-tags)以包含組織ID。

1. [驗證標籤部署](#validate-conversion-mapping)。

## 為ITP 2.2部署JavaScript轉換對應標籤 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>如果您使用ITP 2.0的JavaScript轉換對應標籤，請以下列其中一個標籤取代所有轉換頁面中的現有標籤。<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* 如果您的組織使用單一組織ID (用於搜尋、社交和Commerce帳戶)，請使用以下標籤：

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  其中，以您搜尋、社交和Commerce帳戶的不重複使用者ID取代`{AMO User ID}`。

* 如果您的組織使用多個組織ID，請使用下列標籤：

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  其中：

   * 您以追蹤頁面轉換的組織ID取代值`{xxxxxx@AdobeOrg}`。 對所有轉換頁面使用相同的組織ID。

   * 您會將`{AMO User ID}`取代為您的搜尋、社交和Commerce帳戶的不重複使用者識別碼。

* 如果您使用的標籤管理系統不支援將`imsorgid`變數新增至指令碼標籤，請改用下列程式碼：

  *如果您的組織使用單一組織識別碼：

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  其中，以您搜尋、社交和Commerce帳戶的不重複使用者ID取代`{AMO User ID}`。

   * 如果您的組織使用多個組織ID：

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     其中：

      * 您以追蹤頁面轉換的組織ID取代值`{xxxxxx@AdobeOrg}`。 對所有轉換頁面使用相同的組織ID。

      * 您會將`{AMO User ID}`取代為您的搜尋、社交和Commerce帳戶的不重複使用者識別碼。

如果您不知道組織ID或搜尋、Social和Commerce使用者ID的值，請洽詢您的Adobe帳戶團隊。

### 範例

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### 新增標籤的位置

在任何可能是搜尋點按的登陸頁面的頁面中新增標籤（理想情況下，在所有頁面上，因為登陸頁面可能會隨著時間變更）。 必須在Adobe AdvertisingJavaScript v3轉換追蹤標籤之前載入它。

若將其置於iframe或容器標籤中，則：

* iframe應與最上層網域位於相同層級。

* 轉換對應標籤應該只會比上層網域低一(1)個層級。

## 更新您的JavaScript轉換標籤 {#update-conversion-tags}

如果您的組織使用多個組織ID，請將追蹤頁面轉換的組織ID新增至現有的JavaScript轉換標籤。

如果您的組織使用一個組織ID，則不需要執行此步驟。

### JavaScript V2標籤

在轉換指令碼標籤的開頭新增下列字串：

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

以追蹤頁面轉換的組織ID取代值`{xxxxxx@AdobeOrg}`。

範例：

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

### JavaScript V3標籤

定義`window.EF`後，新增下列字串：

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

以追蹤頁面轉換的組織ID取代值`{xxxxxx@AdobeOrg}`。

範例：

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        window.EF.imsorgid ="abc12345@AdobeOrg";
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

## 驗證標籤部署 {#validate-conversion-mapping}

請您的Adobe帳戶團隊協助您驗證轉換對應標籤和一般轉換標籤（如果您已更新此標籤）。
