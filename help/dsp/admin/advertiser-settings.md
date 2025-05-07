---
title: 廣告商帳戶設定
description: 請參閱可用廣告商設定的說明。
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# 廣告商帳戶設定

*不適用於唯讀使用者*

<!-- Not published -->

## [!UICONTROL General]設定

**[!UICONTROL Advertiser Name]：**&#x200B;廣告商名稱。

**[!UICONTROL Category]：**&#x200B;廣告商業務營運的類別。 當您競標詳細目錄時，會將類別傳達給發佈者。 請務必選擇與廣告一致的類別，否則發佈者可能會拒絕您的廣告。

>[!NOTE]
>
>如果您選取&#x200B;*[!UICONTROL Other]*，則廣告商無法存取DSP [!DNL On Demand Inventory]。

**[!UICONTROL Advertiser URL]：**&#x200B;廣告商的首頁或主要網站URL （以`http://`或`https://`開頭）。

**[!UICONTROL Share all private exchange feeds into this advertiser]：** （僅限新廣告商帳戶）讓廣告商可以使用為組織的DSP帳戶設定的所有私人Exchange摘要。

### [!UICONTROL Adobe IMS IDs]

使用其他Adobe Experience Cloud產品的廣告商，可以使用組織在Experience Cloud中使用的唯一ID，在某些產品間共用資料。 您可以在[!UICONTROL Integrations]區段中設定特定的產品整合。

**[!UICONTROL Account IMS org and ID]：** (廣告商具有其他Experience Cloud產品，這些產品是透過具有多個廣告商的Experience Cloud帳戶所授權；選用)廣告商的Experience Cloud組織ID。

**[!UICONTROL Advertiser IMS org and ID]：** (具有其他Experience Cloud產品的直接授權的廣告商；選擇性)廣告商的Experience Cloud組織ID。

### [!UICONTROL Integrations]

（選用）連結至DSP帳戶的其他Experience Cloud產品。 產品必須與[!UICONTROL Adobe IMS IDs]區段中提供的相同Experience Cloud組織ID相關聯。

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]：** (具有[!DNL Advertising Search, Social, & Commerce]或使用Adobe Advertising轉換畫素的廣告商) DSP與其交換歸因資料的[!DNL Search, Social, & Commerce]帳戶。

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]：** (使用Adobe Analytics的廣告商；選用；僅適用於使用Adobe Advertising轉換追蹤標籤（僅包含[!DNL EF Redirect]和權杖）收集的資料)一或多個[!DNL Analytics]報告套裝，DSP會將其從發佈者和供應方合作夥伴收集的資料，傳送至這些報告套裝。 Analytics也會將其從使用者端網站收集到的資料傳送至DSP。

若要讓資料顯示在報表套裝中，必須啟用適當的[!DNL Search, Social, & Commerce]廣告商層級設定。 此外，廣告商的[!DNL Analytics]帳戶必須設定為從Adobe Advertising接收資料。

>[!WARNING]
>
>如果您移除先前連結的報表套裝，DSP將不再與該套裝交換資料。 可能會看到資料波動。

如需與[!DNL Analytics]整合的詳細資訊，請參閱「[總覽 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)」。

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]：** (使用Adobe Audience Manager或Adobe Analytics的廣告商；選用) Audience Manager或[!DNL Analytics]帳戶，DSP會從中提取廣告商所有Adobe對象的區段中繼資料、階層資料和唯一對象資料。 這包含下列專案的資料：

* Audience Manager區段
* 發佈至Adobe Experience Cloud的[!DNL Analytics]區段
* 使用Adobe Experience Cloud [!DNL Audience Library]建立的區段
* 在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe Advertising的區段

初始同步處理大約需要24小時。 之後，資料會即時同步，延遲一到兩秒。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting]設定

您可以選擇為廣告商的新版位設定預設目標。 使用者可以覆寫任何新位置的預設目標。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]：**&#x200B;每個位置之地理定位的預設國家/地區。 使用者可以變更國家/地區，並針對每個位置設定更具體的地理定位。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]：**&#x200B;預設要隱藏的任何對象或區段。 使用者可以變更每個位置的排除專案。

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

要套用的[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]內容篩選器的型別。 您可以在[位置層級](/help/dsp/campaign-management/placements/placement-settings.md)覆寫廣告商層級設定。

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]：** （選擇性）一或多個預設要封鎖的詳細目錄內容型別。 可能需支付額外費用。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]：** （選擇性）預設要鎖定的一或多個庫存屬性型別。 可能需支付額外費用。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]：** （選擇性）預設要封鎖的一或多個庫存屬性型別。 可能需支付額外費用。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]：** （選擇性）預設要封鎖廣告的成人內容程度： *[!UICONTROL Do Not Block]* （預設）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需支付額外費用。

**[!UICONTROL Alcohol Content]：** （選擇性）預設要封鎖廣告的酒精內容程度： *[!UICONTROL Do Not Block]* （預設）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需支付額外費用。

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

根據透過[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]測量的詐騙流量和可疑活動而封鎖的網站型別。 您可以在[位置層級](/help/dsp/campaign-management/placements/placement-settings.md)覆寫廣告商層級設定。

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：**&#x200B;依預設，會封鎖所有100%無效的流量（包括被劫持裝置上的流量），以供新位置使用。 可能需支付額外費用。

**[!UICONTROL Also block sites with]：** （選擇性）額外的詐騙和無效流量層級，會導致DSP依預設封鎖廣告： *[!UICONTROL None]* （預設值，不會封鎖額外的流量）、*[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、*[!UICONTROL >4% Average Fraud/IVT levels]*、*[!UICONTROL >6% Average Fraud/IVT levels]*、*[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或&#x200B;*[!UICONTROL >25% Average Fraud/IVT levels]*。 可能需支付額外費用。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]：** （選擇性）一或多個欺詐型別，預設會導致DSP封鎖廣告： *[!UICONTROL Fraud]* （會封鎖所有有欺詐的網站）、*[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;及/或&#x200B;*[!UICONTROL Fraud: Zero Ads]*。 可能需支付額外費用。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]：** （選擇性）可導致DSP預設封鎖廣告的可疑網站或應用程式活動型別： *[!UICONTROL None]* （預設，不會根據可疑活動封鎖廣告）、*[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或&#x200B;*[!UICONTROL Suspicious Activity - High or Moderate Risk]*。 可能需支付額外費用。

#### [!UICONTROL Pre-Bid Viewability]

依[!DNL DoubleVerify]和[!DNL Integral Ad Science]選擇性的競標前可見性篩選器，可套用至位置。 針對新版位選取廣告商層級預設值。 您可以在[位置層級](/help/dsp/campaign-management/placements/placement-settings.md)覆寫廣告商層級設定。

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### 影片

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]**。 使用此選項，選取條件。

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]**。 使用此選項，選取條件。

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average player size composition is]**。 使用此選項，選取條件。

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### 顯示

**&#x200B; **&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**。 使用此選項，選取條件。

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**。 使用此選項，選取條件。

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

選用的&#x200B;**[!UICONTROL Video Viewability Targets]**&#x200B;篩選器和選用的&#x200B;**[!UICONTROL Display Viewability Targets]**&#x200B;篩選器。 可能需支付額外費用。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]：**&#x200B;依預設，利用每個發行者的[!DNL Authorized Digital Sellers]清單來使用哪個層級的[[!DNL Ads.txt] 競標前篩選](https://iabtechlab.com/ads-txt-about/)：
* *[!UICONTROL Opt out of ads.txt (default)]*：向所有賣家購買詳細目錄。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：優先從網域的授權直銷商和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：僅從網域的授權直接銷售者和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：只從網域的授權直銷商購買詳細目錄。

您可以在[位置層級](/help/dsp/campaign-management/placements/placement-settings.md)覆寫廣告商層級設定。

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]：**&#x200B;依預設，會啟用即時、競標後篩選條件，以確保廣告可在廣告商鎖定的網站上提供。<!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]：** （僅限[!DNL DoubleVerify]個客戶；選用）與組織的[!DNL DoubleVerify]帳戶相關聯的[!DNL DoubleVerify Authentic Brand Safety]區段ID，預設用於所有位置。 指定ID會使用針對指定區段ID設定的自訂品牌安全規則，封鎖出價後的曝光數。 DSP會為帳戶開立帳單，以取得區段ID的使用量。

ID必須以「51」開頭，且包含8位數。 您可以在位置層級變更或刪除廣告商層級ID。

>[!MORELIKETHIS]
>
>* [建立廣告商帳戶](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
