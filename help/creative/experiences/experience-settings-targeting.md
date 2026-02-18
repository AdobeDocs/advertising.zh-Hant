---
title: 目標體驗設定
description: 請參閱目標廣告體驗的所有設定說明。
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: ace6005869ea4102878091c4799259961aeecb63
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# 目標廣告體驗設定

## [!UICONTROL Experience basics]節

**[!UICONTROL Ad Type]：** （現有體驗為唯讀）體驗中包含的廣告型別： *[!UICONTROL Standard Display]*、*[!UICONTROL Dynamic Display]*、*[!UICONTROL Dynamic Display]*、*[!UICONTROL Standard Video]*&#x200B;或&#x200B;*[!UICONTROL Display Video]*。 儲存體驗後，您就無法變更廣告型別。

**[!UICONTROL Advertiser]：** （現有體驗為唯讀）將對體驗中包含的創意和目標組合出價的廣告商。 儲存體驗後，您就無法變更廣告商。

**[!UICONTROL Experience Name]：**&#x200B;體驗的唯一名稱。 **秘訣：**&#x200B;在Advertising DSP或其他DSP中使用體驗作為廣告時，請使用可以輕鬆找到的名稱。

**[!UICONTROL Creative Library]：** （現有體驗為唯讀）要用於體驗的單一創意程式庫。 儲存體驗後，就無法變更資料庫。

## [!UICONTROL Default creatives]節

**\[指定的預設創意\]：**&#x200B;當瀏覽器無法顯示指派給體驗的創意時(例如當瀏覽器未啟用JavaScript或廣告伺服器因延遲而無法個人化廣告時)，所使用的預設創意。 對於標準顯示體驗，針對體驗適用的每個廣告大小包含一個影像創意內容。 對於標準視訊體驗，請針對體驗適用的每個廣告大小包含一個視訊創意。 您的選擇決定了可用於體驗的創意大小。

對於決策樹目標定位的體驗，您可以使用決策樹內包含相同大小創意的創意套件組合來覆寫預設創意內容。<!-- verify -->

* 若要新增具有不同維度的預設創作，請按一下&#x200B;**[!UICONTROL + Add Sizes]**，從右側窗格中選取要新增的每個創意旁邊的核取方塊，然後按一下&#x200B;**[!UICONTROL Add Creatives]**。

* 若要刪除預設創意，請將游標停留在創意縮圖上，然後按一下![刪除](/help/creative/assets/delete.png "刪除")。

* 若要刪除所有預設創意，請按一下![刪除](/help/creative/assets/delete.png "刪除") **[!UICONTROL Delete all]**。

* 若要顯示或隱藏右邊的[創意內容]窗格，請按一下右邊窗格右上角的![顯示/隱藏](/help/creative/assets/hide-show-creatives.png "顯示/隱藏")。

## [!UICONTROL Targeting]節

體驗層級目標會與DSP的鎖定目標選項一起套用；階層鎖定目標行為可能會因DSP而異。 例如，Adobe Advertising DSP會將廣告層級鎖定目標套用在（而非）位置層級鎖定目標之上。 請確定您的廣告體驗包含與您將要實作它的行銷活動相容的目標定位。

**[!UICONTROL Targeting]：** （現有體驗為唯讀）使用決策樹和自動建立標籤來啟用創意目標定位。 儲存體驗後，便無法變更此設定。

**[!UICONTROL Language Targeting]：** （僅含標準廣告的體驗；選擇性；現有體驗為唯讀）檢查使用者的瀏覽器語言設定，並在可以使用指定語言的創意內容時，使用該語言顯示創意內容。 無法使用瀏覽器指定語言的創意內容時，將改用[!UICONTROL Preferred language]設定。

儲存體驗後，便無法變更此設定。

**[!UICONTROL Preferred language]：** （僅具有標準廣告的體驗；現有體驗為唯讀）從體驗建立的所有廣告的語言，啟用[!UICONTROL Language Targeting]時除外。 儲存體驗後，便無法變更此設定。

## [!UICONTROL Advanced]節

**資料傳遞：** （現有體驗為唯讀；選擇性）根據DSP、發行者或合作夥伴在曝光時即時傳遞的特定索引鍵/值組來鎖定使用者(例如SKU=01234567890123或Cart=empty)。 您可以指定最多五個預設的資料傳遞索引鍵（引數）。 在決策樹中設定鎖定目標時，您可以納入一個資料傳遞目標節點層級、選擇性地自訂索引鍵，以及指定每個節點的目標值。 如果您在建立體驗時未在此欄位中指定任何索引鍵，您仍可在決策樹中指定它們。

每個鍵都會附加為廣告體驗標籤中的巨集，您可產生該巨集以實施為DSP中的廣告。

**半徑：** （僅限使用動態廣告的體驗；選擇性）目標饋送檔案中指定的美國郵遞區號的半徑；選取從0哩到200哩的半徑。 用來為體驗建立動態廣告的摘要檔案必須包含一個[!UICONTROL ZIP]欄<!-- or a user-named column mapped to a ZIP column -->，且該檔案中的每個產品列都有值。 例如，半徑為10哩時，可向95110徑10哩內的使用者顯示95110中可用產品的廣告（由使用者的IP位址決定）。

**RT畫素：** （現有體驗為唯讀；選擇性） [!UICONTROL Creative]將畫素重新定位到潛在目標。 當您在決策樹中設定目標時，可以包含一個RT畫素目標節點層級。 對於每個節點，您將指定要定位的畫素，以及在指定的創意組合中顯示創意所需的畫素屬性值。 如果您在建立體驗時未在此欄位中指定畫素，您仍可在決策樹中指定畫素。<!-- May move this to just within the decision tree. -->

**標籤：**<!-- should be "Labels" --> （選用）任何套用至體驗的[!DNL Creative]特定標籤。 您可以在體驗檢視中依標籤篩選體驗，並在[!UICONTROL Experience Label]中包含[!UICONTROL Custom Creative Report]維度。

* 若要選取現有標籤，請按一下![向下](/help/creative/assets/chevron-down.png "向下")，然後選取要套用的每個標籤旁的核取方塊。

* 若要搜尋現有標籤，請在標簽名稱內開始輸入文字字串。

* 若要建立要套用的新標籤，請開啟清單，按一下&#x200B;**+新增標籤**，在[!UICONTROL Label]欄位中輸入新標簽名稱，然後按一下&#x200B;**建立**。

* 若要移除標籤，請取消選取標簽名稱旁的核取方塊。

**曝光追蹤URL：** （選用）要附加至從體驗建立之任何廣告的登陸頁面URL的協力廠商曝光追蹤URL。 您最多可以包含五個URL。 若要新增其他URL，請按一下![圖示](/help/creative/assets/create.png) **[!UICONTROL Add More]並輸入URL。

輸入URL後，頁面下方會列出所有[可用的巨集](/help/creative/creative-macros.md)及其取代的資料。 若要在URL中插入其中一個巨集，請將游標停留在巨集描述上，然後按一下[複製到剪貼簿] ![ [複製到剪貼簿] ](/help/creative/assets/copy-to-clipboard.png "，然後將巨集貼到URL欄位中您想要的任何位置。")

>[!NOTE]
>
>* [!DNL Creative]會自動在登陸頁面URL加上自己的曝光追蹤標籤作為前置詞。
>* 您可以[為體驗](experience-tracking-urls-targeting.md)中的任何創意內容覆寫此URL。
>* 您也可以在[!UICONTROL Client JS]欄位中輸入協力廠商JavaScript曝光數追蹤程式碼

**點選追蹤URL：** （選用） （選用）要附加至登陸頁面URL的協力廠商點選追蹤URL。 您最多可以包含五個URL。 若要新增其他URL，請按一下![圖示](/help/creative/assets/create.png) **[!UICONTROL Add More]並輸入URL。

輸入URL後，頁面下方會列出所有[可用的巨集](/help/creative/creative-macros.md)及其取代的資料。 若要在URL中插入其中一個巨集，請將游標停留在巨集描述上，然後按一下[複製到剪貼簿] ![ [複製到剪貼簿] ](/help/creative/assets/copy-to-clipboard.png "，然後將巨集貼到URL欄位中您想要的任何位置。")

>[!NOTE]
>
>* [!DNL Creative]會自動在登陸頁面URL加上自己的曝光追蹤標籤作為前置詞。
>* 您可以[為體驗](experience-tracking-urls-targeting.md)中的任何創意內容覆寫此URL。

**使用者端JS：** （選擇性）下列任一項：

* （當廣告商使用符合OBA規範的廠商進行廣告時） JavaScript程式碼會指向允許使用者選擇退出線上行為目標定位(OBA)的廣告覆蓋。

* 要附加至登陸頁面的任何第三方JavaScript曝光追蹤程式碼。 **注意：**&#x200B;您也可以在[!UICONTROL Impression Tracking URL]欄位中輸入協力廠商曝光追蹤URL。

>[!MORELIKETHIS]
>
>* [建立決策樹定位的體驗](experience-create-targeting.md)
>* [編輯決策樹定位的體驗](experience-edit-targeting.md)
>* [可用於追蹤URL的巨集](/help/creative/creative-macros.md)
