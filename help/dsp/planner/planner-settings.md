---
title: 連線電視連線方案的設定
description: 請參閱連線電視觸及計畫的設定說明。
feature: DSP Planner
source-git-commit: 72ee396019d5a444bd326fe659ce68eb3490a439
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 連線電視連線方案的設定

*Beta功能*

| 引數 | 說明 | 必填？ |
| --- | --- | --- |
| 名稱 | 用來識別計畫的名稱。 | 是 |
| 廣告商 | 帳戶中為其建立計畫的特定廣告商。 | 是 |
| 媒體型別 | 要納入計畫中的媒體型別。<br><br>目前，僅限 [!UICONTROL Connected TV] 可用。 | 是 |
| 日期範圍 | 計畫的開始和結束日期。<br><br>開始日期不能早於目前日期。 日期範圍不得超過90天。 | 是 |
| 目標型別 | 目標的型別(例如 [!UICONTROL Budget])考量納入計畫。<br><br>目前，僅限 [!UICONTROL Budget] 可用。 | 是 |
| 目標值 | 預測的目標值。 如需更精確的預測結果，請使用大於5000 USD的值。 | 是 |
| 最高出價 | 針對1000次曝光要支付的最大金額。 如果 [!UICONTROL Connected TV] 媒體型別已選取，請輸入至少10美元的值。 | 是 |
| 頻率上限 | 不重複住戶應該收到廣告的次數。<br><br>若您實作計畫且必須建立多個版位，請在封裝層級（而非版位層級）套用頻率上限設定，以確保正確傳送。 | 是 |
| 地理定位 | 作為目標包含或排除的位置。 | 是 |
| 詳細目錄目標定位 | 要納入或排除作為目標的詳細目錄來源。 請至少選取一個摘要或來源。 | 是 |
| 對象目標定位 | 要納入或排除作為目標的對象。 | 否 |
| 廣告持續時間 | 要考量用於計畫的廣告持續時間。 | 否 |

>[!MORELIKETHIS]
>
>* [關於DSP Planner工具](planner-about.md)
>* [建立連線電視連線計畫](planner-create.md)
>* [複製連線電視連線計畫](planner-duplicate.md)
>* [編輯連線電視連線計畫](planner-edit.md)
>* [匯出連線電視觸及計畫](planner-export.md)
>* [重新產生連線電視觸及計畫的預測](planner-forecast.md)
>* [封存連線電視觸及計畫](planner-archive.md)
