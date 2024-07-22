---
description: ' [!DNL Marketo Measure]  JavaScript の実装のベストプラクティス -  [!DNL Marketo Measure]'
title: ' [!DNL Marketo Measure] JavaScript の実装のベストプラクティス'
exl-id: 0359ad27-81e8-4902-a23a-49a5646a44d0
feature: Tracking
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 100%

---

# [!DNL Marketo Measure]JavaScript の実装のベストプラクティス {#best-practices-for-implementing-marketo-measure-javascript}

## 概要 {#overview}

[!DNL Marketo Measure] JavaScript は、web 訪問者のデジタルマーケティングインタラクションを追跡し、オンラインタッチポイントデータを作成する [!DNL Marketo Measure] 機能の鍵となります。[!DNL Marketo Measure] JavaScript をサイト全体に正しく包括的にデプロイすると、収集されたセッションデータから正確なタッチポイントデータが確実に生成されます。

[!DNL Marketo Measure] JavaScript のデプロイメントに不一致があると、セッションデータが中断され、次のような問題が発生する可能性があります。

* 正しくないチャネル／サブチャネルのアトリビューション
* ソースデータの損失
* 高レベルの誤ったダイレクトトラフィック
* 一貫性のないレポート

[!DNL Marketo Measure] JavaScript は、[!DNL Marketo Measure] アカウントの基盤部分であり、成功の鍵です。

## ベストプラクティス {#best-practice}

[!DNL Marketo Measure] JavaScript を実装および管理する場合は、次のベストプラクティスに留意してください。

* すべてのドメインが [!DNL Marketo Measure] アカウントにリストされていることを確認します
   * ドメインに関して懸念がある場合は、サポートにお問い合わせください
* すべてのページに JavaScript をデプロイします。
   * 特定のページにのみ JavaScript を配置すると、セッションデータが中断され、正しくない [!DNL Marketo Measure] データが発生します
* タッチポイントを作成しないサイト上のフォームには、[!DNL Marketo Measure] Exclude スクリプトを追加する必要があります
   * この除外スクリプトにより、[!DNL Marketo Measure] セッションデータが中断されず、ソースデータが適切な場所に維持することが保証されます。
      * 抑制する一般的なフォームの例を次に示します。
         * 顧客ログイン
         * パスワードフォームを忘れた場合のフォーム
         * 購読解除フォーム
         * キャリアアプリケーションフォーム
* 以下にリストされている [!DNL Marketo Measure] スクリプトの追加リソースの「追加の考慮事項」および「特別な注意を払うべきフォーム」の節を確認して、特別な処理が必要なシナリオがないか確認します

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

[!DNL Marketo Measure] JavaScript の設定は初期実装中に適用されますが、サイトや管理するチームに変更を行うと、[!DNL Marketo Measure] のトラッキングが中断される可能性があります。[!DNL Marketo Measure] JavaScript が正しくかつ包括的にデプロイされていることを年に 1 回確認することをお勧めします。さらに、組織に web サイト用の変更プロトコルのドキュメントがある場合は、[!DNL Marketo Measure] JavaScript をすべての新しいページに保持／追加する必要があることを説明する部分があることを確認します。

JavaScript 設定のレビューをトリガーする可能性があるその他の理由としては、次のようなものがあります。

* マーケティングチームの入れ替わり
* サイト構造の変更と更新
* サイトの移行
* ドメインの変更
* 他の会社とその web プロパティの買収
