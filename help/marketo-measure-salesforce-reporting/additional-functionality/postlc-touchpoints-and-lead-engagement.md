---
unique-page-id: 18874562
description: PostLC タッチポイントとリードエンゲージメント — Marketo Measure — 製品ドキュメント
title: PostLC Touchpoints とリードエンゲージメント
exl-id: 3ee5c571-195e-46c7-b150-fedcbc3614cb
feature: Touchpoints
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 3%

---

# PostLC Touchpoints とリードエンゲージメント {#postlc-touchpoints-and-lead-engagement}

[!DNL Marketo Measure] リード後の作成 (PostLC) タッチポイントは、マルチタッチアトリビューションモデル（W-Shape 以降）を使用するお客様が使用できます。 リードまたは連絡先が Web サイトに戻り、フォームの入力を続けると、これらのフォーム送信は PostLC タッチポイントとして登録されます。 これらのタッチポイントを使用すると、最初のコンバージョンの長後に、どのコンテンツがリードをサイトに引き続き関与させているかを確認できます。 PostLC タッチポイントは、商談内のすべての中間タッチポイントと属性クレジットを共有します。10%の属性クレジットは、中間タッチポイントに割り当てられ、すべてのタッチに均等に配分されます。

![](assets/1.png)

表示される PostLC タッチポイントの数を調整できます。 [!DNL SFDC]. 通常は、最大 5 つの PostLC タッチポイントをプッシュすることをお勧めします。各タッチポイントは、 [!DNL SFDC].

>[!NOTE]
>
>PostLC タッチポイント設定の調整方法については、この記事の最後に記載されています。

PostLC タッチポイントは動的です。 リードまたは連絡先として、引き続き PostLC フォームを送信します。 [!DNL Marketo Measure] は、CRM の PostLC タッチポイントを更新して、最新のフォーム送信を表示します。 特に、5 個の PostLC タッチポイントの制限を設定している場合、 [!DNL Marketo Measure] 常に 5 つを押し出す _最新_ タッチポイントから CRM にアクセスできます。  この例では、このアカウントは PostLC の制限を 4 つのタッチポイントに設定しています。 このリードは、CRM で使用できる PostLC タッチポイントの最大数に既に達しています。 最後の PostLC タッチは2/6/2018でした。 もしこの人が翌日別のフォームに記入するなら [!DNL Marketo Measure] は、最初の PostLC タッチポイントを11/9/2017から削除し、2/7/2018から最新のタッチポイントを追加します。

![](assets/2.png)

>[!NOTE]
>
>[!DNL Marketo Measure] リードまたは連絡先の PostLC タッチポイントのみを更新し、商談の PostLC 属性タッチポイントは更新しません。 連絡先上のすべての関連する PostLC タッチポイントが商談に含まれます。

## PostLC タッチポイント設定の変更方法 {#how-to-change-postlc-touchpoint-settings}

リードまたは連絡先の PostLC タッチポイント設定を調整するには、以下の手順に従います。

**リード**

1. にログインします。 [!DNL Marketo Measure] アカウント [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} をクリックし、 [!UICONTROL 設定].

1. CRM で、を選択します。 **[!UICONTROL リード]**.

1. リードにプッシュする postLC タッチポイントの数を入力し、 **[!UICONTROL 保存]**.

   ![](assets/3.png)

**連絡先**

1. にログインします。 [!DNL Marketo Measure] アカウント [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} をクリックし、 [!UICONTROL 設定].

1. CRM で、を選択します。 **[!UICONTROL 連絡先]**.

1. 連絡先にプッシュする postLC タッチポイントの数を入力し、 **[!UICONTROL 保存]**.

   ![](assets/4.png)
