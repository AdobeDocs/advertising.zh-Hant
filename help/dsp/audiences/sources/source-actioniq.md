---
title: 「轉換使用者ID，從 [!DNL ActionIQ] 至通用ID」
description: 「瞭解如何啟用DSP以擷取您的 [!DNL ActionIQ] 第一方區段。」
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
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

## 步驟2：

## 步驟3：

1. 在您的對象庫中驗證（當您從以下位置建立或編輯對象時可使用此庫） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 或在位置設定內)填入的區段，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。

   這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾計數應在九(9)小時內顯示。 如需有關可接受的ID轉譯率以及區段計數可能不同的原因的資訊，請參閱&quot;[電子郵件ID和通用ID之間的資料差異](#universal-ids-data-variances).」

區段每24小時會重新整理一次。

## 疑難排解

若要疑難排解翻譯速率和使用者計數問題，請參閱&quot;[支援啟用通用ID](/help/dsp/audiences/universal-ids.md).」

若要疑難排解轉換程式的問題，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [轉換使用者ID來源 [!DNL Adobe Real-Time CDP] 至通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [轉換使用者ID來源 [!DNL Tealium] 至通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
