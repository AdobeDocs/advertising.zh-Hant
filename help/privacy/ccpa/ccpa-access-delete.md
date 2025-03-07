---
title: Adobe Advertising對加州消費者隱私法的支援&#58；消費者資料存取和刪除支援
description: 瞭解支援的資料請求型別、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例。
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: a3e39ca4fa89f84ddc2669662c34bccb4425a2bb
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Adobe Advertising對加州消費者隱私法的支援：消費者資料存取和刪除支援

*適用於[!DNL Adobe Advertising Search, Social, & Commerce]、Adobe Advertising DSP、Adobe Advertising Creative和Adobe Advertising DCO*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需《加州消費者隱私法》的相關建議，請諮詢您的法律顧問。

加州消費者隱私法(CCPA)是加州的最新隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供有關個人資訊的新權利，並對在加州經營業務的特定實體施加資料保護責任。 CCPA給予消費者存取及刪除其個人資訊的權利，且消費者有權選擇退出能將個人資訊「銷售」給第三方的某些活動。

企業能決定哪些個人資料要交由Adobe Experience Cloud代表您處理和儲存。

身為您的服務提供者，Adobe Advertising會為您的企業提供支援，以履行CCPA所規範的適用於使用Adobe Advertising產品和服務的義務，包括管理存取和刪除個人資訊的請求，以及管理選擇退出個人資訊銷售的請求。

本檔案說明[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP (Demand Side Platform)和[!DNL Advertising DCO] （身為服務提供者）如何支援消費者使用Adobe [!DNL Experience Platform Privacy Service API]和[!DNL Privacy Service UI]存取和刪除個人資訊的權利。

如需Advertising DSP如何支援消費者選擇退出個人資訊銷售的權利，請參閱[加州消費者隱私法的Adobe Advertising支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)。

如需CCPA適用Adobe隱私權服務的詳細資訊，請參閱[Adobe隱私權中心](https://www.adobe.com/privacy/ccpa.html)。

## Adobe Advertising支援的資料請求型別

Adobe Experience Platform讓企業能夠完成下列工作：

* 在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]記憶體取消費者的Cookie層級資料或裝置識別碼層級資料（適用於行動應用程式中的廣告）。
* 針對使用瀏覽器的消費者，刪除儲存在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中的Cookie層級資料；或者針對使用行動裝置上應用程式的消費者，刪除儲存在[!DNL DSP]中的ID層級資料。
* 檢查一個或所有現有請求的狀態。

## 傳送Adobe Advertising請求的必要設定

若要向Adobe Advertising請求存取和刪除消費者個人資訊，您必須：

1. 部署JavaScript程式庫以擷取和移除客戶的Cookie。 所有Adobe Experience Cloud解決方案都使用相同的資料庫`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >請求某些Experience Cloud解決方案不需要JavaScript資料庫，但請求給Adobe Advertising則需要它。

   您應將程式庫部署在客戶可提交存取和刪除請求的網頁上，例如您公司的隱私權入口網站。 資料庫可協助您擷取Adobe Cookie （名稱空間識別碼： `gsurferID`），這樣您就可以透過[!DNL Adobe Experience Platform Privacy Service API]提交這些身分識別，作為存取和刪除請求的一部分。

   當客戶要求刪除個人資料時，程式庫也會從客戶的瀏覽器中刪除客戶的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，後者會停止將目標定位為具有受眾區段的一般使用者。 不過，當消費者要求從[!DNL Creative]、[!DNL DSP]或[!DNL DCO]刪除個人資料時，資料庫也會傳送要求給Adobe Advertising，要求選擇退出客戶區段鎖定目標。 對於具有[!DNL Search, Social, & Commerce]的廣告商，建議您提供客戶一個[https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)的連結，其中說明如何選擇退出對象區段鎖定目標。

1. 識別您的Experience Cloud組織ID，並確定其已連結至您的Adobe Advertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，通常會加上「@AdobeOrg」。 大部分Experience Cloud客戶已指派組織ID。 如果您的行銷團隊或內部[!DNL Adobe]系統管理員不知道您的組織ID，或不確定其是否已布建，請聯絡您的Adobe帳戶團隊。 您需要組織識別碼，才能使用`imsOrgID`名稱空間將請求提交至隱私權API。

   >[!IMPORTANT]
   >
   >請聯絡貴公司的Adobe Advertising代表，確認貴組織的所有Adobe Advertising帳戶（包括[!DNL DSP]帳戶或廣告商、[!DNL Search, Social, & Commerce]帳戶及[!DNL Creative]或[!DNL DCO]帳戶）都與您的Experience Cloud組織ID連結。

1. 使用[Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （適用於自動要求）或[Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （適用於臨機要求）來提交要求，以代表消費者存取和刪除個人資訊給Adobe Advertising，以及檢查現有要求的狀態。

   對於擁有行動應用程式以便與客戶互動並透過[!DNL DSP]啟動行銷活動的廣告商，您必須下載適用於Experience Cloud的隱私權就緒行動SDK。 Mobile SDK可讓企業設定選擇退出狀態標幟、擷取消費者的裝置ID （名稱空間ID： `deviceID`），以及將請求提交至Privacy Service API。 您的行動應用程式將需要SDK 4.15.0版或更新版本。

   當您提交消費者存取請求時，Privacy Service API會根據指定的Cookie或裝置ID傳回消費者的資訊，而您之後必須將這些資訊傳回給消費者。

   當您提交消費者刪除請求時，Cookie ID或裝置ID以及所有成本、點選數以及與Cookie相關的收入資料都會從伺服器刪除。

   >[!NOTE]
   >
   >如果您的企業有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 但是，您可以向多個Adobe Advertising子解決方案（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]和[!DNL DCO]）提出一個API請求，每個子解決方案使用一個帳戶。

若要取得Adobe Advertising的支援，所有步驟都是必要的。 如需有關這些事項以及您需要使用Adobe Experience Platform Privacy Service執行的其他相關工作的詳細資訊，以及尋找必要專案的位置，請參閱[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)。

## Adobe Advertising JSON請求中的必填欄位值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud組織ID*>

&quot;users&quot;：

* `"key":` &lt;*通常是客戶的名稱*>

* `"action":` `**access**`或`**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示[[!DNL AdCloud] Cookie空間](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix)）

   * `"value":` &lt;*從`AdobePrivacy.js`*&#x200B;擷取的實際客戶的Cookie ID值>

* `"include": **adCloud**` （適用於此請求的[[!DNL Adobe] 產品](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix)）

* `"regulation": **ccpa**` （適用於此請求的隱私權法規）

## 消費者使用從AdobePrivacy.js擷取的Adobe Advertising使用者ID提交的請求範例

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
    "regulation":"ccpa"
}
```

## 針對存取請求所傳回的資料欄位

以下是Adobe Advertising的個人資訊存取回應範例。

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
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
