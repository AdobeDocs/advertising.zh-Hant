---
title: 關於網站連結擴充功能
description: 瞭解網站連結擴充功能。
exl-id: c2d96440-62da-4b57-a98e-d7b94882d6c5
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# 關於網站連結擴充功能

僅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]*

網站連結是文字廣告清單中的額外文字連結。 使用網站連結將使用者直接帶往您網站中的特定頁面。 廣告網路會根據網站連結與廣告的相關性，決定要顯示哪些網站連結與廣告。 您可以選擇加入每個網站連結的描述性文字，這些文字可能包含在廣告中。 當廣告復本與網站連結高度相關時，廣告網路可能會自動顯示帳戶中具有網站連結之現有廣告的廣告復本。 [!DNL Google Ads]可能會在案頭廣告中顯示2到6個網站連結，在行動廣告中最多可顯示4個網站連結。 [!DNL Microsoft Advertising]可能會顯示兩個、四個或六個有說明的網站連結，或是4-6個沒有說明的網站連結。

您可以在帳戶層級建立共用的網站連結文字和設定，包括網站連結可和廣告一起出現的日期。

## [!UICONTROL Sitelinks]和[!UICONTROL Associations]檢視

[!UICONTROL Campaigns] > [!UICONTROL Campaigns]中的[!UICONTROL Extensions] > [!UICONTROL Sitelinks]資料庫會列出您所有的帳戶層級網站連結，而且您可以在此建立和管理您的共用網站連結。 請參閱廣告網路說明，以取得每個[[!DNL Google Ads] 帳戶](https://support.google.com/google-ads/answer/6372658)和每個[[!DNL Microsoft Advertising] 帳戶](https://help.ads.microsoft.com/#apex/3/en/52001)的廣告擴充功能數目上限。 資料庫中的網站連結不會與廣告搭配使用，直到您將它們指派給帳戶實體為止。

從[!UICONTROL Extensions] > [!UICONTROL Associations]檢視中，您可以將任何網站連結儘可能指派給帳戶層級（[!DNL Google Ads]僅限）、行銷活動層級或廣告群組層級（[!DNL Google Ads]僅限）的所有廣告。

## 網站連結的效能資料

搜尋、Social和Commerce會將點按的廣告擴充功能以及產生的轉換對應到與包含擴充功能的廣告相關聯的關鍵字。 搜尋、Social和Commerce中沒有費用或擴充功能層級的點選資料。 不過，在[的[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)中，當「連結型別」欄中的值列為`sl:<Sitelink text>` （例如sl：請參閱目前的選件）時，您可以分辨交易是否源自網站連結（而非廣告本身）。

在[!DNL Google Ads]和[!DNL Microsoft Advertising]中，您可以在[!DNL Ad Extensions]標籤上看到成本和點選資料。

>[!MORELIKETHIS]
>
>* [管理共用的網站連結延伸模組](sitelink-extension-manage.md)
>* [將共用的網站連結擴充功能與行銷活動或廣告群組建立關聯](sitelink-extension-associate.md)
