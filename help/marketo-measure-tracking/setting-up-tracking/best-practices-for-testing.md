---
unique-page-id: 18874722
description: テストのベストプラクティス — [!DNL Marketo Measure]  — 製品ドキュメント
title: テストのベストプラクティス
exl-id: ff95a1a9-d324-47f5-b47d-39014dff77e4
source-git-commit: 993a326c377b3b6ff48c4e0114b59297f9ca2ca6
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

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

1. フォーム送信用に CRM で作成されたレコード（リードまたは連絡先）を探し、タッチポイントが適切に作成されたことを確認します。

>[!NOTE]
>
>以下の [!DNL Marketo Measure] リードと次のアイテムの間の在庫レポート [!DNL Marketo Measure] タッチポイントを使用するか、ページレイアウトを次で更新するように選択した場合はリード/連絡先ページレイアウトを確認します。 [!DNL Marketo Measure] 詳細。 データの処理には時間がかかる場合があります。
