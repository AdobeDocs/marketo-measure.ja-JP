---
unique-page-id: 18874678
description: ' [!DNL Marketo Measure] AdWords タグ付けについて –  [!DNL Marketo Measure]'
title: ' [!DNL Marketo Measure] AdWords のタグ付けについて'
exl-id: c6658766-d3a8-46ed-b2d2-826eb61ce269
feature: APIs, Integration, UTM Parameters
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 6%

---

# [!DNL Marketo Measure] AdWords タグ付けについて {#understanding-marketo-measure-adwords-tagging}

広告を非常にきめ細かく追跡するには、広告宛先 URL が一意である必要があります。 これを実現するために、自動タグ付け [!DNL Marketo Measure]、トラッキングパラメーターを [!DNL AdWords] 広告の広告宛先 URL に自動的に追加します。 以下の例を見てみましょう。

次の URL は、詳細なデータを提供しません：

* `http://example.com/landing-page?myParam=foo`

ただし、[!DNL Marketo Measure] のパラメーターがあるので、同じ URL で詳細なデータが提供されます。

* `http://example.com/landing-page?myParam=foo&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

## 自動タギング [!DNL Marketo Measure] 仕組み {#how-marketo-measure-auto-tagging-works}

**追跡テンプレート [!DNL Marketo Measure] 見つかった場合：**

* [!DNL Marketo Measure] のパラメーターを追跡テンプレートに追加します。
* サードパーティのリダイレクトが Kenshoo や Marin などのトラッキングテンプレートで見つかった場合、[!DNL Marketo Measure] のアクションは実行されません。 代わりに、[ アカウントのサードパーティツールにパラメーターを追加  [!DNL Marketo Measure]  する ](/help/api-connections/utilizing-marketo-measures-api-connections/how-bid-management-tools-affect-marketo-measure.md){target="_blank"} 必要があります。

ただし、トラッキングテンプレートが見つからない場合は、次のよ [!DNL Marketo Measure] になります。

* すべての広告宛先 URL をスキャンして、[!DNL Marketo Measure] パラメーターを確認します。
* 見つかった場合は、行ってもよい。
* 見つからない場合、[!DNL Marketo Measure] のパラメーターを広告宛先 URL の末尾に追加します。 新規広告の場合、[!DNL Marketo Measure] は作成から 2 時間以内にパラメーターを広告宛先 URL に追加します。
* 自動タグ付けを有効にする前にトラッキングテンプレートを用意することが重要です [!DNL Marketo Measure] そうすることで、テンプレートに添付し、広告履歴のリセットを防ぐことができます。

[!DNL Marketo Measure] では、アカウントレベル、キャンペーンレベルまたは広告グループレベルのトラッキングテンプレートを使用することをお勧めします。これにより、広告履歴の中断や削除のリスクなしに、すべての広告のパラメーターを追加および削除できます。

## 追跡テンプレート {#tracking-templates}

[!DNL Google AdWords] で説明しているように、トラッキングテンプレートは、ランディングページに到達するために使用される URL です。 収集されたトラッキング情報は、広告トラフィックの把握に使用されます。 Googleについて詳しくは、[ ここをクリック ](https://support.google.com/adwords/answer/7197008?hl=en){target="_blank"} してください。

[!DNL Marketo Measure] では、広告履歴の中断や削除のリスクなしにすべての広告に関するパラメーターの追加と削除が可能なので、アカウントレベル、キャンペーンレベルまたは広告グループレベルのトラッキングテンプレートを使用することをお勧めします。

を使用することをお勧めするトラッキングテンプレート [!DNL Marketo Measure]2 つあります。 次の手順を使用して、適切なバージョンを判断します。

* すべての広告 URL に「?」が含まれる場合 その中で、次の URL を使用します。

`{lpurl}&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

* 広告 URL に「?」が含まれていない場合 その中で、次の URL を使用します。

`{lpurl}?_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

## アカウントレベルでのトラッキングテンプレートの設定 {#setting-up-a-tracking-template-at-the-account-level}

1. [!DNL Google AdWords] アカウントにログインします。

1. 展開ウィンドウで **[!UICONTROL すべてのキャンペーン]** をクリックしてから **[!UICONTROL 設定]** をクリックします。

   ![](assets/1.png)

1. 上部の **[!UICONTROL アカウント設定]** をクリックし、次に **[!UICONTROL トラッキングテンプレート]** をクリックします。 [!DNL Marketo Measure] 追跡テンプレートを入力します。

   ![](assets/2-1.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

## キャンペーンレベルでの追跡テンプレートの設定 {#setting-up-a-tracking-template-at-the-campaign-level}

1. 展開ウィンドウで **[!UICONTROL すべてのキャンペーン]** をクリックしてから **[!UICONTROL キャンペーン]** をクリックします。

   ![](assets/3.png)

1. 該当するキャンペーンをすべて選択するか、「**[!UICONTROL すべてを選択]**」をクリックし、「**[!UICONTROL 編集]**」をクリックして、「**[!UICONTROL トラッキングテンプレートを変更]**」をクリックします。

   ![](assets/4-1.png)

1. [!DNL Marketo Measure] Tracking Template を入力し、「**[!UICONTROL Apply]**」をクリックします。

## 広告グループレベルでのトラッキングテンプレートの設定： {#setting-up-a-tracking-template-at-the-ad-group-level}

1. 展開ウィンドウで、**[!UICONTROL すべてのキャンペーン]** をクリックしてから **[!UICONTROL 広告グループ]** をクリックします。

   ![](assets/5-1.png)

1. 該当するすべての広告グループを選択するか、「すべて選択」を選択し、「**[!UICONTROL 編集]**」をクリックします。次に、「**[!UICONTROL トラッキングテンプレートを変更]**」をクリックします。

1. [!DNL Marketo Measure] Tracking Template を入力し、「**[!UICONTROL Apply]**」をクリックします。

   ![](assets/6-1.png)

## よくある質問 {#faq}

**Q：接続されたユーザーに必要な権限を教えてください。**

A: userinfo.email

**Q：費用データのインポートにはどの程度の時間がかかりますか？**

A: 6 時間

**Q：広告データのインポートにはどの程度の時間がかかりますか？**

A: 4 時間

**Q：動的検索広告の場合、提供されたクリエイティブの見出し、説明などの組み合わせを追跡できますか？**

A：動的検索広告の個々のクリエイティブの詳細は取得できませんが、自動タギングが有効になっている場合は、クリエイティブ ID と属性収益を取得できます。

>[!NOTE]
>
>変更が完了したら、完了です。 設定中にご質問がある場合は [&#128279;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}Marketo サポートまでお問い合わせください。

アカウントレベルのトラッキングテンプレートの作成に関するGoogleの手順については、[ ここをクリック ](https://support.google.com/adwords/answer/6076199?hl=en#tracking){target="_blank"} してください。
