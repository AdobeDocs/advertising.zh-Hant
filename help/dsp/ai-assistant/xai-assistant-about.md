---
title: 關於Advertising DSP中的AI助理
description: 瞭解如何使用DSP AI助理來疑難排解套件和位置、報告和搜尋產品使用說明。
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
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%
---
# 關於Advertising DSP中的AI助理

DSP中的AI Assistant是對話式介面，可讓您從單一聊天方塊執行DSP中任何可用的代理式工作流程。 您可以建立新工作，或要求協助繼續先前的工作。

您的交談記錄會保留在所有工作流程中，每個交談都會自動命名。 您的查詢未與其他使用者共用。

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## 支援的工作流程

下列工作流程可協助您更有效地完成工作：

<!-- And links to all sections/pages -->

| 功能 | 說明 | 範例查詢 | 回應 |
| --- | --- | --- | --- |
| [疑難排解](troubleshooting-agent.md) | 診斷所選即時套件或位置的效能和傳送問題。<ul><li>僅限刊登：診斷超支、花費過少和無法花費。 代理程式會評估相關的步調、投標、目標定位和預算上限因素。</li><li>僅限套件：診斷效能問題，包括CPA上升或ROAS下降。 代理程式不會診斷參與量度，例如CTR、CPC、點按或曝光數。</li></ul>每個交談會針對一個套件或位置說明一項診斷。 收到結果後，開始新的對話以診斷另一個問題、封裝或位置。<br><br>代理程式無法變更設定、建立或編輯行銷活動或行銷活動元件。 它也無法診斷暫停、完成、封存或排程的封裝或位置。 | 刊登版位支出問題：<ul><li>我的刊登版位昨天停止花費，即使交易進行中。 為什麼？</li><li>為什麼這個位置在過去5天支出不足？</li><li>我們飛行已經過半，步調明顯落後。 為什麼？</li></ul>套件效能問題：<ul><li>為什麼這個封裝的CPA在上星期有所增加？</li><li>為何ROAS拒絕此套件？</li></ul> | 回應包括限制效能的因素，並提供解決問題的建議。 |
| [深入分析](insights-agent.md) | 取得行銷活動量度和完整報告，而不需手動建立報告。 您可以提出有關特定量度的簡單問題，例如行銷活動的支出或CPA，或要求特定維度（例如單一行銷活動、位置或對象）或跨維度（依行銷活動和廣告商的劃分）的更複雜報表。 您可以將結果下載為CSV檔案。 | <ul><li>[行銷活動名稱]上週花費了多少？<li>[行銷活動名稱]本月收到多少轉換？</li><li>哪些刊登版位的速度落後超過20%？</li></li>依封裝顯示[促銷活動名稱]的CPA</li></ul> | 會顯示報告的前幾列，其中包含預覽完整報告以及以[!DNL Microsoft Excel]逗號分隔值檔案(.csv)下載報告的連結。 |
| [產品檔案搜尋](documentation-search.md) | 在[Advertising DSP指南](/help/dsp/home.md)中搜尋概念及作法內容，若為使用Advertising Creative的廣告商，則搜尋[Advertising Creative指南](/help/creative/home.md)。 答案僅以[Experience League](https://experienceleague.adobe.com/zh-hant/docs/advertising)中針對這些產品所記錄的資料為依據。<br><br>詢問有關行銷活動管理、最佳化、對象管理、交易、報告及其他產品功能的問題。 | <ul><li>如何將廣告附加至投放位置？</li><li>Adobe DSP中有哪些鎖定目標選項？</li><li>在刊登版位設定中使用不同步調選項有何後果？</li><li>哪些報表包含住戶層級資料？</li><li>如何為[!DNL Creative]體驗建立廣告標籤？</li></ul> | 回應包含內嵌引文和底部的可展開[!UICONTROL Documentation Sources]清單。 按一下任何引文或來源清單，開啟相關頁面。<br><br>回應可能也會包含後續問題與建議，以協助您調整查詢，並尋找更多資訊。 |

## 開啟AI助理 {#ai-assistant-open}

* 按一下任何頁面右上角的![代理聊天](/help/dsp/assets/agent-chat.png "代理聊天")。

## 展開對話方塊

1. 在[聊天箱](#ai-assistant-open)頂端按一下![進入全熒幕](/help/dsp/assets/fullscreen.png "進入全熒幕")以進入全熒幕模式。

1. 若要將聊天箱傳回面板模式，請按一下&#x200B;**[!UICONTROL < Back>]**。

<!-- 

No ability to narrow down list of child entities for a selected parent as of 10/26/26.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. Build the query:

   * To see examples of queries by topic and optionally copy one to use:
   
     1. Click **[!UICONTROL Learn]**, **[!UICONTROL Troubleshoot]**, or **[!UICONTROL Insights]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   * To enter your own query:
   
     1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
     
        For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
        
        Available dimensions include:
        
        * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
        * The advertiser: [!UICONTROL Advertiser]
        * Advertising Creative entities: [!UICONTROL Experience]
        * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

     1. Enter your query, and then click ![Submit query](/help/dsp/assets/submit.png "Submit query") or press the **Enter** key on your keyboard.
        
   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

 -->

<!--

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

-->

## 編寫查詢和提示的最佳實務 {#writing-queries}

* **清楚明確**。 使用完整問題（「如何訂閱隨選詳細目錄？」）、任務片語（「訂閱隨選詳細目錄」）或主題片語（「隨選詳細目錄」）。

* **請勿在同一查詢**&#x200B;中合併不同型別的請求，除非您希望它們儲存在相同的交談中。

* **相關時包含日期範圍**&#x200B;以縮小您想要的資料範圍。

* 儘可能與產品功能（例如「行銷活動」或「交易」）的UI辭彙&#x200B;**相符**。

  對於常見動作（例如「新增」、「附加」或「指派」），您可以使用同義字。

* **新增詳細資料**&#x200B;以縮小或擴大結果。 視需要完善後續問題。

* **不必擔心標點符號與大寫**，除非它們會影響意義。

>[!MORELIKETHIS]
>
>* [使用AI助理建立報告](insights-agent.md)
>* [使用AI助理疑難排解效能和傳遞問題](troubleshooting-agent.md)
>* [建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)
>* [使用AI助理搜尋產品檔案](documentation-search.md)
>* [使用先前的AI助理交談](previous-conversations.md)
