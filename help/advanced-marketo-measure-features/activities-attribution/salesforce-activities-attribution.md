---
unique-page-id: 18874708
description: Salesforce アクティビティ属性 — [!DNL Marketo Measure]  — 製品ドキュメント
title: Salesforce アクティビティ属性
exl-id: 1dc6f15b-2a45-4ed3-9fa3-5267366d1f45
feature: Attribution, Salesforce
source-git-commit: a2a7657e8377fd5c556d38f6eb815e39d2b8d15e
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 1%

---

# Salesforce アクティビティ属性 {#salesforce-activities-attribution}

The [!DNL Marketo Measure] Salesforce アクティビティ統合により、特定のタスクおよびイベントレコードが属性モデルに取り込まれます。 セールスメールやセールス電話の呼び出しなど、クレジットが支払われていないものを追跡し始めます。 アクティビティルールを設定するには、次の場所に移動する必要があります： [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure){target="_blank"}. そこから、 **[!UICONTROL 設定]** 」タブをクリックし、 **[!UICONTROL アクティビティ]** タブをクリックします。

セールスチームを非常に幸せにしようとしています！ 簡単なチュートリアルをご覧ください。

![](assets/1.png)

まず始めに、 [!DNL Marketo Measure] キャンペーン。 定義したルールごとに、レコードを [!DNL Marketo Measure] 名前を付けることができるキャンペーン。 必要に応じて複数のキャンペーンを追加します。 ペイドメディアキャンペーンの隣にあるアウトバウンドセールスキャンペーンの効果を測定すると想像してみてください。

これを使用します [!DNL Marketo Measure] マッピング先のチャネルを示すキャンペーン名。 アウトバウンドセールスについてまだ考えている場合は、おそらくすべてのアウトバウンドセールスキャンペーンを BDR チャネルに配置する必要があります。

この階層について理解する：

* チャネル
   * サブチャネル
      * キャンペーン
      * キャンペーン
   * サブチャネル
      * キャンペーン

>[!TIP]
>
>例えば、各セールス担当に対して一意のキャンペーンを設定する場合は、動的な置き換えパラメーターを利用して [!DNL Marketo Measure] キャンペーン名。 同じ例で、 `"Outbound Sales - {AssignedTo}"` そして私たちはそれを何かのようなものに変えます `"Outbound Sales - Jill"` または `"Outbound Sales - Jack."` どれだけ時間を節約したか分からない！

![](assets/2.png)

一度、 [!DNL Marketo Measure] キャンペーン名が設定されている場合は、アクティビティルールを設定します。

ルールは、どのレコードが属性を持つ資格があるかを示すフィルターとして機能します。 同様のロジックを使用して CRM でレポートを作成し、そのレポートを生成すると仮定します。 および/または文の組み合わせを使用し、任意の一致、次を含む、次の語句で始まる、次の語句で終わる、次と等しいなどの様々な演算子を使用できる柔軟性があります。 ボックスルール内またはボックス外のレイヤー「or」ステートメント内に「and」ステートメントを定義します。

![](assets/3.png)

>[!NOTE]
>
>数式フィールドは、ルール内で使用できず、選択リストには表示されません。 数式はバックグラウンドで計算され、レコードは変更されないので、 [!DNL Marketo Measure] は、レコードがルールに適合するかどうかを検出できません。
>
>ID フィールドには、 CrmEvent.CreatedById などの正しい値を必ず使用してください。 [!DNL Salesforce IDs] は 18 文字です ( 例：0054H000007WmrfQAC)。

最後に、を購入者タッチポイント日として使用する日付または日付/時間フィールドの 1 つを選択します。 標準フィールドとカスタムフィールドのどちらも選択できます。

>[!TIP]
>
>パッケージのインストールで、 [!DNL Marketo Measure] アクティビティレコードにカスタムの購入者タッチポイント日フィールドが含まれています。 ステータスが変更された日付など、動的な日付を使用する場合は、CRM ワークフローを使用して「購入者タッチポイントの日付」を設定し、ここでこの手順で「購入者タッチポイントの日付」を選択できます。

![](assets/4.png)

タスクまたはイベントに別のルールを設定することを忘れないでください。 セールスチームがアクティビティの記録に使用するオブジェクトを把握する必要があります。

![](assets/5.png)

これらの新しいタッチポイントを適切なタッチポイントに配置したい場合があります。 [マーケティングチャネル](https://experience.adobe.com/#/marketo-measure/MyAccount/Business?busView=false&amp;id=10#/!/MyAccount/Business/Account.Settings.SettingsHome?tab=Channels.Online%20Channels){target="_blank"}. それには、先ほど作成した新しい Campaign マッピングでチャネルを定義します。 BDR チャネルの新しい行を作成して、キャンペーンがアウトバウンドで始まるようにします。

>[!TIP]
>
>チャネル定義を追加する場合、ワイルドカード値を使用すると、演算子を簡単に次のように記述できます。
>
>次で始まる ( Outbound)&#42; )
>
>次を含む ( &#42;Outbound&#42; )
>
>次の値で終わる ( &#42;送信 )
>
>ワイルドカードは基本的に「等しい」を意味しないので、必要に応じて必ず使用してください。

| **演算子** | **使用例** |
|---|---|
| 次と等しい | 単一の値 — 完全一致 |
| 次を含む | 単一の値 — 値を含む |
| 任意に一致 | 複数の値 — 完全一致 |
| いずれかに一致（次を含む） | 複数の値 — &#42;値&#42;, &#42;値 &#42;値&#42; |

![](assets/6.png)

最後に、新しいチャネルのコストを入力するオプションがあります。 アドビの [マーケティング費用のアップロード](https://experience.adobe.com/#/marketo-measure/MyAccount/Business?busView=false&amp;id=10#/!/MyAccount/Business/Account.Settings.SettingsHome?tab=Reporting.Marketing%20Spend){target="_blank"} では、チャネルレベル、サブチャネルレベルまたはキャンペーンレベルでの支出を入力できます。 新しい [!DNL Marketo Measure] キャンペーンでは、関連コストを月単位で追加し、各キャンペーンの ROI を確認できます。

![](assets/7.png)

>[!MORELIKETHIS]
>
>[アクティビティ属性に関する FAQ](/help/advanced-marketo-measure-features/activities-attribution/activities-attribution-faq.md)
