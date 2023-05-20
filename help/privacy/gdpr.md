---
title: Adobe廣告支援一般資料保護法規
description: 瞭解支援的資料請求類型、必需的設定和欄位值，以及使用舊產品ID和返回的資料欄位的API訪問請求示例
feature: GDPR
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---

# Adobe廣告支援一般資料保護法規

*對於 [!DNL Adobe Advertising Search, Social, & Commerce];Adobe廣DSP告；Adobe廣告創意；和Adobe廣告DCO*

>[!IMPORTANT]
>
>本檔案內容不是法律意見，不是代替法律意見。 請咨詢您的法律顧問，以獲得有關一般資料保護法規的建議。

2018年5月25日生效的《一般資料保護條例》(GDPR)允許歐盟(EU)境內的所有個人（資料主體）控制其個人資料並簡化國際商業的監管環境。 本法適用於在處理個人資料時向歐盟境內的個人提供商品或服務、監控其行為或從其收集個人資料的所有企業（資料控制器），而不管資料控制器的業務所在地。

Adobe Experience Cloud為客戶接收和儲存任何個人資料充當資料處理器。 作為資料控制器，您將確定Adobe Experience Cloud代表您處理和儲存的個人資料。

本文檔介紹如何 [!DNL Advertising Search, Social, & Commerce];廣告創意；廣告DSP(Demand Side Platform);和 [!DNL Advertising DCO] 使用Adobe Experience Platform Privacy ServiceAPI和Privacy ServiceUI支援資料主體的GDPR資料存取和刪除權限。

有關GDPR對您的業務意味著什麼的詳細資訊，請參見 [GDPR和您的業務](https://www.adobe.com/privacy/general-data-protection-regulation.html)。

## 支援的Adobe廣告資料請求類型

Adobe Experience Platform為企業提供了完成以下任務的能力：

* 訪問資料主題的Cookie級資料或設備ID級資料（用於移動應用中的廣告） [!DNL Search, Social, & Commerce]。 [!DNL Creative]。 [!DNL DSP]或 [!DNL DCO]。
* 刪除儲存在 [!DNL Search, Social, & Commerce]。 [!DNL Creative]。 [!DNL DSP]或 [!DNL DCO] 使用瀏覽器的資料主題；或刪除儲存在 [!DNL DSP] 使用移動設備上應用的資料主題。
* 檢查一個或所有現有請求的狀態。

## 發送Adobe廣告請求所需的設定

要請求訪問和刪除Adobe廣告的資料，您需要：

1. 部署JavaScript庫以檢索和刪除資料主題Cookie。 同一個圖書館， `AdobePrivacy.js`，用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript庫，但對Adobe廣告的請求需要它。

   您應在網頁上部署庫，資料主題可從該網頁上提交訪問和刪除請求，如您公司的隱私門戶。 庫可幫助您檢索AdobeCookie(命名空間ID: `gsurferID`)，以便您可以提交這些標識作為訪問的一部分，並通過Adobe Experience Platform Privacy ServiceAPI刪除請求。

   當資料主題要求刪除個人資料時，庫還從資料主題的瀏覽器中刪除資料主題的cookie。

   >[!NOTE]
   >
   >刪除個人資料與「選擇退出」不同，後者會阻止具有受眾段的最終用戶的目標。 但是，當資料主題要求從 [!DNL Creative]。 [!DNL DSP]或 [!DNL DCO]，該庫還向Adobe廣告發送請求，以從段目標中選擇資料主題。 對於具有 [!DNL Search, Social, & Commerce]，我們建議您提供資料主題的連結 [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)，說明如何選擇不以受眾為目標。

1. 確定您的Experience Cloud組織ID，並確保它連結到您的Adobe廣告帳戶。

   Experience Cloud組織ID是附加有「@AdobeOrg」的24個字元的字母數字字串。 大多數Experience Cloud客戶已分配了組織ID。 如果您的營銷團隊或內部Adobe系統管理員不知道您的組織ID，或者不確定是否已預配，請通過gdprsupport@adobe.com與Adobe客戶服務部聯繫。 您需要組織ID才能使用 `imsOrgID` 命名空間。

   >[!IMPORTANT]
   >
   >聯繫您公司的Adobe廣告代表，確認您公司的所有Adobe廣告帳戶，包括 [!DNL DSP] 或者廣告商， [!DNL Search, Social, & Commerce] 帳戶和 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結到您的Experience Cloud組織ID。

1. 使用 [Adobe Experience Platform Privacy ServiceAPI](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （用於自動請求）或 [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （針對臨時請求）代表資料主題向Adobe廣告提交訪問和刪除請求，並檢查現有請求的狀態。

   對於擁有移動應用與資料主題交互併發起活動的廣告商DSP，您需要下載適合隱私的移動軟體開發工具包進行Experience Cloud。 移動SDK允許資料控制器設定opt-out狀態標誌，檢索資料主題的設備ID(命名空間ID:設備ID)，並將請求提交到Privacy ServiceAPI。 您的移動應用需要SDK 4.15.0版或更高版本。

   當您提交資料主題的訪問請求時，Privacy ServiceAPI將根據指定的cookie或設備ID返回資料主題的資訊，然後您必須返回資料主題。

   提交資料主題的刪除請求時，會從伺服器中刪除與cookie關聯的Cookie ID或設備ID以及所有成本，按一下，並刪除與cookie關聯的收入資料。

   >[!NOTE]
   如果您的公司具有多個Experience Cloud組織ID，則必須為每個API請求發送單獨的API請求。 但是，您可以向多個Adobe廣告子解決方案發出一個API請求([!DNL Search, Social, & Commerce]。 [!DNL Creative]。 [!DNL DSP], [!DNL DCO])，每個子解決方案有一個帳戶。

所有這些步驟對於Adobe廣告是必要的。 有關使用Adobe Experience Platform Privacy Service執行這些任務和其他相關任務的詳細資訊，以及在何處查找需要的項目，請參閱 [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html)。

## Adobe廣告JSON請求中的必需欄位值

&quot; &quot;公司上下文&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*IMS組織ID值*>

`"users":`

* `"key":` &lt;*通常資料主題的名稱*>

* `"action":` 或 `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (表示 [!DNL adcloud] cookie空間)

   * `"value":` &lt;*從中檢索到的實際資料主題的cookie ID值`AdobePrivacy.js`*>

* `"include": **adCloud**` (即適用於請求的Adobe產品)

* `"regulation": **gdpr**` （即適用於請求的隱私法規）

## 資料主題使用從中檢索的Adobe廣告用戶ID提交的請求示例 `AdobePrivacy.js`

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
}
```

## 為訪問請求返回的資料欄位

下面是Adobe廣告的訪問響應示例。

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
