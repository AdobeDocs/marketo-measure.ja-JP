---
description: ' [!DNL Marketo Measure] 階層型サブスクリプションから [!DNL Marketo Measure] Ultimateに移行する際の移行プロセスについて説明します。'
title: 階層から [!DNL Marketo Measure] Ultimateへの移行
feature: Integration, Tracking, Attribution
exl-id: 828c9bba-3835-484a-bd80-84b5a6b67e22
TQID: https://experienceleague.adobe.com/Q-VV8-RWaGb-lk-vr3y9KK9SjTlsugPJ-N4HrSH5uxA
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
feature_v2: id: c8f57308-7e33-4e41-a385-b55041c78939
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 1%

---

# Tier 1-2から[!DNL Marketo Measure] Ultimateへの移行 {#migration-from-tier-to-marketo-measure-ultimate}

この記事では、Tier 1 サブスクリプションまたは2 サブスクリプションから[!DNL Marketo Measure] Ultimateに移行するユーザーの移行プロセスについて説明します。

>[!IMPORTANT]
>
>移行が完了するまで、既存の階層インスタンスを保持することを忘れないでください。

## データ収集 {#data-collection}

### Web トラフィックデータ {#web-traffic-data}

* JavaScriptのデプロイメントに変更は必要ありません。

* 新しいUltimate インスタンスでドメインを有効にします。

* 必要に応じて、チケットを送信して過去のweb データを移行および再処理します。

* 広告の統合機能は変更されませんが、Ultimateで再度接続することを忘れないでください。 その前に、Tier テナントの広告アカウントの接続を解除していることを確認してください。

>[!NOTE]
>
>過去の広告コストのデータはインポートされません。 広告アカウントが再接続された後にのみ、広告コストデータを読み込みます。

### エンタープライズデータ接続 {#enterprise-data-connection}

CRM接続やMarketo Engage接続を含む、あらゆるソースデータ接続をAEPに再実装します。

## データ変換 {#data-transformation}

* リードとアカウントのマッチングや予測エンゲージメントスコアなどのAccount-Based Marketing機能は、Ultimateでは利用できません。

   * ただし、AEPを通じてリードとアカウントの照合結果を読み込み、プラットフォーム内で使用することはできます。

* Ultimateでは、CRMとの直接の連携がないので、CRMの過去のステージの移行は、直接読み取るのではなく推測されます。

   * 商談レコードとタイムスタンプを読み取り、現在のステージを確認し、過去のステージを推測します。

## レポート {#reporting}

* UltimateがCRMにデータをプッシュしない。

   * CRMにデータをプッシュする場合は、Marketo Measure SnowflakeからCRMにデータを抽出するために、カスタム ETL パイプラインが必要です。 CRMでカスタムデータモデルを設定する必要があります。

* すべての「もっと知る」ダッシュボードは、アトリビューション AI ダッシュボードが追加され、階層化されたソリューションと同じままです。
