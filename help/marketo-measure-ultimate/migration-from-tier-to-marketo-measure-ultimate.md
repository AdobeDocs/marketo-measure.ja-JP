---
description: ' [!DNL Marketo Measure]  階層型サブスクリプションから  [!DNL Marketo Measure] Ultimate に移行する際の移行プロセスについて説明します。'
hide: true
hidefromtoc: true
title: 階層から Ultimate へ  [!DNL Marketo Measure]  移行
feature: Integration, Tracking, Attribution
source-git-commit: 0c94276bec390bb67dafe5dd679c1a0378a05c85
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# 階層 1～2 から [!DNL Marketo Measure] Ultimate への移行 {#migration-from-tier-to-marketo-measure-ultimate}

この記事では、Tier 1 または 2 のサブスクリプションからMarketo Measure Ultimate へ移行するユーザーの移行プロセスについて説明します。

>[!IMPORTANT]
>
>移行が完了するまで、既存の階層インスタンスを必ず保持してください。

## データ収集 {#data-collection}

### ウェブトラフィックデータ {#web-traffic-data}

* JavaScriptのデプロイメントに変更は必要ありません。

* 新しい Ultimate インスタンスでドメインを有効にします。

* 必要に応じて、履歴 web データを移行および再処理するためのチケットを送信します。

* 広告の統合は変わりませんが、Ultimate で再接続することを忘れないでください。 その前に、階層テナントの広告アカウントを切断していることを確認してください。

>[!NOTE]
>
>広告コストの履歴データはインポートされません。 広告アカウントが再接続された後に進む広告コストデータのみをインポートします。

### エンタープライズデータ接続 {#enterprise-data-connection}

CRM 接続やMarketo Engage接続を含め、AEP のすべてのソースデータ接続を再実装する。

## データ変換 {#data-transformation}

* リードとアカウントのマッチングおよび予測エンゲージメントスコアを含むAccount-Based Marketing機能は、Ultimate では使用できません。

   * ただし、AEP からリードとアカウントのマッチング結果を読み込んで、プラットフォーム内で使用することはできます。

* 直接の CRM 接続がないので、Ultimate では、CRM の過去のステージ遷移が、直接読み取られるのではなく推論されます。

   * 商談レコードとタイムスタンプを読み取って現在のステージを確認し、過去のステージを推測します。

## レポート {#reporting}

* Ultimate はデータを CRM にプッシュしません。

   * データを CRM にプッシュする場合は、カスタム ETL パイプラインを使用してMarketo Measure Snowflakeから CRM にデータを抽出します。 CRM でカスタムデータモデルを設定する必要があります。

* Attribution AIすべての Discover ダッシュボードは、データダッシュボードが追加された、階層型ソリューションと同じです。
