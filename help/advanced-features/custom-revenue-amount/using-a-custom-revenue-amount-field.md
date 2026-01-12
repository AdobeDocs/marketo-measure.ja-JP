---
description: カスタムの「売上高」フィールドの使用 –  [!DNL Marketo Measure]
title: カスタム収益額フィールドの使用
exl-id: 517ea4f9-aa83-48d0-8ce7-003f4a907430
feature: Custom Revenue Amount
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 2%

---


# カスタム収益額フィールドの使用 {#using-a-custom-revenue-amount-field}

デフォルトでは、バイヤー属性タッチポイントは、次の 2 つのフィールドのいずれかから商談額を取り込みます。

* 金額（SFDCのデフォルト）
* [!DNL Marketo Measure] 商談の金額（カスタム）

商談にカスタムの「金額」フィールドを使用している場合、Buyer Touchpointの売上高を計算するためのワークフローを設定する必要があります。 これには、[!DNL Salesforce] に関するより高度な知識が必要なので、SFDC管理者の支援が必要になる場合があります。

まず、次の情報が必要です。

* 金額フィールドの API 名

ここから、ワークフローの作成を開始します。

## Salesforce Lightning でのワークフローの作成 {#create-the-workflow-in-salesforce-lightning}

次の手順は、Salesforce Lightning を使用する場合に実行します。 まだSalesforce Classic を使用している場合、これらの手順 [&#x200B; 以下に示します &#x200B;](#create-the-workflow-in-salesforce-classic)。

1. 「設定」から、「クイック検索」ボックスに「フロー」と入力し、「**[!UICONTROL フロー]**」を選択して Flow Builder を開始します。 右側のパネルから「**[!UICONTROL 新しいフロー]**」ボタンをクリックします。

   ![Salesforce フロービルダー（新規フローボタン付き） &#x200B;](assets/using-a-custom-revenue-amount-field-1.png)

1. **[!UICONTROL レコードトリガーフロー]** を選択し、右下の **[!UICONTROL 作成]** をクリックします。

   ![&#x200B; 「レコードトリガーフロー」オプションを使用したフロータイプの選択 &#x200B;](assets/using-a-custom-revenue-amount-field-2.png)

1. 開始を設定ウィンドウで、商談オブジェクトを選択します。 「[!UICONTROL トリガーを設定 &#x200B;]」セクションで、「**[!UICONTROL レコードが作成または更新されました]**」を選択します。

   ![&#x200B; 商談オブジェクトが選択された状態で開始ウィンドウを設定 &#x200B;](assets/using-a-custom-revenue-amount-field-3.png)

1. [ エントリ条件の設定 ] セクションの [!UICONTROL &#x200B; 条件要件 &#x200B;] で、[**[!UICONTROL カスタム条件ロジックが満たされています]**] を選択します。
   * 検索フィールドから、カスタムの「金額」フィールドを選択します。
   * 演算子を **Is Null**、値を **[!UICONTROL False]** に設定します。
   * 評価条件を **[!UICONTROL レコードが更新され、条件要件を満たすたびに]** に設定します。

   ![&#x200B; カスタム条件ロジックを使用したエントリ条件の設定 &#x200B;](assets/using-a-custom-revenue-amount-field-4.png)

1. 「フローの最適化」セクションで、「高速フィールド更新 **[!UICONTROL を選択し]** す。 右下の **[!UICONTROL 完了]** をクリックします。

   ![&#x200B; 「高速フィールド更新」を選択した場合のフロー設定の最適化 &#x200B;](assets/using-a-custom-revenue-amount-field-5.png)

1. 要素を追加するには、プラス（+）アイコンをクリックし、「**[!UICONTROL トリガーレコードを更新]**」を選択します。

   ![&#x200B; 「トリガーするレコードを更新」オプションを含むフロー要素メニュー &#x200B;](assets/using-a-custom-revenue-amount-field-6.png)

1. 新規「レコードの更新」ウィンドウで、次の情報を入力します。

   * ラベルを入力 – API 名が自動的に生成されます
   * 「How to Find Records to Update and Set Their Values」で、「**[!UICONTROL フローをトリガーした商談レコードを使用]** を選択します。
   * 「[!UICONTROL &#x200B; フィルター条件を設定 &#x200B;]」セクションで、レコードを更新するための条件要件として **[!UICONTROL レコードを常に更新]** を選択します。
   * 「[!UICONTROL &#x200B; キャンペーンレコードのフィールド値を設定 &#x200B;]」の「フィールド」で、「Marketo Measure商談額」フィールド（**bizible2__Bizible_Opportunity_Amount__c**）と「値」から選択します。 次に、カスタムの「金額」フィールドを選択します。
   * 「**[!UICONTROL 完了]**」をクリックします。

   ![&#x200B; フィールド値マッピングを使用したレコード設定の更新 &#x200B;](assets/using-a-custom-revenue-amount-field-7.png)

1. 「**[!UICONTROL 保存]**」をクリックします。ポップアップが表示されます。 フローを保存ウィンドウに「フローラベル」と入力します（フロー API 名は自動的に生成されます）。 再度「**[!UICONTROL 保存]**」をクリックします。

   ![&#x200B; ラベルフィールドを使用したフローダイアログの保存 &#x200B;](assets/using-a-custom-revenue-amount-field-8.png)

1. **[!UICONTROL アクティブ化]** ボタンをクリックして、フローをアクティブ化します。

   ![&#x200B; 「アクティブ化」ボタン付きフローの概要ページ &#x200B;](assets/using-a-custom-revenue-amount-field-9.png)

## Salesforce Classic でのワークフローの作成 {#create-the-workflow-in-salesforce-classic}

次の手順は、Salesforce Classic を使用する場合に実行します。 Salesforce Lightning に切り替えた場合は、これらの手順を参照してください [&#x200B; 上記を参照 &#x200B;](#create-the-workflow-in-salesforce-lightning)。

1. **[!UICONTROL 設定]**/**[!UICONTROL 作成]**/**[!UICONTROL ワークフローと承認]**/**[!UICONTROL ワークフロールール]** に移動します。

   ![&#x200B; ワークフロールールを表示するSalesforce Classic のナビゲーションメニュー &#x200B;](assets/using-a-custom-revenue-amount-field-10.png)

1. 「**[!UICONTROL 新規ルール]**」を選択し、オブジェクトを「Opportunity」に設定して、「次へ **[!UICONTROL をクリックし]** す。

   ![&#x200B; 「新規ルール」ボタンを含むワークフロールールページ &#x200B;](assets/using-a-custom-revenue-amount-field-11.png)

   ![Opportunity に設定されたワークフローのルールのオブジェクト選択 &#x200B;](assets/using-a-custom-revenue-amount-field-12.png)

1. ワークフローの設定 ルール名を「Update [!DNL Marketo Measure] Opportunity Amount」として設定します。 評価条件を「作成済み、および編集するたびに」に設定します。 ルール条件に対して、カスタム「金額」フィールドを選択し、演算子 [!UICONTROL &#x200B; 「次に等しくない」 &#x200B;] を選択して、「値」フィールドを空白のままにします。

   ![&#x200B; ルールの条件と評価の設定を使用したワークフロー設定 &#x200B;](assets/using-a-custom-revenue-amount-field-13.png)

1. ワークフローアクションの追加。 この選択リストを「[!UICONTROL &#x200B; 新しいフィールドの更新 &#x200B;] に設定します。
   ![&#x200B; 「新しいフィールドを更新」オプションを含んだワークフローアクションダイアログを追加 &#x200B;](assets/using-a-custom-revenue-amount-field-14.png)

1. フィールド情報を入力します。 「名前」フィールドには、「[!DNL Marketo Measure] 商談額」という名前を使用することをお勧めします。 「一意の名前」は、「名前」フィールドに基づいて自動的に入力されます。 「更新するフィールド」選択リストで、「[!DNL Marketo Measure] のオポチュニティ金額」を選択します。 フィールドを選択したら、「フィールドの変更後にワークフロールールを再評価」ボックスを選択します。 「新しいフィールド値を指定」で、「式を使用して新しい値を設定」を選択します。 空のボックスに、カスタムの「金額」フィールドの API 名をドロップします。 「**[!UICONTROL 保存]**」をクリックします。

   ![&#x200B; 名前、フィールドマッピングおよび数式設定を示すフィールド更新設定 &#x200B;](assets/using-a-custom-revenue-amount-field-15.png)

1. ワークフローのロールアップページに戻ります。「アクティベート」してください。準備が整いました。 アクティブ化するには、新しいワークフローの横にある **[!UICONTROL 編集]** をクリックし、次に **[!UICONTROL アクティブ化]** をクリックします。

   これらの手順を完了したら、「カスタム商談 [!UICONTROL &#x200B; フィールドの新しい値を持つワークフローをトリガーにするために、商談を更新する必要があり &#x200B;] す。

   これは、SFDC内のデータローダーを通じてオポチュニティを実行することで実現できます。 データローダーの使用について詳しくは、[&#x200B; この記事 &#x200B;](/help/advanced-marketo-measure-features/custom-revenue-amount/using-data-loader-to-update-marketo-measure-custom-amount-field.md){target="_blank"} を参照してください。

途中でご不明な点がある場合は、Adobe アカウントチーム（アカウントマネージャー）または [[!DNL Marketo]  サポート &#x200B;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。
