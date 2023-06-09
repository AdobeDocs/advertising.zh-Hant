---
title: 歸因規則的計算方式
description: 瞭解Adobe Advertising如何計算每種型別的歸因規則。
source-git-commit: d4237253af7110a3ed02595c466c01359f5601d4
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# 如何針對Adobe Advertising計算歸因規則

*僅具有Adobe廣告轉換追蹤的廣告商*

<!-- Verify statements about cross-device events -->

廣告商層級歸因規則是用來將轉換資料（可能跨多個廣告管道）歸因於一系列導致轉換的事件。

在Advertising Search、Social和Commerce （Search、Social和Commerce）的報表預設和自訂檢視以及Search、Social和Commerce （某些使用者角色）的產品組合層級模擬中，選取的規則僅用於檢視、報表或模擬資料。 各種歸因規則的套用方式如下。

>[!NOTE]
>
>* 歸因規則適用於任何頻道中付費廣告的點按次數，以及顯示廣告和社交廣告的曝光數。 它們不適用於付費搜尋廣告的曝光，無法在事件層級追蹤。
>* Adobe Advertising一律會在轉換前為每個網路瀏覽者儲存下列事件： a)第一次付費點選； b)每個管道最多10次點選（搜尋、社交或顯示），包括第一次點選；以及c)最多10次顯示曝光次數。 <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* 在Advertising DSP和Advertising Creative中，跨裝置定義只會考慮所選歸因規則中的事件路徑。<!-- cross-device attribution via LiveRamp only -->
* 在報表和管理檢視中，為某個值顯示的小數位數會依貨幣而定，但Adobe Advertising會儲存更精確的值。

## 上一個事件（預設）

將轉換歸因於廣告商的系列內最後一次付費點選 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 或者，如果沒有發生付費點按，則為廣告商的最近一次曝光 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).

如果轉換之前只有曝光次數，則會將轉換視為 *檢視*，此量度會根據廣告商的 [檢視權數設定](/help/search-social-commerce/glossary.md#uv) 或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法。

![上一個事件歸因百分比](/help/search-social-commerce/assets/attribution-percent-last-event.png "上一個事件歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑： Click1、Click2、Click3、轉換120美元

轉換歸因於Click 3，金額為120美元。

### 同時包含曝光次數和點按次數的範例

**注意：** 曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、轉換120美元

轉換的金額為120美元，歸因於Click 1。

### 具有所有曝光數的範例

**注意：** 僅適用於顯示廣告和社交廣告的曝光數。

事件路徑： Impression 1、Impression 2、Impression 3、120美元的轉換

轉換歸因於印象3。 由於轉換是檢視，所以會套用報表設定的「轉換歸因」區段中選取的檢視估價方法：

* 如果報表引數指定了加權檢視權數，則該權重會套用至檢視。 例如，如果廣告商的瀏覽權數為40%，則120 USD x 40% = 48 USD，因此48 USD歸因於「印象3」。

* 如果報表引數指定使用原始值做為閱覽，則閱覽權重不會套用至閱覽，而完整的120美元會歸因於「印象3」。

+++

<!-- end examples as collapsible content -->

## 第一個事件

將轉換歸因於廣告商的系列中的第一個付費點選 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 或者，如果沒有發生付費點按，則為廣告商網站內的首次曝光 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). 此規則僅適用於單一裝置上的事件。

當轉換之前只有曝光時，轉換會被視為 *檢視*，此量度會根據廣告商的 [檢視權數設定](/help/search-social-commerce/glossary.md#uv) 或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法。

![第一個事件歸因百分比](/help/search-social-commerce/assets/attribution-percent-first-event.png "第一個事件歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換120美元

轉換的金額為120美元，歸因於Click 1。

### 同時包含曝光次數和點按次數的範例

**注意：** 曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、轉換120美元

轉換的金額為120美元，歸因於Click 1。

### 具有所有曝光數的範例

**注意：** 僅適用於顯示廣告和社交廣告的曝光數。

事件路徑： Impression 1、Impression 2、Impression 3、120美元的轉換

轉換歸因於印象1。 由於轉換是檢視，因此會套用報表設定的「（顯示促銷活動）轉換歸因」區段中選取的檢視估價方法：

* 如果報表引數指定了加權檢視權數，則該權重會套用至檢視。 例如，如果廣告商的瀏覽權數為40%，則120 x 40% = 48美元，因此48美元歸因於「印象1」。

* 如果報表引數指定使用原始值做為閱覽，則閱覽權重不會套用至閱覽，而完整的120美元會歸因於「曝光數1」。

+++

<!-- end examples as collapsible content -->

## 權重第一個事件更多

將轉換歸因於廣告商發生的一系列中的所有事件 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)，但會給予第一個事件最大的權重，並連續給予以下事件較小的權重。此規則僅適用於單一裝置上的事件。

當轉換之前只有曝光時，轉換會被視為 *檢視*，此量度會根據廣告商的 [檢視權數設定](/help/search-social-commerce/glossary.md#uv) 或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法。

當轉換路徑包含付費點按和曝光數時，不同的Adobe廣告產品會以不同的方式處理曝光數：

* 在搜尋、社交和商務中， [印象覆寫權重](/help/search-social-commerce/glossary.md#i-j)  — 在廣告商的曝光次數覆寫權重設定中以及在報表、檢視或自訂模擬引數中指定的 — 會先套用至曝光次數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會將曝光次數覆寫權重納入歸因考量。

![權重第一個事件更多歸因百分比](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "權重第一個事件更多歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換120美元

歸因：按一下1 = 60 USD、按一下2 = 40 USD、按一下3 = 20 USD （總計120 USD）

### 同時包含曝光次數和點按次數的範例

**注意：** 曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### （僅限搜尋、Social和Commerce）使用10%的預設「曝光覆蓋權重」

由於事件序列同時包含曝光次數和點按次數，因此曝光次數覆寫權數會套用至曝光。

歸因： Impression 1 = 8 USD、Click 1 = 72 USD、Impression 2 = 4 USD、Click 2 = 36 USD （總計120 USD）

#### 使用(僅限DSP)無曝光覆寫權重或（僅限搜尋、Social和Commerce） 0%的「曝光覆寫權重」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因： Impression 1 = 0 USD、Click 1 = 80 USD、Impression 2 = 0 USD、Click 2 = 40 USD （總計120 USD）

### 具有所有曝光數的範例

**注意：** 只適用於顯示廣告的曝光數。

事件路徑： Impression 1、Impression 2、Impression 3、120美元的轉換

由於轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每個曝光的值：

* 如果報表引數指定了加權檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則「曝光數1 = 24美元」、「曝光數2 = 16美元」、「曝光數3 = 8美元」（總計48美元）

* 如果報表引數指定使用原始值做為閱覽，則閱覽權重不會套用至曝光，而完整的120美元會分成三個曝光：曝光1 = 60美元、曝光2 = 40美元、曝光3 = 20美元（總計120美元）

+++

<!-- end examples as collapsible content -->

## 均勻分佈

>[!NOTE]
>
>此規則僅適用於單一裝置上的事件。

將轉換同等地歸因於廣告商活動中發生的系列每個事件 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).

當轉換之前只有曝光時，轉換會被視為 *檢視*，此量度會根據廣告商的 [檢視權數設定](/help/search-social-commerce/glossary.md#uv) 或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法。

當轉換路徑包含付費點按和曝光數時，不同的Adobe廣告產品會以不同的方式處理曝光數：

* 在搜尋、社交和商務中， [印象覆寫權重](/help/search-social-commerce/glossary.md#i-j)  — 在廣告商的曝光次數覆寫權重設定中以及在報表、檢視或自訂模擬引數中指定的 — 會先套用至曝光次數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會將曝光次數覆寫權重納入歸因考量。

![平均歸因百分比](/help/search-social-commerce/assets/attribution-percent-even.png "平均歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換成120美元

沒有印象會導致轉換，因此印象覆寫權重不適用，並且轉換會平均分配到三次點按：

歸因：按一下1 = 40 USD、按一下2 = 40 USD、按一下3 = 40 USD （總計120 USD）

### 同時包含曝光次數和點按次數的範例

**注意：** 曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### （僅限搜尋、Social和Commerce）使用10%的預設「曝光覆蓋權重」

由於事件序列同時包含曝光次數和點按次數，因此曝光次數覆寫權數會套用至曝光次數。

歸因： Impression 1 = 6 USD、Click 1 = 54 USD、Impression 2 = 6 USD、Click 2 = 54 USD （總計120 USD）

#### 使用(僅限AdobeAdvertising DSP)無曝光次數覆寫權數，或（僅限搜尋、Social和Commerce） 0%的「曝光次數覆寫權數」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因： Impression 1 = 0 USD、Click 1 = 60 USD、Impression 2 = 0 USD、Click 2 = 60 USD （總計120 USD）

## 具有所有曝光數的範例

**注意：** 只適用於顯示廣告的曝光數。

事件路徑： Impression 1、Impression 2、Impression 3、120美元的轉換

由於轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每個曝光的值：

* 如果報表引數指定了加權檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則「曝光數1 = 16美元」、「曝光數2 = 16美元」、「曝光數3 = 16美元」（總計48美元）

* 如果報表引數指定使用原始值做為閱覽，則閱覽權重不會套用至曝光，而完整的120美元會分成三個曝光：曝光1 = 40美元、曝光2 = 40美元、曝光3 = 40美元（總計120美元）

+++

<!-- end examples as collapsible content -->

## 加權最後一個事件更多

將轉換歸因於廣告商發生的一系列中的所有事件 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)，但會給予最後一個事件最多權重，並連續給予前一個事件較少權重。

當轉換之前只有曝光時，轉換會被視為 *檢視*，此量度會根據廣告商的 [檢視權數設定](/help/search-social-commerce/glossary.md#uv) 或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法。

當轉換路徑包含付費點按和曝光數時，不同的Adobe廣告產品會以不同的方式處理曝光數：

* 在搜尋、社交和商務中， [印象覆寫權重](/help/search-social-commerce/glossary.md#i-j)  — 在廣告商的曝光次數覆寫權重設定中以及在報表、檢視或自訂模擬引數中指定的 — 會先套用至曝光次數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會將曝光次數覆寫權重納入歸因考量。

![權重上一個事件更多歸因百分比](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "權重上一個事件更多歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、轉換120美元

歸因：按一下3 = 60 USD、按一下2 = 40 USD、按一下1 = 20 USD （總計120 USD）

### 同時包含曝光次數和點按次數的範例

**注意：** 曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### （僅限搜尋、Social和Commerce）使用10%的預設「曝光覆蓋權重」

由於事件序列同時包含曝光次數和點按次數，因此曝光次數覆寫權數會套用至曝光次數。

歸因： Impression 1 = 4 USD、Click 1 = 36 USD、Impression 2 = 8 USD、Click 2 = 72 USD （總計120 USD）

#### 使用(僅限DSP)無曝光覆寫權重或（僅限搜尋、Social和Commerce） 0%的「曝光覆寫權重」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因： Impression 1 = 0 USD、Click 1 = 40 USD、Impression 2 = 0 USD、Click 2 = 80 USD （總計120 USD）

### 具有所有曝光數的範例

**注意：** 曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Impression 2、Impression 3、120美元的轉換

由於轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每個曝光的值：

* 如果報表引數指定了加權檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則將「包含所有點按的範例」中的每個值乘以40%：Impression 3 = 24 USD， Impression 2 = 16 USD， Impression 1 = 8 USD （總計48 USD）

* 如果報表引數指定使用原始值做為閱覽，則完整的120 USD會由曝光數平分：曝光3 = 60 USD、曝光2 = 40 USD、曝光1 = 20 USD （總計120 USD）

+++

<!-- end examples as collapsible content -->

## U形

將轉換歸因於廣告商發生的一系列中的所有事件 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)，但會給予第一個事件和最後一個事件最大的權重，而連續給予轉換路徑中間事件的權重較低。

當轉換之前只有曝光時，轉換會被視為 *檢視*，此量度會根據廣告商的 [檢視權數設定](/help/search-social-commerce/glossary.md#uv) 或 — 依指定 — 根據報表、檢視或自訂模擬引數中指定的檢視估價方法。

當轉換路徑包含付費點按和曝光數時，不同的Adobe廣告產品會以不同的方式處理曝光數：

* 在搜尋、社交和商務中， [印象覆寫權重](/help/search-social-commerce/glossary.md#i-j)  — 在廣告商的曝光次數覆寫權重設定中以及在報表、檢視或自訂模擬引數中指定的 — 會先套用至曝光次數。

* 在DSP中，會忽略曝光數，只有點按次數會加權。 DSP不會將曝光次數覆寫權重納入歸因考量。

![U形歸因百分比](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U形歸因百分比")

<!-- start examples as collapsible content -->

+++事件計算範例

### 包含所有點按的範例

事件路徑：按一下1、按一下2、按一下3、按一下4、轉換120美元

歸因：按一下1 = 36 USD、按一下2 = 24 USD、按一下3 = 24 USD、按一下4 = 36 USD （總計120 USD）

### 同時包含曝光次數和點按次數的範例

**注意：** 曝光次數僅適用於顯示廣告和社交廣告。

事件路徑： Impression 1、Click 1、Impression 2、Click 2、120美元的轉換

#### （僅限搜尋、Social和Commerce）使用10%的預設「曝光覆蓋權重」

由於事件序列同時包含曝光次數和點按次數，因此曝光次數覆寫權數會套用至曝光次數。

歸因： Impression 1 = 6 USD、Click 1 = 54 USD、Impression 2 = 6 USD、Click 2 = 54 USD （總計120 USD）

#### 使用(僅限DSP)無曝光覆寫權重或（僅限搜尋、Social和Commerce） 0%的「曝光覆寫權重」

由於事件序列同時包含曝光次數和點按次數，因此會忽略曝光次數。

歸因： Impression 1 = 0 USD、Click 1 = 60 USD、Impression 2 = 0 USD、Click 2 = 60 USD （總計120 USD）

### 具有所有曝光數的範例

**注意：** 只適用於顯示廣告的曝光數。

事件路徑： Impression 1、Impression 2、Impression 3、Impression 4、120美元的轉換

由於轉換是檢視，所以會套用檢視估價方法（而非曝光覆寫權數）來決定每個曝光的值：

* 如果報表引數指定了加權檢視權數，則該權重會套用至曝光值。 例如，如果檢視權重為40%，則按一下1 = 14.40 USD，按一下2 = 9.60 USD，按一下3 = 9.60 USD，按一下4 = 14.40 USD （總計48 USD）

* 如果報表引數指定使用原始值做為閱覽，則完整的120 USD會在曝光之間平分：點按1 = 36 USD、點按2 = 24 USD、點按3 = 24 USD、點按4 = 36 USD （總計120 USD）

+++

<!-- end examples as collapsible content -->
