---
title: Advertising Creative 2.0的新增功能
description: 瞭解Adobe Advertising Creative 2.0的最新更新與新功能。
cloud: Experience Cloud
product: advertising cloud
solution: Advertising
index: false
exl-id: 0d25f665-b5f9-4d27-851a-2a456fe2cbf8
source-git-commit: d9dee4daf396c2aa84ba6b0635e8a819fe9932be
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# 在[!DNL Creative] 2.0中有何不同？

*已關閉的Beta*

<!-- The following features are new or recently changed. -->

| 日期 | 功能 | 說明 | 以取得詳細資訊 |
| ---- | ------- | ----------- | -------------------- |
| 2025年2月10日 | [!UICONTROL Creative Libraries] | 之前，您有一個創意程式庫。 現在，您可以為每個廣告商建立多個程式庫。 | 請參閱&quot;[關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)&quot;。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] | [!UICONTROL Creatives]檢視包含[!UICONTROL Standard Ads]和[!UICONTROL Dynamic Ads]的索引標籤。<ul><li>**[!UICONTROL Standard Ads]標籤**&#x200B;可讓您上傳和管理影像、HTML5、彈性的HTML5和協力廠商創意內容。</li><li>**[!UICONTROL Dynamic Ads]**&#x200B;索引標籤可讓您管理使用定義的廣告範本從上傳摘要檔案建立的動態產生廣告；之前，動態廣告是在[!DNL Adobe Advertising Dynamic Creative Optimization (DCO)]內產生。<br><br>目前，您可以預覽、複製和刪除動態廣告。 您也可以將動態廣告附加至目標廣告體驗的創意套件組合或非目標體驗的廣告標籤。 只有管理員使用者可以建立動態產生的廣告。</li></ul> | 請參閱&quot;[關於您的創意程式庫](/help/creative/creative-libraries/creative-libraries-about.md)&quot;。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] | 將多個創意內容分組到&#x200B;*組合*&#x200B;中，以便輕鬆新增到體驗中。 您可以建立標準廣告組合，並將標準創意附加至這些組合。 同樣地，您可以建立動態廣告套裝，並將動態創意附加至這些套裝。 | 請參閱[管理Creative組合](/help/creative/creative-libraries/bundle-manage.md)。 |
| | [!UICONTROL Experiences] | 在新的廣告體驗設定中，您現在可指定體驗是否使用決策樹目標定位，而且一旦儲存體驗，便無法變更設定。 具有決策樹鎖定目標的體驗與沒有決策樹鎖定目標的體驗的工作流程不同。 | 請參閱&quot;[建立具有鎖定目標的體驗](/help/creative/experiences/experience-create-targeting.md)&quot;和&quot;[建立沒有鎖定目標的體驗](/help/creative/experiences/experience-create-no-targeting.md)&quot;。 |
| | [!UICONTROL Experiences] | 您現在只能從單一創意程式庫使用創意套件組合來建立目標體驗，而不能使用個別創意成果。 您仍然可以從單一資料庫將個別創意內容附加至非目標體驗，而無需決策樹定位。<br><br>由於結構變更，您的舊版體驗將於今年稍後淘汰。 | 自助服務客戶：在新使用者介面中重建體驗。 請參閱&quot;[建立具有鎖定目標的體驗](/help/creative/experiences/experience-create-targeting.md)&quot;。<br><br>受管理的服務客戶：您的Adobe帳戶團隊將在新的使用者介面中重建您的體驗。 |
| | [!UICONTROL Experiences] | 使用Advertising DSP的廣告商可選擇將標籤直接上傳至Advertising DSP促銷活動作為廣告。 | 請參閱&quot;[匯出並實作即時體驗的廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)&quot; |
| | DCO體驗 | 舊版DCO體驗將於今年稍後淘汰。 您的Adobe帳戶團隊將在[!DNL Creative]中重新建置您的DCO體驗作為動態廣告，除了具有其他鎖定目標的DCO體驗將重新建置為[!DNL Creative]體驗。 | — |
| | 廣告標籤 | 廣告伺服器端點將變更為Advertising DSP廣告伺服器。<br><br>新廣告標籤包含傳遞通用ID的其他引數（以及Cookie ID）。 | 自助服務客戶：在[!DNL Creative]中取得體驗後，請取代現有行銷活動中的廣告標籤。 請參閱&quot;[匯出並實作即時體驗的廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)&quot;。<br><br>受管理的服務客戶：您的Adobe客戶團隊將取代現有行銷活動中的廣告標籤。 |
| | 重新定位畫素 | 重新定位畫素端點將變更為Adobe Advertising UDB服務。<br><br>新畫素包含其他引數，可傳遞除了Cookie ID以外的通用ID。 | 自助服務客戶：建立新的重新目標畫素並新增至您的網頁。 請參閱&quot;[管理重新目標畫素](/help/creative/pixels/retargeting-pixel-manage.md)&quot;。<br><br>Managed Service客戶：您的Adobe客戶團隊將建立並共用新的重新定位畫素（如果適用）；將新畫素新增至您的網頁。 |
| | 轉換畫素 | 舊版DCO畫素將於今年稍後淘汰，將需要[!DNL Adobe]個轉換畫素。 | 自助服務客戶：具有[!DNL Analytics for Advertising]的客戶必須將DCO轉換畫素取代為[!DNL Analytics for Advertising] [!DNL Last Event Service]畫素和Adobe Analytics畫素。 其他所有人都必須以Adobe Advertising轉換畫素取代DCO轉換畫素。<br><br>受管理的服務客戶：您的Adobe客戶團隊將建立並共用所有適用的Adobe Advertising轉換畫素；將您的DCO轉換畫素取代為Adobe Advertising轉換畫素。 |
