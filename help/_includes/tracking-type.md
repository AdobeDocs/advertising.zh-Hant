---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# 帳戶和行銷活動設定中的「追蹤型別」欄位

**[!UICONTROL Tracking Type]：** 產生URL的方法：

* *[!UICONTROL EF Redirect]* （預設）：適用於想使用Adobe廣告轉換追蹤服務的客戶。 此方法會產生唯一的點選追蹤ID，並將使用者重新導向至AdobeAdvertising伺服器以供追蹤，然後再傳送至使用者端的登陸頁面。

   此方法有預設追蹤選項，您可以選擇性地加以自訂，您也可以指定要附加至每個URL的引數。

* *[!UICONTROL No EF Redirect]：* 適用於只想使用自己點選追蹤程式碼的使用者端。 搜尋、Social和Commerce不提供點選追蹤ID或重新導向程式碼。 對於具有目的地URL的帳戶，每個目的地URL都與基本URL相同。

   **附註：**

   * 只有代理商帳戶管理員、Adobe帳戶管理員和管理員使用者可以變更此值。
   * 如果您變更追蹤方法，則必須重新產生帳戶的追蹤URL。
   * 行銷活動層級追蹤選項會覆寫帳戶層級設定。
