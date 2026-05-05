---
title: 管理自訂目標
description: 瞭解如何定義成功事件，協助您達成套件層級的最佳化目標。
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# 管理自訂目標

*適用於連結至Search、Social和Commerce帳戶的DSP帳戶*

目標定義廣告商為實現其業務目標而設定的成功事件。 目標可作為[自訂目標](/help/dsp/campaign-management/packages/package-settings.md)用於DSP套件。 每個使用最佳化目標&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;的套件都必須包含自訂目標，以協助達成整體最佳化目標。

目標包含要追蹤和最佳化的量度（屬性），以及這些量度的相對權重。 每個目標可以包括：

* **[!UICONTROL Goal]個量度**，代表廣告商的主要成功量度。 通常會包含套件的核心業務結果，例如Revenue、Leads或Sales。 每個目標必須至少有一個目標量度。

* 選用的&#x200B;**[!UICONTROL Assist]量度**，可協助、預測、領先於或有助於推動目標量度。 範例包括參與量度，例如測試裝置和試用版。

  您可以讓[!DNL Adobe AI]自動指派並更新加權協助事件，以將您的目標事件最大化。 如果您偏好指派自己的加權協助量度，DSP可選擇根據Adobe Advertising和Adobe Analytics的過去效能資料來建議協助量度。 您可以選擇是否要套用建議。

目標選項的所有變更都會在欄位層級進行追蹤，並在變更記錄中列出。

>[!PREREQUISITES]
>
>在建立目標之前，您必須先將DSP帳戶連結至具有相同Adobe Experience Cloud組織ID的搜尋、社交和Commerce帳戶，即使您並非搜尋、社交和Commerce客戶。 如果您的DSP帳戶未連結至[!DNL Search, Social, & Commerce]帳戶，請連絡您的Adobe帳戶團隊。

>[!NOTE]
>
>* Advertising搜尋、社交和Commerce也使用目標。 每個搜尋、社交和Commerce產品組合都必須有目標，以便最佳化功能可以為該產品組合建立點按和收入模型。
>* 您可以在多個DSP套件和/或多個搜尋、社交和Commerce產品組合中使用相同的目標。

## 可用量度

您可以在目標中包含下列任一專案：

* Adobe Advertising使用[Adobe Advertising轉換追蹤畫素](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)追蹤的量度。

* （具有[!DNL Adobe Analytics for Advertising]的廣告商） [從Adobe Analytics](/help/integrations/analytics/overview.md)同步的轉換和網站參與量度。

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## 目標狀態

[!UICONTROL Settings] > [!UICONTROL Custom Objectives]檢視會指出每個目標的狀態。 值可包括：

* *[!UICONTROL Waiting]*：在產生建議之前，目標處於草稿狀態。

* *[!UICONTROL Active]*：目標已儲存且可使用。

## 建議狀態

* *[!UICONTROL Not Initiated]*：未要求任何建議。

* *[!UICONTROL Generating]*：正在產生建議。

* *[!UICONTROL Ready]*：建議可供套用。

* *[!UICONTROL Error]*：無法產生建議。

## 建立目標

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]**。

1. 輸入[目標設定](#custom-objective-settings)。

   當您選擇自動競標時，可以將屬性（量度）指派給目標做為&quot;[!UICONTROL Goal]&quot;量度。 對於自訂出價，您可以將屬性指派為&quot;[!UICONTROL Goal]&quot;或加權&quot;[!UICONTROL Assist]&quot;量度，但您必須至少包含一個目標量度。

   目標和協助標籤不會影響最佳化。 只有所包含量度的權重會影響最佳化。

1. （具有自訂競標的目標；選擇性）若要根據過去的效能資料產生建議的協助量度，請按一下底部區段中的&#x200B;**[!UICONTROL Generate]**。 在&#x200B;**[!UICONTROL Generate Recommendation]**&#x200B;中，按一下&#x200B;**[!UICONTROL Generate]**。

   建議量度的產生最多需要20分鐘。 產生建議時，自訂目標的狀態為&#x200B;*[!UICONTROL Waiting]*。 產生建議後，您可以「[檢視並套用建議的協助事件](#view-apply-recommendations)」。

1. （如果您沒有產生建議）在右上方，按一下&#x200B;**[!UICONTROL Save]**。

在使用最佳化目標&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot;或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;之套件的[DSP套件設定](/help/dsp/campaign-management/packages/package-settings.md)中，目標名稱現在包含在[!UICONTROL Custom Goals]清單中。 當您選取目標作為封裝的自訂目標時，[!UICONTROL Conversion Metric]清單會包含目標的所有目標量度。

## 編輯目標

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 在列中，按一下&#x200B;**...*** > **[!UICONTROL Edit]**。

1. 變更任何[目標設定](#custom-objective-settings)。

1. （建議可用時；選擇性）檢視並選擇性地套用建議的量度：

   1. 在底部，按一下&#x200B;**[!UICONTROL View Recommendations]**。

   1. 若要套用建議，請執行下列任一項作業：

      * 按一下建議旁的&#x200B;**[!UICONTROL Apply]**。

      * 手動調整建議，然後按一下建議旁的&#x200B;**[!UICONTROL Apply]**。

   1. 按一下&#x200B;**[!UICONTROL Close]**&#x200B;以關閉[!UICONTROL Recommendations]清單。

   變更會在目標設定同步後生效。

1. （具有自訂競標的目標；選擇性）若要根據過去的效能資料產生建議的協助量度，請按一下底部區段中的&#x200B;**[!UICONTROL Generate]**。 在&#x200B;**[!UICONTROL Generate Recommendation]**&#x200B;中，按一下&#x200B;**[!UICONTROL Generate]**。

   建議量度的產生最多需要20分鐘。 產生建議時，自訂目標的狀態為&#x200B;*[!UICONTROL Waiting]*。 產生建議後，您可以「[檢視並套用建議的協助事件](#view-apply-recommendations)」。

1. （如果您沒有產生新建議）在右上方，按一下&#x200B;**[!UICONTROL Save]**。

## 檢視並套用建議的協助事件 {#view-apply-recommendations}

*具有自訂競標的目標*

當目標狀態為&#x200B;*[!UICONTROL Active]*&#x200B;且[!UICONTROL Recommendation Status]為&#x200B;*[!UICONTROL Ready]*&#x200B;時，您可以檢視建議並選擇性地套用建議。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 在列中，按一下&#x200B;**...*** > **[!UICONTROL Edit]**。

1. 在底部，按一下&#x200B;**[!UICONTROL View Recommendations]**。

1. （選用）若要套用建議，請執行下列其中一項作業：

   * 按一下建議旁的&#x200B;**[!UICONTROL Apply]**。

   * 手動調整建議，然後按一下建議旁的&#x200B;**[!UICONTROL Apply]**。

1. 按一下&#x200B;**[!UICONTROL Close]**&#x200B;以關閉[!UICONTROL Recommendations]清單。

1. 按一下右上角的&#x200B;**[!UICONTROL Save]**。

   變更會在目標設定同步後生效。

## 檢視自訂目標的變更記錄

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 在列中，按一下&#x200B;**...*** > **[!UICONTROL Change Log]**。

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## 自訂目標設定 {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| 章節 | 引數 | 說明 |
|---------|-----------|-------------|
| 基本詳細資訊 | AMOClient | 廣告商的唯一Adobe Advertising ID。 |
| 基本詳細資訊 | 目標名稱 | 目標的名稱。<br><br>Advertising DSP的所有目標名稱都必須加上前置詞「ADSP_」（不區分大小寫），例如「ADSP_Registrations」。 當您想要將其指派給封裝時，請使用易於識別的名稱。 |
|  | 說明 | （選用）目標的說明。 當您將游標停留在「自訂目標」清單中的名稱上時，就會出現說明。 如果您不包含說明，則會重複目標名稱。 |
| 競標策略 |  | 目標的競標策略，其決定您可以設定的事件型別：<ul><li><b>[!UICONTROL Automated Bidding]：</b>將屬性（量度）指派給目標做為[!DNL goal]個量度。 [!DNL Adobe AI]會自動指派及更新加權協助事件，以使用平衡funnel方法最大化您的目標事件。</li><li><b>[!UICONTROL Custom Bidding]：</b>將屬性指派為&quot;[!DNL goal]&quot;或加權&quot;[!DNL assist]&quot;事件，以設定您自己的競標策略。 將此進階選項用於預先定義的策略。</li></ul>變更競標策略會清除所有先前選取的量度。 |
| 屬性 | [!UICONTROL Available Metrics] | 為廣告商追蹤的所有量度。 若要新增度量作為目標，請按一下度量名稱旁的<b>[!UICONTROL Goal]</b>。 （僅限[!UICONTROL Custom Bidding]）若要新增協助指派的目標量度的量度，請按一下量度名稱旁的<b>[!UICONTROL Assist]</b>。<br><br><b>注意：</b> [!DNL Analytics]個自訂事件遵循此命名慣例： `custom_event_[*event #*]_[*Analytics report suite ID*]`。 範例： `custom_event_16_examplersid.` [!DNL Analytics]維度和區段不適用於Adobe Advertising最佳化。<br><br><b>提示：</b>為獲得最佳效能，自訂目標（目標）中的組合量度每天至少要有10次轉換。 若未包含，最佳作法是將其他支援的轉換量度（例如產品頁面或應用程式啟動）新增至目標。 如需准則，請參閱[建立自訂目標的最佳實務](#custom-goal-best-practices)。 |
|  | 選取的量度 | 目標中包含的每個轉換量度的名稱。 執行下列任一項作業：<ul><li>若要新增度量作為目標，請在[!UICONTROL Available Metrics]欄中按一下度量名稱旁的<b>[!UICONTROL Goal]</b>。</li><li>（僅限[!UICONTROL Custom Bidding]策略）若要新增協助指派的目標量度的量度，請在[!UICONTROL Available Metrics]欄中按一下量度名稱旁的<b>[!UICONTROL Assist]</b>。 然後輸入相對於目標中其他量度的量度數字加權。 權重必須介於0.001到1之間，而且可以包含小數。 預設權重為1。</li><li>（僅限[!UICONTROL Custom Bidding]策略）若要編輯協助量度的權重，請在欄位內按一下，然後輸入相對於目標中其他量度的量度數字權重。 權重必須大於零(0)，並且可能包含小數。 預設權重為1。</li><li>若要從目標移除量度，請將游標停留在量度名稱上，然後按一下&#x200B;**[!UICONTROL X]**。/li></ul>**附註：**<ul><li>請確定不同的量度及其權重相對而言有意義。 例如，您無法直接比較計數與金額。</li><li>目標權重之間較大的相對變動可能會導致效能暫時波動，因此請在變更後監視效能。</li></ul>. |

>[!MORELIKETHIS]
>
>* [最佳化目標及使用方式](/help/dsp/optimization/optimization-goals.md)
>* 自訂目標的[最佳評分](/help/dsp/optimization/custom-goal.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [管理轉換](/help/dsp/admin/conversion-metrics-manage.md)
