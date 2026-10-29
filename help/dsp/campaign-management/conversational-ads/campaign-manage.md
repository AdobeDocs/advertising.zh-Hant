---
title: 管理[!DNL ChatGPT Ads]個對話式廣告行銷活動
description: 瞭解如何建立和管理[!DNL ChatGPT Ads]行銷活動、廣告群組和聊天卡廣告，這是一項Beta版功能，可在AI助理對話中放置廣告。
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
source-wordcount: '1188'
ht-degree: 0%
---
# 管理[!DNL ChatGPT Ads]對話式廣告行銷活動、廣告群組和廣告

*Beta功能*

在[對話式廣告帳戶](account-manage.md)中管理[!DNL ChatGPT Ads]行銷活動、廣告群組和聊天卡廣告。

當月月底您的其他發票中有[!DNL ChatGPT Ads]個使用量需要付費。 如有計費問題，請聯絡您的Adobe客戶團隊。

## [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns]檢視 {#campaign-views-about}

[!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns]檢視包含三個索引標籤： [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]和[!UICONTROL Ads]。 每個索引標籤都會列出所選帳戶的促銷活動、廣告群組或廣告，以及所選日期範圍的績效資料。 行銷活動、廣告群組和廣告層級的效能資料包含[!UICONTROL Impressions]、[!UICONTROL Clicks]、[!UICONTROL Spend]、[!UICONTROL CTR]、[!UICONTROL Avg CPC]和[!UICONTROL Avg CPM]。

>[!NOTE]
>
>* 設定為檢視申報檢視中稅捐值的組織在[!DNL ChatGPT Ads]中看不到它們。 手動計算稅捐值。

### 可用動作

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* [建立](#campaign-create)或[編輯](#campaign-edit)行銷活動

* [建立](#ad-group-create)或[編輯](#ad-group-edit)現有行銷活動的廣告群組

* [建立](#ad-create)或[編輯](#ad-edit)現有廣告群組的廣告

* [啟動或暫停行銷活動、廣告群組或廣告](#pause-activate)

* [封存行銷活動、廣告群組或廣告](#archive)

* [從行銷活動向下展開至廣告群組和廣告](#drill-down)

* [重新整理行銷活動、廣告群組或廣告清單](#refresh)

## 行銷活動

### 建立[!DNL ChatGPT Ads]對話式廣告行銷活動 {#campaign-create}

建立行銷活動時，您可以選擇建立其第一個廣告群組和廣告。 每個步驟會在您按一下&#x200B;**[!UICONTROL Next]**&#x200B;後立即建立該實體，因此您無法返回上一個步驟 — 如果您之後需要變更某些專案，請在精靈關閉後加以編輯。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在子功能表中，按一下「**[!UICONTROL Campaigns]**」標籤。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]>[!UICONTROL Campaign]**。

1. 指定[行銷活動設定](#campaign-settings)。

1. 按一下&#x200B;**[!UICONTROL Next]**&#x200B;以儲存行銷活動設定。

1. 執行下列任一項作業：

   * 如果您不想要建立行銷活動的廣告群組，請按一下&#x200B;**[!UICONTROL Close]**。

     >[!TIP]
     >
     >若要稍後建立廣告群組或廣告，請參閱&quot;[建立廣告群組](#ad-group-create)&quot;或&quot;[建立廣告](#ad-create)&quot;。

   * （選用）建立廣告群組：

     1. 指定[廣告群組設定](#ad-group-settings)。

     1. 按一下&#x200B;**[!UICONTROL Next]**&#x200B;儲存廣告群組設定。

     1. （選擇性）如果您不想為行銷活動建立廣告，請按一下&#x200B;**[!UICONTROL Close]**。

   * （建立廣告群組後為選用）建立廣告：

     1. 指定[廣告設定](#ad-settings)。

     1. 按一下&#x200B;**[!UICONTROL Create ad]**。

### 編輯[!DNL ChatGPT Ads]對話式廣告行銷活動設定 {#campaign-edit}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左側的子功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. （如有必要）在資料表上方，按一下&#x200B;**[!UICONTROL Campaigns]**&#x200B;標籤。

1. 將游標停留在資料列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

1. 編輯任何[行銷活動設定](#campaign-settings)、[廣告群組設定](#ad-group-settings)和[廣告設定](#ad-settings)。

1. 按一下&#x200B;**[!UICONTROL Save]**。

### [!DNL ChatGPT Ads]對話式廣告行銷活動設定 {#campaign-settings}

**[!UICONTROL Campaign name]：**&#x200B;促銷活動的唯一名稱。 名稱必須至少包含三個字元。

**[!UICONTROL Campaign type]：** （唯讀） *Standard*&#x200B;是唯一可用的型別。

**[!UICONTROL Objective]：**&#x200B;促銷活動要聚焦的量度： *觸及*&#x200B;或&#x200B;*點按*。 目標會決定行銷活動廣告群組的競標型別。

**[!UICONTROL Locations]：** （選擇性）要鎖定的一或多個特定位置。 若要鎖定所有位置，請將此設定留空。 若要指定特定位置，請輸入至少兩個出現在名稱中的任何位置的字母，然後按一下搜尋結果中的名稱。

**[!UICONTROL Budget type]：** *每日預算*&#x200B;或&#x200B;*期限預算*。

**[!UICONTROL Budget]：**&#x200B;指定預算型別的預算。 值必須大於零(0)。

**[!UICONTROL Start date]：**&#x200B;行銷活動開始的日期（以帳戶的時區表示）。

**[!UICONTROL Set an end date]：** （選用）可讓您指定行銷活動的結束日期。 選取此選項時，請指定&#x200B;**[!UICONTROL End date]**。

## 廣告群組

### 為現有的行銷活動建立[!DNL ChatGPT Ads]廣告群組 {#ad-group-create}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在子功能表中，按一下「**[!UICONTROL Campaigns]**」標籤。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]>[!UICONTROL Ad Group]**。

1. 指定[廣告群組設定](#ad-group-settings)，包括父促銷活動。

1. 按一下&#x200B;**[!UICONTROL Create ad group]**。

## 編輯[!DNL ChatGPT Ads]廣告群組 {#ad-group-edit}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左側的子功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Ad Groups]**&#x200B;標籤。

1. 將游標停留在資料列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

1. 編輯[廣告群組](#ad-group-settings)設定。

1. 按一下&#x200B;**[!UICONTROL Save]**。

### [!DNL ChatGPT Ads]廣告群組設定 {#ad-group-settings}

**[!UICONTROL Parent campaign]：** （僅現有行銷活動的廣告群組）廣告群組所屬的行銷活動。

**[!UICONTROL Ad group name]：**&#x200B;廣告群組的唯一名稱。 名稱必須至少包含三個字元。

**[!UICONTROL Maximum CPC bid]**&#x200B;或&#x200B;**[!UICONTROL Maximum CPM bid]：**&#x200B;每次點按或1,000次曝光所支付的金額上限。 值必須大於零(0)。 行銷活動的目標會決定競標欄位： *點按次數*&#x200B;個行銷活動顯示&#x200B;**[!UICONTROL Maximum CPC bid]**，以及&#x200B;*觸及範圍*&#x200B;個行銷活動顯示&#x200B;**[!UICONTROL Maximum CPM bid]**。

>[!TIP]
>
>較高的出價可能會贏得更多拍賣。

**[!UICONTROL Context hints]：** （選擇性）與您產品或服務相關的交談、主題或關鍵字的說明。 這些提示會指導比對，但並非完全符合目標規則。

## 廣告

### 為現有的廣告群組建立[!DNL ChatGPT Ads]聊天卡廣告 {#ad-create}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在子功能表中，按一下「**[!UICONTROL Campaigns]**」標籤。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. 按一下右上角的&#x200B;**[!UICONTROL Create]>[!UICONTROL Ad]**。

1. 指定[廣告設定](#ad-settings)，包括父行銷活動和廣告群組。

1. 按一下&#x200B;**[!UICONTROL Create ad]**。

## 編輯[!DNL ChatGPT Ads]聊天卡廣告 {#ad-edit}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左側的子功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Ads]**&#x200B;標籤。

1. 將游標停留在資料列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

1. 編輯[ad](#ad-settings)設定。

1. 按一下&#x200B;**[!UICONTROL Save]**。

### [!DNL ChatGPT Ads]聊天卡廣告設定 {#ad-settings}

**[!UICONTROL Parent campaign]**&#x200B;和&#x200B;**[!UICONTROL Parent ad group]：** （僅現有廣告群組中的廣告）廣告所屬的行銷活動和廣告群組。

**[!UICONTROL Ad name]：**&#x200B;廣告的唯一名稱。 名稱必須至少包含三個字元。

**[!UICONTROL Ad URL (Link)]：**&#x200B;登陸頁面URL，從`http://`或`https://`開始。

**[!UICONTROL Title (headline)]：**&#x200B;廣告標題。 標題必須介於3到50個字元之間。 **注意：**&#x200B;某些位置型別的標題可能會被截斷。

**[!UICONTROL Description]：**&#x200B;廣告內文。 說明必須介於3到100個字元之間。

**[!UICONTROL Ad image]：**&#x200B;要包含在廣告中的JPG或PNG影像。 若要上傳影像，請按一下（新廣告） **[!UICONTROL Upload image (PNG/JPG)]**&#x200B;或&#x200B;**[!UICONTROL Change image]**，然後在您的裝置或網路上尋找並選取檔案。

**[!UICONTROL Preview]：**&#x200B;根據廣告設定的廣告預覽。

## 啟動或暫停[!DNL ChatGPT Ads]行銷活動、廣告群組或廣告 {#pause-activate}

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左側的子功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. 在&#x200B;**[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;索引標籤上，尋找列。

1. 在&#x200B;**[!UICONTROL Active]**&#x200B;欄中，執行下列任一項作業：

   * 若要啟動暫停的專案，請開啟切換按鈕（向右）。

   * 若要暫停作用中專案，請關閉切換按鈕（向左）。

## 封存[!DNL ChatGPT Ads]行銷活動、廣告群組或廣告 {#archive}

封存會從[!UICONTROL Conversational Ads]檢視中永久移除行銷活動、廣告群組或廣告。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左側的子功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，選取廣告商和[!DNL ChatGPT Ads]帳戶。

1. 在&#x200B;**[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;索引標籤上，將游標停留在資料列上，然後按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Archive]**。

## 從[!DNL ChatGPT Ads]個行銷活動向下展開至廣告群組和廣告 {#drill-down}

* 按一下行銷活動列，僅在&#x200B;**[!UICONTROL Ad Groups]**&#x200B;索引標籤上檢視其廣告群組，或按一下廣告群組列，僅在&#x200B;**[!UICONTROL Ads]**&#x200B;索引標籤上檢視其廣告。

若要移除篩選器並檢視檢視中的所有列，請按一下資料表格上方篩選器中的&#x200B;**X**。

## 重新整理行銷活動、廣告群組或廣告清單 {#refresh}

若其他使用者已進行變更或新增，則重新顯示促銷活動、廣告群組或廣告清單。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;檢視中，按一下資料表上方的&#x200B;**[!UICONTROL Refresh]**。

>[!MORELIKETHIS]
>
>* [管理對話式廣告帳戶](account-manage.md)
