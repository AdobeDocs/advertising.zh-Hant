---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---
# GGL和MS帳戶設定、行銷活動設定和一些廣告設定中的登陸頁面尾碼欄位

**[!UICONTROL Landing Page Suffix]：** （僅限[!DNL Google Ads]和[!DNL Microsoft Advertising]帳戶；選擇性）任何要附加至最終URL結尾以追蹤資訊的引數；包含您的企業必須追蹤的所有引數。 範例： `param1=value1&param2=value2`

使用Adobe Advertising轉換追蹤的帳戶必須在尾碼中包含廣告網路的點選識別碼（[!DNL Google Ads]為`gclid`或[!DNL Microsoft Advertising]為`msclkid`）。

具有Adobe Analytics整合的帳戶必須使用s_kwcid引數。 如果帳戶具有伺服器端s_kwcid實施，則當使用者按一下廣告時，引數會自動新增；否則，您必須在此處手動新增。 請參閱Google Ads的[必要尾碼格式](/help/search-social-commerce/tracking/formats-click-tracking-google.md)和Microsoft Advertising的[必要尾碼格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)。

**附註：**

* [!UICONTROL Auto Upload]追蹤設定未更新此欄位。

* 較低層級的登陸頁面尾碼會覆寫帳戶層級的尾碼。 為方便維護，除非需要對個別帳戶元件進行不同追蹤，否則請僅使用帳戶層級的尾碼。 若要在廣告群組層級或更低層級設定尾碼，請使用廣告網路的編輯器。
