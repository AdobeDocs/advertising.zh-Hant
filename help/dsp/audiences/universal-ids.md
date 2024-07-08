---
title: 支援啟用通用ID
description: 瞭解以下方面的支持：導入通用 ID 細分受眾群、創建自定義細分受眾群以跟蹤通用 ID，以及將第一方細分受眾群中的其他用戶標識符轉換至通用 ID，以便進行無 Cookie 目標定位。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# 支援啟用通用ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta功能*

DSP 支持以人為本的通用 ID，用于跨 DSP 支持的數位格式的無 Cookie 單裝置（非跨裝置）目標定位。

* 您可使用控制面板，[!DNL Connect][!DNL LiveRamp]手動將已驗證的 [[!DNL LiveRamp] [!DNL RampIDs]] 直接傳送至DSP。請參閱「[手動匯入已驗證的區段來源 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)」。

* DSP 可以引入由在 客戶 数据平台 （CDP） 中構建的哈希電子郵件 ID 組成的第一方細分，並將其轉換 ID [!DNL Unified ID 2.0 (UID2.0)] 和 [!DNL LiveRamp] [!DNL RampIDs] ID。有關支持的客戶數據平臺、每種支援的通用 ID 類型的可用功能以及相關工作流程的詳細信息，請參閱“[關於第一方受眾源](/help/dsp/audiences/sources/source-about.md)”。

* 您可以創建自定義細分受眾群來跟蹤與 ID5 通用 ID 關聯的使用者，這些使用者接觸到來自桌面和移動裝置的廣告，以及造訪特定網頁的使用者。 ID5 使用概率模型來分配從各種用戶信號和瀏覽器信號派生的 ID。 有關說明，請參閱「[建立和實施自定義區段](/help/dsp/audiences/custom-segment-create.md)」。

* 除了通過 Cookie 或裝置 ID 追蹤的使用者之外，某些供應商提供的第三方細分可能會自動包含通用 ID。 例如，來自 [!DNL Eyeota] 的區段可能自動包含ID5 ID，而來自的 [!DNL Lotame] 區段可能包含UID2.0 ID。 區段詳細信息包括每種類型的大小。 每個區段的通常使用費（在區段名稱旁邊註明）適用;ID5 ID不收取額外費用。

## 依通用 ID 類型傳送報表

* **自定義報告：** 自定義報告中提供了按通用 ID 類型劃分的成本、印象、點擊、轉換和頻率數據。

* **[!DNL Analytics]報表：** 已實施所有必要步驟的廣告客戶 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 可以在 中 [!DNL Analytics]查看按通用 ID 類型進行的視圖式轉化。

  >[!IMPORTANT]
  >
  >為了正確轉換 歸因，請確保廣告的點進 URL 同時 [包含 EF ID 和 AMO ID](/help/integrations/analytics/ids.md)。

* **細分受眾群詳細信息：** 對於所有區段類型，區段詳細信息包括按通用 ID 類型和 Cookie 或裝置 ID 跟踪的裝置類型對象大小。

## 如何在版位中Target通用ID物件

>[!NOTE]
>
>您無法變更即時刊登中的目標 ID 類型。 如有必要，您可以重複即時刊登並在新刊登中更改目標 ID 類型。

在新、已排程或暫停的刊登中，執行以下操作：

1. 在本節中 [!UICONTROL Geo-Targeting] ，指定要目標的地理區域。 每個通用 ID 合作夥伴僅允許在特定地理區域使用用戶 目標定位，並且設置中 [!UICONTROL Targeting] 僅提供符合條件的 ID 類型。

1. 在本節中 [!UICONTROL Audience Targeting] ，執行以下操作：

   1. 在設定中 [!UICONTROL Included Audiences] ，選取用戶數據已轉換為通用 ID 的區段。

      如有需要，您可以包含其他區段。

   1. 在設定中 [!UICONTROL Targeting] ：

      1. 選取要目標的通用 ID 類型。

         設定包括選項 “[!UICONTROL Legacy IDs]” 和 “[!UICONTROL Universal ID]，” 其中可能包括子選項 “[!UICONTROL ID5]”、“[!UICONTROL RampID]，” 和 “[!UICONTROL Unified ID2.0].” 選定的地理目標決定了可用的子選項。

         您可以同時選取「[!UICONTROL Legacy IDs]」與「[!UICONTROL Universal ID]」，但每刊登只能選取一種通用 ID。 當您同時選取舊版ID和通用ID時，競標優先權會優先投給通用ID。

      1. （如有需要）接受使用通用 ID 的服務條款協定。

         在將數據轉換到新的 ID 類型之前，DSP 帳戶中的用戶必須接受服務條款協定。 每種 ID 類型、每種帳戶只能接受一次條款。

請參閱“[放置設定](/help/dsp/campaign-management/placements/placement-settings.md)”。

## 測試與數據驗證的最佳實務

對於可使用Adobe Analytics測量的區段和ID5型區段，請使用 [!DNL RampID]下列最佳作法。

* 激活區段后約 24 小時，請在 > [!UICONTROL All Audiences]內[!UICONTROL Audiences]檢查區段的轉換后 ID 計數。如果ID計數意外，請連絡Adobe Systems帳戶團隊。

  有關區段計數如何變化的詳細資訊，請參閱「[電子郵件 ID 和通用 ID](#universal-ids-data-variances) 之間數據差異的原因」。

* 不要更改現有的包和版位。 但是，如果您沒有任何增量預算來測試通用 ID，請減少原始預算以資助測試。

* 複製原始套餐和展示位置，根據測試的大小調整預算，將受眾群體更改為使用 [!DNL RampID]基於 ID5 的細分受眾群（適用於經過身份驗證的使用者）或基於 ID5 的細分受眾群（適用於未經身份驗證的使用者），並驗證新套餐和展示位置是否用完了全部預算。

   * 要將基於通用 ID 的細分的效果與其他對象標識符（例如 Cookie 或 行動裝置廣告 ID）目標定位展示位置的效果進行比較，請創建一個具有單獨的基於 ID 的通用刊登和基於舊版 ID 的刊登的行銷活動。

     要獲得完整的重定向測試，請為經過身份驗證的使用者目標 RampID，為未經身份驗證的使用者 ID5。

     獲得最佳性能不應是主要的比較。 相反，請確定哪些 ID 可以很好地擴展，這可能會在以後為您的優化和預算分配提供資訊。 長期目標是彌補損失的印象，並在 cookie 淘汰時網站流量。

   * 要比較總瀏覽器覆蓋面，請在同一刊登中目標通用的基於ID的細分受眾群和基於舊版ID的細分受眾群。 使用与上一個用例相同的行銷活動設置，但您無需分攤行銷活動預算。

     出價優先權授予通用 ID，但當通用 ID 不可用時，舊版 ID 會收到出價。 請務必比較不同瀏覽器 （包括 鉻黃、Safari 和 Mozilla） 的覆蓋面。

     >[!NOTE]
     >
     >頻次上限適用於個別ID。 當用戶具有多種 ID 類型時，您達到該用戶的數量可能會超出預期。

* 請記住，經過身份驗證對象細分受眾群的覆蓋面自然小於基於Cookie細分受眾群的覆蓋面，使用其他目標定位選項會進一步縮小您的覆蓋面。 謹慎使用精細目標定位，尤其是將多個目標與 AND 語句聯接在一起時。

## 電子郵件ID和通用ID之間數據差異的原因 {#universal-ids-data-variances}

* 經過哈希處理的電子郵件ID翻譯為ID5 ID：

  概率模型的誤差變數為 +/- 5%。 這意味著它可以高估或低估 5% 的對象計數。

* 經過哈希處理的電子郵件 ID 翻譯為 [!DNL RampIDs]：

   * 當多個配置文件使用相同的电子郵件 ID 時，DSP 區段計数可能低於 客戶 数据平台中的設定檔計数。 例如，在 Adobe Photoshop 中，您可以使用單個電子郵件 ID 建立公司 帳戶和個人帳戶。 但是，如果兩個配置檔都屬於同一個人，則配置檔映射到一個電子郵件ID，並相應地映射到一個 [!DNL RampID]。

   * A [!DNL RampID] 可以升級為新值。 如果 [!DNL LiveRamp] 無法識別電子郵件 ID 或無法將其映射到其資料庫中的現有 [!DNL RampID] ID，則會為電子郵件 ID 分配一個新 [!DNL RampID] ID。 將來，當他們可以將電子郵件ID映射到另一個 [!DNL RampID] ID或可以收集有關同一電子郵件ID的更多資訊時，他們會將其升級 [!DNL RampID] 為新值。 [!DNL LiveRamp]將此操作稱為從「派生」[!DNL RampID]升級到「維護」。 [!DNL RampID]但是，DSP 不會獲取派生和維護 [!DNL RampIDs] 之間的映射，因此無法從DSP 區段中刪除以前版本的 RampID。 在這種情況下，區段計数可能大於設定檔計数。

     範例： 一位用戶登 [!DNL Adobe] 入網站並流覽Photoshop 頁面。 如果沒有 [!DNL LiveRamp] 關於電子郵件ID的任何現有資訊，那麼他們會為其分配一個派生 [!DNL RampID]的，比如D123。 15天后，用戶訪問了同一頁面，但在 [!DNL LiveRamp] 這15天內進行了升級 [!DNL RampID] ，並重新分配給 [!DNL RampID] 了M123。 儘管客戶數據平台的區段“Photoshop Enthusiast”只有一個用戶电子郵件ID，但DSP 區段有兩個RampID：D123和M123。

## 疑難排解

如果您沒有看到用戶計數，或者對象尺寸較小，請檢查以下內容：

* 如果您使用 [!DNL Flashtalking] 或 [!DNL Google Campaign Manager 360] 廣告，請確保廣告的點擊後進 URL 附加了正確的宏。 請參閱廣告](/help/integrations/analytics/macros-flashtalking.md)和[[!DNL Google Campaign Manager 360] 廣告](/help/integrations/analytics/macros-google-campaign-manager.md)的[[!DNL Flashtalking] 宏。

* 確保在您的網站上實施正確的通用 ID 合作夥伴專用代碼，以匹配現場事件和廣告曝光。 視需要與您或[!DNL ID5]代表合作[!DNL LiveRamp]。

* （For [!DNL RampIDs] and [!DNL UID 2.0] ID） 請確認您的 [DSP 資料來源配置正確](/help/dsp/audiences/sources/source-manage.md#source-settings)，且已為產生的對象區段填入用戶計數。

* 如果您的覆蓋面低於預期，請檢查對象區段邏輯是否不太精細。

* 確保您的行銷活動、套餐和刊登設置正確無誤。<!-- wording-->

如果您無法解決問題，請與Adobe Systems客戶團隊聯繫。

>[!MORELIKETHIS]
>
>* [關於第一方受眾來源](/help/dsp/audiences/sources/source-about.md)
>* [管理物件來源以啟動通用ID Audiences](/help/dsp/audiences/sources/source-manage.md)
>* [建立和實施自定義區段](/help/dsp/audiences/custom-segment-create.md)
>* [手動匯入已驗證的區段，來源： [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [關於觀眾管理](/help/dsp/audiences/audience-about.md)
>* [版面設定](/help/dsp/campaign-management/placements/placement-settings.md)
