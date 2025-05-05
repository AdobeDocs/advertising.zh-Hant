---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# RSA廣告設定中的廣告標題欄位

**[!UICONTROL Ad Titles]：**&#x200B;至少有三個和最多十五個廣告標題（標題），並附選用的定點陣圖釘。 廣告網路顯示的廣告最多有三個標題；至少輸入三個。 每個標題的長度上限為30個字元，包括任何動態
文字（例如關鍵字和廣告自訂者的值）。

若要插入廣告自訂程式，請使用下列格式，其中`Default text`是當摘要檔案未包含有效值時要插入的選用值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

若要將標題釘選至特定位置，請選取釘選選項（例如&quot;[!UICONTROL Pinned at position 1]&quot;）。 每個位置必須至少有一個標題可用。 如果您將多個標題釘選至相同位置，則最終廣告會一律在指定位置包含這些標題之一。 釘選到位置3的標題可能無法與廣告一起顯示。

若要新增其他標題，請按一下&#x200B;**[!UICONTROL + Add]**。
