---
title: 檢視警示
description: 瞭解如何檢視行銷活動和行銷活動元件的警示和建議解決方案。
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# 檢視警示

*Beta功能*

DSP可協助您識別任何行銷活動或行銷活動元件何時發生問題。 對於每個問題，DSP都會建立具有時間戳記的警報，以及解決此問題的建議動作。 警報的原因包括設定問題（例如，當投放位置沒有附加廣告或交易設定錯誤時）、廣告拒絕和行銷活動健康問題（例如廣告傳送或效能不佳）。 促銷活動、套件、位置、廣告和交易層級提供警報。

警報可在下列位置使用：

* A [!UICONTROL Pulse Panel] 圖示於 [!UICONTROL Campaigns]， [!UICONTROL Packages] 和封裝詳細資料， [!UICONTROL Placements]、和 [!UICONTROL Ads] 檢視會指出該檢視中的專案是否有任何警示。 當圖示有藍色圓點(![警報可用時的Pulse面板圖示](/help/dsp/assets/alerts-panel.png "警報可用時的Pulse面板圖示"))，警示可供使用。 沒有可見點時(![無可用警報時的Pulse Panel圖示](/help/dsp/assets/alerts-panel-empty.png "無可用警報時的Pulse Panel圖示"))，沒有可用的警示。

* 相同檢視中的資料表包含&quot;[!UICONTROL Alerts]「欄」，指出專案（或其元件）何時發生問題。 警示指標包括「嚴重」(![關鍵](/help/dsp/assets/indicator-critical.png "關鍵"))，「警告」(![警告](/help/dsp/assets/indicator-warning.png "警告"))和「資訊」(![資訊](/help/dsp/assets/indicator-information.png "資訊"))。

您可以開啟任何警報的相關行銷活動管理檢視，以便視需要編輯設定以解決問題。

您也可以選擇略過個別警報，將其從 [!UICONTROL Pulse] 面板。

基礎問題解決後，警報和警報指示器會自動消失。

## 在中檢視警示 [!UICONTROL Pulse Panel]

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 執行下列任一項作業：

   * （適用於此檢視的所有警報）在任何行銷活動管理檢視的工具列右側，按一下 ![警報可用時的Pulse面板圖示](/help/dsp/assets/alerts-panel.png "警報可用時的Pulse面板圖示").

   * （特定行銷活動的所有警報）按一下行銷活動列的警報指示器，然後按一下 **[!UICONTROL View in Pulse panel]**.

   * （針對特定套件、位置或廣告的所有警示）執行下列動作：

      1. 按一下行銷活動名稱。

      1. 在子功能表中，按一下 **[!UICONTROL Packages]**， **[!UICONTROL Placements]**，或 **[!UICONTROL Ads]** 以開啟相關的促銷活動元件檢視。

      1. 按一下套件、位置或廣告列的警報指示器，然後按一下 **[!UICONTROL View in Pulse Panel]**.

   所有與行銷活動及其元件相關聯的警報（包括目標交易）都會列在清單中。 依照預設，嚴重警示會先列出。

1. （可選）若要根據偵測到的第一個日期將警報分組，或依警報狀態、元件狀態、元件型別或特定促銷活動名稱篩選警報，請按一下 ![篩選按鈕](/help/dsp/assets/filter.png) 在面板的右上方，選取篩選選項，然後按一下 **[!UICONTROL Apply]**.

1. 若要檢視特定警示型別的所有受影響行銷活動元件清單，請按一下警示名稱，例如&quot;[!UICONTROL Package: No Active Placement (*N*)]「。 若要檢視每個受影響元件的詳細資訊，包括建議的動作，請按一下 [!UICONTROL EXPAND ALL] 或按一下元件名稱。 若要開啟任何受影響元件的相關促銷活動管理檢視，以便進行建議的變更，請將游標停留在元件名稱上，然後按一下 ![前往檢視](/help/dsp/assets/go-to-view.png "前往檢視").

1. （選擇性）若要忽略（隱藏）警示，請將游標停留在元件名稱上，然後按一下 ![忽略](/help/dsp/assets/alert-ignore.png "忽略")，然後按一下 **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

在略過警示以復原動作後，您還有幾秒鐘的時間。 選項訊息關閉後，您就無法取消動作。

1. （選用）若要擷取已忽略的警報，請篩選警報以顯示 [!UICONTROL Alert Status] / &quot;[!UICONTROL All]「或」[!UICONTROL Ignored].」 若要取消忽略警示，請將游標停留在元件名稱上，然後按一下 ![取消忽略](/help/dsp/assets/alert-un-ignore.png "取消忽略").

## 關閉 [!UICONTROL Pulse Panel]

* 在工具列右側，按一下 ![警報可用時的Pulse面板圖示](/help/dsp/assets/alerts-panel.png "警報可用時的Pulse面板圖示") 或 ![無可用警報時的Pulse Panel圖示](/help/dsp/assets/alerts-panel-empty.png "無可用警報時的Pulse Panel圖示").

>[!MORELIKETHIS]
>
>* [Campaign Management檢視中的效能報表型別](campaign-reports-about.md)
