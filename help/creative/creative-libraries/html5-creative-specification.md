---
title: HTML5創意規格
description: 參考Advertising Creative的HTML5創意規格。
feature: Creative Standard Creatives
exl-id: 06d29442-d688-4fb8-ad6f-cba0a897fde0
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# 適用於Advertising Creative的HTML5創意規格

本檔案概述[!DNL Creative]中HTML5創意元件的需求和API支援。 此API允許開發HTML5創意，其屬性可在創意交付時設定。

## 範圍

[!DNL Creative]支援HTML5橫幅，其非多媒體創意內容會出現在頁面的設定邊界內。 您可以使用下列型別的HTML5創意：

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5：**&#x200B;支援最多5個可在創意建立和販運期間設定的登陸頁面URL。

* **彈性的HTML5：**&#x200B;支援最多5個可在創意建立和販運期間設定的登陸頁面URL，也可在創意建立和販運期間修改創意屬性。

## 需求

### 資料夾和壓縮需求

* 創意內容必須封裝為ZIP檔案（.ZIP格式）。 巢狀ZIP檔案不受支援，因此請勿在外部壓縮資料夾中包含壓縮資料夾。

* ZIP檔案必須至少包含一個HTML檔案(主要HTML顯示檔案)，其中包含對[!DNL Creative] JavaScript資料庫的參照。 主要HTML檔案可在根資料夾或子資料夾中。

* 主要的HTML檔案可命名為任何名稱，只要它不包含特殊字元即可，不過建議使用`index.html`。

* 呈現最終創意所需的所有支援資產必須位於與HTML顯示檔案相同的資料夾或主資料夾的子資料夾中。

* 請勿在創意內容中包含創意內容未參考的任何檔案。

### 納入Advertising Creative JavaScript檔案

主要HTML檔案（不含其他檔案）必須包含對JavaScript檔案`AMOLibrary.js`的參照。 使用以下位址呼叫`<head>`區段第一行中的檔案：

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

此檔案包含的函式可確保對退出事件進行本機測試而不會發生問題。

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5創意需求

#### 支援靜態HTML5中的點進URL

##### `amo.registerClick(clkVar, clkUrl)`

註冊點進URL和用於參考每個URL的相關引數（稱為`clickTag`）。 此API會通知[!DNL Creative]廣告伺服器新增點選追蹤的位置。 您可以使用此API來註冊最多五個點按標籤變數，每個變數都有對應的登陸頁面URL。

>[!NOTE]
>
>您在HTML5創意內容中包含的靜態URL僅供本機測試使用，且將被覆寫。 當您上傳HTML5創意內容時，會為每個`clickTag`變數定義預設登陸頁面。 當您將上傳的HTML5創意內容指派給廣告體驗時，您可以選擇覆寫每個`clickTag`變數的預設登陸頁面，而[!DNL Creative]會在您儲存體驗時新增點選追蹤至URL。

###### 引數

* `clkVar` — 點選變數的名稱（通常是「clickTag」），以雙引號括住。

* `clkUrl` — 此點選變數的登陸頁面URL，以雙引號括住。

###### 使用情況

在主要HTML檔案的`<head>`區段中呼叫`amo.registerClick()`。

###### 範例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

觸發退出事件，將使用者重新導向至為`clickTag`設定的登陸頁面。 在本機測試期間，此函式會提醒開發人員傳遞至函式的URL是否已註冊。

###### 引數

* `clkTag` — 您使用`amo.registerClick()`函式指派登陸頁面URL時所使用的點選變數名稱（以單引號括住）。

* `event` — （選用） JavaScript的「點選」事件物件。 這會記錄點按的座標，進一步用於分析創意成果。

###### 使用情況

在主要HTML檔案的`<body>`區段中呼叫`amo.onAdClick()`。

###### 範例

`amo.onAdClick('clickTag')`或`amo.onAdClick('clickTag',clickEvt)`

### 彈性的HTML5創意需求

#### 支援彈性HTML5中的點進URL

##### `amo.registerClick(clkVar, clkUrl)`

註冊點進URL和用於參考每個URL的相關引數（稱為`clickTag`）。 此API會通知[!DNL Creative]廣告伺服器新增點選追蹤的位置。 您可以使用此API來註冊最多五個點按標籤變數，每個變數都有對應的登陸頁面URL。

>[!NOTE]
>
>您在HTML5創意內容中包含的靜態URL僅供本機測試使用，且將被覆寫。 當您上傳HTML5創意內容時，會為每個`clickTag`變數定義預設登陸頁面。 當您將上傳的HTML5創意內容指派給廣告體驗時，您可以選擇覆寫每個`clickTag`變數的預設登陸頁面，而[!DNL Creative]會在您儲存體驗時新增點選追蹤至URL。

###### 引數

* `clkVar` — 點選變數的名稱（通常是「clickTag」），以雙引號括住。

* `clkUrl` — 此點選變數的登陸頁面URL，以雙引號括住。

###### 使用情況

在主要HTML檔案的`<head>`區段中呼叫`amo.registerClick()`。

###### 範例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

觸發退出事件，將使用者重新導向至為`clickTag`設定的登陸頁面。 在本機測試期間，此函式會提醒開發人員傳遞至函式的URL是否已註冊。

###### 引數

* `clkTag` — 您使用`amo.registerClick()`函式指派登陸頁面URL時所使用的點選變數名稱（以單引號括住）。

* `event` — （選用） JavaScript的「點選」事件物件。 這會記錄點按的座標，進一步用於分析創意成果。

###### 使用情況

在主要HTML檔案的`<body>`區段中呼叫`amo.onAdClick()`。

###### 範例

`amo.onAdClick('clickTag')`或`amo.onAdClick('clickTag',clickEvt)`

#### 支援彈性HTML5中的創意屬性

##### `amo.registerAttribute(key, type, value)`

定義可在創意或體驗建立時變更的創意屬性。 您最多可以定義20個創意屬性，這些屬性可在創意或體驗建立時設定。

>[!NOTE]
>
>此方法中定義的值僅用於本機開發，不會用於即時廣告服務。

###### 引數

* `key` — 屬性的英數字元名稱。 它必須以字母字元開頭。

* `type` — 屬性的型別（`TEXT`或`IMAGE`）。

* `value` — 測試的屬性值。 對於型別`IMAGE`的屬性，該值必須是影像檔案的相對路徑。

###### 使用情況

在本機模式測試期間，呼叫`amo.registerAttribute()`以註冊一個創意屬性、型別和值。 任何用作範例值的影像檔案都應與上傳的套件一起封裝在ZIP檔案中。

##### `amo.attributes`

查詢創意屬性變數名稱和值的JSON物件。 物件鍵是屬性名稱，值是這些屬性的值。

在本機測試模式中，機碼值組是由`amo.registerAttribute` API登入的組。 對於生產，創意屬性變數名稱和值必須在創意建立和販運時設定。

### Creative內容需求

Advertising DSP中大部分的顯示器交換都有以下創意需求：

* 實線邊框必須環繞所有廣告影像。

* 不允許展開廣告。

* 登入頁面必須在新視窗中開啟。

* 登入頁面網域及其子網域不得超過35個字元。 **注意：**&#x200B;最終登陸頁面URL是在DSP中定義，而不是在HTML5資產中定義。

* 任何廣告產品的免責宣告都必須包含在廣告本身中，而不僅僅是登陸頁面上。

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## JSON物件和陣列形式的範例內容

### JSON物件的內容範例

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### JSON陣列形式的範例內容

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## 範例HTML5 creative

### 範例資料夾結構（解壓縮後）

* index.html

* /assets （資料夾）

   * bg.jpg (JPG、PNG、SVG或GIF影像)

### 簡單HTML5創意內容的HTML檔案範例(index.html)

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### 靜態HTML5創意內容的HTML檔案範例(index.html)

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [將標準創意內容新增至創意內容庫](/help/creative/creative-libraries/creative-add-standard.md)
