---
unique-page-id: 18874722
description: テストのベストプラクティス — [!DNL Marketo Measure]
title: テストのベストプラクティス
exl-id: ff95a1a9-d324-47f5-b47d-39014dff77e4
feature: Tracking
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 16%

---

# テストのベストプラクティス {#best-practices-for-testing}

様々な種類のフォームをすべてテストし、 [!DNL Marketo Measure] JavaScript は正常に動作しています。

## 推奨テストプロセス {#recommended-test-process}

1. 匿名ブラウザーを使用するか、各フォーム送信テストの間で cookie を消去します _および_ 毎回異なる電子メールアドレスを使用します。

   >[!TIP]
   >
   >ベストプラクティスは、テストであることを示す内容と時刻を含む偽の E メールを使用することです。 例： `testing830am@test.com`.

1. 検索エンジンで検索を開始する ( 例： `google.com`) または直接フォームに移動します。

1. 一意の電子メールアドレスを使用して、Web サイト上のフォームを送信します。

1. フォームを送信するページの URL と使用する電子メールアドレスを記録します。

1. そのフォーム送信に対して CRM（リードまたは連絡先）で作成されたレコードを見つけて、タッチポイントが適切に作成されたことを確認します。

>[!NOTE]
>
>次の項目を使用できます。 [!DNL Marketo Measure] リードと次のアイテムの間の在庫レポート [!DNL Marketo Measure] タッチポイントを使用するか、ページレイアウトを次で更新するように選択した場合はリード/連絡先ページレイアウトを確認します。 [!DNL Marketo Measure] 詳細。 データの処理には時間がかかる場合があります。
