---
title: 設定的必要條件 [!DNL Google Analytics] 資料來源
description: 瞭解在設定之前必須完成的步驟 [!DNL Google Analytics] 資料來源。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 設定的必要條件 [!DNL Google Analytics] 資料來源

在您可以設定之前 [!DNL Google Analytics] 資料來源，您必須將搜尋、Social和商務查詢字串引數&quot;ef_id&quot;建立為主要索引鍵，以從中傳遞資料 [!DNL Google Analytics] 至「搜尋」、「社交」和「商務」。 設定每個的主索引鍵 [!DNL Google Analytics] 您要為其同步資料的帳戶和屬性組合。 組織中的其他人可能需要完成這些任務；請參閱下方以瞭解更多資訊。

如果您的廣告或關鍵字的登陸頁面URL尚未包含Search、Social和Commerce重新導向，請先新增它們。

## 先決條件1：在所有適用廣告帳戶的登陸頁面URL中實作搜尋、社交和商務權杖（「ef_id」查詢字串引數）

在相關行銷活動的每個付費搜尋點選上，以唯一的 `ef_id` 必須產生並以查詢字串形式附加至登陸頁面URL，例如 `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`，其中 `&ef_id=abcde:123456789:s` 是附加符號， `ef_id` 金鑰，以及 `ef_id` 值。 若要包含ef_id，相關廣告網路帳戶和行銷活動必須具備 [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]」和 [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].」

若為現有帳戶和促銷活動，則可能已實作ef_id。

如果未包含ef_id，請向您的Adobe帳戶團隊尋求協助。

完成所有先決條件後， `ef_id` 作為傳遞資料的主要金鑰 [!DNL Google Analytics] 至「搜尋」、「社交」和「商務」。

## 先決條件2：在每個相關的自訂維度中擷取搜尋、社交和商務權杖（「ef_id」查詢字串引數） [!DNL Google Analytics] 屬性

針對每個重複下列工作 [!DNL Google Analytics] 您要為其同步資料的帳戶和屬性組合。 另請參閱 [[!DNL Google Analytics] 有關建立及實作自訂維度的檔案](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) 以取得這些工作的說明。

1. 在 [!DNL Google Analytics]，建立自訂維度「`ef_id`「。 將維度的範圍設定為 [!DNL User]，並將維度設為「作用中」。

   >[!NOTE]
   >
   >此先決條件需要相關屬性的編輯許可權。

1. 更新您的 [!DNL Google Analytics] 追蹤程式碼，用來擷取ef_id查詢字串引數（當其出現在登陸頁面URL中時）的值，並將其儲存於ef_id自訂維度中。

   >[!NOTE]
   >
   >ef_id應僅在登陸頁面URL中。

   例如，如果登陸頁面URL為 `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`，然後中的ef_id維度的值 [!DNL Google Analytics] 是 `abcde:123456789:s`.

   >[!NOTE]
   >
   >應由合格的開發人員完成此先決條件。

>[!MORELIKETHIS]
>
>* [關於同步 [!DNL Google Analytics] 轉換量度](data-source-about.md)
>* [設定 [!DNL Google Analytics] 以資料來源檢視](data-source-configure.md)
>* [編輯 [!DNL Google Analytics] 資料來源](data-source-edit.md)
>* [暫停資料來源的同步處理](data-source-pause.md)
>* [重新驗證 [!DNL Google Analytics] 資料來源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 資料來源設定](data-source-settings.md)
>* [附錄 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)

