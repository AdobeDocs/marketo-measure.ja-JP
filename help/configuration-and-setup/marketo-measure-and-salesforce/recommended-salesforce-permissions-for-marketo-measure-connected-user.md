---
unique-page-id: 18874696
description: ' [!DNL Marketo Measure] 接続ユーザー –  [!DNL Marketo Measure]に対する推奨 [!DNL Salesforce] 権限'
title: ' [!DNL Marketo Measure] 接続ユーザーに推奨される [!DNL Salesforce] 権限'
exl-id: b74aa28b-4a7b-42d1-8df0-d1ae0ff1f338
feature: Salesforce
TQID: https://experienceleague.adobe.com/ImKgikcl5a3LJhBs8VnvWFZAxLkEY0r3Ip0XVZoHE-g
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 441
ht-degree: 27%

---

# [!DNL Marketo Measure]接続ユーザーに推奨される[!DNL Salesforce]権限 {#recommended-salesforce-permissions-for-marketo-measure-connected-user}

[!DNL Marketo Measure] は、接続された [!DNL Salesforce] ユーザーを通じて [!DNL Marketo Measure] アプリ内でデータを送受信します。

タッチポイントデータを[!DNL Salesforce] インスタンスにプッシュするには、接続されたユーザーが[!DNL Marketo Measure]個のカスタムオブジェクト（つまり、Buyer TouchpointとBuyer Attribution Touchpoint）と、リードや連絡先などの標準[!DNL Salesforce] オブジェクトにアクセスできる必要があります。 Salesforce](/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md)の[[!DNL Marketo Measure] を参照してください。

[!DNL Salesforce]管理者ユーザーライセンスは、デフォルトで必要なデータ権限を持つことが多いため、接続ユーザーとして機能できます。 ただし、統合ユーザーまたは専用の[!DNL Salesforce] ユーザーライセンスを使用して、[!DNL Marketo Measure]がインスタンスに与える影響を追跡することをお勧めします。

[!DNL Marketo Measure] データが正確に流れるように、次の権限をお勧めします：

* 専用ユーザーに対する[!DNL Marketo Measure]管理者の権限セット

管理された権限セットは、SFDC 管理者に、[!DNL Marketo Measure] オブジェクトからレコードを作成、読み取り、書き込み、削除する権限を付与します。

* 変換済みリードの表示と編集の権限セット

これにより、[!DNL Marketo Measure] は、リードが連絡先にコンバートされた後、リードを装飾できます。 この権限セットが有効でない場合、大幅なデータトラッキングギャップが生じる可能性があります。 詳細については、[[!DNL Salesforce Trailblazer]  コミュニティ ](https://help.salesforce.com/s/articleView?language=en_US&id=leads_view_edit_converted.htm&type=5)を参照してください。

* [!DNL Salesforce] マーケティングユーザーチェックボックス

「[!UICONTROL マーケティングユーザー]」チェックボックスを使用すると、ユーザーは、キャンペーンを作成したり、キャンペーンインポートウィザードを使用したりできます。 このオプションが選択されていない場合、そのユーザができるのは、キャンペーンおよび高度なキャンペーン設定の表示、単一のリードまたは取引先責任者のキャンペーン履歴の編集およびキャンペーンレポートの実行のみです。 [!DNL Marketo Measure] には、キャンペーンオブジェクトに対する読み取りおよび書き込み権限が必要です。

**追加のトラブルシューティング**

[!DNL Marketo Measure]でデータの読み取りまたは書き込み中に問題が発生している場合は、次の調査を行うと便利です。

* [!DNL Salesforce] キューへのアクセス

専用ユーザーがキュー内のリードにアクセスできない場合は、[!DNL Marketo Measure] データを使用してリードを変更できません。 これを実現するには、キューへのアクセスを許可する役割を階層内に持つか、ユーザーに個別にアクセス権を付与します。

* フィールドレベルのセキュリティとアクセシビリティ

フィールドレベルのセキュリティとフィールドアクセシビリティは関連していますが、いくつかの重要な違いがあります。 フィールドレベルのセキュリティは、特定のプロファイルに対するフィールドの表示を定義します。一方、フィールドアクセシビリティは、フィールドレベルのセキュリティとページレイアウト設定にもとづいて、フィールドを編集できるかどうかを決定します。 [!DNL Marketo Measure] パッケージの権限セットを使用すると、必要なフィールドオブジェクトのセキュリティ設定を受け取ることができます。 正しいフィールドアクセシビリティを使用するには、接続されたユーザーがページレイアウトに[!DNL Marketo Measure] フィールドを持つ必要がある場合があります。 レイアウトの[!DNL Marketo Measure] フィールドでは、[!DNL Marketo Measure] データを[!DNL Salesforce]にマッピングできます。 これは、特定の[!DNL Salesforce]環境によって異なります。

すべての組織の[!DNL Salesforce]には個別のニーズがありますが、[!DNL Marketo Measure] アクセスのニーズとセキュリティ プロトコルのバランスを取るための要件を提供しています。 [[!DNL Marketo Support]](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}さんに連絡することを躊躇しないでください。
