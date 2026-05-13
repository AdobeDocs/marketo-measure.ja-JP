---
description: ステージマッピングのベストプラクティス - [!DNL Marketo Measure]
title: ステージマッピングのベストプラクティス
exl-id: 1ed380a1-4a3a-4761-b70f-cdf2e290329d
feature: Tracking, Custom Models
TQID: https://experienceleague.adobe.com/qhyIo6WXhidNmLJhkattZDP-SG6tPxrVtzl7I8fwGPg
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 479
ht-degree: 4%

---

# ステージマッピングのベストプラクティス {#best-practices-for-stage-mapping}

## 概要 {#overview}

[!DNL Marketo Measure] アカウントの「ステージのマッピング」セクションには、[!DNL Marketo Measure]がCRMから自動的に取得するステージと、カスタムアトリビューションモデルを使用する場合に定義したカスタムステージの概要が表示されます。 お客様の[!DNL Marketo Measure] データの有効性は、これらのステージが正しく順序付けられているかどうかにかかっています。これにより、[!DNL Marketo Measure]がお客様のfunnelとfunnel全体のレコードの進行状況を正確に把握できます。

[!DNL Marketo Measure] インスタンスの「ステージのマッピング」セクションには、CRMのアクティブなステージと非アクティブなステージの両方が表示されます。 Adobe funnelの現状を把握し、各段階を可能な限り適切に順序付けします。

このセクションで管理されるその他の機能はFunnelのステージで、アトリビューションを適用せずにfunnelにステージを追加することができます。 Funnelのステージはタッチポイントとして追跡され、CRMの「タッチポイントの順位」フィールドに入力されます。 これらのFunnel ステージは、[!DNL Marketo Measure] Discoverの様々なジャーニーボードでも表されます。

## ベストプラクティス {#best-practices}

初めてステージマッピングを評価する場合でも、funnelの注文を確認する場合でも、次のベストプラクティスを念頭に置くことが重要です。

* 注文が全てです！
   * [!DNL Marketo Measure]がCRMからアクティブなステージと非アクティブなステージの両方を取得することを考慮して、リード/取引先責任者または商談で使用できるステージがグループ化され、それに応じて並べ替えられることを確認します
* カスタムステージを定義する際は、ステージの定義に使用するフィールドに対して、フィールド履歴トラッキングが有効になっていることを確認します
* カスタムステージの定義に数式フィールドを使用しない
   * ブール値フィールドは、ベストプラクティスの推奨事項です
* 「リード」または「コンタクト」ステージのセクションは、「失注」、「オープン」および「コンバージョン」に分かれています。ステージが適切なステージのセクションにあることを確認します
   * ステージが正しくないステージセクションにある場合、非常に不正確な[!DNL Marketo Measure] データになる可能性があります
   * Marketo Measure Ultimateのお客様で、デフォルトのダッシュボードオブジェクトを「連絡先」に設定している場合は、リード（[詳細情報](/help/marketo-measure-ultimate/data-integrity-requirement.md){target="_blank"}）に固有の次の2つのフィールドを使用しないでください。
      * b2b.personStatus
      * b2b.isConverted
* 「商談ステージ」セクションは、「失注」、「オープン」、「獲得」に分かれています。ステージが適切なステージのセクションにあることを確認します
   * ステージが正しくないステージセクションにある場合、[!DNL Marketo Measure]収益またはパイプライン収益データが非常に正しくない可能性があります
* 重複したステージ名は使用しないでください（システムがそれらを検出し、自動的に削除します）。
* NULL値をチェックするルールを設定するには、「値」テキストボックスを空白のままにします。

## メンテナンスのベストプラクティス {#best-practices-for-maintenance}

年に1回ステージマッピングを確認すると、[!DNL Marketo Measure]の商談データが正確かつ最新であることを確認できます。

ステージマッピングのレビューをトリガーする可能性があるその他の理由には、次のようなものがあります。

* マーケティングチームの入れ替わり
* CRMの各段階に対する変更は
* 組織のfunnelのアップデート
* [!DNL Marketo Measure] レポートに誤った収益データが表示されています

>[!MORELIKETHIS]
>
>[Funnel ステージとカスタムモデル ステージの違い](/help/advanced-marketo-measure-features/custom-attribution-models/custom-attribution-model-and-setup.md#the-difference-between-funnel-stages-and-custom-model-stages)
