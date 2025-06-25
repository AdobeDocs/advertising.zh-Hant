---
title: 將搜尋、社交和Commerce追蹤的轉換量度上傳至 [!DNL Google Ads]
description: 瞭解如何將搜尋、社交和Commerce追蹤的轉換量度上傳至 [!DNL Google Ads]。
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 將搜尋、社交和Commerce追蹤的轉換量度上傳至[!DNL Google Ads]

*僅具有[!DNL Google Ads]帳戶和Adobe Advertising轉換追蹤的廣告商*

搜尋、Social和Commerce可選擇上傳至[!DNL Google Ads]所有轉換量度，以供使用Adobe Advertising轉換追蹤服務的[!DNL Google Ads]個促銷活動追蹤。 此選項無法讓轉換可用於混合最佳化。 如果您想要使用Adobe轉換進行混合最佳化，請參閱「[啟用將目標上傳至廣告網路](objective-upload-to-networks.md)」。

每日上傳包含追蹤的`gclid`值、使用廣告商層級歸因模型定義的轉換值，以及時間戳記。 如果更新歸因模型，下次上傳時將會使用新模型，但不會更新過去的資料以使用新模型。

>[!NOTE]
>
>上傳內容不包含從摘要檔案上傳至Adobe Advertising的轉換量度。

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**。

1. 選取&#x200B;**[!UICONTROL Upload Conversions to Google Ads]**&#x200B;旁的核取方塊。

1. (在歐洲經濟區(EEA)或英國(UK)從事業務的廣告商；選擇性)如果您已向EEA和英國使用者收集同意，可上傳其資料以供廣告用途，請選取&#x200B;**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;旁的核取方塊

1. 按一下&#x200B;**[!UICONTROL Save]**。

1. （若您的轉換是在經理帳戶層級追蹤） [在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;為您的經理帳戶新增認證](/help/search-social-commerce/admin/manager-accounts.md)。

>[!MORELIKETHIS]
>
>* [啟用上傳目標至廣告網路](objective-upload-to-networks.md)
