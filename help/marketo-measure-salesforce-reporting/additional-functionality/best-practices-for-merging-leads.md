---
unique-page-id: 18874734
description: リードを結合する際のベストプラクティス - [!DNL Marketo Measure]
title: リードのマージのベストプラクティス
exl-id: d9293ed7-a794-4e52-a269-20a7fb36ce50
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---

# リードのマージのベストプラクティス {#best-practices-for-merging-leads}

[!DNL Salesforce] でリードを結合する場合、データが失われないように常に注意する必要があります。

参考までに、[!DNL Salesforce] サポートの [ リードの結合方法 ](https://help.salesforce.com/s/articleView?id=leads_merge.htm&amp;language=en_US&amp;type=5) の分類を以下に示します。

[!DNL Marketo Measure] の出番は、結合されたレコードに入力するフィールドを選択する時です。 マスターレコードを選択する際に、新しいレコードに引き継ぐように [!DNL Marketo Measure] のフィールドが選択されていることを検証します。

データを含むレコードが複数ある場合 [!DNL Marketo Measure]、最初に作成したリード用に選択したフィールドがマスターレコードにあることを確認します。 追加の [!DNL Marketo Measure] データは、「インサイト」セクションに表示されます。 また、トラッキング対象のリードのメールアドレスが、保持されているメールアドレスであることも確認してください。これにより、新しいアトリビューションデータを使用してそのリードを引き続き更新できるからです。

そこから、リードを自由に結合でき、[!DNL Marketo Measure] のデータは新しいレコードに引き継がれます。

ご不明な点については、Adobeアカウントチーム（アカウントマネージャー）または [Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。

![](assets/1.jpg)
