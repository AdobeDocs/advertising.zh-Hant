---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# 最終URL尾碼定義

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]：** ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] 僅限accounts；選用)任何要附加至最終URL結尾以追蹤資訊的引數；包含您的企業必須追蹤的所有引數。 範例：`param1=value1&param2=value2`

在使用Adobe廣告轉換追蹤的帳戶中，尾碼必須包含廣告網路的點選識別碼(`msclkid` 的 [!DNL Microsoft Advertising]； `gclid` 的 [!DNL Google Ads])。

具有Adobe Analytics整合的帳戶必須使用s_kwcid引數。 如果帳戶有伺服器端s_kwcid實作，則當使用者按一下廣告時，引數會自動新增；否則，您必須在此處手動新增。 請參閱 [必要的字尾格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) 和 [必要的字尾格式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* 此欄位未由 [!UICONTROL Auto Upload] 追蹤設定。
>* 較低層級的最終URL尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同的追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。

