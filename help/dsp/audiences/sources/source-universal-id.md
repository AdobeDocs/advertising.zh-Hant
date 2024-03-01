---
title: 啟用通用ID合作夥伴的已驗證區段
description: 瞭解如何透過通用ID解決方案來啟用已驗證的對象。
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 5d031fe746dc5051320e5d2092f9148b5a8a1bd5
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# 啟用通用ID合作夥伴的已驗證區段

若要透過Advertising DSP中的通用ID解決方案啟用已驗證受眾，您的區段必須轉譯為 [!DNL RampIDs]，這些區段可在可競標環境中辨識。 您可以透過以下其中一種方式來達到此目的：

* 善用DSP與的整合 [!DNL Adobe Real-Time Customer Data Platform (CDP)] 和 [!DNL Adobe-LiveRamp Retrieval API].

* 從手動傳送已驗證區段至DSP [!DNL LiveRamp] [!DNL Connect] 儀表板。

## 任務

1. 無論是哪一個選項，請連絡 `adcloud-support@adobe.com` 在DSP中啟用下列設定，可讓您在DSP促銷活動中定位已驗證的區段一次 [啟動工作流程中的所有步驟都已完成](source-adobe-rtcdp.md)：

   * [!DNL LiveRamp] [!DNL RampID] 從共用區段前的行銷活動設定 [!DNL Real-Time CDP]

   * 帳戶層級」[!UICONTROL LiveRamp segments]「選項

1. (使用者可透過手動共用已驗證的區段 [!DNL LiveRamp])在「 」中完成以下步驟 [!DNL LiveRamp] [!DNL Connect] 儀表板：

   1. 啟用目的地圖磚 **[!DNL AAC API 1P Onboarding]**.

   1. 設定 [!DNL Identifier Settings] 至 **[!DNL Ramp ID]** 僅限。

      ![識別碼設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （選用）如果您仍要接收Cookie型識別碼，請建立第二個 [!DNL AAC API 1P Onboarding] 目的地並排顯示&quot;[!DNL Cookies]，&quot; &quot;[!DNL IDFA]，」和「[!DNL AAID]「」已選取。

## 測試和資料驗證的最佳作法

* **Target [!DNL RampID]不同行銷活動中的區段和Cookie型區段。**

   * 行銷活動設定只允許優先處理一個識別碼。

   * 目前， [!DNL RampIDs] 在網站上的事件期間無法擷取。 這表示某些自訂目標（例如最低CPA和ROAS）無法與已驗證的區段搭配使用。 只有在您具備嚴格的效能KPI時，才使用Cookie型區段。

* **在下列兩個位置中建立一個位置 [!DNL RampID] 和Cookie型行銷活動。**

   * 定位共用的區段 [!DNL LiveRamp] 使用標準區段啟用程式。

   * 與您的Adobe Advertising支援團隊合作，驗證正確的資料分佈。

若要進一步瞭解DSP與的整合 [!DNL LiveRamp]，連絡人 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [關於從受眾來源啟用已驗證的區段](source-about.md)
>* [建立對象來源以啟用第一方對象](source-create.md)
>* [對象來源設定](source-settings.md)
>* [Adobe Advertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
