---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# RSA廣告設定中的廣告說明欄位

**[!UICONTROL Ad Descriptions]：**&#x200B;至少有兩個、最多四個廣告說明（含選用的位置圖釘）。 廣告網路會顯示最多有兩個說明的廣告；至少輸入兩個。 每個說明的長度上限為90個字元，包括任何動態文字（例如關鍵字和廣告自訂者的值）。

若要插入廣告自訂程式，請使用下列格式，其中`Default text`是當摘要檔案未包含有效值時要插入的選用值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

若要將說明釘選至特定位置，請選取釘選選項（例如&quot;[!UICONTROL Pinned at position 1]&quot;）。 每個位置必須至少有一個說明。 如果您將多個說明釘選至相同位置，則最終廣告會一律在指定位置包含這些說明之一。 釘選到位置2的說明可能無法與廣告一起顯示。

若要新增其他說明，請按一下&#x200B;**[!UICONTROL + Add]**。
