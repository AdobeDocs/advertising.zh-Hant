---
title: 詳細目錄摘要的文字廣告和回應式搜尋廣告範本設定
description: 參考詳細目錄摘要的文字廣告和回應式搜尋廣告範本設定。
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# 詳細目錄摘要的文字廣告和回應式搜尋廣告範本設定


*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

>[!NOTE]
>
>* 在範本中保留下列字元以指定欄名稱和修飾元名稱，因此禁止在所有屬性欄位中做為文字： `[ ] < > `
>* 在[!DNL Yandex templates]中，您只能在URL中使用動態引數`{param1}`和`{param2}`，而且您不能在廣告說明中使用動態價格插入。

## \[在所有索引標籤上方\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[左側面板\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]：** （選用）將所有新廣告群組（不適用於[!DNL Yandex]）、關鍵字和廣告對應至現有行銷活動，而非建立行銷活動。 如果啟用此選項，請選取對應方法。

在行銷活動層級使用[!UICONTROL Map Only]需要與產品分類法緊密相連並輕鬆對應到資料摘要的現有帳戶結構。

**[!UICONTROL Map Method]：** （為行銷活動啟用[!UICONTROL Map Only]時）新廣告群組（不適用於[!DNL Yandex]）、關鍵字和廣告對應到現有行銷活動的方法：

* *[!UICONTROL Contains Anywhere]：*&#x200B;將資料新增至名稱包含指定字串的現有行銷活動（如果存在）。

* *[!UICONTROL Contains Exactly]：*&#x200B;將資料新增至名稱包含指定字串的現有行銷活動（如果存在）。

* *[!UICONTROL Exactly Matches]* （預設值）：將資料新增至具有相同名稱的現有行銷活動（如果存在）。

找不到相符專案時，會忽略行銷活動的所有資料。 如果找到多個相符的行銷活動，則關鍵字和廣告會對映至所有關鍵字。

**[!UICONTROL Campaign Tracking Template]：** （僅具有最終/進階URL的帳戶；選用）行銷活動層級追蹤範本，其會指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。 此值會覆寫帳戶層級設定，但更精細層級的追蹤範本（以關鍵字為最精細）會覆寫此值。

* 針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動附加重新導向和追蹤代碼。

* 若要內嵌最終URL：

   * （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）如需表示追蹤範本中最終URL的引數清單，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348)中「可用的[!DNL ValueTrack]引數」一節中的（[!DNL Microsoft Advertising]僅限） [[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799/2)或（[!DNL Google Ads]僅限）「追蹤範本」引數。

   * （僅限[!DNL Yahoo! Japan Ads]）使用引數`!{unescapedurl}`來指示登陸頁面URL。

   * 您可以選擇加入URL引數以及針對促銷活動定義的任何自訂引數，以&amp;分隔，例如`{lpurl}?matchtype={matchtype}&device={device}`。

* 對於協力廠商重新導向和追蹤，請輸入值。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]：** （在[!DNL Google Ads]和[!DNL Yandex]行銷活動設定中）要放置廣告的網路：

* *[!UICONTROL Search]：*&#x200B;要投標贊助者搜尋清單。

  （[!DNL Google Ads]個行銷活動）若要在[!DNL Google Ads]個搜尋合作夥伴的清單中包含競標，請選取&#x200B;**[!UICONTROL Search partners]**&#x200B;旁的核取方塊。

* *[!UICONTROL Content]：*&#x200B;若要對內容（顯示）網路清單中的位置出價。 **注意：**&#x200B;您無法使用範本建立版位。 當您選取此選項時，請使用<!-- insert link -->大量表單或<!-- insert links -->廣告群組，並在[!UICONTROL Search] > [!UICONTROL Campaigns]檢視中設定版位，為每個廣告群組建立版位，並指定顯示網路上要鎖定哪些頁面。

**[!UICONTROL Languages]：** （僅限[!DNL Google Ads]搜尋和顯示網路）行銷活動中廣告的一或多個目標語言。

[!DNL Google Ads]會根據使用者的[!DNL Google]語言設定或搜尋查詢、目前頁面或最近在[!DNL Google Display Network]檢視的頁面的語言，來決定使用者的語言。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]：** （僅具有最終/進階URL的帳戶）廣告群組層級追蹤範本，此範本會指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。

針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動附加重新導向和追蹤代碼。

對於協力廠商重新導向和追蹤，請輸入值。 若要指出登入頁面URL：

* 適用於Yahoo！ Japan Ads帳戶，使用引數{lpurl}。

* 如需Microsoft Advertising和Google Ads帳戶可用的引數，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348)中「可用的[!DNL ValueTrack]引數」一節中的[[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799)或「僅追蹤範本」引數。

此值會覆寫帳戶和促銷活動層級的設定，但更精細層級的追蹤範本（以關鍵字為最精細）會覆寫此值。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]：**&#x200B;指定廣告群組（或[!DNL Yandex]帳戶的行銷活動）的關鍵字，可由靜態文字、指定檔案中的欄和修飾元的任意組合所組成。 當指定的摘要檔案透過範本傳播時，欄名稱和修飾詞會被實際資料取代。

若要將欄名稱或修飾元群組插入為動態引數，請在輸入欄位中按一下，然後按一下欄清單中的欄名稱或修飾元清單中的[修飾元名稱](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)。 若要為相同關鍵字指定多個關鍵字或多個相符型別，請在不同的行中輸入它們。 若要指定關鍵字比對型別，請在欄名稱前後使用下列比對型別語法：

* 針對[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]範本：

   * 對於動態引數： Broad Match = `[keyword]`，[!UICONTROL Keyword]欄中第一個字詞的Broad Match Modifier （例如+blue suede shoes） = `+[keyword]`，Keyword欄中每個字詞的Broad Match Modifier （例如+blue +suede +shoes） = `+[keyword]+`，Phrase Match = `"[keyword]"`，Exact Match = `[[keyword]]`

   * 針對靜態關鍵字：廣泛比對= `keyword`、廣泛比對修飾詞= `+keyword`，或片語比對= `"keyword"`

     您無法在此輸入具有完全相符和標準相符語法的靜態關鍵字，因為它們被括弧(`[]`)括住，就像動態引數一樣。

* 針對[!DNL Yandex]範本：

   * 針對動態引數：插入資料行名稱，例如`[keyword]`。 若要指出相符型別，請使用[[!DNL Yandex]特定語法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 **注意：**&#x200B;對於廣泛比對辭彙，請使用下列語法： Broad Match Modifier for the first term in the Keyword column （例如+blue suede shoes） = `+[keyword]`， Broad Match Modifier for each term in the Keyword column （例如+blue +suede +shoes） = `+[keyword]+`

   * 對於靜態關鍵字：僅支援搜尋關鍵字。 使用關鍵字的[[!DNL Yandex]特定語法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 不支援括弧(`[]`)表示字元順序。

>[!NOTE]
>
>* 您可以在關鍵字引數之前或之後（但不能同時在這兩處）將逗號分隔值括在括弧中，以手動方式在「關鍵字」欄位中加入多個修飾元值。 例如，`(cheap, discount, affordable)[product]`會為每個產品產生三個個別的廣告。
>* 如果您未指定相符型別，則會使用預設相符型別「廣泛」。
>* 不支援負值相符專案。
>* Google廣泛比對修飾詞現在與某些語言的片語比對有相同的比對行為，而且您無法建立新的廣泛比對修飾詞關鍵字。 如需詳細資訊，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/10286719)。

**[!UICONTROL Map Only]：**&#x200B;將任何新廣告新增至找到指定關鍵字的廣告群組（或[!DNL Yandex]帳戶的行銷活動），而非建立新的關鍵字。 若要啟用此選項，請選取核取方塊。 啟用此選項後，指定關鍵字中的任何Param 1和Param 2變數都不會套用，因為關鍵字存在。

**[!UICONTROL Keyword Final URL]：** （具有最終/進階URL的帳戶；選擇性）廣告網路使用者按一下您的廣告時所進入的登陸頁面URL。 其必須包含與顯示URL相同的網域，而且最終URL中的任何引數都必須符合廣告點選後登陸頁面URL中的引數。 登陸頁面網域或子網域內可包含重新導向，但登陸頁面網域外不可包含重新導向。

如果您使用[!DNL Google Merchant Center]摘要並在&quot;[!DNL Link]&quot;欄中包含此值，則請在此欄位中插入該欄。

>[!NOTE]
>
>* 如果您在張貼透過範本傳播的資料時產生追蹤URL，則追蹤引數會根據帳戶追蹤設定附加至此值。
>* （[!DNL Google Ads]帳戶）避免使用巨集，巨集不會取代來自啟用平行追蹤之來源的點選。 如果廣告商必須使用巨集，則Adobe帳戶團隊應與客戶支援或實作團隊合作以新增它們。

**[!UICONTROL Keyword Tracking Template]：** （具有最終/進階URL的帳戶；選用）追蹤範本，其會指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。 最精細層級的追蹤範本（以關鍵字為最精細）會覆寫所有其他層級的值。

* 針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動附加重新導向和追蹤代碼。

* 您可以選擇輸入協力廠商重新導向與追蹤。

* 若要指出登入頁面URL：

   * （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）如需表示追蹤範本中最終URL的引數清單，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348)中「可用的[!DNL ValueTrack]引數」一節中的（[!DNL Microsoft Advertising]僅限） [[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799)或（[!DNL Google Ads]僅限）「追蹤範本」引數。

   * （僅限[!DNL Yahoo! Japan Ads]）使用引數`!{lpurl}`來指示登陸頁面URL。

**[!UICONTROL Param 1]**， **[!UICONTROL Param 2]\[[!DNL Google Ads]範本\]：** （僅限[!DNL Google Ads]範本）指定檔案中代表[!DNL Google Ads] `{param1}`或`{param2}`變數的資料行，您可以將其包含在範本中建立之任何廣告的廣告復本或顯示URL中。 若要插入動態引數，請在輸入欄位中按一下，然後按一下欄清單中的欄名稱。 當摘要檔案透過範本傳播時，欄名稱會以實際資料取代。

如果使用任一引數，您可選擇僅將引數套用至新關鍵字，或同時更新不是從範本建立的現有關鍵字的值：

* **[!UICONTROL Do Not Apply to Existing Keywords]** （預設值）：僅針對使用範本建立的新關鍵字插入引數值。

* **[!UICONTROL Apply to Existing Keywords: Constant]：**&#x200B;除了從摘要建立新關鍵字之外，Search、Social和Commerce也會更新非使用範本建立之廣告群組中所有現有關鍵字的引數值。 輸入用於所有這些關鍵字的單一數值。 範本必須至少包含一個關鍵字。

* **[!UICONTROL Apply to Existing Keywords: Min]：**&#x200B;除了從摘要建立新關鍵字之外，只要摘要檔案包含引數的數值，而且最多有一個小數點但不含逗號、貨幣符號或程式碼，或任何其他字元，Search、Social和Commerce也會更新廣告群組中，未使用範本建立的所有現有關鍵字的引數值。 摘要檔案中的引數最小值會用於所有現有關鍵字。 例如，如果摘要檔案有[!UICONTROL Param1]個21500和22000值，則現有關鍵字的[!UICONTROL Param1]值會變更為21500。 範本必須至少包含一個關鍵字。 **秘訣：**&#x200B;只有當您已緊密設定廣告群組主題，讓關鍵字擁有相同值是合理的時，才使用此選項。

摘要檔案中的資料欄位最多可包含25個字元，而且只能包含具有下列非數字字元的數值資料：

* （使用&quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;引數時）最多只能有一小數點。

* （當您未使用&quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;引數時）：

   * 值前面或後面可附加貨幣符號或代碼。 例如，2.000,00英鎊和2000GBP有效。

   * 該值可以包括逗號(，)或句點(.) 做為分隔符號，並加上選用的句號(.) 或逗號(，)表示分數值。 例如，1,000.00和2.000,10有效。

   * 值可以在前面加上百分比符號(%)、加號(+)或減號(-)。 例如，20%、208+和–42.32有效。

   * 兩個數字可以用正斜線內嵌。 例如，4/1和0.95/0.45有效。

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising]範本\]：** （僅限[!DNL Microsoft Advertising]個範本）標題、文字、顯示URL或最終URL包含`{Param2}`個動態替代字串時，要作為廣告替代值的字串。 長度上限為70個字元，但請注意，您使用廣告元素的最大長度（例如，廣告標題最多可包含25個字元）。

**[!UICONTROL Param 3]：** （僅限[!DNL Microsoft Advertising]個範本）標題、文字、顯示URL或最終URL包含`{Param3}`動態替代字串時，要做為廣告替代值的字串。 長度上限為70個字元，但請注意，您使用廣告元素的最大長度（例如，廣告標題最多可包含25個字元）。

**[!UICONTROL Initial Bid (&lt;Match Type or Ad Type>)]：**&#x200B;具有指定符合型別或廣告型別的每個關鍵字的初始競標。

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]：** （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]行銷活動）廣告型別： *[!UICONTROL Expanded Search Ads]*&#x200B;或&#x200B;*[!UICONTROL Responsive Search Ads]*。

**[!UICONTROL Prefill]：** （選擇性）以原始廣告復本欄位的文字，預先填入所有替代廣告復本欄位。

### [!UICONTROL Headlines]

**[!UICONTROL Pin]：** （僅限回應式搜尋廣告）必須包含標題/標題的廣告位置（例如&quot;[!UICONTROL Pinned at position 1]&quot;）。 預設值為[!UICONTROL Unpinned]。

每個位置必須至少有一個標題可用。 如果您將多個標題釘選至相同位置，則最終廣告會一律在指定位置包含這些標題之一。 釘選到位置3的標題可能無法與廣告一起顯示。

**[!UICONTROL Headline 1]**、**[!UICONTROL Headline 2]**、**[!UICONTROL Headline 3]：** （僅限回應式搜尋廣告）廣告標題（標題）。 每個廣告變數必須至少包含三個廣告標題，以及最多15個廣告標題。 廣告網路會顯示最多有三個標題的廣告。 每個標題的長度上限為30個字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]：** (現有Microsoft Advertising標準文字廣告僅限；唯讀)廣告的標題或第一行。 Microsoft Advertising已棄用標準文字廣告的建立和編輯。

**[!UICONTROL Headline 1]**，**[!UICONTROL Headline 2]：** （僅限[!DNL Google Ads]和[!DNL Yahoo! Japan Ads]擴充/延伸文字廣告範本）廣告的標題。 每行的長度上限（在任何動態引數取代後）為30個字元或15個雙位元組字元。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]：** （[!DNL Google Ads]僅展開文字廣告範本；選擇性）廣告的第三個標題。 最大長度（在任何動態引數取代後）為30個字元或15個雙位元組字元。

**[!UICONTROL Title]：** （僅限[!DNL Yandex]）廣告的標題或第一行。 最大為33個字元。

**[!UICONTROL Title Part 1]**， **[!UICONTROL Title Part 2]：** (Microsoft Advertising僅展開文字廣告)廣告的標題。 每行的長度上限（在任何動態引數取代後）為30個字元或15個雙位元組字元。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]：** (Microsoft Advertising僅展開文字廣告)廣告內文。 長度上限（在任何動態引數取代後）為80個字元或40個雙位元組字元（例如中文、日文和韓文）。

### [!UICONTROL Descriptions]

**[!UICONTROL Description]：**&#x200B;廣告內文。

* (Google Ads擴充文字廣告範本)長度上限（取代任何動態引數後）為90個字元或45個雙位元組字元。

* (Yahoo！ 日本廣告範本)長度上限（替換任何動態引數後）為80個字元或40個雙位元組字元。

* （Yandex範本）長度上限（替換任何動態引數後）為75個字元，且單一字元不得超過22個字元。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]：** （僅限回應式搜尋廣告）必須包含說明的廣告位置（例如&quot;[!UICONTROL Pinned at position 1]&quot;）。 預設值為[!UICONTROL Unpinned]。 每個位置必須至少有一個說明。

如果您將多個說明釘選至相同位置，則最終廣告會一律在指定位置包含這些說明之一。 釘選到位置2的說明可能無法與廣告一起顯示。

**[!UICONTROL Description 1]**，**[!UICONTROL Description 2]：** （僅限回應式搜尋廣告）廣告說明。 每個廣告變數必須至少包含兩個和最多四個廣告說明。 廣告網路會顯示最多有兩個說明的廣告；至少輸入兩個。 每個說明的長度上限為90個字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]：** (Google僅展開文字廣告範本；選擇性)廣告的第二行。 長度上限（在任何動態引數取代後）為90個字元或45個雙位元組字元。

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**， **[!UICONTROL Display Path 2]：** （僅限展開文字和回應式搜尋廣告；選擇性）要在基底URL後面連續包含的一或兩個URL路徑。 他們應在廣告中更詳細地說明產品或服務。 例如，如果您將[!UICONTROL Display Path 1]的「鞋子」與[!UICONTROL Display Path 2]的「戶外」新增至基底URL www.example.com，則URL為www.example.com/Shoes/Outdoor。 每個欄位的長度上限（在任何動態引數取代後）為15個字元或7個雙位元組字元。

針對回應式搜尋廣告，請使用下列格式插入廣告自訂程式，其中`Default text`為當摘要檔案未包含有效值時要插入的選用值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}`，例如`{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}`，例如`{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]：** （僅現有[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]標準文字廣告；唯讀）廣告中顯示的URL。

[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]已棄用標準文字廣告的建立和編輯。

**[!UICONTROL Base URL]：** （僅具有目的地URL的帳戶）使用者被帶往的頁面。 其中可能包含協力廠商重新導向和追蹤程式碼。 如果您使用Adobe Advertising轉換追蹤服務，且行銷活動設定包含使用[!UICONTROL EF Redirect]和在廣告層級新增追蹤，則Search、Social和Commerce會自動將其自己的重新導向和追蹤程式碼新增至廣告。

若要將欄名稱或修飾元群組插入為動態引數，請在輸入欄位中按一下，然後按一下欄清單中的欄名稱或在[!UICONTROL Modifiers]清單中的[修飾元名稱](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)。

**[!UICONTROL Final URL]：** （具有最終/進階URL的帳戶）使用者按一下您的廣告時所前往的登陸頁面URL。 其必須包含與顯示URL相同的網域，而且最終URL中的任何引數都必須符合廣告點選後登陸頁面URL中的引數。 登陸頁面網域或子網域內可包含重新導向，但登陸頁面網域外不可包含重新導向。

如果您使用[!DNL Google Merchant]中央摘要並將此值包含在「[!UICONTROL Link]」欄中，則請將該欄插入此欄位。

>[!NOTE]
>
>* 如果您在張貼透過範本傳播的資料時產生追蹤URL，則追蹤引數會根據帳戶追蹤設定附加至此值。
>* （[!DNL Google Ads]帳戶）避免使用巨集，巨集不會取代啟用平行追蹤之來源的點按。 如果廣告商必須使用巨集，Adobe帳戶團隊應與客戶支援或實作團隊合作以新增巨集。

**[!UICONTROL Tracking Template]：** （具有最終/進階URL的帳戶；選用）追蹤範本，其會指定所有離登陸網域重新導向和追蹤引數，並將最終URL內嵌在引數中。 最精細層級的追蹤範本（以關鍵字為最精細）會覆寫所有其他層級的值。

針對Adobe Advertising轉換追蹤（在行銷活動設定包含&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;時套用），搜尋、社交和Commerce會在您儲存記錄時自動附加重新導向和追蹤代碼。

對於協力廠商重新導向和追蹤，請輸入值。 若要指出登入頁面URL：

* 適用於Yahoo！ Japan Ads帳戶，使用引數{lpurl}。

* 如需Microsoft Advertising和Google Ads帳戶可用的引數，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/6305348)中「可用的[!DNL ValueTrack]引數」一節中的[[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/3/en/56799)或「僅追蹤範本」引數。

**\[原始廣告欄位下方的替代廣告欄位\]：** （選擇性）廣告的替代廣告復本集，如果原始廣告復本中的任何一行超過傳播期間填入資料後的動態引數允許長度上限，就可以使用此替代廣告復本。

>[!NOTE]
>
>* 如果選取了[!UICONTROL Prefill]選項，則替代欄位會預先填入原始欄位，您可以視需要編輯它們。
>* 只有超過最大長度的廣告文案欄位會取代為替代值。 例如，如果只有原始標題或標題太長，則產生的廣告變化會使用替代標題或標題以及原始說明。 因此，請確保替代廣告文案與原始廣告文案結合時有意義。
>* 如果原始廣告復本符合搜尋引擎的長度要求，則會捨棄替代廣告復本。

**\[Component\] [!UICONTROL Ad Label Classifications] > \[Label Classification and Value\]：** （選用）最多五個現有標籤分類的值，可指派給使用範本建立或編輯的廣告變化。 針對您想要指派標籤分類的每個促銷活動元件：

1. 按一下核取方塊。

1. 設定廣告變化範本的標籤分類值：

   * 針對要指派給元件的每個標籤分類和值，請執行以下操作：

      1. 按一下&#x200B;**[!UICONTROL Add Label Classification]**。

      1. 選取現有的標籤分類，然後選取現有值或輸入新值。

         每個值的長度上限為100個字元，可包含ASCII和非ASCII字元。

         若要插入欄名稱做為標籤分類值的動態引數，請按一下輸入欄位（第二個欄位），然後按一下欄清單中的欄名稱。

         每個行銷活動元件的每個分類只能包含一個值。 例如，行銷活動可以有Color=Red但不可以有Color=Red和Color=Blue。

         * 若要變更現有的標籤分類值，請選取或輸入新值。

         * 若要移除現有的標籤分類值，請按一下值旁的&#x200B;**[!UICONTROL X]**。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [關於使用詳細目錄摘要自動化廣告管理](../inventory-feeds-about.md)
>* [管理修飾元](../modifiers-manage.md)
>* [管理詳細目錄資料摘要檔案](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [透過範本傳播摘要資料](../feed-data-propagate.md)
>* [從詳細目錄摘要張貼行銷活動資料至廣告網路](../propagated-data-post.md)
