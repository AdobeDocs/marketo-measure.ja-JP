---
description: Marketo Measure ユーザー向けのプライバシーリクエストガイダンス
title: プライバシーリクエスト
exl-id: 883e475f-9868-412a-b505-230556f38484
feature: APIs, Tracking
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 53%

---


# プライバシーリクエスト {#privacy-requests}

このドキュメントでは、[!DNL Privacy Service] UIと&#x200B;**[!DNL Privacy Service]API**&#x200B;を通じて[!DNL Marketo Measure]に送信できる個々のデータプライバシー要求の管理の概要を説明します。

[!DNL Marketo Measure]から消費者データにアクセスして削除する個々のリクエストを送信するには、次の2つの方法があります。

* [[!DNL Privacy Service] UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/overview.html){target="_blank"}を使用します。
* **[!DNL Privacy Service]API**&#x200B;を使用します。 [こちら](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html){target="_blank"}のドキュメントと[こちら](https://developer.adobe.com/experience-platform-apis/references/privacy-service/){target="_blank"}の API リファレンスを参照してください。

[Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja){target="_blank"} では、データアクセスとデータ削除の 2 種類のリクエストがサポートされます。

ここでは、アクセスリクエストと削除リクエストの作成方法について説明します。

## Marketo Measureのリクエストを送信するには、設定が必要です {#required-setup-to-send-requests-for-marketo-measure}

[!DNL Marketo Measure]のデータへのアクセスと削除を要求するには、次の操作を行う必要があります。

1. 以下を特定します。

   a. IMS Org ID

   b. アクションを実行するユーザーの電子メールアドレス

   IMS 組織 ID は、24 文字の英数字から成る文字列で、末尾に @AdobeOrg が付きます。 マーケティングチームまたはアドビの内部システム管理者が組織の IMS Org ID を把握していない場合は、アドビカスタマーケア（gdprsupport@adobe.com）にお問い合わせください。 Privacy API にリクエストを送信するには、IMS 組織 ID が必要です。

1. [!DNL Privacy Service]では、アクセス要求と削除要求を[!DNL Marketo Measure]に送信し、既存の要求のステータスを確認できます。

## [!DNL Marketo Measure] JSON リクエストの必須フィールド値 {#required-field-values-in-marketo-measure-json-requests}

“companyContexts”：

* &quot;namespace&quot;：**imsOrgID**
* &quot;value&quot;：`<Your IMS Org ID Value>`

&quot;users&quot;：

* &quot;action&quot;: [!UICONTROL access]またはdelete
* “userIDs”：
   * &quot;namespace&quot;: email
   * &quot;type&quot;: standard
   * &quot;value&quot;：`<Data Subject's Email Address>`

“include”：

* **marketoMeasure** （リクエストに適用されるAdobe製品）

“regulation”：

* **gdpr、**、**ccpa**、**pdpa**、**lgpd_bra**&#x200B;**nzpa_nzl** のいずれか（リクエストに適用されるプライバシー規則）

## 例 1：GDPR 削除リクエスト {#gdpr-delete-request}

JSON リクエスト

```json
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

```json
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

```json
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

```json
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
