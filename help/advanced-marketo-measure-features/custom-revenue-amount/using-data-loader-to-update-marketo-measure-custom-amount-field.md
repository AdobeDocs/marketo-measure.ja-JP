---
unique-page-id: 18874771
description: データローダーを使用した更新  [!DNL Marketo Measure]  カスタム金額フィールド - [!DNL Marketo Measure]
title: データローダーを使用したMarketo Measureのカスタム金額フィールドの更新
exl-id: 55e91ac4-a835-48e0-a6ce-1d85b32aeac0
feature: Custom Revenue Amount
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# データローダーを使用したカスタム金額フィールド [!DNL Marketo Measure] 更新 {#using-data-loader-to-update-marketo-measure-custom-amount-field}

[!DNL Marketo Measure] では、[!DNL Marketo Measure] でカスタム収益フィールド（標準の「金額」フィールドを使用）を使用する際に商談値を更新する便利なオプションとして、データローダーを使用することをお勧めします。 データローダーは、[!DNL Marketo Measure] 更新スクリプトを使用するよりも推奨されます。これは、スクリプトの実行中にユーザーがすべてのSalesforce検証ルールを無効にする必要があるから [!DNL Marketo Measure] す。

## データローダーを使用したカスタム金額フィールド [!DNL Marketo Measure] 更新{#using-data-loader-to-update-marketo-measure-custom-amount-field-1}

1. 次を使用して Excel シートを作成します。

   * 商談 ID
   * 「カスタム商談額」フィールド（優先収益フィールド）
   * [!DNL Marketo Measure] Opportunity Amount」フィールド

1. 優先収益フィールドの値をコピーして、「[!UICONTROL [!DNL Marketo Measure] Opportunity Amount]」フィールドに貼り付けます。 次に、.csv ファイルを使用してこれらの商談を更新します。

**_または、Salesforceでカスタムリストビューを使用してすべてのオポチュニティを一括編集することもできます…_**

1. すべてのオポチュニティ用のカスタムリスト表示を作成します。
1. 優先収益フィールドにフィルターを追加しても空白にはなりません _および_[!UICONTROL Marketo] 「商談額の測定」フィールドが空白になります。
1. **[!UICONTROL 一括編集]** をクリックしますが、実際には何も変更しません。
1. 「**[!UICONTROL 保存]**」をクリックします。これにより、ワークフローのトリガーが設定され、「[!DNL Marketo Measure] Opportunity Amount」フィールドに「Software Revenue」フィールドが表示されます。
