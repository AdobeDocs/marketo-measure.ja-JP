---
unique-page-id: 18874582
description: '"[!DNL Marketo Measure] Salesforce オブジェクト — [!DNL Marketo Measure]  — 製品ドキュメント»'
title: '"[!DNL Marketo Measure] Salesforce オブジェクト»'
exl-id: d5d6f334-6531-40fa-b043-75b49d8f43d5
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 1%

---

# [!DNL Marketo Measure] Salesforce オブジェクト {#marketo-measure-salesforce-objects}

>[!NOTE]
>
>&quot;[!DNL Marketo Measure]」 （アドビのドキュメント内）。ただし、CRM には「Bizible」が表示されます。 アドビは現在、その更新をおこなっており、ブランディングの変更が CRM に反映される予定です。

条件 [!DNL Marketo Measure] が [!DNL Salesforce] (SFDC)、複数のカスタム [!DNL Marketo Measure] オブジェクトが追加されます。 この記事では、これらのカスタムのいくつかの説明を提供します [!DNL Marketo Measure] オブジェクト。 一部のオブジェクト [!DNL Marketo Measure] に追加 [!DNL Salesforce] 次の場合：

* [購入者タッチポイント](#touchpoint)
* [購入者の属性タッチポイント](#attribution)
* [[!DNL Marketo Measure] 人物](#person)
* [[!DNL Marketo Measure] A/B テスト](#ab)
* [[!DNL Marketo Measure] イベント](#events)

追跡したいものによってキャプチャされたタッチポイントは、 [!DNL Bizible Salesforce] パッケージ。

[!DNL Marketo Measure] 特定の規格に関連するオブジェクト [!DNL Salesforce] オブジェクト。 これにより、 [!DNL Marketo Measure] および [!DNL Salesforce] オブジェクトをまとめます。 次の表に、次の内容を示します。 [!DNL Salesforce] オブジェクト [!DNL Marketo Measure] オブジェクトはに関連します。

![](assets/1-1.png)

## 購入者タッチポイント {#buyer-touchpoint}

この [!UICONTROL 購入者タッチポイント] (BT) オブジェクトは、個人のマーケティングストーリーを伝えます。 リードと連絡先によって生成されたマーケティングタッチポイントに関連するすべてのデータを格納します。 BT は、タッチポイントがどのマーケティングチャネルから来たか、または特定のリード/連絡先を Web サイトに導いた Ad Campaign の情報を示します。

BT オブジェクトは、リードページと連絡先ページに、 **関連リスト** （下の画像を参照）。

![](assets/2-1.png)

「BT 関連リスト」には、リードまたは連絡先に属するすべてのタッチポイントが表示されます。 リスト内にはカスタム [!DNL Marketo Measure] 各タッチポイントに関する詳細を提供するフィールド。 「 Buyer Touchpoint ID 」をクリックすると、 Buyer Touchpoint Detail ページに移動します。このページには、その Web セッション中にリード/連絡先が訪問した最初の Web ページ (**ランディングページ**) をクリックします。

## 購入者の属性タッチポイント {#buyer-attribution-touchpoint}

この [!UICONTROL 購入者の属性タッチポイント] オブジェクトは、オポチュニティに関連する連絡先のマーケティングインタラクションのストーリーを示します。 これには、 *帰属* マーケティングタッチポイントに関連するデータ。 このオブジェクトを使用すると、各マーケティングタッチポイントに関連する売上高クレジットの数を確認できます。 使用しているアトリビューションモデルのタイプによって、タッチポイントに起因する売上高の割合が決まります。

購入者属性タッチポイント (BAT) は、購入者タッチポイント (BT) データを持つ連絡先に関連する商談が作成された場合にのみ作成されます。 BAT は商談なしでは作成されません。 オポチュニティが作成されると、BAT オブジェクトは [!DNL Salesforce] *金額* フィールドに値を入力し、タッチポイントにどの程度の売上高をもたらすかを把握します。

A **ワークフロー** を使用する場合は、 [カスタム金額フィールド](/help/advanced-marketo-measure-features/custom-revenue-amount/using-a-custom-revenue-amount-field.md) をクリックして、Opportunity オブジェクトの売上高を表示します。 [!DNL Marketo Measure] は、カスタムの「金額」フィールドに表示される情報を読み取れないので、タッチポイントに売上高属性データを設定できません。 このワークフローでは、 **[!DNL Marketo Measure]商談額** フィールド ( [!DNL Marketo Measure] カスタムフィールドを使用して、カスタムの「金額」フィールドの売上高の値を「商談の金額」フィールドにマッピングします。

![](assets/3-1.png)

BAT オブジェクトは、 [!UICONTROL 商談], [!UICONTROL 連絡先]、および [!UICONTROL アカウント] 関連リストとしてのオブジェクト。 このリストには、商談に属する属性データを持つすべてのタッチポイントが表示されます。 「 Buyer Attribution Touchpoint ID 」をクリックすると、「 Buyer Attribution Touchpoint Detail 」ページに移動します。 ここでは、より具体的なアトリビューションデータと、タッチポイントの元に関する情報（購入者タッチポイントオブジェクトから提供されるものと同様）を確認できます。

## [!DNL Marketo Measure] 人物 {#marketo-measure-person}

この [!DNL Marketo Measure] 「Person Object」は、リードオブジェクトと連絡先オブジェクトを関連付けます。 Salesforce は、同じレポート内でリードと連絡先オブジェクトを使用してレポートを作成するオプションを提供していません。 リードと連絡先オブジェクトに関連付けると、 [!DNL Marketo Measure] 「担当者」を使用すると、同じレポート内の両方のオブジェクトに関するレポートを作成できます。 これは、リードが連絡先に変換された場合に特に便利です。 日付： [!DNL Marketo Measure] 担当者レコードには、対応するリード/連絡先レコード、その人物に関連するタッチポイントの関連リスト、および人物 ID（常にリード/連絡先の電子メールアドレス）のルックアップが表示されます。 以降 [!DNL Marketo Measure] リードと連絡先オブジェクトに関連する担当者。このオブジェクトには、 [!DNL Marketo Measure] 購入者属性タッチポイントに結び付けられた人物レコード。 以下に、 [!DNL Marketo Measure] Salesforce 内の担当者レコード：

![](assets/4.png)

## [!DNL Marketo Measure] A/B テスト {#marketo-measure-a-b-test}

A/B テストを [!DNL Optimizely] または VWO(Visual Web Optimizer) を使用して、これらのアカウントを [!DNL Marketo Measure] Salesforce 内で A/B テストデータを表示するアカウント。 この [!DNL Marketo Measure] A/B テストオブジェクトを使用すると、基本的に Optimizely/VWO から A/B テストデータを取得し、そのデータをリードと連絡先に結び付けることができます。

![](assets/5.png)

この [!DNL Marketo Measure] A/B テストオブジェクトは、 [!UICONTROL リード], [!UICONTROL 連絡先] および [!UICONTROL 商談] ページ。 リストは、Optimizely または VWO を通じて実行しているすべての実験とバリエーションを表示し、特定のリードと連絡先に関連する実験とバリエーションを確認できます。

## [!DNL Marketo Measure] イベント {#marketo-measure-events}

この [!DNL Marketo Measure] イベントオブジェクトを使用すると、Web サイトで発生した特定のイベントを追跡できます。 Web サイトで発生する特定のイベントを追跡するには、ページに加えて、カスタムコードを追加する必要があります。 [!DNL Marketo Measure] JavaScript。 取り込んだ情報は、 [!DNL Marketo Measure] オブジェクト関連リスト ( [!UICONTROL リード], [!UICONTROL 連絡先] および [!UICONTROL 商談] ページ。 この [!DNL Marketo Measure] Events オブジェクト *次の値と等しくない* 属性データに関連付けます。 このオブジェクトの目的は、訪問者が Web サイト上で特定のアクションを実行しているかどうかを確認することです。

## [!DNL Marketo Measure] フィールド {#marketo-measure-fields}

によって取り込まれたデータ [!DNL Marketo Measure] JavaScript がカスタムにプッシュされます [!DNL Marketo Measure] アドビの [!DNL Marketo Measure] オブジェクト。 特定のフィールドは、特定のオブジェクトにのみ存在します。 の用語集 [!DNL Marketo Measure] フィールドを入力してください [ここをクリック](/help/introduction-to-marketo-measure/overview-resources/glossary-of-marketo-measure-fields.md). のビジュアライゼーションの場合 [!DNL Marketo Measure] 各 [!DNL Marketo Measure] 関連するフィールドを選択してください。 [ここをクリック](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-object-and-field-taxonomy.md).

## [!DNL Marketo Measure] レポートとダッシュボード {#marketo-measure-reports-and-dashboards}

この [!DNL Marketo Measure] に追加されたレポートとダッシュボード [!DNL Salesforce] には、標準のレポート機能とデータ視覚化機能が用意されています。 これらは基本です [!DNL Marketo Measure] タッチポイントデータをすばやく整理、分析、理解できるレポートです。
