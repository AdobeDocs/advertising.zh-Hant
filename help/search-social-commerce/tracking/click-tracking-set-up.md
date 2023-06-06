---
title: 設定Cookie型點選追蹤
description: 瞭解如何設定及驗證點選追蹤標籤。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# 設定Cookie型點選追蹤

若要讓Search、Social和Commerce追蹤點按，必須設定並驗證下列元素。

1. (Adobe客戶團隊)將廣告商設定為畫素客戶。

1. [為每個廣告商的廣告網路帳戶和行銷活動指定正確的追蹤選項](#set-up-click-tracking-options).

1. 如有需要， [產生追蹤URL並上傳](#generate-upload-tracking-urls) （適用於某些促銷活動元素）。

1. [驗證一些點選追蹤URL的格式，然後測試以驗證是否開啟了正確的登陸頁面](#validate-tracking-urls).

## 設定廣告網路帳戶和行銷活動的追蹤選項 {#set-up-click-tracking-options}

*代理商客戶經理， [!DNL Adobe] 僅帳戶管理員和管理員使用者角色*

1. 請針對每個廣告網路帳戶，執行下列動作：

   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. 將游標停留在帳戶名稱上，按一下 ![功能表圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表圖示")，然後選取 **[!UICONTROL Edit]**.

   1. 按一下 **[!UICONTROL Set Account Tracking]**.

   1. 對於 [!UICONTROL Tracking Type] 設定，選取 **[!UICONTROL EF Redirect]**.

   1. (可讓Search、Social和Commerce與Adobe Analytics交換資料或追蹤中發生的轉換) [!DNL Apple Safari])選取 [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. （可選）開啟 **[!UICONTROL Auto Upload]** 用於在Search、Social和Commerce下次與其同步時自動將新追蹤URL上傳到廣告網路的選項。 此值會繼承為帳戶中所有促銷活動的預設值，但可以在促銷活動層級覆寫。

1. 請針對每個行銷活動，執行下列動作：

   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子功能表中，按一下 **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. 將游標停留在促銷活動名稱上，按一下 ![功能表圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表圖示")，然後選取 **[!UICONTROL Edit]**.

   1. 按一下 **[!UICONTROL Set Campaign Tracking]**. 然後選取「 」選項，以 **[!UICONTROL Override Account Tracking]**.

   1. 對於 [!UICONTROL Tracking Type] 設定，選取 **[!UICONTROL EF Redirect]**.

   1. (可讓Search、Social和Commerce與Adobe Analytics交換資料或追蹤中發生的轉換) [!DNL Apple Safari])選取 [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. （可選）開啟 **[!UICONTROL Auto Upload]** 用於在Search、Social和Commerce下次與其同步時自動將新追蹤URL上傳到廣告網路的選項。 此值會繼承為帳戶中所有促銷活動的預設值，但可以在促銷活動層級覆寫。

## 產生和上傳追蹤URL {#generate-upload-tracking-urls}

請參閱「[何時及如何產生點選追蹤URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).」

### 測試點選追蹤URL的格式 {#validate-tracking-urls}

驗證點選追蹤URL是否開啟了正確的登陸頁面。

1. 透過將流量傳送至廣告商的中繼環境來模擬廣告點選：

   1. 在文字編輯器中，貼上點選追蹤URL、變更登陸頁面URL以指向廣告商中繼環境中的相同頁面，然後將新URL貼到瀏覽器的位址列並按 **[!DNL Enter]** 金鑰。

   1. 在瀏覽器的預存Cookie中尋找Cookie。

   1. 在中繼網站上完成交易，然後確認成功頁面觸發了正確的畫素。 畫素追蹤的實際引數會因廣告商和追蹤URL而異。 在以下範例中，廣告商想要追蹤新應用程式的數量和新收入的金額：

      若是新的一般使用者（使用全新Cookie），應觸發下列畫素：

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      如果Cookie不是最新的，則應引發下列畫素：

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. 對網域中的數個點選追蹤URL重複此動作。

1. 對每個網域重複步驟1，並相應地使用不同的登陸頁面。

1. 必要時，請確認Search、Social和Commerce可以看到交易ID的畫素(`ev_transid`)的測試期間產生。

>[!MORELIKETHIS]
>
>* [何時及如何產生點選追蹤URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)

