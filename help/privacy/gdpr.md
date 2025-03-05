---
title: Adobe Advertising支援一般資料保護規範
description: 瞭解支援的資料請求型別、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8e9dac77b4f687fb175adaf27a4e726fa80ca7b4
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Adobe Advertising支援一般資料保護規範

*適用於[!DNL Adobe Advertising Search, Social, & Commerce]、Adobe Advertising DSP、Adobe Advertising Creative和Adobe Advertising DCO*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 請諮詢您的法律顧問，以獲得有關一般資料保護規範的建議。

2018年5月25日生效的一般資料保護規範(GDPR)賦予歐盟(EU)境內所有個人（資料主體）掌控其個人資料的權利，並簡化國際業務的法規環境。 此法律適用於向歐盟境內之個人提供商品或服務、監控其行為或收集其個人資料的所有企業（資料控管單位），無論資料控管單位的營業地點為何，其個人資料處理作業均適用此法律。

Adobe Experience Cloud代表客戶擔任資料處理者的角色，依指示接收和儲存的任何個人資料。 身為資料控管單位，您可以決定要由Adobe Experience Cloud代表您處理和儲存哪些個人資料。

本檔案說明[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP (Demand Side Platform)和[!DNL Advertising DCO]如何使用Adobe Experience Platform Privacy Service API和Privacy Service UI支援資料主體的GDPR資料存取和刪除許可權。

如需有關GDPR對您業務之意義的詳細資訊，請參閱[GDPR與您的業務](https://www.adobe.com/privacy/general-data-protection-regulation.html)。

## Adobe Advertising支援的資料請求型別

Adobe Experience Platform讓企業能夠完成下列工作：

* 在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]記憶體取資料主體的Cookie層級資料或裝置ID層級資料（適用於行動應用程式中的廣告）。
* 針對使用瀏覽器的資料主體，刪除儲存在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中的Cookie層級資料；針對使用行動裝置上應用程式的資料主體，刪除儲存在[!DNL DSP]中的ID層級資料。
* 檢查一個或所有現有請求的狀態。

## 傳送Adobe Advertising請求的必要設定

若要請求存取和刪除Adobe Advertising的資料，您必須：

1. 部署JavaScript程式庫以擷取和移除您的資料主體Cookie。 所有Adobe Experience Cloud解決方案都使用相同的資料庫`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >請求某些Experience Cloud解決方案不需要JavaScript資料庫，但請求給Adobe Advertising則需要它。

   您應將資料庫部署在資料主體可提交存取和刪除請求的網頁上，例如您公司的隱私權入口網站。 資料庫可協助您擷取[!DNL Adobe] Cookie （名稱空間識別碼： `gsurferID`），這樣您就可以透過Adobe Experience Platform Privacy Service API提交這些身分識別，作為存取和刪除請求的一部分。

   當資料主體要求刪除個人資料時，資料庫也會從資料主體的瀏覽器中刪除資料主體的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，後者會停止以對象區段鎖定一般使用者。 但是，當資料主體要求從[!DNL Creative]、[!DNL DSP]或[!DNL DCO]刪除個人資料時，資料庫也會傳送要求給Adobe Advertising，以選擇退出資料主體進行區段鎖定目標。 對於具有[!DNL Search, Social, & Commerce]的廣告商，建議您提供資料主體一個[https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)的連結，說明如何選擇退出對象區段鎖定目標。

1. 識別您的Experience Cloud組織ID，並確定其已連結至您的Adobe Advertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，通常會加上「@AdobeOrg」。 大部分Experience Cloud客戶已指派組織ID。 如果您的行銷團隊或內部[!DNL Adobe]系統管理員不知道您的組織ID，或不確定其是否已布建，請透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您需要組織識別碼，才能使用`imsOrgID`名稱空間將請求提交至隱私權API。

   >[!IMPORTANT]
   >
   >請聯絡貴公司的Adobe Advertising代表，確認貴組織的所有Adobe Advertising帳戶（包括[!DNL DSP]帳戶或廣告商、[!DNL Search, Social, & Commerce]帳戶及[!DNL Creative]或[!DNL DCO]帳戶）都與您的Experience Cloud組織ID連結。

1. 使用[Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （適用於自動要求）或[Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （適用於臨機要求），代表資料主體向Adobe Advertising提交存取和刪除要求，以及檢查現有要求的狀態。

   如果廣告商擁有行動應用程式，能與資料主體互動並與DSP一起推出行銷活動，您必須下載適用於Experience Cloud的隱私權就緒行動SDK。 Mobile SDK可讓資料控管單位設定選擇退出狀態旗標、擷取資料主體的裝置ID （名稱空間ID： `deviceID`），以及將請求提交至Privacy Service API。 您的行動應用程式將需要SDK 4.15.0版或更新版本。

   當您提交資料主體的存取請求時，Privacy Service API會根據指定的Cookie或裝置ID傳回資料主體的資訊，然後您必須將其傳回給資料主體。

   當您提交資料主體的刪除請求時，Cookie ID或裝置ID以及所有成本、點按和與Cookie相關聯的收入資料都會從伺服器刪除。

   >[!NOTE]
   >
   >如果您的公司有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 但是，您可以向多個Adobe Advertising子解決方案（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]和[!DNL DCO]）提出一個API請求，每個子解決方案使用一個帳戶。

Adobe Advertising需要所有步驟。 如需關於這些事項以及您需要使用Adobe Experience Platform Privacy Service執行的其他相關工作的詳細資訊，以及尋找必要專案的位置，請參閱&quot;[Privacy Service概觀](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)&quot;。

## Adobe Advertising JSON請求中的必填欄位值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud組織ID*>

`"users":`

* `"key":` &lt;*通常是資料主體的名稱*>

* `"action":` `**access**`或`**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示[!DNL adcloud] Cookie空間）

   * `"value":` &lt;*從`AdobePrivacy.js`*&#x200B;擷取的實際資料主體的Cookie ID值>

* `"include": **adCloud**` （適用於此請求的[!DNL Adobe]產品）

* `"regulation": **gdpr**` （適用於此請求的隱私權法規）

## 資料主體使用從`AdobePrivacy.js`擷取的Adobe Advertising使用者ID提交的請求範例

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
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```

<!-- Changed example from BlueKai (no longer supported) to Exelate -->
