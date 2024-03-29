---
unique-page-id: 18874696
description: 推奨 [!DNL Salesforce] 権限： [!DNL Marketo Measure] 接続ユーザ — [!DNL Marketo Measure]
title: ' [!DNL Marketo Measure] 接続ユーザーに推奨される [!DNL Salesforce] 権限'
exl-id: b74aa28b-4a7b-42d1-8df0-d1ae0ff1f338
feature: Salesforce
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 14%

---

# 推奨 [!DNL Salesforce] 権限： [!DNL Marketo Measure] 接続ユーザ {#recommended-salesforce-permissions-for-marketo-measure-connected-user}

[!DNL Marketo Measure] は、接続された [!DNL Salesforce] ユーザーを通じて [!DNL Marketo Measure] アプリ内でデータを送受信します。

タッチポイントデータを [!DNL Salesforce] インスタンス、接続したユーザーは、 [!DNL Marketo Measure] カスタムオブジェクト（購入者のタッチポイントおよび購入者のアトリビューションのタッチポイント）および標準 [!DNL Salesforce] リードや連絡先などのオブジェクト。 詳しくは、 [[!DNL Marketo Measure] Salesforce 内](/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md).

[!DNL Salesforce] 管理者ユーザーライセンスは、通常はデフォルトで必要なデータ権限を持っているので、接続ユーザーとして使用できます。 ただし、チームは、統合ユーザーまたは専用の [!DNL Salesforce] の影響を追跡するためのユーザーライセンス [!DNL Marketo Measure] をインスタンスに追加します。

次の権限を使用して、 [!DNL Marketo Measure] データの正確なフロー：

* [!DNL Marketo Measure] 専用ユーザーの管理者権限セット

管理された権限セットは、SFDC 管理者に、[!DNL Marketo Measure] オブジェクトからレコードを作成、読み取り、書き込み、削除する権限を付与します。

* 変換済みリードの権限セットの表示と編集

これにより、[!DNL Marketo Measure] は、リードが連絡先にコンバートされた後、リードを装飾できます。この権限セットが有効になっていない場合、データトラッキングに大きなギャップが生じる可能性があります。 詳しくは、 [[!DNL Salesforce Trailblazer] コミュニティ](https://help.salesforce.com/s/articleView?language=en_US&amp;id=leads_view_edit_converted.htm&amp;type=5).

* [!DNL Salesforce] マーケティングユーザーチェックボックス

「[!UICONTROL マーケティングユーザー]」チェックボックスを使用すると、ユーザーは、キャンペーンを作成したり、キャンペーンインポートウィザードを使用したりできます。このオプションを選択しない場合、ユーザーはキャンペーンと高度なキャンペーン設定の表示、1 つのリードまたは連絡先に関するキャンペーン履歴の編集、キャンペーンレポートの実行のみを行うことができます。 [!DNL Marketo Measure] は、campaign オブジェクトに対して読み書きを行う機能が必要です。

**その他のトラブルシューティング**

次の場合 [!DNL Marketo Measure] は、まだデータの読み取りや書き込みで問題が発生しています。次の点を調べると役に立つ可能性があります。

* アクセス先 [!DNL Salesforce] キュー

専用ユーザーがキュー内のリードにアクセスできない場合、 [!DNL Marketo Measure] データ。 これを実現するには、キューへのアクセスを許可する階層内にロールを持つか、ユーザーに個別にアクセス権を付与します。

* フィールドレベルのセキュリティとアクセシビリティ

フィールドレベルのセキュリティとフィールドのアクセシビリティは関連していますが、いくつかの主な違いがあります。 フィールドレベルのセキュリティでは、特定のプロファイルのフィールドの表示を定義します。フィールドアクセシビリティでは、フィールドレベルのセキュリティとページレイアウトの設定に基づいてフィールドを編集可能にするかどうかを決定します。 の使用 [!DNL Marketo Measure] パッケージの権限セットには、必要なフィールドオブジェクトセキュリティ設定が含まれます。 場合によっては、正しいフィールドのアクセシビリティを得るために、接続しているユーザーが [!DNL Marketo Measure] フィールドをページレイアウトで使用できます。 [!DNL Marketo Measure] レイアウト上のフィールドで、 [!DNL Marketo Measure] マッピング先のデータ [!DNL Salesforce]. これは、お客様の特定の [!DNL Salesforce] 環境。

すべての組織の [!DNL Salesforce] 個々のニーズがありますが、バランスを取るための要件をお客様に提供します [!DNL Marketo Measure] セキュリティプロトコルを使用してアクセスニーズに対応します。 ～に手を差し伸べることを躊躇しないでください。 [[!DNL Marketo Support]](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.
