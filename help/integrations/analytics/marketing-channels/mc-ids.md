---
title: 使用Adobe AdvertisingID建立 [!DNL Marketing Channels] 規則
description: 瞭解如何使用Adobe AdvertisingID來建立 [!DNL Analytics Marketing Channels]的處理規則。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# 使用Adobe AdvertisingID建立[!DNL Marketing Channels]處理規則

*僅整合Adobe Advertising-Adobe Analytics的廣告商*

您可以使用Adobe AdvertisingID （[AMO ID和EF ID](../ids.md)）在Adobe Analytics中設定[!DNL Marketing Channels]處理規則。 針對您Adobe Advertising促銷活動的特定規則，使用Adobe AdvertisingID。

## 處理規則中的AMO ID

AMO ID是用於報告[!DNL Analytics]內Adobe Advertising資料的主要追蹤程式碼。 AMO ID是由Adobe管理的動態值串連，以在[!DNL Analytics]內提供精細報表。 它儲存在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=zh-Hant)或rVar維度(AMO ID)中。 AMO ID可在[!DNL Analytics]中設定有兩種方式：

* 點進追蹤：Adobe Advertising會在連結中設定`s_kwcid`查詢字串引數，而當點進發生時，[!DNL Analytics]會從登陸頁面URL中挑選引數。
* 檢視追蹤（僅限[!DNL DSP]）： Last Event Service會在伺服器端偵測檢視，並將AMO ID傳送至[!DNL Analytics]。 在此情況下，URL不包含`s_kwcid`引數。

AMO ID中的動態值表示所追蹤的行銷管道：

* AMO ID中的前置字元可用來識別[!DNL Marketing Channels]中的最上層通道。

* AMO ID內文中的字元短語表示更具體的行銷活動型別。

* 尾碼「vt」適用於[!DNL DSP]閱覽流量，可用來建立個別的點進和閱覽[!DNL DSP]管道。

可忽略其餘的AMO ID。

| [!UICONTROL AMO ID] | 頻道 | 規則邏輯 |
|--------|---------|--------------------|
| ！ctv （尾碼） | [!UICONTROL DSP Connected TV View-through] | 結尾為 |
| ！d！ （內文） | [!UICONTROL Display Network] | 包含 |
| ！g！ （內文） | [!UICONTROL Google Search] | 包含 |
| ！s！ （內文） | [!UICONTROL Search Partner] | 包含 |
| ！u！ （內文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| ！ytv！ （內文） | [!UICONTROL YouTube Video Ad] | 包含 |
| ！yts！ （內文） | [!UICONTROL YouTube Search Ad] | 包含 |
| ！vp！ （內文） | [!UICONTROL Google Video Partners] | 包含 |
| ！vt （尾碼） | [!UICONTROL DSP View-through] | 結尾為 |
| 阿爾！ （前置詞） | [!UICONTROL Paid Search] | 開頭為 |
| AC！ （前置詞） | [!UICONTROL DSP] | 開頭為 |

### 使用AMO ID的處理規則範例

[!UICONTROL Paid Search]管道的[!DNL Marketing Channels]處理規則可能如下所示：

![ [!UICONTROL Paid Search]規則的範例](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

[!UICONTROL YouTube Video Ads]管道的[!DNL Marketing Channels]處理規則可能如下所示：

![ [!UICONTROL YouTube Video Ads]規則的範例](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 請務必依序執行您的規則。 如果以上兩個規則依序執行，[!DNL YouTube]視訊廣告流量將全部落在[!UICONTROL Paid Search]頻道之下，因為AMO ID的開頭都會是「AL！」 並包含「！ytv！」。

## 處理規則中的EF ID

AMO EF ID (EF ID)是[!DNL Analytics for Advertising]整合中使用的第二個追蹤程式碼。 其主要用途是追蹤並將[!DNL Analytics]個事件資料傳遞至Adobe Advertising。 每次點進或檢視發生時，系統都會產生唯一的EF ID，即使同一位訪客擁有完全相同的廣告亦然。 [!DNL Analytics]報表使用者介面中未使用EF ID，因為它通常會超過[!DNL Analytics]中每個變數限制500,000個不重複值，使其無法用於報表。 Adobe Advertising量度和中繼資料不會套用至EF ID，而只會套用至AMO ID。 Adobe Advertising中的行銷活動最佳化需要新增的追蹤粒度，因此兩個ID都是必要的。

雖然EF ID維度並未直接在[!DNL Analytics]報表中使用，但EF ID仍適合用於建立行銷管道。 EF ID尾碼會指出頻道（顯示或搜尋），以及造訪是由點進還是檢視所驅動。 EF ID中的分隔符號是冒號，而非AMO ID中的驚歎號。

| EF ID尾碼 | 頻道 |
|-------|---------|
| ：s | [!UICONTROL Paid Search] |
| ：d | [!UICONTROL Display Click-through] |
| ：i | [!UICONTROL Display View-through] |

### 使用EF ID的處理規則範例

#### 顯示點進規則

僅擷取點進次數，以建立「顯示」點進行銷管道。 因為點進和檢視的AMO ID相同，所以此規則會使用EF ID變數和`ef_id`查詢字串引數。

有時會透過URL （預設值）追蹤點進。 在其他情況下，點進是透過伺服器端的「上次事件服務」追蹤，因此URL不包含`ef_id`引數。 因此，規則會檢查EF ID變數或`ef_id`查詢字串引數結尾為&quot;：d&quot;的條件。 使用&quot;`Any`&quot;運運算元，因為您想要為任一條件觸發此規則。

![顯示點進規則的範例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 顯示檢視規則

若要建立「顯示」檢視管道，請建立EF ID結尾為&quot;：i&quot;的規則。 由於訪客未按一下廣告，瀏覽追蹤不會在URL中包含`ef_id`或`s_kwcid`，因此規則只需要一個條件。

![顯示檢視規則範例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [基礎（共 [!DNL Analytics Marketing Channels]](mc-overview.md)個）
>* [為什麼管道資料在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之間可能不同
>* [搭配Adobe Advertising資料使用 [!DNL Analytics Marketing Channels] ](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 進行Adobe Advertising報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hant)
>* [Adobe AdvertisingID已由 [!DNL Analytics]](/help/integrations/analytics/ids.md)使用
