---
title: 品牌安全與媒體品質
description: 進一步瞭解品牌安全和媒體品質功能。
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: e8cb734e313b6aecfb75dfcbf70347efe83254a5
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# 品牌安全與媒體品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP提供一套品牌保護功能，以確保您的每個行銷活動在品牌安全的環境中都能觸及真正的使用者。

我們的詐騙監控團隊與業界領先的合作夥伴密切合作，例如 [!DNL Interactive Advertising Bureau]， [!DNL Trust and Accountability Group] [!DNL (TAG)]、和 [!DNL WhiteOps]，以謹慎組織我們平台上的詳細目錄。 透過主動管理我們的供應，DSP可確保平台上的所有廣告商都免受非人為流量（機器人、編目程式、資料中心流量和詐騙）的影響，並僅在品牌安全的環境中提供。

除了提供中央品質管理之外，我們相信可讓廣告商設計符合其品牌的控制項。 DSP提供與整合 [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]， [!DNL Oracle Data Cloud]、和 [!DNL Peer39]，確保每個廣告商都能選擇其所需的詐騙防護、情境式篩選和關鍵字鎖定目標等級。

## 品質方案

### 使用進行詳細目錄驗證 [!DNL Ads.txt] 支援

[[!DNL Ads.txt]，代表 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) 是推出的計畫，由 [!DNL Interactive Advertising Bureau] ([!DNL IAB])，以利在公開市場上適當地呈現詳細目錄，從而打擊非法的流量來源和網域詐騙。 參與的發行商和經銷商公開宣佈獲授權銷售其數位庫存的公司，以及這些關係的性質，方法是 `ads.txt` 網域最上層的頁面(例如 `example.com/ads.txt`)。

DSP支援 [!DNL ads.txt] 藉由讀取每個發行者的 `ads.txt` 檔案，並可讓您選擇僅向已驗證的購買 [!DNL ads.txt] 賣家。 例如，透過比對銷售商，我們看到存取 `nytimes.com` 敬紐約時報&#39; `ads.txt` 檔案中，我們可以識別哪些是合法的，哪些是非法的，如果位置設定為僅向經過驗證的賣家購買，我們會封鎖違規者。 <!-- can we actually mention NY Times? -->

您可以設定預設值 [!DNL ads.txt] 每個廣告商的控制項<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後（選擇性） [自訂每個位置的設定](/help/dsp/campaign-management/placements/placement-settings.md) 至：

* 僅向網域的授權直銷商購買詳細目錄

* 僅向網域的授權直銷者和經銷商購買詳細目錄

* 優先從網域的授權直接銷售者和經銷商購買詳細目錄

* 從所有賣家購買詳細目錄

### 平台詐騙監視

DSP已建立強大的內部工具與系統，與業界領先廠商(例如 [!DNL Whiteops] 和 [!DNL Integral Ad Science].

此外，Adobe與 [!DNL IAB] 和 [!DNL TAG] 利用如下的工具，確保強大的產業標準詐騙封鎖功能以保護我們的廣告商 [!DNL ads.txt] （請參閱上一節）、 [!DNL IAB] 機器人和編目程式清單，以及 [!DNL TAG] 資料中心IP清單。

透過我們多維度的品質方法，團隊可監控異常和無效的流量模式，確保受保護庫存的無效流量不會超過3%。 任何可疑的詳細目錄（包括特定網域的詳細目錄或來自特定發行商或銷售商的詳細目錄）會立即在平台上封鎖。

### 存貨對應、分層及分類

清查對應是新清查新增到我們的平台之前，所有新清查都需要進行的詳細稽核和上線流程。 此程式旨在確保DSP上所有存貨的安全性與品質。

* **對應：** 我們的詳細目錄團隊會仔細檢閱每個網域，並評估以下方面：

   * 品牌安全

   * 廣告型別驗證

   * 通用內容、重複網域和假廣告服務

* **分層：** 我們全面檢查品牌在整個生態系統的存在，以分類不同階層的詳細目錄。 您可以 [將目標定位到您的位置](/help/dsp/campaign-management/placements/placement-settings.md) 至這些層級，以獲得所需的觸及率：

   * **[!UICONTROL T1]**  — 國際知名品牌網站

   * **[!UICONTROL T2]**  — 美觀的網站，既具最新狀態，沒有使用者產生的內容，且通常缺乏全球知名度

   * **[!UICONTROL T3]**  — 使用者產生的內容和細分內容

* **網站分類：** 為確保內容輕鬆鎖定和封鎖，我們會根據屬性的內容，使用DSP定義的網站類別來標籤每個屬性。 您可以 [針對每個位置鎖定或排除這些網站類別](/help/dsp/campaign-management/placements/placement-settings.md) 根據位置目標。

### 網站封鎖的完整支援

DSP提供全域封鎖網站清單，以及可建立廣告商和帳戶自訂封鎖網站清單的選項。

#### DSP全域封鎖的網站清單 {#global-blocked-sites}

DSP會維護全球封鎖的網站清單，列出被認為不安全的網站，以便在其上執行廣告。 此清單包含含有令人反感內容（例如仇恨或恐怖）的網站，以及受到機器人、假前置式廣告、不相符的網域和其他詐騙活動感染的網站。

在我們根除詐騙廣告商之活動的品牌安全方案中，所有網站都會使用圖表封鎖網站清單中的措施進行篩選。 所有未通過品牌安全檢查的網站都會新增至全域封鎖的網站清單。 由於DSP會以動態方式管理此清單，因此網站可隨時根據最新的品牌安全分析來開啟或關閉清單。

當您在全域封鎖的網站清單中加入網站作為版位目標時，該網站會以紅色驚歎號(！)標示。 這表示廣告不會在已標幟的網站上執行。

>[!NOTE]
>
>您可以選擇啟用「 」，略過附加至受信任私人交易的標準顯示廣告的全域封鎖網站清單[!UICONTROL Allow unscreened sites]中的「 」選項 [位置設定](/help/dsp/campaign-management/placements/placement-settings.md). 如有必要，Adobe帳戶團隊還可以選擇在交易的發佈者設定中，針對公開（拍賣層級）交易停用網站封鎖。

#### 帳戶層級和廣告商層級的封鎖網站清單

使用者還可以維護帳戶層級和廣告商層級的封鎖網站清單<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->，這些都會自動用於所有版位。 除了全域封鎖的網站清單之外，還會套用較低層級的封鎖網站清單。

## 協力廠商整合

### 內容篩選

內容篩選可讓您根據廣告將提供的頁面內容，鎖定或封鎖廣告商機。 Adobe透過與業界領先廠商的整合提供內容篩選： [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39]. 目前篩選的範例包括 [!UICONTROL Adult Content]， [!UICONTROL Natural Disasters]， [!UICONTROL Legal Drinking Age]， [!UICONTROL MANGA]， [!UICONTROL Epidemics]、和 [!UICONTROL G-rated Sites].

您可以為每個廣告商設定預設內容篩選控制項<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後（選擇性） [自訂每個位置的設定](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能時可能需支付額外費用。

![Comscore標誌](/help/dsp/assets/comscore-logo.png) ![DoubleVerify標誌](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science標誌](/help/dsp/assets/ias-logo.png) ![Peer39標誌](/help/dsp/assets/peer39-logo.png)

### 競標前詐騙封鎖

善用我們的協力廠商整合，與 [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39] 以封鎖來自行銷活動的非人類流量。 這些整合提供領先業界的競標前封鎖功能，將行銷活動中的一般和複雜無效流量（GIVT和SIVT）減至最少。

您可以為每個廣告商設定預設的競標前詐騙封鎖控制項<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後（選擇性） [自訂每個位置的設定](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能時可能需支付額外費用。

如需功能的詳細資訊，請直接連絡您偏好的廠商，或連絡您的Adobe客戶團隊。

![DoubleVerify標誌](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science標誌](/help/dsp/assets/ias-logo.png) ![Peer39標誌](/help/dsp/assets/peer39-logo.png)

### 競標前可見性 {#pre-bid-viewability}

由我們領先業界的合作夥伴提供支援的競標前可檢視度篩選器 [!DNL DoubleVerify]， [!DNL Oracle Advertising] ([!DNL Moat])，以及 [!DNL Integral Ad Science] 允許廣告商確保其行銷活動在視訊和顯示內容中符合其想要的可檢視度效能目標。

您可以為每個廣告商設定預設可檢視度篩選器<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後（選擇性） [自訂每個位置的設定](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能時可能需支付額外費用。

![DoubleVerify標誌](/help/dsp/assets/doubleverify-logo.png) ![oracleAdvertising標誌](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science標誌](/help/dsp/assets/ias-logo.png)

### 注意力目標定位和測量

[!DNL Adobe's] 合作關係 [!DNL Adelaide] 為廣告商提供Adelaide量度的支援»[!DNL Attention Units]，會根據眼睛追蹤、曝光和結果資料測量媒體品質。

[位置層級競標前注意目標定位](/help/dsp/campaign-management/placements/placement-settings.md) 可讓廣告商鎖定特定的關注層級，以改善客戶參與度。

此外，廣告商可啟用 [位置層級的追蹤 [!UICONTROL Attention Score] 量度](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (加權平均數 [!DNL Attention Units] 跨曝光數)，以瞭解哪些置入策略產生最佳業務結果。

每項獨立功能需額外付費。

### 主題目標定位

DSP主題鎖定目標可讓您利用我們領先業界的情境式合作夥伴，鎖定或封鎖關鍵字清單 [!DNL Comscore] 和 [!DNL Oracle Data Cloud] (先前稱為 [!DNL Grapeshot])。 主題鎖定目標可協助您確保廣告始終在符合您品牌的環境中提供，包括封鎖有害內容或確保在可確保產生更大結果的環境中花費。

主題鎖定目標需要您直接與合作夥伴平台建立自訂主題區段。 建立區段後，您可以 [在中鎖定或排除區段ID [!UICONTROL Audience Targeting] 每個位置的區段](/help/dsp/campaign-management/placements/placement-settings.md). 此功能可能需支付額外費用。

若要建立自訂主題區段：

* 若要建立 [!DNL Comscore] 帳戶並建立自訂區段，您可以要求登入 [!DNL Activation Segment Manager] 在 [https://agents.comscore.com](https://agents.comscore.com). 請參閱 [[!DNL Comscore] 說明中心](https://comscoreactivation.zendesk.com/hc/) 以取得設定自訂區段的完整指示。 自訂區段的費用可見於 [!DNL Segment Manager] 當您建立它們時。

* 開始使用 [!DNL Oracle Data Cloud]，連絡人 [!DNL Oracle Data Cloud] 或您的Adobe客戶團隊。

![Comscore標誌](/help/dsp/assets/comscore-logo.png) ![Grapeshot標誌](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP已與 [!DNL DoubleVerify] 提供其 [!DNL Authentic Brand Safety] 目標定位解決方案，可讓您建立一組集中的品牌安全需求，以針對所有購買平台達成一致性。

一旦您建置 [!DNL DoubleVerify] 品牌安全區段與必要的鎖定目標，您可以在DSP中使用它，以跨網路環境使用競標前來複製您的競標後區塊規則。

您可以指定 [!DNL DoubleVerify] 每個廣告商的區段ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後（選擇性） [啟用或停用 [!UICONTROL Authentic Brand Safety] 適用於每個位置](/help/dsp/campaign-management/placements/placement-settings.md). DSP會針對節段ID的用途開立科目帳單。

如需功能的詳細資訊，請連絡 [!DNL DoubleVerify] 直接或聯絡您的Adobe客戶團隊。

![DoubleVerify標誌](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
