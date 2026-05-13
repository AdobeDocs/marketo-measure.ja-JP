---
unique-page-id: 18874765
description: Salesforce サンドボックスとのMarketo Measure統合のテスト - [!DNL Marketo Measure]
title: Salesforce サンドボックスでのMarketo Measure統合のテスト
exl-id: df40b000-4572-46df-aef5-8f690ca8ed7a
feature: Salesforce
TQID: https://experienceleague.adobe.com/Es3alliU-EbPfMFY6gOybcr12HGgKVHyu97r7ZfRPFA
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 362
ht-degree: 9%

---

# Salesforce サンドボックスでのMarketo Measure統合のテスト {#testing-the-marketo-measure-integration-with-a-salesforce-sandbox}

>[!NOTE]
>
>ドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には引き続き「Bizible」と表示されます。 アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

[!DNL Marketo Measure]の主な機能の1つは、web サイト上のアクションを通じてデジタルマーケティング活動を追跡し、そのデータをリードと連絡先を通じて本番環境[!DNL Salesforce org]にプッシュする機能です。 ただし、通常、Sandbox統合内ではweb サイトから作成されたインバウンドリードはないため、データに注目するのは純粋にオフラインの観点からとなります。

テストの両方のフェーズで参照される2つのソースを次に示します。 [手順1 ～ 4](https://help.salesforce.com/s/articleView?id=lead_import_wizard.htm&language=en_US&type=5)および[手順5 ～ 6](/help/channel-tracking-and-setup/offline-channels/legacy-processes/syncing-offline-campaigns.md)。 これらのドキュメントは、一部の分野でより詳細に説明されているため、確認することをお勧めします。

1. キャンペーンにアップロードできるように、CSVにいくつかのリードを作成する必要があります。 これを行うには、実稼動Salesforceのレポートを通じて一部のリードを書き出します。 それ以外の場合は、Excel ファイルでリードを手動で作成し、インポート用にCSVとして保存できます。 レコードは約20枚しか必要ありません。 ファイルには次の列が必要です。

   1. メール
   1. 会社
   1. 名前（姓）
   1. 名（オプションですが推奨）

1. サンドボックス環境にログインします。
1. テストキャンペーンを作成します。 イベントやニュースレターなどのキャンペーンタイプを使用します。
1. キャンペーンを作成したら、**[!UICONTROL メンバーの管理]**/**[!UICONTROL メンバーの追加]**/**[!UICONTROL ファイルの読み込み]**&#x200B;を選択して、リードをキャンペーンメンバーとしてアップロードします。
1. 完了したら、Campaign ページレイアウトに戻り、ピックリストフィールドである「バイヤタッチポイントを有効にする」ことができます。 値を選択してください：**[!UICONTROL すべてのキャンペーンメンバーを含める]**。

これが完了すると、[!DNL Marketo Measure]と[!DNL Salesforce]の間で同期が開始され、タッチポイントがリードレコードに適用されます。 レポート タブ内の[!UICONTROL 購入者タッチポイントレポート &#x200B;] フォルダーに見つかった「リードに関するBuyer Touchpoint」というレポートを使用して、翌日に確認することをお勧めします。 レポートで各リードのタッチポイントが設定されている場合は、これは成功の兆候です。
