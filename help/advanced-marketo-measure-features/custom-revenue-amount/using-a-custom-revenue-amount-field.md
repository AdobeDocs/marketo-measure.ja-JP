---
unique-page-id: 18874793
description: カスタムの「売上高」フィールドの使用 –  [!DNL Marketo Measure]
title: カスタム収益額フィールドの使用
exl-id: 517ea4f9-aa83-48d0-8ce7-003f4a907430
feature: Custom Revenue Amount
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 3%

---

# カスタム収益額フィールドの使用 {#using-a-custom-revenue-amount-field}

デフォルトでは、バイヤー属性タッチポイントは、次の 2 つのフィールドのいずれかから商談額を取り込みます。

* 金額（SFDC のデフォルト）
* [!DNL Marketo Measure] 商談の金額（カスタム）

商談にカスタムの「金額」フィールドを使用している場合、Buyer Touchpointの売上高を計算するためのワークフローを設定する必要があります。 この操作には、[!DNL Salesforce] に関するより高度な知識が必要なので、SFDC 管理者の支援が必要になる場合があります。

まず、次の情報が必要です。

* 金額フィールドの API 名

ここから、ワークフローの作成を開始します。

## Salesforce Lightning でのワークフローの作成 {#create-the-workflow-in-salesforce-lightning}

以下の手順は、Salesforce Lightning ユーザー向けです。 Salesforce Classic を引き続き使用する場合は、これらの手順 [ 以下に示す ](#create-the-workflow-in-salesforce-classic) を参照してください。

1. 「設定」から、「クイック検索」ボックスに「フロー」と入力し、「**[!UICONTROL フロー]**」を選択して Flow Builder を開始します。 右側のパネルから「**[!UICONTROL 新しいフロー]**」ボタンをクリックします。

   ![](assets/using-a-custom-revenue-amount-field-1.png)

1. **[!UICONTROL レコードトリガーフロー]** を選択し、右下の **[!UICONTROL 作成]** をクリックします。

   ![](assets/using-a-custom-revenue-amount-field-2.png)

1. 開始を設定ウィンドウで、商談オブジェクトを選択します。 「[!UICONTROL トリガーを設定 ]」セクションで、「**[!UICONTROL レコードが作成または更新されました]**」を選択します。

   ![](assets/using-a-custom-revenue-amount-field-3.png)

1. [ エントリ条件の設定 ] セクションの [!UICONTROL  条件要件 ] で、[**[!UICONTROL カスタム条件ロジックが満たされています]**] を選択します。
   * 検索フィールドから、カスタムの「金額」フィールドを選択します。
   * 演算子を **Is Null**、値を **[!UICONTROL False]** に設定します。
   * 評価条件を **[!UICONTROL レコードが更新され、条件要件を満たすたびに]** に設定します。

   ![](assets/using-a-custom-revenue-amount-field-4.png)

1. 「フローの最適化」セクションで、「高速フィールド更新 **[!UICONTROL を選択し]** す。 右下の **[!UICONTROL 完了]** をクリックします。

   ![](assets/using-a-custom-revenue-amount-field-5.png)

1. 要素を追加するには、プラス（+）アイコンをクリックし、「**[!UICONTROL トリガーレコードを更新]**」を選択します。

   ![](assets/using-a-custom-revenue-amount-field-6.png)

1. 新規「レコードの更新」ウィンドウで、次の情報を入力します。

   * ラベルを入力 – API 名が自動的に生成されます
   * 「How to Find Records to Update and Set Their Values」で、「**[!UICONTROL フローをトリガーした商談レコードを使用]** を選択します。
   * 「[!UICONTROL  フィルター条件を設定 ]」セクションで、レコードを更新するための条件要件として **[!UICONTROL レコードを常に更新]** を選択します。
   * 「[!UICONTROL  キャンペーンレコードのフィールド値を設定 ]」の「フィールド」で、「Marketo Measure商談額」フィールドと「開始値」フィールドを選択します。 次に、カスタムの「金額」フィールドを選択します。
   * 「**[!UICONTROL 完了]**」をクリックします。

   ![](assets/using-a-custom-revenue-amount-field-7.png)

1. 「**[!UICONTROL 保存]**」をクリックします。ポップアップが表示されます。 フローを保存ウィンドウに「フローラベル」と入力します（フロー API 名は自動的に生成されます）。 再度「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/using-a-custom-revenue-amount-field-8.png)

1. **[!UICONTROL アクティブ化]** ボタンをクリックして、フローをアクティブ化します。

   ![](assets/using-a-custom-revenue-amount-field-9.png)

## Salesforce Classic でのワークフローの作成 {#create-the-workflow-in-salesforce-classic}

次の手順は、Salesforce Classic ユーザーを対象としています。 Salesforce Lightning に切り替えた場合は、これらの手順 [ 上記を参照 ](#create-the-workflow-in-salesforce-lightning) を参照してください。

1. **[!UICONTROL 設定]**/**[!UICONTROL 作成]**/**[!UICONTROL ワークフローと承認]**/**[!UICONTROL ワークフロールール]** に移動します。

   ![](assets/using-a-custom-revenue-amount-field-10.png)

1. 「**[!UICONTROL 新規ルール]**」を選択し、オブジェクトを「Opportunity」に設定して、「次へ **[!UICONTROL をクリックし]** す。

   ![](assets/using-a-custom-revenue-amount-field-11.png)

   ![](assets/using-a-custom-revenue-amount-field-12.png)

1. ワークフローの設定 ルール名を「Update [!DNL Marketo Measure] Opportunity Amount」として設定します。 評価条件を「作成済み、および編集するたびに」に設定します。 ルール条件に対して、カスタム「金額」フィールドを選択し、演算子 [!UICONTROL  「次に等しくない」 ] を選択して、「値」フィールドを空白のままにします。

   ![](assets/using-a-custom-revenue-amount-field-13.png)

1. ワークフローアクションの追加。 この選択リストを「[!UICONTROL  新しいフィールドの更新 ] に設定します。
   ![](assets/using-a-custom-revenue-amount-field-14.png)

1. フィールド情報を入力します。 「名前」フィールドには、「[!DNL Marketo Measure] 商談額」という名前を使用することをお勧めします。 「一意の名前」は、「名前」フィールドに基づいて自動的に入力されます。 「更新するフィールド」選択リストで、「[!DNL Marketo Measure] のオポチュニティ金額」を選択します。 フィールドを選択したら、「フィールドの変更後にワークフロールールを再評価」ボックスを選択します。 「新しいフィールド値を指定」で、「式を使用して新しい値を設定」を選択します。 空のボックスに、カスタムの「金額」フィールドの API 名をドロップします。 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/using-a-custom-revenue-amount-field-15.png)

1. ワークフローのロールアップページに戻ります。「アクティベート」してください。準備が整いました。 アクティブ化するには、新しいワークフローの横にある **[!UICONTROL 編集]** をクリックし、次に **[!UICONTROL アクティブ化]** をクリックします。

   これらの手順を完了したら、「カスタム商談 [!UICONTROL  フィールドの新しい値を持つワークフローをトリガーにするために、商談を更新する必要があり ] す。

   これは、SFDC 内のデータローダーを通じてオポチュニティを実行することで実現できます。 データローダーの使用について詳しくは、[ この記事 ](/help/advanced-marketo-measure-features/custom-revenue-amount/using-data-loader-to-update-marketo-measure-custom-amount-field.md) を参照してください。

途中でご不明な点がございましたら、Adobeアカウントチーム（担当のアカウントマネージャー）または [[!DNL Marketo]  サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。
