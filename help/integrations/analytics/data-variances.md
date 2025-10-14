---
title: ' [!DNL Analytics] 和Adobe Advertising之間的預期資料差異'
description: ' [!DNL Analytics] 和Adobe Advertising之間的預期資料差異'
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# [!DNL Analytics]和Adobe Advertising之間的預期資料差異

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

具有[!DNL Analytics for Advertising] <!-- (A4AdC) -->整合的廣告商會透過Adobe Advertising和Adobe Analytics追蹤付費廣告。 透過多個系統追蹤媒體、行銷活動和管道時，來自不同系統的相同資料集很少完全相符。 本檔案說明您應如何預期透過Adobe Advertising販運的媒體資料，與[!DNL Analytics]內追蹤媒體之不同系統中的資料進行比較。

>[!NOTE]
>
>本檔案著重於Adobe Advertising和分析，但許多要點也可以轉移到其他追蹤解決方案。

## 類似報表中的歸因差異

### 回顧期間和歸因模型可能不同

[!DNL Analytics for Advertising]整合使用兩個變數（[!DNL eVars]或[!DNL rVars] \[保留的[!DNL eVars]]\）來擷取[EF ID和AMO ID](ids.md)。 這些變數是透過單一回顧視窗（即點進和檢視歸因的時間）和歸因模型來設定。 除非另有指定，否則變數會設定為符合預設、廣告商層級的點按回顧視窗和Adobe Advertising中的歸因模型。

不過，回顧視窗和歸因模型可在Analytics （透過[!DNL eVars]）和Adobe Advertising中設定。 此外，在Adobe Advertising中，歸因模型不僅可在廣告商層級（用於競標最佳化）設定，也可在個別資料檢視和報告內設定（僅用於報告目的）。 例如，組織可能偏好使用均勻分佈歸因模型來最佳化，但對Advertising DSP或[!DNL Advertising Search, Social, & Commerce]中的報表使用上次接觸歸因。 變更歸因模型會變更已歸因的轉換次數。

如果在一個產品中修改了報表回顧期間或歸因模型，而在另一個產品中修改了報表回顧期間或歸因模型，則來自每個系統的相同報表會顯示不同的資料：

* **不同回顧期間所導致的差異範例：**

  假設Adobe Advertising有60天的點選回顧期間，而[!DNL Analytics]有30天的回顧期間。 並假設使用者透過Adobe Advertising追蹤廣告進入網站，離開，然後在第45天返回並轉換。 Adobe Advertising會將轉換歸因於初始造訪，因為轉換發生在60天回顧期間內。 但是，[!DNL Analytics]無法將轉換歸因於初始造訪，因為轉換發生在30天的回顧期間過期之後。 在此範例中，Adobe Advertising報告的轉換次數高於[!DNL Analytics]。

  ![歸因於Adobe Advertising但不歸因於[!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)的轉換範例

* **不同歸因模型造成的差異範例：**

  假設使用者在轉換之前與三個不同的Adobe Advertising廣告互動，且將收入作為轉換型別。 如果Adobe Advertising報表使用平均分配模型來歸因，則會將收入平均歸因於所有廣告。 但是，如果[!DNL Analytics]使用上次接觸歸因模型，則會將收入歸因於最後一個廣告。 在以下範例中，Adobe Advertising會將擷取至這三個廣告的30美元收入中的平均10美元歸因於每個廣告，而[!DNL Analytics]會將所有30美元的收入歸因於使用者看到的最後一個廣告。 當您比較來自Adobe Advertising和[!DNL Analytics]的報告時，可以預期結果會因為歸因不同而有所差異。

  根據不同的歸因模型，![歸因於Adobe Advertising和[!DNL Analytics]的不同收入](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳實務是在Adobe Advertising和[!DNL Analytics]中使用相同的回顧期間和歸因模型。 請視需要與您的Adobe帳戶團隊合作，以識別目前設定並維持設定同步。

這些相同的概念適用於使用不同回顧期間或歸因模型的任何其他類似管道。

#### 檢視追蹤的不同回顧期間 {#impression-lookback}

在Adobe Advertising中，歸因是以點按數和曝光數為基礎，您可以為點按數和曝光數設定不同的回顧期間。 但在[!DNL Analytics]中，歸因是以點進和檢視為基礎，且您無法選擇為點進和檢視設定不同的歸因期間；追蹤從初次網站造訪開始的每個專案。 曝光可能會在檢視發生的同一天或多個天前發生，而時間可能會影響每個系統中歸因視窗的開始位置。

一般而言，大部分的檢視轉換發生得足夠快，以至於兩個系統都可計入評分。 不過，某些轉換可能會發生在Adobe Advertising曝光回顧期間之外，但發生在[!DNL Analytics]回顧期間內；這類轉換歸因於[!DNL Analytics]中的檢視，但不會歸因於Adobe Advertising中的曝光。

在以下範例中，假設訪客在第1天收到廣告，在第2天執行瀏覽式造訪（也就是在沒有先前按一下廣告的情況下造訪廣告的登陸頁面），並在第45天轉換。 在此情況下，Adobe Advertising將會從1天到14天追蹤使用者（使用14天回溯），[!DNL Analytics]將會從2天到61天追蹤使用者（使用60天回溯），而第45天的轉換將會歸因於[!DNL Analytics]內的廣告，但不會歸因於Adobe Advertising內的廣告。

![歸因於[!DNL Analytics]而非Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)的檢視轉換範例

不一致的其他原因在於，在Adobe Advertising中，您可以指派自訂的&#x200B;*瀏覽權數*，此自訂權數與點選型轉換的歸因權數相關。 預設的檢視權重為40%，這表示檢視轉換會計為點按式轉換值的40%。 [!DNL Analytics]未提供此類顯示轉換的加權。 舉例來說，如果您使用預設的檢視權數，在[!DNL Analytics]中擷取的100美元收入訂單會在Adobe Advertising中折扣為40美元，差異為60美元。

比較Adobe Advertising與[!DNL Analytics]報表之間的檢視轉換時，請考量這些差異。

#### 可用的歸因模型

| Adobe Advertising歸因 | [!DNL Analytics]歸因 | [!DNL eVar]/[!DNL rVar]配置 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 不適用 | 不適用 |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>不使用* |
| [!UICONTROL Weight Last Event More] | 不適用 | 不適用 |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 不適用 |
| 不適用 | [!UICONTROL J-Shaped] | 不適用 |
| 不適用 | [!UICONTROL Inverse-J] | 不適用 |
| 不適用 | [!UICONTROL Custom] | 不適用 |
| 不適用 | [!UICONTROL Participation] | 不適用 |
| 不適用 | [!UICONTROL Algorithmic] | 不適用 |

>[!NOTE]
>
>若為線性配置，[!DNL Analytics]會平均分配單一造訪中所有[!DNL eVar]值的成功事件，因此請使用具有「造訪」的[!DNL eVar]到期日的線性配置。 不過，針對廣告，使用線性歸因會導致配置並非真正為線性，且產生的不太理想的報表。 例如，如果訪客在轉換至三個個別造訪之前與三個廣告互動，則只有上次造訪中看到的廣告會歸因於轉換，而非全部三個廣告。
>
>此外，將轉換配置切換至「線性」或是從「線性」切換分配時，不會顯示歷史資料，導致報表中的資料陳述錯誤。 例如，線性配置可能會將收入分配給多個不同的[!DNL eVar]值。 如果您將配置變更為「最近」，則該收入的100%將與最近的單一值相關聯。 此關聯可能會導致錯誤的結論。
>
>為避免混淆，[!DNL Analytics]會在報表介面中隱藏歷史資料。 如果您將[!DNL eVar]變更回初始配置設定，則可以檢視歷史資料，但您不應僅為了存取歷史資料而變更[!DNL eVar]配置設定。 Adobe建議，當您想要為已記錄的資料套用新的配置設定時，請使用新的[!DNL eVar]，而不是變更已具有大量歷史資料的[!DNL eVar]的配置設定。

在[https://experienceleague.adobe.com/zh-hant/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/zh-hant/docs/analytics/analyze/analysis-workspace/attribution/models)檢視[!DNL Analytics]歸因模型及其定義的清單。

如果您已登入[!DNL Search, Social, & Commerce]，您可以找到清單

* （北美使用者） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （所有其他使用者） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe Advertising中的事件日期歸因

在Adobe Advertising中，您可以依關聯的點選日期/事件日期（點選或曝光事件的日期）或交易日期（轉換日期）來報告轉換資料。 [!DNL Analytics]中不存在點選/事件日期報告的概念；在[!DNL Analytics]中追蹤的所有轉換都會依交易日期報告。 因此，可能會以Adobe Advertising和[!DNL Analytics]中的不同日期報告相同的轉換。 例如，假設有一位使用者在1月1日點選廣告並在1月5日轉換。 如果您依Adobe Advertising的事件日期檢視轉換資料，則轉換會在發生點按的1月1日回報。 在[!DNL Analytics]中，相同的轉換在1月5日回報。

![歸因於不同日期的轉換範例](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels]中的歸因

[[!DNL Analytics Marketing Channels] 報告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=zh-Hant)可讓您設定規則，以根據點選資訊的不同方面識別不同的行銷管道。 您可以使用`ef_id`查詢字串引數來識別管道，以將Adobe Advertising追蹤管道（[!UICONTROL Display Click Through]、[!UICONTROL Display View Through]和[!UICONTROL Paid Search]）追蹤為[!DNL Marketing Channels]。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. -->不過，即使[!DNL Marketing Channels]報表可以追蹤Adobe Advertising管道，資料可能因為數個原因而與Adobe Advertising報表不符。 如需詳細資訊，請參閱下列章節。

>[!NOTE]
>
> 下列核心概念也適用任何涉及Adobe Advertising中未追蹤之行銷活動的多頻道追蹤，例如[`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html?lang=zh-Hant)變數（也稱為「追蹤代碼」維度或&quot;[!DNL eVar] 0&quot;）和自訂[!DNL eVar]追蹤。

### [!DNL Marketing Channels]中可能有不同的歸因模型

大部分[!DNL Marketing Channels]報告已設定[!UICONTROL Last Touch]歸因，而最後偵測到的行銷管道已為其指派100%轉換值。 對[!DNL Marketing Channels]報表和Adobe Advertising報表使用不同的歸因模型，會導致歸因轉換中的差異。

### [!DNL Marketing Channels]中可能不同的回顧期間

可以自訂[!DNL Marketing Channels]的回顧期間。 在Adobe Advertising中，點按回顧視窗是可供設定的，但固定的60天視窗很常見。 如果這兩種產品使用不同的回顧期間，可能會出現資料不一致的情況。

### [!DNL Marketing Channels]中的不同頻道歸因

Adobe Advertising報表只會擷取透過Adobe Advertising販運的付費媒體(針對[!DNL Advertising Search, Social, & Commerce]個廣告的付費搜尋，以及針對Advertising DSP廣告的顯示)，而[!DNL Marketing Channels]報表則可以追蹤所有數位頻道。 這可能會導致歸因於轉換的管道不一致。

例如，付費搜尋和免費搜尋管道通常具有共生關係，每個管道互相協助。 [!DNL Marketing Channels]報告將某些轉換歸因於Adobe Advertising沒有的免費搜尋，因為它沒有追蹤免費搜尋。

也可以考慮檢視顯示廣告、點選付費搜尋廣告、點選電子郵件訊息內部，然後下單30美元的客戶。 即使Adobe Advertising和[!DNL Marketing Channels]都使用上次接觸歸因模型，轉換仍會分別以不同方式歸因於各個。 Adobe Advertising沒有[!UICONTROL Email]管道的存取權，所以將計入轉換的付費搜尋。 但是，[!DNL Marketing Channels]可以存取所有三個管道，因此會將[!UICONTROL Email]的轉換歸功。

![Adobe Advertising與[!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)中不同的轉換歸因範例

如需量度可能有所差異的詳細解釋，請參閱&quot;[為何管道資料在Adobe Advertising和 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)之間可能有所差異&quot;。

## Adobe Analytics [!DNL Paid Search Detection]中的資料差異

[!DNL Analytics]中的[舊版 [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html?lang=zh-Hant)功能可讓公司[定義規則，以追蹤指定搜尋引擎的付費和有機搜尋流量](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html?lang=zh-Hant)。 [!DNL Paid Search Detection]規則同時使用查詢字串和反向連結網域來識別付費和免費搜尋流量。 [!DNL Paid Search Detection]報告是較大的[尋找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html?lang=zh-Hant)報告群組的一部分，這些報告會在指定事件（例如購物車結帳）發生或造訪結束時過期。

以下是建立[!DNL Paid Search Detection]規則集的介面：

![&#x200B; [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)中付費搜尋偵測規則集的範例

產生的[!DNL Paid Search Detection]報告包括[!UICONTROL Paid Search Engine]、[!UICONTROL Paid Search Keywords]、[!UICONTROL Natural Search Engine]和[!UICONTROL Natural Search Keywords]報告。

請留意[!DNL Paid Search Detection]報表中資料的下列兩個限制：

* [!UICONTROL Paid Search Keywords]和[!UICONTROL Natural Search Keywords]報表顯示由反向連結URL所識別的搜尋查詢，而非使用者競標的關鍵字。 Adobe Advertising和[!DNL Analytics]報表會顯示實際的關鍵字，因此請勿期望它們與[!DNL Paid Search Detection]關鍵字報表一致。

* 當[!DNL Paid Search Detection]功能最初建立時，原始搜尋查詢（使用者在搜尋引擎的搜尋列中輸入的字元字串）更容易透過轉介URL提供給廣告商。 現今，搜尋引擎大多將搜尋查詢模糊化，且[!DNL Paid Search Detection]關鍵字報告的值有限，因為大部分查詢資料都在「未指定」下。

  透過[!DNL Analytics for Advertising]，廣告商仍可在[!DNL Analytics]中追蹤付費關鍵字。 反向連結網域會通知引擎報告哪個搜尋引擎帶動了流量。 由於廣告商特定帳戶資訊未繫結至反向連結網域，因此所有流量都會列在搜尋引擎下。 在相同搜尋引擎中有多個帳戶的廣告商，應參考Adobe Advertising或[!DNL Analytics]報表，以取得帳戶特定報表。

### 為什麼要設定[!DNL Paid Search Detection]？

[!DNL Paid Search Detection]報告可讓您識別[[!DNL Analytics Marketing Channels] 報告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=zh-Hant)中的免費搜尋流量。 區分付費搜尋流量與免費搜尋流量，是瞭解免費搜尋為完整行銷生態系統帶來價值的重要方法。

## [!DNL Analytics for Advertising]的點進資料驗證 {#data-validation}

針對您的整合，您應該驗證點進資料，以確保網站上的所有頁面都正確追蹤點進。

在[!DNL Analytics]中，驗證[!DNL Analytics for Advertising]追蹤的最簡單方法之一，就是使用「AMO ID例項與點按」計算量度來比較例項與點按，其計算方式如下：

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances]代表在網站上追蹤[AMO ID](ids.md)的次數。 每次點選廣告時，AMO ID (`s_kwcid`)引數都會新增至登陸頁面URL。 因此，[!UICONTROL AMO ID Instances]的數量類似於點選次數，並可根據實際的廣告點選進行驗證。 我們通常看到[!DNL Search, Social, & Commerce]有85%的符合率，而[!DNL DSP]流量有30%的符合率（篩選為僅包含點進[!UICONTROL AMO ID Instances]時）。 搜尋和顯示之間的預期差異，可以用預期的流量行為來解釋。 搜尋會擷取意圖，因此使用者通常打算從他們的查詢按一下搜尋結果。 然而，看過顯示廣告或線上視訊廣告的使用者更有可能無意中點選廣告，然後或是從網站跳出，或是捨棄在追蹤頁面活動之前載入的新視窗。

在Adobe Advertising報表中，您可以使用&quot;[!UICONTROL EF ID Instances]&quot;量度而非[!UICONTROL AMO ID Instances]，以類似方式比較例項與點按：

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

雖然您應該預期AMO ID與EF ID之間的符合率很高，但不要預期100%的同位檢查，因為AMO ID和EF ID基本上會追蹤不同的資料，而且此差異可能會導致總計[!UICONTROL AMO ID Instances]和[!UICONTROL EF ID Instances]的細微差異。 如果[!DNL Analytics]中的總計[!UICONTROL AMO ID Instances]與Adobe Advertising中的[!UICONTROL EF ID Instances]相差1%以上，請連絡您的Adobe帳戶團隊以尋求協助。

如需AMO ID與EF ID的詳細資訊，請參閱[Analytics使用的Adobe AdvertisingID](ids.md)。

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### 疑難排解點按和執行個體之間的差異

如果[!UICONTROL EF ID Instances]對點按率低於85%，請檢查下列專案：

* 您是否遺漏了帳戶或任何子層級的點選追蹤，或者您是否擁有重複的點選追蹤（例如，帳戶和促銷活動層級）？

  在「搜尋、社交和Commerce」中，[下載帳戶的大量表單](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)以檢查追蹤URL。

  此外，在[!DNL Analytics]中，您可以檢視是否使用&quot;[!DNL AMO ID]至[!DNL EF ID]&quot;計算量度一致附加AMO ID和EF IF，其計算方式如下：

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  大於100%的值表示遺失的EF ID比AMO ID還多。

* 登入頁面是否有載入問題，以致無法擷取AMO ID和EF ID？

* 是否重新導向登陸頁面URL，導致AMO ID和EF ID遺失？

* 所有登入頁面都使用設定的報表套裝嗎？

>[!NOTE]
>
>理論上，一個例項有可能有多個點按。 請務必檢查不同裝置（例如桌上型電腦、行動裝置和平板電腦）上的點選次數。

## 比較[!DNL Analytics for Advertising]中的資料集與Adobe Advertising中的資料集

[AMO ID](ids.md) （s_kwcid查詢字串引數）是用於[!DNL Analytics]中的報告，而[EF ID](ids.md) （ef_id查詢字串引數）是用於Adobe Advertising中的報告。 由於這些值是不同的值，因此一個值可能會損毀或未新增至登陸頁面。

例如，假設我們有下列登陸頁面：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

其中EF ID是&quot;`test_ef_id`&quot;，而AMO ID是&quot;`test_amo_id`&quot;。

如果發生網站端重新導向，則URL結尾可能會像這樣：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

其中EF ID是&quot;`test_ef_id`&quot;，而AMO ID是&quot;`test_amo_id#redirectAnchorTag`&quot;。

在此範例中，加入錨點標籤會在AMO ID中新增非預期字元，導致Analytics無法辨識的值。 此AMO ID不會進行分類，在[!DNL Analytics]個報表中，與其相關的轉換會落在&quot;[!UICONTROL unspecified]&quot;或&quot;[!UICONTROL none]&quot;之下。

幸運的是，雖然這類問題很常見，但通常不會造成高比例的差異。 但是，如果您發現[!DNL Analytics]中的AMO ID與Adobe Advertising中的EF ID之間有大幅差異，請聯絡您的Adobe帳戶團隊以尋求協助。

## 其他量度考量事項

### 點按與造訪之間的差異 {#clicks-vs-visits}

兩者看似類似，但點按和造訪代表不同的資料：

* **點按：** [!DNL DSP]或搜尋引擎在訪客點按發佈者網站上的廣告時記錄點按。

* **造訪：** [!DNL Analytics]會將[造訪](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=zh-Hant)定義為使用者的一系列頁面檢視，並根據數個條件之一結束，例如30分鐘未活動。

顧名思義，點選可能導致多次造訪。

考量以下範例：使用者1和使用者2都可以透過按一下Adobe Advertising廣告來存取網站。 使用者1檢視了四個頁面，然後離開一天了，所以最初的點按會導致一次造訪。 使用者2檢視兩個頁面，離開進行45分鐘的午餐，返回，再檢視兩個頁面，然後離開；在這種情況下，初始點按導致兩次造訪。

![點按與造訪之間差異的範例](/help/integrations/assets/a4adc-visits-example.png)

### 點按與點進之間的差異

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

點按和點進是兩個不同的量度：

* **點按：** [!DNL DSP]或搜尋引擎在訪客點按發佈者網站上的廣告時記錄點按。

* **點進次數：** [!DNL Analytics]在訪客登陸目的地網站時記錄點進，登陸頁面載入，且頁面底部的[!DNL Analytics]請求將資料傳送到[!DNL Analytics]。

點按和點進次數可能會因為意外廣告點按而有很大的差異。 我們觀察到顯示廣告上的大部分點按都是意外點按，且這些意外訪客在登陸頁面載入前點選了「上一步」按鈕，因此[!DNL Analytics]無法記錄點進。 這尤其適用於最有可能意外點選的廣告，例如行動廣告、視訊廣告和填滿畫面的廣告，且必須在使用者檢視頁面之前關閉。

由於頻寬或可用的處理能力較低，在行動裝置上載入的網站也不太可能導致點進，導致載入登陸頁面所需的時間較長。 50-70%的點按不會產生點進次數，這種情況很常見。 在行動環境中，差異可能高達90%，這是由於瀏覽器速度較慢，以及使用者在捲動頁面或嘗試關閉廣告時意外點按廣告的可能性較高。

點按資料也可能會記錄於無法以目前追蹤機制記錄點進的環境中（例如進入或離開行動應用程式的點按），或廣告商僅針對其部署了一種追蹤方法(例如使用閱覽JavaScript方法，即封鎖第三方Cookie追蹤點按但不追蹤點進的瀏覽器)。 Adobe建議同時部署點選URL追蹤和閱覽JavaScript追蹤方法的一個主要原因，就是為了將可追蹤點進的涵蓋範圍最大化。

### 對非Adobe AdvertisingDimension使用Adobe Advertising流量量度

Adobe Advertising為Analytics提供[廣告專用流量量度以及來自 [!DNL DSP] 和 [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md)的相關維度。 Adobe Advertising提供的量度僅適用於指定的Adobe Advertising維度，而且資料不適用於[!DNL Analytics]中的其他維度。

例如，如果您依帳戶檢視[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]量度(這是Adobe Advertising維度)，則帳戶會顯示總計[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]。

![使用Adobe Advertising維度的報表中Adobe Advertising量度的範例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

不過，如果您依頁面上的維度（例如頁面）檢視[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]量度(其Adobe Advertising未提供資料)，則每個頁面的[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]均為零(0)。

![使用不支援之維度的報表中Adobe Advertising量度的範例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用[!UICONTROL AMO ID Instances]代替具有非Adobe AdvertisingDimension的點按

由於您無法將[!UICONTROL AMO Clicks]與網站上的維度搭配使用，因此您可能想要找到等同於點按的維度。 您可能會以造訪次數來替代，但這並非最佳選項，因為每位訪客可能會有多次造訪。 (請參閱&quot;[點按與造訪之間的差異](#clicks-vs-visits)&quot;。 我們建議改用[!UICONTROL AMO ID Instances]，這是擷取AMO ID的次數。 雖然[!UICONTROL AMO ID Instances]與[!UICONTROL AMO Clicks]不完全相符，但這是測量網站點按流量的最佳選項。 如需詳細資訊，請參閱[針對 [!DNL Analytics for Advertising]](#data-validation)的點進資料驗證。

不支援的維度![&#128279;](/help/integrations/assets/a4adc-amo-id-instances.png)的範例[!UICONTROL AMO ID Instances]而非[!UICONTROL Adobe Advertising Clicks]

>[!MORELIKETHIS]
>
>* [總覽 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe AdvertisingID已由 [!DNL Analytics]](/help/integrations/analytics/ids.md)使用
>* 在Analysis Workspace中[Adobe Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [為何資料可能因Adobe Advertising和 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)而異
