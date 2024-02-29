---
unique-page-id: 18874771
description: データローダを使用した更新 [!DNL Marketo Measure] カスタム金額フィールド — [!DNL Marketo Measure]
title: データローダーを使用したMarketo Measureのカスタム金額フィールドの更新
exl-id: 55e91ac4-a835-48e0-a6ce-1d85b32aeac0
feature: Custom Revenue Amount
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# データローダを使用した更新 [!DNL Marketo Measure] カスタム金額フィールド {#using-data-loader-to-update-marketo-measure-custom-amount-field}

[!DNL Marketo Measure] では、カスタム売上高フィールドを使用する場合（標準の「Amount」フィールドを使用）、商談の値を更新する便利なオプションとして、Data Loader を使用することをお勧めします。 [!DNL Marketo Measure]. データローダーは、 [!DNL Marketo Measure] スクリプトを更新すると、ユーザは、 [!DNL Marketo Measure] スクリプトを実行します。

## データローダを使用した更新 [!DNL Marketo Measure] カスタム金額フィールド{#using-data-loader-to-update-marketo-measure-custom-amount-field-1}

1. 以下を含む Excel シートを作成します。

   * 商談 ID
   * カスタム商談額フィールド（希望する収益フィールド）
   * [!DNL Marketo Measure] 商談額フィールド

1. 希望する売上高フィールドの値を [!UICONTROL [!DNL Marketo Measure] 商談額] フィールドに入力します。 次に、 .csv ファイルを使用してこれらの商談を更新します。

**_または、Salesforce にアクセスし、カスタムのリスト表示を使用して、すべての商談を一括編集することもできます。_**

1. すべての商談に対してカスタムリストビューを作成します。
1. 優先売上高フィールドのフィルターの追加は空白ではありません _および_ [!UICONTROL Marketo] 「商談額を測定」フィールドが空白です。
1. クリック **[!UICONTROL 一括編集]**&#x200B;でも実際には何も変更しないでください。
1. 「**[!UICONTROL 保存]**」をクリックします。これにより、トリガーを設定して [!DNL Marketo Measure] 「商談額」フィールドに「ソフトウェアの売上高」フィールドが表示されます。
