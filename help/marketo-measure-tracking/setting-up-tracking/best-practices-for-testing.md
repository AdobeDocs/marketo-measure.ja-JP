---
unique-page-id: 18874722
description: テストのベストプラクティス - [!DNL Marketo Measure]
title: テストのベストプラクティス
exl-id: ff95a1a9-d324-47f5-b47d-39014dff77e4
feature: Tracking
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 19%

---

# テストのベストプラクティス {#best-practices-for-testing}

必要な各種フォームをすべてテストして、[!DNL Marketo Measure] JavaScriptが正しく動作していることを確認する必要があります。

## 推奨テストプロセス {#recommended-test-process}

1. シークレットブラウザーを使用するか、各フォーム送信テストの間に Cookie を消去します _および_ 毎回異なるメールアドレスを使用します）。

   >[!TIP]
   >
   >ベストプラクティスは、テストであることを示す内容と時間帯を含んだ偽のメールを使用することです。 例：`testing830am@test.com`。

1. 検索エンジン（`google.com` など）で検索を開始するか、フォームに直接移動します。

1. 一意のメールアドレスを使用して、web サイトにフォームを送信します。

1. フォームを送信するページの URL と、使用するメールアドレスを記録します。

1. そのフォーム送信に対して CRM（リードまたは連絡先）で作成されたレコードを見つけて、タッチポイントが適切に作成されたことを確認します。

>[!NOTE]
>
>[!DNL Marketo Measure] タッチポイントを使用したリードなどの [!DNL Marketo Measure] しい在庫レポートを使用したり、[!DNL Marketo Measure] しい詳細でページレイアウトを更新することを選択した場合は、リード/連絡先ページレイアウトを調べたりできます。 データが処理されるまでしばらく時間がかかる場合があります。
