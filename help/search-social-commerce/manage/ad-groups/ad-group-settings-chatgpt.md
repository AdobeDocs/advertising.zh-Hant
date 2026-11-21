---
title: '[!DNL ChatGPT]廣告群組設定'
description: 參考[!DNL ChatGPT]廣告群組的設定。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
source-git-commit: 487af67f7215bf4a070af5e813649288141b0ed4
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# [!DNL ChatGPT]廣告群組設定

[!DNL ChatGPT]中的&#x200B;*廣告是[!DNL OpenAI]*&#x200B;的試行功能

## [!UICONTROL Basic Settings]索引標籤

*僅限新廣告群組*

**[!UICONTROL Network]：**&#x200B;廣告網路。

**[!UICONTROL Account]：**&#x200B;廣告網路帳戶。

**[!UICONTROL Campaign]：**&#x200B;行銷活動。 建立廣告群組後，就無法變更促銷活動。

## [!UICONTROL Ad Group Details]索引標籤

**[!UICONTROL Ad Group name]：**&#x200B;促銷活動中的唯一廣告群組名稱，至少包含三個字元。

**[!UICONTROL Status]：**&#x200B;廣告群組的顯示狀態： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。 新廣告群組的預設值為&#x200B;*[!UICONTROL Active]*。

**[!UICONTROL Bid strategy]：** （具有目標[!UICONTROL Clicks]或[!UICONTROL Conversions]的行銷活動）如何競標廣告群組中的廣告：

* *[!UICONTROL Autobid]：* （新廣告群組的預設值） [!DNL OpenAI]會根據行銷活動目標，自動調整競標以從您的預算中獲得最多點按次數或轉換次數。 您沒有輸入競標金額。 此選項適用於每日和期限行銷活動預算。

* *[!UICONTROL Target CPC]：* （具有目標[!UICONTROL Clicks]的行銷活動）對每次點按平均成本目標的出價。 在[!UICONTROL Target CPC]欄位中輸入目標。

* *[!UICONTROL Target CPA]：* （具有目標[!UICONTROL Conversions]的行銷活動）朝向平均每次轉換成本目標投標。 在[!UICONTROL Target CPA]欄位中輸入目標。

* *[!UICONTROL Manual: Max bid]：* （僅現有手動競標廣告群組）以唯讀金額保留現有的最高競標。 您可以保留此策略，或切換至[!UICONTROL Autobid]或行銷活動目標的目標策略。 此選項不適用於新的廣告群組，或編輯已使用自動競標或目標競標的廣告群組時。

現有的手動競標廣告群組不會自動變更為其他策略。 僅編輯目標金額或不相關的設定不會變更現有的目標競標策略。

**[!UICONTROL Target CPC]：** （競標策略為[!UICONTROL Target CPC]的廣告群組；必要）您想要實現的每次點按平均成本（以帳戶的貨幣表示）。 輸入正數。 這是平均成本目標，而非最高出價。

**[!UICONTROL Target CPA]：** （競標策略為[!UICONTROL Target CPA]的廣告群組；必要）您想要實現的每次轉換平均成本（以帳戶的貨幣表示）。 輸入正數。 這是平均成本目標，而非最高出價。

**[!UICONTROL Maximum CPC bid]：** （具有目標[!UICONTROL Clicks]的行銷活動；僅現有的手動競標廣告群組；唯讀）您每次點按支付的現有最高金額。

**[!UICONTROL Conversion-optimized bid cap]：** （具有目標[!UICONTROL Conversions]的行銷活動；僅現有的手動競標廣告群組；唯讀）您願意為轉換競標的現有最大金額。 [!DNL OpenAI]使用預測的轉換率，將此值轉換為每次曝光的拍賣競標。

**[!UICONTROL Maximum CPM bid]：** （具有目標[!UICONTROL Reach]的行銷活動）您以帳戶的貨幣支付一千次曝光的最大金額。 輸入0.01到5000之間的值。 觸及行銷活動沒有[!UICONTROL Bid strategy]選項。

**[!UICONTROL Context hints (optional)]：**&#x200B;您的產品或服務可能相關的交談、主題或關鍵字的說明。 以逗號或分行符號分隔提示。 您的提示可用於引導比對，但不是完全相符的目標規則。 請參閱[[!DNL ChatGPT Ads] 有關如何撰寫有效內容提示的說明](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints)。

**[!UICONTROL Landing Page Suffix]：** （選用）任何要附加至登陸頁面URL結尾以追蹤資訊的引數。 範例： `param1=value1&param2=value2`。

>[!MORELIKETHIS]
>
>* [管理廣告群組](ad-group-manage.md)
