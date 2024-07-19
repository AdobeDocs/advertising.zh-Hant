---
title: 設定a [!DNL Google Analytics] 資料來源的先決條件
description: 瞭解設定 [!DNL Google Analytics] 資料來源之前必須完成的步驟。
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 設定[!DNL Google Analytics]資料來源的先決條件

在設定[!DNL Google Analytics]資料來源之前，您必須建立Search、Social和Commerce查詢字串引數&quot;ef_id&quot;作為主索引鍵，將資料從[!DNL Google Analytics]傳遞至Search、Social和Commerce。 為您要同步資料的每個[!DNL Google Analytics]帳戶和屬性組合設定主索引鍵。 組織中的其他人可能需要完成這些任務；請參閱下方以瞭解更多資訊。

如果您的廣告或關鍵字的登陸頁面URL尚未包含搜尋、Social和Commerce重新導向，請先新增。

## 先決條件1：在所有適用廣告帳戶的登陸頁面URL中實作搜尋、社交和Commerce權杖（「ef_id」查詢字串引數）

在相關行銷活動的每個付費搜尋點選上，必須產生唯一的`ef_id`，並以查詢字串形式附加至登陸頁面URL，例如`https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`，其中`&ef_id=abcde:123456789:s`為附加符號、`ef_id`鍵和`ef_id`值。 若要包含ef_id，相關廣告網路帳戶和行銷活動必須具有[!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot;和[!UICONTROL Redirect Type] &quot;[!UICONTROL Token]&quot;。

若為現有帳戶和促銷活動，則可能已實施ef_id。

如果未包含ef_id，請向您的Adobe帳戶團隊尋求協助。

完成所有先決條件後，`ef_id`會作為主索引鍵，以將資料從[!DNL Google Analytics]傳遞至Search、Social和Commerce。

## 先決條件2：在每個相關[!DNL Google Analytics]屬性的自訂維度中擷取搜尋、社交和Commerce權杖（&quot;ef_id&quot;查詢字串引數）

針對您想要同步資料的每個[!DNL Google Analytics]帳戶和屬性組合，重複下列工作。 如需這些工作的說明，請參閱有關建立及實作自訂維度的[[!DNL Google Analytics] 檔案](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article)。

1. 在[!DNL Google Analytics]中，建立名為&quot;`ef_id`&quot;的自訂維度。 將維度的範圍設定為[!DNL User]，並將維度設定為作用中。

   >[!NOTE]
   >
   >此先決條件需要相關屬性的編輯許可權。

1. 更新您的[!DNL Google Analytics]追蹤程式碼，擷取ef_id查詢字串引數（當其出現在登陸頁面URL中時）的值，並將其儲存在ef_id自訂維度中。

   >[!NOTE]
   >
   >ef_id應僅在登陸頁面URL中。

   例如，如果登陸頁面URL為`https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`，則[!DNL Google Analytics]中ef_id維度的值為`abcde:123456789:s`。

   >[!NOTE]
   >
   >應由合格的開發人員完成此先決條件。

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [將 [!DNL Google Analytics] 檢視設定為資料來源](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停同步處理資料來源](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
