---
description: Marketo Measure ユーザー向けテストガイダンスのベストプラクティス
title: テストのベストプラクティス
exl-id: ff95a1a9-d324-47f5-b47d-39014dff77e4
feature: Tracking
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: dcbeff6e-0253-5a4b-9ac2-1b67cc4a6286
    internal-label: Tracking
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 18%
---
# テストのベストプラクティス {#best-practices-for-testing}

[!DNL Marketo Measure] JavaScriptが正常に動作していることを確認するために、必要なさまざまな種類のフォームをすべてテストする必要があります。

## 推奨テストプロセス {#recommended-test-process}

1. シークレットブラウザーを使用するか、各フォーム送信テスト _と_&#x200B;の間でCookieをクリアして、毎回異なる電子メールアドレスを使用します。

   >[!TIP]
   >
   >ベストプラクティスは、テストであることを示す何かを含む偽の電子メールと時間帯を使用することです。 例：`testing830am@test.com`。

1. 検索エンジン （例：`google.com`）で検索を開始するか、フォームに直接移動します。

1. 一意のメールアドレスを使用して、web サイトでフォームを送信します。

1. フォームを送信するページのURLと、使用した電子メールアドレスを記録します。

1. そのフォーム送信に対して CRM（リードまたは取引先責任者）で作成されたレコードを見つけて、顧客接点が適切に作成されたことを確認します。

>[!NOTE]
>
>[!DNL Marketo Measure]のタッチポイントを持つリードなど、[!DNL Marketo Measure]のストックレポートを使用できます。または、[!DNL Marketo Measure]個の詳細を含むページレイアウトを更新することを選択した場合は、リード/連絡先ページレイアウトを参照してください。 データが処理されるまでに時間がかかることがあります。
