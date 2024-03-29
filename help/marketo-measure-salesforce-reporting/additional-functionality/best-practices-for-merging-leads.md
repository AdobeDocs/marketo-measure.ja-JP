---
unique-page-id: 18874734
description: リードのマージのベストプラクティス — [!DNL Marketo Measure]
title: リードのマージのベストプラクティス
exl-id: d9293ed7-a794-4e52-a269-20a7fb36ce50
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---

# リードのマージのベストプラクティス {#best-practices-for-merging-leads}

でリードをマージする場合 [!DNL Salesforce]を使用する場合は、常に注意して、データが失われないようにします。

以下に、 [リードのマージ方法](https://help.salesforce.com/s/articleView?id=leads_merge.htm&amp;language=en_US&amp;type=5) から [!DNL Salesforce] サポート。

ここで、 [!DNL Marketo Measure] は、マージされたレコードに入力されるフィールドを選択するタイミングになります。 マスターレコードを選択したら、 [!DNL Marketo Measure] フィールドが選択され、新しいレコードに引き継がれます。

次の条件を満たす複数のレコードがある場合 [!DNL Marketo Measure] データを入力する場合は、マスターレコードに、最初に作成されたリード用に選択されたフィールドが含まれていることを確認します。 その他 [!DNL Marketo Measure] データが「インサイト」セクション内に表示されます。 また、追跡するリードの電子メールアドレスが、保持されている電子メールアドレスであることを確認します。これにより、新しい属性データを使用してそのリードを引き続き更新できます。

ここから、リードと [!DNL Marketo Measure] データは新しいレコードに引き継がれます。

ご質問がある場合は、Adobeアカウントチーム（担当のアカウントマネージャー）に気軽に連絡し、または [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.

![](assets/1.jpg)
