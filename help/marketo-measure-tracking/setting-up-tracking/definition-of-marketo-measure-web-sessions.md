---
unique-page-id: 18874564
description: の定義 [!DNL Marketo Measure] ウェブセッション — [!DNL Marketo Measure]
title: ' [!DNL Marketo Measure]  web セッションの定義'
exl-id: ddf4f19d-2024-413a-b0ae-4efd468c24de
feature: Tracking
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 97%

---

# [!DNL Marketo Measure] web セッションの定義 {#definition-of-marketo-measure-web-sessions}

[!DNL Marketo Measure] が web セッションを定義する方法を説明します。

**Web セッション**&#x200B;とは、一定期間における個人の web サイトとのインタラクションを指します。セッションは、ユーザーが web サイトを訪問すると開始されます。

例えば、Haley が adobe.com を訪問するとします。サイトを訪問すると、セッションが開始します。Haley がタブ／web ブラウザーを閉じるか、サイトから移動してサイトを離れると、セッションが終了します。

1 人のユーザーが同時に複数のセッションを開くことはできません。Haley が [!DNL adobe.com] を 10 個の異なるタブで開いても、web サイトへの訪問に関連して作成されるセッションは 1 つだけです。

## [!DNL Marketo Measure] が新しいセッションを定義する方法？ {#how-does-marketo-measure-define-a-new-session}

セッションが終了するタイミングと新しいセッションが開始するタイミングを決定する要素がいくつかあります。[!DNL Marketo Measure] セッションが終了する主な方法は、次の 2 つです。

* **時間ベースの有効期限**
* **チャネルベースの有効期限**

## 時間ベースの有効期限 {#time-based-expiration}

**セッションの持続時間**

[!DNL Marketo Measure] セッションは、web サイトで 30 分間アクティビティがないと終了します。例：

Haley が adobe.com を訪問すると、セッションが開始します。数分間 web サイトを探索した後、コンピューターから離れますが、web サイトは開いたままにします。セッションは、30 分間アクティビティがないと終了します。

現在、[!DNL Marketo Measure] は、ページナビゲーションとフォーム送信のみをアクティビティと見なします。Web ページをスクロールしたり、ページ上の要素にポインタを合わせたりすることは、アクティビティと見なされません。そのため、Haley がブログ投稿を読むために adobe.com を訪問し、読むのに 1 時間かかる場合、ページ上のコンテンツをスクロールしていても、web セッションは 30 分後に終了します。

## チャネルベースの有効期限 {#channel-based-expiration}

[!DNL Marketo Measure] は、ユーザーが別のデジタルマーケティングチャネルまたは外部 web サイトからユーザーの web サイトを訪問するたびに、新しいセッションを開始します。これには以下が含まれます。

* リファラル web サイト
* ソーシャルチャネル（[!DNL Facebook]、[!DNL LinkedIn] など）
* 有料またはオーガニック検索チャネル（[!DNL Google/Bing]）

**リファレル web サイトとソーシャルチャネル**

訪問者がリファレル web サイトまたはソーシャルチャネルからユーザーの web サイトを訪問すると、新しいセッションが開始されます。

Haley が LinkedIn を利用しており、[!DNL Marketo Measure] の投稿をクリックして、アドビ web サイトにリダイレクトされるとします。次に、[!DNL Facebook] をスクロールしている際に、Haley は別の [!DNL Marketo Measure] の投稿を見つけます。この投稿をクリックすると、アドビのサイトにリダイレクトされ、[!DNL LinkedIn] に関連する最初の web セッションが終了し、[!DNL Facebook] に関連する新しいセッションが開始されます。

**有料またはオーガニック検索チャネル**

ユーザーが有料またはオーガニック検索チャネルを通じてサイトを訪問すると、新しいセッションが開始されます。Haley がオーガニック検索を通じて アドビ web サイトを訪問してから、すぐに Google の有料広告を通じてユーザーの web サイトを訪問すると、2 つの別個のセッションが作成されます。

**Web ダイレクトトラフィック**

訪問者が web サイトの URL をアドレスバーに入力して web サイトを訪問した場合、必ずしも新しいセッションが開始されるわけではありません。

Haley の最初の web セッションがリファレルサイト、ソーシャルチャネルまたは有料／オーガニック検索チャネルからの訪問の結果として開始され、その後、web ダイレクト経由でサイトを訪問しても、新しいセッションは開始されません。

_ただし_、Haley の最初の web セッションが web ダイレクトから開始され、_外部／リファレルサイト_&#x200B;経由で web サイトを訪問すると、最初のセッションは終了し、外部／リファレルサイトに関連する新しいセッションが開きます。

## Google Analytics セッション {#google-analytics-sessions}

[!DNL Marketo Measure] と Google Analytics がセッションを定義する方法には、いくつかの類似点があります。セッションの定義方法の詳細については、次のGoogle Analyticsを参照してください。 [https://support.google.com/analytics/answer/2731565?hl=en](http://support.google.com/analytics/answer/2731565?hl=ja){target="_blank"}
