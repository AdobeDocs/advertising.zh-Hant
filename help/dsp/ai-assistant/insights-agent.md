---
title: 使用AI助理建立報告
description: 瞭解如何使用Adobe Advertising DSP AI Assistant的見解代理程式來查詢行銷活動量度、產生報表及下載CSV檔案。
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
source-git-commit: ffe7424d4e225a95b279b06a7df3b85bf0cbcdbf
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%
---
# 使用AI助理建立報告

*Beta功能*

使用AI Assistant的見解代理程式來取得行銷活動、行銷活動元件、Advertising Creative體驗、廣告商和廣告目標的量度和完整報告，而不需手動建立報告。 您可以提出有關特定量度的簡單問題，例如行銷活動的支出或CPA，或針對特定維度（例如單一行銷活動或對象）或跨維度（針對每個行銷活動和廣告商的劃分）要求更複雜的報表。 您可以將結果下載為CSV檔案。

>[!IMPORTANT]
>
>AI產生的回應可能不準確或誤導。 一律先驗證回應和來源，再將其用於影響成本或投入的決策。

## 範例查詢

* [行銷活動名稱]上週花費了多少？

* [行銷活動名稱]本月收到多少轉換？

* 依封裝顯示[促銷活動名稱]的CPA。

* 哪些刊登版位的速度落後超過20%？

* 比較過去15天所有行銷活動和套件的淨支出。

## 提交查詢

您可以在一則訊息中詢問多個問題，但一次只能詢問一則訊息。 請等待回應，然後再傳送其他回應。

1. 按一下任何頁面右上角的![代理聊天](/help/dsp/assets/agent-chat.png "代理聊天")。

1. 建置查詢：

   1. 執行下列任一項作業：

      * 輸入您自己的查詢。

      * 若要檢視查詢範例：

        1. 按一下&#x200B;**[!UICONTROL Insights]**&#x200B;以展開區段。

        1. （選擇性）若要將範例查詢的文字複製到輸入欄位：

           1. 按一下範例。

           1. （選用）編輯文字以符合您的需求。

   1. （選擇性）若要將查詢焦點放在特定維度值（例如特定行銷活動），您可以選擇將游標插入您希望維度值出現的位置，按一下![提及實體](/help/dsp/assets/prompt-entity.png "提及實體")，選取維度，然後選取維度值。

      例如，針對維度[!UICONTROL Campaign]，您可以從所有要報告的行銷活動清單中選取。

      可用的維度包括：

      * 行銷活動實體： [!UICONTROL Campaign]、[!UICONTROL Package]、[!UICONTROL Placement]、[!UICONTROL Ad]
      * 廣告商： [!UICONTROL Advertiser]
      * Advertising Creative實體： [!UICONTROL Experience]
      * 廣告目標： [!UICONTROL Audience]、[!UICONTROL City]、[!UICONTROL Country]、[!UICONTROL State]、[!UICONTROL DMA]、[!UICONTROL Retargeting Pixel]、[!UICONTROL Device OS]、[!UICONTROL Device Browser]、[!UICONTROL Device Type]、[!UICONTROL Zip Code]

   如需有關查詢的詳細資訊，請參閱[撰寫查詢和提示的最佳實務](ai-assistant-about.md#writing-queries)。

1. 按一下![送出查詢](/help/dsp/assets/submit-prompt.png "送出查詢")，或按鍵盤上的&#x200B;**Enter**&#x200B;鍵。 如果代理程式要求其他資訊，請提供必要資訊。

   會顯示報表的前幾列，其中包含預覽完整報表和下載報表的連結。

   畫面會顯示所產生報表的幾列。

>[!TIP]
>
>若要詢問其他問題，或關於其他封裝或位置，[開始新的交談](#conversation-new)。

## 從聊天室下載或預覽完整報告

* 若要下載完整報告的復本，請按一下[匯出]。![](/help/dsp/assets/download.png "")

  根據瀏覽器的正常程式，檔案會下載為[!DNL Microsoft Excel]個逗號分隔值檔案(.csv)。 檔案名稱為「DSP_Insights_Report_&lt;job_number>」。

* 若要在側面板中預覽完整報告，請按一下![預覽](/help/dsp/assets/agent-chat-preview.png "預覽")。 若要從預覽下載報告，請按一下![匯出](/help/dsp/assets/download.png "匯出")。

  如果您下載報表，則會根據瀏覽器的正常程式，以[!DNL Microsoft Excel]逗號分隔值檔案(.csv)格式下載。 檔案名稱為「DSP_Insights_Report_&lt;job_number>」。

## 開始新交談 {#conversation-new}

每個交談或查詢對話串會分別儲存，以便您區分先前的交談。

1. 在[聊天箱](#ai-assistant-open)頂端按一下![開始新交談](/help/dsp/assets/new-selection.png "開始新交談")。

1. [提交查詢](#query-submit)。

## 展開並最小化聊天箱

1. 在[聊天箱](#ai-assistant-open)頂端按一下![進入全熒幕](/help/dsp/assets/fullscreen.png "進入全熒幕")以進入全熒幕模式。

1. 若要將聊天箱傳回面板模式，請按一下&#x200B;**[!UICONTROL < Back>]**。

>[!MORELIKETHIS]
>
>* [關於Advertising DSP中的AI小幫手](ai-assistant-about.md)
>* [使用先前的AI助理交談](previous-conversations.md)
