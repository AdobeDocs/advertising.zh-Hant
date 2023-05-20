---
title: 建立和實施自定義段
description: 瞭解如何建立和實施自定義網段，以跟蹤暴露在廣告中的用戶或訪問您網頁的用戶。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 建立和實施自定義段

您可以通過建立和實施自定義段來收集自己的第一方受眾DSP資料。 您可以使用該段跟蹤a)案頭、移動和CTV設備中暴露在廣告中的用戶和b)訪問特定網頁的用戶。 以後，您可以用附加廣告來重新定位網段中的用戶，或阻止網段中的用戶接收附加廣告。

>[!NOTE]
>
>要跟蹤您網站上消費者選擇退出銷售請求的用戶ID，請根據加利福尼亞消費者隱私法(CCPA)建立 [CCPA選擇不銷售分部](ccpa-opt-out-segment-create.md)。

1. 建立段：

   1. 在主菜單中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**。

   1. 在資料表上方，按一下 **[!UICONTROL Create]**。

   1. 輸入唯一 **[!UICONTROL Segment Name]**。

   1. 對於 **[!UICONTROL Segment Type]**&#x200B;選中 *[!UICONTROL Custom]*。

   1. 輸入 **[!UICONTROL Segment Window]**，即用戶cookie在段中停留的天數。

      預設窗口為45天。 輸入一(1)到365之間的值。

   1. 按一下 **[!UICONTROL Save]**.

1. 根據需要複製並實施標籤以跟蹤段：

   1. 返回到 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**。

   1. 將游標置於段行上，然後按一下 **[!UICONTROL Get Pixel]**。

      * 要跟蹤網頁的案頭和移動訪問者：

         1. 複製標有「」的頁面視圖跟蹤標籤[!UICONTROL Desktop or mobile websites]&quot;

         1. 將標籤提供給廣告商或網站聯繫人以進行部署。

            廣告商的IT部門或其他組可能需要安排標籤部署，或獲得有關標籤部署的資訊。
      * 要跟蹤在案頭、移動或CTV設備上暴露在廣告單元中的用戶：

         1. 複製標籤為「」的印象跟蹤標籤[!UICONTROL Desktop or mobile ads]&quot;


1. 將標籤添加到 [!UICONTROL Pixel] 或 [!UICONTROL Event Pixels] 的下界 [[!UICONTROL Tracking] 每個相關放置的設定](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking)。

實施跟蹤標籤後，您可以將受眾目標中的段或排除項用於任何位置。

>[!TIP]
>
>跟蹤用戶時跟蹤段大小。

>[!MORELIKETHIS]
>
>* [關於受眾管理](audience-about.md)
>* [編輯段資訊](segment-edit.md)
>* [刪除段](segment-delete.md)
>* [查看段的跟蹤像素](segment-view-pixels.md)
>* [共用或停止共用段](segment-share.md)
>* [建立和實施 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [建立可重用的受眾](reusable-audience-create.md)
>* [可用的第三方資料提供程式](third-party-data-providers.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)

