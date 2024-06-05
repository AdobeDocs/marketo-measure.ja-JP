---
description: 最新のリリースノート -  [!DNL Marketo Measure]
title: 最新のリリースノート
exl-id: e93ff03e-ea21-41f4-abb8-32313ee74c0c
feature: Release Notes
source-git-commit: 97a82ae0649ae5b1349d025a7a7cf433bc64bc7e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 57%

---

# リリースノート：2024年 {#release-notes-2024}

2024年リリースのすべての新機能と更新された機能については、以下を参照してください。

## 第 3 四半期リリース {#q3-release}

<p>

**リマインダー：Salesforce フィールドの非推奨（廃止予定） - 6 月 14 日（Pt）**

昨年お知らせしたとおり、当社は、統合を簡素化し、Salesforce 標準オブジェクトにエクスポートする必要性を排除するために、リード/連絡先オブジェクトへのエクスポートジョブを段階的に廃止します。 次の手順に従って、タッチポイントオブジェクトから同じデータを取得できます [ここに記載されています](/help/release-notes/previous-releases/2023.md#deprecations){target="_blank"}. また、このデータをリード/連絡先オブジェクトに追加するワークフローの作成に関するドキュメントも共有します。 2024 年 6 月 14 日（PT）に廃止予定が発効します。

この変更により、次の 2 つの主なメリットが得られます。

* **Salesforce API コストの削減**：お客様は、Salesforce API のコストを約 10% 削減できると期待できます。
* **統合の効率化**：エクスポートジョブでのエラーの最大数は、これらのプロセスに関連しています。 これらを削除すると、統合が大幅に効率化されます。

**起因する商談ダッシュボード**

新しいを紹介できるのを楽しみにしています [起因する商談ダッシュボード](/help/marketo-measure-discover-ui/dashboards/attributed-opportunity-dashboard.md){target="_blank"}は、マーケティング活動が新興のパイプライン機会と成熟したパイプライン機会の両方にどのように貢献するかを包括的に把握できるように設計されています。 このダッシュボードを使用すると、戦略に起因するオープンな商談とクローズされた商談の詳細を掘り下げて、商談ステージでフィルタリングできる柔軟性を備えています。 アトリビューションされた商談額の観点で最も高くランクされたチャネル、サブチャネルまたはキャンペーンに関するインサイトが提供され、アトリビューションされた商談額の合計と、アトリビューションされたオープンおよびクローズされた商談の数が表示されます。

**Marketo Measure Ultimate のMarketo Engage Cookie 同期**

Marketo Measure Ultimate でMarketo Engage Cookie 同期が使用できるようになりました。 この機能を使用するには：

1. AEP スキーマページで、B2B ユーザースキーマを編集し、フィールドグループに「Marketo Engageユーザーの詳細」を追加します。
1. データを MMU に取り込む際には、フィールドグループの Cookie ID フィールドをMarketo Engageの Cookies フィールドにマッピングします。

**階層 2 のお客様に対して有効なブーメランステージ**

以前は Tier 3 のお客様のみが利用できましたが、Boomerang Stage 機能は、2024 年 6 月 13 日（PT）以降、Tier 2 のすべてのお客様も利用できるようになります。 この機能について詳しくは、以下のドキュメントを参照してください。

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

