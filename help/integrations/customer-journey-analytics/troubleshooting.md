---
title: 疑難排解Customer Journey Analytics中的Adobe Advertising資料
description: 瞭解如何疑難排解及解決Customer Journey Analytics中的Adobe Advertising資料問題。
feature: Integration with Adobe Customer Journey Analytics
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 33382b092be521df814a81aad3c7ae661d853174
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 0%

---

# 疑難排解Customer Journey Analytics中的Adobe Advertising資料

以下是可能的資料問題及其原因。

## 摘要報告

+++ Customer Journey Analytics中沒有摘要報表資料可用於Advertising DSP或Advertising Search、Social和Commerce。

請確認下列專案：

* 從Adobe Advertising到Customer Journey Analytics的摘要已啟用。 請洽詢您的Adobe客戶團隊。

* 您的Adobe Advertising維度/分類/查詢資料集和摘要資料集包含在Customer Journey Analytics連線中。

* 您的Adobe Advertising維度和摘要量度包含在Customer Journey Analytics資料檢視中。

* Customer Journey Analytics Workspace所參照的資料檢視是正確的。

如果您已驗證上述所有設定，但仍看不到摘要資料，請在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)為您的組織開啟支援票證。

+++

+++ 廣告商1的Customer Journey Analytics中有摘要報表資料可以使用，但廣告商2則沒有。

確認已針對廣告商2啟用從Adobe Advertising到Customer Journey Analytics的摘要。 請洽詢您的Adobe客戶團隊。

如果為廣告商啟用了摘要，但您仍然看不到摘要資料，請在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)為您的組織開啟支援票證。

+++

+++ （搜尋、社交和Commerce使用者） Customer Journey Analytics中的摘要報表資料可用於一個[!DNL Google Ads]、[!DNL Meta Ads]或[!DNL Microsoft Advertising]帳戶，但不能用於另一個帳戶。

確認特定廣告網路帳戶已啟用從Adobe Advertising到Customer Journey Analytics的摘要。 請洽詢您的Adobe客戶團隊。

如果帳戶已啟用摘要，但您仍看不到摘要資料，請在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)為您的組織開啟支援票證。加入廣告網路帳戶的[!UICONTROL Account ID]。
.

+++

+++ Customer Journey Analytics Workspace中的摘要報表資料與Advertising DSP或Advertising Search、Social和Commerce中的資料不同，或是某些行銷活動和行銷活動實體缺少摘要資料。

請確認下列專案：

* 您在[!DNL Workspace]和Adobe Advertising報表中使用相同的日期範圍。

* 在[!DNL Workspace]和Adobe Advertising報表中套用的任何篩選器和區段都不會造成資料差異。

如果您確定資料不一致，請在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)為您的組織開啟支援票證。加入廣告網路帳戶的[!UICONTROL Account ID]。
.包含熒幕擷取畫面和電子表格，以顯示差異的證據。您的Adobe客戶團隊可回溯修正資料摘要，以視需要解決差異。

+++

## 事件層級報表

+++ CJA Customer Journey Analytics Workspace中的轉換資料（例如`Page Views`）不適用於報表維度（例如`Campaign`）。

從驗證障礙最少的專案開始，驗證以下內容：

* 適用的轉換量度為網頁/線上事件，Adobe Advertising可將其歸因於維度。

* 您使用正確的資料檢視。

* Adobe Advertising正在追蹤適用網站上的點進和檢視。<!-- Link to validation instructions in the user guide -->

* 在分類資料集的Customer Journey Analytics連線中，[!DNL Key]和[!DNL Matching Key]設定的值正確無誤： [!DNL Key]： `Tracking Code` (_customername.adLens2.trackingCode)，[!DNL Matching Key]： `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* [!DNL Adobe Advertising]服務已新增至Adobe Experience Platform資料流，資料流的對應結構描述是`XDM ExperienceEvent Schema`，而欄位群組`Adobe Advertising Cloud ExperienceEvent Full Extension`已新增至結構描述。

* Adobe Advertising設定已在WebSDK擴充功能中正確設定並發佈。

如果您已驗證上述所有設定，但仍看不到轉換資料，請在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)為您的組織開啟支援票證。 包含廣告網路帳戶的[!UICONTROL Account ID]。

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [總覽](overview.md)
>* [由 [!DNL Customer Journey Analytics]](ids.md)使用的Adobe Advertising ID
>* [必要條件](prerequisites.md)
>* [設定資料收集、資料傳輸及報告](set-up.md)
>* Customer Journey Analytics中的[Adobe Advertising量度和維度](advertising-data-in-cja.md)
>* （Adobe Analytics使用者） [收集AMO ID和EF ID的歷史資料，以用於Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
