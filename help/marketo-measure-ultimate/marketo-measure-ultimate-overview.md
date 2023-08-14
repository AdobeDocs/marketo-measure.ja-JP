---
description: '''[!DNL Marketo Measure] Ultimate の概要 — [!DNL Marketo Measure]  — 製品ドキュメント`'
title: '[!DNL Marketo Measure] Ultimate の概要'
exl-id: fada9479-0671-4698-8043-c67d7977577b
feature: Integration, Tracking, Attribution
source-git-commit: a2a7657e8377fd5c556d38f6eb815e39d2b8d15e
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 2%

---

# [!DNL Marketo Measure] Ultimate の概要 {#marketo-measure-ultimate-overview}

[!DNL Marketo Measure] （以前の Bizible）は、マーケターに、売上高の促進と、会社の投資回収率の最大化に最も効果的なマーケティング活動に関するインサイトを提供します。 [!DNL Marketo Measure] は、チャネルパフォーマンスを自動的に追跡およびレポートするマーケティングアトリビューションソリューションで、どのチャネルが最も顧客エンゲージメントに貢献しているかを明確に示し、それに応じてマーケティング費用を最適化できます。

[!DNL Marketo Measure Ultimate] には、次のその他の機能が含まれています。

* ほとんどのデータソースと同じタイプの複数のデータソースから取り込み、すべてのデータを取り込んで属性を設定します。
   * Salesforce や Dynamics だけでなく、ほとんどすべての CRM で使用できます。
   * 複数の CRM インスタンスや MAP インスタンスを 1 つに接続 [!DNL Marketo Measure] インスタンス。
   * サードパーティのウェビナー登録および参加データを取り込む。

* フィールドマッピングと変換機能を使用して、データを柔軟に変換し、適切なデータ形状を確保します。

* 含まれる Data Warehouse を通じて外部アプリケーションでアトリビューションインサイトを利用できるようにし、インサイトをワークフローに統合します。 より詳細な結果データおよび BI ベースのレポート ( 詳細な結果データへのアクセスを提供し、分析とレポートに任意の BI ツールを使用する機能を提供するSnowflakeData Warehouseを含む )。

* RTCDP（B2B または B2P エディション）との統合により、RTCDP のお客様向けに統合された B2B アトリビューションソリューションを RTCDP および [!DNL Marketo Measure] 両方とも、一元化されたAdobe Experience Platform(AEP) データから機能します。

**[!DNL Marketo Measure]階層 1 ～ 3**

![](assets/marketo-measure-ultimate-overview-1.png)

**[!DNL Marketo Measure Ultimate]**

![](assets/marketo-measure-ultimate-overview-2.png)

## の新機能 [!DNL Marketo Measure Ultimate] {#whats-new-in-marketo-measure-ultimate}

**AEP を通じて B2B データを読み込む**

マーケターは、AEP を通じて B2B データ（アカウント、商談、連絡先、リード、キャンペーン、キャンペーンメンバー、アクティビティなど）を取り込む必要があります。 直接の CRM 接続とMarketo Engage接続は、Ultimate では使用できなくなりました。 マーケターは、引き続き、を通じた直接接続と Web アクティビティの追跡を通じて Ad Platform データを取り込みます。 [!DNL Marketo Measure] javascript.

![](assets/marketo-measure-ultimate-overview-3.png)

**デフォルトの通貨設定**

[!DNL Marketo Measure Ultimate] は、ユーザーが変更するまで、デフォルトの通貨を USD に設定します。 新しいデフォルト通貨を設定すると、再処理せずにデータが更新されます。 選択した通貨がターゲットの ISO コードとして存在する限り、コンバージョン率を送信する必要はありません。

![](assets/marketo-measure-ultimate-overview-4.png)

**[!DNL Marketo Measure Ultimate]Sandbox**

[!DNL Marketo Measure Ultimate] インスタンスを作成する前に、AEP サンドボックスにマッピングする必要があります [!DNL Marketo Measure] 宛先データフロー（AEP 内）

>[!NOTE]
>
>A [!DNL Marketo Measure Ultimate] 実稼動インスタンスは、AEP 実稼動サンドボックス ( [!DNL Marketo Measure Ultimate] 開発者インスタンスは、AEP 開発者サンドボックスにマッピングする必要があります。

サンドボックスマッピングの選択が保存されると、現時点ではアプリケーション内で変更できなくなります。 変更するには、次の場所にアクセスしてください： [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.

特定のデータソースの特定のエンティティ（アカウントなど）のデータは、1 つのデータセットにのみ取り込むことができます。 各データセットは 1 つのデータフローにのみ含めることができます。 違反は、実行時にデータフローを停止します。

![](assets/marketo-measure-ultimate-overview-5.png)

**ステージマッピング**

すべて [!DNL Marketo Measure Ultimate] ルールは、データセットに固有です。 ステージマッピングルールは、すべてのデータセットと選択したすべてのステージに対して作成する必要があります。

次の 6 つの組み込みステージがあります。

* 失われたリード
* リードオープン
* 変換済みリード
* 失われた商談
* 商談のオープン
* 成立した商談

「損失」、「獲得」および「コンバート済み」の各セクションでは、カスタムステージを使用できません。 ただし、マッピングルールを更新することで、ソースデータを組み込みの失注/獲得/変換済みステージにマッピングできます。

カスタムステージは、オープンセクションに対してのみ定義できます。
ステージマッピングに CRM ステージが自動的に含まれなくなりました。

次の 4 つの組み込みステージをルールと共にマッピングする必要があります ( 他の 2 つのリードのマッピングルール（「失われたリード」と「変換されたリード」はオプション）。

* リードオープン
* 失われた商談
* 商談のオープン
* 成立した商談

ルール条件は、データセット固有です。 ステージマッピングルールは、リード損失およびリードコンバートを除くすべてのデータセットとすべてのステージに対して作成する必要があります。

ファネルとブーメラン、カスタムモデルの選択はありません。 ファネル、ブーメラン、カスタムモデルでは、すべてのステージが選択されます。 サポートするステージの数には制限があります。15 個のカスタムと 6 個のビルトインステージです。

![](assets/marketo-measure-ultimate-overview-6.png)

キャンペーンメンバーのタッチポイントルールとアクティビティのタッチポイントルールは、データセットに固有です。

![](assets/marketo-measure-ultimate-overview-7.png)

![](assets/marketo-measure-ultimate-overview-8.png)

Ultimate には直接の CRM 接続がないので、属性タッチポイントは CRM に書き込まれません。

[!DNL Marketo Measure] ABM ML サービス（リード — アカウントマッチングと予測エンゲージメントスコア）は、 [!DNL Marketo Measure Ultimate]. RT-CDP B2B エディションには、このようなサービスが無料で含まれています。

## 制限事項 {#limitations}

* 現時点では、データ変換ルールで使用できるフィールドは限られています。
* 既存の Tier 1/2/3ユーザーには移行パスはありません。 新しい実装が必要ですが、アドビは追跡対象の Web アクティビティデータを既存のインスタンスから移行する際に役立ちます。

>[!MORELIKETHIS]
>
>[Marketo Measure Ultimate Destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/adobe/marketo-measure-ultimate.html?lang=en){target="_blank"}
