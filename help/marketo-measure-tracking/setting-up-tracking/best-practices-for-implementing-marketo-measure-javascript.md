---
description: 実装のベストプラクティス [!DNL Marketo Measure] JavaScript - [!DNL Marketo Measure]  — 製品ドキュメント
title: 実装のベストプラクティス [!DNL Marketo Measure] JavaScript
exl-id: 0359ad27-81e8-4902-a23a-49a5646a44d0
source-git-commit: cf144eb4bc9282ae6a260acd3735f24644292a19
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 実装のベストプラクティス [!DNL Marketo Measure] JavaScript {#best-practices-for-implementing-marketo-measure-javascript}

## 概要 {#overview}

この [!DNL Marketo Measure] JavaScript は、Web 訪問者のデジタルマーケティングインタラクションを追跡し、 [!DNL Marketo Measure] オンラインタッチポイントデータを作成する機能。 を持つ [!DNL Marketo Measure] サイト全体に正しく包括的にデプロイされた JavaScript により、収集されたセッションデータで正確なタッチポイントデータが生成されます。

のデプロイメントでの不整合 [!DNL Marketo Measure] JavaScript は、セッションデータで中断を引き起こし、次の結果が生じる可能性があります。

* チャネル/サブチャネルのアトリビューションが正しくありません
* ソースデータの喪失
* 誤った直接トラフィックの高レベル
* レポートの一貫性が失われました

[!DNL Marketo Measure] JavaScript は、 [!DNL Marketo Measure] アカウントと鍵を活用して成功を収めてください。

## ベストプラクティス {#best-practice}

の実装と管理に関しては、 [!DNL Marketo Measure] JavaScript では、次のベストプラクティスに留意してください。

* すべてのドメインが [!DNL Marketo Measure] アカウント
   * お使いのドメインに関するご不明な点は、サポートまでお問い合わせください
* すべてのページに JavaScript をデプロイします。
   * 特定のページにのみ JavaScript を配置すると、セッションデータに中断が発生し、誤った結果が生じます [!DNL Marketo Measure] データ
* サイト上のフォームで、タッチポイントを作成しない場合は、必ず [!DNL Marketo Measure] スクリプトを除外
   * この除外スクリプトは、 [!DNL Marketo Measure] セッションデータは中断されず、ソースデータはそのまま残ります
      * 抑制する一般的なフォームの例を次に示します。
         * 顧客ログイン
         * パスワードフォームを忘れた場合
         * フォームを配信停止
         * キャリアアプリケーションフォーム
* 追加の「その他の考慮事項」および「Formsが特に注意を払うための注意事項」の節を確認します。 [!DNL Marketo Measure] 以下に示すスクリプトリソースを使用して、特別な処理が必要なシナリオを確認します

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

この [!DNL Marketo Measure] JavaScript は、初回導入時に適用され、サイトや管理するチームに対する変更により、 [!DNL Marketo Measure] トラッキング。 次を確認することをお勧めします： [!DNL Marketo Measure] JavaScript は、年に 1 回、適切かつ包括的にデプロイされます。 また、組織が Web サイトに関する変更プロトコルに関するドキュメントのタイプを持っている場合は、それを説明する部分があることを確認します。 [!DNL Marketo Measure] JavaScript は、新しいすべてのページで保持または追加する必要があります。

JavaScript の設定のレビューにトリガーが生じる可能性があるその他の理由は次のとおりです。

* マーケティングチームの売上高
* サイト構造の変更と更新
* サイトの移行
* ドメインの変更
* 他の会社とその Web プロパティの取得
