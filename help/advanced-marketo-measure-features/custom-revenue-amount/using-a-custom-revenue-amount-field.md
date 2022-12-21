---
unique-page-id: 18874793
description: カスタムの「売上高」フィールドの使用 — [!DNL Marketo Measure]  — 製品ドキュメント
title: カスタムの「売上高」フィールドの使用
exl-id: 517ea4f9-aa83-48d0-8ce7-003f4a907430
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 2%

---

# カスタムの「売上高」フィールドの使用 {#using-a-custom-revenue-amount-field}

デフォルトでは、購入者の属性タッチポイントは、次の 2 つのフィールドのいずれかから商談額を引き出します。

* 金額（SFDC デフォルト）
* [!DNL Marketo Measure] 商談額（カスタム）

商談のカスタムの「金額」フィールドを使用する場合は、購入者のタッチポイント売上高を計算するために、ワークフローを設定する必要があります。 これには、より高度な知識が必要です [!DNL Salesforce]の場合は、SFDC 管理者からの支援が必要になる場合があります。

最初に、次の情報が必要になります。

* 金額フィールドの API 名

ここから、ワークフローの作成を開始します。

1. に移動します。 **[!UICONTROL 設定]** > **[!UICONTROL 作成]** > **[!UICONTROL ワークフローと承認]** > **[!UICONTROL ワークフロールール]**.

   ![](assets/1.jpg)

1. 選択 **[!UICONTROL 新規ルール]**&#x200B;をクリックし、オブジェクトを「商談」に設定して、 **[!UICONTROL 次へ]**.

   ![](assets/2.jpg)

   ![](assets/3.jpg)

1. ワークフローを設定します。 ルール名を「Update」に設定します。 [!DNL Marketo Measure] 商談の金額。」 評価条件を「作成済み、編集されるたびに」に設定します。 ルールの条件で、カスタムの「金額」フィールドを選択し、演算子を選択します。 [!UICONTROL 「次と等しくない」として] 「値」フィールドは空白のままにします。

   ![](assets/4.jpg)

1. ワークフローアクションを追加します。 この選択リストを&quot;[!UICONTROL 新しいフィールドの更新].&quot;

   ![](assets/5.jpg)

1. ここでフィールド情報を入力します。 「名前」フィールドでは、次の名前を使用することをお勧めします。&quot;[!DNL Marketo Measure] 商談額」 「一意の名前」は、「名前」フィールドに基づいて自動的に入力されます。 「更新するフィールド」の選択リストで、「[!DNL Marketo Measure] 商談の金額。」 フィールドを選択した後、「フィールドの変更後にワークフロールールを再評価」ボックスを選択します。 「新しいフィールド値を指定」で、「数式を使用して新しい値を設定」を選択します。 空のボックスに、カスタムの「Amount」フィールドの API 名をドロップします。 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/6.png)

1. ワークフローのロールアップページに戻ります。必ず「有効化」を実行してください。 有効にするには、 **編集** 新しいワークフローの横にあるをクリックし、 **有効化**.

   これらの手順を完了したら、ワークフローに新しい値を [!UICONTROL カスタム商談] フィールドに入力します。

   これは、SFDC 内のデータローダーを通じて商談を実行することで実現できます。 でのデータローダーの使用の詳細を確認してください。 [この記事](/help/advanced-marketo-measure-features/custom-revenue-amount/using-data-loader-to-update-marketo-measure-custom-amount-field.md).

途中でご質問がある場合は、カスタマーサクセスマネージャーに気軽にお問い合わせください。 [[!DNL Marketo] サポート](https://nation.marketo.com/t5/support/ct-p/Support){target=&quot;_blank&quot;}。
