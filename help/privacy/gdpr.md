---
title: 一般資料保護規範的Adobe Advertising支援
description: 瞭解支援的資料請求型別、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 80072930c0506a017a927ce53eaad900a2642e92
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---

# 一般資料保護規範的Adobe Advertising支援

*的 [!DNL Adobe Advertising Search, Social, & Commerce]；Adobe Advertising DSP；Adobe Advertising Creative；和Adobe AdvertisingDCO*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 請諮詢您的法律顧問，以獲得有關一般資料保護規範的建議。

2018年5月25日生效的一般資料保護規範(GDPR)賦予歐盟(EU)境內所有個人（資料主體）掌控其個人資料的權利，並簡化國際業務的法規環境。 此法律適用於向歐盟境內之個人提供商品或服務、監控其行為或收集其個人資料的所有企業（資料控管單位），無論資料控管單位的營業地點為何，其個人資料處理作業均適用此法律。

Adobe Experience Cloud代表客戶擔任資料處理者的角色，依指示接收和儲存的任何個人資料。 身為資料控管單位，您可以決定要由Adobe Experience Cloud代表您處理和儲存哪些個人資料。

本檔案說明如何 [!DNL Advertising Search, Social, & Commerce]；Advertising Creative；Advertising DSP (Demand Side Platform)；和 [!DNL Advertising DCO] 使用Adobe Experience Platform Privacy Service API和Privacy ServiceUI，支援資料主體存取GDPR資料和刪除許可權。

如需深入瞭解GDPR對您業務所代表的意義，請參閱 [GDPR與您的業務](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## 支援的Adobe Advertising資料請求型別

Adobe Experience Platform讓企業能夠完成下列工作：

* 在中存取資料主體的Cookie層級資料或裝置ID層級資料（適用於行動應用程式中的廣告） [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO].
* 刪除儲存在中的Cookie層級資料 [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO] 適用於使用瀏覽器的資料主體；或刪除儲存在中的ID層級資料 [!DNL DSP] 適用於在行動裝置上使用應用程式的資料主體。
* 檢查一個或所有現有請求的狀態。

## 傳送Adobe Advertising請求的必要設定

若要請求存取和刪除Adobe Advertising資料，您需要：

1. 部署JavaScript程式庫以擷取和移除您的資料主體Cookie。 相同的程式庫， `AdobePrivacy.js`，適用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >請求某些Experience Cloud解決方案不需要JavaScript程式庫，但Adobe Advertising請求需要它。

   您應將資料庫部署在資料主體可提交存取和刪除請求的網頁上，例如您公司的隱私權入口網站。 資料庫會協助您擷取 [!DNL Adobe] Cookie (名稱空間ID： `gsurferID`)，讓您可以透過Adobe Experience Platform Privacy Service API提交這些身分識別，作為存取和刪除請求的一部分。

   當資料主體要求刪除個人資料時，資料庫也會從資料主體的瀏覽器中刪除資料主體的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，後者會停止以對象區段鎖定一般使用者。 但是，當資料主體要求從以下位置刪除個人資料時： [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO]，資料庫也會傳送要求給Adobe Advertising選擇退出資料主體進行區段定位。 適用於廣告商與 [!DNL Search, Social, & Commerce]，我們建議您為資料主體提供連結， [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)，說明如何選擇退出對象區段鎖定目標。

1. 識別您的Experience Cloud組織ID，並確定其已連結至您的Adobe Advertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，後面接著「@AdobeOrg」。 大部分Experience Cloud客戶已指派組織ID。 如果您的行銷團隊或內部 [!DNL Adobe] 系統管理員不知道您的組織ID，或不確定是否已布建，然後透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您將需要組織ID，才能使用將請求提交至隱私權API。 `imsOrgID` 名稱空間。

   >[!IMPORTANT]
   >
   >請聯絡貴公司的Adobe Advertising代表，確認貴組織的所有Adobe Advertising帳戶，包括 [!DNL DSP] 帳戶或廣告商， [!DNL Search, Social, & Commerce] 帳戶，以及 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結至您的Experience Cloud組織ID。

1. 使用 [ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （適用於自動化請求）或 [PRIVACY SERVICEUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant) （適用於臨時請求）代表資料主體向Adobe Advertising提交存取和刪除請求，並檢查現有請求的狀態。

   如果廣告商擁有行動應用程式，且與資料主體互動並透過DSP推出行銷活動，您將需要下載適用於隱私權的行動SDK以進行Experience Cloud。 行動SDK可讓資料控制方設定選擇退出狀態標幟、擷取資料主體的裝置ID (名稱空間ID： `deviceID`)，並將請求提交至Privacy Service API。 您的行動應用程式將需要SDK 4.15.0版或更新版本。

   當您提交資料主體的存取請求時，Privacy ServiceAPI會根據指定的Cookie或裝置ID傳回資料主體的資訊，然後您必須將其傳回給資料主體。

   當您提交資料主體的刪除請求時，Cookie ID或裝置ID以及所有成本、點按和與Cookie相關聯的收入資料都會從伺服器刪除。

   >[!NOTE]
   >
   >如果您的公司有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 不過，您可以向多個Adobe Advertising子解決方案提出一個API請求([!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]、和 [!DNL DCO])，每個子解決方案各有一個帳戶。

所有這些步驟都是Adobe Advertising的必要步驟。 如需這些事項以及您需要使用Adobe Experience Platform Privacy Service執行的其他相關工作的詳細資訊，以及尋找所需專案的位置，請參閱&quot;[Privacy Service概觀](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).」

## Adobe Advertising JSON請求中的必填欄位值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud組織ID*>

`"users":`

* `"key":` &lt;*通常是資料主體的名稱*>

* `"action":` 兩者之一 `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (表示 [!DNL adcloud] Cookie空間)

   * `"value":` &lt;*擷取自之實際資料主體的Cookie ID值`AdobePrivacy.js`*>

* `"include": **adCloud**` (亦即 [!DNL Adobe] 適用於此要求的產品)

* `"regulation": **gdpr**` （適用於此請求的隱私權法規）

## 資料主體使用從中擷取之Adobe Advertising使用者ID提交的請求範例 `AdobePrivacy.js`

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
```

## 針對存取請求所傳回的資料欄位

以下是Adobe Advertising的存取回應範例。

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
