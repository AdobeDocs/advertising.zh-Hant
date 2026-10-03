---
title: 對象區段邏輯的語法
description: 參考您可用來定義對象區段邏輯的語法。
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: 'https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: b4dc2b3d-fdb5-55cd-9190-f1076d8563e4
    internal-label: DSP Audiences
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%
---
# 對象區段邏輯的語法

建立可重複使用的對象時，您可以使用英數字元區段ID （索引鍵）及下列語法來手動定義區段邏輯：

* ()表示群組
* [!DNL OR]的`||` <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* [!DNL AND]的&amp;&amp;
* ! 針對[!DNL NOT] （排除）

>[!NOTE]
>
>* 所有指定的區段群組都會包括在內，除非其前面有！ （會將其排除）。
>* 您可以[從[!UICONTROL Audiences] > [!UICONTROL All audiences]尋找對象](reusable-audience-clipboard.md)的區段ID。

例如，下列邏輯：

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

表示（純英文）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>在位置設定中，您可以使用儲存的對象作為明確鎖定的對象，或作為單獨的對象來排除鎖定的對象。 請確定您的區段邏輯反映使用對象的目的。

>[!MORELIKETHIS]
>
>* [將可重複使用對象的區段金鑰複製到剪貼簿](reusable-audience-clipboard.md)
>* [關於對象管理](audience-about.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [對象設定](audience-settings.md)
>* [可用的協力廠商資料提供者](third-party-data-providers.md)
