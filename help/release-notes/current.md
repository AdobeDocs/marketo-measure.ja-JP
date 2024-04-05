---
description: 最新のリリースノート — [!DNL Marketo Measure]
title: 最新のリリースノート
exl-id: e93ff03e-ea21-41f4-abb8-32313ee74c0c
feature: Release Notes
source-git-commit: 81ce4ead229e461eeb9e6e3b1e951108b627a4e8
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 1%

---

# リリースノート：2024年 {#release-notes-2024}

2024 年リリースのすべての新機能および更新された機能については、以下を参照してください。

## 第 2 四半期リリース {#q2-release}

<p>

**サードパーティ Cookie のフェーズアウトに対するMarketo Measure機能の廃止**

プライバシーに関する懸念の高まりに対応して、サードパーティ cookie は廃止され、Google Chrome の 2024 年第 3 四半期の期限が終了を告げています。 Marketo Measureは、Google/DoubleClick のインプレッション Cookie に依存する、サードパーティ Cookie、特にクロスドメイントラッキングとビュースルーアトリビューションに依存する特定の機能を廃止します。 この変更は、他のMarketo Measure機能やファーストパーティ cookie の使用には影響しません。 Googleのタイムラインに従い、これらの機能は 6 月 1 日までに廃止される予定ですが、この日より前に収集されたデータは、引き続きお客様がアクセスできます。

* [Marketo Measureでのサードパーティ Cookie の廃止の適応](https://nation.marketo.com/t5/employee-blogs/adapting-to-third-party-cookie-deprecation-in-marketo-measure/ba-p/345110){target="_blank"}
* [Marketo Measureの Cookie](/help/marketo-measure-tracking/setting-up-tracking/marketo-measure-cookies.md){target="_blank"}

**拡張されたエラー処理の段階的な展開**

4 月 25 日に、アプリ内での権限エラーのパルス通知を即座に開始し、エクスポートジョブがエラー発生時に一時停止する新しいアプローチに移行する、エクスポートジョブの拡張エラー処理の段階的なロールアウトを導入します。 この変更は、データの整合性と可視性を向上させ、よりスムーズで信頼性の高いデータ管理プロセスをユーザーに提供することを目的としています。 移行をスムーズに進め、操作の中断を最小限に抑えるため、アドビでは、次の 2 つの段階で変更を実装しています。

* Pulse Notifications の即時使用可能：書き出しジョブ中に権限エラーが発生した場合は、アプリ内パルス通知が送信されます。 これにより、エクスポートが中断されることはありませんが、現在のジョブに影響を与えることなく、エラーに関する情報を得るのに役立ちます。
* 4 月 25 日のジョブ一時停止の実装：4 月 25 日以降、書き出しジョブ中に権限エラーが発生した場合は、データがスキップされないようにジョブが一時停止されます。 問題が発生した場合は通知され、権限が修正されると、書き出しジョブは中断した場所からシームレスに再開されます。

_これが重要な理由_

データの整合性と将来の検証の強化統合：データの損失を防ぎ、正確性を確保するために、問題が発生した最初の段階でジョブを停止します。 これにより、迅速な問題解決が可能になり、データ書き出しの品質とシステムの信頼性が向上します。

即時表示：パルス通知を導入すると、権限エラーに対する迅速な応答が可能になり、操作に対する潜在的な影響を防ぐことができます。

_移行のサポート_

この変更に対応するために、 [ドキュメントを作成しました](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"} 明確なエラーの説明と包括的なトラブルシューティング手順を含む

**linkedIn統合に必要なアクション**

LinkedInは最近、リード同期 API の更新バージョンをリリースしました。 中断を回避するため、5 月 20 日までにMarketo MeasureインスタンスのLinkedIn接続を再認証してください。

