---
title: 建立位置
description: 瞭解如何建立版位。
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# 建立位置

>[!TIP]
>
>根據特定行銷活動目標或報告需求建立刊登版位。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下要包含版位的行銷活動名稱。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。 在功能表的[!UICONTROL Placement Types]區段中，按一下位置型別。

   位置型別會決定位置可包含的廣告型別。

1. 輸入[位置設定](placement-settings.md)：

   1. 指定[!UICONTROL Placement Basics]設定。

   1. 在[!UICONTROL Goals]區段中，指定[!UICONTROL Gross Budget]，並選擇性地指定其他位置目標。

      有些欄位有預設值，您可以加以覆寫。

      如果位置指派到的套件具有套件層級的步調，則您的目標和步調設定會反映套件設定。

   1. （選擇性）在[!UICONTROL Geo-Targeting]區段中，縮小要包含或排除的位置。

      如果您未識別特定位置，則會鎖定所有位置。

      >[!NOTE]
      >
      >Roku位置無法使用城市和DMA位置。

   1. 在[!UICONTROL Inventory Targeting]區段中，縮小要包含或排除的詳細目錄來源。

      對於大多數版位型態，預設會包含所有存貨型態及每種型態的所有來源。 對於[!DNL Roku]個位置，您必須指定詳細目錄型別和來源。

   1. （選擇性）在[!UICONTROL Site Targeting]區段中，縮小您要鎖定的網站，並指定要排除的任何網站。

   1. （選擇性）在[!UICONTROL Audience Targeting]區段中：

      1. 縮小對象範圍。 這包括選取要定位在位置中的對象區段。

         對於[!DNL Roku]個位置，您可以納入一或多個可與[!DNL Roku] （選擇加入）確定性資料集比對的對象區段，以善用[DSP與 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md)的唯一對象比對。

      1. （適用於具有人物層級跨裝置目標定位的行銷活動；選用）當刊登版位鎖定一或多個特定對象時，請為刊登版位啟用人物型跨裝置目標定位。

         [!DNL LiveRamp]僅使用美國資料提供以人物為基礎的跨裝置目標定位。 所有廣告商皆可透過$0.35 CPM使用該服務，透過使用[!DNL LiveRamp]裝置圖表傳送的曝光數（亦即，在目標受眾區段中找不到裝置）來取得曝光數。

   1. （選用）在[!DNL Brand Safety and Media Targeting]區段中，為您的位置套用品牌安全限制。

   1. （選擇性）在[!DNL Tracking]區段中，為刊登版位中的廣告輸入協力廠商事件畫素或轉換畫素。

      >[!NOTE]
      >
      >（[!DNL Roku]位置） [!DNL Roku]核准的第三方畫素廠商包括[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。

1. 按一下&#x200B;**[!UICONTROL Create Placement]**。

1. （選用）在刊登版位中附加廣告：

   1. 按一下&#x200B;**[!UICONTROL Attach an ad]**。

   1. 執行下列任一項作業：

      * 若要建立新廣告：

         1. 按一下&#x200B;**[!UICONTROL Create a New Ad].**

         1. 指定[音訊廣告](/help/dsp/campaign-management/ads/ad-settings-audio.md)、[連線電視](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)、[顯示廣告](/help/dsp/campaign-management/ads/ad-settings-display.md)、[行動廣告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)、[原生廣告](/help/dsp/campaign-management/ads/ad-settings-native.md)、[前段廣告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)或[通用視訊廣告](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)的廣告設定。

        >[!NOTE]
        >
        >通用視訊版位只能包含通用視訊廣告。

         1. 按一下&#x200B;**[!UICONTROL Save & Submit for Review]**。

         1. （選擇性）針對您想要為位置建立的每個其他廣告，按一下「**[!UICONTROL Attach Another Ad]**」，然後重複步驟1至3。

         1. 如果您不打算附加任何現有的廣告，請按一下&#x200B;**[!UICONTROL I'm done for now]**。

      * 若要在行銷活動中附加現有廣告：

      1. 按一下&#x200B;**[!UICONTROL Select an Ad]**。

      1. 執行下列任一項作業：

         * 若要一次新增一個廣告：

            1. 在廣告名稱旁，按一下&#x200B;**[!UICONTROL Select].**

            1. （選擇性）針對您想要附加的每個其他廣告，按一下「**[!UICONTROL Attach Another Ad]**」，然後重複此程式。

         * 若要一次新增最多20個廣告：

            1. 選取廣告清單上方的核取方塊。

            1. 選取每個要新增的廣告旁的核取方塊。

            1. 按一下&#x200B;**[!UICONTROL Attach]**。

            1. 在廣告名稱旁邊，按一下&#x200B;**[!UICONTROL Select]**。

      1. （選用）若要覆寫版位中特定廣告的預設投放期間和廣告輪換：

         1. 按一下&#x200B;**[!UICONTROL Custom Schedule Ads]**。

         1. 執行下列任一項作業：

            * 若要新增航班，請按一下&#x200B;**[!UICONTROL Add Flight]**，然後指定開始日期和結束日期。

            * 若要將現有航班新增至廣告，請按一下航班欄的廣告列中的&#x200B;**[!UICONTROL +]**。

            * 若要從廣告中移除現有的航班，請按一下航班欄的廣告列中的&#x200B;**[!UICONTROL x]**。

            * （如果有多個廣告有相同的投放位置）若要不平均旋轉廣告，請按一下投放位置資訊中的&#x200B;**[!UICONTROL Even Rotation]**，然後輸入每個廣告旋轉的相對權重，以百分比表示。

              總重量必須等於100。

         1. 按一下右上角的&#x200B;**[!UICONTROL Continue]**。

         1. 檢閱航班詳細資料，然後按一下&#x200B;**[!UICONTROL Save & Finish]**。

>[!MORELIKETHIS]
>
>* [關於位置管理](placement-about.md)
>* [編輯版位](placement-edit.md)
>* [管理刊登版位的競標乘數](placement-manage-bid-multipliers.md)
>* [編輯刊登版位的廣告排程](placement-edit-ad-schedule.md)
>* [暫停或啟動位置](placement-pause-activate.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [位置設定](placement-settings.md)
>* [檢視刊登版位預測報告](/help/dsp/campaign-management/reports/placement-forecast.md)
>* 關於通用視訊的[常見問題集](/help/dsp/campaign-management/faq-universal-video.md)
>* [鍵盤快速鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [疑難排解效能](/help/dsp/optimization/troubleshooting-performance.md)
>* [影片：如何建立標準顯示位置](https://video.tv.adobe.com/v/340454)
