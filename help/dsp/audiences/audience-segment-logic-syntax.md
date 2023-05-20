---
title: 受眾段邏輯的語法
description: 引用可用於定義受眾段邏輯的語法。
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 受眾段邏輯的語法

建立可重用的受眾時，可以使用字母數欄位ID（鍵）和以下語法手動定義段邏輯：

* ()表示組
* `||` 為 [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp; [!DNL AND]
* ! 為 [!DNL NOT] （排除）

>[!NOTE]
>
>* 所有指定的段組都包括在內，除非它們前面有！ （不包括他們）。
>* 你可以 [查找受眾的段ID](reusable-audience-clipboard.md) 從 [!UICONTROL Audiences] > [!UICONTROL All audiences]。


例如，以下邏輯：

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

平均數（普通英語）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>在放置設定中，可以將保存的受眾用作顯式目標受眾或作為單獨的受眾從目標中排除。 確保段邏輯反映您將使用受眾的目的。

>[!MORELIKETHIS]
>
>* [將可重用受眾的段鍵複製到剪貼簿](reusable-audience-clipboard.md)
>* [關於受眾管理](audience-about.md)
>* [建立可重用的受眾](reusable-audience-create.md)
>* [受眾設定](audience-settings.md)
>* [可用的第三方資料提供程式](third-party-data-providers.md)

