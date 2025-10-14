---
description: プライバシーリクエスト - [!DNL Marketo Measure]
title: プライバシーリクエスト
exl-id: 883e475f-9868-412a-b505-230556f38484
feature: APIs, Tracking
source-git-commit: 4787f765348da71bc149c997470ce678ba498772
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 20%

---

# プライバシーリクエスト {#privacy-requests}

このドキュメントでは、[!DNL Privacy Service] UI と **[!DNL Privacy Service]API** を使用して [!DNL Marketo Measure] に送信できる個々のデータプライバシーリクエストの管理の概要について説明します。

個々のリクエストを送信して、[!DNL Marketo Measure] から消費者データにアクセスしたり削除したりするには、次の 2 つの方法があります。

* [[!DNL Privacy Service] UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/overview.html?lang=ja){target="_blank"} を使用する。
* **[!DNL Privacy Service]API** を使用する。 詳しくは、ドキュメント [&#x200B; こちら &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=ja){target="_blank"} および API リファレンス [&#x200B; こちら &#x200B;](https://developer.adobe.com/experience-platform-apis/references/privacy-service/){target="_blank"} を参照してください。

[Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja){target="_blank"} は、データアクセスおよびデータ削除の 2 種類のリクエストをサポートしています。

アクセスリクエストと削除リクエストの作成方法を見てみましょう。

## Marketo Measureのリクエストを送信するために必要な設定 {#required-setup-to-send-requests-for-marketo-measure}

[!DNL Marketo Measure] のデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. 以下を特定します。

   a. IMS 組織 ID

   b.行動の対象となるユーザーのメールアドレス

   IMS 組織 ID は、24 文字の英数字から成る文字列で、末尾に @AdobeOrg が付きます。マーケティングチームまたは社内Adobeシステム管理者が、組織の IMS 組織 ID を把握していない場合は、Adobeカスタマーケア（gdprsupport@adobe.com）にお問い合わせください。 Privacy API にリクエストを送信するには、IMS 組織 ID が必要です。

1. [!DNL Privacy Service] では、[!DNL Marketo Measure] にアクセスリクエストと削除リクエストを送信し、既存のリクエストのステータスを確認できます。

## [!DNL Marketo Measure] JSON リクエストの必須フィールド値 {#required-field-values-in-marketo-measure-json-requests}

「companyContexts」:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: `<Your IMS Org ID Value>`

「ユーザー」:

* 「アクション」:「アクセス [!UICONTROL &#x200B; または削除 &#x200B;]
* &quot;userIDs&quot;:
   * 「名前空間」：メール
   * &quot;type&quot;：標準
   * &quot;value&quot;: `<Data Subject's Email Address>`

&quot;include&quot;:

* **marketoMeasure** （リクエストに適用されるAdobe商品）

規制：

* **gdpr**、**ccpa**、**pdpa**、**lgpd_bra**、または **nzpa_nzl** （リクエストに適用されるプライバシー規制）

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
