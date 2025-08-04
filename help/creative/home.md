---
title: Advertising Creative 2.0的新增功能
description: 瞭解Adobe Advertising Creative 2.0的最新更新與新功能。
cloud: Experience Cloud
product: advertising cloud
solution: Advertising
index: false
exl-id: 0d25f665-b5f9-4d27-851a-2a456fe2cbf8
source-git-commit: 780c84aa8dadb52b55d5ca2bee6974b56972793b
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 0%

---

# 在[!DNL Creative] 2.0中有何不同？

*已關閉的Beta*

<!-- The following features are new or recently changed. -->

| 日期 | 功能 | 說明 | 以取得詳細資訊 |
| ---- | ------- | ----------- | -------------------- |
| 2025年8月4日 | 廣告[!DNL]體驗的對象目標] | 當您設定廣告體驗的對象目標時，您現在可以選取是要&#x200B;*[!UICONTROL Include any]* （預設）還是要選取節點的指定目標&#x200B;*[!UICONTROL Include all]*。 此選項會決定使用者是否必須至少屬於其中一個指定對象，或屬於所有指定對象，才能符合曝光資格。<br><br>使用此選項，&quot;[!UICONTROL Split targets to create nodes]&quot;的現有選項將無法再使用。 | 請參閱&quot;[新增目標節點至最終層級](/help/creative/experiences/experience-target-node-add-final.md)&quot;、&quot;[在節點](/help/creative/experiences/experience-target-node-add-inner.md)之間插入目標節點&quot;以及&quot;[新增同層級目標節點](/help/creative/experiences/experience-target-node-add-sibling.md)&quot;。 |
| 2025年7月10日 | 視訊創意 | 支援現在適用於第一方視訊創作以及視訊專用套件和體驗：<ul><li>您現在可以上傳第一方視訊創意，並將其新增至視訊專用組合。 在套件設定中，「[!UICONTROL Bundle Type]」選項現在包含[!UICONTROL Standard Display]、[!UICONTROL Dynamic Display]和[!UICONTROL Standard Video]。</li><li>您可以使用視訊套件建立視訊專用廣告體驗。 廣告體驗設定現在包含&quot;[!UICONTROL Ad Type]&quot;設定，包含[!UICONTROL Standard Display]、[!UICONTROL Dynamic Display]和[!UICONTROL Video]選項。 您可以根據點進率、完成率或自訂目標來最佳化視訊廣告。</li><li>視訊廣告體驗標籤的標籤是由視訊持續時間和位元速率所定義，而非廣告大小。</li><li>視訊廣告會自動轉碼為Adobe Advertising DSP編碼，以便您預覽。 您可以選擇將其他DSP的轉碼套用至[!UICONTROL Tag Manager]中的任何廣告體驗標籤。</li></ul> | 請參閱&quot;[關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)&quot;、&quot;[管理創意組合](/help/creative/creative-libraries/bundle-manage.md)&quot;、&quot;[目標體驗設定](/help/creative/experiences/experience-settings-targeting.md)&quot;、&quot;[非目標體驗設定](/help/creative/experiences/experience-settings-no-targeting.md)以及&quot;[自訂視訊廣告體驗標籤的轉碼選項](/help/creative/experiences/experience-tag-video-transcoding.md)&quot;。 |
| 2025年5月21日 | [!UICONTROL Creative Libraries] | 您現在可以將影像從Adobe Experience Manager資產庫新增至[!UICONTROL Creative Libraries]，以便在廣告體驗中使用這些影像。 | 請參閱&quot;[設定Adobe Experience Manager影像資產的存取權](/help/creative/creative-libraries/aem-assets-configure.md)&quot;和&quot;[將標準創意內容新增至創意資源庫](/help/creative/creative-libraries/creative-add-standard.md)&quot;。 |
| 2025年2月10日 | [!UICONTROL Creative Libraries] | 之前，您有一個創意程式庫。 現在，您可以為每個廣告商建立多個程式庫。 | 請參閱&quot;[關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)&quot;。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] | [!UICONTROL Creatives]檢視包含[!UICONTROL Standard Ads]和[!UICONTROL Dynamic Ads]的索引標籤。<ul><li>**[!UICONTROL Standard Ads]標籤**&#x200B;可讓您上傳和管理影像、HTML5、彈性的HTML5和協力廠商創意內容。</li><li>**[!UICONTROL Dynamic Ads]**&#x200B;索引標籤可讓您管理使用定義的廣告範本從上傳摘要檔案建立的動態產生廣告；之前，動態廣告是在[!DNL Adobe Advertising Dynamic Creative Optimization (DCO)]內產生。<br><br>目前，您可以預覽、複製和刪除動態廣告。 您也可以將動態廣告附加至目標廣告體驗的創意套件組合或非目標體驗的廣告標籤。 只有管理員使用者可以動態產生廣告。</li></ul> | 請參閱&quot;[關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)&quot;。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] | 將多個創意內容分組到&#x200B;*組合*&#x200B;中，以便輕鬆新增到體驗中。 您可以建立標準廣告組合，並將標準創意附加至這些組合。 同樣地，您可以建立動態廣告套裝，並將動態創意附加至這些套裝。 | 請參閱[管理Creative組合](/help/creative/creative-libraries/bundle-manage.md)。 |
| | [!UICONTROL Experiences] | 在新的廣告體驗設定中，您現在可指定體驗是否使用決策樹目標定位，而且一旦儲存體驗，便無法變更設定。 具有決策樹鎖定目標的體驗與沒有決策樹鎖定目標的體驗的工作流程不同。 | 請參閱&quot;[建立具有鎖定目標的體驗](/help/creative/experiences/experience-create-targeting.md)&quot;和&quot;[建立沒有鎖定目標的體驗](/help/creative/experiences/experience-create-no-targeting.md)&quot;。 |
| | [!UICONTROL Experiences] | 您現在只能從單一創意程式庫使用創意套件組合來建立目標體驗，而不能使用個別創意成果。 您仍然可以從單一資料庫將個別創意內容附加至非目標體驗，而無需決策樹定位。<br><br>由於結構變更，您的舊版體驗將於今年稍後淘汰。 | 自助服務客戶：在新使用者介面中重建體驗。 請參閱&quot;[建立具有鎖定目標的體驗](/help/creative/experiences/experience-create-targeting.md)&quot;。<br><br>受管理的服務客戶：您的Adobe帳戶團隊將在新的使用者介面中重建您的體驗。 |
| | [!UICONTROL Experiences] | 使用Advertising DSP的廣告商可選擇將標籤直接上傳至Advertising DSP促銷活動作為廣告。 | 請參閱&quot;[匯出並實作即時體驗的廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)&quot; |
| | DCO體驗 | 舊版DCO體驗將於今年稍後淘汰。 您的Adobe帳戶團隊將在[!DNL Creative]中重新建置您的DCO體驗作為動態廣告，除了具有其他鎖定目標的DCO體驗將重新建置為[!DNL Creative]體驗。 | — |
| | 廣告標籤 | 廣告伺服器端點將變更為Advertising DSP廣告伺服器。<br><br>新廣告標籤包含傳遞通用ID的其他引數（以及Cookie ID）。 | 自助服務客戶：在[!DNL Creative]中取得體驗後，請取代現有行銷活動中的廣告標籤。 請參閱&quot;[匯出並實作即時體驗的廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)&quot;。<br><br>受管理的服務客戶：您的Adobe客戶團隊將取代現有行銷活動中的廣告標籤。 |
| | 重新定位畫素 | 重新定位畫素端點將變更為Adobe Advertising UDB服務。<br><br>新畫素包含其他引數，可傳遞除了Cookie ID以外的通用ID。 | 自助服務客戶：建立新的重新目標畫素並新增至您的網頁。 請參閱&quot;[管理重新目標畫素](/help/creative/pixels/retargeting-pixel-manage.md)&quot;。<br><br>Managed Service客戶：您的Adobe客戶團隊將建立並共用新的重新定位畫素（如果適用）；將新畫素新增至您的網頁。 |
| | 轉換畫素 | 舊版DCO畫素將於今年稍後淘汰，將需要[!DNL Adobe]個轉換畫素。 | 自助服務客戶：具有[!DNL Analytics for Advertising]的客戶必須將DCO轉換畫素取代為[!DNL Analytics for Advertising] [!DNL Last Event Service]畫素和Adobe Analytics畫素。 其他所有人都必須以Adobe Advertising轉換畫素取代DCO轉換畫素。<br><br>受管理的服務客戶：您的Adobe客戶團隊將建立並共用所有適用的Adobe Advertising轉換畫素；將您的DCO轉換畫素取代為Adobe Advertising轉換畫素。 |
