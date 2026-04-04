---
title: 關於 [!DNL Google Ads] 轉換值規則
description: 瞭解如何在搜尋、社交和Commerce中檢視和管理 [!DNL Google Ads] 轉換值規則。
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# 關於[!DNL Google Ads]轉換值規則

搜尋、社交和Commerce會自動從您的[帳戶同步](https://support.google.com/google-ads/answer/10518330)轉換值規則[!DNL Google Ads]。 轉換值規則可讓您根據使用者資訊（包括裝置型別、位置和對象區段）調整轉換事件的值。 透過Google智慧競標，您可以在搜尋、顯示、購物和效能最大化行銷活動中使用價值型競標規則。 對於具有Maximize Conversions和Target ROAS競標策略的行銷活動，[!DNL Google Ads]演演算法將開始偏好具有較高值的轉換。

行銷活動層級轉換值規則會覆寫帳戶層級規則。 當轉換符合多個轉換值規則時，只會套用其中一個規則。 通常會套用最明確的規則，但請參閱不同規則條件型別[[!DNL Google Ads] 的優先順序的](https://support.google.com/google-ads/answer/10520348)檔案。

## [!UICONTROL Conversion Value Rules]檢視和功能

在[!DNL Google Ads]介面中建立的所有規則都會在24小時內同步，並可在[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]檢視中使用。 有些帳戶可以管理其轉換值規則：

* 在已在個別帳戶或行銷活動層級追蹤轉換的帳戶中，您可以建立、編輯和變更帳戶層級和行銷活動層級規則的狀態。

  這些帳戶可以連結到[!DNL Google Ads]個管理員帳戶，但它們不能使用跨帳戶轉換追蹤（針對此追蹤，會跨管理員帳戶中的所有帳戶來追蹤轉換）。

* 在使用跨帳戶轉換追蹤的帳戶中，您的帳戶層級和促銷活動層級規則繼承自管理員帳戶，且為唯讀。

## 使用搜尋、社交和Commerce產品組合的轉換值規則

當廣告商帳戶設定為將「搜尋」、「社交」和「Commerce」目標上傳至「[!DNL Google Ads]」，且您在具有目標的產品組合中加入使用轉換值規則的促銷活動時，[!DNL Google Ads]會將轉換值規則套用至目標中指定的原始轉換值。 因此，搜尋、社交和Commerce中的轉換資料與[!DNL Google Ads]中的轉換資料不同。

例如，假設目標使用單一轉換量度「銷售機會」，並將來自行動裝置的轉換權重設為10，將來自非行動裝置的轉換權重設為10。 搜尋、Social和Commerce會將任一裝置型別的事件計為一(1)次轉換，並將轉換值計為10。 然而，假設該投資組合中的行銷活動使用轉換值規則「如果裝置為行動，則乘以2。」 當為該行銷活動追蹤行動銷售機會事件時，[!DNL Google Ads]也會將轉換計數計為一(1)，但轉換值計為(10 x 2) = 20。

若要檢視規則的詳細資訊，包括套用規則之前的原始轉換值，請參閱[ [!DNL Google Ads]中的](https://support.google.com/google-ads/answer/10519848)轉換值規則報告。

>[!MORELIKETHIS]
>
>* [建立 [!DNL Google Ads] 轉換值規則](create-google-conversion-value-rule.md)
>* [編輯 [!DNL Google Ads] 轉換值規則](edit-google-conversion-value-rule.md)
>* [變更 [!DNL Google Ads] 轉換值規則](change-the-status-of-google-conversion-value-rule.md)的狀態
>* [[!DNL Google Ads] 轉換值規則設定](google-conversion-value-rule-settings.md)

