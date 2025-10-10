---
title: 決策樹配置
description: 瞭解使用目標定位的體驗的決策樹配置。
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: 4057f413b58343580a965f9a419af1e002892ff6
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# [!DNL Creative]個體驗的決策樹配置

當您為體驗啟用「[!UICONTROL Targeting]」選項時，您會使用決策樹設定體驗。

最初，每個決策樹都是以根層級「全部」開始。 您可以新增一或多個目標節點，然後將創意套件組合指派至決策樹每個分支中的最終節點。 依照預設，決策樹會垂直顯示，但您可以選擇改為水準檢視決策樹。

![沒有目標的垂直決策樹範例](/help/creative/assets/experience-decision-tree-no-targets.png "沒有目標的垂直決策樹範例")

![沒有目標的水準決策樹範例](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "沒有目標的水準決策樹範例")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
-->

## 辭彙

**樹狀結構：**&#x200B;整體決策結構為具有分支的樹狀結構。

**目標節點：**&#x200B;分支中的目標。

**分葉節點：**&#x200B;指派給最終目標節點的一組創意。

## 決策樹中的目標

每個決策樹最多可以有五個層次的目標。 體驗層級目標會與DSP的鎖定目標選項一起套用；階層鎖定目標行為可能會因DSP而異。 請確定您的廣告體驗包含與您將要實作它的行銷活動相容的目標定位。

每個目標層級可包含多個分支，每個分支有一或多個具有相同目標型別的節點（受眾區段、地理位置型別、指定資料傳遞索引鍵的值、指定重新定位畫素的屬性或裝置類別）。 您可以在已為其指定預設影像創意或視訊創意的每個廣告大小中，將創意組合指派給最低層級的目標節點。

![含有目標的決策樹範例](/help/creative/assets/experience-decision-tree.png "含有目標的決策樹範例")

將目標節點新增至最終層級時，請指定新節點的目標。 系統會自動為不符合指定目標的所有人建立其他同層級節點「其他專案」。 然後您可以新增其他同層級節點，其中包含相同型別的不同目標。

但是，當您在現有層級之間插入目標節點時，新層級的第一個節點最初會被指派給「全部」。 若要識別特定目標，請在相同層次建立同層級目標節點，您可為其指定實際目標。 此動作會建立目標節點，並將「所有」節點取代為「其他一切」節點（包括先前指派給「所有」的所有創意組合）。 然後您可以新增其他同層級節點，其中包含相同型別的不同目標。

對於所有父節點，您可以選擇複製所有子目標節點和創意組合，並將其貼到相同層級的另一個節點中。 您可以將貼上的節點新增至現有框架，或以它們取代現有框架。

## 決策樹中的創意內容

將創意套件組合指派至體驗中的每個最終目標節點。

在具有創意套裝的每個節點內，您可以選擇旋轉包含的創意內容，a)以演演算法最佳化點進率或自訂目標，b)根據指定的權重，或c)以特定順序旋轉。 您也可以選擇以指定的時間順序旋轉創意，或旋轉相同選項的任何組合。

您可以視需要自訂個別創意內容的登陸頁面URL、曝光追蹤URL和點選追蹤URL。<!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [關於Advertising Creative 2.0](experience-about.md)中的體驗
>* [建立鎖定目標的體驗](/help/creative/experiences/experience-create-targeting.md)
>* [目標體驗設定](/help/creative/experiences/experience-settings-targeting.md)
