---
description: ' [!DNL Marketo Measure]  階層型サブスクリプションから  [!DNL Marketo Measure] Ultimateに移行する際の移行プロセスについて説明します。'
title: 層から  [!DNL Marketo Measure] Ultimateへの移行
feature: Integration, Tracking, Attribution
exl-id: 828c9bba-3835-484a-bd80-84b5a6b67e22
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 1%

---

# 階層 1～2 から [!DNL Marketo Measure] Ultimateへの移行 {#migration-from-tier-to-marketo-measure-ultimate}

この記事では、Tier 1 または 2 のサブスクリプションからUltimateへ移行するユーザーの移行プロセス [!DNL Marketo Measure] 概要を説明します。

>[!IMPORTANT]
>
>移行が完了するまで、既存の階層インスタンスを必ず保持してください。

## データ収集 {#data-collection}

### ウェブトラフィックデータ {#web-traffic-data}

* JavaScriptのデプロイメントに変更は必要ありません。

* 新しいUltimate インスタンスでドメインを有効にします。

* 必要に応じて、履歴 web データを移行および再処理するためのチケットを送信します。

* 広告の統合は変更されませんが、Ultimateで必ず再接続してください。 その前に、階層テナントの広告アカウントを切断していることを確認してください。

>[!NOTE]
>
>広告コストの履歴データはインポートされません。 広告アカウントが再接続された後に進む広告コストデータのみをインポートします。

### エンタープライズデータ接続 {#enterprise-data-connection}

CRM 接続やMarketo Engage接続など、AEPのすべてのソースデータ接続を再実装する。

## データ変換 {#data-transformation}

* リードとアカウントのマッチングおよび予測エンゲージメントスコアを含むAccount-Based Marketing機能は、Ultimateでは使用できません。

   * ただし、AEPからリードとアカウントのマッチング結果を読み込んで、プラットフォーム内で使用することはできます。

* Ultimateでは、直接 CRM 連携がないので、CRM の履歴ステージ遷移は直接読み取られるのではなく、推論されます。

   * 商談レコードとタイムスタンプを読み取って現在のステージを確認し、過去のステージを推測します。

## レポート {#reporting}

* Ultimateはデータを CRM にプッシュしません。

   * データを CRM にプッシュする場合は、カスタム ETL パイプラインを使用してMarketo Measure Snowflakeから CRM にデータを抽出します。 CRM でカスタムデータモデルを設定する必要があります。

* すべての Discover ダッシュボードは、アトリビューション AI ダッシュボードが追加された、階層型ソリューションと同じです。
