---
unique-page-id: 18874535
description: フルサークルから [!DNL Marketo Measure] に移行中 –  [!DNL Marketo Measure]
title: Full Circle から [!DNL Marketo Measure] への移行
exl-id: fd471771-33e2-413a-b155-02ba6e32e10c
feature: Attribution, Fundamentals
TQID: https://experienceleague.adobe.com/OhedmCiywt5OWRw1EMsLdnLs-Sxv4DWNpZdwXqHok9E
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 634
ht-degree: 0%

---

# フルサークルから[!DNL Marketo Measure]に移行中 {#transitioning-to-marketo-measure-from-full-circle}

フルサークルから[!DNL Marketo Measure]に移動しますか？ 実際、多くのマーケターがアジャイルマーケティングに関心を示しています。 ここでは、留意すべき最大の点と、移行した他の顧客から学んだ教訓を紹介します。

## キャンペーンベーストラッキングとマルチSourceトラッキングの違い {#campaign-based-tracking-vs-multi-source-tracking}

[!UICONTROL  フルサークル ]でのやり取りはすべて、CRM キャンペーンメンバーシップを通じて追跡されます。 [!DNL Marketo Measure]では、購買ジャーニーは、JavaScript、CRM キャンペーンメンバーシップ、CRM アクティビティレコードの組み合わせによってコンパイルされます。 「アトリビューションレポートを機能させるには、CRM キャンペーンでのあらゆるインタラクションを追跡する必要がある」から「アトリビューションレポートを機能させるには、このインタラクションのサブセットのみをCRM キャンペーンで追跡する必要がある」へと精神的に切り替えるのは困難です。

一般的に、[!DNL Marketo Measure]が主な種類のインタラクションのタッチポイントレコードを作成する方法は次のとおりです。

* サイトでのフォーム入力：[!DNL Marketo Measure] JavaScript
* サイトのページビュー：このページビューが指定されたCRM マイルストーン（リードまたは商談作成など）を促進した場合にのみ、[!DNL Marketo Measure] JavaScriptによって作成されます
* 会議や見本市などのオフラインインタラクション：CRM キャンペーンメンバーシップ
* サイト以外のインターネット上のどこでも発生するデジタルインタラクション（リストのアップロードを生成するサードパーティサイトでホストされるウェビナーなど）: CRM キャンペーンメンバーシップ
* 営業部門とのインタラクション：CRM アクティビティレコード

CRM キャンペーン管理に慣れており、既存のプロセスを維持したい場合も、問題ありません。 CRM キャンペーン内のすべてのインタラクションを追跡し続けても、[!DNL Marketo Measure]に問題はありません。 タッチポイントの重複を避けるために、必要なキャンペーンサブセットからタッチポイントのみを作成するロジックを設計できます。

## 可視性とアトリビューションの違い {#visibility-vs-attribution}

フルサークルの設定のほとんどは、マーケティング施策やセールス施策において、顧客とのあらゆるやり取りを確認できます。 ページビュー、繰り返しページ訪問、3回続くキャンペーンへのメンバーシップ - Full Circleは、これらすべてを表示します。 ページを300回閲覧した場合、Full Circleは300件の重複キャンペーンを作成し、それぞれにメンバーシップを付与します。 [!DNL Marketo Measure]は使用していません。これは、私たちの設計上の意識的な決定です。

[!DNL Marketo Measure]は、有意義なインタラクションを明らかにし、最も影響力のある顧客接点に適切に重みを割り当てるアトリビューションストーリーを提供することを目的としています。 例えば、[!DNL Marketo Measure] フレームワークでは、日常的なタッチポイントとしてページビュー（フォーム入力なし）が表示されません。 スタンドアロンのページビューは、購入ジャーニーを前進させる上で影響を与える可能性は低いですが、指定されたCRM マイルストーン（リードや商談作成など）の前の最新のインタラクションである場合は、タッチポイントを作成します。 私たちはあなたにすべてを見せたくありません。 アトリビューションの観点から重要なものをお見せします。

[!DNL Marketo Measure]担当者と協力して、チームが利用できなくなるデータに関する適切な期待値を設定します。

## Pre-[!DNL Marketo Measure] データ {#pre-marketo-measure-data}

標準的な推奨事項は、[!DNL Marketo Measure] JavaScriptをデプロイした日からレポートとデータ収集を開始することです。これは、以前のFull Circleのお客様の場合は2倍になります。 上記の2つのセクションについて考えてみましょう。より多くのデータが表示されることに慣れており、CRM キャンペーンメンバーシップから取得されるすべてのデータに慣れています。 [!DNL Marketo Measure]導入前のデータの一部またはすべてを含める場合は、JavaScript導入日を通じてリンゴと比較することはありません。

ただし、多くの顧客がこの履歴データを必要としていることは確かに理解しています。特に、セールスサイクルが長い（90日を超える）場合は、[!DNL Marketo Measure]前のデータを[!DNL Marketo Measure]個のデータに可視化することをお勧めします。 これを[!DNL Marketo Measure]担当者と慎重に話し合い、実装日を調整すると、チャネルのパフォーマンスやエンゲージメントが改善または減少したり、その他の誤った推測が生じる可能性があることに常に注意してください。

## まとめ {#in-summary}

しかし当社は、多くの顧客がこうした変化に対応できるように支援してきました。 [!DNL Marketo Measure]担当者と協力して、上記の影響と、その他の懸念事項を理解してください。
