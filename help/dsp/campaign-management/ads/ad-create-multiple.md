---
title: 建立多個第三方廣告
description: 瞭解如何同時建立多個第三方廣告。
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 建立多個第三方廣告

您可以上傳標籤來一次建立最多500個第三方廣告，這些標籤會指向在第三方廣告伺服器上託管的創意資產。 您可以包含廣告的追蹤畫素。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

您可以使用提供的範本上傳[!DNL DoubleClick]和[!DNL Flashtalking]標籤工作表或手動填入的檔案。

>[!TIP]
>
> 最佳實務是使用透過HTTPS安全地提供的第三方廣告。 使用HTTPS提供的URL以「https」開頭。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下要包含廣告之行銷活動的名稱。

1. 按一下資料表上方的&#x200B;**[!UICONTROL Create]**。 在功能表的[廣告型別]區段中，按一下&#x200B;**[!UICONTROL Bulk upload ads]**。

1. 選取裝載廣告的廣告伺服器： *[!UICONTROL DoubleClick]*、*[!UICONTROL Flashtalking]*&#x200B;或&#x200B;*[!UICONTROL Other]*。

1. （[!DNL DoubleClick]和[!DNL Flashtalking]廣告）選取要用於每個視訊資產和每個顯示資產的標籤型別。 可用選項會依廣告伺服器而有所不同。

1. （除[!DNL DoubleClick]和[!DNL Flashtalking]以外的所有廣告伺服器上的廣告）按一下「**[!UICONTROL Download this template]**」以下載[!DNL Microsoft Excel]試算表(XLSX)格式的範本，您可以填入廣告資料並在本機儲存。 必要的資料行包括[!UICONTROL Ad Name]、[!UICONTROL VAST/VPAID URL or Ad Tag]和[!UICONTROL Ad Types]。

1. 按一下&#x200B;**[!UICONTROL Upload]**&#x200B;並從您的裝置或網路中選取.xlsx或.xls格式的檔案。

   針對[!DNL DoubleClick]和[!DNL Flashtalking]廣告，從廣告伺服器上傳未編輯的標籤工作表。 若是其他廣告伺服器，請使用您在步驟3下載的範本。

1. 上傳完成後，請按一下&#x200B;**[!UICONTROL Start Building Ads]**。

1. 檢閱每個廣告的詳細資訊和狀態：

   1. （使用[!DNL Google]或[!DNL Flashtalking]標籤的通用視訊廣告）按一下&#x200B;**[!UICONTROL Ad Type]**&#x200B;欄位並選取&#x200B;**[!UICONTROL Universal Video]**。

   1. （通用視訊廣告）針對每個新廣告，按一下![編輯](/help/dsp/assets/edit.png)、選取[適用的視訊格式](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)，然後按一下&#x200B;**儲存**。

   1. 檢閱每個廣告的狀態，此狀態會根據上傳標籤的驗證檢查。

   1. （選用）對每個廣告執行下列任一項作業：

      * 若要預覽廣告，請按一下廣告列中的![播放](/help/dsp/assets/play.png)。

      * 若要編輯廣告詳細資料，請按一下[編輯] ![](/help/dsp/assets/edit.png)，編輯詳細資料，然後按一下[儲存] **&#x200B;**。

      * 若要移除廣告，請按一下廣告列中的&#x200B;**[!UICONTROL X]**。

1. 按一下&#x200B;**[!UICONTROL Create *N *個廣告]**。

1. 執行下列任一項作業：

   * 按一下&#x200B;**[!UICONTROL Done]**。

   * （如果廣告遭拒；選擇性）若要編輯廣告記錄並重新提交廣告以供檢閱，請執行下列動作：

      1. 按一下廣告名稱。

      1. 編輯廣告設定。

      1. 按一下&#x200B;**[!UICONTROL Save & submit for review]**。

>[!NOTE]
>
>通用視訊廣告只能附加至通用視訊位置。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [廣告規格](ad-specs.md)
>* [建立單一廣告](ad-create.md)
>* [影片：如何大量上傳協力廠商廣告標籤](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html?lang=zh-Hant)
>* 關於通用視訊的[常見問題集](/help/dsp/campaign-management/faq-universal-video.md)
