---
description: セグメンテーションのベストプラクティス -  [!DNL Marketo Measure]
title: セグメンテーションのベストプラクティス
exl-id: 68281210-383b-4688-86e9-27fbdc1fabbb
feature: Segmentation
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: ht
source-wordcount: '450'
ht-degree: 100%

---

# セグメンテーションのベストプラクティス {#best-practices-for-segmentation}

## 概要 {#overview}

[!DNL Marketo Measure] セグメント化では、CRM フィールドに基づいてルール（基本的にはフィルター）を定義し、個々のセグメントにバケット化できます。これらのセグメントは、Discover ダッシュボードおよび [!DNL Salesforce] レポートで使用できるようになります。

セグメント化は、[!DNL Marketo Measure] アカウント、特に Discover ボード内での利用にとって重要です。[!DNL Marketo Measure] Discover ボードは事前に定義されたフィルターのセットに制限されているので、セグメント化により、[!DNL Salesforce] レポートの場合と同じように Discover でデータを分析できます。

[!DNL Salesforce] にプッシュされると、セグメント値は「セグメント」フィールドに書き込まれ、購入者のタッチポイントレポートタイプ内に含まれます。これにより、両方のプラットフォームにわたって均等なレポートが可能になります。セグメントは、任意のタッチポイントの「タッチポイントの詳細」でも見つけることができます。

[!UICONTROL Discover] にプッシュすると、セグメントはすべてのボードにあるフィルタードロップダウンメニュー内に使用可能なフィルターとして表示されます。

## ベストプラクティス {#best-practice}

初めてセグメント化を定義する場合でも、以前に確立されたセグメント化を単にレビューする場合でも、次のベストプラクティスに留意してください。

* 簡素化します。
* セグメント名を組織の命名法に合わせます。つまり、カテゴリ = フィルター名、セグメント = フィルター値です
* ルールでは数式フィールドを使用しないでください
* 可能な限り、リード／取引先責任者と商談の両方でセグメント化を作成し、ファネル全体で使用できるようにします
   * Marketo Measure Ultimate のお客様で、デフォルトのダッシュボードオブジェクトを取引先責任者として設定している場合は、リードに固有の以下の 2 つのフィールドを使用しないでください（[詳しくは、こちらを参照してください](/help/marketo-measure-ultimate/data-integrity-requirement.md){target="_blank"}）。
      * b2b.personStatus
      * b2b.isConverted
   * すべてのセグメントカテゴリがファネル全体で整列するわけではありません
      * 例えば、「商談タイプ」のセグメントカテゴリはリードと関係ありませんが、「地域」に関連するセグメントはファネル全体で定義できるカテゴリの可能性があります
* CRM 内にあるか BI ツール内にあるかに関わらず、現在データのスライス方法を考慮し、[!DNL Marketo Measure] のセグメントとして作成して、Discover で同じレポートを作成できるようにすることを検討してください

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

少なくとも年に 2 回セグメント化をレビューすると、セグメント化が最新の状態になります。ベストプラクティスとして、[!DNL Marketo Measure] アカウント設定の「[!UICONTROL セグメント]」タブ内でルールをレビューすると共に、[!DNL Salesforce] 内でレポートを取得して実際のセグメントをレビューすることをお勧めします。これらの手順は、ユーザーとチームがセグメント化と、[!DNL Marketo Measure] レポートに自信を持てるようにするのに役立ちます。

セグメント化のレビューをトリガーする可能性があるその他の理由としては、次のようなものがあります。

* マーケティングチームの入れ替わり
* セグメントの定義に使用するフィールドの変更
* 既に確立されているセグメントへの追加または変更

>[!MORELIKETHIS]
>
>[カスタムセグメント化の設定方法](/help/advanced-marketo-measure-features/segmentation/custom-segmentation.md)
