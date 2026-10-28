---
title: 使用AI助理疑難排解效能和傳送問題
description: 使用Adobe Advertising DSP AI Assistant的疑難排解代理程式，診斷DSP套件和位置的支出、步調和傳送問題。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 0f6d32b5409cc95f09d0b0f28cdeee72a7861892
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%
---
# 使用AI助理疑難排解效能和傳送問題

*Beta功能*

*僅支援英文*

AI Assistant的疑難排解代理程式會識別限制即時套件和位置效能的因素，並根據歷史資料提供逐步指示和建議，以解決問題。 疑難排解代理程式可協助診斷下列型別的效能和傳送問題：

* （僅限刊登版位）支出問題，包括超支、支出過少及無法支出。 代理程式會評估診斷過程中相關的步調、競標、目標定位和預算上限因素。

* （僅限套件）效能問題，包括CPA上升或ROAS下降。 代理程式不會診斷參與量度，例如CTR、CPC、點按或曝光數。

每個交談都涵蓋單一套件或位置的單一診斷。 代理程式傳送結果後，即會開始新的交談，詢問不同的問題或不同的封裝或位置。

代理程式無法變更設定；建立或編輯行銷活動或行銷活動元件；或診斷暫停、完成、封存或排程封裝或位置的問題。

>[!IMPORTANT]
>
>AI產生的回應可能不準確或誤導。 一律先驗證回應和來源，再將其用於影響成本或投入的決策。

## 範例查詢

### 疑難排解刊登廣告支出問題

* 我的刊登版位昨天停止花費，即使交易進行中。 為什麼？

* 為什麼這個位置在過去5天支出不足？

* 我們飛行已經過半，步調明顯落後。 為什麼？

### 疑難排解套件效能問題

* 為什麼這個封裝的CPA在上星期有所增加？

* 為何ROAS拒絕此套件？

## 從AI助理提交查詢

您可以在一則訊息中詢問多個問題，但一次只能詢問一則訊息。 請等待回應，然後再傳送其他回應。

1. 按一下任何頁面右上角的![代理聊天](/help/dsp/assets/agent-chat.png "代理聊天")。

1. 建置查詢：

   * 輸入您自己的查詢。

   * 若要檢視查詢範例，請按一下&#x200B;**[!UICONTROL Troubleshoot]**&#x200B;展開區段。

     1. （選擇性）若要將範例查詢的文字複製到輸入欄位：

        1. 按一下範例。

        1. （選用）編輯文字以符合您的需求。

   如需有關查詢的詳細資訊，請參閱[撰寫查詢和提示的最佳實務](ai-assistant-about.md#writing-queries)。

   >[!NOTE]
   >
   >* 如果您未指定日期範圍，則代理程式會根據問題型別選取合理的預設值。 例如，如果您在詢問促銷活動量度時未指定日期範圍，則結果會針對促銷活動持續時間。
   >* 如果您有目標CPA，請將其納入查詢中（例如「針對目標$50診斷CPA」）。 如果您未指定目標，代理程式就會使用預設目標。

1. 按一下![送出查詢](/help/dsp/assets/submit-prompt.png "送出查詢")，或按鍵盤上的&#x200B;**Enter**&#x200B;鍵。

1. 如果AI助理要求其他資訊，請提供。

>[!TIP]
>
>若要詢問其他問題，或關於其他封裝或位置，[開始新的交談](#conversation-new)。

## 從[!UICONTROL Packages]或[!UICONTROL Placements]檢視提交查詢

您可以在一則訊息中詢問多個問題，但一次只能詢問一則訊息。 請等待回應，然後再傳送其他回應。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下行銷活動的名稱。

1. 執行下列任一項作業：

   * （適用於封裝）在[!UICONTROL Packages]檢視中，按一下封裝名稱旁的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**。

   * （針對位置）在子功能表中，按一下&#x200B;**[!UICONTROL Placements]**。 在位置名稱旁，按一下「**[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**」。

1. 建置查詢：

   * 輸入您自己的查詢。

   * 若要檢視查詢範例，請按一下&#x200B;**[!UICONTROL Troubleshoot]**&#x200B;展開區段。

     1. （選擇性）若要將範例查詢的文字複製到輸入欄位：

        1. 按一下範例。

        1. （選用）編輯文字以符合您的需求。

   如需有關查詢的詳細資訊，請參閱[撰寫查詢和提示的最佳實務](ai-assistant-about.md#writing-queries)。

   >[!NOTE]
   >
   >* 如果您未指定日期範圍，則代理程式會根據問題型別選取合理的預設值。 例如，如果您在詢問促銷活動量度時未指定日期範圍，則結果會針對促銷活動持續時間。
   >* 如果您有目標CPA，請將其納入查詢中（例如「針對目標$50診斷CPA」）。 如果您未指定目標，代理程式就會使用預設目標。

1. 按一下![送出查詢](/help/dsp/assets/submit-prompt.png "送出查詢")，或按鍵盤上的&#x200B;**Enter**&#x200B;鍵。

1. 如果AI助理要求其他資訊，請提供。

>[!TIP]
>
>若要詢問其他問題，或關於其他封裝或位置，[開始新的交談](#conversation-new)。

## 開始新交談 {#conversation-new}

每個交談（或查詢對話串）會分別儲存，以便您區分先前的交談。

1. 在[聊天箱](#ai-assistant-open)頂端按一下![開始新交談](/help/dsp/assets/new-selection.png "開始新交談")。

1. [提交查詢](#query-submit)。

## 展開並最小化聊天箱

1. 在[聊天箱](#ai-assistant-open)頂端按一下![進入全熒幕](/help/dsp/assets/fullscreen.png "進入全熒幕")以進入全熒幕模式。

1. 若要將聊天箱傳回面板模式，請按一下&#x200B;**[!UICONTROL < Back>]**。

>[!MORELIKETHIS]
>
>* [關於Advertising DSP中的AI小幫手](ai-assistant-about.md)
>* [使用先前的AI助理交談](previous-conversations.md)
