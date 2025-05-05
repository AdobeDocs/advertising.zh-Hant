---
title: 支援啟用通用ID
description: 瞭解匯入通用ID區段、建立自訂區段以追蹤通用ID以及將第一方區段中的其他使用者識別碼轉換為通用ID以進行無cookie定位的相關支援。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 202f4ae8e6633672b7af12937f0b35da5052f7fc
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# 支援啟用通用ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta功能*

DSP支援以人物為基礎的通用ID，以用於DSP支援的數位格式無cookiless、single-device (not cross-device)目標定位。

* 您可以使用[!DNL LiveRamp] [!DNL Connect]儀表板，直接手動將已驗證的[[!DNL LiveRamp] [!DNL RampIDs]]傳送至DSP。 請參閱&quot;[從 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手動匯入已驗證的區段。&quot;

* DSP可以擷取您的第一方區段(由您客戶資料平台(CDP)內建的雜湊電子郵件ID所組成)，並將其轉換為[!DNL LiveRamp] [!DNL RampIDs]和[!DNL Unified ID 2.0 (UID2.0)] ID。 如需關於受支援客戶資料平台、每種受支援通用ID型別的可用功能及相關工作流程的詳細資訊，請參閱[關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)。

* 您可以建立自訂區段，以追蹤哪些使用者與ID5通用ID相關聯，且接觸到桌上型電腦和行動裝置上的廣告，以及造訪特定網頁。 ID5會使用機率模型來指派衍生自各種使用者訊號和瀏覽器訊號的ID。 如需指示，請參閱&quot;[建立及實作自訂區段](/help/dsp/audiences/custom-segment-create.md)&quot;。

* 除了Cookie或裝置ID所追蹤的使用者外，某些廠商的第三方區段可能會自動包含通用ID。 例如，來自[!DNL Eyeota]的區段可能會自動包含ID5 ID，而來自[!DNL Lotame]的區段可能會包含UID2.0 ID。 區段詳細資訊包括每種型別的大小。 每個區段的一般使用費（列在區段名稱旁）適用；ID5 ID不需額外付費。

## 依通用ID型別建立報表

* **自訂報告：**&#x200B;自訂報告中提供依據通用ID型別的成本、曝光數、點選數、轉換數和頻率資料。

* **[!DNL Analytics]報告：**&#x200B;具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)且已實作所有必要步驟的廣告商可以在[!DNL Analytics]中看到依據通用ID型別的瀏覽轉換。

  >[!IMPORTANT]
  >
  >如需正確的轉換歸因，請確定廣告的點進URL同時包含[EF ID和AMO ID](/help/integrations/analytics/ids.md)。

* **區段詳細資料：**&#x200B;對於所有區段型別，區段詳細資料包含依通用ID型別以及依Cookie或裝置ID追蹤的裝置型別的對象人數。

## 如何在位置中鎖定通用ID對象

>[!NOTE]
>
>您無法在即時位置中變更目標ID型別。 如有必要，您可以複製即時版位，並在新版位中變更目標ID型別。

在新的、已排程或已暫停的位置中，執行下列動作：

1. 在[!UICONTROL Geo-Targeting]區段中，指定要鎖定的地理區域。 每個通用ID合作夥伴只允許在特定地理區域中使用者鎖定目標，[!UICONTROL Targeting]設定中只有符合資格的ID型別可用。

1. 在[!UICONTROL Audience Targeting]區段中，執行下列動作：

   1. 在[!UICONTROL Included Audiences]設定中，選取要為其將使用者資料轉換為通用ID的區段。

      如有需要，您可以包含其他區段。

   1. 在[!UICONTROL Targeting]設定中：

      1. 選取要定位的通用ID型別。

         設定包含選項&quot;[!UICONTROL Legacy IDs]&quot;和&quot;[!UICONTROL Universal ID]&quot;，其中可能包含子選項&quot;[!UICONTROL ID5]&quot;、&quot;[!UICONTROL RampID]&quot;和&quot;[!UICONTROL Unified ID2.0]&quot;。 選取的地理目標會決定可用的子選項。

         您可以同時選取&quot;[!UICONTROL Legacy IDs]&quot;和&quot;[!UICONTROL Universal ID]&quot;，但每個位置只能選取一種型別的通用ID。 當您同時選取舊有ID和通用ID時，會為通用ID指定競標偏好設定。

      1. （如有必要）接受使用通用ID的服務合約條款。

         您必須先接受DSP帳戶的使用者服務合約條款，才能將資料轉換為新的ID型別。 每個帳戶的每個ID型別只能接受一次條款。

請參閱[位置設定](/help/dsp/campaign-management/placements/placement-settings.md)。

## 測試和資料驗證的最佳作法

針對可使用Adobe Analytics測量的[!DNL RampID]型區段和ID5型區段，使用下列最佳實務。

* 啟用區段約24小時後，請在[!UICONTROL Audiences] > [!UICONTROL All Audiences]內檢查區段的轉換識別碼計數。 如果ID計數屬意外，請聯絡您的Adobe帳戶團隊。

  請參閱&quot;[電子郵件ID與通用ID之間的資料差異](#universal-ids-data-variances)&quot;，以取得有關區段計數差異方式的詳細資訊。

* 請勿變更現有的套件和位置。 但是，如果您沒有任何用於測試通用ID的增量預算，請減少原始預算以資助測試。

* 複製原始套件和刊登版位、根據測試大小調整預算、將對象變更為使用[!DNL RampID]型區段（適用於已驗證的使用者）或ID5型區段（適用於未驗證的使用者），以及驗證新套件和刊登版位是否花費其完整預算。

   * 若要比較通用ID型區段的效能，與鎖定其他受眾識別碼（例如Cookie或行動廣告ID）之刊登版位的效能，請建立具有個別通用ID型刊登版位和舊版ID型刊登版位的行銷活動。

     若要進行完整的重新鎖定目標測試，請同時鎖定已驗證使用者的RampID和未驗證使用者的ID5。

     取得最佳效能不應是主要比較。 而是要判斷哪些ID的規模良好，這可能會在稍後通知您的最佳化和預算分配。 長期目標是要彌補在Cookie淘汰時遺失的曝光次數和網站流量。

   * 若要比較瀏覽器的總觸及率，請在相同位置鎖定通用ID型區段和舊有以ID型區段。 使用與上一個使用案例相同的行銷活動設定，除了您不需要分割行銷活動預算。

     通用ID會獲得競標偏好設定，但舊有ID會在無法使用通用ID時收到競標。 請務必比較不同瀏覽器(包括Chrome、Safari和Mozilla)中的觸及率。

     >[!NOTE]
     >
     >頻率上限適用於個別ID。 當使用者有多種ID型別時，您接觸該使用者的次數可能會超出您的預期。

* 請記住，已驗證身分的受眾區段的觸及率自然會小於Cookie型區段的觸及率，而使用其他鎖定目標選項會進一步減少您的觸及率。 謹慎使用精細鎖定目標，尤其是使用AND陳述式連結多個目標。

## 電子郵件ID和通用ID之間的資料差異 {#universal-ids-data-variances}

### 可接受的差異層級

雜湊電子郵件地址轉換為通用ID的翻譯率應大於90%；如果所有雜湊電子郵件地址都是唯一的，則[!DNL RampIDs]的翻譯率尤其應是95%。 例如，如果您從客戶資料平台傳送100個雜湊電子郵件地址，應將其轉譯為至少95個[!DNL RampIDs]或超過90種其他型別的通用ID。 較低的翻譯率可能表示有問題。 如需可能的解釋，請參閱&quot;[變異的原因] (#universal-ids-data-variances-causes&quot;。

若翻譯率低於70%，請與[!DNL RampIDs]的Adobe客戶團隊連絡以進行進一步調查。

### 差異原因 {#universal-ids-data-variances-causes}

* 所有區段：

  區段對裝置計數使用錯誤變異為+/- 5%的概率模型。 這表示可能會高估或低估對象人數5%。

* 已轉譯為[!DNL RampIDs]的雜湊電子郵件ID：

   * 當多個設定檔使用相同的電子郵件ID時，DSP區段計數可能會低於客戶資料平台內的設定檔計數。 例如，在Adobe Photoshop中，您可以使用單一電子郵件ID建立公司帳戶和個人帳戶。 但如果兩個設定檔都屬於同一個使用者，則設定檔會對應至一個電子郵件ID，並對應至一個[!DNL RampID]。

   * [!DNL RampID]可以升級為新值。 如果[!DNL LiveRamp]無法辨識電子郵件ID或無法將其對應至其資料庫中的現有[!DNL RampID]，則會指派新的[!DNL RampID]給電子郵件ID。 未來當他們可以將電子郵件ID對應到另一個[!DNL RampID]或收集有關相同電子郵件ID的更多資訊時，他們就會將[!DNL RampID]升級為新值。 [!DNL LiveRamp]參考此動作為從「衍生」[!DNL RampID]升級至「維護」[!DNL RampID]。 不過，DSP無法在衍生與維護的[!DNL RampIDs]之間取得對應，因此無法從DSP區段中移除舊版的RampID。 在這種情況下，區段計數可以大於設定檔計數。

     範例：使用者登入[!DNL Adobe]網站並造訪Photoshop頁面。 如果[!DNL LiveRamp]沒有任何關於電子郵件ID的現有資訊，則會指派衍生[!DNL RampID]，例如D123。 15天後，使用者造訪了相同頁面，但[!DNL LiveRamp]在這15天內升級了[!DNL RampID]，並將[!DNL RampID]重新指派為M123。 即使客戶資料平台的「Photoshop Enthusiast」區段只有使用者的一個電子郵件ID，DSP區段還是有兩個RampID：D123和M123。

## 疑難排解

如果您沒有看到使用者計數，或您的對象人數偏低，請檢查下列專案：

* 如果您使用[!DNL Flashtalking]或[!DNL Google Campaign Manager 360]廣告，請確定廣告的點進URL已附加正確的巨集。 檢視[[!DNL Flashtalking] 廣告](/help/integrations/analytics/macros-flashtalking.md)和[[!DNL Google Campaign Manager 360] 廣告](/help/integrations/analytics/macros-google-campaign-manager.md)的巨集。

* 請確定您的網站上已實作正確的、通用ID合作夥伴專用程式碼，以符合站上事件和廣告曝光。 視需要與您的[!DNL LiveRamp]或[!DNL ID5]代表合作。

* （針對[!DNL RampIDs]與[!DNL UID 2.0] ID）請確定您的[DSP資料來源已正確設定](/help/dsp/audiences/sources/source-manage.md#source-settings)，而且已針對產生的對象區段填入使用者計數。

* 如果您的觸及率低於預期，請檢查對象區段邏輯是否不太精細。

* 請確認您的行銷活動、封裝和位置設定正確。<!-- wording-->

如果您無法解決問題，請聯絡您的Adobe客戶團隊。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](/help/dsp/audiences/sources/source-manage.md)
>* [建立和實施自訂區段](/help/dsp/audiences/custom-segment-create.md)
>* [從 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手動匯入已驗證的區段
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
