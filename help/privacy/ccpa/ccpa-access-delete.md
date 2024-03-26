---
title: Adobe Advertising對加州消費者隱私法的支援：消費者資料存取和刪除支援
description: 瞭解支援的資料請求型別、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例。
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 5edcd810c86f3b3ae65ccc92748177fa8cd0765e
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---

# 加州消費者隱私法的Adobe Advertising支援：消費者資料存取和刪除支援

*的 [!DNL Adobe Advertising Search, Social, & Commerce]；Adobe Advertising DSP；Adobe Advertising Creative；和Adobe AdvertisingDCO*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需《加州消費者隱私法》的相關建議，請諮詢您的法律顧問。

加州消費者隱私法(CCPA)是加州的最新隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供有關個人資訊的新權利，並對在加州經營業務的特定實體施加資料保護責任。 CCPA給予消費者存取及刪除其個人資訊的權利，且消費者有權選擇退出能將個人資訊「銷售」給第三方的某些活動。

企業能決定哪些個人資料要交由Adobe Experience Cloud代表您處理和儲存。

作為您的服務提供者，Adobe Advertising會為您的企業提供支援，以履行CCPA所規範的適用於使用Adobe Advertising產品和服務的義務，包括管理存取和刪除個人資訊的請求，以及管理選擇退出個人資訊銷售的請求。

本檔案說明如何 [!DNL Advertising Search, Social, & Commerce]；Advertising Creative；Advertising DSP (Demand Side Platform)；和 [!DNL Advertising DCO]  — 作為服務提供者 — 支援消費者使用Adobe存取和刪除個人資訊的權利 [!DNL Experience Platform Privacy Service API] 和 [!DNL Privacy Service UI].

如需Advertising DSP如何支援消費者選擇退出個人資訊銷售的權利的詳細資訊，請參閱 [加州消費者隱私法的Adobe Advertising支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

如需CCPAAdobe隱私權服務的詳細資訊，請參閱 [Adobe隱私中心](https://www.adobe.com/privacy/ccpa.html).

## 支援的Adobe Advertising資料請求型別

Adobe Experience Platform讓企業能夠完成下列工作：

* 在中存取消費者的Cookie層級資料或裝置ID層級資料（適用於行動應用程式中的廣告） [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO].
* 刪除儲存在中的Cookie層級資料 [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO] 適用於使用瀏覽器的消費者；或刪除儲存在中的ID層級資料 [!DNL DSP] 適用於在行動裝置上使用應用程式的消費者。
* 檢查一個或所有現有請求的狀態。

## 傳送Adobe Advertising請求的必要設定

若要請求存取和刪除Adobe Advertising中的消費者個人資訊，您需要：

1. 部署JavaScript程式庫以擷取和移除客戶的Cookie。 相同的程式庫， `AdobePrivacy.js`，適用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >請求某些Experience Cloud解決方案不需要JavaScript程式庫，但Adobe Advertising請求需要它。

   您應將程式庫部署在客戶可提交存取和刪除請求的網頁上，例如您公司的隱私權入口網站。 資料庫可協助您擷取AdobeCookie (名稱空間ID： `gsurferID`)，這樣您就可以在存取和刪除請求時，透過提交這些身分識別， [!DNL Adobe Experience Platform Privacy Service API].

   當客戶要求刪除個人資料時，程式庫也會從客戶的瀏覽器中刪除客戶的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，後者會停止將目標定位為具有受眾區段的一般使用者。 但是，當消費者要求刪除以下專案的個人資料時： [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO]，程式庫也會傳送要求給Adobe Advertising選擇退出客戶區段鎖定目標。 適用於廣告商與 [!DNL Search, Social, & Commerce]，建議您向客戶提供以下連結至 [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)，說明如何選擇退出對象區段鎖定目標。

1. 識別您的Experience Cloud組織ID，並確定其已連結至您的Adobe Advertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，後面接著「@AdobeOrg」。 大部分Experience Cloud客戶已指派組織ID。 如果您的行銷團隊或內部 [!DNL Adobe] 系統管理員不知道您的組織ID，或不確定是否已布建該ID，然後聯絡您的Adobe帳戶團隊。 您將需要組織ID，才能使用將請求提交至隱私權API。 `imsOrgID` 名稱空間。

   >[!IMPORTANT]
   >
   >請聯絡貴公司的Adobe Advertising代表，確認貴組織的所有Adobe Advertising帳戶，包括 [!DNL DSP] 帳戶或廣告商， [!DNL Search, Social, & Commerce] 帳戶，以及 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結至您的Experience Cloud組織ID。

1. 使用 [ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （適用於自動化請求）或 [PRIVACY SERVICEUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant) （適用於臨時請求）代表消費者提交存取和刪除個人資訊的請求給Adobe Advertising，並檢查現有請求的狀態。

   適用於擁有行動應用程式的廣告商，以便與客戶互動並推出促銷活動與 [!DNL DSP]，您必須下載適用於隱私權的行動SDK，才能Experience Cloud。 行動SDK可讓企業設定選擇退出狀態標幟，擷取消費者的裝置ID (名稱空間ID： `deviceID`)，並將請求提交至Privacy Service API。 您的行動應用程式將需要SDK 4.15.0版或更新版本。

   當您提交消費者存取請求時，Privacy ServiceAPI會根據指定的Cookie或裝置ID傳回消費者的資訊，然後您必須將其傳回給消費者。

   當您提交消費者刪除請求時，Cookie ID或裝置ID以及所有成本、點選數以及與Cookie相關的收入資料都會從伺服器刪除。

   >[!NOTE]
   >
   >如果您的企業有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 不過，您可以向多個Adobe Advertising子解決方案提出一個API請求([!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]、和 [!DNL DCO])，每個子解決方案各有一個帳戶。

若要獲得Adobe Advertising的支援，所有這些步驟都是必要的。 如需這些事項以及您需要使用Adobe Experience Platform Privacy Service執行的其他相關工作的詳細資訊，以及可在何處找到所需專案的資訊，請參閱 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Adobe Advertising JSON請求中的必填欄位值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud組織ID*>

&quot;users&quot;：

* `"key":` &lt;*通常是客戶的名稱*>

* `"action":` 兩者之一 `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (表示 [!DNL adcloud] Cookie空間)

   * `"value":` &lt;*擷取自之實際客戶的Cookie ID值`AdobePrivacy.js`*>

* `"include": **adCloud**` (亦即 [!DNL Adobe] 適用於此要求的產品)

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
