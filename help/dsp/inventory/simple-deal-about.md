---
title: 關於[!UICONTROL Simple Ad Serving]
description: 瞭解使用事件追蹤畫素的[!UICONTROL Simple Ad Serving]筆交易。
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 關於[!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving]會使用單一專屬版位，為指定發行者及單一廣告型別提供保證、未決策的廣告傳送及報告。 當您的發行者無法透過交易識別碼執行您的交易時，請使用[!DNL Simple Ad Serving]。 所有目標定位、預算步調和上限，以及頻率上限都由發佈商處理。 透過事件追蹤畫素執行這些交易。

透過[!UICONTROL Simple Ad Serving]，每個廣告會由發佈者（網站服務）直接提供，而DSP會提供事件追蹤畫素以傳送給發佈者，發佈者必須實作畫素並流量DSP廣告。 視詳細目錄型別而定，事件畫素會測量曝光數、點進次數和視訊播放事件。

提供下列廣告型別：

* 桌上型電腦標準前段
* 平板電腦和行動標準前段廣告
* 連線電視標準前段
* 顯示
* 音訊

您可以在[!UICONTROL Inventory] > [!UICONTROL Deals]檢視中建立[!UICONTROL Simple Ad Serving]交易。 DSP會自動為廣告產生子型別為&quot;[!DNL Simple ad serving]&quot;的位置。 此位置將目標鎖定在交易，但不允許額外的目標定位、預算或頻率上限。 您只能編輯部分交易設定，例如交易名稱、CPM、曝光次數和投放日期。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving]個刊登版位不符合帳戶的可用資金，或行銷活動和封裝預算。 但是，支出會被追蹤並計入這些預算。 即使CPM為$0，系統仍一律會追蹤事件資料。

>[!MORELIKETHIS]
>
>* [建立[!UICONTROL Simple Ad Serving]交易](simple-deal-create.md)
>* [編輯[!UICONTROL Simple Ad Serving]交易設定](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving]設定](simple-deal-settings.md)
>* [檢視交易的詳細報告](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
