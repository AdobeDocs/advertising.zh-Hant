---
title: 「轉換使用者ID，從 [!DNL ActionIQ] 至通用ID」
description: 「瞭解如何啟用DSP以擷取您的 [!DNL ActionIQ] 第一方區段。」
feature: DSP Audiences
source-git-commit: ecab6e81575128718156bb0bde1a5ea33a21d5f0
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# 轉換使用者ID來源 [!DNL ActionIQ] 至通用ID

*Beta功能*

將DSP整合用於 [!DNL ActionIQ] 客戶資料平台，將雜湊電子郵件地址轉換為通用ID以用於目標定位廣告。

有 <!-- NN --> 要分享資料的步驟，從 [!DNL ActionIQ] 使用DSP：

1. [在DSP中建立對象來源](#source-create).

1. ？

## 步驟1：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-create.md) 將受眾匯入您的DSP帳戶或廣告商帳戶，請指定 [通用識別碼格式](source-about.md) 您要將使用者識別碼轉換到哪個位置。

1. 建立對象來源後，請將原始程式碼金鑰與 [!DNL ActionIQ] 使用者。

1. 完成所有步驟後，請在對象庫中驗證（您從建立或編輯對象時可使用此對象庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 區段會在24小時內填入。 比較通用ID的數量與原始雜湊電子郵件地址的數量。

   雜湊電子郵件地址轉譯為通用ID的速率應大於90%。 例如，如果您從客戶資料平台傳送100個雜湊電子郵件地址，則應將其轉譯為90個以上的通用ID。 90%或更低的翻譯率是個問題。 如需區段計數可能變異的詳細資訊，請參閱&quot;[電子郵件ID與通用ID之間資料差異的原因](#universal-ids-data-variances).」

   如需疑難排解支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

區段每24小時會重新整理一次。

## 步驟2：

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [建立對象來源以啟用通用ID對象](source-create.md)
>* [對象來源設定](source-settings.md)
>* [轉換使用者ID來源 [!DNL Adobe Real-Time CDP] 至通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [轉換使用者ID來源 [!DNL Tealium] 至通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
