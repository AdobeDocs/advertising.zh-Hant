---
title: 管理廣告
description: 瞭解搜尋、社交和Commerce中的廣告，包括可用的廣告型別。
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# 關於廣告

僅&#x200B;*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和現有[!DNL Baidu]帳戶*

廣告可以顯示在目標網站上（針對內容或針對位置的行銷活動）；當使用者搜尋廣告群組中的其中一個關鍵字（針對搜尋行銷活動）或搜尋您網站上的內容時（在[!DNL Google Ads]僅限搜尋行銷活動中的動態搜尋廣告）；或當使用者執行與您[!DNL Google Merchant Center]或[!DNL Microsoft Merchant Center]產品摘要中的其中一個專案相關的搜尋時（在[!DNL Google Ads]中的購物廣告或在[!DNL Microsoft Advertising]行銷活動中的產品廣告）。

## 可用的廣告型別

您可以在同步的廣告網路帳戶中建立和管理廣告群組的支援廣告型別：

* 在鎖定搜尋網路為目標的行銷活動中，針對廣告群組&#x200B;**文字廣告或展開文字廣告**。 文字廣告可包含選用的追蹤引數，這些引數可覆寫廣告群組或促銷活動層級引數。 根據廣告網路，您或許可以建立展開/延伸的文字廣告或標準文字廣告。

* 針對[!DNL Microsoft Audience Network]上[!DNL Microsoft Advertising]個行銷活動的跨裝置、原生&#x200B;**對象廣告**。 根據行銷活動設定，您有兩個對象廣告選項：

   * 如果促銷活動連結至商家中心商店，則讓廣告網路使用商店的產品資訊，自動為促銷活動產生廣告摘要型廣告。 您不需要為行銷活動建立摘要型廣告，但您必須建立具有使用者定位的廣告群組。

   * 如果行銷活動未連結到商家中心帳戶，則使用回應式廣告格式建立影像型對象廣告，其中包含多個文字和影像資產。 廣告網路會使用最有效的廣告元素組合來組合廣告，並在[!DNL MSN]、[!DNL Outlook.com]和[!DNL Microsoft Edge]之類的網站上顯示廣告。

* 搜尋網路上有[!DNL Google Ads]個促銷活動的&#x200B;**僅限通話的廣告**。 僅限來電廣告是包含電話號碼的文字廣告。 您可以選擇使用[!DNL Google Ads]指派的轉接號碼進行進階通話報告。

* **已針對搜尋促銷活動中的[!DNL Google Ads]和[!DNL Microsoft Advertising]動態搜尋廣告群組，展開動態搜尋廣告** （現在在廣告網路上僅稱為「動態搜尋廣告」）。 動態搜尋廣告會使用您網站的內容（而非關鍵字）來決定何時顯示您的廣告。 廣告網路會動態產生標題、選擇登陸頁面URL和顯示URL，並自動產生最終URL。

  您可以為廣告群組設定特定的動態搜尋目標，藉此定義網站中其內容用於鎖定動態搜尋廣告的頁面。 對於[!DNL Google Ads]，您可以在Search、Social和Commerce中建立動態搜尋目標；對於[!DNL Microsoft Advertising]，您必須在[!DNL Microsoft Advertising]中建立它們。 在[!DNL Google Ads]個行銷活動中，您可以選擇在行銷活動的&quot;[!DNL DSA Options]&quot;區段中指定網站網域和語言，而不是或除了建立動態搜尋目標之外。

  當使用者的搜尋字詞與您其中一個關鍵字型行銷活動中的關鍵字完全相符時，就會顯示關鍵字型行銷活動的廣告，而非動態搜尋廣告。 當使用者的搜尋字詞為廣泛的相符字詞或符合您其中一個關鍵字的片語，且您的動態搜尋廣告擁有較高的廣告排名時，廣告網路會顯示動態搜尋廣告，而非以關鍵字為目標的廣告。

  如需動態搜尋廣告的詳細資訊，請參閱[[!DNL Google Ads] 檔案](https://support.google.com/google-ads/answer/2471185)和[[!DNL Microsoft Advertising] 檔案](https://help.ads.microsoft.com/#apex/ads/en/56794)。

* 針對[!DNL Microsoft Advertising]搜尋行銷活動的&#x200B;**多媒體廣告**。 多媒體廣告是以顯著的主線和側邊欄位置顯示的大型影像廣告，且每頁只顯示一個多媒體廣告。 它們可以包含多個文字和影像資產，例如回應式廣告，而廣告網路會使用最有效的廣告元素組合來組合廣告。 多媒體廣告不會取代文字廣告投放位置。

* 購物網路上&#x200B;**[!DNL Microsoft Advertising]個產品（購物）廣告**&#x200B;的促銷行。 購物廣告會使用您現有[!DNL Microsoft Merchant Center]產品摘要中的產品（而非關鍵字）來決定顯示廣告的方式和位置。 廣告文案與登入頁面URL會根據摘要中的產品資訊自動產生，但您可以選擇設定促銷明細行以納入廣告群組。

  您可以從[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups]檢視，為廣告群組設定個別的產品群組，以控制哪些產品會與您的[!DNL Microsoft Advertising]購物廣告一起顯示。

  如需有關產品/購物廣告工作流程的詳細資訊，請參閱&quot;[實作 [!DNL Microsoft Advertising] 購物行銷活動](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot;。  如需有關產品廣告的其他資訊，請參閱[Microsoft Advertising檔案](https://help.ads.microsoft.com/#apex/3/en/51082)。

* 搜尋網路上[!DNL Google Ads]和[!DNL Microsoft Advertising]行銷活動的回應式搜尋廣告。 廣告網路會動態地從一組廣告標題和說明中組合文字型回應式搜尋廣告，以偏好同時表現優異的組合。 廣告最多包含三個標題、兩個說明，以及來自基本URL和選用的path1和path2欄位的可自訂URL。 您可以選擇將廣告標題和說明釘選至特定位置。

>[!NOTE]
>
>[!DNL Google Ads]不會在其原生編輯器外提供有關顯示為廣告的文字組合的資料。 如需每個文字組合報表的詳細資訊，請參閱[Google Ads檔案](https://support.google.com/google-ads/answer/7684791)。

## [!UICONTROL Ads]檢視

您可以從[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads]檢視建立、編輯和變更廣告狀態。

## 廣告層級的成效資料

廣告層級資料適用於大多數廣告型別。

但是，它無法用於[!DNL Google Ads]動態搜尋廣告(DSA)、最高效能、智慧購物和[!DNL YouTube]行銷活動。 行銷活動的廣告層級資料總計與行銷活動資料總計之間預期會不符。

| 廣告網路/行銷活動/廣告型別 | 資料可用性 |
|---|---|
| [!DNL Google Ads]動態搜尋廣告(DSA) | 行銷活動、廣告群組 |
| [!DNL Google Ads]最高效能 | Campaign |
| [!DNL Google Ads]購物，智慧型購物 | 行銷活動、廣告群組 |
| [!DNL Google Ads] [!DNL YouTube] | 行銷活動、廣告群組 |

>[!MORELIKETHIS]
>
>* [管理廣告](ad-manage.md)
