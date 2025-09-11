---
title: 可用報表欄
description: 請參閱自訂報表中可用欄的說明。
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: ae7431218dcb547ded53d4bad1a79b894ee973fe
workflow-type: tm+mt
source-wordcount: '2307'
ht-degree: 0%

---

# 可用報表欄

<!-- Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

| 量度型別 | 子型別 | 欄名稱 | 說明 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | 外部廣告伺服器指派的廣告ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | DSP中廣告的唯一識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | 使用者指派的廣告名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | 廣告的格式。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | 使用者變更的或日期輸入所表示的廣告分類： *[!UICONTROL live]*、*[!UICONTROL scheduled]*、*[!UICONTROL completed]*&#x200B;或&#x200B;*[!UICONTROL archived]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | 廣告商的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | 使用者為行銷活動指派的總預算。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | 行銷活動的結束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | DSP中促銷活動的唯一識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | 使用者指派的行銷活動名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | 行銷活動的第一個日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | 內容/影片標題。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | 內容系列。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | 內容型別。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | 由[IAB技術實驗室](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md)定義的生產品質。 值可以`Unknown`、`Professionally Produced`、`Prosumer`或`User Generated`。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | [IAB技術實驗室](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md)所定義的內容型別。 值可以包含`Video,` `Game`、`Music`、`Application`、`Text`、`Other`或`Unknown`。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | 內容分級，例如PG或R。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | 廣告是否出現在直播串流中： `Not Live`或`Live`。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | 內容長度（以秒為單位）；通常用於視訊或音訊。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | 使用ISO-639-1-alpha-2的內容語言。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | 年、月、日。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | 日[!UICONTROL of Week] | 特定日期，例如[!UICONTROL Monday]或[!UICONTROL Tuesday]。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | 年、月、日和小時。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | 月份和年份。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | 從0到23的該小時時間。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | 相關周的日期範圍，從星期日至星期六。 範例： 2021-02-18到2021-03-07。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | 顯示廣告的瀏覽器供應商(例如Google或Mozilla)。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | 顯示廣告的瀏覽器版本（例如[!UICONTROL Safari 4.3]或[!UICONTROL Chrome 7.0]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | 顯示廣告的瀏覽器（例如[!UICONTROL Chrome]或[!UICONTROL Firefox]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Environment] | 廣告是否顯示在&#x200B;*[!UICONTROL sites]*&#x200B;或&#x200B;*[!UICONTROL Apps]*&#x200B;上。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | 顯示廣告的裝置型別（例如[!UICONTROL Set Top Box]或[!UICONTROL Mobile Phone]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | 顯示廣告之裝置的製造商（例如[!UICONTROL Samsung]、[!UICONTROL Lenovo]或[!UICONTROL Apple]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | 顯示廣告的裝置型號（例如[!UICONTROL iPhone XS]或[!UICONTROL Galaxy Note 7]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | 顯示廣告之作業系統的廠商（例如[!UICONTROL Microsoft]或[!UICONTROL Apple]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | 顯示廣告的作業系統版本（例如[!UICONTROL Windows 10]或[!UICONTROL iOS Mojave]） |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | 顯示廣告的作業系統（例如[!UICONTROL Apple iOS]或[!UICONTROL Android]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal ID] | 透過外部供給合作夥伴指派給交易的唯一識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Feed Name] | 在DSP中輸入之使用者指派的交易名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Feed Source] | 提供存貨的供給端合作夥伴。 這通常是發佈者，但也可以是SSP。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | 詳細目錄的分類： *[!UICONTROL Private]、* *[!UICONTROL On Demand]、*&#x200B;或&#x200B;*[!UICONTROL Public]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | 媒體歸因的供應方合作夥伴(SSP)。 |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | 裝置收到廣告的次數，根據唯一的Cookie或裝置ID而定。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | 報告資料所屬的城市。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | 報告資料所屬的國家/地區。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | 報告資料所屬的指定市場區域(DMA)。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | 報告資料的歸因狀態。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | 對象。 報表支援最多10個不重複受眾。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | 行銷活動。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | 創意長度。 報表支援最多10個不重複的創意長度。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | 裝置。 報表支援最多10部不重複裝置。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | 摘要型別。 報表支援最多10種不重複摘要型別。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | 媒體型別。 報表支援最多10種不重複媒體型別。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | 發行者。 此報表支援最多10個不重複發行者。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | 套件。<!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | 位置。<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | 提供廣告印象的網站或應用程式。 報表最多可支援10個不重複網站或應用程式。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | 作為刊登版位自訂識別碼使用的刊登版位標籤。 報表最多可支援10個不重複的位置標籤。<!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | 對象。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | 行銷活動。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | 創意長度。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | 裝置。 （例如CTV、桌上型電腦等） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | 媒體型別。 （例如顯示器、音訊等） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | 發行者。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | 位置。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | 封裝的結束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | 套件的步調目標金額。 此金額以支出或曝光次數表示。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | DSP中套件的唯一識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | 封裝的名稱 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | 封裝開始日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | 位置結束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | （已棄用） DSP指派給舊版[!DNL TubeMogul]轉換事件的轉換ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | （已棄用）指派給舊版[!DNL TubeMogul]轉換事件的轉換名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | DSP中位置的唯一識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | 使用者指派的位置名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | 位置預算。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | 此位置的最高出價。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Device Environment] | 位置要定位的裝置環境： （*[!UICONTROL Desktop]*、*[!UICONTROL Mobile]*&#x200B;和/或&#x200B;*[!UICONTROL Connected TV]）*。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | 位置結束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | 刊登開始日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | 作為刊登版位自訂識別碼使用的刊登版位標籤。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | 與可計費區段相關的說明。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | 與計費區段相關聯的唯一關鍵值。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | 可計費區段的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | 與區段關聯的說明，由資料提供者提供。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | 與區段相關聯的唯一關鍵值。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | 區段名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | 與區段相關聯的資料提供者名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | DSP中網站或應用程式的唯一識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | 網站的名稱。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | 上傳後處理的視訊長度。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | DSP中視訊創意的唯一識別碼。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | 使用者指派的創意內容名稱。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | [!UICONTROL App/Site Distinct Uniques]除以[!UICONTROL App/Site Uniques]。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | 僅在此應用程式上可觸及的裝置總數。 這個值不包含向多個發佈者中的廣告公開的檢視器。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | [!UICONTROL Total Spend]除以[!UICONTROL App/Site Distinct Uniques]。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | [!UICONTROL Total Spend]除以[!UICONTROL App/Site Uniques]。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | 已接受曝光的目標家庭宇宙的估計百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | 顯示給不重複專案的平均曝光次數。 對於某些詳細目錄，發佈者不會傳遞裝置識別碼，且這些曝光不會包含在此值中。 [!UICONTROL Frequency (by App/Site)]報表中有類似的量度，但並未估計該量度。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | （包含在[!UICONTROL Frequency (by Impression)]報告中）指定頻率劃分的估計曝光數。 DSP的估計是以曝光數範例為基礎。 對於某些詳細目錄，發佈者不會傳遞裝置識別碼，且這些曝光不會包含在此值中。 [!UICONTROL Frequency (by App/Site)]報表中有類似的量度，但並未估計該量度。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | （包含在[!UICONTROL Frequency (by Impression)]報表中）在特定頻率下記錄的不重複瀏覽器或裝置數目。 DSP的估計是以曝光數範例為基礎。 對於某些詳細目錄，請勿傳遞裝置識別碼，而且這些曝光不會包含在此值中。 [!UICONTROL Frequency (by App/Site)]報表中有類似的量度，但並未估計該量度。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | DSP （拍賣）在日期範圍內看到的不重複家庭總數。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | 將裝置圖表用於以人物為基礎的跨裝置鎖定目標所獲得的曝光總數。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Frequency] | 每個家庭的曝光頻率。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | 僅依報告的維度觸及家庭的頻率，包括維度最多三個值的交集。 例如，如果您使用[!UICONTROL Placement]維度，則可檢視個別版位所達到的頻率、任意兩個版位組合所達到的頻率，以及任意三個版位組合所達到的頻率。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | 僅由報告維度觸及的家庭數目，計算為僅由報告維度<code>[觸及的]IP位址 — 由任何其他維度觸及的[IP位址]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | 只透過報告維度觸及的家庭百分比，計算方式為<code>[維度觸及的IP位址百分比] - [任何其他維度觸及的IP位址百分比]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Impressions] | 提供的廣告曝光總數。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | 為了可檢視度而提供的曝光總數。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | 僅報告維度提供的可測量曝光總數，包括最多三個維度值的交集。 例如，如果您使用[!UICONTROL Placement]維度，則可檢視個別版位所達到的可測量曝光數、任意兩個版位組合所達到的可測量曝光數，以及任意三個版位組合所達到的可測量曝光數。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | 總支出。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | 到達的不重複住戶總數（不同的IP位址）。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | 僅由報告維度觸及的不重複住戶總數（不同的IP位址），包括維度最多三個值的交集。 例如，如果您使用[!UICONTROL Placement]維度，則可檢視個別版位所觸及的唯一家庭、任意兩個版位組合所觸及的共同家庭，以及任意三個版位組合所觸及的共同家庭。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | 總支出除以已達的遞增家庭。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | 總支出除以達到的不重複家庭。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | 每個家庭的曝光頻率。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | 僅由報告維度觸及的家庭數目，計算為僅由報告維度[觸及的]IP位址 — 任何其他維度[觸及的]IP位址。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | 只透過報告維度觸及的家庭百分比，計算方式為[維度觸及的IP位址百分比] - [任何其他維度觸及的IP位址百分比]。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | 提供的廣告曝光總數。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | 為了可檢視度而提供的曝光總數。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | 總支出。 |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | 到達的不重複住戶總數（不同的IP位址）。 |
| [!UICONTROL Metric] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | 鎖定的ID型別。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | 每次收購的平均總成本，計算方式為<code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | 每次廣告點按的平均總成本，計算方式為<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | 每個已完成視訊檢視的平均成本，計算方式為<code>[!UICONTROL Gross Spend] / [!UICONTROL 100% Completions]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | 每1000次曝光的平均成本，計算方式為<code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | 每個視訊檢視的平均成本，計算方式為<code>[!UICONTROL Gross Spend] / [!UICONTROL Views]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | 每1000個可檢視曝光的平均成本，計算方式為<code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1000</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | 每次廣告點按的平均淨成本，計算方式為<code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Clicks]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | 每個已完成視訊檢視的平均淨成本，計算方式為<code>[!UICONTROL Net Spend] / [!UICONTROL 100% Completions]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | 每1000次曝光的平均淨成本，計算方式為<code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | 每個視訊檢視的平均淨成本，計算方式為<code>[!UICONTROL Net Spend] / [!UICONTROL Views]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | 在CPM上限出價的總出價百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | DSP為位置競標的不同使用者人數。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Data Net Spend] | 透過DSP計費的對象區段資料費用總淨成本。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Media Net Spend] | 透過DSP計費的可計費媒體總淨成本，包括技術費用。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Other Net Spend] | 透過DSP計費的其他服務費用（協力廠商驗證合作夥伴、廣告服務等）總成本。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | 協力廠商對象區段和資料服務的預估稅捐。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | 預估的媒體稅金，包含套用至DSP中媒體成本再計費和技術費用服務的稅金。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | 透過DSP計費的其他服務費用（包括協力廠商驗證合作夥伴、主題鎖定目標等）估計稅金。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Margin %] | （啟用利潤管理時）利潤百分比，由<code>([!UICONTROL Gross Spend] - [!UICONTROL Net Spend]) / [!UICONTROL Gross Spend]計算</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | 不收取任何技術費用的非收費與收費媒體成本總和。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | 每1000個可檢視曝光的平均淨成本，計算方式為<code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Net Spend] | 未透過DSP計費的對象區段資料費用總淨成本。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Fees] | 非計費媒體的總淨成本，包括未透過DSP計費的技術費用。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | 未透過DSP計費的其他服務費用（協力廠商驗證合作夥伴、廣告服務等）總成本。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Billable Net Spend] | [!UICONTROL Billable Spend (Media)]、[!UICONTROL Billable Spend (Data)]和[!UICONTROL Billable Spend (Other)]的總和。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | 每1000次曝光的平均淨資料成本，計算方式為<code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Data Net Spend] | 對象區段資料費用的總淨成本。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | 每1000次曝光的平均淨媒體成本，計算方式為<code>[!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Media Net Spend] | 包括技術費用在內的媒體淨成本總計。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | [!UICONTROL Net Spend (Media)]、[!UICONTROL Net Spend (Data)]和[!UICONTROL Net Spend (Other)]的總和。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | [!UICONTROL Non-billable Spend (Media)]、[!UICONTROL Non-billable Spend (Data)]和[!UICONTROL Non-billable Spend (Other)]的總和。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | 其他費用的每1000次曝光的平均淨成本，計算方式為<code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Other Net Spend] | 其他服務費用（協力廠商驗證合作夥伴、廣告服務等）的總淨成本。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | 觀看整個廣告的檢視百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | 觀看整個廣告的檢視次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | 觀看整個廣告的可檢視曝光數百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | 至少觀看廣告四分之一的檢視率。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | 觀看廣告至少一個四分位數的檢視次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | 觀看廣告至少四分位數的檢視百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | 觀看廣告至少四分位數的檢視次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | 觀看廣告至少四分位數的可檢視曝光次數百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | 觀看廣告至少四分位數的檢視百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | 觀看廣告至少四分位數的檢視次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | 平均百分比的廣告觀看至完成，計入所有檢視。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | 廣告覆蓋和橫幅的點按次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | 點按次數百分比除以廣告曝光數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | 點按百分比除以視訊檢視。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | 隨附橫幅點按次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | 點按百分比除以隨附橫幅曝光數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | 隨附橫幅曝光次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | 用來檢視廣告的網際網路連線型別（例如Wifi或4g LTE）。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 已投放廣告的互動次數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 廣告印象總數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | 提供導致視訊檢視的曝光次數百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | 視訊檢視的平均持續時間（以秒為單位）。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | 對廣告的所有點按總和。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | 影片廣告被檢視的總分鐘數。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | 視訊廣告檢視總數。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | 平均播放器寬度和高度。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | 為了可檢視度而提供的曝光總數。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | 提供可測量可檢視度的曝光百分比，計算為<code>[!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | 由於iFrame不相容，因此無法測量可檢視度的曝光百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | 由於廣告單位上不支援的可檢視度追蹤而無法測量的可檢視度曝光次數。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | 由於其他原因而無法測量可檢視度的曝光百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | 無法測量可檢視度的廣告曝光次數。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | 無法測量可檢視度的廣告曝光百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | 由於此廣告單位不支援的可檢視度追蹤而無法測量的可檢視度曝光百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | 所有可測量曝光的可檢視曝光百分比，計算為<code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | 視為可檢視的廣告曝光次數。 |
| [!UICONTROL Conversion Metrics] | [在報告設定中依廣告商分組] | [廣告商特定轉換] | 指定的廣告商特定轉換量度或Adobe Analytics事件的總計。 |
| [!UICONTROL Custom Goals] | [在報告設定中依廣告商分組] | [廣告商特定自訂目標] | 包含在指定[自訂目標](/help/dsp/optimization/custom-goal.md)中的所有轉換的加權總和。 |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal CPA|The average cost per acquisition, calculated by <code>Gross Spend / Custom Goal</code> | -->
<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [關於自訂報告](/help/dsp/reports/report-about.md)
>* [建立自訂報告](/help/dsp/reports/report-create.md)
>* [複製自訂報告](/help/dsp/reports/report-copy.md)
>* [編輯自訂報告](/help/dsp/reports/report-edit.md)
>* [自訂報告設定](/help/dsp/reports/report-settings.md)
