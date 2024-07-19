---
title: 設定Cookie型點選追蹤
description: 瞭解如何設定及驗證點選追蹤標籤。
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# 設定Cookie型點選追蹤

若要讓「搜尋」、「社交」和「Commerce」追蹤點按，必須設定並驗證下列元素。

1. (Adobe客戶團隊)將廣告商設定為畫素客戶。

1. [請為每個廣告商的廣告網路帳戶和行銷活動指定正確的追蹤選項](#set-up-click-tracking-options)。

1. 必要時，[產生追蹤URL並上傳部分行銷活動專案的追蹤URL](#generate-upload-tracking-urls)。

1. [驗證一些點選追蹤URL的格式，並測試它們以驗證是否開啟了正確的登陸頁面](#validate-tracking-urls)。

## 設定廣告網路帳戶和行銷活動的追蹤選項 {#set-up-click-tracking-options}

*僅限代理商帳戶管理員、[!DNL Adobe]帳戶管理員和系統管理員使用者角色*

1. 請針對每個廣告網路帳戶，執行下列動作：

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]>[!UICONTROL Accounts]**。

   1. 將游標停留在帳戶名稱上，按一下![功能表圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表圖示")，然後選取&#x200B;**[!UICONTROL Edit]**。

   1. 按一下&#x200B;**[!UICONTROL Set Account Tracking]**。

   1. 針對[!UICONTROL Tracking Type]設定，選取&#x200B;**[!UICONTROL EF Redirect]**。

   1. (若要允許搜尋、社交和Commerce與Adobe Analytics交換資料，或追蹤[!DNL Apple Safari]中發生的轉換)選取[!UICONTROL Redirect Type]選項&#x200B;**[!UICONTROL Token]**。

   1. （選用）開啟&#x200B;**[!UICONTROL Auto Upload]**&#x200B;選項，在下次Search、Social和Commerce與其同步時，自動將新追蹤URL上傳至廣告網路。 此值繼承為帳戶中所有促銷活動的預設值，但可在促銷活動層級覆寫。

1. 針對每個行銷活動，執行下列動作：

   1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子功能表中，按一下&#x200B;**[!UICONTROL Live]>[!UICONTROL Campaigns]**。

   1. 將游標停留在行銷活動名稱上，按一下![功能表圖示](/help/search-social-commerce/assets/arrow-dropdown-menu.png "功能表圖示")，然後選取&#x200B;**[!UICONTROL Edit]**。

   1. 按一下&#x200B;**[!UICONTROL Set Campaign Tracking]**。 然後選取&#x200B;**[!UICONTROL Override Account Tracking]**&#x200B;的選項。

   1. 針對[!UICONTROL Tracking Type]設定，選取&#x200B;**[!UICONTROL EF Redirect]**。

   1. (若要允許搜尋、社交和Commerce與Adobe Analytics交換資料，或追蹤[!DNL Apple Safari]中發生的轉換)選取[!UICONTROL Redirect Type]選項&#x200B;**[!UICONTROL Token]**。

   1. （選用）開啟&#x200B;**[!UICONTROL Auto Upload]**&#x200B;選項，在下次Search、Social和Commerce與其同步時，自動將新追蹤URL上傳至廣告網路。 此值繼承為帳戶中所有促銷活動的預設值，但可在促銷活動層級覆寫。

## 產生和上傳追蹤URL {#generate-upload-tracking-urls}

請參閱&quot;[何時及如何產生點選追蹤URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)&quot;。

### 測試點選追蹤URL的格式 {#validate-tracking-urls}

驗證點選追蹤URL是否開啟了正確的登陸頁面。

1. 透過將流量傳送至廣告商的中繼環境來模擬廣告點選：

   1. 在文字編輯器中，貼上點選追蹤URL、變更登陸頁面URL以指向廣告商中繼環境中的相同頁面，然後將新URL貼到瀏覽器的位址列中，然後按&#x200B;**[!DNL Enter]**&#x200B;鍵。

   1. 在您的瀏覽器儲存的Cookie中尋找Cookie。

   1. 在中繼網站上完成交易，然後確認成功頁面是否引發正確的畫素。 畫素追蹤的實際引數會因廣告商和追蹤URL而異。 在下列範例中，廣告商想要追蹤新應用程式的數量與新收入的金額：

      若是新的一般使用者（具有新的Cookie），應引發下列畫素：

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      如果Cookie不是最新的，則應引發下列畫素：

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. 對網域中的數個點選追蹤URL重複此動作。

1. 對每個網域重複步驟1，並相應地使用不同的登陸頁面。

1. 必要時，請確認Search、Social和Commerce可以看到測試期間產生的交易ID (`ev_transid`)畫素。

>[!MORELIKETHIS]
>
>* [何時及如何產生點選追蹤URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
