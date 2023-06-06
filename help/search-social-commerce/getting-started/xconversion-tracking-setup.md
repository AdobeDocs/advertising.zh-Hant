---
title: 設定網頁的轉換追蹤
description: 瞭解如何啟用Adobe廣告以追蹤由廣告曝光次數和點按次數產生的轉換。
source-git-commit: cd8367fbae2234cfdb937c5da8f21f94a615e92a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 設定網頁的轉換追蹤

<!-- I don't think this is necessary here -- we already have a bullet point in the implementation overview -- so removing from TOC. -->

在您產生轉換資料報表之前，Adobe廣告需要每個關鍵字和廣告的曝光數、點選數、成本和轉換（交易）資料。 Adobe廣告也會使用此資料來建立所需的資料預測模型，以最佳化行銷活動預算以及您關鍵字和廣告的競標。

若要啟用Adobe廣告以追蹤由廣告曝光次數和點按次數產生的轉換，您需要執行下列動作：

* 在Search、Social和Commerce管理的每個廣告行銷活動的每個關鍵字、廣告、位置、網站連結和產品群組的追蹤範本或目的地URL中，加入唯一的點選追蹤代碼（並可能加入將一般使用者重新導向至追蹤伺服器的其他代碼）。 這可讓Adobe廣告追蹤每個廣告印象（僅適用於顯示廣告和社交廣告）以及廣告上的每次點按。

* 以下列其中一種方式追蹤轉換資料：

   * **Adobe廣告追蹤的轉換：** 廣告商會在每個轉換頁面上插入Adobe廣告轉換追蹤標籤。

   * **Adobe Analytics轉換：** 廣告商會對所有轉換使用Adobe Analytics追蹤。

   * **[!DNL Google Analytics]轉換：** 廣告商使用 [!DNL Google Analytics] 標籤以追蹤所有轉換。

   * **廣告商追蹤的轉換：** 廣告商提供每日摘要檔案，其中包含線上和離線轉換資料的任意組合。

如需實作追蹤的詳細資訊，請參閱「追蹤」上的說明章節。

>[!MORELIKETHIS]
>
>* [產生Adobe廣告轉換標籤](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [使用「追蹤URL」工具產生搜尋、社交和商務點選追蹤URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [解碼搜尋、社交和商務點選追蹤URL](/help/search-social-commerce/tools/click-tracking-url-decode.md)

