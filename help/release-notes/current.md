---
description: 最新のリリースノート - [!DNL Marketo Measure]
title: 最新のリリースノート
exl-id: e93ff03e-ea21-41f4-abb8-32313ee74c0c
feature: Release Notes
source-git-commit: db71cbfaf7deb5b724ac4babc38e835c04fadac7
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 1%

---

# リリースノート：2024年 {#release-notes-2024}

2024 年のリリースの新機能と更新された機能については、以下を参照してください。

## 第 2 四半期リリース {#q2-release}

<p>

**サードパーティ Cookie の廃止に対応したMarketo Measure機能の廃止**

プライバシーに関する懸念の高まりに対応して、サードパーティ cookie は段階的に廃止されつつあり、Google Chrome の 2024 年第 3 四半期の期限が終了を示しています。 Marketo Measureでは、サードパーティ cookie に依存する特定の機能、特にGoogle/DoubleClick インプレッション cookie に依存するクロスドメイントラッキングとビュースルーアトリビューションは非推奨（廃止予定）になります。 この変更は、他のMarketo Measure機能やファーストパーティ cookie の使用には影響しません。 Googleのタイムラインに従い、これらの機能は 6 月 1 日までに廃止される予定ですが、この日付より前に収集されたデータには引き続きご利用いただけます。

* [Marketo Measureでのサードパーティ Cookie の非推奨（廃止予定）への対応](https://nation.marketo.com/t5/employee-blogs/adapting-to-third-party-cookie-deprecation-in-marketo-measure/ba-p/345110){target="_blank"}
* [Marketo Measureの cookie](/help/marketo-measure-tracking/setting-up-tracking/marketo-measure-cookies.md){target="_blank"}

**強化されたエラー処理の段階的なロールアウト**

アドビでは、書き出しジョブのエラー処理を強化する段階的なロールアウトを導入しています。まず、権限エラーのアプリ内パルス通知の即時通知から始め、4 月 25 日（PT）に、書き出しジョブがエラー時に一時停止する新しいアプローチに移行します。 この変更は、データの整合性と可視性を向上させ、ユーザーに対してよりスムーズで信頼性の高いデータ管理プロセスを確保することを目的としています。 スムーズな移行と運用の中断の最小化を実現するために、アドビでは、次の 2 つのフェーズでこれらの変更を実装しています。

* Pulse 通知の即時の利用：エクスポートジョブ中に権限エラーが発生した場合、アプリ内のパルス通知が届きます。 これにより、書き出しが中断されることはありませんが、現在のジョブに影響を与えずにエラーを学ぶことができます。
* 4 月 25 日のジョブ一時停止の実装：4 月 25 日（PT）以降、エクスポートジョブ中に権限エラーが発生した場合は、データがスキップされないように、ジョブを一時停止します。 問題が発生すると通知され、権限が修正されると、書き出しジョブは中断した場所からシームレスに再開されます。

_これが重要な理由_

データの整合性の強化と統合の将来性の保証：データの損失を防ぎ、正確性を確保するために、トラブルの最初の兆候でジョブを停止します。 これにより、問題を迅速に解決し、データ書き出しの品質とシステムの信頼性を向上させることができます。

即時表示：パルス通知を導入すると、権限エラーに対して迅速に応答し、操作への影響を防ぐことができます。

_移行のサポート_

この変更に適応するには、 [ドキュメントが作成されました](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"} 明確なエラーの説明と包括的なトラブルシューティング手順が記載されています。

<br>
**LinkedIn連携に必要な対応**

LinkedInは最近、Lead Sync API の更新バージョンをリリースしました。 中断を避けるために、5 月 20 日（PT）までにMarketo Measure インスタンスでLinkedIn接続を再認証してください。

