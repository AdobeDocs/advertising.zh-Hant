---
title: 「轉換使用者ID，從 [!DNL ActionIQ] 至通用ID」
description: 「瞭解如何啟用DSP以擷取您的 [!DNL ActionIQ] 第一方區段。」
feature: DSP Audiences
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 轉換使用者ID來源 [!DNL ActionIQ] 至通用ID

*Beta功能*

將DSP整合用於 [!DNL ActionIQ] 客戶資料平台，將雜湊電子郵件地址轉換為通用ID以用於目標定位廣告。

有 <!-- NN --> 要分享資料的步驟，從 [!DNL ActionIQ] 使用DSP：

1. [在DSP中建立對象來源](#source-create).

1. ？

## 步驟1：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md) 將受眾匯入您的DSP帳戶或廣告商帳戶，請指定 [通用識別碼格式](source-about.md) 您要將使用者識別碼轉換到哪個位置。

1. 建立對象來源後，請將原始程式碼金鑰與 [!DNL ActionIQ] 使用者。

1. 
   <!-- ActionIQ-specific step(s) -->

1. 在您的對象庫中驗證（當您從以下位置建立或編輯對象時可使用此庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 或在位置設定內)填入的區段，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。

   這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾計數應在九(9)小時內顯示。

   如需有關可接受的ID轉譯率以及區段計數可能不同的原因的資訊，請參閱&quot;[電子郵件ID和通用ID之間的資料差異](#universal-ids-data-variances).」

   如需疑難排解支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

區段每24小時會重新整理一次。

## 步驟2：

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [轉換使用者ID來源 [!DNL Adobe Real-Time CDP] 至通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [轉換使用者ID來源 [!DNL Tealium] 至通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
