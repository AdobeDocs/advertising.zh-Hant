---
title: 歸因規則的計算方式
description: 瞭解Adobe Advertising如何計算每種型別的歸因規則。
exl-id: 15beeadd-bb65-4efe-8c4f-34c4a48cc775
feature: Search Reports, DSP Custom Reports
source-git-commit: 513d81cf835ccbffa16581799f0dc8306681e3ad
workflow-type: tm+mt
source-wordcount: '2711'
ht-degree: 0%

---

# 如何計算Adobe Advertising的歸因規則

*僅追蹤Adobe Advertising轉換的廣告商*

<!-- Verify statements about cross-device events -->

廣告商層級歸因規則是用來將轉換資料（可能跨多個廣告管道）歸因於一系列導致轉換的事件。

您也可以在下列位置選取歸因規則，以僅將規則套用至產生的資料：

* DSP

   * 具有多重接觸歸因的自訂報表

* 搜尋、社交和Commerce

   * 自訂報表

   * 預設和自訂檢視

   * （部分使用者角色） Portfolio層級模擬。

>[!NOTE]
>
>* 歸因規則適用於任何頻道中付費廣告的點按次數，以及顯示廣告和社交廣告的曝光數。 它們不適用於付費搜尋廣告的曝光數，無法在事件層級進行追蹤。
>* Adobe Advertising一律會在轉換前為每個Web瀏覽者儲存下列事件： a)第一次付費點按； b)每個管道最多10次點按（搜尋、社交或顯示），包括第一次點按；以及c)最多10次顯示曝光數。<!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
>* 在Advertising DSP和Advertising Creative中，跨裝置定義只會考慮所選歸因規則中的事件路徑。<!-- cross-device attribution via LiveRamp only -->
>* 在報表和管理檢視中，針對某個值所顯示的小數位數會依貨幣而定，但Adobe Advertising會儲存更精確的值。

## 上次事件（預設）

將轉換歸因於廣告商的[點按回顧視窗](/help/search-social-commerce/glossary.md#c-d)內系列中的最後一個付費點按，如果沒有發生付費點按，則歸因於廣告商的[點按回顧視窗](/help/search-social-commerce/glossary.md#i-j)內的最後一個點按。

如果轉換之前只有曝光數，則轉換會視為&#x200B;*檢視*，其會根據廣告商的[檢視權數設定](/help/search-social-commerce/glossary.md#uv)加權，或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法加權。

![上次事件歸因百分比](/help/search-social-commerce/assets/attribution-percent-last-event.png "上次事件歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑： Click1、Click2、Click3、轉換120美元

該轉換歸因於Click 3，金額為120美元。

### 同時包含曝光次數與點按次數的範例

**注意：**&#x200B;曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、轉換120美元

轉換金額為120美元，歸因於Click 1。

### 具有所有曝光的範例

**注意：**&#x200B;只有顯示廣告和社交廣告的曝光數才適用。

事件路徑：曝光次數1、曝光次數2、曝光次數3、轉換120美元

此轉換歸因於印象3。 因為轉換是檢視，所以會套用報表設定的「轉換歸因」區段中選取的檢視估價方法：

* 如果報表引數指定了加權的顯示比例，則該權重會套用至顯示比例。 例如，如果廣告商的檢視權重為40%，則120 USD x 40% = 48 USD，因此48 USD歸因於「印象3」。

* 如果報表引數指定使用原始值做為閱覽，則閱覽權重不會套用至閱覽，而完整的120美元會歸因於「曝光數3」。

+++

<!-- end examples as collapsible content -->

## 第一個事件

將轉換歸因於廣告商的[點按回顧視窗](/help/search-social-commerce/glossary.md#c-d)內的系列中的第一個付費點按，如果沒有發生付費點按，則歸因於廣告商的[點按回顧視窗](/help/search-social-commerce/glossary.md#i-j)內的第一印象。 此規則僅適用於單一裝置上的事件。

當轉換之前只有曝光數時，轉換會視為&#x200B;*檢視*，其會根據廣告商的[檢視權數設定](/help/search-social-commerce/glossary.md#uv)加權，或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法加權。

![第一個事件歸因百分比](/help/search-social-commerce/assets/attribution-percent-first-event.png "第一個事件歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換120美元

轉換金額為120美元，歸因於Click 1。

### 同時包含曝光次數與點按次數的範例

**注意：**&#x200B;曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、轉換120美元

轉換金額為120美元，歸因於Click 1。

### 具有所有曝光的範例

**注意：**&#x200B;只有顯示廣告和社交廣告的曝光數才適用。

事件路徑：曝光次數1、曝光次數2、曝光次數3、轉換120美元

該轉換歸因於曝光次數1。 由於轉換是檢視，在「（顯示促銷活動）轉換」中選取的檢視估價方法
套用報表設定的「歸因」區段：

* 如果報表引數指定了加權的顯示比例，則該權重會套用至顯示比例。 例如，如果廣告商的瀏覽權數為40%，則120 x 40% = 48美元，因此48美元歸因於「曝光數1」。

* 如果報表引數指定使用原始值做為閱覽，則閱覽權重不會套用至閱覽，而完整的120美元會歸因於「曝光數1」。

+++

<!-- end examples as collapsible content -->

## 加權第一個事件更多

將轉換歸因於發生在廣告商的[點按回顧視窗](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧視窗](/help/search-social-commerce/glossary.md#i-j)內的系列中的所有事件，但給予第一個事件最大權重，並連續給予以下事件較小的權重。此規則僅適用於單一裝置上的事件。

當轉換之前只有曝光數時，轉換會視為&#x200B;*檢視*，其會根據廣告商的[檢視權數設定](/help/search-social-commerce/glossary.md#uv)加權，或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法加權。

當轉換路徑包含付費點按次數和曝光數時，曝光數會依不同的Adobe Advertising產品而以不同的方式處理：

* 在Search、Social和Commerce中，[曝光覆寫權數](/help/search-social-commerce/glossary.md#i-j) （在廣告商的曝光覆寫權數設定中以及報表、檢視或自訂模擬引數中指定）會先套用至曝光數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會在歸因中考量曝光數覆寫權重。

![加權第一個事件更多歸因百分比](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "加權第一個事件更多歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換120美元

歸因：按一下1 = 60 USD、按一下2 = 40 USD、按一下3 = 20 USD （總計120 USD）

### 包含曝光次數和點按次數的範例

**注意：**&#x200B;曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### (僅限搜尋、社交和Commerce)使用10%的預設「曝光覆寫權重」

由於事件序列同時包含曝光次數和點按次數，曝光覆寫權數會套用至曝光次數。

歸因：曝光數1 = 8美元，點選次數1 = 72美元，曝光數2 = 4美元，點選次數2 = 36美元（總計120美元）

#### (僅限DSP)不使用「曝光覆寫權數」或(僅限搜尋、Social和Commerce) 0%的「曝光覆寫權數」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因：曝光數1 = 0 USD、點選次數1 = 80 USD、曝光數2 = 0 USD、點選次數2 = 40 USD （總計120 USD）

### 具有所有曝光的範例

**注意：**&#x200B;只有顯示廣告的曝光數才適用。

事件路徑：曝光次數1、曝光次數2、曝光次數3、轉換120美元

因為轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每次曝光的值：

* 如果報表引數指定了加權的檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則印象1 = 24美元，印象2 = 16美元，印象3 = 8美元（總計48美元）

* 如果報表引數指定使用原始值作為閱覽，則閱覽權重不會套用至曝光數，而完整的120美元會分為三個曝光數：曝光數1 = 60美元、曝光數2 = 40美元、曝光數3 = 20美元（總計120美元）

+++

<!-- end examples as collapsible content -->

## 均勻分佈

>[!NOTE]
>
>此規則僅適用於單一裝置上的事件。

將轉換平均歸因於發生在廣告商的[點按回顧期間](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)內的一系列中的每個事件。

當轉換之前只有曝光數時，轉換會視為&#x200B;*檢視*，其會根據廣告商的[檢視權數設定](/help/search-social-commerce/glossary.md#uv)加權，或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法加權。

當轉換路徑包含付費點按次數和曝光數時，曝光數會依不同的Adobe Advertising產品而以不同的方式處理：

* 在Search、Social和Commerce中，[曝光覆寫權數](/help/search-social-commerce/glossary.md#i-j) （在廣告商的曝光覆寫權數設定中以及報表、檢視或自訂模擬引數中指定）會先套用至曝光數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會在歸因中考量曝光數覆寫權重。

![偶數歸因百分比](/help/search-social-commerce/assets/attribution-percent-even.png "偶數歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換120美元

沒有印象會導致轉換，因此印象覆寫權重不適用，並且轉換在三次點按之間平均分配：

歸因：按一下1 = 40 USD、按一下2 = 40 USD、按一下3 = 40 USD （總計120 USD）

### 包含曝光次數和點按次數的範例

**注意：**&#x200B;曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### (僅限搜尋、社交和Commerce)使用10%的預設「曝光覆寫權重」

由於事件序列同時包含曝光次數和點按次數，曝光覆寫權數會套用至曝光次數。

歸因：曝光數1 = 6美元，點選次數1 = 54美元，曝光數2 = 6美元，點選次數2 = 54美元（總計120美元）

#### (僅限Adobe Advertising DSP)不使用「曝光覆寫權數」或(僅限搜尋、Social和Commerce) 0%的「曝光覆寫權數」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因：曝光數1 = 0 USD、點選次數1 = 60 USD、曝光數2 = 0 USD、點選次數2 = 60 USD （總計120 USD）

## 具有所有曝光的範例

**注意：**&#x200B;只有顯示廣告的曝光數才適用。

事件路徑：曝光次數1、曝光次數2、曝光次數3、轉換120美元

因為轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每次曝光的值：

* 如果報表引數指定了加權的檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則Impression 1 = 16 USD、Impression 2 = 16 USD、Impression 3 = 16 USD （總計48 USD）

* 如果報表引數指定使用原始值作為閱覽，則閱覽權重不會套用至曝光數，而完整的120美元會分為三個曝光數：曝光數1 = 40美元、曝光數2 = 40美元、曝光數3 = 40美元（總計120美元）

+++

<!-- end examples as collapsible content -->

## 加權最後一個事件更多

將轉換歸因於發生在廣告商的[點按回顧視窗](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧視窗](/help/search-social-commerce/glossary.md#i-j)內的系列中的所有事件，但給予最後一個事件最大的權重，並連續減少對先前事件的權重。

當轉換之前只有曝光數時，轉換會視為&#x200B;*檢視*，其會根據廣告商的[檢視權數設定](/help/search-social-commerce/glossary.md#uv)加權，或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法加權。

當轉換路徑包含付費點按次數和曝光數時，曝光數會依不同的Adobe Advertising產品而以不同的方式處理：

* 在Search、Social和Commerce中，[曝光覆寫權數](/help/search-social-commerce/glossary.md#i-j) （在廣告商的曝光覆寫權數設定中以及報表、檢視或自訂模擬引數中指定）會先套用至曝光數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會在歸因中考量曝光數覆寫權重。

![加權最後一個事件更多歸因百分比](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "加權最後一個事件更多歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換120美元

歸因：按一下3 = 60 USD、按一下2 = 40 USD、按一下1 = 20 USD （總計120 USD）

### 包含曝光次數和點按次數的範例

**注意：**&#x200B;曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### (僅限搜尋、社交和Commerce)使用10%的預設「曝光覆寫權重」

由於事件序列同時包含曝光次數和點按次數，曝光覆寫權數會套用至曝光次數。

歸因：曝光數1 = 4美元，點選次數1 = 36美元，曝光數2 = 8美元，點選次數2 = 72美元（總計120美元）

#### (僅限DSP)不使用「曝光覆寫權數」或(僅限搜尋、Social和Commerce) 0%的「曝光覆寫權數」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因：曝光數1 = 0 USD、點選次數1 = 40 USD、曝光數2 = 0 USD、點選次數2 = 80 USD （總計120 USD）

### 具有所有曝光的範例

**注意：**&#x200B;曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Impression 2、Impression 3、120美元的轉換

因為轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每次曝光的值：

* 如果報表引數指定了加權的檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則將「包含所有點按的範例」中的每個值乘以40%：Impression 3 = 24 USD， Impression 2 = 16 USD， Impression 1 = 8 USD （總計48 USD）

* 如果報表引數指定使用原始值作為閱覽，則完整的120 USD會由曝光數平分：曝光數3 = 60 USD、曝光數2 = 40 USD、曝光數1 = 20 USD （總計120 USD）

+++

<!-- end examples as collapsible content -->

## U形

將轉換歸因於發生在廣告商的[點按回顧視窗](/help/search-social-commerce/glossary.md#c-d)和[曝光回顧視窗](/help/search-social-commerce/glossary.md#i-j)內的系列中的所有事件，但給予第一個事件和最後一個事件的權重最大，連續減少對轉換路徑中間事件的權重。

當轉換之前只有曝光數時，轉換會視為&#x200B;*檢視*，其會根據廣告商的[檢視權數設定](/help/search-social-commerce/glossary.md#uv)加權，或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法加權。

當轉換路徑包含付費點按次數和曝光數時，曝光數會依不同的Adobe Advertising產品而以不同的方式處理：

* 在Search、Social和Commerce中，[曝光覆寫權數](/help/search-social-commerce/glossary.md#i-j) （在廣告商的曝光覆寫權數設定中以及報表、檢視或自訂模擬引數中指定）會先套用至曝光數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會在歸因中考量曝光數覆寫權重。

![U形歸因百分比](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U形歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、按一下4、轉換120美元

歸因：按一下1 = 36美元，按一下2 = 24美元，按一下3 = 24美元，按一下4 = 36美元（總計120美元）

### 包含曝光次數和點按次數的範例

**注意：**&#x200B;曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### (僅限搜尋、社交和Commerce)使用10%的預設「曝光覆寫權重」

由於事件序列同時包含曝光次數和點按次數，曝光覆寫權數會套用至曝光次數。

歸因：曝光數1 = 6美元，點選次數1 = 54美元，曝光數2 = 6美元，點選次數2 = 54美元（總計120美元）

#### 使用(僅限DSP)無曝光覆寫權數，或(僅限搜尋、Social和Commerce)0%的「曝光覆寫權數」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因：曝光數1 = 0 USD、點選次數1 = 60 USD、曝光數2 = 0 USD、點選次數2 = 60 USD （總計120 USD）

### 具有所有曝光的範例

**注意：**&#x200B;只有顯示廣告的曝光數才適用。

事件路徑：曝光次數1、曝光次數2、曝光次數3、曝光次數4、轉換120美元

因為轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每次曝光的值：

* 如果報表引數指定了加權的檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則按一下1 = 14.40 USD，按一下2 = 9.60 USD，按一下3 = 9.60 USD，按一下4 = 14.40 USD （總計48 USD）

* 如果報表引數指定使用原始值作為閱覽，則完整的120 USD會由曝光數平分：按一下1 = 36 USD、按一下2 = 24 USD、按一下3 = 24 USD、按一下4 = 36 USD （總計120 USD）

+++

<!-- end examples as collapsible content -->
