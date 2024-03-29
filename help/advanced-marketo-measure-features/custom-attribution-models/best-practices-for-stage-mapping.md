---
description: ステージマッピングのベストプラクティス — [!DNL Marketo Measure]
title: ステージマッピングのベストプラクティス
exl-id: 1ed380a1-4a3a-4761-b70f-cdf2e290329d
feature: Tracking, Custom Models
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 4%

---

# ステージマッピングのベストプラクティス {#best-practices-for-stage-mapping}

## 概要 {#overview}

「ステージマッピング」セクション ( [!DNL Marketo Measure] アカウントは、次の段階の概要を説明します。 [!DNL Marketo Measure] は、カスタムアトリビューションモデルを使用している場合に、CRM と定義したカスタムステージからを自動的に取り込みます。 お客様の [!DNL Marketo Measure] データは、次のステージが正しく並べ替えられているので、 [!DNL Marketo Measure] では、ファネルと、同じファネル全体でのレコードの進行を正確に把握できます。

(「 [!DNL Marketo Measure] インスタンスを選択すると、CRM のアクティブなステージと非アクティブなステージの両方が表示されます。 すべてのステージを、現在のファネルの状態に合わせて、最高の能力に合わせて並べます。

この節で管理される追加の機能はファネルステージで、アトリビューションを適用せずにファネルにステージを追加できます。 ファネルステージは、タッチポイントとして追跡され、CRM の「タッチポイントの位置」フィールドに入力されます。 これらのファネルステージは、 [!DNL Marketo Measure] 検出。

## ベストプラクティス {#best-practices}

初めてステージマッピングを評価する場合でも、ファネルの順序を確認する場合でも、次のベストプラクティスを念頭に置いておくことが重要です。

* 命令が全てだ！
   * 検討中 [!DNL Marketo Measure] CRM からアクティブなステージと非アクティブなステージの両方を取り込み、リード/連絡先または商談で使用できるステージがグループ化され、それに応じて並べ替えられていることを確認します。
* カスタムステージを定義する際に、ステージの定義に使用するフィールドに対して、フィールド履歴の追跡が有効になっていることを確認します。
* 数式フィールドを使用してカスタムステージを定義しないでください
   * ベストプラクティスの推奨事項は、ブール型フィールドです。
* 「リード」または「連絡先」のステージ・セクションは、「損失」、「オープン」、「コンバート済」に分割されています。ステージが適切なステージ・セクションにあることを確認してください。
   * 間違ったステージセクションにステージがあると、高度に誤った結果になる可能性があります [!DNL Marketo Measure] データ
   * Marketo Measure Ultimate のお客様で、デフォルトのダッシュボードオブジェクトを連絡先に設定している場合は、リード ([詳細情報](/help/marketo-measure-ultimate/data-integrity-requirement.md){target="_blank"}) をクリックします。
      * b2b.personStatus
      * b2b.isConverted
* 商談ステージのセクションは、損失、オープン、獲得に分割されています。ステージが適切なステージのセクションにあることを確認してください。
   * 間違ったステージセクションにステージがあると、高度に誤った結果になる可能性があります [!DNL Marketo Measure] 売上高またはパイプライン売上高データ
* 重複するステージ名の使用は避けます（システムによって重複するステージ名が検出され、自動的に削除されます）。
* NULL 値をチェックするルールを設定するには、「値」テキスト・ボックスを空白のままにします。

## メンテナンスのベストプラクティス {#best-practices-for-maintenance}

年に 1 回ステージマッピングを確認すると、商談データが [!DNL Marketo Measure] は正確で最新の状態です。

ステージマッピングのレビューをトリガーにするその他の理由は次のとおりです。

* マーケティングチームの入れ替わり
* CRM ステージに対する変更
* 組織のファネルの更新
* 売上高データが正しく表示されていません [!DNL Marketo Measure] レポート

>[!MORELIKETHIS]
>
>[ファネルステージとカスタムモデルステージの違い](/help/advanced-marketo-measure-features/custom-attribution-models/custom-attribution-model-and-setup.md#the-difference-between-funnel-stages-and-custom-model-stages)
