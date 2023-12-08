---
title: 預期資料差異： [!DNL Analytics] 和Adobe Advertising
description: 預期資料差異： [!DNL Analytics] 和Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: fb0634643e40b67e50461823f976a93129e2f038
workflow-type: tm+mt
source-wordcount: '3217'
ht-degree: 0%

---

# 預期資料差異： [!DNL Analytics] 和Adobe Advertising

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

使用「 」的廣告商 [!DNL Analytics for Advertising] <!-- (A4AdC) --> 整合可透過Adobe Advertising和Adobe Analytics追蹤付費廣告。 透過多個系統追蹤媒體、行銷活動和管道時，來自不同系統的相同資料集很少完全相符。 本檔案說明應如何預期透過Adobe Advertising販運的媒體資料，與在其中追蹤媒體的不同系統中的資料進行比較 [!DNL Analytics].

>[!NOTE]
>
>本檔案著重於Adobe Advertising和分析，但許多要點也可以轉移到其他追蹤解決方案。

## 類似報表中的歸因差異

### 回顧期間和歸因模型可能不同

此 [!DNL Analytics for Advertising] 整合使用兩個變數([!DNL eVars] 或 [!DNL rVars] \[保留 [!DNL eVars]]\)以擷取 [EF ID和AMO ID](ids.md). 這些變數是透過單一回顧視窗（即點進和檢視歸因的時間）和歸因模型來設定。 除非另有指定，否則變數會設定為符合預設、廣告商層級的點按回顧視窗和Adobe Advertising中的歸因模型。

不過，回顧視窗和歸因模型可在Analytics中設定(透過 [!DNL eVars])和Adobe Advertising中。 此外，在Adobe Advertising中，歸因模型不僅可在廣告商層級（用於競標最佳化）設定，也可在個別資料檢視和報告內設定（僅用於報告目的）。 例如，組織可能偏好使用均勻分佈歸因模型來最佳化，但對Advertising DSP中的報表使用上次接觸歸因，或 [!DNL Advertising Search, Social, & Commerce]. 變更歸因模型會變更已歸因的轉換次數。

如果在一個產品中修改了報表回顧期間或歸因模型，而在另一個產品中修改了報表回顧期間或歸因模型，則來自每個系統的相同報表將顯示不同的資料：

* **不同回顧期間所導致的差異範例：**

  假設Adobe Advertising有60天的點選回顧視窗且 [!DNL Analytics] 有30天的回溯期。 並假設使用者透過Adobe Advertising追蹤廣告進入網站，離開，然後在第45天返回並轉換。 Adobe Advertising會將轉換歸因於初始造訪，因為轉換發生在60天回顧期間內。 [!DNL Analytics]但是，無法將此轉換歸因於初始造訪，因為轉換發生在30天的回顧期間過期之後。 在此範例中，Adobe Advertising報告的轉換次數會高於 [!DNL Analytics] 會。

  ![歸因於Adobe Advertising但不歸因的轉換範例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同歸因模型所導致的差異範例：**

  假設使用者在轉換之前與三個不同的Adobe Advertising廣告互動，且將收入作為轉換型別。 如果Adobe Advertising報表使用均勻分佈模型來歸因，則會將收入平均歸因到所有廣告。 如果 [!DNL Analytics] 不過，會使用上次接觸歸因模型，然後將收入歸因於最後一個廣告。 在以下範例中，Adobe Advertising會將擷取至三個廣告的30美元收入中的平均10美元歸因於每個廣告，而 [!DNL Analytics] 將收入的所有30 USD歸因於使用者看到的最後一個廣告。 當您從Adobe Advertising比較報告與 [!DNL Analytics]，即可預期看出歸因差異的影響。

  ![歸因於Adobe Advertising和的其他收入 [!DNL Analytics] 根據不同的歸因模型](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳實務是在Adobe Advertising和中使用相同的回顧期間和歸因模型 [!DNL Analytics]. 請視需要與您的Adobe帳戶團隊合作，以識別目前設定並維持設定同步。

這些相同的概念適用於使用不同回顧期間或歸因模型的任何其他類似管道。

#### 檢視追蹤的不同回顧期間 {#impression-lookback}

在Adobe Advertising中，歸因是以點按數和曝光數為基礎，您可以為點按數和曝光數設定不同的回顧期間。 在 [!DNL Analytics]不過，歸因是以點進和檢視為基礎，而您不可以選擇為點進和檢視設定不同的歸因期間；追蹤從初次網站造訪開始的每個專案。 曝光可能會在檢視發生的同一天或多個天前發生，這可能會影響每個系統中歸因視窗的開始位置。

一般而言，大部分的檢視轉換發生得足夠快，以至於兩個系統都可計入評分。 不過，有些轉換可能會發生在Adobe Advertising曝光回顧期間之外，但也可能發生在 [!DNL Analytics] 回顧視窗；這類轉換歸因於 [!DNL Analytics] 但不會對Adobe Advertising的印象造成影響。

在以下範例中，假設訪客在第1天收到廣告、在第2天執行瀏覽式造訪（亦即在沒有先前按一下廣告的情況下造訪廣告的登陸頁面），並在第45天轉換。 在此情況下，Adobe Advertising將會從第1天至第14天追蹤使用者（使用14天回溯）， [!DNL Analytics] （使用60天回顧）將追蹤第2至61天的使用者，而第45天的轉換將歸因於 [!DNL Analytics] 但不會在Adobe Advertising內。

![中的檢視轉換範例 [!DNL Analytics] 但不包括Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

不一致的其他原因在於，在Adobe Advertising中，您可以將瀏覽轉換指派給自訂 *檢視權數* 相對於歸因於點選型轉換的權重。 預設的檢視權重為40%，這表示檢視轉換會計為點按式轉換值的40%。 [!DNL Analytics] 不提供此類檢視轉換的加權。 例如，在中擷取的100美元收入訂單 [!DNL Analytics] 如果您使用預設的檢視權數，Adobe Advertising將折扣為40美元，差異為60美元。

比較Adobe Advertising和之間的檢視轉換時，請考量這些差異 [!DNL Analytics] 報表。

#### 可用的歸因模型

| Adobe Advertising歸因 | [!DNL Analytics] 歸因 | [!DNL eVar]/[!DNL rVar] 配置 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 不適用 | 不適用 |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>請勿使用* |
| [!UICONTROL Weight Last Event More] | 不適用 | 不適用 |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 不適用 |
| 不適用 | [!UICONTROL J-Shaped] | 不適用 |
| 不適用 | [!UICONTROL Inverse-J] | 不適用 |
| 不適用 | [!UICONTROL Custom] | 不適用 |
| 不適用 | [!UICONTROL Participation] | 不適用 |
| 不適用 | [!UICONTROL Algorithmic] | 不適用 |

>[!NOTE]
>
>若為線性配置， [!DNL Analytics] 對所有專案平均地屬性化成功事件 [!DNL eVar] 單次造訪中的值，因此請使用線性配置搭配 [!DNL eVar] 「造訪」的到期日。 不過，針對廣告，使用線性歸因會導致配置並非真正為線性，且產生的不太理想的報表。 例如，如果訪客在轉換至三個個別造訪之前與三個廣告互動，則只有上次造訪中看到的廣告會歸因於轉換，而非全部三個廣告。
>
>此外，將轉換配置切換至「線性」或是從「線性」切換分配時，不會顯示歷史資料，而可能導致報表中的資料陳述錯誤。 例如，線性配置可能會將收入分成許多不同的收入 [!DNL eVar] 值。 如果您將配置變更為「最近」，則該收入的100%將與最近的單一值相關聯。 此關聯可能會導致錯誤的結論。
>
>為避免混淆， [!DNL Analytics] 讓歷史資料在報表介面中無法使用。 若您變更以下專案，即可檢視歷史資料： [!DNL eVar] 回到初始配置設定，不過您不應變更 [!DNL eVar] 配置設定僅供存取歷史資料之用。 Adobe建議使用新的 [!DNL eVar] 當您想要為已記錄的資料套用新的配置設定，而不是變更 [!DNL eVar] 已有大量歷史資料。

檢視清單 [!DNL Analytics] 歸因模型及其定義位於 [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

如果您已登入 [!DNL Search, Social, & Commerce]，您可以找到清單

* （北美使用者） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （所有其他使用者） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe Advertising中的事件日期歸因

在Adobe Advertising中，您可以依關聯的點選日期/事件日期（點選或曝光事件的日期）或交易日期（轉換日期）來報告轉換資料。 中不存在點選/事件日期報告的概念 [!DNL Analytics]；所有追蹤的轉換 [!DNL Analytics] 會依交易日期報告。 因此，相同的轉換可能會以不同的日期Adobe Advertising和報告 [!DNL Analytics]. 例如，假設有一位使用者在1月1日點選廣告並在1月5日轉換。 如果您依Adobe Advertising檢視依事件日期的轉換資料，則轉換將會在點選發生時的1月1日回報。 在 [!DNL Analytics]，相同的轉換將在1月5日回報。

![歸因於不同日期的轉換範例](/help/integrations/assets/a4adc-conversions-based-on.png)

## 歸因 [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] 報告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) 可讓您設定規則，以根據點選資訊的不同方面識別不同的行銷管道。 您可以追蹤Adobe Advertising追蹤的管道([!UICONTROL Display Click Through]， [!UICONTROL Display View Through]、和 [!UICONTROL Paid Search])作為 [!DNL Marketing Channels] 藉由使用 `ef_id` 用於識別通道的查詢字串引數。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 然而，即使 [!DNL Marketing Channels] 報表可以追蹤Adobe Advertising管道，資料可能因為Adobe Advertising報表的數個原因而不相符。 如需詳細資訊，請參閱下列章節。

>[!NOTE]
>
> 下列核心概念也適用任何涉及Adobe Advertising中未追蹤之行銷活動的多頻道追蹤，例如 [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 變數(也稱為「追蹤代碼」維度或&quot;[!DNL eVar] 0&quot;)和自訂 [!DNL eVar] 追蹤。

### 中的潛在不同歸因模型 [!DNL Marketing Channels]

最多 [!DNL Marketing Channels] 報告設定了 [!UICONTROL Last Touch] 上次偵測到的行銷管道會針對歸因指定100%的轉換值。 對使用不同的歸因模型 [!DNL Marketing Channels] 報表和Adobe Advertising報表將導致歸因轉換中的差異。

### 中可能不同的回顧期間 [!DNL Marketing Channels]

的回顧期間 [!DNL Marketing Channels] 可自訂。 在Adobe Advertising中，點按回顧視窗是可供設定的，但固定的60天視窗很常見。 如果這兩種產品使用不同的回顧期間，可能會出現資料不一致的情況。

### 中的不同頻道歸因 [!DNL Marketing Channels]

Adobe Advertising報表只會擷取透過Adobe Advertising(付費搜尋 [!DNL Advertising Search, Social, & Commerce] 廣告，以及適用於Advertising DSP廣告的顯示)，但 [!DNL Marketing Channels] 報表可追蹤所有數位頻道。 這可能會導致歸因於轉換的管道不一致。

例如，付費搜尋和免費搜尋管道通常具有共生關係，每個管道互相協助。 此 [!DNL Marketing Channels] 報表會將某些轉換歸因於免費搜尋，但Adobe Advertising不會這麼做，因為它不會追蹤免費搜尋。

也可以考慮檢視顯示廣告、點選付費搜尋廣告、點選電子郵件訊息內部，然後下單30美元的客戶。 即使Adobe Advertising和 [!DNL Marketing Channels] 兩者都使用上次接觸歸因模型，轉換仍會以不同方式歸因於每一個。 Adobe Advertising無權存取 [!UICONTROL Email] 管道，因此會將轉換的付費搜尋視為評分。 [!DNL Marketing Channels]但是，可以存取所有三個管道，因此會獲得評分 [!UICONTROL Email] 進行轉換。

![Adobe Advertising中的不同轉換歸因範例vs [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

如需量度可能有所差異之原因的詳細解釋，請參閱&quot;[為何管道資料可能因Adobe Advertising和事件而異 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).」

## Adobe Analytics中的資料差異 [!DNL Paid Search Detection]

此 [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) 中的功能 [!DNL Analytics] 允許公司 [定義追蹤付費和有機搜尋流量的規則](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) 指定搜尋引擎的。 此 [!DNL Paid Search Detection] 規則會同時使用查詢字串和反向連結網域來識別付費和免費搜尋流量。 此 [!DNL Paid Search Detection] 報表是以下大型群組的一部分： [尋找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) 報表，會在指定事件（例如購物車結帳）發生或造訪結束時過期。

以下是建立 [!DNL Paid Search Detection] 規則集：

![中設定的付費搜尋偵測規則範例 [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

產生的結果 [!DNL Paid Search Detection] 報表包括 [!UICONTROL Paid Search Engine]， [!UICONTROL Paid Search Keywords]， [!UICONTROL Natural Search Engine]、和 [!UICONTROL Natural Search Keywords] 報表。

請注意下列兩種資料限制 [!DNL Paid Search Detection] 報表：

* 此 [!UICONTROL Paid Search Keywords] 和 [!UICONTROL Natural Search Keywords] 報表會顯示由反向連結URL識別的搜尋查詢，而非使用者競標的關鍵字。 Adobe Advertising和 [!DNL Analytics] 報表會顯示實際的關鍵字，因此請勿要求它們與 [!DNL Paid Search Detection] 關鍵字報告。

* 當 [!DNL Paid Search Detection] 這項功能原本是建立的，原始搜尋查詢（使用者在搜尋引擎的搜尋列中輸入的字元字串）可透過轉介URL讓廣告商更容易取得。 現今，搜尋引擎大多將搜尋查詢模糊化， [!DNL Paid Search Detection] 關鍵字報表的值有限，因為大多數查詢資料都在「未指定」下。

  替換為 [!DNL Analytics for Advertising]，廣告商仍可在以下位置追蹤付費關鍵字： [!DNL Analytics]. 反向連結網域會通知引擎報告哪個搜尋引擎帶動了流量。 由於廣告商特定帳戶資訊未繫結至反向連結網域，因此所有流量都會列在搜尋引擎下。 在相同搜尋引擎中有多個帳戶的廣告商，應該參考Adobe Advertising或 [!DNL Analytics] 帳戶特定報表的報表。

### 為何設定 [!DNL Paid Search Detection]？

此 [!DNL Paid Search Detection] 報表可讓您識別以下專案中的免費搜尋流量： [[!DNL Analytics Marketing Channels] 報表](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). 區分付費搜尋流量與免費搜尋流量，是瞭解免費搜尋為完整行銷生態系統帶來價值的重要方法。

## 的點進資料驗證 [!DNL Analytics for Advertising] {#data-validation}

針對您的整合，您應該驗證點進資料，以確保網站上的所有頁面都正確追蹤點進。

在 [!DNL Analytics]，最簡單的驗證方法之一 [!DNL Analytics for Advertising] 追蹤是指使用「點選次數」將點選次數與例項進行比較 [!UICONTROL AMO ID Instances]「計算量度，計算方式如下：

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] 代表此專案發生的次數： [AMO ID](ids.md) 會在網站上受到追蹤。 每次點選廣告時，AMO ID (`s_kwcid`)引數已新增至登陸頁面URL。 「 」的數量 [!UICONTROL AMO ID Instances]因此，類似於點選次數，可根據實際廣告點選進行驗證。 我們通常看到80%的符合率 [!DNL Search, Social, & Commerce] 和30%符合率 [!DNL DSP] 流量（篩選為僅包含點進時） [!UICONTROL AMO ID Instances])。 搜尋和顯示之間的預期差異，可以用預期的流量行為來解釋。 搜尋會擷取意圖，因此使用者通常打算從他們的查詢按一下搜尋結果。 然而，看過顯示廣告或線上視訊廣告的使用者更有可能無意中點選廣告，然後或是從網站跳出，或是捨棄在追蹤頁面活動之前載入的新視窗。

在Adobe Advertising報表中，您也可使用&quot;[!UICONTROL ef_id_instances]「量度而非 [!UICONTROL AMO ID Instances]：

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

雖然您應該預期AMO ID和EF ID之間的符合率很高，但不要預期100%的同位檢查，因為AMO ID和EF ID基本上會追蹤不同的資料，而這個差異可能會導致總數略有差異 [!UICONTROL AMO ID Instances] 和 [!UICONTROL EF ID Instances]. 如果總計 [!UICONTROL AMO ID Instances] 在 [!DNL Analytics] 差異於 [!UICONTROL EF ID Instances] 超過1%的Adobe Advertising客戶，請連絡您的Adobe客戶團隊以尋求協助。

如需AMO ID和EF ID的詳細資訊，請參閱 [Analytics使用的Adobe AdvertisingID](ids.md).

以下為追蹤例項點按的工作區範例。

![追蹤例項點按的工作區範例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比較中的資料集 [!DNL Analytics for Advertising] 與Adobe Advertising中的比較

此 [AMO ID](ids.md) （s_kwcid查詢字串引數）適用於中的報表 [!DNL Analytics]，以及 [EF ID](ids.md) 用於Adobe Advertising中的報告。 由於這些值是不同的值，因此一個值可能會損毀或未新增至登陸頁面。

例如，假設我們有下列登陸頁面：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

其中EF ID為&quot;`test_ef_id`」且AMO ID為「`test_amo_id`.」

如果發生網站端重新導向，則URL結尾可能會像這樣：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

其中EF ID為&quot;`test_ef_id`」且AMO ID為「`test_amo_id#redirectAnchorTag`.」

在此範例中，加入錨點標籤會在AMO ID中新增非預期字元，導致Analytics無法辨識的值。 此AMO ID將不會進行分類，而且與其相關的轉換會落在「[!UICONTROL unspecified]「或」[!UICONTROL none]&quot; in [!DNL Analytics] 報表。

幸運的是，雖然這類問題很常見，但通常不會造成高比例的差異。 不過，如果您發現中的AMO ID之間有很大差異， [!DNL Analytics] 和EF IDAdobe Advertising，請聯絡您的Adobe帳戶團隊以尋求協助。

## 其他量度考量事項

### 點按與造訪之間的差異 {#clicks-vs-visits}

兩者看似類似，但點按和造訪代表不同的資料：

* **按一下：** [!DNL DSP] 或者，當訪客點按發佈商網站上的廣告時，搜尋引擎會記錄一次點按。

* **造訪：** [!DNL Analytics] 定義 [造訪](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 作為使用者的一系列頁面檢視，根據數個條件之一結束，例如30分鐘閒置。

顧名思義，點選可能導致多次造訪。

考量以下範例：使用者1和使用者2都可以透過按一下Adobe Advertising廣告來存取網站。 使用者1檢視了四個頁面，然後離開一天了，所以最初的點按會導致一次造訪。 使用者2檢視兩個頁面，離開進行45分鐘的午餐，返回，再檢視兩個頁面，然後離開；在這種情況下，初始點按導致兩次造訪。

![點按與造訪之間差異的範例](/help/integrations/assets/a4adc-visits-example.png)

### 點按與點進之間的差異

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

點按和點進是兩個不同的量度：

* **按一下：** [!DNL DSP] 或者，當訪客點按發佈商網站上的廣告時，搜尋引擎會記錄一次點按。

* **點進次數：** [!DNL Analytics] 會記錄訪客在登陸目的地網站時的點進、登陸頁面載入，以及 [!DNL Analytics] 頁面底部的請求會將資料傳送至 [!DNL Analytics].

點按和點進次數可能會因為意外廣告點按而有很大的差異。 我們觀察到顯示廣告上的大部分點按都是意外點按，且這些意外訪客在登陸頁面載入之前點選了「上一步」按鈕，因此 [!DNL Analytics] 無法錄製點進。 這尤其適用於最有可能意外點選的廣告，例如行動廣告、視訊廣告和填滿畫面的廣告，且必須在使用者檢視頁面之前關閉。

由於頻寬或可用的處理能力較低，在行動裝置上載入的網站也不太可能導致點進，導致載入登陸頁面所需的時間較長。 50-70%的點按不會產生點進次數，這種情況很常見。 在行動環境中，差異可能高達90%，這是由於瀏覽器速度較慢，以及使用者在捲動頁面或嘗試關閉廣告時意外點按廣告的可能性較高。

點按資料也可能會記錄於無法使用目前追蹤機制記錄點進的環境中（例如進入或離開行動應用程式的點按），或廣告商僅針對其部署了一種追蹤方法的環境中（例如使用閱覽JavaScript方法，封鎖第三方Cookie的瀏覽器將追蹤點進，但不會追蹤點進）。 Adobe建議同時部署點選URL追蹤和閱覽JavaScript追蹤方法的一個主要原因，就是為了將可追蹤點進的涵蓋範圍最大化。

### 對非Adobe AdvertisingDimension使用Adobe Advertising流量量度

Adobe Advertising為Analytics提供 [廣告專用流量量度和相關維度，來自 [!DNL DSP] 和 [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Adobe Advertising提供的量度僅適用於指定的Adobe Advertising維度，而且資料不適用於中的其他維度。 [!DNL Analytics].

例如，如果您檢視 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 「依帳戶」的量度(這是Adobe Advertising維度)，您就會看到總計 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 依帳戶。

![在報表中使用Adobe Advertising維度來Adobe Advertising量度的範例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

不過，如果您檢視 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 依頁面維度（例如頁面）的量度(若其Adobe Advertising未提供資料)，則 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 對於每一頁，則是零(0)。

![使用不支援之維度的報表中Adobe Advertising量度的範例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] 以非Adobe AdvertisingDimension代替點按

因為您無法使用 [!UICONTROL AMO Clicks] 若使用網站上的維度，您可以找到等同於點按的維度。 您可能會以造訪次數來替代，但這並非最佳選項，因為每位訪客可能會有多次造訪。 (請參閱&quot;[點按與造訪之間的差異](#clicks-vs-visits).」 我們建議改用 [!UICONTROL AMO ID Instances]，即擷取AMO ID的次數。 當 [!UICONTROL AMO ID Instances] 將不符合 [!UICONTROL AMO Clicks] 確切地說，這是測量網站點按流量的最佳選項。 如需詳細資訊，請參閱&quot;[的點進資料驗證 [!DNL Analytics for Advertising]](#data-validation).」

![範例： [!UICONTROL AMO ID Instances] 而非 [!UICONTROL Adobe Advertising Clicks] 針對不支援的維度](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis Workspace中的Adobe Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [為何資料可能因Adobe Advertising與不同而異 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
