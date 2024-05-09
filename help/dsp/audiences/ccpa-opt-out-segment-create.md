---
title: 建立並實作CCPA選擇退出銷售區段
description: 瞭解如何建立並實作區段，以追蹤消費者選擇退出銷售請求中的使用者ID。
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# 建立並實作CCPA選擇退出銷售區段

您可以建立區段，以根據加州消費者隱私法(CCPA)追蹤網站上消費者選擇退出銷售請求的使用者ID。 使用者會無限期留在CCPA選擇退出銷售區段中。

實施區段畫素標籤後，Adobe Advertising會代表廣告商開始收集ID集區。

>[!NOTE]
>
>* 如需有關如何使用Adobe Experience Platform Privacy Service API將CCPA選擇退出銷售請求傳達給Adobe Advertising的資訊，請參閱 [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* 若要追蹤出於與追蹤CCPA選擇退出銷售事件無關之目的而造訪網頁的使用者，以及接觸到來自案頭、行動和CTV裝置廣告的使用者，請建立 [自訂區段](/help/dsp/audiences/custom-segment-create.md).

1. 建立區段：

   1. 在主功能表中，按一下 **受眾>區段**.

   1. 在資料表格上方，按一下 **[!UICONTROL Create]**.

   1. 輸入唯一值 **[!UICONTROL Segment Name]**.

      建議的區段名稱： &quot;&lt;*您的廣告商名稱*> - CCPA選擇退出銷售」（例如「Acme - CCPA選擇退出銷售」）

   1. 對於 [!UICONTROL Segment Type]，選取 **[!UICONTROL CCPA Opt-out of sale]**.

   1. 按一下 **[!UICONTROL Save]**.

1. 複製並實作畫素標籤以追蹤區段：

   1. 返回至 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 在區段列中，將游標停留在新區段上並按一下 **[!UICONTROL Get pixel]**.

   1. 複製影像畫素(開頭為 `<img src="https://rtd-tm.everesttech.net"`)，以收集網頁中桌上型電腦和行動訪客的使用者ID。

   1. 將標籤提供給廣告商或網站連絡人，以使用公司用來追蹤CCPA選擇退出銷售請求的機制進行部署（例如使用同意管理平台）。

      廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

      實作畫素後，Adobe Advertising會代表廣告商開始收集ID集區。

      雖然實作選擇和邏輯取決於廣告商，但以下範例為廣告商如何引發畫素：

      1. 消費者登陸廣告商的首頁。
      1. 消費者找到並點按廣告商的「CCPA選擇退出銷售」按鈕。
      1. 消費者會看到廣告商與其合作的服務提供者清單。
      1. 消費者會勾選方塊，選擇退出將資料銷售給Adobe Advertising。

         此動作會觸發畫素，並收集指定&#39;&#39;內的消費者Cookie ID[!UICONTROL CCPA Opt-out of sale]「區段。

>[!MORELIKETHIS]
>
>* [加州消費者隱私法的Adobe Advertising支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [關於 [!UICONTROL CCPA Opt-out-of-Sale] 區段與報表](ccpa-opt-out-about.md)
>* [擷取消費者選擇退出銷售報表](ccpa-opt-out-segment-report-retrieve.md)
>* [建立及實作自訂區段](custom-segment-create.md)
>* [關於對象管理](audience-about.md)
