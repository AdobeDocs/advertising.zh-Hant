---
title: 建立及實作自訂區段
description: 瞭解如何建立及實作自訂區段，以追蹤曝光於廣告的使用者或造訪您網頁的使用者。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# 建立及實作自訂區段

您可以透過建立及實作自訂DSP區段來收集您自己的第一方對象資料。 您可以使用區段來追蹤a)接觸到來自桌上型電腦和行動裝置廣告的使用者，以及b)造訪特定網頁的使用者。 您稍後可以在區段中以其他廣告重新鎖定使用者，或避免區段中的使用者收到其他廣告。

>[!NOTE]
>
>若要追蹤您網站上消費者選擇退出銷售要求的使用者ID，請根據加州消費者隱私法(CCPA)，建立[CCPA選擇退出銷售區段](ccpa-opt-out-segment-create.md)。

## 追蹤ID5 ID的區段先決條件

*Beta功能*

* 在您產生區段以追蹤與ID5 ID相關聯的使用者之前，請先與[!DNL ID5]簽署合約並取得您組織的合作夥伴ID。 如需指示，請聯絡您的Adobe客戶團隊。

* 針對Adobe Analytics中的測量，您必須：

   1. 完成實作 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)的所有[必要條件，並確定已在您的追蹤URL中填入[AMO ID和EF ID](/help/integrations/analytics/ids.md)。

   1. 在初始化最後一個事件服務之前的任何位置，將下列引數新增至您網頁(在 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)所需的[JavaScript程式碼之前或之內)。

      ```window.id5PartnerId=ID5_PartnerID;```

      範例：

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      如需完整標籤格式，請參閱「[JavaScript轉換追蹤標籤格式3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)」和「[JavaScript轉換追蹤標籤格式2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)」。

   1. 使用任何瀏覽器偵錯工具來確認每個呼叫都是起始至網域`lasteventf-tm.everesttech.net`，並包含引數`_les_id5`，以加密的ID5 ID作為其值。

## 建立及實作自訂區段

1. 建立區段：

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Segments]**。

   1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。

   1. 輸入唯一的&#x200B;**[!UICONTROL Segment Name]**。

   1. 針對&#x200B;**[!UICONTROL Segment Type]**，選取&#x200B;*[!UICONTROL Custom]*。

   1. 輸入&#x200B;**[!UICONTROL Lookback Window]**，這是使用者的Cookie在區段中保留的天數。

      預設期間為45天。 輸入從一(1)到365的值。

   1. 按一下&#x200B;**[!UICONTROL Advanced]**&#x200B;以展開進階設定，然後選取區段標籤追蹤的使用者識別碼型別：

      * *[!UICONTROL Cookies]：* （預設）區段標籤會追蹤Cookie。

      * [!UICONTROL Universal IDs (Beta)]：

         * *[!UICONTROL ID5]：*&#x200B;區段標籤追蹤[!DNL ID5]個ID。 對於傳遞到通用ID的曝光，不會產生任何費用。

        **[!UICONTROL Terms of Service]：**&#x200B;使用通用ID的服務合約條款。 您或DSP帳戶中的其他使用者必須接受條款一次，才能將通用ID用於新ID型別。 若客戶擁有受管理的服務合約，您的Adobe客戶團隊將取得您的同意，並代表貴組織接受條款。 若要閱讀條款，請按一下&#x200B;**>**。 若要接受條款，請捲動至條款底部，然後按一下&#x200B;**[!UICONTROL Accept]**。

   1. 按一下&#x200B;**[!UICONTROL Save]**。

1. 視需要複製並實作標籤以追蹤區段：

   1. 返回&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Segments]**。

   1. 將游標停留在區段列上，然後按一下&#x200B;**[!UICONTROL Get Pixel]**。

      * 若要追蹤網頁的案頭和行動訪客：

         1. 複製標籤為「[!UICONTROL Desktop or mobile websites]」的頁面檢視追蹤標籤。

         1. （追蹤[!DNL ID5] ID之區段的標籤）在複製的標籤中，將`ID5_PARTNER_ID`取代為[!DNL ID5]指派給貴組織的合作夥伴ID。

            例如，如果您的ID5合作夥伴ID為`abcde`，而產生的區段標籤為

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            然後在標籤中以`abcde`取代`ID5_PARTNER_ID`以取得下列專案：

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            貴組織在與[!DNL ID5]簽署合約時收到合作夥伴識別碼。 如果您不知道合作夥伴ID，請聯絡您的Adobe客戶團隊。

            標籤不需要執行此步驟來追蹤案頭或行動裝置上廣告單元所公開的使用者的[!DNL ID5] ID。

         1. 為廣告商或網站連絡人提供標籤以進行部署。

            廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

      * 若要追蹤在桌上型電腦或行動裝置上向廣告單位公開的使用者：

         1. 複製標示為&quot;[!UICONTROL Desktop or mobile ads]&quot;的曝光追蹤標籤。

         1. 將標籤新增至每個相關廣告的[!UICONTROL Pixel]標籤或每個相關位置](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking)的[[!UICONTROL Tracking]設定的[!UICONTROL Event Pixels]區段。

實施追蹤標籤後，您即可在任何位置的對象目標或排除專案中使用區段。

>[!TIP]
>
>在追蹤使用者時追蹤區段大小。

>[!MORELIKETHIS]
>
>* [關於對象管理](audience-about.md)
>* [編輯區段資訊](segment-edit.md)
>* [刪除區段](segment-delete.md)
>* [檢視區段的追蹤畫素](segment-view-pixels.md)
>* [共用或停止共用區段](segment-share.md)
>* [建立並實作[!UICONTROL CCPA Opt-Out-of-Sale]區段](ccpa-opt-out-segment-create.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [可用的協力廠商資料提供者](third-party-data-providers.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
