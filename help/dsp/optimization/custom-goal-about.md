---
title: 關於自訂目標
description: 瞭解自訂目標，以在針對最低CPA或最高ROAS而最佳化的套件中定義成功事件。
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: d1ebb6a12a04b969ba8558912c3ac76bb1632b3c
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 關於自訂目標

自訂目標定義廣告商實現其業務目標所需的成功事件。 每個使用最佳化目標的套件»[!UICONTROL Highest ROAS - Custom Goal]「或」[!UICONTROL Lowest CPA - Custom Goal]「必須包含有助於實現整體最佳化目標的自訂目標。 您可以建立自訂目標為 *目標* 在 [!DNL Advertising Search, Social, & Commerce].

![自訂目標](/help/dsp/assets/objective-goals.png)

每個自訂目標包含一或多個轉換量度，以及這些量度的相對權重。 可用的轉換量度包含使用Adobe Advertising轉換畫素並透過Adobe Analytics追蹤的所有量度。

>[!NOTE]
>
>* [!DNL Analytics] 維度和區段無法用於Adobe Advertising最佳化。
>* 若要在DSP中使用Analytics事件，請與您的Adobe帳戶團隊合作，設定廣告商層級的整合。
>* [!DNL Analytics] 自訂事件會遵循以下命名慣例： `custom_event_[*event #*]_[*Analytics report suite ID*]`. 範例： `custom_event_16_examplersid`

例如，假設三個轉換量度與您的其中一個行銷活動中的特定套件相關：價值20美元的「PDF下載」、價值30美元的「電子郵件註冊」和價值40美元的「訂單確認」。 如果您想要根據客戶動作的一次性貨幣值賦予權重，則屬性的相對權重為1、2和1.5。

請參閱 [建立自訂目標的最佳實務](custom-goal-best-practices.md) 以取得如何設定自訂目標的秘訣。

一旦您 [建立自訂目標](custom-goal-create.md)，您可以 [將其指派給封裝](/help/dsp/campaign-management/packages/package-settings.md) 使用Adobe Sensei進行報告和演演算法最佳化。

>[!MORELIKETHIS]
>
>* [建立自訂目標](custom-goal-create.md)
>* [建立自訂目標的最佳實務](custom-goal-best-practices.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
