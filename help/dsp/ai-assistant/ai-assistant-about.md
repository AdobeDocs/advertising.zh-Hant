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
source-git-commit: fc59d590863f0014c5d0466019f1d7f787b23744
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%
---
# 關於Advertising DSP中的AI助理

DSP中的AI Assistant是對話式介面，可讓您從單一聊天方塊執行DSP中任何可用的代理式工作流程。 您可以建立新工作，或要求協助繼續先前的工作。

您的交談記錄會保留在所有工作流程中，每個交談都會自動命名。 您的查詢未與其他使用者共用。

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## 支援的工作流程

下列工作流程可協助您更有效地完成工作：

<!-- And links to all sections/pages -->

| 功能 | 說明 | 回應 |
| --- | --- | --- |
| [對象產生器代理程式](/help/dsp/ai-assistant/audience-builder-agent.md) | （Beta功能）產生可重複使用的受眾，其中可包含任何您可用的第一方和第三方區段，甚至包括其他儲存的受眾。 | 回應會先包含對象定義，然後是產生的對象區段，您可將其儲存為對象。 |
| [疑難排解](troubleshooting-agent.md) | （Beta功能）診斷即時套件和位置的效能和傳送問題。 | 回應包括限制效能的因素，並提供解決問題的逐步指示和建議。 |
| [深入分析](insights-agent.md) | （Beta功能）取得行銷活動量度和完整報表，無需手動建立報表。 您可以將結果下載為CSV檔案。 | 會顯示報告的前幾列，其中包含預覽完整報告以及以[!DNL Microsoft Excel]逗號分隔值檔案(.csv)下載報告的連結。 |
| [產品檔案搜尋](documentation-search.md) | 在[Advertising DSP指南](/help/dsp/home.md)中搜尋概念及作法內容，若為使用Advertising Creative的廣告商，則搜尋[Advertising Creative指南](/help/creative/home.md)。 | 回應包含內嵌引文和底部的可展開[!UICONTROL Documentation Sources]清單。 按一下任何引文或來源清單，開啟相關頁面。<br><br>回應可能也會包含後續問題與建議，以協助您調整查詢，並尋找更多資訊。 |

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
