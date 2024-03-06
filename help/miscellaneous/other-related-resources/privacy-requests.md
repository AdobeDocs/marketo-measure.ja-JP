---
description: プライバシーリクエスト — [!DNL Marketo Measure]
title: プライバシーリクエスト
exl-id: 883e475f-9868-412a-b505-230556f38484
feature: APIs, Tracking
source-git-commit: 4787f765348da71bc149c997470ce678ba498772
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 20%

---

# プライバシーリクエスト {#privacy-requests}

このドキュメントでは、に送信できる個々のデータのプライバシーリクエストの管理の概要を説明します [!DNL Marketo Measure] から [!DNL Privacy Service] UI と **[!DNL Privacy Service]API**.

から消費者データにアクセスして削除する個々のリクエストを送信できます。 [!DNL Marketo Measure] 次の 2 つの方法で説明します。

* を通じて [[!DNL Privacy Service] UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/overview.html){target="_blank"}.
* を通じて **[!DNL Privacy Service]API**. ドキュメントを参照してください [ここ](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html){target="_blank"} and the API reference [here](https://developer.adobe.com/experience-platform-apis/references/privacy-service/){target="_blank"}.

The [Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja){target="_blank"} は、データアクセスとデータ削除の 2 種類のリクエストをサポートします。

ここでは、アクセスリクエストと削除リクエストの作成方法について説明します。

## Marketo Measureのリクエストを送信するための必須設定 {#required-setup-to-send-requests-for-marketo-measure}

のデータのアクセスおよび削除をリクエストするには、以下を実行します。 [!DNL Marketo Measure]を使用する場合は、次の操作を行う必要があります。

1. 以下を特定します。

   a. IMS Org ID

   b.行動を起こす人のメールアドレス

   IMS 組織 ID は、24 文字の英数字から成る文字列で、末尾に @AdobeOrg が付きます。マーケティングチームまたは内部Adobeシステム管理者が組織の IMS Org ID を把握していない場合は、Adobeカスタマーケア (gdprsupport@adobe.com) にお問い合わせください。 Privacy API にリクエストを送信するには、IMS 組織 ID が必要です。

1. In [!DNL Privacy Service]を使用すると、アクセス要求と削除要求を [!DNL Marketo Measure]、および既存のリクエストのステータスを確認します。

## 必須フィールド値： [!DNL Marketo Measure] JSON リクエスト {#required-field-values-in-marketo-measure-json-requests}

&quot;companyContexts&quot;:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: `<Your IMS Org ID Value>`

&quot;users&quot;:

* &quot;action&quot;：次のいずれか [!UICONTROL アクセス] または削除
* &quot;userIDs&quot;:
   * &quot;namespace&quot;: email
   * &quot;type&quot;: standard
   * &quot;value&quot;: `<Data Subject's Email Address>`

&quot;include&quot;:

* **marketoMeasure** ( リクエストに適用されるAdobe製品 )

&quot;regulation&quot;:

* **gdpr**, **ccpa**, **pdpa**, **lgpd_bra**&#x200B;または **nzpa_nzl** （リクエストに適用されるプライバシー規則）

## 例 1：GDPR 削除リクエスト {#gdpr-delete-request}

JSON リクエスト

```text
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "1231659F56A68A8B7F000101@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
        "delete"
      ],
      "userIDs": [
        {
          "namespace": "email",
          "type": "standard",
          "value": "john.doe@adobe.com"
        }
      ]
    }
  ],
  "include": [
    "marketoMeasure"
  ],
  "regulation": "gdpr",
}
```

JSON 応答

```text
{
  "requestId": "16331241037112570RX-245",
  "totalRecords": 1,
  "jobs": [
    {
      "jobId": "997b01e3-9568-402c-904b-b4e60a437875",
      "customer": {
        "user": {
          "action": [
            "delete"
          ],
          "userIDs": [
            {
              "namespace": "email",
              "value": "john.doe@adobe.com",
              "type": "standard",
              "namespaceId": 6,
              "isDeletedClientSide": false
            }
          ]
        }
      }
    }
  ]
}
```

## 例 2：CCPA アクセスリクエスト {#ccpa-access-request}

JSON リクエスト

```text
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "1231659F56A68A8B7F000101@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
        "access"
      ],
      "userIDs": [
        {
          "namespace": "email",
          "type": "standard",
          "value": "john.doe@adobe.com"
        }
      ]
    }
  ],
  "include": [
    "marketoMeasure"
  ],
  "regulation": "ccpa",
}
```

JSON 応答

```text
{
  "requestId": "16329573462631890RX-207",
  "totalRecords": 1,
  "jobs": [
    {
      "jobId": "3115e42d-011b-47ab-a2b0-ed4356af4d3e",
      "customer": {
        "user": {
          "action": [
            "access"
          ],
          "userIDs": [
            {
              "namespace": "email",
              "value": "john.doe@adobe.com",
              "type": "standard",
              "namespaceId": 6,
              "isDeletedClientSide": false
            }
          ]
        }
      }
    }
  ]
}
```
