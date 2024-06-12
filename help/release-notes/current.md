---
description: 最新のリリースノート -  [!DNL Marketo Measure]
title: 最新のリリースノート
exl-id: e93ff03e-ea21-41f4-abb8-32313ee74c0c
feature: Release Notes
source-git-commit: 97a82ae0649ae5b1349d025a7a7cf433bc64bc7e
workflow-type: ht
source-wordcount: '792'
ht-degree: 100%

---

# リリースノート：2024年 {#release-notes-2024}

2024年リリースのすべての新機能と更新された機能については、以下を参照してください。

## 第 3 四半期リリース {#q3-release}

<p>

**リマインダー：Salesforce フィールドの廃止予定 - 6月14日（PT）**

昨年発表したように、アドビでは統合を簡素化し、Salesforce 標準オブジェクトに書き出す必要性をなくすために、リード／取引先責任者オブジェクトへの書き出しジョブを段階的に廃止する予定です。[ここに記載されている](/help/release-notes/previous-releases/2023.md#deprecations){target="_blank"}手順に従って、タッチポイントオブジェクトから同じデータを取得できます。また、このデータをリード/取引先責任者オブジェクトに追加するワークフローの作成に関するドキュメントも共有します。2024年6月14日（PT）にこの廃止が実施されます。

この変更により、次の 2 つの主なメリットが得られます。

* **Salesforce API コストの削減**：お客様は、Salesforce API コストの約 10％の削減を期待できます。
* **統合の効率化**：書き出しジョブでのエラーの最大数は、これらのプロセスに関連しています。これらをなくすことで、統合が大幅に効率化されます。

**起因する商談ダッシュボード**

新しい[起因する商談ダッシュボード](/help/marketo-measure-discover-ui/dashboards/attributed-opportunity-dashboard.md){target="_blank"}を導入できることを嬉しく思います。このダッシュボードは、マーケティング活動が初期と成熟期のパイプラインの機会の両方にどのように貢献するかの全体像を把握できるように設計されています。このダッシュボードでは、戦略に起因するすべてのオープンな商談とクローズされた商談の詳細を掘り下げて、商談ステージごとに柔軟にフィルタリングできます。ここでは、起因する商談額の観点で最も高くランクされたチャネル、サブチャネルまたはキャンペーンに関するインサイトが提供され、起因する商談額の合計と、起因するオープンな商談およびクローズされた商談の数が表示されます。

**Marketo Measure Ultimate の Marketo Engage cookie 同期**

Marketo Measure Ultimate で Marketo Engage cookie 同期を使用できるようになりました。この機能を使用するには：

1. AEP スキーマページで、B2B ユーザスキーマを編集し、フィールドグループ「Marketo Engage ユーザの詳細」を追加します。
1. データを MMU に取り込む際には、フィールドグループの cookie ID フィールドを Marketo Engage の cookie フィールドにマッピングします。

**階層 2 のお客様向けに有効なブーメランステージ**

以前は階層 3 のお客様のみが利用可能であったブーメランステージ機能は、2024年6月13日（PT）以降、階層 2 のすべてのお客様も利用できるようになります。この機能について詳しくは、以下のドキュメントを参照してください。

* [ブーメランステージとタッチポイント](/help/advanced-marketo-measure-features/boomerang/boomerang-stages-and-touchpoints.md){target="_blank"}
* [ブーメランステージの設定](/help/advanced-marketo-measure-features/boomerang/setting-up-boomerang-stages.md){target="_blank"}
* [ブーメランステージのシナリオ](/help/advanced-marketo-measure-features/boomerang/boomerang-stage-scenarios.md){target="_blank"}

<p>

## 第 2 四半期リリース {#q2-release}

<p>

**サードパーティ cookie の段階的廃止に対応した Marketo Measure 機能の廃止**

プライバシーに関する懸念の高まりに対応して、サードパーティ cookie は段階的に廃止されており、Google Chrome の 2024年第 3 四半期の期限は、その終了を示しています。Marketo Measure では、サードパーティ cookie に依存する特定の機能、特に Google／DoubleClick インプレッション cookie に依存するクロスドメイントラッキングとビュースルーアトリビューションを廃止する予定です。この変更は、Marketo Measure の他の機能やファーストパーティ cookie の使用には影響しません。Google のタイムラインに従って、これらの機能は 6月1日（PT）までに廃止する予定ですが、この日付より前に収集したデータには引き続きアクセスできます。

* [Marketo Measure でのサードパーティ cookie の非推奨（廃止予定）への適応](https://nation.marketo.com/t5/employee-blogs/adapting-to-third-party-cookie-deprecation-in-marketo-measure/ba-p/345110){target="_blank"}
* [Marketo Measure の Cookie](/help/marketo-measure-tracking/setting-up-tracking/marketo-measure-cookies.md){target="_blank"}

**強化されたエラー処理の段階的なロールアウト**

アドビでは、書き出しジョブの強化されたエラー処理の段階的なロールアウトを導入しています。まず、権限エラーに対するアプリ内パルス通知の即時提供から始め、エラーの時点で書き出しジョブが一時停止する新しいアプローチに移行します。この変更は、データの整合性と可視性を向上させ、ユーザに対してよりスムーズで信頼性の高いデータ管理プロセスを確保することを目的としています。スムーズな移行と運用の中断を最小限に抑えるために、アドビでは、次の 2 つのフェーズでこれらの変更を実装しています。

* パルス通知の即座提供：書き出しジョブ中の権限エラーについては、アプリ内パルス通知を受信します。これにより、書き出しが中断されることはありませんが、現在のジョブに影響を与えることなくエラーについて学ぶのに役立ちます。
* 4月25日（PT）のジョブ一時停止の実装：**延期** - Marketo Measure ユーザからのフィードバックを考慮した結果、当初 4月25日（PT）に予定されていたエラー時点での書き出しジョブの一時停止の実装を延期することを決定しました。アドビでは、ジョブの停止が最も効果的なアプローチではない可能性があることを認識しています。データの整合性を維持し、中断を最小限に抑える、より優れたソリューションを見つけることに全力で取り組んでいます。ユーザのニーズにより密接に一致するソリューションを確実に提供できるまで、現在のシステムへの変更は保留します。

_これが重要な理由_

データの整合性の強化と統合の将来性の確保：データの損失を防ぎ、正確性を確保するために、問題の最初の兆候が見られた時点でジョブを停止します。これにより、問題を迅速に解決でき、データ書き出しの品質とシステムの信頼性が向上します。

即時表示：パルス通知の導入により、権限エラーへの迅速な対応が可能になり、運用への潜在的な影響を防ぐことができます。

_移行のサポート_

この変更に適応するために、アドビでは、エラーの明確な説明と包括的なトラブルシューティング手順を記載した[ドキュメントを作成しました](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"}。

<br>

**LinkedIn 統合に必要なアクション**

LinkedIn は最近、Lead Sync API の更新バージョンをリリースしました。中断を避けるために、Marketo Measure インスタンスの LinkedIn 接続を 5月20日（PT）までに再認証してください。

