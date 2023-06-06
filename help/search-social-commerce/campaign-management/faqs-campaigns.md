---
title: 行銷活動常見問題集
description: 檢視有關行銷活動管理和行銷活動資料檢視問題的解答。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# 行銷活動管理常見問題集

## 一般資訊

+++我是否可以將行銷活動和元件從某個帳戶移至另一個帳戶？

請勿將具有唯一ID的行銷活動或行銷活動元件移動或複製到具有不同帳戶ID的帳戶。 這麼做會導致資料錯誤。
+++

+++何時會從廣告網路更新點按資料？

從搜尋引擎提取前一天點選資料的程式於06:00在廣告商的時區開始。

此外， [!DNL Google Ads] 搜尋網路上當天的行銷活動層級績效量度在廣告商時區的08:00和16:00提取。
+++

+++哪些動作會造成關鍵字和廣告遺失歷史記錄？

>[!NOTE]
>
>（擁有產品組合的廣告商）在Search、Social和Commerce收集資料以建立新模型時，期望新關鍵字和相符型別組合的效能不穩定。

**中的動作 [!UICONTROL Search] > [!UICONTROL Campaigns] 檢視、在Bulksheet發佈程式中，以及在廣告網路自己的編輯器中：**

刪除現有關鍵字或廣告，並在以下情況下建立另一個關鍵字或廣告：

* ([!DNL Baidu]， [!DNL Google Ads]、和 [!DNL Yandex])您可以編輯關鍵字名稱。

* ([!DNL Google Ads]， [!DNL Microsoft Advertising]、和 [!DNL Yandex])您變更關鍵字的相符型別。

* 您可以在廣告群組之間移動關鍵字。

* ([!DNL Google Ads] 動態搜尋廣告， [!DNL Microsoft Advertising] 展開文字廣告，以及其他支援的廣告網路上的所有廣告型別)您可以編輯廣告文案（標題/標題或說明）或廣告影像。

* 您可以在廣告群組之間移動廣告。

**產品存貨摘要過帳程式中的事件：**

在下列情況下，現有廣告或關鍵字會遭到刪除，並建立另一個廣告或關鍵字：

* 摘要檔案包含在廣告變數中使用的欄的新值。

* 自上次傳播後，廣告的範本設定已變更。

* 新的摘要檔案中包含的廣告或關鍵字列，說明a)在先前的檔案中，但b)從那時起已被省略，並已根據摘要資料設定暫停或刪除。

根據 [摘要資料設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)，則在下列情況下可能會刪除現有廣告或關鍵字：

* 新的摘要檔案不包含現有廣告或關鍵字的列。

* 已發佈摘要檔案之元件的排程結束日期發生。

* 料號的庫存量會降至摘要資料設定中指定的最小值以下。
+++

+++([!DNL Google Ads] campaigns)變更我的的 [!DNL Google]已還原 — tracked轉換。

如果您在「搜尋」、「社交」和「商務」中變更交易屬性的顯示名稱，您的變更會以設定的名稱覆寫。 [!DNL Google Ads]. 在內變更任何名稱 [!DNL Google Ads].
+++

+++(Google Ads行銷活動)我可以在產品組合中使用共用預算進行行銷活動嗎？

為了獲得最佳結果，請勿新增 [!DNL Google Ads] 行銷活動至 [!DNL Google Ads] 共用預算（如果他們位在最佳化的產品組合中）」[!UICONTROL Auto adjust campaign budget limits].」 如果您這麼做， [!DNL Google Ads] 覆寫「搜尋、Social和商務」最佳化的行銷活動預算，這可能會導致競標效率低下。
+++

+++([!DNL Google Ads] 行銷活動)是否可將行動和非行動使用者傳送至不同的登陸頁面？

您可以使用 [!DNL Google Ads] [!DNL ValueTrack] 引數 `{ifmobile}` 和 `{ifnotmobile}` 若要使用適用於您網站的兩種方式之一，判斷登入頁面的網域名稱：

* 使用以下專案將行動裝置指定為主機伺服器 `{ifmobile:m}{ifnotmobile:www}`.

   例如， `http://{ifmobile:m}{ifnotmobile:www}.example.com` 將行動使用者帶至m.example.com，將非行動使用者帶至www.example.com。

* 使用以下專案將行動裝置指定為頂級網域： `{ifmobile:mobi}{ifnotmobile:com}`.

   例如， `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` 將行動使用者帶至www.example.mobi，將非行動使用者帶至www.example.com。

在這兩種情況下，具有搜尋、社交和商務追蹤的基礎URL都會包含未編碼的 `{}` 標籤和附加至基底URL的任何其他引數。

>[!NOTE]
>
>請勿使用完整URL做為ifnotmobile和ifmobile引數的值；僅使用URL的變數部分（例如「m」與「www」或「mobi」與「com」）。

+++

+++([!DNL Google Ads] 搜尋網路上的行銷活動)今日顯示哪些資料？

[!DNL Google Ads] 搜尋網路上當天的行銷活動層級績效量度在廣告商時區的08:00和16:00提取。

在 [!UICONTROL Campaigns] 標籤中的文字 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 檢視和 [!UICONTROL Optimization] > [!UICONTROL Portfolios] 檢視，當您針對 [!UICONTROL Today] 或是包含當天的自訂日期範圍，資料將包含最近提取的資料。

>[!NOTE]
>
>點按、曝光和轉換的資料會延遲三個小時，直到下次提取資料時才會完成。

+++

+++([!DNL Google Ads] 和 [!DNL Microsoft Advertising])搜尋、社交和商務是否支援對中的廣告進行平行追蹤 [!DNL Google Ads] 或 [!DNL Microsoft Advertising]？

平行追蹤會將客戶直接從您的廣告傳送至最終URL，而您的追蹤範本URL （包含點選測量）會載入背景；因此，您的登入頁面載入更快。

搜尋、社交和商務支援使用廣告網路的點選識別碼(`msclkid` 的 [!DNL Microsoft Advertising]； `gclid` 的 [!DNL Google Ads])。 使用 [帳戶層級](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) 或 [行銷活動層級](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (稱為&quot;[!DNL final URL suffix]&quot;在廣告網路中)，會附加至登陸頁面URL，以追蹤來自支援平行追蹤之瀏覽器的子廣告點按。 請參閱 [必要的字尾格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) 和 [必要的字尾格式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

當使用者在不支援平行追蹤的瀏覽器上檢視您的廣告時，廣告網路會改用循序追蹤：客戶會先傳送至您的追蹤範本URL，這樣可能會先將客戶重新導向至中繼追蹤伺服器，然後再重新導向至最終URL。 廣告網路帳戶的所有追蹤範本都應包含您在中使用的相同點選識別碼引數 [!UICONTROL Landing Page Suffix]. 請參閱 [追蹤範本格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) 和 [追蹤範本格式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++為什麼我的廣告的追蹤URL包含&quot;`&EV_HASH={<hash>}`？」

當您使用上傳廣告時 [產品詳細目錄摘要](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 若帳戶具有「搜尋、Social和商務」畫素重新導向，以及關鍵字和創意層級追蹤，則「搜尋、Social和商務」會將雜湊引數和值新增至廣告的追蹤範本或目的地URL，以識別其是使用詳細目錄摘要功能建立的。
+++

## 詳細目錄摘要

+++（產品詳細目錄摘要）我是否應該暫停或刪除過時廣告，或適用於庫存量低於指定最小值的產品的廣告？

這取決於廣告商的業務需求。

當您暫停廣告時，如果您重新提交相同的廣告或庫存水準高於最低值，廣告就會重新啟用。 這可讓您保留廣告的歷史記錄。

當您刪除並重新提交廣告時，會建立新廣告，且需要累積歷史資料。 不過，如果您不想重新提交已刪除的廣告，則擁有歷史資料並不重要。
+++

+++（產品詳細目錄摘要）如果我刪除廣告範本然後建立新的相同範本，下一個摘要檔案中的遺漏專案會暫停（當摘要檔案設定已設定這樣做時）嗎？

如果下一個摘要檔案缺少行專案，而您先前未透過先前的摘要檔案從新範本張貼這些行專案，則缺少的行專案不會識別為「遺失」，因此不會建立它們。 若要避免此問題，請在傳播及張貼新檔案的資料之前，透過新範本傳播上一個摘要檔案並張貼資料。
+++

+++（產品詳細目錄摘要）我可以在不影響廣告品質分數的情況下更新產品價格嗎？

對象 [!DNL Google Ads] 行銷活動，是： [!DNL Google Ads] `{Param 1}` 和 `{Param 2}` 變數可讓您在廣告變數中動態插入數值，而不會刪除和重新建立廣告，因此不會影響品質分數。

若要使用 `{Param 1}` 或 `{Param 2}` 變數，將資料檔案中的「價格」欄對應至適當摘要範本中的該變數，然後將變數納入您的廣告變數範本中。

例如，如果欄名為「Price」，然後開啟建立廣告的摘要範本，按一下旁邊的輸入欄位 **[!UICONTROL Param 1]**，然後按一下 **[!UICONTROL Price]** 中的欄 [!UICONTROL Feeds/Available Columns] 清單，其中插入 `[Price]` 作為的值 [!UICONTROL Param 1]. 然後，在摘要範本底部的廣告變數範本中，插入 `{param1:default text}`，其中「預設文字」為文字，可在摘要檔案中的引數欄為廣告列空白時使用。

當您提交資料時，的資料欄位 [!UICONTROL Param1] 和 [!UICONTROL Param2] 欄最多可包含25個字元，包括數值資料、貨幣符號和貨幣代碼，以及下列非數值字元： `, . % + - /`
+++

+++從存貨摘要產生的行銷活動有許多孤立交易。

如果 [摘要資料設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) 設定為刪除各種情況下的廣告，則點選廣告後發生的任何延遲轉換都可能導致 [孤立交易](/help/search-social-commerce/glossary.md#o-p). 最佳實務是暫停廣告，而非刪除廣告。 如果廣告在長時間後仍未收到任何收入，您可以透過Bulksheet或廣告管理檢視將其刪除。
+++

## 帳戶和行銷活動相關的效能問題

+++我的一些行銷活動所花費的金額或多或少於行銷活動預算。

* 在最佳化的產品組合中，這是正常的，設定有&quot;[!UICONTROL Auto-adjust campaign budget limits]」選項。 啟用此選項後，您最多可能會花費 *N* 乘以每個行銷活動的預算，其中 *N* 是「」的值[!UICONTROL Multiple]」設定。 此選項可讓最佳化功能視需要調整個別行銷活動的支出，同時引導整個產品組合達成其目標。
* 若 [!DNL Google Ads] 行銷活動使用共用預算，然後 [!DNL Google Ads] 會視需要調整個別行銷活動的支出，以花費整個共用預算。
+++
