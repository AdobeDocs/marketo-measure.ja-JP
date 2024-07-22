---
description: ステージマッピングのベストプラクティス - [!DNL Marketo Measure]
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

[!DNL Marketo Measure] アカウントの「ステージマッピング」セクションでは、CRM から自動的に取り込 [!DNL Marketo Measure] れるステージと、カスタム属性モデルを使用する場合に定義したカスタムステージの概要が説明されます。 [!DNL Marketo Measure] データの有効性は、これらのステージが正しく並べ替えられていることに依存して [!DNL Marketo Measure] るので、ファネルとそのファネル全体でのレコードの進行状況を正確に理解できます。

[!DNL Marketo Measure] インスタンスの「ステージマッピング」セクションには、CRM のアクティブなステージと非アクティブなステージの両方が表示されます。 ファネルの現在の状態に合わせて、能力を最大限に発揮するようにすべてのステージを並べ替えます。

この節で管理される追加機能は、ファネルステージです。この機能を使用すると、アトリビューションを適用せずにファネルにステージを追加できます。 ファネルステージは、タッチポイントとして追跡され、CRM の「タッチポイント位置」フィールドに入力されます。 これらのファネルステージは、[!DNL Marketo Measure] Discover の様々なジャーニーボードでも表示されます。

## ベストプラクティス {#best-practices}

ステージマッピングを初めて評価する場合でも、ファネルの順序をレビューするだけの場合でも、次のベストプラクティスを念頭に置くことが重要です。

* 秩序が全てだ！
   * CRM からアクティブなステージ [!DNL Marketo Measure] 非アクティブなステージの両方を取り込むことを検討し、リード/連絡先またはオポチュニティで使用できるすべてのステージがそれに応じてグループ化され、順序付けられていることを確認します
* カスタムステージを定義する場合は、ステージの定義に使用されるすべてのフィールドでフィールド履歴のトラッキングが有効になっていることを確認します
* 式フィールドを使用してカスタムステージを定義しないでください
   * ブール値フィールドは、ベストプラクティスの推奨事項です
* リードまたは連絡先ステージのセクションは、損失、オープン、コンバートに分かれています。ステージが適切なステージセクションにあることを確認します
   * 誤ったステージセクションにステージがあると、[!DNL Marketo Measure] データが非常に不正確になる場合があります
   * Marketo Measure Ultimate のお客様で、デフォルトのダッシュボードオブジェクトを連絡先として設定している場合、リード固有の以下の 2 つのフィールドを使用しないでください（[ 詳細情報 ](/help/marketo-measure-ultimate/data-integrity-requirement.md){target="_blank"}）。
      * b2b.personStatus
      * b2b.isConverted
* 商談ステージのセクションは、損失、オープン、獲得に分かれています。ステージが適切なステージセクションにあることを確認してください
   * 誤ったステージセクションにステージがあると、[!DNL Marketo Measure] ージの売上高やパイプラインの売上高データが非常に不正確になる可能性があります
* 重複したステージ名の使用は避けてください（システムによって検出され、自動的に削除されます）。
* NULL 値をチェックするルールを設定するには、値テキスト・ボックスを空白のままにします。

## メンテナンスのベストプラクティス {#best-practices-for-maintenance}

年に 1 回ステージマッピングをレビューすることで、[!DNL Marketo Measure] の商談データが正確かつ最新であることを確認できます。

ステージマッピングのレビューをトリガーするその他の理由には、次のものがあります。

* マーケティングチームの入れ替わり
* CRM ステージに対する変更
* 組織のファネルに対する更新
* [!DNL Marketo Measure] レポートに間違った売上高データが表示される

>[!MORELIKETHIS]
>
>[ ファネルステージとカスタムモデルステージの違い ](/help/advanced-marketo-measure-features/custom-attribution-models/custom-attribution-model-and-setup.md#the-difference-between-funnel-stages-and-custom-model-stages)
