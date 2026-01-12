---
description: Salesforce サンドボックスを使用したMarketo Measure統合のテスト - [!DNL Marketo Measure]
title: Salesforce サンドボックスを使用したMarketo Measure統合のテスト
exl-id: df40b000-4572-46df-aef5-8f690ca8ed7a
feature: Salesforce
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 10%

---


# Salesforce サンドボックスを使用したMarketo Measure統合のテスト {#testing-the-marketo-measure-integration-with-a-salesforce-sandbox}

>[!NOTE]
>ドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には引き続き「Bizible」と表示されます。アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

[!DNL Marketo Measure] の主な機能の 1 つは、Web サイト上のアクションを通じてデジタルマーケティングの取り組みを追跡し、リードや連絡先を通じてそのデータを実稼動 [!DNL Salesforce org] ージにプッシュする機能です。 ただし、通常、サンドボックス統合内の web サイトから作成されたインバウンドリードはないので、データは純粋にオフラインの観点から焦点を当てます。

テストの両方のフェーズで参照する 2 つのソースを次に示します。 [ 手順 1～4](https://help.salesforce.com/s/articleView?id=lead_import_wizard.htm&language=en_US&type=5) および [ 手順 5～6](/help/channel-tracking-and-setup/offline-channels/legacy-processes/syncing-offline-campaigns.md)。 一部の領域で詳細を説明しているため、これらのドキュメントを確認することをお勧めします。

1. キャンペーンにアップロードできるように、CSV でリードを作成する必要があります。 その方法は、実稼動Salesforceのレポートを使用して一部のリードを書き出すことです。 それ以外の場合は、Excel ファイルでリードを手動で作成し、それを CSV として保存して読み込むことができます。 必要なレコードは約 20 件だけです。 ファイルには次の列が必要です。

   1. メール
   1. 会社
   1. 名前（姓）
   1. 名（オプションですが推奨）

1. サンドボックス環境にログインします。
1. テストキャンペーンを作成します。 イベントやニュースレターなどのキャンペーンタイプを使用します。
1. キャンペーンを作成したら、**[!UICONTROL メンバーを管理]**/**[!UICONTROL メンバーを追加]**/**[!UICONTROL ファイルをインポート]** を選択して、リードをキャンペーンメンバーとしてアップロードします。
1. その後、キャンペーンページレイアウトに戻ると、選択リストフィールドである「バイヤータッチポイントを有効にする」ようになります。 値 **[!UICONTROL すべてのキャンペーンメンバーを含める]** を選択します。

その後、[!DNL Marketo Measure] と [!DNL Salesforce] の同期が開始され、リードレコードにタッチポイントが適用されます。 「レポート」タブの「バイヤータッチポイントレポート [!UICONTROL  フォルダーにある「リードに関するBuyer Touchpoint」というレポートを使用して、翌日 ] 確認することをお勧めします。 レポートで各リードのタッチポイントに値が入力される場合、これは成功の兆候です。
