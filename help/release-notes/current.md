---
description: 最新のリリースノート -  [!DNL Marketo Measure]
title: 最新のリリースノート
exl-id: e93ff03e-ea21-41f4-abb8-32313ee74c0c
feature: Release Notes
source-git-commit: cbb2afd48c0e462768be0a7cfe56007ae285c492
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 71%

---

# リリースノート：2024年 {#release-notes-2024}

2024年リリースのすべての新機能と更新された機能については、以下を参照してください。

## 第 2 四半期リリース {#q2-release}

<p>

**サードパーティ cookie の段階的廃止に対応した Marketo Measure 機能の廃止**

プライバシーに関する懸念の高まりに対応して、サードパーティ cookie は段階的に廃止されており、Google Chrome の 2024年第 3 四半期の期限は、その終了を示しています。Marketo Measure では、サードパーティ cookie に依存する特定の機能、特に Google／DoubleClick インプレッション cookie に依存するクロスドメイントラッキングとビュースルーアトリビューションを廃止する予定です。この変更は、Marketo Measure の他の機能やファーストパーティ cookie の使用には影響しません。Google のタイムラインに従って、これらの機能は 6月1日（PT）までに廃止する予定ですが、この日付より前に収集したデータには引き続きアクセスできます。

* [Marketo Measure でのサードパーティ cookie の非推奨（廃止予定）への適応](https://nation.marketo.com/t5/employee-blogs/adapting-to-third-party-cookie-deprecation-in-marketo-measure/ba-p/345110){target="_blank"}
* [Marketo Measure の Cookie](/help/marketo-measure-tracking/setting-up-tracking/marketo-measure-cookies.md){target="_blank"}

**強化されたエラー処理の段階的なロールアウト**

エクスポートジョブのエラー処理の強化に関する段階的なロールアウトを導入します。まず、権限エラーのアプリ内パルス通知の即時通知を開始し、エラーが発生した時点でエクスポートジョブが一時停止する新しいアプローチに移行します。 この変更は、データの整合性と可視性を向上させ、ユーザに対してよりスムーズで信頼性の高いデータ管理プロセスを確保することを目的としています。スムーズな移行と運用の中断を最小限に抑えるために、アドビでは、次の 2 つのフェーズでこれらの変更を実装しています。

* パルス通知の即座提供：書き出しジョブ中の権限エラーについては、アプリ内パルス通知を受信します。これにより、書き出しが中断されることはありませんが、現在のジョブに影響を与えることなくエラーについて学ぶのに役立ちます。
* 4 月 25 日のジョブ一時停止の実装： **延期** -Marketo Measureをご利用のお客様からの声を踏まえ、当初 4 月 25 日を予定していた失敗時の対応を延期することといたしました。 我々は，雇用の停止が最も効果的なアプローチではないかもしれないと認識する。 データの整合性を維持し、中断を最小限に抑える、より優れたソリューションの発見に取り組んでいます。 ユーザーのニーズにより適したソリューションを提供できるようになるまで、現在のシステムの変更を延期します。

_これが重要な理由_

データの整合性の強化と統合の将来性の確保：データの損失を防ぎ、正確性を確保するために、問題の最初の兆候が見られた時点でジョブを停止します。これにより、問題を迅速に解決でき、データ書き出しの品質とシステムの信頼性が向上します。

即時表示：パルス通知の導入により、権限エラーへの迅速な対応が可能になり、運用への潜在的な影響を防ぐことができます。

_移行のサポート_

この変更に適応するために、アドビでは、エラーの明確な説明と包括的なトラブルシューティング手順を記載した[ドキュメントを作成しました](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"}。

<br>

**LinkedIn 統合に必要なアクション**

LinkedIn は最近、Lead Sync API の更新バージョンをリリースしました。中断を避けるために、Marketo Measure インスタンスの LinkedIn 接続を 5月20日（PT）までに再認証してください。

