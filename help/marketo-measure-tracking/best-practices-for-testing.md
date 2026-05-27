---
description: Marketo Measure ユーザー向けテストガイダンスのベストプラクティス
title: テストのベストプラクティス
exl-id: ff95a1a9-d324-47f5-b47d-39014dff77e4
feature: Tracking
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
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

1. そのフォーム送信に対して CRM（リードまたは連絡先）で作成されたレコードを見つけて、タッチポイントが適切に作成されたことを確認します。

>[!NOTE]
>
>[!DNL Marketo Measure]のタッチポイントを持つリードなど、[!DNL Marketo Measure]のストックレポートを使用できます。または、[!DNL Marketo Measure]個の詳細を含むページレイアウトを更新することを選択した場合は、リード/連絡先ページレイアウトを参照してください。 データが処理されるまでに時間がかかることがあります。
