---
title: ' [!DNL FreeWheel] 廣告提交的錯誤碼'
description: 參考向 [!DNL FreeWheel]提交廣告時傳回的錯誤碼。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 3%

---

# [!DNL FreeWheel]個廣告提交的錯誤碼

失敗的廣告提交錯誤訊息可能來自Advertising DSP或[!DNL FreeWheel]。 錯誤訊息顯示在[[!UICONTROL Freewheel Status]對話方塊](freewheel-check-status.md)的[!UICONTROL API Response]欄中。

## Advertising DSP內部錯誤

| 錯誤訊息 | 說明 | 後續步驟 |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel]尚未回應提交成功或失敗。 | 10分鐘後再檢查狀態。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel]不接受沒有指定時鐘編號的UK廣告。 | 為廣告指派時脈編號，然後重新提交廣告。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 當您嘗試提交廣告時，轉碼器尚未完成廣告的轉碼。 | 請稍候10分鐘，然後重新提交廣告。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 提交的交易未設定為程式化保證交易。 [!DNL FreeWheel]只接受保證交易。 | 將交易ID設定為程式化預留交易。 當您在交易ID工作流程結束時儲存程式化預留預設位置時，廣告會自動提交至[!DNL FreeWheel]。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id\> | 提交的交易ID不存在，或在Adobe端非作用中。 | 確定交易有效，然後重新提交廣告。 |
| [!DNL \[public_id=]\&lt;deal\>]不存在 | 提交的交易識別碼不存在於[!DNL FreeWheel]結尾。 | 請聯絡您的[!DNL FreeWheel]代表以確認交易識別碼。 |
| [!DNL Ad with identifier] \&lt;*廣告名稱*\> [!DNL was not found.] | 提交的廣告金鑰不存在或在Adobe端非作用中。 | 找到正確的廣告金鑰，然後重新提交廣告。 |
| [!DNL Pending Submission] | 提交作業仍在等候中。 | 重新整理頁面。 |

{style="table-layout:auto"}

## [!DNL Freewheel] API錯誤

| 程式碼 | 含義 | 說明 | 後續步驟 |
|--- |--- |--- |--- |
| 401 | 未獲授權 | 存取認證不正確、遺失或無效。 | 請聯絡您的Adobe客戶團隊。 |
| 403 | 已禁止 | 伺服器理解要求但拒絕授權。 | 請聯絡您的Adobe客戶團隊。 |
| 404 | 找不到 | 您要求的資源無法使用。 如果在PUT操作中找不到創作ID，則會傳回404。 | 請聯絡您的Adobe客戶團隊。 |
| 405 | 不允許的方法 | 使用資源不支援的要求方法(例如，使用需要POST傳送資料的方法上的GET，或使用唯讀資源上的PUT)對資源提出要求。 | 請聯絡您的Adobe客戶團隊。 |
| 408 | 請求逾時 | 處理此要求時發生逾時。 逾時通常是因為同時要求獨佔存取特定資源所導致。 | 當您收到此狀態時，請重新提交請求。 如果問題仍然存在，請聯絡您的Adobe客戶團隊。 |
| 422 | 無法處理的實體 | 無效的資源。 當要求內文無效或建立/更新的資源無效時（例如，找不到交易ID時），就會發生此錯誤。 如需詳細資訊，請參閱[FreeWheel API 422錯誤](#freewheel-422-errors)。 | 請聯絡您的Adobe客戶團隊。 |
| 500 | 內部伺服器錯誤 | API系統錯誤。 | 請聯絡您的Adobe客戶團隊。 |

{style="table-layout:auto"}

## [!DNL Freewheel] API 422錯誤 {#freewheel-422-errors}

| 程式碼 | HTTP程式碼 | 說明 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | 請求資料的JSON格式無效。 檢查錯誤訊息以取得詳細資料。 |
| DATA_VALIDATION_FAILURE | 422 | 請求資料缺少必填欄位或資料型別無效。 檢查錯誤訊息以取得詳細資料。 |
| DATA_DEAL_INVALID | 422 | 交易設定錯誤或不存在。 檢查錯誤訊息以取得詳細資料。 |
| DATA_DEAL_GET_失敗 | 422 | 找不到交易或其設定有問題。 檢查錯誤訊息以取得詳細資料。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | 創作URL無效。 檢查錯誤訊息以取得詳細資料。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | 創意內容未連結至交易的廣告單元節點。 檢查錯誤訊息以取得詳細資料。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | 創意內容未更新。 檢查錯誤訊息以取得詳細資料。 |
| DATA_DSP_GET_失敗 | 422 | DSP不存在於系統中。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | 創意內容不會從廣告單位中取消連結。 |
| DATA_CREATIVE_DELETE_FAILURE | 422 | 未刪除創意。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | 未偵測到URL。 |
| DATA_ENTITY_NOT_FOUND | 422 | 創意內容不存在。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [在 [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)中設定程式化預留交易的概觀
>* [在交易識別碼收件匣中接受交易](deal-id-inbox-accept.md)
>* [提交程式化保證交易的廣告給 [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [檢查 [!DNL FreeWheel] 程式化預留交易的廣告狀態](/help/dsp/inventory/freewheel-check-status.md)
