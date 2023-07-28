---
title: 模型精度報表設定
description: 瞭解模型準確性報表的必要和選用設定。
exl-id: 0d0e6ace-3cb3-4cf4-8cbf-3dd5a356f35e
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '1782'
ht-degree: 0%

---

# 模型精度報表設定

| 標籤 | 引數 | 說明 |
|----|----|----|
| 不適用 | [!UICONTROL Name] | （選用）報表和範本的名稱（若您將報表另存為範本）。 如果您套用現有的範本，則預設會填入範本名稱。 如果您未套用範本或輸入名稱，則報表命名為 <code><client name>-<date and time>-<report type></code> (例如「acme - 2009年4月3日11」:25:上午19:00 PDT — 關鍵字」)（預設）。<br><br>您可以選擇輸入自訂名稱，但不要使用副檔名。<br><br>如果您要建立範本以 [將報表傳送至FTP目錄](/help/search-social-commerce/reports/automation/ftp-reports.md)，您就可以選擇在檔案名稱的任何位置加入「CSV」（大寫字母），以CSV格式（而非預設的TSV格式）建立檔案。 另請參閱 [傳送至FTP目錄之報告的檔案名稱需求](/help/search-social-commerce/reports/automation/ftp-reports.md). |
|  | [!UICONTROL Save as template] | （除非您想要根據排程執行報表，否則為選用）將報表設定儲存為範本，可在 [!UICONTROL Reports] > [!UICONTROL Report Templates] 檢視並重複使用以建立新報表。 若要將報表另存為範本，請選取核取方塊。<br><br>若要根據排程執行報表，您必須將設定儲存為範本。<br><br><b>注意：</b> 您可以將目前的引數集儲存為新範本，即使它以現有範本為基礎。 |
|  | [!UICONTROL Type] | 要產生的報表型別。 |
| [!UICONTROL Basic  Settings] | [!UICONTROL Template] | （選用）要套用的報表範本，它會根據範本預先填入報表選項。 系統會列出為報表型別儲存且可供您使用的所有範本。<br><br>如果選取範本，您仍可變更報表選項，甚至可將報表另存為新範本。 |
|  | [!UICONTROL Data Aggregation] | ([!UICONTROL Forecast Accuracy Report only])報表每一列應呈現的時間單位。 唯一的選項是 <i>[!UICONTROL Daily]</i>. |
|  | [!UICONTROL Date Range] | 要產生資料的日期範圍：<ul><li><i>[預設範圍]：</i> 常見的時間增量清單，範圍從 <i>[!UICONTROL Today]</i> 至 <i>[!UICONTROL Last 180 Days]</i>. 預設值為 <i>[!UICONTROL Last 7 Days]</i>，會報告資料可用的過去七天。 <b>注意：</b> <i>[!UICONTROL Last Month]</i>， <i>[!UICONTROL Last 3 Months]</i>、和 <i>[!UICONTROL Last 6 Months]</i> 顯示前一個日曆月的資料。</li><li><i>[!UICONTROL Custom Date Range]：</i> 指定開始日期和結束日期。 以YYYY/MM/DD或M/D/YYYY格式輸入日期，或按一下 ![行事曆](/help/search-social-commerce/assets/calendar.png "行事曆") 欄位旁邊，並選取日期。</li></ul> |
|  | [!UICONTROL Conversions Based on] | 如何報告轉換資料：<ul><li><i>[!UICONTROL Transaction date]</i> （預設值）：檢視交易日期在指定期間內發生的交易。 此選項會顯示指定期間內已賺取的收入。</li><li><i>[!UICONTROL Click date]：</i> 檢視在指定時段內因點按而發生的交易。 當產品組合在點按和交易之間有重大延遲時，此選項可用於計算產品組合的每次點按歷史收入，其指示一段時間內預期的收入行為。</li></ul> |
|  | \[主要篩選器\] | 要包含的投資組合。 依預設，如果您未進行選取，所有產品組合的資料都會包含在報表中。 您可選擇指定個別投資組合，以縮小要報告的資料範圍。<br><br>若要選取投資組合，請選取投資組合名稱旁的核取方塊，然後按一下>>將其移至 [!UICONTROL Selected Filters] 欄。<br><br><b>附註：</b><ul><li>依預設，僅列出使用中和最佳化的產品組合。 若要檢視暫停和刪除的投資組合，請按一下 ![向下鍵](/help/search-social-commerce/assets/arrow-down-expand.png "向下鍵") 旁邊 <b>[!UICONTROL Show]</b>，並選取 <b>[!UICONTROL All]</b>.</li><li>產生的資料會用於目前對應至指定產品組合的行銷活動。 其中不包含日期範圍內位於產品組合中但尚未存在的行銷活動的資料。</li></ul> |
| [!UICONTROL Columns] | \[報表欄\] | 報表中顯示的資料欄及其順序：<ul><li>若要新增欄，請按一下左欄中的量度名稱，然後按一下 ![向右鍵](/help/search-social-commerce/assets/arrow-right-customize.png "向右鍵").</li><li>若要移除欄，請按一下右側欄中的測量結果名稱，然後按一下 ![向左鍵](/help/search-social-commerce/assets/arrow-left-customize.png "向左鍵").</li><li>若要將報表中的欄移至左側，請按一下右欄中的量度名稱，然後按一下 ![向上鍵](/help/search-social-commerce/assets/arrow-up-customize.png "向上鍵").</li><li>若要將報表中的欄移至右側，請按一下右欄中的量度名稱，然後按一下 ![向下鍵](/help/search-social-commerce/assets/arrow-down-customize.png "向下鍵").</li></ul> |
|  | [!UICONTROL Order Results/Limit Rows by] | ([!UICONTROL Forecast Accuracy Report] 僅限)依據報表中包含的最多兩欄來排序報表。 每種報表型別的預設值不同。若要自訂排序順序，請選取報表欄，然後選取 <i>[!UICONTROL Ascending]</i> （顯示從A到Z或從1到100的結果）或 <i>[!UICONTROL Descending]</i> （顯示從Z到A或從100到1的結果）。 指定至少一個要排序的資料行。 如果您依兩欄排序，則報表會先依指定的第一欄排序，然後再依指定的第二欄排序。 |
|  | [!UICONTROL Share with others] | ([!UICONTROL Forecast Accuracy Report] 僅限)允許有權存取相同廣告商資料的其他使用者檢視產生的報告，以及（如果您將報告另存為範本）使用範本但不編輯或刪除它。 依預設，不會選取此選項。 <b>注意：</b> 無論此設定為何，您的報表和範本一律顯示給更高（管理員）角色的所有使用者，以及任何指派的「Adobe帳戶專案團隊」成員。 |
| [!UICONTROL Advanced Filters] | \[進階篩選器\] | ([!UICONTROL Forecast Accuracy Report] 僅限於)只有在量度的值符合指定條件時，才會傳回列；量度不需要納入報表中作為欄。 可用量度清單會依報告型別而異，但可能包括廣告商的自訂衍生量度、每個廣告網路和產品組合元件的ID和屬性名稱(例如 [!UICONTROL Campaign ID] 和 [!UICONTROL Campaign Status])、廣告商的收入量度（交易屬性），以及廣告網路中與點選相關的量度。 可用的運運算元包括 <i>[!UICONTROL contains]</i>， <i>[!UICONTROL starts with]</i>， <i>[!UICONTROL equals]</i>， <i>[!UICONTROL is greater than]</i>， <i>[!UICONTROL is greater than or equal to]</i>， <i>[!UICONTROL is less than]</i>， <i>[!UICONTROL is less than or equal to]</i>，或 <i>[!UICONTROL isn't equal to]</i>.<br><br>若要套用一或多個篩選器，請執行下列動作：<ul><li>選取量度和運運算元，然後輸入適用的值。 例如，若只要傳回超過100次點選的關鍵字，請選取 [!UICONTROL Clicks]，選取 [!UICONTROL >]，然後在輸入欄位中輸入100。</li><li>（若要套用其他篩選器）對於每個其他篩選器，請按一下 **[!UICONTROL +Add Filter]**，選取 **[!UICONTROL AND]** 或 **[!UICONTROL OR]**，選取量度和運運算元，然後輸入適用的值。</li></ul> |
| [!UICONTROL Attribution] | [!UICONTROL Rule] | (僅使用Adobe Advertising轉換追蹤服務的廣告商)在報表中，如何在一連串導致轉換的事件中歸因轉換資料（可能跨多個廣告頻道和產品組合）：<ul><li><i>[!UICONTROL First Event]：</i> 將轉換歸因於廣告商的系列中的第一個付費點選 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 或者，如果沒有發生付費點按，則為廣告商的最近一次曝光 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).</li><li><i>[!UICONTROL Weight First Event More]：</i> 將轉換歸因於廣告商發生之系列中的所有事件 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)，但會給予第一個事件最大的權重，並連續給予下列事件較小的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>[!UICONTROL Even Distribution]:</i></li> 將轉換平等地歸因於系列中的每個事件廣告商的瀏覽權數，而不是印象覆寫權數。</li><li><i>[!UICONTROL Weight Last Event More]：</i> 將轉換歸因於廣告商發生之系列中的所有事件 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)，但會給予最後一個事件最大的權重，並連續給予前一個事件較小的權重。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li><li><i>[!UICONTROL Last Event]</i> （預設）：將轉換歸因於廣告商的系列中的最後一個付費點選 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 或者，如果沒有發生付費點按，則為廣告商的最近一次曝光 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j).</li><li><i>U形：</i> 將轉換歸因於廣告商發生之系列中的所有事件 [按一下回顧視窗](/help/search-social-commerce/glossary.md#c-d) 和 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j)，但會給予第一個事件和最後一個事件最大的權重，而連續給予轉換路徑中間事件的權重較低。 當轉換前同時有付費點按和曝光時，指定的曝光覆寫權數會進一步套用至曝光。 當轉換之前只有曝光次數時，曝光次數會根據廣告商的瀏覽權數（而非曝光次數覆寫權數）加權。</li></ul><b>附註：</b><ul><li>歸因規則適用於顯示廣告的曝光數，以及任何頻道中付費廣告的點選數。 它們不適用於付費搜尋或社交廣告的曝光數，無法在事件層級進行追蹤。</li><li>當您使用任何歸因規則(除了&quot;[!UICONTROL Last Event]「規則，導致轉換的事件可能發生在多個產品組合中。 若是如此，則只有在報表中包含這些產品組合中的廣告或關鍵字時，報表才會包含轉換的資料。</li></ul> |
|  | [!UICONTROL Impression Override Weight] | (適用於所有歸因規則，但不包括 [!UICONTROL Last Event] 或 [!UICONTROL First Event])當轉換前面同時有付費點按和曝光數時，會將指定的轉換值百分比歸因於廣告商中發生的曝光數 [曝光回顧期間](/help/search-social-commerce/glossary.md#i-j). 預設值為10%；您可以將此值變更為從0到100的任何整數。 此值僅用於報表中。<br><br>如果轉換之前只有曝光數，則廣告商的 [檢視權數](/help/search-social-commerce/glossary.md#u-v)會套用至曝光數，而非曝光數覆寫權重。 |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Report Schedule] | (選用；僅適用於&quot;[!UICONTROL Save as template]」選項已選取)何時執行報表： <i>[!UICONTROL Now]</i> （只執行一次報表；預設）， <i>[!UICONTROL Daily]</i>， <i>[!UICONTROL Weekly on] [星期]</i>，或 <i>[!UICONTROL Every Month] [日期]</i>. 所有期間，除了 <i>[!UICONTROL Now]</i>，在廣告商的時區中選取小時，從上午9:00開始。 |
|  | [!UICONTROL Email Recipients] | <b>注意：</b>  此設定僅在電子郵件通知用於 [!UICONTROL Reports] 為 [啟用範圍 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>報表完成或因錯誤而取消時，要傳送通知的已註冊Search、Social和Commerce使用者電子郵件地址。 依預設，會輸入您使用者帳戶的地址。 若要指定多個地址，請用逗號、空格或新行加以區隔。 如果報表被排程重複執行，則每次完成報表時都會傳送通知。 |
|  | [!UICONTROL Email Notification] | <b>注意：</b>  此設定僅在電子郵件通知用於 [!UICONTROL Reports] 為 [啟用範圍 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>(當 [!UICONTROL Email Recipients] 已指定)傳送至任何指定地址的電子郵件通知中要包含的內容：<ul><li><i>[!UICONTROL Notification Only]</i> （預設值）：僅傳送報表完成或失敗的通知，不含附件。 通知包含所有報表格式的暫時下載連結。</li><li><i>[!UICONTROL XLS Attachment]：</i> 在檔案小於約10 MB時加入XLS格式的已完成報表副本。 超過1 MB的檔案會經過壓縮。</li><li><i>[!UICONTROL TSV Attachment]：</i> 在檔案小於約10 MB時加入TSV格式的已完成報表副本。 超過1 MB的檔案會經過壓縮。</li><li><i>[!UICONTROL CSV Attachment]：</i> 在檔案小於約10 MB時加入CSV格式的已完成報表副本。 超過1 MB的檔案會經過壓縮。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [關於模型精度報表](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [此 [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [此 [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [產生模型準確度報告](model-accuracy-report-generate.md)
