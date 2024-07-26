---
title: 連線電視連線方案的設定
description: 請參閱連線電視觸及計畫的設定說明。
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 84cf49c9e366938479e9fea2ede55925f1cb3e51
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# 連線電視連線方案的設定

| 引數 | 說明 | 必填？ |
| --- | --- | --- |
| [!UICONTROL Name] | 用來識別計畫的名稱。 | 是 |
| [!UICONTROL Advertiser] | 帳戶中為其建立計畫的特定廣告商。 | 是 |
| [!UICONTROL Media Type] | 要納入計畫中的媒體型別。<br><br>目前只有[!UICONTROL Connected TV]可用。 | 是 |
| [!UICONTROL Date Range] | 計畫的開始和結束日期。<br><br>開始日期不能早於目前日期。 日期範圍不得超過90天。 | 是 |
| [!UICONTROL Goal Type] | 要考慮用於計畫的目標型別（例如[!UICONTROL Budget]）。<br><br>目前只有[!UICONTROL Budget]可用。 | 是 |
| [!UICONTROL Goal Value] | 預測的目標值。 如需更精確的預測結果，請使用大於5000 USD的值。 | 是 |
| [!UICONTROL Max Bid] | 針對1000次曝光要支付的最大金額。 如果選取了[!UICONTROL Connected TV]媒體型別，請輸入至少10美元的值。 | 是 |
| [!UICONTROL Frequency Cap] | 不重複住戶應該收到廣告的次數。<br><br>當您實作計畫且必須建立多個刊登版位時，請在封裝層級（而非刊登版位層級）套用頻率上限設定，以確保正確傳遞。 | 是 |
| [!UICONTROL Geo-Targeting] | 作為目標包含或排除的位置。 選項包括：<ul><li>國家、城市、州：按一下&#x200B;**[!UICONTROL Country/State/City]**&#x200B;標籤；選取區域是&#x200B;*國家*、*州*&#x200B;或&#x200B;*城市*；可選擇展開任何位置以檢視其子元件，然後按一下位置旁的&#x200B;**[!UICONTROL Include]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**。</li><li>美國的指定市場區域(DMA)：按一下&#x200B;**[!UICONTROL DMA]**&#x200B;標籤；可選擇展開任何狀態以檢視其DMA，然後按一下位置旁的&#x200B;**[!UICONTROL Include]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**。</li><li>郵遞區號：您可以：<ul><li>按一下「**[!UICONTROL Search postal code]**」標籤、選取國家、輸入完整的城市名稱或城市名稱內含的字母，然後按&#x200B;**[Enter]**&#x200B;鍵、按一下正確的城市名稱以檢視該城市的所有郵遞區號、按一下正確的郵遞區號，然後按一下&#x200B;**[!UICONTROL Include]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**。</li><li>按一下&#x200B;**[!UICONTROL Paste postal code]**&#x200B;標籤，選取國家，輸入或貼上逗號分隔值，然後按一下&#x200B;**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。</li></ul></li></ul> | 是 |
| [!UICONTROL Inventory Targeting] | 要納入或排除作為目標的詳細目錄來源。 請至少選取一個摘要或來源。 | 是 |
| [!UICONTROL Site/App Targeting] | 要納入或排除作為目標的網站和應用程式。 每行輸入一個網址，然後按一下&#x200B;**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。 | 否 |
| [!UICONTROL Audience Targeting] | 要納入或排除作為目標的對象。 | 否 |
| [!UICONTROL Ad duration] | 要考量用於計畫的廣告持續時間。 | 否 |

>[!MORELIKETHIS]
>
>* [關於DSP Planner工具](planner-about.md)
>* [建立連線電視觸及計畫](planner-create.md)
>* [複製連線電視連線計畫](planner-duplicate.md)
>* [編輯連線電視觸及計畫](planner-edit.md)
>* [匯出連線電視觸及計畫](planner-export.md)
>* [重新產生連線電視觸及計畫的預測](planner-forecast.md)
>* [封存連線電視觸及計畫](planner-archive.md)
