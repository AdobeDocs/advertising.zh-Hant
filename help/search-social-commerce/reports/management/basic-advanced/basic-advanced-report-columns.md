---
title: 基本和進階報表的報表欄
description: 瞭解基本和進階報告的可用資料欄。
exl-id: 649cdfa0-e6f2-4881-9f9d-8217e2547d99
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: af7f2dbb2b53b6f61b848a75a081c402341df979
workflow-type: tm+mt
source-wordcount: '3745'
ht-degree: 0%

---

# 基本和進階報表的報表欄

| 欄 | 說明 |
| ---- | ---- |
| \[廣告商專屬的自訂（衍生）量度\] | 您建立的[自訂量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md)的值（根據現有量度計算）。 |
| \[廣告商特定標籤分類\] | 實體層級目前套用至實體的任何標籤分類。 多個標籤分類使用逗號(，)分隔。 |
| \[廣告商專用轉換量度\] | 指定的轉換量度或網站參與量度的轉換次數。 |
| \[Google追蹤的轉換\] | 請參閱「GGL\*、GGL_CT\*和GGL_XD_CT\*」專案。 |
| [!UICONTROL 7-Day Click Accuracy] | ([!UICONTROL Portfolio Report])前七天點按預測的平均準確度，不包括當天（不包括報表的指定日期範圍），以百分比表示。 |
| [!UICONTROL 7-Day Cost Accuracy] | ([!UICONTROL Portfolio Report])前七天成本預測的平均準確度，不包括當天（不包括報表的指定日期範圍），以百分比表示。 |
| [!UICONTROL 7-Day Revenue Accuracy] | ([!UICONTROL Portfolio Report])前七天收入預測的平均準確度，不包括當天（不包括報表的指定日期範圍），以百分比表示。 |
| [!UICONTROL Account] | 帳戶名稱。 |
| [!UICONTROL Account Status] | 搜尋、社交和Commerce中的帳戶狀態： <ul><li><i>[!UICONTROL Enabled]：</i> （預設）對於同步的廣告網路，Search、Social和Commerce可以登入廣告網路帳戶來擷取行銷活動資料，並啟用其他適用的功能，例如最佳化和追蹤產生。<br><br>對於未同步的廣告網路，可以使用適用的功能，例如最佳化和/或追蹤產生。</li><li><i>[!UICONTROL Disabled]：</i>對於同步的廣告網路，Search、Social和Commerce不會登入廣告網路帳戶，因此不會擷取行銷活動資料，且停用其他適用的功能，例如最佳化和追蹤產生。 系統仍會儲存您啟用帳戶時收集的資料，但您日後建立的所有行銷活動管理檢視及所有報表，都不會包含帳戶停用期間的資料。<br><br>對於未同步的廣告網路，無法使用適用的功能，例如最佳化和/或追蹤產生。</li></ul> |
| [!UICONTROL Active Ad Groups] | 作用中廣告群組的數量。 |
| [!UICONTROL Active Ads/Creatives] | 作用中廣告/創意內容的數量。 |
| [!UICONTROL Active Campaigns] | 作用中行銷活動的數量。 |
| [!UICONTROL Active Keywords] | 作用中的關鍵字數目。 |
| [!UICONTROL Ad Group] | 廣告群組。 |
| [!UICONTROL Ad Group ID] | 可識別現有廣告群組的唯一ID。 |
| [!UICONTROL Ad Group Status] | 廣告群組狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Group Type] | 廣告群組型別，例如<i>[!UICONTROL Audience]</i> （僅適用於對象行銷活動）、<i>[!UICONTROL Demand Gen]</i> （僅適用於需求一般行銷活動）、<i>[!UICONTROL Display]</i> （僅適用於顯示行銷活動）、<i>[!UICONTROL Search Dynamic]</i> （僅適用於動態搜尋廣告）、<i>[!UICONTROL Search Standard]</i> （僅適用於回應式搜尋廣告和現有的擴充文字廣告）、<i>[!UICONTROL Shopping Showcase]</i>、<i>[!UICONTROL Shopping Product]</i> （僅適用於標準購物行銷活動）或<i>[!UICONTROL Shopping Smart]</i> （適用於智慧購物行銷活動）。 對於某些行銷活動型別，單一行銷活動可包含多個廣告型別。 |
| [!UICONTROL Ad Groups] | 指派標籤值的廣告群組數目。 |
| [!UICONTROL AD Name] | 廣告群組名稱；與[!UICONTROL Ad Group]的值相同。 |
| [!UICONTROL Ad Recall Lift] | （僅限[!DNL Meta]個行銷活動）兩天內記住您廣告的估計人數。 |
| [!UICONTROL Ad Recall Rate] | （僅限[!DNL Meta]個行銷活動）兩天內記住您廣告的估計人數除以您已聯絡的人數，以百分比表示。 |
| [!UICONTROL Ad Size] | 廣告的維度。 |
| [!UICONTROL AD Strength] | （[!DNL Google Ads]個回應式搜尋廣告）廣告的效果： <i>[!UICONTROL average]</i>、<i>[!UICONTROL excellent]</i>、<i>[!UICONTROL good]</i>、<i>[!UICONTROL no_ads]</i>、<i>[!UICONTROL pending]</i>、<i>[!UICONTROL poor]</i>、<i>[!UICONTROL unknown]</i>或<i>[!UICONTROL unspecified]</i>。 |
| [!UICONTROL Adgroup MBA] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]行銷活動）目前的廣告群組層級行動競標調整，決定在行動裝置上顯示廣告時如何調整競標。 |
| [!UICONTROL Advertiser] | 廣告商名稱。 |
| [!UICONTROL Advertiser ID] | 廣告商的搜尋、社交和Commerce帳戶的數值ID。 |
| [!UICONTROL Avg Position] | 指定日期範圍內的廣告平均位置。<br><br>對於[!DNL Google Ads]和[!DNL Yahoo! Japan Ads]行銷活動，此資料僅在2019年9月之前可用。 對於[!DNL Microsoft Advertising]，此資料僅在2021年1月22日之前可用。 |
| [!UICONTROL Base URL] | 關鍵字的基本URL，包括為促銷活動或帳戶設定的任何附加引數。 其中不包含任何搜尋、社交和Commerce重新導向與追蹤程式碼。 |
| [!UICONTROL Bid Strategy] | （大多數廣告網路）對於行銷活動或行銷活動元件，這是行銷活動的競標策略。 對於連結至經理帳戶的廣告網路帳戶，這是跨帳戶競標策略。 可用的值會依廣告網路而異。 |
| [!UICONTROL Business Name] | （[!DNL Microsoft Advertising]個回應式廣告）企業名稱。 |
| [!UICONTROL Call to Action] | （[!DNL Microsoft Advertising]個回應式與多媒體廣告）廣告中包含的行動號召。 |
| [!UICONTROL Campaign] | 行銷活動。 |
| [!UICONTROL Campaign Budget] | 行銷活動預算。 |
| [!UICONTROL Campaign MBA] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]行銷活動）目前的行銷活動層級行動競標調整，決定在行動裝置上顯示廣告時如何調整競標。 |
| [!UICONTROL Campaign Product Scope Filter] | （僅使用購物網路的行銷活動）商家帳戶中的產品，可為行銷活動建立產品廣告。 |
| [!UICONTROL Campaign Start Date] | 對行銷活動出價的第一天。 |
| [!UICONTROL Campaign Status] | 行銷活動狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Ended]</i>或<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Campaign Type] | 行銷活動型別，例如<i>[!UICONTROL Audience (Ctv Video)]</i><i>[!UICONTROL Audience (Feed)]</i>、<i>[!UICONTROL Audience (Image)]</i>、<i>[!UICONTROL Audience (Video)]</i>、<i>[!UICONTROL Brand Shopping]</i>、<i>[!UICONTROL Demand Gen]</i>、<i>[!UICONTROL Search and Display]</i>、<i>[!UICONTROL Standard Display]</i>、<i>[!UICONTROL Standard Performance Max]</i>、<i>[!UICONTROL Standard Search]</i>、<i>[!UICONTROL Standard Shopping]</i>、<i>[!UICONTROL Store Ad]</i>、<i>[!UICONTROL Video]</i>或<i>[!UICONTROL Others]</i>。 |
| [!UICONTROL Channel Type] | 行銷管道型別： <i>[!UICONTROL Search]</i>或<i>[!UICONTROL Content]</i>。 當報告設定中的報告[!UICONTROL Search/Content]設定為&quot;[!UICONTROL Combined]&quot;時，此欄不包括在內。 |
| [!UICONTROL City] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Transaction Report])產生點按的城市。 這是根據使用者的IP位址所決定。 |
| [!UICONTROL Click Match Type] | 關鍵字元合所點選廣告的型別。 除了具有多個相符型別的[!DNL Microsoft Advertising]關鍵字外，這與[!UICONTROL Listing Match Type]相同。 對於[!DNL Microsoft Advertising]關鍵字，這是實際點按的相符型別。 |
| [!UICONTROL Click Value] | ([!UICONTROL Portfolio Report])為投資組合目標指定的點按值。 |
| [!UICONTROL Click/Impression Time] | ([!UICONTROL Transaction Report])造成轉換的點選或曝光發生的時間。 |
| [!UICONTROL Clicks] | 指定日期範圍內的廣告點選次數。 |
| [!UICONTROL Client ID1]，[!UICONTROL Client Id 1] | （[!UICONTROL Keyword Report]、[!UICONTROL Ad Variation Report]和[!UICONTROL Transaction Report]；摘要式追蹤實作）關鍵字或廣告的使用者端特定追蹤ID，已在摘要檔案中傳送。 |
| [!UICONTROL Client Id 2] | （[!UICONTROL Keyword Report]和[!UICONTROL Transaction Report]；摘要式追蹤實作）關鍵字或廣告的使用者端特定追蹤ID，已在摘要檔案中傳送。 |
| [!UICONTROL Client Transaction ID] | ([!UICONTROL Transaction Report])唯一交易識別碼。 |
| [!UICONTROL Constraint End Date] | ([!UICONTROL Constraint Report])限製作用中的最後一天。 |
| [!UICONTROL Constraint Name] | ([!UICONTROL Constraint Report])條件約束名稱。 |
| [!UICONTROL Constraint Start Date] | ([!UICONTROL Constraint Report])限製作用中的第一天。 |
| [!UICONTROL Constraint Status] | ([!UICONTROL Constraint Report])條件約束的狀態： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Paused]</i>。 |
| [!UICONTROL Constraint Type] | ([!UICONTROL Constraint Report])條件約束的型別： <i>[!UICONTROL Bid/Pos Constraint]</i>、<i>[!UICONTROL Bid Shift]</i>、<i>[!UICONTROL Campaign Budget]</i>、<i>[!UICONTROL Context Sensitive Bid]</i>、<i>[!UICONTROL Incremental Bidding]</i>、<i>[!UICONTROL Max CPA]</i>、<i>[!UICONTROL Min Margin]</i>、<i>[!UICONTROL Variable Bid Position]</i>、<i>[!UICONTROL Search Engine Min Bid]</i>或<i>[!UICONTROL Variable Position]</i>。 |
| [!UICONTROL Constraints] | 圖元上任何適用限制的名稱，以逗號分隔。 |
| [!UICONTROL Content IS] | 您在顯示/對象網路上收到廣告的曝光數除以您符合資格接收的預估曝光數。 在[!DNL Microsoft Advertising]中，這稱為&quot;[!UICONTROL Audience IS]&quot;。 |
| [!UICONTROL Content IS Lost (budget)] | 由於您的每日或每月預算太低，您在顯示/對象網路上的廣告未收到的預估曝光百分比。 在[!DNL Microsoft Advertising]中，這稱為&quot;[!UICONTROL Audience lost IS (budget)]&quot;。 |
| [!UICONTROL Content IS Lost (rank)] | 由於廣告排名不佳，您在顯示/對象網路上的廣告未顯示的預估曝光百分比。 在[!DNL Microsoft Advertising]中，這稱為&quot;[!UICONTROL Audience lost IS (rank)]&quot;。 |
| [!UICONTROL Conversion Type] | ([!UICONTROL Transaction Report])轉換前的動作：<ul><li><i>[!UICONTROL Click:]</i>轉換前至少發生一次付費點按。</li><li><i>[!UICONTROL Impression:]</i>轉換前未發生任何付費點按，因此轉換是由檢視所產生（沒有任何付費點按的印象）。</li></ul> |
| [!UICONTROL Cost] | 指定日期範圍內的廣告總成本。 |
| [!UICONTROL Country] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])產生點按的國家/地區。 這是根據使用者的IP位址所決定。 |
| [!UICONTROL CPC] | 指定日期範圍內廣告的每次點按成本(CPC)。 |
| [!UICONTROL Creative Base URL] | 廣告的基本URL，包括為促銷活動或帳戶設定的任何附加引數。 其中不包含任何搜尋、社交和Commerce重新導向與追蹤程式碼。 |
| [!UICONTROL Creative Destination URL] | 廣告的最終URL或目的地URL （包括任何追蹤引數）。 |
| [!UICONTROL Creative Name] | （僅限[!DNL Yahoo! Japan]）廣告影像名稱。 |
| [!UICONTROL Creative Title]，[!UICONTROL Creative Title2] - [!UICONTROL Creative Title3] | 廣告的標題或標題。 不同的創意型別有不同數量的必要和選用標題行。 若要在[!DNL Microsoft Advertising]個回應式廣告或多媒體廣告中檢視[!UICONTROL Creative Title4]和更高的欄，請在報表設定中加入&quot;[!UICONTROL Creative Titles]&quot;欄。 |
| [!UICONTROL Creative Titles] | （僅適用於多媒體和回應式搜尋廣告）為每個廣告的簡短標題新增一欄（&quot;[!UICONTROL Creative Title]&quot;到&quot;[!UICONTROL Creative Title15]&quot;）。 當您包含此欄時，您不需要包含其他[!UICONTROL Creative Title]欄，但是請編輯[!UICONTROL Order Results/Limit Rows By]區段來依[!UICONTROL Creative Titles]排序，而非[!UICONTROL Creative Title]。 |
| [!UICONTROL Creative Type] | 廣告格式。 可能的值如下： <i>[!UICONTROL App Install Ad]</i>、<i>[!UICONTROL Call Only Ad]</i>、<i>[!UICONTROL Demand Gen Carousel Ad]</i> （多影像轉盤廣告）、<i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>、<i>[!UICONTROL Demand Gen Product Ad]</i>和<i>[!UICONTROL Demand Gen Video Ad]</i>、<i>[!UICONTROL Display Ad]</i>、<i>[!UICONTROL Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Text Ad]</i>、<i>[!UICONTROL Legacy Text Ad]</i>、<i>[!UICONTROL Multimedia Ad]</i>、<i>[!UICONTROL Product Ad]</i>、<i>[!UICONTROL Responsive Ad]</i>、<i>[!UICONTROL Responsive Search Ad]</i>或<i>[!UICONTROL Text Ad]</i>。 |
| [!UICONTROL CTR] | 點進率，即點按次數除以所包含廣告的曝光次數。 |
| [!UICONTROL Currency] | 適用的貨幣型別（例如「USD」或「GBP」）。<br><br><b>注意：</b>如果報表包含不同貨幣的帳戶資料，則任何「[!UICONTROL Total]」貨幣值只是欄中所有數字的總和，無論貨幣為何。 |
| [!UICONTROL Current Bid] | 目標的目前出價。 |
| [!UICONTROL Current First Page Bid] | （僅限[!DNL Google Ads]個行銷活動）當[!DNL Google]搜尋查詢符合關鍵字時，目前要放在搜尋結果第一頁上的廣告所需的預估每次點按成本(CPC)競標。<br><br>對於單一關鍵字和相符型別組合，此值是該組合目前所需的第一個頁面競標。 當在多個行銷活動中使用相同的關鍵字和相符型別組合時，此值是目前所有執行個體中所需的最低第一頁競標。 |
| [!UICONTROL Current Quality Score] | （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]行銷活動）廣告網路所指定的關鍵字或競標單位的目前品質分數。 其範圍從1 （低）到10 （完美）。 對於單一關鍵字和相符型別組合，此值是該組合的目前分數。 當在多個行銷活動中使用相同的關鍵字和相符型別組合時，此值是所有執行個體中目前的最大分數。<br><br>廣告網路會使用品質分數來決定出價與廣告位置。 它是根據許多因素計算的，包括關鍵字與其相關廣告、使用者的搜尋查詢及登入頁面品質的相關性。 對於[!DNL Google Ads]中的關鍵字，也會考量關鍵字的點進率，對於[!DNL Microsoft Advertising]中的關鍵字，也會考量登入頁面所提供的使用者體驗。 |
| [!UICONTROL Custom Bid Level] | (只針對顯示網路的Google行銷活動)投出競價的層級為：<i>[!UICONTROL Ad Group]</i>、<i>[!UICONTROL Age]</i>、<i>[!UICONTROL Gender]</i>、<i>[!UICONTROL Interest and List]</i>、<i>[!UICONTROL Keyword]</i>、<i>[!UICONTROL Placement]</i>、<i>[!UICONTROL Vertical]</i>、<i>[!UICONTROL None]</i>或<i>[!UICONTROL Unknown]</i>。 |
| [!UICONTROL Description1] - [!UICONTROL Description4] | 廣告內文。 不同的創意型別有不同數量的必要和選用說明行。 若要在[!DNL Microsoft Advertising]個回應式廣告或多媒體廣告中檢視[!UICONTROL Description3]和[!UICONTROL Description4]欄，請在報表設定中加入&quot;[!UICONTROL Descriptions]&quot;欄。 |
| [!UICONTROL Descriptions] | （[!DNL Microsoft Advertising]個回應式及多媒體廣告）為每個廣告的說明列（&quot;[!UICONTROL Description1]&quot;到&quot;[!UICONTROL Description4]&quot;）新增一欄。 包含此欄時，您不需要包含其他[!UICONTROL Description]欄。 |
| [!UICONTROL Device] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads]和[!DNL Yahoo Native]行銷活動）顯示廣告的裝置型別： <i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Mobile]</i>、<i>[!UICONTROL Tablets]</i>、<i>[!UICONTROL Other]</i>或<i>[!UICONTROL N/A]</i> （無值）。 其他廣告網路的資料列值為N/A。<br><br>在搜尋行銷活動中，如果關鍵字、廣告和/或廣告擴充功能的追蹤範本或目的地URL包含引數，以便依裝置(`&ev_dvc={device}&ev_dvm={devicemodel}`)在廣告點按時追蹤資料，則每個裝置型別的資料列也會包含轉換資料。 否則，如果轉換資料無法歸因於裝置型別，則會將其彙總在具有「[!UICONTROL Device]」值[!UICONTROL N/A]的個別列中。 |
| [!UICONTROL Display Path 1] | （僅限[!DNL Google Ads]個延伸文字廣告）廣告基底URL之後的第一個顯示路徑。 |
| [!UICONTROL Display Path 2] | （僅限[!DNL Google Ads]個延伸文字廣告）廣告基底URL之後的第二個顯示路徑。 |
| [!UICONTROL Display Type] | 已過時 |
| [!UICONTROL Display URL] | 廣告的顯示URL，這是一般使用者在廣告中看到的內容。 |
| [!UICONTROL DMA] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])點按產生的指定數值市場區域（例如751代表丹佛）。 這是根據使用者的IP位址所決定。 |
| [!UICONTROL Domain] | ([!UICONTROL Domain Referral Report]， [!UICONTROL Keyword Report])產生點按的網域名稱。 |
| [!UICONTROL eCPM] | 有效CPM，或指定日期範圍內每1000次曝光所支付的平均成本。 會針對CPM或CPC行銷活動計算eCPM值。 |
| [!UICONTROL EF Campaign ID] | 搜尋、Social和Commerce指派給行銷活動的數值ID。 |
| [!UICONTROL EF ID] | ([!UICONTROL Transaction Report]) (具有Adobe Advertising轉換追蹤服務的廣告商和具有權杖的&quot;[!UICONTROL EF Redirect]&quot;追蹤方法)點選或轉換的權杖。<ul><li>對於[!DNL Google Ads]個搜尋廣告，EF ID是`{gclid}:G:s`，其包含Google點按識別碼(GCLID)和網路型別（搜尋的網路&quot;）。</li><li> 對於[!DNL Microsoft Advertising]個搜尋廣告，EF ID是`{msclkid}:G:s`，其包含Microsoft點按識別碼(MSCLKID)和網路型別（搜尋的網路&quot;）。</li><li>若是其他廣告網路上的搜尋廣告，EF ID包含瀏覽者ID、點選時間和網路型別。</li><li>若是顯示廣告，EF ID包含瀏覽者ID、點選或曝光時間，以及網路型別。</li></ul> |
| [!UICONTROL EF Pixel Location ID] | ([!UICONTROL Geo Distribution Report]；僅供搜尋、社交和Commerce使用)地理位置的內部ID，用於標準化資料。 |
| [!UICONTROL EF Portfolio Group ID] | 投資組合所屬投資組合群組的數值ID。 |
| [!UICONTROL EF Search Engine ID] | 搜尋、Social和Commerce指派給廣告網路的數值ID： [!DNL Google Ads]的<i>[!UICONTROL 3]</i>、[!DNL Microsoft Advertising]的<i>[!UICONTROL 10]</i>、[!DNL Meta]的<i>[!UICONTROL 45]</i>、[!DNL Yahoo! Display Network]的<i>[!UICONTROL 86]</i>、[!DNL Naver]的<i>[!UICONTROL 87]</i>、[!DNL Baidu]的<i>[!UICONTROL 88]</i>、[!DNL Yandex]的<i>[!UICONTROL 90]</i>、[!DNL Yahoo! Japan Ads]的<i>[!UICONTROL 94]</i>、[!DNL Yahoo Native]的<i>[!UICONTROL 105]</i> （已棄用），或[!DNL Pinterest]的<i>[!UICONTROL 106]</i> （已棄用）。 |
| [!UICONTROL End Date] | 最後報告日期。 |
| [!UICONTROL Engagement Rate] | （影片廣告）參與次數除以廣告顯示次數。 |
| [!UICONTROL Engagements] | （影片廣告）使用者觀看您的廣告至少10秒的次數，或如果廣告不到10秒則為完整廣告。 |
| [!UICONTROL Est. Clicks] | （[!UICONTROL Geo Distribution Report]；僅限搜尋和顯示行銷活動）廣告群組/行銷活動/產品組合的預估點按次數。 此值可能與廣告網路提供的值不同。 |
| [!UICONTROL Estimated Cost] | Search、Social和Commerce已追蹤之相關廣告的總估計成本。 此值可能與廣告網路提供的值不同。 |
| [!UICONTROL Estimated Impressions] | （僅限顯示行銷活動） Search、Social和Commerce已追蹤的估計廣告曝光數。 此值可能與[!UICONTROL Impressions]欄的值不同（可用時），後者顯示廣告網路提供的值。 |
| [!UICONTROL Exclude (yes/no)] | 對於相符產品的廣告，是排除競標(<i>[!UICONTROL Yes]</i>)還是允許競標(<i>[!UICONTROL No]</i>)。 |
| [!UICONTROL First Page CPC] | (僅限Google行銷活動)指定日期範圍內出現在搜尋結果第一頁上的廣告每次點按成本(CPC)。 |
| [!UICONTROL Frequency] | （僅限[!DNL Meta]個行銷活動）某人檢視您廣告的平均次數。 |
| `GGL*`、`GGL_CT*`和`GGL_XD_CT*`個[[!DNL Google Ads]追蹤的轉換] | （[!DNL Google Ads]個搜尋和購物網路行銷活動） [!DNL Google Ads]個追蹤的轉換，每個轉換最多有三個個別的量度：<ul><li>`GGL*` — （當您追蹤時）關鍵字的轉換值，以「GGL」首碼開頭（例如GGL Purchase）。</li><li>`GGL_CT*` — 轉換次數（計數），以「GGL_CT」首碼開頭（例如GGL_CT_Purchase）。</li><li>`GGL_XD_CT*` — （當可用於轉換型別時，當您追蹤時）以「GGL_XD_CT_」首碼(例如GGL_XD_CT_Purchase)開頭的[!DNL Google Ads]所測量的跨裝置轉換次數（計數）。</li></ul><br>每個轉換都是依競標單位和點按日期來記錄；無法在事件層級使用。 如需有關[!DNL Google Ads]追蹤的轉換的詳細資訊，請參閱「搜尋、社交和Commerce中的[[!DNL Google Ads] 轉換資料](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」。 |
| [!UICONTROL Impr. (Abs. Top) %] | （僅限[!DNL Google Ads]）在自然搜尋結果上方顯示為第一個廣告的廣告印象百分比。 |
| [!UICONTROL Impr. (Top) %] | （僅限[!DNL Google Ads]）顯示在有機搜尋結果上方的廣告印象百分比。 |
| [!UICONTROL Impressions] | 指定日期範圍內的廣告曝光次數。 |
| [!UICONTROL Interaction Rate] | （視訊廣告）互動次數除以廣告顯示次數（視訊和縮圖曝光數）。 |
| [!UICONTROL Interactions] | （影片廣告）人們觀看您廣告的次數。 |
| [!UICONTROL Is_Click_Objectives] | ([!UICONTROL Portfolio Report]) <i>true</i> （當產品組合包含具有[!UICONTROL Maximize Clicks]競標策略的行銷活動時），否則<i>false</i>。 |
| [!UICONTROL Keyword] | 關鍵字。<br><br><b>注意：</b>如果報告在啟用內容的搜尋行銷活動中包含來自廣告群組的資料，則此欄會包含適用的廣告群組名稱，例如「（廣告群組內容）您的廣告群組名稱」。 對於搜尋促銷活動中的網站目標位置，此欄沒有值。 |
| [!UICONTROL Keyword ID] | 可識別現有關鍵字的唯一ID。 |
| [!UICONTROL Keyword Status] | 搜尋字詞符合的關鍵字狀態： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i>或<i>[!UICONTROL Disapproved]</i>。 |
| [!UICONTROL Label Classification] | （[!UICONTROL Label Classification Report]和[!UICONTROL Label Value Report]）標籤分類。 |
| [!UICONTROL Label Value] | （[!UICONTROL Label Classification Report]和[!UICONTROL Label Value Report]）標籤分類的值。 |
| [!UICONTROL Language] | （顯示行銷活動）目標對象語言。 |
| [!UICONTROL Link Type] | （[!UICONTROL Keyword Report]；[!DNL Google Ads]及[!DNL Microsoft Advertising]行銷活動；只有為報告指定的歸因規則為「最後一個事件」時，資料才可用）當資料列報告由於點選廣告副檔名（而不是廣告本身）或產品/購物廣告而導致的轉換時，此欄會顯示被點選的連結型別和標題：<ul><li>`pla:*` — 產品廣告列為`pla:<product ID>`，例如&quot;pla：8525822&quot;。</li><li>`sl:*` — 網站連結列為`sl:<Sitelink text>`，例如「sl：請參閱目前的選件」。</li></ul> |
| [!UICONTROL Listing Match Type] | 關鍵字元合廣告清單的型別、內容目標行銷活動中的廣告<i>[!UICONTROL Content]</i>或網站目標行銷活動中的版位<i>[!UICONTROL Sitecpc]</i>。 針對[!DNL Microsoft Advertising]關鍵字，這可能包含多個相符型別（例如&quot;[!UICONTROL Broad]，[!UICONTROL Exact]&quot;）。 |
| [!UICONTROL Location] | （顯示行銷活動）目標對象位置。 |
| [!UICONTROL Long Creative Title1] - [!UICONTROL Long Creative Title5] | （在[!DNL Microsoft Advertising]個回應式及多媒體廣告的已完成報表列中）廣告的長標題。 若要檢視這些欄，請在報表設定中加入&quot;[!UICONTROL Long Creative Titles]&quot;欄。 |
| [!UICONTROL Long Creative Titles] | （針對[!DNL Microsoft Advertising]個回應式與多媒體廣告）為每個廣告的長標題新增一欄（&quot;[!UICONTROL Long Creative Title1]&quot;到&quot;[!UICONTROL Long Creative Title5]&quot;）。 |
| [!UICONTROL Market Type] | 市場型別： <i>[!UICONTROL search]</i>或<i>[!UICONTROL social]</i> |
| [!UICONTROL Max Spend % Target] | （產品組合中具有[!UICONTROL ROI]、[!UICONTROL CPT]或[!UICONTROL Marginal Cost per Transaction]支出策略的行銷活動）產品組合的最大每日預算目標。 |
| [!UICONTROL Max Spend (%)] | ([!UICONTROL Network Constraint Report])為廣告網路設定的產品組合支出百分比上限。 對於使用限制型別&quot;[!UICONTROL Min-Max]&quot;的投資組合，這是[!UICONTROL Max %]值。 對於使用限制型別&quot;[!UICONTROL Target Spend]&quot;的投資組合，這是[!UICONTROL Target Spend]值。 |
| [!UICONTROL Method ID] | ([!UICONTROL Portfolio Report]) |
| [!UICONTROL Metro Code] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])做為曝光數或點按數來源的數值Metro代碼（例如Denver的us-751）。 這是根據搜尋使用者的IP位址所判斷。 |
| [!UICONTROL Min Spend (%)] | ([!UICONTROL Network Constraint Report])為廣告網路設定的投資組合最小支出百分比。 對於使用限制型別&quot;[!UICONTROL Min-Max]&quot;的投資組合，如果設定了[!UICONTROL Min %]，則這是[!UICONTROL Min %]值。 對於使用限制型別&quot;[!UICONTROL Target Spend]&quot;的投資組合，這是[!UICONTROL Target Spend]值。 |
| [!UICONTROL Network Account ID] | 由網路指派的帳戶ID。 |
| [!UICONTROL Network Ad Group ID] | 由網路指派的廣告群組ID。 |
| [!UICONTROL Network Campaign ID] | 網路指派的行銷活動ID。 |
| [!UICONTROL Network Campaign Objective] | （僅限[!DNL Meta]個行銷活動）行銷活動的目標。 |
| [!UICONTROL Objective Name] | 投資組合的目標。 |
| [!UICONTROL Objective Value] | 根據投資組合目前目標計算的總加權轉換。 |
| [!UICONTROL Objective Value Calculation] | 用於衍生目標值的計算。 |
| [!UICONTROL Outbound Clicks] | （僅限[!DNL Meta]個行銷活動）將使用者從[!DNL Meta]擁有的屬性移除的廣告內連結點選次數。 |
| [!UICONTROL Parent Product Groupings] | 父級產品群組的完整階層，層級之間有`>>` （例如`All Products>>CategoryL1=Animals`） （如適用）。 |
| [!UICONTROL Partition Type] | 產品群組的型別： <i>[!UICONTROL Sub-Division]</i> （父產品群組）或<i>[!UICONTROL Unit]</i> （具有競標的子產品群組的最低層級）。 |
| [!UICONTROL Path Position] | ([!UICONTROL Transaction Report])轉換路徑中事件的位置。 |
| [!UICONTROL Path Total] | ([!UICONTROL Transaction Report])路徑位置的事件總數。 |
| [!UICONTROL Portfolio] | 投資組合。 |
| [!UICONTROL Portfolio Count] | ([!UICONTROL Portfolio Report])與目標相關聯的投資組合數目。<!-- This count is different than what I see within the Objectives view. --> |
| [!UICONTROL Portfolio Group Name] | 投資組合所屬投資組合群組的名稱。 |
| [!UICONTROL Portfolio ID] | 數值投資組合ID。 |
| [!UICONTROL Portfolio Spend Strategy] | ([!UICONTROL Portfolio Report])投資組合的支出策略： <i>[!UICONTROL Daily]</i>、<i>[!UICONTROL Weekly]</i>、<i>[!UICONTROL Monthly]</i>、<i>[!UICONTROL ROI]</i>、<i>[!UICONTROL Day of week]</i>、<i>[!UICONTROL Day of month]</i>、<i>[!UICONTROL CPT]</i>、<i>[!UICONTROL Marginal CPT]</i>、<i>[!UICONTROL Google Target CPA]</i>或<i>[!UICONTROL Google Target ROAS]</i>。 |
| [!UICONTROL Portfolio Status] | 投資組合狀態：<ul><li><i>[!UICONTROL Optimize]：</i>最佳化功能正在收集相關行銷活動的點按和收入資料、建立用於最佳化的資料模型，以及最佳化出價、行銷活動預算和行銷活動競標策略目標（視最佳化型別和競標策略而定）。</li><li><i>[!UICONTROL Active]：</i>最佳化功能正在收集相關行銷活動的點按和收入資料，並正在模型化資料，但並未最佳化出價或行銷活動預算。</li><li><i>[!UICONTROL Inactive]：</i>最佳化功能正在收集相關行銷活動的點按資料以用於報表用途，但是它不會將資料模型化，也不會將競標或行銷活動預算最佳化。</li></ul> |
| [!UICONTROL Portfolio Target] | ([!UICONTROL Portfolio Report])投資組合的支出策略的每日目標。 對於每日/每月和一週/月的某天策略，會顯示當天的目標。 |
| [!UICONTROL Preferred Devices] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]行銷活動）廣告設定會將偏好設定授予<i>[!UICONTROL Mobile ads]</i>或<i>[!UICONTROL All ads]</i>。 |
| [!UICONTROL Product Group ID] | 廣告網路指派給產品群組的數值ID。 |
| [!UICONTROL Product Group Name] | 產品群組的名稱。 |
| [!UICONTROL Product Group Status] | 產品群組的狀態。 |
| [!UICONTROL Product Groupings] | 父級產品群組。 |
| [!UICONTROL Product ID] | （[!UICONTROL Keyword Report]； [!DNL Google Ads]產品清單廣告）與廣告一起顯示的產品識別碼。<br><br><b>注意：</b>只有當產品清單包含追蹤引數`ev_plx=<GMC product ID>`時，才會擷取識別碼，您必須在[!DNL Google Merchant Center]內新增該引數。 |
| [!UICONTROL Raw Transaction Data] | ([!UICONTROL Transaction Report])轉換量度的收入（例如1代表一個註冊，12代表一個12美元的訂單）。 如果多個競標單位具有相同的交易ID，則追蹤ID的收入會根據指定點按日期的點按次數（當點按資料可用時）分割。 |
| [!UICONTROL Reach] | （僅限[!DNL Meta]個行銷活動）至少看過一次您廣告的人數。 注意： [!DNL Meta]會每天對使用者設定檔的觸及範圍進行重複資料刪除，因此[!DNL Meta]和搜尋、社交及Commerce所報告的數字可能會有所不同。 |
| [!UICONTROL Region] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])曝光數或點按數源自的區域或美國/加拿大州。 這是根據使用者的IP位址所決定。 |
| [!UICONTROL SE Creative ID] | 由網路指派的廣告ID。 |
| [!UICONTROL Search (Abs. Top) IS] | （[!DNL Google Ads]和[!DNL Microsoft Advertising]）您從絕對頂端位置收到的曝光數（有機搜尋結果上方的第一個廣告）除以您有資格從頂端位置收到的預估曝光數。 低於10%的百分比會顯示為&quot;`<10%`&quot;或&quot;`0.0999`&quot;。 |
| [!UICONTROL Search (Top) IS] | （[!DNL Google Ads]和[!DNL Microsoft Advertising]）您在上層位置收到的曝光數（在有機搜尋結果上方）除以您有資格在上層位置收到的預估曝光數。 低於10%的百分比會顯示為&quot;`<10%`&quot;或&quot;`0.0999`&quot;。 |
| [!UICONTROL Search Engine] | 廣告網路。 |
| [!UICONTROL Search exact match IS] | 您收到的完全符合關鍵字的搜尋閱聽次數，除以您符合資格收到的預估完全符合閱聽次數。 如果此數字偏低，可能是因為您的出價太低，或是因為廣告品質或相關性太低。 |
| [!UICONTROL Search impr. share] | （僅限[!DNL Google Ads]）您收到的曝光數除以您符合資格接收的預估曝光數。 低於10%的百分比會顯示為「&lt;10%」，高於90%的百分比會顯示為「`>90%`」。 |
| [!UICONTROL Search lost abs. top IS (budget)] | （[!DNL Google Ads]和[!DNL Microsoft Advertising]）您的廣告不是優先於自然搜尋結果的時間百分比，因為您的每日或每月預算太低。 對於Google廣告行銷活動，超過90%的百分比會表示為&quot;`>90%`&quot;或&quot;`0.9001`&quot;。 |
| [!UICONTROL Search lost abs. top IS (rank)] | （[!DNL Google Ads]和[!DNL Microsoft Advertising]）由於廣告排名不佳，您的廣告不是優先於有機搜尋結果的時間百分比。 對於Google廣告行銷活動，超過90%的百分比會表示為&quot;`>90%`&quot;或&quot;`0.9001`&quot;。 |
| [!UICONTROL Search lost IS (budget)] | （僅限[!DNL Google Ads]）由於每日或每月預算太低，未顯示廣告的時間百分比。 此量度僅在行銷活動層級提供。 超過90%的百分比會顯示為&quot;`>90%`&quot;或&quot;`0.9001`&quot;。 |
| [!UICONTROL Search lost IS (rank)] | （僅限[!DNL Google Ads]）由於廣告排名不佳而未顯示廣告的時間百分比。 超過90%的百分比會顯示為&quot;`>90%`&quot;或&quot;`0.9001`&quot;。 |
| [!UICONTROL Search lost top IS (budget)] | （[!DNL Google Ads]和[!DNL Microsoft Advertising]）您的廣告未顯示在自然搜尋結果上方的時間百分比，因為您的每日或每月預算太低。 針對[!DNL Google Ads]行銷活動，超過90%的百分比會指示為&quot;`>90%`&quot;或&quot;`0.9001`&quot;。 |
| [!UICONTROL Search lost top IS (rank)] | （[!DNL Google Ads]和[！DNL [!DNL Microsoft Advertising]]）由於廣告排名不佳，您的廣告未顯示在有機搜尋結果上方的時間百分比。 對於Google廣告行銷活動，超過90%的百分比會表示為&quot;`>90%`&quot;或&quot;`0.9001`&quot;。 |
| [!UICONTROL Search Term] | ([!UICONTROL Transaction Report])使用者查詢的搜尋字詞。 |
| [!UICONTROL SETrackingOnly] | 您正在追蹤帳戶但未出價： <i>[!UICONTROL TRUE]</i>或<i>[!UICONTROL FALSE]</i>。 |
| [!UICONTROL Site] | （網域反向連結報表和[!UICONTROL Keyword Report]；網站目標位置）產生點按的網站。 |
| [!UICONTROL Start Date] | 報告的第一天。 |
| [!UICONTROL State] | （地理分佈報表，[!UICONTROL Keyword Report]）產生交易的狀態。 這是根據使用者的IP位址所決定。 |
| [!UICONTROL Surfer ID] | ([!UICONTROL Transaction Report])完成交易的使用者識別碼。 |
| [!UICONTROL Thru Plays] | （僅限[!DNL Meta]個行銷活動）完整觀看廣告的檢視次數。 |
| [!UICONTROL Top of Page CPC] | (僅限Google行銷活動)指定日期範圍內出現在搜尋結果頁面頂端的廣告每次點按成本(CPC)。 |
| [!UICONTROL Tracking URL] | （僅限以搜尋為目標的關鍵字）追蹤範本或內嵌有（如適用）搜尋、社交和Commerce追蹤程式碼的目標URL。 |
| [!UICONTROL Transaction Property Name] | ([!UICONTROL Transaction Report])交易貸記的廣告商特定轉換量度。 |
| [!UICONTROL Transaction Time] | ([!UICONTROL Transaction Report])將指定的轉換量度貸記的時間。 |
| [!UICONTROL Two Second Continuous Video Plays] | （僅限[!DNL Meta]個行銷活動）視訊播放至少連續兩秒的次數。 |
| [!UICONTROL User Account Type] | 已過時 |
| [!UICONTROL User SE Account ID] | Search、Social和Commerce指派給廣告網路的數值ID。 |
| [!UICONTROL Video Average Play Time] | （僅限[!DNL Meta]個行銷活動）單次曝光所播放視訊的平均時間，包括重新播放視訊所花費的時間。 |
| [!UICONTROL Video Plays] | （僅限[!DNL Meta]個行銷活動）視訊開始播放的次數，不含重播。 |
| [!UICONTROL Video Played at 25 Percent Count]、[!UICONTROL Video Played at 50 Percent Count]、[!UICONTROL Video Played at 75 Percent Count]和[!UICONTROL Video Played at 100 Percent Count] | （影片廣告）播放達25%、50%、75%或100%的影片數量。 |
| [!UICONTROL VideoQuartile25Rate]、[!UICONTROL VideoQuartile50Rate]、[!UICONTROL VideoQuartile75Rate]和[!UICONTROL VideoQuartile100Rate] | （影片廣告）影片播放達25%、50%、75%或100%的百分比。 |
| [!UICONTROL View Rate] | （視訊廣告）檢視或參與次數除以廣告顯示次數（視訊和縮圖曝光數）。 |
| [!UICONTROL Views] | （影片廣告）人們觀看或參與您廣告的次數。 |
| [!UICONTROL ViewThroughConversions] | （對象網路上的廣告）由一或多次曝光但無點按產生的轉換次數。 |

<!-- HOW IS MARKET TYPE DIFFERENT FROM CHANNEL TYPE? And what are all possible values for each? -->

>[!MORELIKETHIS]
>
>* [關於基本和進階報告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [產生基本或進階報告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [基本和進階報表設定](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
