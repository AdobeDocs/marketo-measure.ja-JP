---
unique-page-id: 18874562
description: PostLC タッチポイントとリードエンゲージメント — Marketoの測定 — 製品ドキュメント
title: PostLC タッチポイントとリードエンゲージメント
exl-id: 3ee5c571-195e-46c7-b150-fedcbc3614cb
source-git-commit: f13e55f009f33140ff36523212ed8b9ed5449a4d
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# PostLC タッチポイントとリードエンゲージメント {#postlc-touchpoints-and-lead-engagement}

[!DNL Marketo Measure] リード後の作成 (PostLC) タッチポイントは、マルチタッチアトリビューションモデル（W-Shape 以降）を使用するお客様が使用できます。 リードまたは連絡先が Web サイトに戻り、フォームの入力を続けると、これらのフォーム送信は PostLC タッチポイントとして登録されます。 これらのタッチポイントを使用すると、最初のコンバージョンの長後に、どのコンテンツがリードをサイトに引き続き関与させているかを確認できます。 PostLC タッチポイントは、商談内のすべての中間タッチポイントとアトリビューションクレジットを共有します。10%のアトリビューションクレジットは、中間のタッチポイントに割り当てられ、すべてのタッチに均等に配分されます。

![](assets/1.png)

表示される PostLC タッチポイントの数を調整できます。 [!DNL SFDC]. 通常、最大 5 つの PostLC タッチポイントをプッシュすることをお勧めします。各タッチポイントは、 [!DNL SFDC].

>[!NOTE]
>
>PostLC タッチポイント設定の調整方法については、この記事の最後に記載されています。

PostLC タッチポイントは動的です。 リードまたは連絡先として、引き続き PostLC フォームを送信します。 [!DNL Marketo Measure] は、CRM の PostLC タッチポイントを更新して、最新のフォーム送信を表示します。 特に、5 個の PostLC タッチポイントの制限を設定している場合、 [!DNL Marketo Measure] 常に 5 を押す _最新_ タッチポイントから CRM にアクセスできます。  この例では、このアカウントは PostLC の制限を 4 つのタッチポイントに設定しています。 このリードは、CRM で使用できる PostLC タッチポイントの最大数に既に達しています。 最後の PostLC タッチは2/6/2018でした。 もしこの人が翌日別のフォームに記入するなら [!DNL Marketo Measure] は、最新のタッチポイントを2/7/2018から追加するために、11/9/2017から最初の PostLC タッチポイントを削除します。

![](assets/2.png)

>[!NOTE]
>
>[!DNL Marketo Measure] は、リードまたは連絡先の PostLC タッチポイントのみを更新し、商談の PostLC 属性タッチポイントは更新しません。 連絡先上のすべての関連する PostLC タッチポイントが商談に含まれます。

## PostLC タッチポイント設定の変更方法 {#how-to-change-postlc-touchpoint-settings}

リードまたは連絡先の PostLC タッチポイント設定を調整するには、以下の手順に従ってください。

**リード**

1. にログインします。 [!DNL Marketo Measure] アカウント [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure){target=&quot;_blank&quot;} に移動し、 [!UICONTROL 設定].

1. CRM で、を選択します。 **[!UICONTROL リード]**.

1. リードにプッシュする postLC タッチポイントの数を入力し、 **[!UICONTROL 保存]**.

   ![](assets/3.png)

**取引先責任者**

1. にログインします。 [!DNL Marketo Measure] アカウント [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure){target=&quot;_blank&quot;} に移動し、 [!UICONTROL 設定].

1. CRM で、を選択します。 **[!UICONTROL 連絡先]**.

1. 連絡先にプッシュする postLC タッチポイントの数を入力し、 **[!UICONTROL 保存]**.

   ![](assets/4.png)
