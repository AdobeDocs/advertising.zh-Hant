---
title: 管理廣告
description: 瞭解如何建立和管理廣告，包括可用的廣告型別。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 1732
ht-degree: 0%

---

# 管理廣告

*Beta功能*

僅&#x200B;*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]和現有[!DNL Baidu]帳戶*

廣告屬於廣告群組，包含向使用者顯示的內容，例如標題、說明、影像或其他創意元素，具體取決於廣告網路和廣告型別。

當您[透過API連線存取廣告網路帳戶](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，且Search、Social和Commerce已將帳戶資料與廣告網路同步之後，您就可以為[支援的行銷活動型別](/help/search-social-commerce/introduction/supported-inventory.md)建立廣告。 您也可以編輯及變更廣告的狀態。

如需每個廣告網路可用功能的詳細資訊，請參閱[支援的詳細目錄](/help/search-social-commerce/introduction/supported-inventory.md)。

## 關於[!UICONTROL Ads]檢視 {#ad-view-about}

[!UICONTROL Manage] > [!UICONTROL Ads]檢視表會列出所選廣告商帳戶之篩選檢視表中的所有廣告。

### 可用動作

* [建立廣告](#ad-create)

* [從列重新命名廣告](#ad-rename)

* [編輯廣告設定](#ad-edit)

* [變更廣告的狀態或刪除廣告](#ad-status)

* [從[!UICONTROL Ads]檢視管理資料檢視報告](#ad-reports)

## 可用的廣告型別 {#ad-types}

您可以在同步的廣告網路帳戶中建立和管理廣告群組的支援廣告型別：

* 在鎖定搜尋網路為目標的行銷活動中，針對廣告群組&#x200B;**文字廣告或展開文字廣告**。 文字廣告可包含選用的追蹤引數，這些引數可覆寫廣告群組或促銷活動層級引數。 根據廣告網路，您或許可以建立展開/延伸的文字廣告或標準文字廣告。

* 針對[!DNL Microsoft Audience Network]上[!DNL Microsoft Advertising]個行銷活動的跨裝置、原生&#x200B;**對象廣告**。 根據行銷活動設定，您有兩個對象廣告選項：

  * 如果促銷活動連結至商家中心商店，則讓廣告網路使用商店的產品資訊，自動為促銷活動產生摘要型廣告。 您不需要為行銷活動建立摘要型廣告，但您必須建立具有使用者定位的廣告群組。

  * 如果行銷活動未連結到商家中心帳戶，則使用回應式廣告格式建立影像型對象廣告，其中包含多個文字和影像資產。 廣告網路會使用最有效的廣告元素組合來組合廣告，並在[!DNL MSN]、[!DNL Outlook.com]和[!DNL Microsoft Edge]之類的網站上顯示廣告。

* 搜尋網路上有[!DNL Google Ads]個促銷活動的&#x200B;**僅限通話的廣告**。 僅限來電廣告是包含電話號碼的文字廣告。 您可以選擇使用[!DNL Google Ads]指派的轉接號碼進行進階通話報告。

  >[!NOTE]
  >
  >您目前無法建立或編輯僅限來電的廣告。 您可以檢視、變更狀態，或刪除現有的僅限通話廣告。

* **已針對搜尋促銷活動中的[!DNL Google Ads]和[!DNL Microsoft Advertising]動態搜尋廣告群組，展開動態搜尋廣告** （現在在廣告網路上僅稱為「動態搜尋廣告」）。 動態搜尋廣告會使用您網站的內容（而非關鍵字）來決定何時顯示您的廣告。 廣告網路會動態產生標題、選擇登陸頁面URL和顯示URL，並自動產生最終URL。

  如需動態搜尋廣告的詳細資訊，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/2471185)和[[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/ads/en/56794)。

* 針對[!DNL Microsoft Advertising]搜尋行銷活動的&#x200B;**多媒體廣告**。 多媒體廣告是以顯著的主線和側邊欄位置顯示的大型影像廣告，且每頁只顯示一個多媒體廣告。 它們可以包含多個文字和影像資產，例如回應式廣告，而廣告網路會使用最有效的廣告元素組合來組合廣告。 多媒體廣告不會取代文字廣告投放位置。

* 購物網路上&#x200B;**[!DNL Microsoft Advertising]個產品（購物）廣告**&#x200B;的促銷行。 購物廣告會使用您現有[!DNL Microsoft Merchant Center]產品摘要中的產品（而非關鍵字）來決定顯示廣告的方式和位置。 廣告文案與登入頁面URL會根據摘要中的產品資訊自動產生，但您可以選擇設定促銷明細行以納入廣告群組。

  如需產品廣告的詳細資訊，請參閱[Microsoft Advertising檔案](https://help.ads.microsoft.com/#apex/3/en/51082)。

* 搜尋網路上的[!DNL Google Ads]和[!DNL Microsoft Advertising]行銷活動的&#x200B;**回應式搜尋廣告**。 廣告網路會動態地從一組廣告標題和說明中組合文字型回應式搜尋廣告，以偏好同時表現優異的組合。 廣告最多包含三個標題、兩個說明，以及來自基本URL和選用的path1和path2欄位的可自訂URL。 您可以選擇將廣告標題和說明釘選至特定位置。

  >[!NOTE]
  >
  >[!DNL Google Ads]不會在其原生編輯器外提供有關顯示為廣告的文字組合的資料。 如需每個文字組合報表的詳細資訊，請參閱[Google Ads檔案](https://support.google.com/google-ads/answer/7684791)。

### 廣告層級的成效資料

廣告層級資料適用於大多數廣告型別。

但是，它無法用於[!DNL Google Ads]動態搜尋廣告(DSA)、最高效能、智慧購物和[!DNL YouTube]行銷活動。 行銷活動的廣告層級資料總計與行銷活動資料總計之間預期會不符。

| 廣告網路/行銷活動/廣告型別 | 資料可用性 |
|---|---|
| [!DNL Google Ads]動態搜尋廣告(DSA) | 行銷活動、廣告群組 |
| [!DNL Google Ads]最高效能 | Campaign |
| [!DNL Google Ads]購物，智慧型購物 | 行銷活動、廣告群組 |
| [!DNL Google Ads] [!DNL YouTube] | 行銷活動、廣告群組 |

## 建立廣告 {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* 您不需要針對購物行銷活動建立產品廣告；廣告網路會自動建立這些廣告。 不過，對於[!DNL Microsoft Advertising]個購物行銷活動，您可以選擇定義促銷行以包含在廣告中。
>* 您無法建立[!DNL Google Ads]只限通話的廣告。

>[!TIP]
>
>若要同時建立大量廣告，請使用[行銷活動大量表單](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 按一下&#x200B;**[!UICONTROL Create Ads]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步驟中，選取網路、帳戶、行銷活動、廣告群組和廣告型別。

   如需可用廣告型別的詳細資訊，請參閱[可用的廣告型別](#ad-types)。

1. 指定[Baidu文字廣告](ad-settings-baidu-text.md)、[Google Ads擴充動態搜尋廣告](ad-settings-google-dsa.md) （在Google Ads中稱為「動態搜尋廣告」）、[Google Ads回應式搜尋廣告](ad-settings-google-rsa.md)、[Microsoft Advertising擴充動態搜尋廣告](ad-settings-microsoft-dsa.md)、[Microsoft Advertising多媒體廣告](ad-settings-microsoft-multimedia.md)、[Microsoft Advertising產品廣告](ad-settings-microsoft-product.md)、[Microsoft回應式廣告](ad-settings-microsoft-responsive.md)、[Advertising回應式搜尋廣告](ad-settings-microsoft-rsa.md)或[Yandex文字廣告](ad-settings-yandex-text.md)設定的其餘設定。

   >[!NOTE]
   >
   >（具有Adobe Advertising轉換追蹤的行銷活動）如果帳戶或行銷活動設定僅在關鍵字層級指定追蹤，則Search、Social和Commerce不會產生廣告的追蹤。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯]。![](/help/search-social-commerce/assets/edit-new.png "[編輯]。")**[!UICONTROL Edit]**，然後變更廣告設定。

1. 按一下&#x200B;**[!UICONTROL Create]**。

1. &#x200B;<!-- Add link to where to generate this once available to users-->（促銷活動中的購物廣告具有Adobe Advertising轉換追蹤；選用）若要追蹤廣告上的點按，請手動將追蹤URL新增至帳戶、促銷活動或產品群組設定。

## 重新命名廣告 {#ad-rename}

快速重新命名廣告，而不開啟完整的廣告設定。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 將游標停留在廣告列上並按一下&#x200B;**[!UICONTROL ...]>[!UICONTROL Rename]**。

1. 編輯名稱，然後按一下&#x200B;**[!UICONTROL Apply]**。

## 編輯廣告設定 {#ad-edit}

>[!NOTE]
>
>* 下列廣告型別為&#x200B;*可變*，這表示您可以變更廣告文案或影像並保留相同的廣告ID：除了動態搜尋廣告以外的所有[!DNL Google Ads]廣告型別，以及[!DNL Microsoft Advertising]擴充文字廣告。
>* 所有其他支援的廣告為&#x200B;*不可變動*，這表示變更廣告復本或影像將會刪除現有廣告並建立新的廣告。 搜尋、Social和Commerce收集足夠的資料以進行最佳化時，新廣告的效能在幾週內可能會不穩定。
>* 您無法編輯產品廣告的內容，但[!DNL Microsoft Advertising]產品廣告的促銷活動行除外。 不過，您可以暫停或刪除廣告。
>* 您無法編輯[!DNL Google Ads]僅限通話的廣告。 不過，您可以暫停或刪除其中一個專案。
>* 您一次只能編輯一個廣告。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 選取廣告旁的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Ad Details]**&#x200B;步驟中，編輯[百度文字廣告](ad-settings-baidu-text.md)、[Google廣告擴充動態搜尋廣告](ad-settings-google-dsa.md) （現在在Google廣告中稱為「動態搜尋廣告」）、[Google廣告回應式搜尋廣告](ad-settings-google-rsa.md)、[Microsoft Advertising擴充動態搜尋廣告](ad-settings-microsoft-dsa.md)、[Microsoft Advertising多媒體廣告](ad-settings-microsoft-multimedia.md)、[Microsoft Advertising產品廣告](ad-settings-microsoft-product.md)、[Microsoft回應式廣告](ad-settings-microsoft-responsive.md)、[Advertising回應式搜尋廣告](ad-settings-microsoft-rsa.md)或[Yandex文字廣告](ad-settings-yandex-text.md)設定。

1. 按一下&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，請按一下[編輯]。![](/help/search-social-commerce/assets/edit-new.png "[編輯]。")**[!UICONTROL Edit]**，然後變更廣告設定。

1. 按一下&#x200B;**[!UICONTROL Update]**。

## 變更廣告狀態 {#ad-status}

快速變更廣告狀態，無需開啟完整的廣告設定。

您可以暫停支援廣告網路上的任何作用中廣告，以停用其競標。 您稍後可以透過將狀態變回作用中來繼續競標。

您也可以刪除任何作用中或暫停的廣告。 刪除的廣告會從廣告網路中刪除。 當您將其納入資料篩選器時，仍可顯示這些值，但您無法加以變更。

### 啟動或暫停廣告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 選取廣告列的核取方塊。

1. 在大量動作工具列中，變更狀態：

   * 若要啟用暫停的廣告，請按一下&#x200B;**[!UICONTROL Activate]**。

   * 若要暫停作用中的廣告，請按一下&#x200B;**[!UICONTROL Pause]**。

### 刪除廣告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 選取廣告列的核取方塊。

1. 在大量動作工具列中按一下&#x200B;**[!UICONTROL Delete]**。

1. 在確認訊息中，按一下&#x200B;**[!UICONTROL Confirm]**。

## 從[!UICONTROL Ads]檢視管理資料檢視報告 {#ad-reports}

產生一份報表，其中包含[!UICONTROL Ads]檢視中一或多個廣告的資料列，然後以Microsoft Excel工作表檔案（XLXS格式）格式下載報表。 報表會包含檢視中的所有可見欄。

您可以刪除任何產生的報表。

另請參閱&quot;[（舊版UI）從行銷活動管理檢視](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)下載資料&quot;和&quot;[（舊版UI）從[!UICONTROL Downloads]功能表](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)刪除效能資料報表或Bulksheet檔案&quot;。

### 產生含有已篩選資料列的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 指定要下載其資料的廣告：

   * 若要下載特定廣告的資料，請選取廣告旁邊的核取方塊。

   * 若要下載所有廣告的資料，您不需要選取任何核取方塊。 預設會包含所有廣告。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]設定中，輸入唯一的報告名稱，然後按一下&#x200B;**[!UICONTROL Generate]**。

   依預設，檔案名稱為「ad_YYYYYMMDD_NNNN」，其中「NNNN」為循序工作編號（例如「ad_20250402_1326）。

   檔案已新增至[!UICONTROL Recently Generated]清單。

1. （選擇性）若要在檔案完成後下載檔案，請按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 下載完成的報表

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![下載](/help/search-social-commerce/assets/download.png "下載")。

   檔案會依照瀏覽器的正常程式下載。

### 刪除已完成的報告

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 在資料表上方的工具列中，按一下![下載報表](/help/search-social-commerce/assets/download.png "下載報表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]對話方塊的[!UICONTROL Recently Generated]清單中，按一下檔案名稱旁的![刪除](/help/search-social-commerce/assets/delete-new.png "刪除")。

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] 文字廣告設定](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] 延展的動態搜尋廣告設定](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] 回應式搜尋廣告設定](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] 延展的動態搜尋廣告設定](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] 多媒體廣告設定](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] 產品廣告設定](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] 回應式（對象）廣告設定](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] 回應式搜尋廣告設定](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] 文字廣告設定](ad-settings-yandex-text.md)
