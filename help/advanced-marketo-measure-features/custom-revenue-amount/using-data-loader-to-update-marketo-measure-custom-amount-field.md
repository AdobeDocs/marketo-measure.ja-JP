---
unique-page-id: 18874771
description: データ ローダーを使用して [!DNL Marketo Measure]  カスタム金額フィールド - [!DNL Marketo Measure]を更新する
title: データローダーを使用したMarketo Measure カスタム金額フィールドの更新
exl-id: 55e91ac4-a835-48e0-a6ce-1d85b32aeac0
feature: Custom Revenue Amount
TQID: https://experienceleague.adobe.com/5guAGWeWMxJPm-vj8DYyHz2onjh3ERfzKtLcXNr0MM0
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 2%

---

# データ ローダーを使用して[!DNL Marketo Measure] カスタム金額フィールドを更新する {#using-data-loader-to-update-marketo-measure-custom-amount-field}

[!DNL Marketo Measure]では、カスタム収益フィールドを使用する場合に商談の値を更新する便利なオプションとして、データローダーを使用することをお勧めします（[!DNL Marketo Measure]では「金額」フィールドを使用します）。 スクリプトでは、[!DNL Marketo Measure] スクリプトの実行中にすべてのSalesforce検証ルールを無効にする必要があるため、[!DNL Marketo Measure]更新スクリプトを使用するよりもData Loaderを使用することをお勧めします。

## データ ローダーを使用して[!DNL Marketo Measure] カスタム金額フィールドを更新する{#using-data-loader-to-update-marketo-measure-custom-amount-field-1}

1. 次を使用してExcel シートを作成します。

   * 商談 ID
   * カスタム商談金額フィールド（任意の収益フィールド）
   * [!DNL Marketo Measure]商談金額フィールド

1. 任意の収益フィールドから値をコピーして、[!UICONTROL [!DNL Marketo Measure]商談金額] フィールドに貼り付けます。 次に、.csv ファイルを使用してこれらの商談を更新します。

**_または、Salesforceにアクセスし、カスタムリストビューを使用して、すべての商談を一括編集することもできます。..._**

1. すべての商談に対してカスタムリストビューを作成します。
1. 「優先収益」フィールドにフィルターを追加すると、_および_ [!UICONTROL Marketo]の「商談金額を測定」フィールドが空白になります。
1. 「**[!UICONTROL 一括編集]**」をクリックしますが、実際には何も変更しないでください。
1. 「**[!UICONTROL 保存]**」をクリックします。 これにより、ワークフローがトリガーされ、[!DNL Marketo Measure]件の商談金額フィールドに「ソフトウェア収益」フィールドが入力されます。
