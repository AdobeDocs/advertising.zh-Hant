---
title: 行銷活動的相關常見問題集
description: 檢視有關行銷活動管理和行銷活動資料檢視的問答。
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 88b415fff52d623a5daeb00355bfe00054d5402b
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# 關於行銷活動管理的常見問題集

## 一般資訊

+++我是否可以將行銷活動和元件從某個帳戶移至另一個帳戶？

請勿將具有唯一ID的行銷活動或行銷活動元件移動或複製到具有不同帳戶ID的帳戶。 這樣做會導致資料錯誤。
+++

+++何時會從廣告網路更新點按資料？

從搜尋引擎提取前一天點選資料的程式從廣告商時區的06:00開始。

此外，在廣告商時區的搜尋網路上，當天的[!DNL Google Ads]行銷活動層級效能量度分別提取到08:00和16:00。
+++

+++哪些動作會造成關鍵字和廣告遺失歷史記錄？

>[!NOTE]
>
>（擁有產品組合的廣告商）搜尋、Social和Commerce收集資料以建立模型時，期望新關鍵字和相符型別組合的效能不穩定。

**動作（在[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns]檢視中、在Bulksheet張貼程式中，以及在廣告網路自己的編輯器中）：**

在下列情況下，現有關鍵字或廣告會遭到刪除，並會建立另一個關鍵字或廣告：

* （[!DNL Baidu]、[!DNL Google Ads]和[!DNL Yandex]）您編輯關鍵字名稱。

* （[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yandex]）您變更關鍵字的相符型別。

* 您可以在廣告群組之間移動關鍵字。

* （[!DNL Google Ads]個動態搜尋廣告、[!DNL Microsoft Advertising]個展開的文字廣告，以及其他支援的廣告網路上的所有廣告型別）您可以編輯廣告文案（標題/標題或說明）或廣告影像。

* 您可以在廣告群組之間移動廣告。

**產品詳細目錄摘要過帳程式中的事件：**

在下列情況下，現有廣告或關鍵字會被刪除，並會建立另一個廣告或關鍵字：

* 摘要檔案包含在廣告變數中使用的欄的新值。

* 自上次傳播後，廣告的範本設定已變更。

* 新的摘要檔案包含的廣告或關鍵字列，其中a)在先前的檔案中，但b)在之後已省略，並根據摘要資料設定暫停或刪除。

根據[摘要資料設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)，在下列情況下可能會刪除現有的廣告或關鍵字：

* 新的摘要檔案不包含現有廣告或關鍵字的列。

* 已發佈摘要檔案之元件的排程結束日期發生。

* 專案的庫存量會降至摘要資料設定中指定的最低值以下。
+++

+++（[!DNL Google Ads]個行銷活動）我的[!DNL Google]追蹤轉換的顯示名稱變更已還原。

如果您在「搜尋」、「社交」和「Commerce」中變更轉換量度的顯示名稱，您的變更會以[!DNL Google Ads]中設定的名稱覆寫。 在[!DNL Google Ads]中進行任何名稱變更。
+++

+++(Google Ads行銷活動)我可以在產品組合中使用行銷活動的共用預算嗎？

為了獲得最佳結果，如果[!DNL Google Ads]行銷活動位於設定為「[!DNL Google Ads]」的最佳化產品組合，請勿將其新增至[!UICONTROL Auto adjust campaign budget limits]共用預算。 若您這麼做，[!DNL Google Ads]會覆寫Search、Social和Commerce最佳化的行銷活動預算，這可能會造成競標效率低下。
+++

+++（[!DNL Google Ads]個行銷活動）我是否可將行動和非行動使用者傳送至不同的登陸頁面？

您可以使用[!DNL Google Ads] [!DNL ValueTrack]引數`{ifmobile}`和`{ifnotmobile}`，以下列兩種方式之一來判斷登入頁面的網域名稱（如適用於您的網站）：

* 使用`{ifmobile:m}{ifnotmobile:www}`將行動裝置指定為主機伺服器。

  例如，`http://{ifmobile:m}{ifnotmobile:www}.example.com`會將行動使用者帶至m.example.com，將非行動使用者帶至www.example.com。

* 使用`{ifmobile:mobi}{ifnotmobile:com}`將行動裝置指定為最上層網域。

  例如，`http://www.example.{ifmobile:mobi}{ifnotmobile:com}`會將行動使用者帶至www.example.mobi，將非行動使用者帶至www.example.com。

在這兩種情況下，具有搜尋、社交和Commerce追蹤的基礎URL都會包含未編碼的`{}`標籤以及附加至基礎URL的任何其他引數。

>[!NOTE]
>
>請勿使用完整URL作為ifnotmobile和ifmobile引數的值；請只使用URL的變數部分（例如「m」與「www」或「mobi」與「com」）。

+++

+++（[!DNL Google Ads]個搜尋網路行銷活動）今日顯示哪些資料？

在廣告商時區的搜尋網路上，當天的[!DNL Google Ads]行銷活動層級績效量度分別於08:00和16:00提取。

在[!UICONTROL Campaigns] > [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns]檢視和[!UICONTROL Campaigns] > [!UICONTROL Optimization]檢視的[!UICONTROL Portfolios]索引標籤中，當您在[!UICONTROL Today]或包含當天的自訂日期範圍上報告時，資料包含最近同步處理的資料。

>[!NOTE]
>
>點按、曝光和轉換的資料會延遲三個小時，直到下次提取資料時才會完成。

+++

+++追蹤範本和登入頁面尾碼有何不同？

登入頁面尾碼僅用於支援平行追蹤的廣告網路。 在「搜尋、Social和Commerce」中，追蹤範本和登陸頁面尾碼都應包含來自廣告網路的點選識別碼，但追蹤範本應包含其他追蹤引數。

請參閱有關[平行追蹤支援](#parallel-tracking)的下一個常見問題集，以取得使用者按一下廣告時如何載入追蹤範本和登入頁面尾碼的詳細資訊。

+++

+++（[!DNL Google Ads]和[!DNL Microsoft Advertising]）搜尋、社交和Commerce是否支援[!DNL Google Ads]或[!DNL Microsoft Advertising]中廣告的平行追蹤？{#parallel-tracking}

平行追蹤會直接將客戶從您的廣告傳送至最終URL，其中可能包含最終URL尾碼或「登陸頁面尾碼」的附加引數。 您的追蹤範本URL （以及點選測量的其他引數）會單獨在背景中載入，讓您的登入頁面載入更快。

搜尋、社交和Commerce支援使用廣告網路的點選識別碼（`msclkid`為[!DNL Microsoft Advertising]；`gclid`為[!DNL Google Ads]）來平行追蹤搜尋和購物行銷活動。 使用[帳戶層級](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings)或[行銷活動層級](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] （在廣告網路中稱為「[!DNL final URL suffix]」），其會附加至登陸頁面URL，以追蹤來自支援平行追蹤之瀏覽器的子廣告點按。 檢視[的 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)必要尾碼格式和[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)必要尾碼格式。

當使用者在不支援平行追蹤的瀏覽器上檢視您的廣告時，廣告網路會改用循序追蹤：客戶會先傳送至您的追蹤範本URL，這樣可能會先將客戶重新導向至中繼追蹤伺服器，再將其重新導向至最終URL （可能在登入頁面尾碼中包含其他引數）。 廣告網路帳戶的所有追蹤範本都應包含您在[!UICONTROL Landing Page Suffix]中使用的相同點按識別碼引數。 檢視[的 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)追蹤範本格式和[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)追蹤範本格式。
+++

+++為什麼我的廣告的追蹤URL包含&quot;`&EV_HASH={<hash>}`&quot;？

當您針對具有搜尋、社交和Commerce畫素重新導向，以及關鍵字和創意層級追蹤的帳戶，使用[產品詳細目錄摘要](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)上傳廣告時，Search、Social和Commerce會將雜湊引數和值新增至廣告的追蹤範本或目的地URL，以識別其是使用詳細目錄摘要功能建立的。
+++

## 詳細目錄摘要

+++（產品詳細目錄摘要）我是否應該暫停或刪除過時或庫存量低於指定最小值的產品的廣告？

這取決於廣告商的業務需求。

當您暫停廣告時，如果您重新提交相同的廣告或庫存量高於最低值，廣告就會重新啟用。 這可讓您保留廣告的歷史記錄。

當您刪除並重新提交廣告時，將會建立新廣告，而且需要為新廣告累積歷史資料。 不過，如果您不希望重新提交已刪除的廣告，則擁有歷史資料並不重要。
+++

+++（產品詳細目錄摘要）如果我刪除廣告範本然後建立新的相同範本，下一個摘要檔案中是否有遺漏專案已暫停（當摘要檔案設定已設定為這樣做時）？

如果下一個摘要檔案遺失行專案，而您先前未透過先前的摘要檔案從新範本張貼這些行專案，則遺失的行專案不會識別為「遺失」，因此不會建立它們。 若要避免此問題，請透過新範本傳播上一個摘要檔案，並從新檔案傳播及張貼資料之前先張貼資料。
+++

+++（產品詳細目錄摘要）我可以在不影響廣告品質分數的情況下更新產品價格嗎？

對於[!DNL Google Ads]行銷活動，是： [!DNL Google Ads] `{Param 1}`和`{Param 2}`變數可讓您在廣告變化中動態插入數值，而不刪除和重新建立廣告，因此不會影響品質分數。

若要針對價格資料使用`{Param 1}`或`{Param 2}`變數，請將資料檔中的價格欄對應至適當摘要範本中的該變數，然後將變數納入您的廣告變數範本中。

例如，如果該欄名為「Price」，則開啟建立廣告的摘要範本，按一下&#x200B;**[!UICONTROL Param 1]**&#x200B;旁的輸入欄位，然後按一下&#x200B;**[!UICONTROL Price]**&#x200B;清單中的[!UICONTROL Feeds/Available Columns]欄，該欄會插入`[Price]`作為[!UICONTROL Param 1]的值。 然後，在摘要範本底部的廣告變化範本中，插入`{param1:default text}`，其中「預設文字」為文字，在摘要檔案中的引數欄為廣告列空白時使用。

當您提交資料時，[!UICONTROL Param1]和[!UICONTROL Param2]欄的資料欄位最多可包含25個字元，包括數值資料、貨幣符號和貨幣代碼，以及下列非數值字元： `, . % + - /`
+++

+++從存貨摘要產生的行銷活動有許多孤立交易。

如果[摘要資料設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)設定為刪除各種情況下的廣告，則點選廣告後發生的任何延遲轉換都可能導致[孤立交易](/help/search-social-commerce/glossary.md#o-p)。 最佳實務是暫停廣告而非刪除廣告。 如果廣告在很長一段時間後仍未收到任何收入，您可以透過大量表單或廣告管理檢視將其刪除。
+++

## 帳戶和促銷活動相關的效能問題

+++我的一些行銷活動所花費的金額或多或少於行銷活動預算。

* 在設定了&quot;[!UICONTROL Auto adjust campaign budget limits]&quot;選項的最佳化產品組合中，這是正常的。 啟用此選項後，每個行銷活動的預算最多可花費&#x200B;*N*&#x200B;次，其中&#x200B;*N*&#x200B;為&quot;[!UICONTROL Multiple]&quot;設定的值。 此選項可讓最佳化功能視需要調整個別行銷活動的支出，同時引導整個產品組合達成其目標。
* 如果[!DNL Google Ads]個行銷活動使用共用預算，則[!DNL Google Ads]會視需要調整個別行銷活動的支出，以花費整個共用預算。
+++
