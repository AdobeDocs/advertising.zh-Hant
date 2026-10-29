---
title: 管理[!DNL ChatGPT Ads]個對話式廣告帳戶
description: 瞭解如何建立和管理[!DNL ChatGPT Ads]聊天卡廣告的帳戶，這是測試版功能，可在AI助理對話中放置廣告。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%
---
# 管理[!DNL ChatGPT Ads]個對話式廣告帳戶

*Beta功能*

透過Adobe DSP與[!DNL OpenAI Ads]的整合，您可以執行[!DNL ChatGPT Ads]個聊天卡廣告，這些廣告會顯示在[!DNL ChatGPT]個交談中。 針對此功能，DSP會建立對話式廣告帳戶，並代表貴組織購買媒體。 您將無法從ads.openai.com存取廣告帳戶。 使用此功能來測試AI媒體，而不與[!DNL ChatGPT Ads]建立直接關係。

您將獨立於結構不同的一般DSP行銷活動來管理[!DNL ChatGPT Ads]對話式廣告帳戶，包括其行銷活動、廣告群組和廣告。 您還將與您的DSP行銷活動分開[檢視 [!DNL ChatGPT Ads] 行銷活動、廣告群組和廣告](campaign-manage.md#campaign-views-about)的績效資料。

## 適用性

下列專案決定此功能的適用性：

* **現有[!DNL Search, Social, & Commerce]客戶：**&#x200B;如果您的廣告商已使用[!DNL Search, Social, & Commerce]，請在「搜尋」、「社交」和「Commerce」[&#128279;](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)中建立及管理其 [!DNL ChatGPT Ads] 行銷活動，而非DSP。

* **受限產業：**&#x200B;受限類別（例如金融或醫療保健）中的廣告商無法建立對話式廣告帳戶或行銷活動。

如果選取的廣告商不合格，則[!UICONTROL Accounts]和[!UICONTROL Campaigns]標籤會指出原因。 您仍然可以使用廣告商選擇器切換到不同的廣告商。

若要使用此功能，請聯絡您的Adobe客戶團隊以開始入門流程。

## 帳單

您使用DSP帳戶的計費貨幣和計費時區（不論 [!DNL ChatGPT Ads] 帳戶[&#128279;](#account-settings)使用的貨幣和時區為何），在月底您的其他發票上已針對[!DNL ChatGPT Ads]使用情況計費。 如有計費問題，請聯絡您的Adobe客戶團隊。

## [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts]檢視 {#accounts-view}

[!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts]索引標籤列出所選廣告商的[!DNL OpenAI]帳戶。 每個帳戶的資訊包括：

**[!UICONTROL Status]：**&#x200B;帳戶目前是否正在提供廣告： *Active*&#x200B;或&#x200B;*已暫停*。 您無法變更帳戶的狀態；如果您想要暫停或重新啟用帳戶，請聯絡您的Adobe帳戶團隊。

**[!UICONTROL Review status]：** [!DNL OpenAI]檢閱狀態： *檢閱中*、*已核准*&#x200B;或&#x200B;*未核准*。 將游標停留在狀態上（如果有的話）。

**[!UICONTROL Active campaigns]：**&#x200B;帳戶中目前作用中的行銷活動數目。

**[!UICONTROL Cost]：**&#x200B;帳戶的總支出。

### 可用動作

* [檢視帳戶限制](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [建立帳戶](#account-create)

* [編輯帳戶](#account-edit)

* [重新整理帳戶清單](#account-refresh)

* [返回DSP主功能表](#return-to-menu)

## 管理帳戶

### 檢視帳戶限制 {#account-limits}

帳戶限制會限制帳戶在特定日期範圍內的總支出。 您可以檢視帳戶的限制，但只有您的Adobe帳戶團隊可以建立、編輯或移除限制。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Accounts]**&#x200B;檢視中，將游標停留在帳戶列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL View account limit]**。

[!UICONTROL Account limits]頁面列出帳戶的每個限制：

**[!UICONTROL Name]：**&#x200B;限制的名稱。

**[!UICONTROL Amount]：**&#x200B;限制期間的總支出上限。

**[!UICONTROL Period]：**&#x200B;套用限制的日期範圍。

**[!UICONTROL Status]：** *作用中*、*即將到來*&#x200B;或&#x200B;*已完成*。

**[!UICONTROL Spent]：**&#x200B;限制期間內目前所花費的金額。

>[!NOTE]
>
>您無法編輯或移除已完成的限制，且同一帳戶的限制期間不能重疊。

### 建立[!DNL ChatGPT Ads]對話式廣告帳戶 {#account-create}

若要為廣告商建立兩個以上的[!DNL ChatGPT Ads]帳戶，請聯絡您的Adobe帳戶團隊。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 執行下列任一項作業：

   * （僅限您的第一個帳戶）在歡迎畫面上，按一下&#x200B;**[!UICONTROL Create an Account]**。

   * 在&#x200B;**[!UICONTROL Accounts]**&#x200B;檢視中，選取廣告商，然後按一下&#x200B;**[!UICONTROL Create Account]**。

1. 指定[帳戶設定](#account-settings)。

1. 選取&#x200B;**[!UICONTROL I agree to the Terms and Conditions]**&#x200B;核取方塊。

1. 按一下&#x200B;**[!UICONTROL Create account]**。

在[!DNL OpenAI]稽核新帳戶時，這些帳戶會以暫停狀態建立。 帳戶一經核准，DSP就會啟用帳戶。

### 編輯[!DNL ChatGPT Ads]對話式廣告帳戶 {#account-edit}

建立帳戶後，您可以編輯帳戶的合法企業名稱和網站。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Accounts]**&#x200B;檢視中，將游標停留在帳戶列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit account]**。

1. 編輯&#x200B;**[!UICONTROL Legal Business Name]**&#x200B;和/或&#x200B;**[!UICONTROL Advertiser Website]**。 如需有關欄位的詳細資訊，請參閱&quot;[帳戶設定](#account-settings)&quot;。

1. 按一下&#x200B;**[!UICONTROL Save changes]**。

>[!IMPORTANT]
>
>儲存變更會重新啟動[!DNL OpenAI]的帳戶檢閱。 在帳戶重新核准之前，該帳戶將不再提供廣告。

### 重新整理帳戶清單 {#account-refresh}

當其他使用者進行變更或新增時，重新顯示帳號清單。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Accounts]**&#x200B;檢視中，按一下帳戶清單上方的&#x200B;**[!UICONTROL Refresh]**。

### 返回DSP主功能表 {#return-to-menu}

* 在主功能表上方，按一下&#x200B;**[!UICONTROL Back to DSP]**。

### [!DNL ChatGPT Ads]對話式廣告帳戶設定 {#account-settings}

**[!UICONTROL Legal Business Name]：**&#x200B;組織的註冊企業名稱。

**[!UICONTROL Advertiser Website]：**&#x200B;廣告商網站的URL，以`http://`或`https://`開頭。

**[!UICONTROL Country]：**&#x200B;組織合法註冊的國家/地區（不是您要執行廣告的國家/地區）。 此地點必須與組織DSP合約所用的國家/地區相同。 儲存帳戶後，就無法變更此值。

**[!UICONTROL Currency]：** （唯讀）您的Adobe帳戶團隊為[!DNL ChatGPT Ads]帳戶設定的貨幣。 這可能與您的DSP帳戶的貨幣不同，後者會顯示在DSP的其他位置。 **備註：**&#x200B;無論此值為何，所有使用帳單都將使用DSP帳戶所使用的&#x200B;*帳單貨幣*。

**[!UICONTROL Timezone]：** （唯讀）您的Adobe帳戶團隊為[!DNL ChatGPT Ads]帳戶設定的時區。 這可能與DSP帳戶使用的時區不同，後者會顯示在DSP的其他位置。 **注意：**&#x200B;無論此值為何，所有使用帳單都將代表用於DSP帳戶的&#x200B;*計費時區*。

**[!UICONTROL Favicon]：**&#x200B;要做為帳戶網站favicon的影像檔。<!-- How is this used within this context? --> 瀏覽器會在不同的位置顯示網站圖示，例如位址列、標籤或書籤。 檔案必須是JPG、PNG或WEBP格式，且至少為256x256畫素。

若要上傳圖示，請按一下&#x200B;**[!UICONTROL Upload favicon]**，然後在您的裝置或網路上尋找並選取檔案。

**[!UICONTROL I agree to the Terms and Conditions]：**&#x200B;表示您同意所有法律條款的核取方塊。 選取核取方塊以建立帳戶或更新帳戶設定。

>[!MORELIKETHIS]
>
>* [管理對話式廣告行銷活動](campaign-manage.md)
