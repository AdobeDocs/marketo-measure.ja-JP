---
description: '''[!DNL Marketo Measure] 究極の実装ガイド — [!DNL Marketo Measure]  — 製品ドキュメント`'
title: '''[!DNL Marketo Measure] 究極の実装ガイド`'
hide: true
hidefromtoc: true
feature: Integration, Tracking, Attribution
source-git-commit: a1838bec06d1a626bb282f8e7d26814840f860a7
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 6%

---

# [!DNL Marketo Measure] 究極の実装ガイド {#marketo-measure-ultimate-implementation-guide}

導入文

## Ultimate と標準の階層を比較した場合の主な違い {#main-differences-when-using-ultimate-over-standard-tiers}

AEP を通じて B2B データをインポート：マーケターは、AEP を通じて B2B データ（アカウント、商談、連絡先、リード、キャンペーン、キャンペーンメンバー、アクティビティなど）を取り込む必要があります。 ほとんどすべてのデータソースだけでなく、同じタイプの複数のデータソースからも取り込み、すべてのデータをアトリビューションのために取り込みます。

* Salesforce や Dynamics だけでなく、ほとんどすべての CRM で使用できます。
* 複数の CRM インスタンスや MAP インスタンスを 1 つのMarketo Measureインスタンスに接続します。
* サードパーティのウェビナー登録および参加データを取り込みます。

直接の CRM 接続とMarketo Engage接続は、Ultimate では使用できなくなりました。

* Ultimate では、データは CRM にプッシュされません。 お客様は、Data Warehouse のデータを使用できます。
* マーケターは、引き続き、Marketo Measure JavaScript を使用した直接接続と追跡 Web アクティビティを通じて Ad Platform データを取り込みます。

Ultimate ユーザーは AEP でプロビジョニングされます。 既に AEP がある場合、新しいインスタンスは再プロビジョニングされません。

* プロビジョニングされた AEP バージョンには、すべてのソースコネクタ、スキーマデータモデリング、データセット、アドホッククエリサービス、Marketo Measure専用の宛先が含まれます。

詳細情報： [Marketo Measure Ultimate](/help/marketo-measure-ultimate/marketo-measure-ultimate-overview.md){target="_blank"}.

## スキーマとデータセット {#schemas-and-datasets}

>[!NOTE]
>
>チェックアウト [スキーマの構築ブロック](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#building-blocks-of-a-schema){target="_blank"} スキーマ、クラス、フィールドグループの概要。

**XDM スキーマ=クラス+スキーマフィールドグループ&#42;**

* 必須フィールドは変更できません。 必要に応じて、カスタムフィールドを作成して追加できます。
* 階層に基づくフィールド名の例： accountOrganization.annualRevenue.amount

&#42; _スキーマは、クラスと、0 個以上のスキーマフィールドグループで構成されます。 つまり、フィールドグループを使用せずにデータセットスキーマを作成できます。_

![](assets/marketo-measure-ultimate-implementation-guide-1.png)

[データセットの概要](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target="_blank"}:AEP に正常に取り込まれたすべてのデータは、データレイク内にデータセットとして保持されます。 データセットは、スキーマ（列）とフィールド（行）を含むテーブルなど、データの集まりのストレージと管理の構成体です。

## スキーマの作成 {#creating-a-schema}

10 個の標準 B2B スキーマを作成するには、自動生成ユーティリティを使用することをお勧めします。

* ユーティリティのダウンロードとセットアップの手順 [ここにあります](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces.html#set-up-b2b-namespaces-and-schema-auto-generation-utility){target="_blank"}.

を持つユーザーの場合、 _**CDP 権限**_：ソースページに移動してスキーマを作成します。

* ソースから、データを追加/テンプレートを使用を選択します。

![](assets/marketo-measure-ultimate-implementation-guide-2.png)

* 10 個の標準 B2B スキーマを作成するには、アカウントとすべての B2B テンプレートを選択します。

![](assets/marketo-measure-ultimate-implementation-guide-3.png)

## データフロー {#dataflows}

[データフローの概要](https://experienceleague.adobe.com/docs/experience-platform/dataflows/home.html){target="_blank"}

**データフローを作成する手順は次のとおりです。**

1. ソースを選択します。
1. 既存のアカウントを選択するか、アカウントを作成します。
1. 「ソース」からインポートする使用可能なタイプのリストからデータタイプを選択します。
1. 既存のデータセットを選択するか、新しいデータセットを作成します。
1. ソースのフィールドをスキーマにマッピングします。

   >[!NOTE]
   >
   >* 1 つのスキーマタイプを別の同一のスキーマタイプにマッピングすると、自動的に実行されます。
   >* また、システム内の別のフローからマッピングをインポートすることもできます。
   >* 1 つの「ソース」フィールドを複数の宛先フィールドにマッピングすることはできますが、逆はできません。
   >* 計算フィールドを作成できます（ExL: Data Prep マッピング関数）。

   >[!CAUTION]
   >
   >* データフローは編集できますが、マッピングが変更されてもデータはバックフィルされません。
   >* 必須フィールドが NULL の場合、フロー全体が拒否されます。

   >[!NOTE]
   >
   >[Marketo Measure Ultimate Data Integrity Requirement](/help/marketo-measure-ultimate/data-integrity-requirement.md){target="_blank"}

1. データの読み込みケイデンスを設定します。
1. 「確認して完了」をクリックします。
1. データフローステータスの測定 UI 設定の「アカウントステータス」ページを確認します。

**監視：**

データフローのステータスを確認するソース/データフローページ

* データセットのアクティビティの詳細を表示するには、データセットをクリックします。
* データフローエラーを表示するには、データフローを選択し、データフローの実行を選択して、「エラー診断のプレビュー」をクリックします。

## データ検査 {#data-inspection}

ExL: Marketo Measure Ultimate Data Integrity Requirement このドキュメントには、各 XDM の必須フィールドと検査クエリが含まれています。 ExL で公開されます。  — 上に既にタグ付けされています — 再度POSTします???

オプション 1:UI から直接クエリを実行するには、データ管理の「クエリ」タブにアクセスします。

![](assets/marketo-measure-ultimate-implementation-guide-4.png)

オプション 2: [PSQL をダウンロードして使用](https://experienceleague.adobe.com/docs/experience-platform/query/clients/psql.html){target="_blank"} （より高速で信頼性が高くなります）。

## Marketo Measureのデータセットをアクティブ化 {#activate-dataset-for-marketo-measure}

開始する前に、測定 UI 設定の「Experience Platform/サンドボックスマッピング」セクションに移動し、サンドボックスをマッピングします。

>[!CAUTION]
>
>選択した後は変更できません。

1. AEP で、「宛先/Marketo Measureページ」に移動して、データセットを書き出します。
1. 宛先を設定します。
1. データセットをアクティブ化します。
1. データフローステータスの測定 UI 設定の「アカウントステータス」ページを確認します。

>[!NOTE]
>
>* 特定のソースの特定のエンティティ（アカウントなど）のデータは、1 つのデータセットにのみ取り込むことができます。 各データセットは、1 つのデータフローにのみ含めることができます。違反すると、実行時にデータフローが停止します。
>* AEP で宛先全体を削除して、測定のデータを削除します。 無効にすると、新しいデータエクスポートが停止し、古いデータが保持されます。
>* 測定の設定はほとんど同じように見えますが、ステージマッピングなどの一部のパーツは異なります。
>* 新しいデータフローがフロー実行を生成するまでに数時間かかり、その後、定期的な 1 時間間隔で発生します。

測定では、デフォルトの通貨を「通貨」セクションで設定する必要があります

* 複数通貨を使用する場合、コンバージョンを読み取って使用するには、通貨換算レートスキーマを AEP に入力する必要があります。

**ステージマッピング：**

ユーザーデータからステージが自動的にインポートされるわけではないので、すべてのステージを手動でマッピングする必要があります。

* ユーザーは、様々なソースからステージをマッピングできます。

![](assets/marketo-measure-ultimate-implementation-guide-5.png)

ステージがマッピングされていない場合、データが処理される場所がないので、システムは機能しません。

**キャンペーンメンバールール：**

データセットを選択し、それぞれにルールを設定する必要がある。

**エクスペリエンスイベントルール：**

データセットを選択し、アクティビティのタイプを選択する必要があります。

* カスタムアクティビティは、まだサポートされていません。
* お客様に、利用可能なオプションに適合しないアクティビティがある場合は、それらを「注目のアクション」として分類し、カスタムフィールドを使用して区別することをお勧めします。

**オフラインチャネル：**

* データセット固有のチャネルマッピングルールは実行しないので、これはグローバルです。
* 最終的に CRM キャンペーンタイプとチャネルの両方を照合する必要がありますが、現時点では、回避策として両方のフィールドにチャネル名をマッピングできます。
* **チャネルルール：バックフィルしたデータには、ステージ遷移データは含まれません。**

タッチポイントとセグメントの設定は変わりません。
