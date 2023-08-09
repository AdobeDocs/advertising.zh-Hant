---
title: 用於報表的資料
description: 瞭解資料檢視和自訂報告中可用的不同型別資料。
exl-id: 3e1f2967-5034-46bc-8473-63cffeeeecba
feature: Search Reports
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# 用於報表的資料

搜尋、社交和商務包含一組以點選和轉換資料為基礎的完整效能報表。 您可以從以下網站檢視產品組合或廣告帳戶中各種元件的基本效能資料： [!UICONTROL Portfolios] 和 [!UICONTROL Campaigns] 檢視以及產生各種基本和進階報表。

使用Adobe Advertising轉換追蹤服務的廣告商也可以識別反向連結網站的地理位置或網域名稱的點按次數、每個管道中的廣告及導致轉換的各種事件對整體轉換率的貢獻，以及單一轉換的分佈 [轉換量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) 依行銷管道。 可用的報告因使用者帳戶型別而異。 Adobe帳戶團隊有權存取所有報表。

大多數報告都可以自訂，以僅顯示您想要檢視的資訊。 下列標準量度可用於大多數報表，並在廣告層級進行計算：

* **標準效能量度：**

   * **[!UICONTROL Impressions]：** 廣告刊登的總次數。

   * **[!UICONTROL Clicks]：** 廣告中連結的點按總次數。

   * **[!UICONTROL Cost]：** 廣告的總成本。 每次點按付費(PPC)廣告的成本永遠是點按次數乘以每次點按成本。

   * **[!UICONTROL Cost per Click]：** 廣告點按一次的平均成本，即廣告成本除以廣告點按總次數。 例如，如果您對廣告曝光次數花費100美元，且廣告產生10次點按，則每次點按成本為100美元/10=10美元。

   * **[!UICONTROL Average Position]：** （適用時）已投放廣告的平均位置，以曝光次數加權。

   * **[!UICONTROL Estimated Clicks]：** (僅包含在具有Adobe Advertising轉換追蹤服務的廣告商的進階報表中)反向連結網站的城市或網域名稱的估計點按總數。 這可能包括廣告商沒有廣告帳戶的廣告網路資料。

* **轉換量度：** 每個廣告商的轉換量度或針對轉換量度追蹤的交易資料的總轉換次數。 這可能包括轉換和網站參與量度，但不會包括從Adobe Analytics同步的計算量度和進階計算量度。

  其中可能包括 [[!DNL Google Ads] — 追蹤的轉換](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) 和 [[!DNL Google Analytics] — 追蹤的轉換](/help/search-social-commerce/admin/data-sources/data-source-about.md) 已針對廣告商帳戶同步的ID。

* **自訂量度：** 您自己的量度，這是根據現有量度（例如每筆訂單的成本）建立公式所衍生。

## 資料可用性

產生報表時，您可以選擇如何將轉換資料歸因到導致轉換的一系列事件中。 例如，您可以選擇將整個轉換歸因於最後一個事件，或將最後一個事件的權重設定得高於其他事件。 依預設，轉換會歸因於最後一個事件。

根據您為報表指定的歸因規則，每種報表型別的資料可用於以下日期。

| 報表群組 | 報告 | 資料可用的日期 |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | 2021年5月15日開始。<br><br><b>例外：</b> 顯著量度資料自2022年9月8日起提供。 |
| | 所有其他 [!UICONTROL Basic Reports] | 前36個月。<br><br><b>例外：</b> 顯著量度資料自2022年9月8日起提供。 |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | 前45天。 |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | 前兩(2)個月加上本月。 |
| [!UICONTROL Assist Reports] | 全部 | 前18個月。 |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | 上一年。 |
| | [!UICONTROL RSA Assets Report] | 自2022年8月10日起。 |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report] | 過去180天。 |
| | 所有其他 [!UICONTROL Specialty Reports] | 前兩(2)個月。 |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | 前18個月。 |
| [!UICONTROL Change History Report] | — | 前31天。 |

>[!MORELIKETHIS]
>
>* [關於報表](report-about.md)
>* [報表的初始設定工作](initial-setup.md)
