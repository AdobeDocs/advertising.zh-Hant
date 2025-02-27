---
title: 字彙表
description: 請參閱重要辭彙的定義。
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 字彙表 {#glossary}

*已關閉的Beta*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**點進：**&#x200B;導致轉換的廣告點選。

**資料傳遞目標：**&#x200B;資料傳遞目標允許根據DSP、發行者或合作夥伴即時提供的資料來選取廣告元素。 其中可能包含協力廠商資料。

<!-- verify this -->在廣告體驗中，每個資料傳遞目標最多可包含五個索引鍵/值組；您可以在該層級的第一個目標節點中指定索引鍵和至少一個值，而同層級目標節點可使用相同的索引鍵。 每個鍵值組都會附加為巨集，作為此體驗的廣告標籤。 在廣告曝光時，DSP、發佈者或合作夥伴負責將值取代為該曝光專屬的資料。 此資訊會傳回[!DNL Creative]，以便根據體驗中定義的規則顯示適當的廣告體驗。

例如，若要將一或多個可能的創意目標定位為女性且位於區段1234中的檢視者，您可以為目標節點設定資料傳遞目標`gender=female`和`segment=1234`。 提供曝光數的DSP會使用性別和區段資訊填入標籤，而符合指定要求的訪客則會顯示其中一項相關創意內容。

**參與至：**&#x200B;廣告參與（例如捲動轉盤廣告或展開廣告）會導致轉換。 此類事件與按一下廣告以存取登陸頁面或登陸頁面上的事件不同。

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**閱覽：**&#x200B;廣告曝光次數或曝光字串，使用者不按廣告即會導致轉換。
