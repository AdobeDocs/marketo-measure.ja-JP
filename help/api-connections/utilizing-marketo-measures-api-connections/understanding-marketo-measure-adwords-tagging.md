---
unique-page-id: 18874678
description: について [!DNL Marketo Measure] AdWords タグ付け — [!DNL Marketo Measure]  — 製品ドキュメント
title: について [!DNL Marketo Measure] AdWords タグ付け
exl-id: c6658766-d3a8-46ed-b2d2-826eb61ce269
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 2%

---

# について [!DNL Marketo Measure] AdWords タグ付け {#understanding-marketo-measure-adwords-tagging}

非常に詳細なレベルで広告を追跡するには、広告のリンク先 URL を一意にする必要があります。 これを達成するには、 [!DNL Marketo Measure] 自動タグ付けにより、トラッキングパラメーターが [!DNL AdWords] 広告。 次の例を見てみましょう。

次の URL は、詳細なデータを提供しません。

* `http://example.com/landing-page?myParam=foo`

ただし、 [!DNL Marketo Measure] パラメータ：

* `http://example.com/landing-page?myParam=foo&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

## 方法 [!DNL Marketo Measure] 自動タグ付け機能 {#how-marketo-measure-auto-tagging-works}

**If [!DNL Marketo Measure] トラッキングテンプレートを検索します。**

* [!DNL Marketo Measure] により、そのパラメーターがトラッキングテンプレートに追加されます。
* Kenshoo や Marin などのトラッキングテンプレートでサードパーティのリダイレクトが見つかった場合、 [!DNL Marketo Measure] は何も実行しません。 代わりに、 [追加 [!DNL Marketo Measure] アカウント内のサードパーティツールのパラメーター](/help/api-connections/utilizing-marketo-measures-api-connections/how-bid-management-tools-affect-marketo-measure.md){target=&quot;_blank&quot;}。

ただし、トラッキングテンプレートが見つからない場合は、 [!DNL Marketo Measure] は次のようになります。

* すべての広告の宛先 URL をスキャンして [!DNL Marketo Measure] パラメーター。
* 見つかったら行って良い。
* 見つからない場合は、 [!DNL Marketo Measure] は、広告のリンク先 URL の末尾にパラメーターを追加します。 新しい広告の場合、 [!DNL Marketo Measure] は、作成から 2 時間以内に、そのパラメーターを広告のリンク先 URL に追加します。
* 自動タグ付けを有効にして [!DNL Marketo Measure] を添付して、広告履歴のリセットを防ぐことができます。

[!DNL Marketo Measure] では、アカウントレベル、キャンペーンレベル、広告グループレベルのトラッキングテンプレートを使用することをお勧めします。広告履歴の中断や削除のリスクを伴わずに、すべての広告のパラメーターの追加と減算が可能です。

## トラッキングテンプレート {#tracking-templates}

の説明に従って、 [!DNL Google AdWords]の場合、トラッキングテンプレートはランディングページに到達するために使用される URL です。 収集されたトラッキング情報は、広告トラフィックを把握するために使用されます。 [ここをクリック](https://support.google.com/adwords/answer/7197008?hl=ja){target=&quot;_blank&quot;} を参照してください。Google

[!DNL Marketo Measure] では、アカウントレベル、キャンペーンレベル、広告グループレベルトラッキングテンプレートの使用をお勧めします。広告履歴が中断または削除されるリスクを伴わずに、すべての広告のパラメーターの追加と減算が可能です。

トラッキングテンプレートは 2 つあります [!DNL Marketo Measure] では、を使用することをお勧めします。 適切なバージョンを判断するには、次の点に注意してください。

* すべての広告の URL に「?」が含まれている場合 その際に、次の URL を使用します。

`{lpurl}&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

* 広告の URL に「?」がない場合 その際に、次の URL を使用します。

`{lpurl}?_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

## アカウントレベルでのトラッキングテンプレートの設定 {#setting-up-a-tracking-template-at-the-account-level}

1. にログインします。 [!DNL Google AdWords] アカウント。

1. クリック **[!UICONTROL すべてのキャンペーン]** その後 **[!UICONTROL 設定]** をクリックします。

   ![](assets/1.png)

1. クリック **[!UICONTROL アカウント設定]** 時々一番上に **[!UICONTROL トラッキングテンプレート]**. 次を入力します。 [!DNL Marketo Measure] トラッキングテンプレート。

   ![](assets/2-1.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

## キャンペーンレベルでのトラッキングテンプレートの設定 {#setting-up-a-tracking-template-at-the-campaign-level}

1. クリック **[!UICONTROL すべてのキャンペーン]** その後 **[!UICONTROL キャンペーン]** をクリックします。

   ![](assets/3.png)

1. 該当するすべてのキャンペーンを選択するか、 **[!UICONTROL すべてを選択]**&#x200B;をクリックし、 **[!UICONTROL 編集]**&#x200B;をクリックし、 **[!UICONTROL トラッキングテンプレートの変更]**.

   ![](assets/4-1.png)

1. 次を入力します。 [!DNL Marketo Measure] トラッキングテンプレートを選択し、 **[!UICONTROL 適用]**.

## 広告グループレベルでのトラッキングテンプレートの設定： {#setting-up-a-tracking-template-at-the-ad-group-level}

1. クリック **[!UICONTROL すべてのキャンペーン]** その後 **[!UICONTROL 広告グループ]** をクリックします。

   ![](assets/5-1.png)

1. 該当するすべての広告グループを選択するか、「すべて選択」をクリックします。 **[!UICONTROL 編集]** 次に、 **[!UICONTROL トラッキングテンプレートの変更]**.

1. 次を入力します。 [!DNL Marketo Measure] トラッキングテンプレートを選択し、 **[!UICONTROL 適用]**.

   ![](assets/6-1.png)

## よくある質問 {#faq}

**Q:接続したユーザーに必要な権限を教えてください。**

回答：userinfo.email

**Q:支出データのインポートにはどのくらいの時間がかかりますか？**

回答：6 時間

**Q:広告データのインポートにはどの程度の時間がかかりますか？**

回答：4 時間

>[!NOTE]
>
>変更が完了したら、操作が完了します。 自由に手を差し伸べる [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support)設定時に質問がある場合は、{target=&quot;_blank&quot;}。

[ここをクリック](https://support.google.com/adwords/answer/6076199?hl=en#tracking){target=&quot;_blank&quot;} を参照してください。
