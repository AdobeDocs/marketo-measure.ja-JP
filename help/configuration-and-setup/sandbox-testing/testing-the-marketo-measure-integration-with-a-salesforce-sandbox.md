---
unique-page-id: 18874765
description: Salesforce Sandbox とのMarketo Measure統合のテスト — [!DNL Marketo Measure]
title: Salesforce Sandbox とのMarketo Measure統合のテスト
exl-id: df40b000-4572-46df-aef5-8f690ca8ed7a
feature: Salesforce
source-git-commit: 741ab20845de2f3bcde589291d7446a5b4f877d8
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 5%

---

# Salesforce Sandbox とのMarketo Measure統合のテスト {#testing-the-marketo-measure-integration-with-a-salesforce-sandbox}

>[!NOTE]
>
>この場合、[!DNL Marketo Measure]」 （ドキュメント内）が表示されますが、CRM には「Bizible」が表示されます。 アドビは現在、その更新を行っており、ブランディングの変更がまもなく CRM に反映される予定です。

いずれかの [!DNL Marketo Measure] 主な機能は、Web サイト上でのアクションを通じてデジタルマーケティングの取り組みを追跡し、そのデータを実稼動環境にプッシュする機能です [!DNL Salesforce org] リードと連絡先から。 ただし、通常、サンドボックス統合内に Web サイトから作成されたインバウンドリードはないので、データに対する焦点は純粋にオフラインの観点からなります。

次に、テストの両方の段階で参照される 2 つのソースを示します。 [手順 1 ～ 4](https://help.salesforce.com/s/articleView?id=lead_import_wizard.htm&amp;language=en_US&amp;type=5) および [手順 5～6](/help/channel-tracking-and-setup/offline-channels/legacy-processes/syncing-offline-campaigns.md). 一部の領域で詳細な情報が提供されるので、これらのドキュメントを確認することをお勧めします。

1. リードをキャンペーンにアップロードするには、CSV でリードを作成する必要があります。 これをおこなう方法は、実稼動版の Salesforce のレポートから一部のリードを書き出すことです。 それ以外の場合は、Excel ファイルにリードを手動で作成し、読み込むための CSV として保存できます。 必要なレコードは約 20 個です。 ファイルには次の列が必要です。

   1. メール
   1. 会社
   1. 名前（姓）
   1. 名（オプション、推奨）

1. サンドボックス環境にログインします。
1. テストキャンペーンを作成します。 イベントやニュースレターなどのキャンペーンタイプを使用します。
1. キャンペーンを作成したら、「 」を選択して、リードをキャンペーンメンバーとしてアップロードします。 **[!UICONTROL メンバーを管理]** > **[!UICONTROL メンバーを追加]** > **[!UICONTROL ファイルの読み込み]**.
1. 完了したら、キャンペーンページレイアウトに戻り、選択リストフィールドである「Enable Buyer Touchpoints」を選択します。 値を選択します。 **[!UICONTROL すべてのキャンペーンメンバーを含める]**.

この処理が完了すると、 [!DNL Marketo Measure] および [!DNL Salesforce] リードレコードにタッチポイントを適用します。 次の日に、「リードの購入者タッチポイント」というレポートを確認することをお勧めします。詳しくは、 [!UICONTROL 購入者タッチポイントレポート] フォルダーを作成します。 レポートが各リードのタッチポイントに入力されている場合は、成功の兆しです。
