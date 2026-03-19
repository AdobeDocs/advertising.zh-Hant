---
title: 使用Adobe Advertising ID建立 [!DNL Marketing Channels] 規則
description: 瞭解如何使用Adobe Advertising ID來建立 [!DNL Analytics Marketing Channels]的處理規則。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# 使用Adobe Advertising ID建立[!DNL Marketing Channels]處理規則

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

您可以使用Adobe Advertising ID （[AMO ID和EF ID](../ids.md)）在Adobe Analytics中設定[!DNL Marketing Channels]處理規則。 將Adobe Advertising ID用於您Adobe Advertising行銷活動的特定規則。 您處理規則的順序會決定所有可能的資料是否都已正確擷取。

## 處理規則中的AMO ID

AMO ID是主要追蹤程式碼，用於報告[!DNL Analytics]內的Adobe Advertising資料。 AMO ID是由Adobe管理的動態值串連，以在[!DNL Analytics]內提供精細報表。 它儲存在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=zh-Hant)或rVar維度(AMO ID)中。 AMO ID可在[!DNL Analytics]中設定有兩種方式：

* 點進追蹤： Adobe Advertising會在連結中設定`s_kwcid`查詢字串引數，而當點進發生時，[!DNL Analytics]會從登陸頁面URL中挑選引數。

* 檢視追蹤（僅限[!DNL DSP]）： [!DNL Last Event Service]會在伺服器端偵測檢視，並將AMO ID傳送至[!DNL Analytics]。 在此情況下，URL不包含`s_kwcid`引數。

AMO ID中的動態值表示所追蹤的行銷管道：

* AMO ID中的前置字元可用來識別[!DNL Marketing Channels]中的最上層通道。

* AMO ID內文中的字元短語表示更具體的行銷活動型別。

* 尾碼「vt」適用於[!DNL DSP]閱覽流量，可用來建立個別的點進和閱覽[!DNL DSP]管道。

可忽略其餘的AMO ID。

| [!UICONTROL AMO ID] | 頻道 | 規則邏輯 |
|--------|---------|--------------------|
| ！ctv （尾碼） | [!UICONTROL DSP Connected TV ViewThrough] | 結尾為 |
| ！d！ （內文） | [!UICONTROL Display Network] | 包含 |
| ！g！ （內文） | [!UICONTROL Google Search] | 包含 |
| ！s！ （內文） | [!UICONTROL Search Partner] | 包含 |
| ！u！ （內文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| ！ytv！ （內文） | [!UICONTROL YouTube Video Ad] | 包含 |
| ！yts！ （內文） | [!UICONTROL YouTube Search Ad] | 包含 |
| ！vp！ （內文） | [!UICONTROL Google Video Partners] | 包含 |
| ！vt （尾碼） | [!UICONTROL DSP ViewThrough] | 結尾為 |
| 阿爾！ （前置詞） | [!UICONTROL Paid Search] | 開頭為 |
| AC！ （前置詞） | [!UICONTROL DSP Display] | 開頭為 |

## 處理規則中的EF ID

AMO EF ID (EF ID)是[!DNL Analytics for Advertising]整合中使用的第二個追蹤程式碼。 其主要用途是追蹤並傳遞[!DNL Analytics]事件資料至Adobe Advertising。 每次點進或檢視發生時，系統都會產生唯一的EF ID，即使同一位訪客擁有完全相同的廣告亦然。 [!DNL Analytics]報表使用者介面中未使用EF ID，因為它通常會超過[!DNL Analytics]中每個變數限制500,000個不重複值，使其無法用於報表。 Adobe Advertising量度和中繼資料不會套用至EF ID，而只會套用至AMO ID。 Adobe Advertising中的行銷活動最佳化需要新增的追蹤粒度，因此兩個ID都是必要的。

雖然EF ID維度並未直接在[!DNL Analytics]報表中使用，但EF ID仍適合用於建立行銷管道。 EF ID尾碼會指出頻道（顯示或搜尋），以及造訪是由點進還是檢視所驅動。 EF ID中的分隔符號是冒號，而非AMO ID中的驚歎號。

| EF ID尾碼 | 頻道 |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Adobe Advertising的處理規則範例

下列範例規則集著重於廣告管道（付費搜尋、顯示ClickThrough和顯示ViewThrough）的規則。 此外也示範付費搜尋偵測的建議規則（包括該規則與免費搜尋行銷管道邏輯的互動方式）以及免費反向連結網域規則的選擇性更新。

**注意：**&#x200B;顯示區可以分成兩個管道，或根據廣告商偏好設定合併成單一管道。

範例熒幕擷圖中包含其他管道，以說明廣告管道相較於其他管道在典型實施中的建議操作順序。

>[!IMPORTANT]
>
>請參閱「[規則 [!DNL Marketing Channels] 的](#rule-order)作業順序」，以取得有關處理規則順序的資訊。

![一組處理規則的範例](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### 付費搜尋規則

最佳作法是針對[!UICONTROL Paid Search]規則納入兩個附有「Any」運運算元的條件：

* 成本/點按/曝光資料包含AMO ID，因此請包含AMO ID。 AMO ID應該以「AL！」開頭。 以正確配置點選/成本/曝光資料給[!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* [!UICONTROL Paid Search]點進次數的URL一律包含`s_kwcid`查詢字串引數，因此請包含該引數，以確保在訪客導覽回登陸頁面時，能正確進行重複資料刪除。 包括「AL！」 在`s_kwcid`之前，以正確配置點選/成本/曝光資料給[!UICONTROL Paid Search]。

請勿將管道值設為AMO ID。 請改為將名稱設為反向連結網域、搜尋引擎+關鍵字或頁面等。 （這與所有[!DNL Marketing Channels]相關）。

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![付費搜尋規則範例](/help/integrations/assets/a4adc-mc-rule-paid-search.png "付費搜尋規則範例")

### 免費搜尋規則

對於[!UICONTROL Natural Search]，請確定您的[[!UICONTROL Paid Search]偵測規則](https://experienceleague.adobe.com/zh-hant/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection)包含`ef_id`和`s_kwcid`查詢字串引數。 （通常，當Advertising Search、Social和Commerce整合到[!DNL Analytics]中時會自動設定此專案，但如果[!DNL Analytics]管理員在設定整合後變更邏輯，請驗證。）

將規則設為「符合免費搜尋偵測規則」（通常是此管道的預設設定）。

![免費搜尋規則範例](/help/integrations/assets/a4adc-mc-rule-natural-search.png "免費搜尋規則範例")

### 顯示點進規則#1

僅擷取點進次數，以建立「顯示」點進行銷管道。 因為點進和檢視的AMO ID相同，所以此規則會使用EF ID變數和`ef_id`查詢字串引數。

有時會透過URL （預設值）追蹤點進。 在其他情況下，點進是透過伺服器端的「上次事件服務」追蹤，因此URL不包含`ef_id`引數。 因此，規則會檢查EF ID變數或`ef_id`查詢字串引數結尾為&quot;:d&quot;的條件。 使用&quot;`Any`&quot;運運算元，因為您想要為任一條件觸發此規則。

![第一個顯示點進規則的範例](/help/integrations/assets/a4adc-mc-rule-display-ct.png "第一個顯示點進規則的範例")

### 自然反向連結網域規則

（選用）最佳實務是將「是瀏覽的第一個頁面」條件與「任何」運運算元新增至標準[!UICONTROL Natural Referring Domains]規則。 雖然此規則為選用，但若使用者按一下「上一步」按鈕返回登陸頁面，有助於防止自然反向連結處於邊緣案例設定。

![自然反向連結網域規則範例](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "自然反向連結網域規則範例")

### 顯示CTV瀏覽規則

若要追蹤[!DNL DSP]連線電視(CTV)觀看次數，請建立AMO ID結尾為`"!ctv"`的規則。 由於訪客未按一下廣告，瀏覽追蹤不會在URL中包含`ef_id`或`s_kwcid`，而規則只需要一個條件。

![顯示CTV ViewThrough規則範例](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png "顯示CTV ViewThrough規則範例")

### 顯示瀏覽規則

若要建立「顯示ViewThrough」管道，請建立EF ID結尾為&quot;:i&quot;的規則。 由於訪客未按一下廣告，瀏覽追蹤不會在URL中包含`ef_id`或`s_kwcid`，而規則只需要一個條件。

![顯示ViewThrough規則範例](/help/integrations/assets/a4adc-mc-rule-display-vt.png "顯示ViewThrough規則範例")

### 顯示點進規則#2

針對第二個顯示點進規則，設定&#x200B;**AMO ID開頭為&quot;AC！&quot;**。 此第二個規則是用來擷取直接從Adobe Advertising進入[!DNL Analytics]之顯示頻道的點選/成本/曝光資料。 此資料歸因於AMO ID，但不包含具有`ef_id`查詢字串的URL，因此這些點選不會與AMO EF ID （這是第一個「顯示ClickThrough」規則擷取的內容）連結。

![第二個顯示點進規則範例](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "第二個顯示點進規則範例")

## [!DNL Marketing Channels]規則的作業順序 {#rule-order}

![適用於Adobe Advertising相關規則的理想作業順序](/help/integrations/assets/a4adc-mc-rule-order.png "適用於Adobe Advertising相關規則的理想作業順序")

* 將[!UICONTROL Paid Search] *放在* [!UICONTROL Natural Search]之前。 否則，付費搜尋資料可能會分配給免費搜尋。

* 將&#x200B;**第一個** [!UICONTROL Display ClickThrough] *放在* [!UICONTROL Natural Referring Domains]和[!UICONTROL Natural Social]之前。

* 當您使用[!UICONTROL CTV view-throughs]時，請將它放在&#x200B;**&#x200B;之前[!UICONTROL Display ViewThroughs]。 否則，CTV檢視將會擷取為Display ViewThroughs。

* 將[!UICONTROL Display ViewThroughs]個&#x200B;*放在*&#x200B;個其他管道之後，但放在[!UICONTROL Internal]和[!UICONTROL Direct]之前，因為在相同的登陸事件中可能會發生檢視和非[!DNL Advertising]點進。 例如，訪客可能會看到Adobe Advertising廣告、獲得印象，然後透過[!UICONTROL Natural Search]前往網站。

  最佳實務是將其他管道（[!UICONTROL Internal]和[!UICONTROL Direct]除外）優先於閱覽。

* 有些廣告商可能會選擇將[!UICONTROL Display ViewThroughs]優先順序設為[!UICONTROL Natural Referring Domains]。 切換兩個規則的處理順序即可執行此操作。

* **秒** [!UICONTROL Display ClickThrough]規則可用來擷取直接從Adobe Advertising傳入[!DNL Analytics]的點選/成本/曝光資料。 由於此資料只會歸因於AMO ID，因此這些點選不會與AMO EF ID連結。 如果您未設定此規則，則所有點按/成本/曝光資料都在[!UICONTROL Direct]管道下，這是任何不符合[!DNL Marketing Channel]之資料的預設管道。 此規則必須在檢視規則&#x200B;*之後*，否則它會選取任何檢視。

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [基礎（共 [!DNL Analytics Marketing Channels]](mc-overview.md)個）
>* [為什麼管道資料在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之間會有所不同
>* [搭配Adobe Advertising資料使用 [!DNL Analytics Marketing Channels] &#x200B;](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 進行Adobe Advertising報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hant)
>* [由 [!DNL Analytics]](/help/integrations/analytics/ids.md)使用的Adobe Advertising ID