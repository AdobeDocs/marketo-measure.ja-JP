---
description: Marketo Measure ユーザー向け Connected User [!DNL Salesforce]  ガイダンスの推奨  [!DNL Marketo Measure]  権限
title: ' [!DNL Marketo Measure] 接続ユーザーに推奨される [!DNL Salesforce] 権限'
exl-id: b74aa28b-4a7b-42d1-8df0-d1ae0ff1f338
feature: Salesforce
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 23%

---

# 接続ユーザーの推奨 [!DNL Salesforce] 権限 [!DNL Marketo Measure] {#recommended-salesforce-permissions-for-marketo-measure-connected-user}

[!DNL Marketo Measure] は、接続された [!DNL Salesforce] ユーザーを通じて [!DNL Marketo Measure] アプリ内でデータを送受信します。

タッチポイントデータを [!DNL Salesforce] インスタンスにプッシュするには、接続ユーザーが、リードや連絡先などの標準 [!DNL Marketo Measure] オブジェクトだけでなく、[!DNL Salesforce] のカスタムオブジェクト（Buyer TouchpointやBuyer Attribution Touchpoint）へのアクセス権を持っている必要があります。 [[!DNL Marketo Measure] Salesforce内 &#x200B;](/help/configuration-and-setup/how-marketo-measure-and-salesforce-interact.md) を参照してください。

管理者ユーザーライセンス [!DNL Salesforce]、デフォルトで必要なデータ権限を持っていることが多いので、接続ユーザーとして機能できます。 ただし、チームがインスタンスに対する [!DNL Salesforce] の影響を追跡するために、統合ユーザーまたは専用の [!DNL Marketo Measure] ユーザーライセンスの使用をお勧めする場合があります。

データの正確なフローを確保するには、次 [!DNL Marketo Measure] 権限をお勧めします。

* 専用ユーザーの [!DNL Marketo Measure] 管理者アクセス権セット

管理された権限セットは、SFDC 管理者に、[!DNL Marketo Measure] オブジェクトからレコードを作成、読み取り、書き込み、削除する権限を付与します。

* コンバート済みリードの表示および編集権限セット

これにより、[!DNL Marketo Measure] は、リードが連絡先にコンバートされた後、リードを装飾できます。この権限セットが有効になっていない場合、データトラッキングに重大なギャップがある可能性があります。 詳しくは、[[!DNL Salesforce Trailblazer] community](https://help.salesforce.com/s/articleView?language=en_US&id=leads_view_edit_converted.htm&type=5) を参照してください。

* [!DNL Salesforce] マーケティングユーザーのチェックボックス

「[!UICONTROL マーケティングユーザー]」チェックボックスを使用すると、ユーザーは、キャンペーンを作成したり、キャンペーンインポートウィザードを使用したりできます。このオプションが選択されていない場合、そのユーザができるのは、キャンペーンおよび高度なキャンペーン設定の表示、単一のリードまたは取引先責任者のキャンペーン履歴の編集およびキャンペーンレポートの実行のみです。[!DNL Marketo Measure] には、キャンペーンオブジェクトに対する読み取りおよび書き込み権限が必要です。

**その他のトラブルシューティング**

[!DNL Marketo Measure] だデータの読み取りまたは書き込みに関する問題が発生している場合は、次の点を調査すると役に立つ場合があります。

* [!DNL Salesforce] キューへのアクセス

専用ユーザーがキュー内のリードにアクセスできない場合、[!DNL Marketo Measure] のデータを使用してリードを変更することはできません。 これを実現するには、キューへのアクセスを許可する役割を階層内に持つか、ユーザーにアクセス権を個別に付与します。

* フィールドレベルのセキュリティとアクセシビリティ

フィールドレベルのセキュリティとフィールドアクセシビリティには関連がありますが、いくつかの重要な違いがあります。 フィールドレベルのセキュリティは、特定のプロファイルのフィールドの表示を定義し、フィールドアクセシビリティは、フィールドレベルのセキュリティとページレイアウトの設定に基づいてフィールドが編集可能かどうかを決定します。 [!DNL Marketo Measure] パッケージの権限セットを使用して、必要なフィールドオブジェクトのセキュリティ設定を受け取ります。 場合によっては、接続されたユーザーが正しいフィールドのアクセシビリティを得るために、ページレイアウトに [!DNL Marketo Measure] のフィールドを持つ必要があります。 レイアウト上の [!DNL Marketo Measure] フィールドを使用すると、[!DNL Marketo Measure] データを [!DNL Salesforce] にマッピングできます。 これは、特定の [!DNL Salesforce] 環境によって異なります。

すべての組織の [!DNL Salesforce] には個別のニーズがありますが、アドビでは、[!DNL Marketo Measure] しいアクセスのニーズとセキュリティプロトコルのバランスを取るための要件を提供しています。 遠慮しないで [[!DNL Marketo Support]](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} に手を差し伸べてください。
