---
title: 關於使用庫存摘要自動化廣告管理
description: 瞭解進階行銷活動管理，其可讓您根據產品或服務詳細目錄的相關資料，自動管理帳戶結構並提供動態廣告。
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# 關於使用庫存摘要自動化廣告管理

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

進階行銷活動管理的[!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]檢視可讓您根據產品或服務詳細目錄的相關資料，自動建立和更新廣告網路帳戶結構，並提供動態廣告。 您可以每天或視需要隨時上傳含有產品資料的新檔案，或直接連結至[!DNL Google]或[!DNL Microsoft]商家中心帳戶。 使用功能可以：

* 從訂購的資料來源建立新的行銷活動。

* 使用可變更資料元素（例如價格或數量）的動態變數，在處理新資料時動態更新文字和回應式搜尋廣告、[!DNL Google Ads]個購物廣告或[!DNL Microsoft Advertising]個購物廣告。 每次您變更資料時，就會刪除現有的廣告並建立新的廣告。

* 當庫存跌至特定層級以下時、根據指定的結束日期時，或當摘要資料中省略現有元件時，自動暫停或移除廣告群組、關鍵字和廣告。

若要設定廣告，請建立包含變數（預留位置）的詳細目錄摘要範本，然後以已同步的上傳檔案或[Google或Microsoft商家中心帳戶中的實際資料欄取代變數](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)。 變數亦可包含您在檔案中設定的修飾元群組，或檔案中的個別列，以為資料檔案中的每個適用列建立多個廣告、關鍵字、促銷活動或廣告群組。 例如，如果您在廣告標題中使用修飾詞群組變數，且修飾詞群組包含兩個修飾詞（「廉價」和「折扣」），則會為每個產品建立兩個個別的廣告 — 每個修飾詞各一個。 對於[!DNL Google Ads]和[!DNL Microsoft Advertising]動態搜尋廣告，您也可以包含廣告自訂者的值。

| 範本的[!UICONTROL Ad Variation]區段 | 搜尋、社交和Commerce中的修飾元 | 摘要內容 | 產生的廣告 |
|----|----|----|----|
| 標題：購買高階\{<i>產品類別</i>\} &lt;<i>便宜清單</i>>。<br><br>說明1： \{<i>產品名稱</i>\}庫存量龐大。<br><br>說明2：折扣百分比為\{<i>\</i>\}%。 | 修飾元群組&quot;CoeableList&quot;的值：<br><br>&quot;for coeable&quot;<br><br>&quot;at discount&quot; | 產品類別、產品名稱、折扣百分比<br>電子產品、iPod、10<br><br>服飾、襯衫、15<br><br><b>注意：</b>您可以使用逗號或索引標籤來分隔值。 | <u>以低廉價格購買高階電子產品。</u><br>大量平板電腦庫存。 可享受10%的折扣。<br><br><u>以折扣價購買高階電子產品。</u><br>大量平板電腦庫存。 可享受10%的折扣。<br><br><u>廉價購買高檔服裝。</u><br>大量的T恤。 可享受15%的折扣。<br><br><u>購買高檔服裝可享有折扣。</u><br>大量的T恤。 可享受15%的折扣。 |

廣告產生後，您可以選擇檢閱廣告，然後張貼至廣告網路。

>[!NOTE]
>若要使用試算表檔案大量建立或編輯行銷活動資料，請參閱[關於使用大量工作表管理行銷活動資料](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

## 使用詳細目錄摘要管理行銷活動資料的工作流程

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （僅刪除動作）和僅[!DNL Yandex]帳戶*

起初，請至少測試一個摘要檔案或帳戶，然後您可以完全自動化此程式，或繼續在每個步驟控制此程式：

1. （選用）請聯絡您的Adobe客戶團隊，以設定FTP目錄來儲存資料檔案。

   如果您使用FTP目錄，則摘要服務會每兩小時檢查一次新檔案。

   否則，您可以在[!UICONTROL Advanced (ACM)]檢視中手動上傳檔案。

1. 設定[引數以處理摘要資料](feed-settings-manage.md#feed-data-settings)。

   如果您使用FTP，一開始請勿自動將資料張貼至廣告網路。 驗證第一個檔案的輸出並對結果滿意後，您可以變更設定。

1. 將資料檔案上傳至FTP目錄、[在[!UICONTROL Advanced (ACM) view]中手動上傳資料檔案](feed-files-manage.md)，或[啟用Google或Microsoft商家中心帳戶的存取權](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)。

若要手動上傳檔案，您可以等到您建立使用資料檔案的範本為止。

1. （選擇性）建立[修飾元](modifiers-manage.md)的群組，以便在摘要資料範本的各種資料欄位中作為變數使用。

1. [建立一個或多個範本](ad-templates/ad-template-manage.md)，這些範本使用資料欄來建立特定廣告網路帳戶的行銷活動、廣告群組、關鍵字和/或廣告復本。

1. [透過範本傳播摘要資料](feed-data-propagate.md)，範本中的資料行名稱會以檔案或帳戶中的資料取代。 根據範本選項，搜尋、Social和Commerce會使用預設設定為廣告建立新的帳戶結構（促銷活動、廣告群組、關鍵字），或將廣告對應至現有的帳戶結構。

1. （選擇性） [在[!UICONTROL Advanced (ACM)]檢視中預覽輸出](propagated-data-view.md)，並選擇性地檢視[!UICONTROL Propagations]標籤上的資料變更摘要。

1. [將資料](propagated-data-post.md)張貼到相關的廣告網路帳戶。

1. （如果您使用FTP或商家中心帳戶上傳資料；選擇性）驗證第一個摘要檔案的輸出後，請[編輯引數](feed-settings-manage.md#feed-data-settings)以透過相關範本自動傳播後續資料，並將其張貼至相關廣告網路。

1. （當您有新資料檔案時）視需要上傳新檔案、透過範本傳播資料，並將資料發佈到相關廣告網路。 您可以選擇在一個步驟中傳播和發佈資料。

>[!MORELIKETHIS]
>
>* [清查摘要何時建立或刪除帳戶元件？](when-are-components-created-deleted.md)
