---
title: 建立並實施CCPA選擇不銷售部門
description: 瞭解如何建立和實施段，以跟蹤消費者選擇退出銷售請求中的用戶ID。
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 建立並實施CCPA選擇不銷售部門

您可以根據加利福尼亞消費者隱私法(CCPA)建立一個段，以跟蹤用戶ID，從您網站上的消費者選擇退出銷售請求。 用戶無限期地留在CCPA選擇不銷售的部門。

一旦實現段像素標籤，Adobe廣告將開始代表廣告商收集ID池。

>[!NOTE]
>
>* 有關如何使用Adobe Experience Platform Privacy ServiceAPI將CCPA選擇退出銷售請求與Adobe廣告通信的資訊，請參見 [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html)。
>* 要跟蹤訪問網頁的用戶，以跟蹤與CCPA選擇退出銷售事件無關的用戶，以及接觸案頭、移動和CTV設備廣告的用戶，請建立 [自定義段](/help/dsp/audiences/custom-segment-create.md)。


1. 建立段：

   1. 在主菜單中，按一下 **受眾>段**。

   1. 在資料表上方，按一下 **[!UICONTROL Create]**。

   1. 輸入唯一 **[!UICONTROL Segment Name]**。

      建議的段名稱：「&lt;」*您的廣告商名稱*> - CCPA Opt Out of Sale」（例如「Acme - CCPA Opt Of Sale」）

   1. 對於 [!UICONTROL Segment Type]選中 **[!UICONTROL CCPA Opt-out of sale]**。

   1. 按一下 **[!UICONTROL Save]**.

1. 複製並實施像素標籤以跟蹤段：

   1. 返回到 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**。

   1. 在段行中，將游標保持在新段上，然後按一下 **[!UICONTROL Get pixel]**。

   1. 複製影像像素(以開頭 `<img src="https://rtd-tm.everesttech.net"`)以收集網頁的案頭和移動訪問者的用戶ID。

   1. 向廣告商或網站聯繫人提供標籤，以便使用公司用於跟蹤CCPA選擇退出銷售請求（如使用同意管理平台）的機制進行部署。

      廣告商的IT部門或其他組可能需要安排標籤部署，或獲得有關標籤部署的資訊。

      一旦實施該像素，Adobe廣告將開始代表廣告商收集ID池。

      儘管實施選擇和邏輯取決於廣告商，但以下是一個廣告商如何激發像素的示例：

      1. 消費者登陸廣告商首頁。
      1. 消費者會找到並點擊廣告商的「CCPA opt of out of sale」按鈕。
      1. 向消費者提供廣告商與之工作的服務提供商清單。
      1. 消費者會選中該框，選擇不向Adobe廣告銷售資料。

         此操作將觸發像素，並在指定的「」中收集使用者的Cookie ID[!UICONTROL CCPA Opt-out of sale]&quot;段。

>[!MORELIKETHIS]
>
>* [Adobe對加利福尼亞消費者隱私法的廣告支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [關於 [!UICONTROL CCPA Opt-out-of-Sale] 段和報告](ccpa-opt-out-about.md)
>* [檢索消費者選擇不可銷售報表](ccpa-opt-out-segment-report-retrieve.md)
>* [建立和實施自定義段](custom-segment-create.md)
>* [關於受眾管理](audience-about.md)

