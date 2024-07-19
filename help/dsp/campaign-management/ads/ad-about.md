---
title: 關於Advertising DSP中的廣告管理
description: 瞭解廣告管理。
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# 關於Advertising DSP中的廣告管理

<!-- add "The Ads View (Dashboard?)" section -->

DSP支援各種廣告型別透過協力廠商廣告服務標籤(例如Google、Flashtalking或Sizmek)進行廣告傳送，以及原生顯示廣告的直接資產上傳。 您可以個別或大量上傳協力廠商標籤。 大量上傳使用合作夥伴標籤表或大量標籤範本。

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

設定廣告後，請將每個廣告附加至位置，其中包含目標定位引數（例如地理、對象、裝置和詳細目錄目標定位），這些引數可控制行銷活動的傳送方式。 您可以將單一廣告附加至一或多個位置。

## 可用的廣告型別 {#ad-types}

DSP提供下列所有廣告型別。 如需每種廣告型別的完整規格，請參閱[廣告規格](ad-specs.md)。

* **音訊廣告（僅限協力廠商）**：音訊廣告可在數位發行者網站上的內容之間播放，並可作為音訊檔案或與隨附橫幅一起獨立執行。 音訊最適合用來提升品牌知名度，以及與行動受眾互動。 音訊的關鍵績效指標包括[!UICONTROL Completion Rate]和[!UICONTROL Cost per Completion]。

* **顯示廣告（僅限協力廠商）**：顯示廣告是以網頁瀏覽器或應用程式顯示的動畫或靜態影像。 按一下廣告單位會帶領使用者前往品牌網站或微網站。 顯示器最適合用來推動有效率的CPM、增加訊息關聯、新增其他品牌或產品接觸點，以及促使使用者降低購買漏斗。 顯示器的關鍵績效指標包括[!UICONTROL Clicks]、[!UICONTROL Cost per Click]、[!UICONTROL Conversions]和[!UICONTROL Cost per Conversion]。 DSP支援各種顯示橫幅廣告大小。

* **行動廣告（僅限協力廠商）**：行動廣告可以是前段影片(VAST、MRAID)或標準顯示格式。 行動前段視訊可以是自動播放或點按播放，最適合用於跨熒幕觸及觀眾。 行動標準顯示是顯示在行動網頁瀏覽器或應用程式中的靜態影像，最適合用於補充數位視訊購買、推動訊息關聯，以及新增其他品牌或產品接觸點。 行動廣告也可以當作全熒幕收購或行動插頁廣告，這是全熒幕、高影響力的行動廣告，最適合用來為行動對象建立品牌知名度並促進轉換。

* **原生顯示廣告（僅限第一方）**：標準顯示格式支援原生廣告。 原生廣告包括標題和/或標題、說明、標誌和影像。 廣告元素會結合併轉譯以符合發佈者的頁面樣式，因此廣告會與發佈者的自然內容融入，並提高參與度。 原生最能用於品牌認知度，並透過對檢視者友好的廣告促進受眾檢視和參與率。 關鍵績效指標包括[!UICONTROL Clicks]、[!UICONTROL Cost Per Click]、[!UICONTROL Conversions]和[!UICONTROL Cost Per Conversion]。

* **前段廣告（僅限協力廠商）**：前段廣告（VAST和VPAID）會顯示在高階視訊內容之前，並提供沈浸式且吸引人的檢視者體驗。 前段影片可以是互動式、包含豐富媒體功能，並包含覆蓋、變換影像和行動號召。 前段影片廣告的關鍵績效指標包括[!UICONTROL Video Completion Rate]和[!UICONTROL Viewability Rate]。

* **連線電視廣告（僅限協力廠商）**：連線電視廣告會顯示在優質電視視訊內容之前和期間。 所有連線電視清查都會在電視裝置上執行，這表示視訊會在精簡的全熒幕環境中自動播放，而檢視者無法略過。 連線電視是最接近電視廣告的數位視訊格式。 連線電視的關鍵績效指標包括[!UICONTROL Completion Rate]。

* **通用視訊廣告（僅限協力廠商）**：通用視訊廣告可讓您使用單一視訊位置，針對桌上型電腦、行動裝置和連線電視環境的VPAID和VAST詳細目錄設定目標視訊詳細目錄。 它們結合連線電視、前段廣告和行動前段廣告的所有功能，並在視訊內容之前和期間顯示。 通用視訊的關鍵績效指標包括[!UICONTROL Completion Rate]和[!UICONTROL Viewability Rate]。

  通用視訊廣告只能附加至通用視訊位置。

  如需通用視訊廣告的詳細資訊，請參閱[通用視訊常見問題集](/help/dsp/campaign-management/faq-universal-video.md)。

## DSP廣告核准

當您建立廣告時，DSP會檢閱敏感類別、按一下URL功能，以及預覽呈現。

廣告的[!UICONTROL Status]欄最初會顯示紅點。 稽核程式通常需要24到48小時。 然而，損壞的廣告可能會有超過48小時的待處理狀態，因此您有時間在廣告被拒絕之前修復錯誤。 被拒絕的廣告包含拒絕的原因。

當DSP核准廣告時，廣告的狀態列會顯示綠色點。

[!UICONTROL Status]欄](/help/dsp/assets/ad-approval-status.png)中的![核准指標

>[!NOTE]
>
>只有在DSP和SSP皆核准創意內容後，才能提供您的廣告。 每個SSP都有各自的核准需求和流程。

>[!MORELIKETHIS]
>
>* [建立單一廣告](ad-create.md)
>* [建立多個協力廠商廣告](ad-create-multiple.md)
>* [廣告規格](ad-specs.md)
