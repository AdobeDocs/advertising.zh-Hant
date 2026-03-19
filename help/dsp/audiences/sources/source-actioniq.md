---
title: 將使用者ID從 [!DNL ActionIQ] 轉換為通用ID
description: 瞭解如何讓DSP擷取您的 [!DNL ActionIQ] 第一方區段。
feature: DSP Audiences
source-git-commit: 658c8a10c4085690ce4dd7e791883dbf31f1cb10
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 將使用者ID從[!DNL ActionIQ]轉換為通用ID

*Beta功能*

使用DSP與[!DNL ActionIQ]客戶資料平台的整合，將雜湊電子郵件地址轉換為通用識別碼，以用於目標定位廣告。

有<!-- NN -->個步驟可以與DSP共用[!DNL ActionIQ]的資料：

1. [在DSP中建立對象來源](#source-create)。

1. ？

## 步驟1：在DSP中建立對象來源 {#source-create}

1. [建立對象來源](source-manage.md)以將對象匯入您的DSP帳戶或廣告商帳戶，指定您要轉換使用者識別碼的[通用ID格式](source-about.md)。

1. 建立對象原始碼後，請將原始碼金鑰與[!DNL ActionIQ]使用者共用。

## 步驟2：

## 步驟3：

1. 驗證在您的對象資料庫中（當您從[!UICONTROL Audiences] > [!UICONTROL All Audiences]或版位設定中建立或編輯對象時，可使用此資料庫）有區段正在填入，並將通用ID的數量與原始雜湊電子郵件地址的數量進行比較。

   這些區段應該會在24小時內提供給DSP。 DSP收到區段資料後，受眾規模應在九(9)小時內顯示。 如需有關可接受的ID轉譯率以及區段計數可能不同的原因的資訊，請參閱[電子郵件ID與通用ID之間的資料差異](#universal-ids-data-variances)。

區段每24小時會重新整理一次。

## 疑難排解

若要疑難排解翻譯速率和使用者計數問題，請參閱&quot;[啟用通用ID的支援](/help/dsp/audiences/universal-ids.md)&quot;。

若要疑難排解轉換程式的問題，請聯絡您的Adobe客戶團隊或`adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [關於第一方對象來源](/help/dsp/audiences/sources/source-about.md)
>* [管理對象來源以啟用通用ID對象](source-manage.md)
>* [將使用者ID從 [!DNL Adobe Real-Time CDP] 轉換為通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [將使用者ID從 [!DNL Tealium] 轉換為通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)
