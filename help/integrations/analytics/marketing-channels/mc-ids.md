---
title: 使用Adobe廣告ID建立 [!DNL Marketing Channels] 規則
description: 瞭解如何使用Adobe廣告ID建立處理規則 [!DNL Analytics Marketing Channels]。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# 使用Adobe廣告ID建立 [!DNL Marketing Channels] 處理規則

*具有Adobe廣告的廣告商 — 僅Adobe Analytics整合*

可以使用Adobe廣告ID([AMO ID和EF ID](../ids.md)) [!DNL Marketing Channels] 在Adobe Analytics處理規則。 將Adobe廣告ID用於特定於Adobe廣告活動的規則。

## 處理規則中的AMO ID

AMO ID是用於報告Adobe廣告資料的主跟蹤代碼 [!DNL Analytics]。 AMO ID是由Adobe管理的動態值的級聯，用於在 [!DNL Analytics]。 存放在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維(AMO ID)。 可以在中設定AMO ID [!DNL Analytics] 通過兩種方式：

* 點擊跟蹤：Adobe廣告設定 `s_kwcid` 查詢連結中的字串參數，和 [!DNL Analytics] 在進行按一下時從登錄頁URL中選取參數。
* 查看跟蹤([!DNL DSP] 僅):最後一個事件服務在伺服器端檢測到查看，並將AMO ID發送到 [!DNL Analytics]。 在這種情況下，URL不包含 `s_kwcid` 的下界。

AMO ID中的動態值指示跟蹤的市場營銷渠道：

* AMO ID中的前置詞可用於標識內的頂級通道 [!DNL Marketing Channels]。

* AMO ID正文中的字元短語表示更具體的促銷活動類型。

* 尾碼「vt」存在於 [!DNL DSP] 查看通道流量，可用於建立單獨的點擊通道和查看通道 [!DNL DSP] 頻道。

可以忽略AMO ID的其餘部分。

| AMO ID | 頻道 | 規則邏輯 |
|--------|---------|--------------------|
| 阿爾！ （前置詞） | [!UICONTROL Paid Search] | 開頭為 |
| AC! （前置詞） | [!UICONTROL DSP] | 開頭為 |
| !g! （正文） | [!UICONTROL Google Search] | 包含 |
| !s! （正文） | [!UICONTROL Search Partner] | 包含 |
| !d! （正文） | [!UICONTROL Display Network] | 包含 |
| !u! （正文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| !ytv! （正文） | [!UICONTROL YouTube Video Ad] | 包含 |
| !yts! （正文） | [!UICONTROL YouTube Search Ad] | 包含 |
| !vp! （正文） | [!UICONTROL Google Video Partners] | 包含 |
| !vt（尾碼） | [!UICONTROL DSP View-through] | 結尾為 |

### 使用AMO ID的處理規則示例

的 [!DNL Marketing Channels] 處理規則 [!UICONTROL Paid Search] channel可能如下所示：

![示例 [!UICONTROL Paid Search] 規則](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

的 [!DNL Marketing Channels] 處理規則 [!UICONTROL YouTube Video Ads] channel可能如下所示：

![示例 [!UICONTROL YouTube Video Ads] 規則](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 請確保按特定順序運行規則。 如果上述兩條規則按順序運行， [!DNL YouTube] 視頻廣告流量都會被淹沒 [!UICONTROL Paid Search] 因為AMO ID都以&quot;AL!&quot;開頭 並包含&quot;!ytv!&quot;

## 處理規則中的EF ID

AMO EF ID(EF ID)是在 [!DNL Analytics for Advertising] 整合。 它的主要目的是跟蹤和通過 [!DNL Analytics] 事件資料到Adobe廣告。 每次按一下或查看時，都會生成唯一的EF ID，即使它與同一訪問者的廣告完全相同。 EF ID未在 [!DNL Analytics] 報告用戶介面，因為它通常超過了 [!DNL Analytics]使其無法用於報告。 Adobe廣告度量和元資料不應用於EF ID;它們僅應用於AMO ID。 在Adobe廣告中，市場活動優化需要增加的跟蹤粒度，因此需要兩個ID。

雖然EF ID維未直接用於 [!DNL Analytics] 報告時，EF ID在建立市場營銷渠道時非常有用。 EF ID尾碼指示通道（顯示或搜索），以及訪問是由點擊還是查看驅動的。 EF ID中的分隔符是冒號，而不是AMO ID中的感嘆號。

| EF ID尾碼 | 頻道 |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### 使用EF ID的處理規則示例

#### 顯示點擊規則

通過僅捕獲點擊提示建立「顯示」點擊直通市場營銷渠道。 由於AMO ID對於按一下檢查和查看檢查是相同的，因此此規則使用EF ID變數和 `ef_id` 查詢字串參數。

有時，通過URL（預設）跟蹤點擊瀏覽。 在其它情況下，通過伺服器端的「上次事件服務」跟蹤點擊進度，因此URL不包含 `ef_id` 的下界。 因此，該規則檢查EF ID變數或 `ef_id` 查詢字串參數以「：d」結尾。 使用「」`Any`&quot;運算子，因為您希望為任一條件觸發此規則。

![顯示的「點擊」規則示例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 顯示查看規則

要建立「顯示」視圖通道，請建立EF ID以「：i」結尾的規則。 由於訪問者沒有按一下廣告，因此查看跟蹤不包括 `ef_id` 或 `s_kwcid` 的子菜單。

![顯示透視圖規則示例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [渠道資料為何會因Adobe廣告和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] Adobe廣告資料](mc-ac-data.md)
>* [視頻：使用 [!DNL Marketing Channels] 用於Adobe廣告報告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe廣告ID [!DNL Analytics]](/help/integrations/analytics/ids.md)

