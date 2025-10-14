---
unique-page-id: 18874582
description: "[!DNL Marketo Measure] Salesforce オブジェクト - [!DNL Marketo Measure]"
title: 「[!DNL Marketo Measure] Salesforce オブジェクト」
exl-id: d5d6f334-6531-40fa-b043-75b49d8f43d5
feature: Salesforce
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 88%

---

# [!DNL Marketo Measure] Salesforce オブジェクト {#marketo-measure-salesforce-objects}

>[!NOTE]
>
>ドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には引き続き「Bizible」と表示されます。アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

[!DNL Marketo Measure] が [!DNL Salesforce]（SFDC）にインストールされると、複数のカスタム [!DNL Marketo Measure] オブジェクトが追加されます。この記事では、これらのカスタム [!DNL Marketo Measure] オブジェクトのいくつかについて説明します。[!DNL Marketo Measure] が [!DNL Salesforce] に追加するオブジェクトには次のようなものがあります。

* [Buyer Touchpoint](#touchpoint)
* [Buyer Attribution Touchpoint](#attribution)
* [[!DNL Marketo Measure] 担当者](#person)
* [[!DNL Marketo Measure] A/B テスト](#ab)
* [[!DNL Marketo Measure] イベント](#events)

追跡する対象によってキャプチャされたタッチポイントは、[!DNL Bizible Salesforce] パッケージのインストールによって作成されたカスタムオブジェクトに書き込まれます。

[!DNL Marketo Measure] オブジェクトは、特定の標準 [!DNL Salesforce] オブジェクトに関連します。これにより、[!DNL Marketo Measure] オブジェクトと [!DNL Salesforce] オブジェクトをまとめてレポートできます。次の表に、[!DNL Marketo Measure] オブジェクトがどの [!DNL Salesforce] オブジェクトに関連しているかを示します。

![](assets/1-1.png)

## Buyer Touchpoint {#buyer-touchpoint}

[!UICONTROL Buyer Touchpoint]（BT）オブジェクトは、個人のマーケティングストーリーを示します。リードと取引先責任者によって生成されたマーケティングタッチポイントに関連するすべてのデータを格納します。BT には、タッチポイントがどのマーケティングチャネルから来たのか、またはどの広告キャンペーンが特定のリード／取引先責任者を web サイトに導いたのかなどの情報が表示されます。

BT オブジェクトは、リードページと取引先責任者ページに、**関連リスト**&#x200B;として表示されます（下の画像を参照）。

![](assets/2-1.png)

BT 関連リストには、リードまたは取引先責任者に属するすべてのタッチポイントが表示されます。リスト内には、各タッチポイントに関する詳細を提供するカスタム [!DNL Marketo Measure] フィールドがあります。Buyer Touchpoint ID 番号をクリックすると、Buyer Touchpoint の詳細ページに移動します。このページには、web セッション中にリード／取引先責任者が訪問した最初の web ページ（**ランディングページ**）など、タッチポイントに関するさらに詳細な情報が表示されます。

## Buyer Attribution Touchpoint {#buyer-attribution-touchpoint}

[!UICONTROL Buyer Attribution Touchpoint] オブジェクトは、商談に関連する取引先責任者のマーケティングインタラクションのストーリーを示します。マーケティングタッチポイントに関連する&#x200B;*アトリビューション*&#x200B;データが表示されます。このオブジェクトを使用すると、各マーケティングタッチポイントに起因する収益クレジットの数を確認できます。使用しているアトリビューションモデルのタイプによって、タッチポイントに起因する収益の割合が決まります。

Buyer Attribution Touchpoints（BAT）は、Buyer Touchpoint（BT）のデータを持つ取引先責任者に関連する商談が作成された場合にのみ作成されます。BAT は商談がなければ作成されません。商談が作成されると、BAT オブジェクトは商談の「[!DNL Salesforce] *金額*」フィールドを使用して、タッチポイントに起因する収益を把握します。

[カスタム金額フィールド](/help/advanced-marketo-measure-features/custom-revenue-amount/using-a-custom-revenue-amount-field.md)を使用して商談オブジェクトの収益を表示する場合は、**ワークフロー**&#x200B;を作成する必要があります。[!DNL Marketo Measure] は「カスタム金額」フィールドに表示される情報を読み取ることができないので、タッチポイントに収益属性データを入力できません。このワークフローでは、[!DNL Marketo Measure] カスタムフィールドの 1 つである「**[!DNL Marketo Measure]商談金額**」フィールドを使用して、収益値を「カスタム金額」フィールドから「商談金額」フィールドにマッピングします。

![](assets/3-1.png)

BAT オブジェクトは、[!UICONTROL 商談]、[!UICONTROL 取引先責任者]および[!UICONTROL アカウント]オブジェクトに関連リストとして表示されます。このリストには、商談に属する属性データを持つすべてのタッチポイントが表示されます。Buyer Attribution Touchpoint ID をクリックすると、Buyer Attribution Touchpoint の詳細ページに移動します。ここでは、より具体的なアトリビューションデータと、タッチポイント元に関する情報（Buyer Touchpoint オブジェクトから提供されるものと同様）を確認できます。

## [!DNL Marketo Measure] 担当者 {#marketo-measure-person}

[!DNL Marketo Measure] 担当者オブジェクトは、リードオブジェクトと取引先責任者オブジェクトを関連付けます。Salesforce の初期状態では、同じレポート内でリードオブジェクトと、取引先責任者オブジェクトを使用してレポートを作成するオプションを提供していません。[!DNL Marketo Measure] 担当者をリードオブジェクトと取引先責任者オブジェクトに関連付けると、同じレポート内で両方のオブジェクトに関するレポートを作成できます。これは、リードが取引先責任者に転換した際に特に役立ちます。[!DNL Marketo Measure] Person レコードでは、対応するリードや連絡先レコードへのルックアップ、人物に関連付けられたタッチポイントの関連リスト、人物 ID （常にリード/連絡先のメールアドレスです）が表示されます。 [!DNL Marketo Measure] 担当者はリードと取引先責任者オブジェクトに関連しているので、Buyer Attribution Touchpoint に関連付けられた [!DNL Marketo Measure] 担当者レコードは存在しません。以下に、Salesforce 内の [!DNL Marketo Measure] 担当者レコードの例を示します。

![](assets/4.png)

## [!DNL Marketo Measure] A/B テスト {#marketo-measure-a-b-test}

A/B テストを [!DNL Optimizely] または VWO（Visual Web Optimizer）を使用して実行している場合は、それらのアカウントを [!DNL Marketo Measure] アカウントに接続して、Salesforce 内で A/B テストデータを表示できます。[!DNL Marketo Measure] A/B テストオブジェクトを使用すると、基本的に Optimizely／VWO から A/B テストデータを取得し、そのデータをリードと取引先責任者に結び付けることができます。

![](assets/5.png)

[!DNL Marketo Measure] A/B テストオブジェクトは、[!UICONTROL リード]、[!UICONTROL 取引先責任者]および[!UICONTROL 商談]ページに関連リストとして表示されます。このリストには、Optimizely または VWO で実行中のすべての実験とバリエーションが表示され、特定のリードおよび連絡先に関連する実験/バリエーションを確認できます。

## [!DNL Marketo Measure] イベント {#marketo-measure-events}

[!DNL Marketo Measure] イベントオブジェクトを使用すると、web サイトで発生した特定のイベントを追跡できます。Web サイトで発生する特定のイベントを追跡するには、[!DNL Marketo Measure] JavaScript に加えて、ページにカスタムコードを追加する必要があります。取り込んだ情報は、[!DNL Marketo Measure] オブジェクト関連リスト（[!UICONTROL リード]、[!UICONTROL 取引先責任者]および[!UICONTROL 商談]ページ）内に表示されます。[!DNL Marketo Measure] イベントオブジェクトは属性データに&#x200B;*関連付けられません*。このオブジェクトの目的は、訪問者が web サイト上で特定のアクションを実行しているかどうかを確認することです。

## [!DNL Marketo Measure] フィールド {#marketo-measure-fields}

[!DNL Marketo Measure] JavaScriptで取得されたデータは、[!DNL Marketo Measure] オブジェクト内のカスタム [!DNL Marketo Measure] フィールドにプッシュされます。 特定のフィールドは、特定のオブジェクトにのみ存在します。 [[!DNL Marketo Measure] フィールド ] の用語集 &rbrack;(/help/introduction-to-marketo-measure/overview-resources/glossary-of-marketo-measure-fields.md) および [&#x200B; 関連オブジェクトのビジュアライゼーション &#x200B;](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-object-and-field-taxonomy.md) を確認  [!DNL Marketo Measure]  きます。

## [!DNL Marketo Measure] レポートとダッシュボード {#marketo-measure-reports-and-dashboards}

[!DNL Salesforce] に追加された [!DNL Marketo Measure] レポートとダッシュボードには、標準のレポート機能とデータ視覚化機能が用意されています。この基本的な [!DNL Marketo Measure] レポートにより、タッチポイントデータをすばやく整理、分析、理解できます。
