---
description: リードを結合する際のベストプラクティス - [!DNL Marketo Measure]
title: リードのマージのベストプラクティス
exl-id: d9293ed7-a794-4e52-a269-20a7fb36ce50
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 5%

---


# リードのマージのベストプラクティス {#best-practices-for-merging-leads}

[!DNL Salesforce] でリードを結合する場合、データが失われないように常に注意する必要があります。

参考までに、[ サポートの ](https://help.salesforce.com/s/articleView?id=leads_merge.htm&language=en_US&type=5) リードの結合方法 [!DNL Salesforce] の分類を以下に示します。

[!DNL Marketo Measure] の出番は、結合されたレコードに入力するフィールドを選択する時です。 マスターレコードを選択する際に、新しいレコードに引き継ぐように [!DNL Marketo Measure] のフィールドが選択されていることを検証します。

データを含むレコードが複数ある場合 [!DNL Marketo Measure]、最初に作成したリード用に選択したフィールドがマスターレコードにあることを確認します。 追加の [!DNL Marketo Measure] データは、「インサイト」セクションに表示されます。 また、トラッキング対象のリードのメールアドレスが、保持されているメールアドレスであることも確認してください。これにより、新しいアトリビューションデータを使用してそのリードを引き続き更新できるからです。

そこから、リードを自由に結合でき、[!DNL Marketo Measure] のデータは新しいレコードに引き継がれます。

ご不明な点については、Adobe アカウントチーム（アカウントマネージャー）または [Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} までお問い合わせください。

![Marketo Measure フィールドを保持したSalesforceのリード結合ダイアログ ](assets/1.jpg)
