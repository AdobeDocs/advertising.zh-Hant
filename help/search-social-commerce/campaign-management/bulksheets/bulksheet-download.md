---
title: 下載/建立Bulksheet檔案
description: 瞭解如何透過下載廣告網路的帳戶資料來建立Bulksheet檔案。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 0%

---

# 下載/建立Bulksheet檔案

您可以使用一個或多個帳戶的自訂設定來建立大量表單 [支援的廣告網路](bulksheet-about.md#bulksheet-functionality-by-network). 大量表單包含Search、Social和Commerce中的資料。

對於同步的行銷活動，您可以選擇在下載資料之前與廣告網路同步，以確保包括廣告網路端的最新資料變更。 對於所有廣告網路，您可以選擇產生新的點選追蹤URL以包含在檔案中。

>[!NOTE]
>
>您也可以 [根據行銷活動管理檢視中的可見欄建立Bulksheet檔案](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. 在主功能表中，按一下 **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. 在工具列中，按一下 **[!UICONTROL Download Bulksheet]**.

1. 指定 [大量表單設定](#bulksheet-download-settings)：

1. 在**上[!UICONTROL Selections] 標籤，在欄位中輸入或選取資訊。

1. （可選）按一下 **[!UICONTROL Rows and Columns]** 標籤，指定要在大量表單中包含列的帳戶元件和元件狀態，然後指定每個所選元件要包含的欄。

   如需可用大量表單列的清單，請參閱&quot;[依廣告網路大量表單列](#bulksheet-rows-by-ad-network).」

1. （可選）按一下 **[!UICONTROL Filters]** 標籤，然後指出特定行銷活動、廣告群組、廣告/創意、關鍵字、位置和其他要包含在Bulksheet中實體的條件：

   1. 選取引數（實體名稱或ID；或廣告、關鍵字或位置的任何元素）、選取運運算元，然後輸入適用的值。 例如，只傳回標題中包含「鞋子」的廣告 [!DNL Google Ads] 帳戶，選取 *標題*，選取 *[!UICONTROL contains]*，然後輸入 `shoes` 在輸入欄位中。

   1. （若要套用其他篩選器）對於每個其他篩選器，請按一下 **[!UICONTROL +Add Filter]**，選取 **[!UICONTROL AND]** 或 **[!UICONTROL OR]**，選取廣告元素或關鍵字和運運算元，然後輸入適用的值。

1. 按一下 **[!UICONTROL Download].

當工作開始時，視窗會顯示通知，但會保持開啟狀態，以便您可視需要繼續建立其他大量表單。 任何適用於您所選取之新帳戶的指定篩選器和排除專案都會保留。 工作開始時，檔案會列在「大量表單」檢視中。 建立檔案時，您會收到電子郵件通知，其中包含檔案的連結；根據編譯的資料量，通知可能需要幾分鐘或更長時間。 不過，如果檔案產生失敗，則會在「大量表單」檢視中列出錯誤檔案，而您會收到電子郵件通知，其中包含錯誤檔案的連結。

## Bulksheet下載設定 {#bulksheet-download-settings}

| 標籤 | 引數 | 說明 |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | 要上傳資料的帳戶、行銷活動或廣告群組：<ul><li>若要選取帳戶及其所有行銷活動和廣告群組，請選取帳戶名稱旁的核取方塊，然後按一下>>將其移至 [!UICONTROL Selected Filters] 欄。</li><li>若要選取個別行銷活動或廣告群組，請按一下帳戶旁的「 」以將其展開，（如有需要）按一下行銷活動旁的「 」以將其展開，選取行銷活動或廣告群組名稱旁的核取方塊，然後按一下「 >> 」以將其移至 [!UICONTROL Selected Filters] 欄。 例如，若只要取得帳戶1中Campaign 1的資料，請展開Account 1，選取Campaign 1旁的核取方塊，然後將其移至 [!UICONTROL Selected Filters] 欄。</li></ul><b>附註：</b><ul><li>單一大量表單可套用至多個廣告網路中的多個帳戶。 廣告網路專用欄會在大量表單中標示廣告網路名稱(例如「行動電信業者(Google廣告)」)。</li><li>若要檢視任何專案的元件型別，請將游標停留在它上。</li><li>對於行銷活動，廣告網路名稱的第一個字母位於帳戶名稱后的括弧中(例如， [!DNL Google Ads] account)。</li><li>依預設，只會列出使用中和已啟用的帳號及其使用中的元件。 若要檢視暫停和刪除的元件，請按一下 ![向下鍵](/help/search-social-commerce/assets/arrow-down-expand.png "向下鍵") 旁邊 [!UICONTROL Show] 並選取**[!UICONTROL All]. |
|  | [!UICONTROL Generate Tracking URLs] | （可選）在含有追蹤範本的帳戶中包含追蹤範本和登陸頁面尾碼（適用於適用的廣告網路），或在含有目的地URL的帳戶中包含內嵌追蹤程式碼的目標URL，適用於關鍵字、廣告、位置、網站連結和 [!DNL Google Ads] 大量表單中的產品群組。 依預設，會選取此選項。<br><br>選取此選項時，會根據中的引數產生URL [!UICONTROL Campaign Tracking] 區段設定或行銷活動設定。 根據預設，如果追蹤URL已存在，則不會重新產生，除非需要新專案（例如關鍵字元合型別、廣告文字或帳戶的追蹤引數已變更）。<br><br><b>附註：</b><ul><li>如果廣告商使用Adobe廣告轉換追蹤，且相關帳戶未設定為自動產生和上傳追蹤URL，則您必須在基本URL變更後產生新的追蹤URL。</li><li>如果您未選取此選項，您稍後上傳或發佈檔案時仍可產生追蹤URL。</li></ul> |
|  | [!UICONTROL Perform Pre-sync] | （選用）指示Search、Social和Commerce將其檔案與指定的行銷活動同步，以確保所有資料都相同。 依預設，不會選取此選項。<br><b>注意：</b> 搜尋、Social和Commerce會在廣告網路上偵測到新的促銷活動時，以及每次您從Search、Social和Commerce內變更促銷活動資料時，每天自動與廣告網路同步一次。 如果您認為行銷活動或帳戶資料的最近變更是直接在廣告網路中或使用廣告網路的案頭編輯器，請選取此選項。 選取此選項時，建立大量工作表所需的時間較長。 |
|  | [!UICONTROL Bulksheet Name] | 新大量表單的名稱和檔案型別。 依預設，檔案會以定位點分隔值格式建立，並命名為下列其中一項：<ul><li>（適用於廣告網路的所有帳戶） `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（適用於單一帳戶） `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（適用於多個帳戶） `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>您可以重新命名檔案。 名稱不能包含下列字元： `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>或者，變更檔案型別。 選項包括 *[!UICONTROL .tsv]* （以定位點分隔的值）， *[!UICONTROL .txt]* （適用於符合Unicode規範的ASCII文字）， *[!UICONTROL .csv]* （逗號分隔值），或 *[!UICONTROL .zip]* （適用於壓縮的ZIP格式，會解壓縮成TSV檔案）。<br><br><b>秘訣：</b> 對於包含國際字元的區塊工作表，請使用TSV或TXT格式。 |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | 實體及其對應狀態，包含在Bulksheet中，每個專案有一個資料列。 例如，若您包含作用中的行銷活動，則大量工作表會針對每個作用中的行銷活動包含一列。 只包含具有所選狀態的所選圖元。 系統會根據指定的廣告網路預先選取預設值。 依預設，只包含所選圖元的啟動例證。 如需可用大量表單列的清單，請參閱&quot;[依廣告網路大量表單列](#bulksheet-rows-by-ad-network).」<br><br>若要新增或移除圖元，請分別選取或清除圖元旁的核取方塊。 若要新增或移除實體的狀態，請按一下狀態選單旁的，然後分別選取或清除實體旁的核取方塊。 |
|  | [!UICONTROL Cascading Status Hierarchy] | 使用AND運算將子系實體的範圍篩選為具有指定父系實體狀態的範圍。 例如，如果您選取「作用中行銷活動」、「作用中廣告群組」和「作用中關鍵字」，則大量表單只會包含作用中行銷活動之作用中廣告群組中的作用中關鍵字。<br><br>如果您未選取此選項，則不會考慮父項狀態，而篩選器會使用OR操作。 例如，如果您選取「作用中行銷活動」、「作用中廣告群組」和「作用中關鍵字」，則大量表單會包含所有作用中行銷活動、所有作用中廣告群組（無論父行銷活動狀態為何）以及所有作用中關鍵字（無論父行銷活動和廣告群組狀態為何）。 |
|  | [!UICONTROL Bulksheet Columns] | 要包含在已下載Bulksheet檔案中的欄：&lt;ul><li><li>*[!UICONTROL AMO ID]*：(若&quot;[!UICONTROL SE ID]「 」未選取)包含 [!DNL Adobe] — 為每個實體/列產生的唯一識別碼。 Search、Social和Commerce會使用值來決定要編輯的正確身分，但不會將其發佈到廣告網路。 稍後，您可以使用來編輯實體的資料。 [!UICONTROL AMO ID] 做為識別碼，而不是實體ID和父實體ID。</li><li>*[!UICONTROL SE ID]*：(若&quot;[!UICONTROL AMO ID]」未選取)包含每個已包含欄及其上層實體的廣告網路唯一識別碼。 稍後，如果您使用編輯任何實體的資料 [!UICONTROL SE ID] 作為識別碼，您還必須包含父項實體的列(包括其父項 [!UICONTROL SE ID] 值)。</li><li>*[!UICONTROL Platform]*：包含 [!UICONTROL Platform column] ，以表示廣告平台（例如「百度」）。</li><li>*[!UICONTROL Acct Name]*：(若&quot;[!UICONTROL AMO ID]」未選取)包含每個實體/列的廣告網路帳戶名稱。</li><li>\[要包含的欄\]：若要包含所有、無或僅包含與中每個所選實體相關的所選欄 [!UICONTROL Bulksheet Rows] 區段。 若要檢視與實體相關的個別欄，請按一下 ![右箭頭](/help/search-social-commerce/assets/compressed-item.png "右箭頭") 位於實體名稱旁。 依預設，每個選取的實體列都會包含所有相關欄。 取消選取任何實體旁的核取方塊，或任何個別欄旁的核取方塊，將其從大量表單中排除。</li></ul><br><br><b>秘訣：</b> 請務必加入足夠的欄，以識別Bulksheet檔案每一列中的專案。 例如，假設您根據 [!UICONTROL Bulksheet Rows] 選擇器，但會排除所有關鍵字相關的欄。 產生的大量表單會針對每個關鍵字例項包含一列。 但是，由於未包含與關鍵字相關的欄（甚至包括AMO ID或SE ID），因此您無法識別哪個關鍵字例項屬於特定列，而且除非手動新增適當的ID欄和值，否則您無法使用Bulksheet來更新資料。 |
| [!UICONTROL Filters] |  | 要包含在Bulksheet中的特定行銷活動、廣告群組、廣告/創意、關鍵字及/或版位的條件：<ol><li>選取引數（實體名稱或ID；或創意、關鍵字或位置的任何元素），選取運運算元，然後輸入適用的值。<br><br>例如，只傳回標題中包含「鞋子」的廣告 [!DNL Google Ads] 帳戶，選取 *[!UICONTROL Headline]*，選取 *[!UICONTROL contains]*，然後輸入 `shoes` 在輸入欄位中。</li><li>（若要套用其他篩選器）對於每個其他篩選器，請按一下 **[!UICONTROL +Add Filter]**，選取 **[!UICONTROL AND]** 或 **[!UICONTROL OR]**，選取廣告元素或關鍵字和運運算元，然後輸入適用的值。</li></ul> |

## 依廣告網路大量表單列 {#bulksheet-rows-by-ad-network}

| 大量表單列 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft® Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | 附註 |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Adgroup] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Creative] *或* [!UICONTROL Creative (except RSA)] | 是 | 是 | 是 | — | — | 是 | 是 | 是 | 是 | ([!DNL Google  Ads])用於所有廣告型別，但回應式搜尋廣告除外，這些廣告可在 [!UICONTROL Responsive Search Ad] 列。 |
| [!UICONTROL Responsive Search Ad] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | 是 | 是 | 是 | 是 | 是 | — | 是 | 是 | 是 | 僅用於非負值關鍵字。 若要檢視在行銷活動或廣告群組層級建立的負面關鍵字，請使用 [!UICONTROL Campaign Negative Keyword] 或 [!UICONTROL Adgroup Negative Keyword] 列（可用時）。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | 是 | — | — | — | — | — |
| [!UICONTROL Placement] | — | 是 | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | 是 | 是 | — | — | — | — | — | — | 用於廣告群組的動態搜尋目標。 |
| [!UICONTROL Shopping Product Group] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Campaign Negative Keyword] | 是 | 是 | 是 | — | — | — | 是 | 是 | — | 僅用於行銷活動或廣告群組層級建立的負面關鍵字。 若要檢視非負的關鍵字，請使用 [!UICONTROL Keyword] 列（可用時）。 |
| [!UICONTROL Campaign Negative Website] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Site Link] | — | 是 | — | — | — | — | — | 是 | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | 是 | — |
| [!UICONTROL Adgroup Negative Keyword] | 是 | 是 | 是 | — | — | — | 是 | 是 | — | — |
| [!UICONTROL Adgroup Negative Website] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | 是 | 是 | 是 | — | — | — | 是 | 是 | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Campaign Device Target] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Device Target] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Campaign RLSA Target] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | 是 | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | 是 | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [關於使用大量表單管理行銷活動資料](bulksheet-about.md)
>* [張貼大量工作表或已修正的錯誤檔案](bulksheet-post.md)
>* [驗證大量表單檔案中的登入頁面](bulksheet-validate-landing-pages.md)
>* [匯出產生或上傳的大量工作表檔案](bulksheet-export.md)

