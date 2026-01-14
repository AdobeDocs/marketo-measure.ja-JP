---
description: Marketo Measure ユーザー向けSalesforce アクティビティ アトリビューションガイダンス
title: Salesforce アクティビティの属性
exl-id: 1dc6f15b-2a45-4ed3-9fa3-5267366d1f45
feature: Attribution, Salesforce
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 1%

---

# Salesforce アクティビティの属性 {#salesforce-activities-attribution}

[!DNL Marketo Measure] Salesforce アクティビティの統合により、特定のタスクおよびイベントレコードがアトリビューションモデルに取り込まれます。 販売用 E メールや販売用の電話など、期日のクレジットを受け取っていない項目の追跡を開始します。 アクティビティルールを設定するには、[experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} にアクセスしてください。 そこから、「**[!UICONTROL 設定]**」タブに移動して、「**[!UICONTROL アクティビティ]**」タブをクリックします。

![Marketo Measure Salesforce アクティビティの統合によって特定のタスクが呼び出される ](assets/activities-attribution-10.png)

まず、[!DNL Marketo Measure] Campaign と呼ばれる新しい概念を導入します。 定義したルールごとに、名前を付けることができる [!DNL Marketo Measure] Campaign にレコードをバケット化します。 必要に応じて、複数のキャンペーンを追加します。 有料メディアキャンペーンの横にあるアウトバウンドセールスキャンペーンの有効性を測定すると想像してください。

この [!DNL Marketo Measure] キャンペーン名を使用して、マッピング先のチャネルを教えてくれます。 それでもアウトバウンドセールスについて考えている場合は、おそらく、すべてのアウトバウンドセールスキャンペーンを BDR チャネルに配置する必要があります。

この階層について理解します。

* チャネル
   * サブチャネル
      * キャンペーン
      * キャンペーン
   * サブチャネル
      * キャンペーン

>[!TIP]
>
>営業担当者ごとに一意のキャンペーンを設定する場合（例：）は、動的な置き換えパラメーターを使用して [!DNL Marketo Measure] キャンペーン名を入力します。 同じ例で、`"Outbound Sales - {AssignedTo}"` と入力すると、`"Outbound Sales - Jill"` や `"Outbound Sales - Jack."` などに変更されます

![ 営業担当者ごとに一意のキャンペーンを設定する場合 ](assets/activities-attribution-11.png)

[!DNL Marketo Measure] キャンペーン名を設定したら、アクティビティルールを設定します。

ルールは、アトリビューションの対象となるレコードを示すフィルターとして機能します。 類似のロジックを使用して CRM でレポートを作成し、そのレポートを生成していると仮定します。 and/or ステートメントと様々な演算子（`matches any`、`contains`、`starts with`、`ends with`、`is equal to` など）を柔軟に組み合わせて使用できます。 ボックス化されたルール内の `and` ステートメントまたはボックス外のレイヤー `or` ステートメントを定義します。

![ ルールは、どのレコードがあるかを示すフィルターとして機能します ](assets/activities-attribution-12.png)

>[!NOTE]
>
>数式フィールドはルール内で使用できず、選択リストには表示されません。 式はバックグラウンドで計算され、レコードは変更されないの [!DNL Marketo Measure]、レコードが規則に適合するかどうかを検出できません。
>
>CrmEvent.CreatedById などの ID フィールドには正しい値を使用してください。 長さ [!DNL Salesforce IDs]18 文字（0054H000007WmrfQAC）です。

最後に、Buyer Touchpointの日付として使用する日付または日付/時間フィールドを 1 つ選択します。 標準フィールドとカスタムフィールドのどちらも選択できます。

>[!TIP]
>
>パッケージのインストール時に、[!DNL Marketo Measure] クティビティレコードにカスタムBuyer Touchpoint日フィールドが追加されます。 ステータスが変更された日付などの動的な日付を使用する場合は、CRM ワークフローを使用して「Buyer Touchpoint日」を設定し、この手順で「Buyer Touchpoint日」を選択します。

![ パッケージのインストール時に、Marketo Measureにカスタム Buyer Touchpointが含まれる ](assets/activities-attribution-13.png)

タスクまたはイベントに異なるルールを設定することを忘れないでください。 営業チームがアクティビティの記録に使用するオブジェクトを把握する必要があります。

![ タスクまたはイベントに異なるルールを設定することを忘れないでください。 あなた ](assets/activities-attribution-5.png)

これらの新しいタッチポイントを、適切な [ マーケティングチャネル ](https://experience.adobe.com/#/marketo-measure/MyAccount/Business?busView=false&id=10#/!/MyAccount/Business/Account.Settings.SettingsHome?tab=チャネル.Online%20 チャネル){target="_blank"} に配置することになるでしょう。 それには、作成されたばかりの新しいキャンペーンマッピングを使用してチャネルを定義します。

>[!TIP]
>
>チャネル定義を追加する場合は、ワイルドカード値を使用すると、次のような演算子の状態を簡単に設定できます。
>
>次で始まる（アウトバウンド &#42;）
>
>次を含む（&#42; アウトバウンド &#42;）
>
>次で終わる（アウトバウンド &#42;
>
>ワイルドカードは基本的に「次と等しい」という意味ではないので、必要に応じて使用してください。

| **演算子** | **ユースケース** |
|---|---|
| が次と等しい | 単一の値 – 完全一致 |
| 次を含む | 単一値 – 値を含む |
| 一致 | 複数の値 – 完全一致 |
| いずれかと一致する（次を含む） | 複数の値 – &#42;value&#42;、&#42;value、&#42;value&#42; |

![|いずれかと一致する（次を含む） |複数の値 – &amp;42;value&amp;42;, &amp;42;value, &amp;42;value&amp;42; |](assets/activities-attribution-8.png)

最後に、新しいチャネルのコストを入力するオプションがあります。 [ マーケティング費用のアップロード ](https://experience.adobe.com/#/marketo-measure/MyAccount/Business?busView=false&id=10#/!/MyAccount/Business/Account.Settings.SettingsHome?tab=Reporting.Marketing%20Spend){target="_blank"} では、費用をチャネルレベル、サブチャネルレベルまたはキャンペーンレベルで入力できます。 新しい [!DNL Marketo Measure] キャンペーンを使用すると、これらの関連コストを月別に追加し、各キャンペーンの ROI を確認できます。

![ さらに、コストを入力するオプションもあります ](assets/activities-attribution-9.png)

>[!MORELIKETHIS]
>
>[ アクティビティアトリビューションに関する FAQ](/help/channel-tracking-and-setup/activities-attribution-faq.md)
