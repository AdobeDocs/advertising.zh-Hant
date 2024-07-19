---
title: 在 [!DNL Freewheel]中設定PG交易的概觀
description: 瞭解在 [!DNL Freewheel]上執行發行者程式化保證交易的廣告的必要條件和額外步驟。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 在[!DNL Freewheel]中設定程式化預留交易的概觀

在[!DNL Freewheel]上設定與發行者的程式化預留交易需要額外的許可權和步驟。

>[!PREREQUISITES]
>
>請與您的Adobe帳戶團隊合作，確保您的[!DNL DSP]帳戶具有下列許可權：
>
>* 使用[!DNL FreeWheel]程式化保證工作流程的許可權，此工作流程是向[!DNL FreeWheel]提交程式化保證交易的廣告所必需的。
>
>* （如果您與英國發行商合作，而對方要求每個廣告都有[!DNL Clearcast]個時鐘編號），請允許您將時鐘編號加入廣告中。

## 工作流程

1. 使用交易中指定的媒體型別來建立廣告。

   對於某些英國發行者，您的廣告必須包含[!DNL Clearcast]時鐘編號。

1. [接受您已於[!DNL Freewheel]使用交易識別碼收件匣與發行者交涉的交易ID](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)。

   接受交易後，請依照提示操作1)選取要用於交易的廣告，2)建立程式化預留預設位置以提供廣告。

1. [將廣告提交至 [!DNL Freewheel]](freewheel-submit.md)

   廣告必須先提交並核准，才能執行。

1. [檢查廣告提交狀態](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [在交易識別碼收件匣中接受交易](deal-id-inbox-accept.md)
>* [提交程式化保證交易的廣告給 [!DNL Freewheel]](freewheel-submit.md)
>* [檢查 [!DNL FreeWheel] 程式化預留交易的廣告狀態](freewheel-check-status.md)
>*  [!DNL Freewheel] 廣告提交的[錯誤碼](freewheel-error-codes.md)
