---
title: 建立決策樹定位的體驗
description: 瞭解如何使用AI驅動或手動決策樹編輯器建立目標式廣告體驗。
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%
---
# 建立決策樹定位的體驗

使用決策樹建立目標式廣告體驗。 每個體驗都會使用來自單一創意資料庫的廣告。

AI驅動編輯器(Beta)依預設會開啟。 您可以透過AI代理程式設定樹狀結構，或直接編輯其畫布。 您也可以切換至現有的手動編輯器。

>[!NOTE]
>
>* 建立目標體驗後，您之後將無法變更為使用不同工作流程的非目標體驗。
>* 請確定您的廣告體驗包含與您將要實作它的行銷活動相容的目標定位。 階層式鎖定目標行為可能因DSP而異。 當您將廣告體驗標籤上傳至Advertising DSP並將其附加至刊登版位時，廣告層級鎖定目標會套用至刊登版位層級鎖定目標上方（而非取代該）。 例如，如果位置鎖定澳洲的使用者，而廣告鎖定日本的使用者，則廣告會鎖定「其他所有人」分支。

## 建立體驗

1. 在主功能表中，按一下&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 按一下&#x200B;**[!UICONTROL Create New Experience]**。

1. 輸入[一般體驗設定](experience-settings-targeting.md)，並啟用&#x200B;**[!UICONTROL Targeting]**。

1. 按一下&#x200B;**[!UICONTROL Create]**。

   AI導向的決策樹編輯器會針對新體驗開啟。

1. 使用下列任一程式來設定樹狀結構。

## 使用AI導向編輯器設定樹狀結構(Beta) {#ai-editor}

1. 在對話中，說明您要的目標定位結構，包括每個分支的條件，以及如何處理不符合指定目標的檢視者。

1. 檢閱畫布中的樹狀結構。 若要要求變更，請在交談中說明。 在與畫布互動之前，請等候助理完成處理。

1. （可選）直接在畫布中調整樹狀結構：

   * [新增最終層級目標](experience-target-node-add-final.md#ai-editor)、[插入目標層級](experience-target-node-add-inner.md#ai-editor)或[新增同層級目標](experience-target-node-add-sibling.md#ai-editor)。

   * [複製子節點和創意](experience-target-node-copy.md#ai-editor)或[刪除節點](experience-target-node-delete.md#ai-editor)。

1. [將創意組合指派給最終節點](experience-assign-creative-bundles.md#ai-editor)，並選擇性[自訂創意最佳化和排程](experience-optimization-scheduling-targeting.md)和[追蹤URL](experience-tracking-urls-targeting.md#ai-editor)。

   若要發佈體驗，您必須將套件組合指派給每個最終節點，或使用體驗的預設創意。 儲存時，您可以將預設值指派給未指派的節點。

1. （可選）編輯一般體驗設定：

   1. 若要儲存您要保留的任何樹狀結構變更，請按一下&#x200B;**[!UICONTROL Save]**。

   1. 按一下&#x200B;**[!UICONTROL Experience Form]**，然後按一下&#x200B;**[!UICONTROL Yes]**&#x200B;以捨棄未儲存的樹狀結構變更並開啟表單。

   1. 編輯[一般體驗設定](experience-settings-targeting.md)，然後按一下&#x200B;**[!UICONTROL Save]**。

      AI驅動編輯器隨即開啟。

1. [儲存體驗](#save)。

## 使用手動編輯器設定樹狀結構 {#manual-editor}

1. 在AI驅動編輯器中，按一下&#x200B;**[!UICONTROL Manual Decision Tree]**，然後按一下&#x200B;**[!UICONTROL Yes]**&#x200B;以離開AI驅動編輯器。

   在切換前儲存您要保留的任何AI編輯器變更。 確認交換器會捨棄未儲存的樹狀結構變更。

1. （可選）變更檢視設定：

   * 移動滑桿來放大或縮小。

   * 按一下![以垂直樹狀檢視](/help/creative/assets/tree-vertical.png "以垂直樹狀檢視")或![以水準樹狀檢視](/help/creative/assets/tree-horizontal.png "以水準樹狀檢視")，在垂直和水平檢視之間切換。

   您的檢視設定會儲存到您登出為止。

1. 設定廣告目標和對應的創意內容：

   * [新增最終層級目標](experience-target-node-add-final.md#manual-editor)、[在節點之間插入目標](experience-target-node-add-inner.md#manual-editor)，或[新增同層級目標](experience-target-node-add-sibling.md#manual-editor)。

   * [複製子節點和創意](experience-target-node-copy.md#manual-editor)或[刪除節點](experience-target-node-delete.md#manual-editor)。

   * [指派創意組合](experience-assign-creative-bundles.md#manual-editor)，並選擇性[自訂創意最佳化和排程](experience-optimization-scheduling-targeting.md)和[追蹤URL](experience-tracking-urls-targeting.md#manual-editor)。

1. （選擇性）若要編輯一般體驗設定，請按一下&#x200B;**[!UICONTROL Experience Form]**&#x200B;並編輯[一般體驗設定](experience-settings-targeting.md)。

1. [儲存體驗](#save)。

## 儲存體驗 {#save}

以下步驟適用於兩個編輯器。

{{$include /help/_includes/experience-save.md}}

## 儲存體驗的廣告標籤和視訊轉碼

當體驗上線時，[!DNL Creative]會自動為每個適用的創意大小或視訊持續時間建立一個廣告標籤。 然後，您可以[匯出廣告標籤，並在DSP](/help/creative/experiences/experience-tag-export.md)中實作該標籤。

對於視訊廣告體驗，視訊創意內容會由Adobe Advertising DSP自動轉碼為VAST 2.0標籤，以便您預覽。 您可以選擇將其他DSP[&#128279;](experience-tag-video-transcoding.md)的轉碼套用至任何視訊廣告體驗標籤。

>[!MORELIKETHIS]
>
>* [目標體驗設定](experience-settings-targeting.md)
>* [新增目標節點至最終層級](experience-target-node-add-final.md)
>* [在節點之間插入目標節點](experience-target-node-add-inner.md)
>* [在節點之間新增同層級目標節點](experience-target-node-add-sibling.md)
>* [將子節點和創意內容複製到相同層級的另一個節點](experience-target-node-copy.md)
>* [將創意內容指派給最終節點](experience-assign-creative-bundles.md)
>* [自訂指派組合中創作的追蹤URL](experience-tracking-urls-targeting.md)
>* [自訂創意最佳化與排程](experience-optimization-scheduling-targeting.md)
>* [匯出並實作即時體驗的廣告體驗標籤](/help/creative/experiences/experience-tag-export.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [檢視體驗的變更記錄](/help/creative/experiences/experience-view-change-log.md)
