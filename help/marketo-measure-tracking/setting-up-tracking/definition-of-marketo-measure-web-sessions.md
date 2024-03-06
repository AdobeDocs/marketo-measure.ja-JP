---
unique-page-id: 18874564
description: の定義 [!DNL Marketo Measure] ウェブセッション — [!DNL Marketo Measure]
title: ' [!DNL Marketo Measure]  web セッションの定義'
exl-id: ddf4f19d-2024-413a-b0ae-4efd468c24de
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 61%

---

# [!DNL Marketo Measure] web セッションの定義 {#definition-of-marketo-measure-web-sessions}

[!DNL Marketo Measure] が web セッションを定義する方法を説明します。

**Web セッション**&#x200B;とは、一定期間における個人の web サイトとのインタラクションを指します。セッションは、ユーザーが web サイトを訪問すると開始されます。

例えば、Haley が adobe.com を訪問するとします。サイトを訪問すると、セッションが開始します。Haley がタブ／web ブラウザーを閉じるか、サイトから移動してサイトを離れると、セッションが終了します。

1 人のユーザーが同時に複数のセッションを開くことはできません。Haley が開いた場合 [!DNL adobe.com] 10 個の異なるタブでは、Sarah の web サイトへの訪問に関連して作成されたセッションは 1 つだけです。

## [!DNL Marketo Measure] が新しいセッションを定義する方法？ {#how-does-marketo-measure-define-a-new-session}

セッションが終了するタイミングと新しいセッションが開始するタイミングを決定する要素がいくつかあります。[!DNL Marketo Measure] セッションが終了する主な方法は、次の 2 つです。

* **時間ベースの有効期限**
* **チャネルベースの有効期限**

## 時間ベースの有効期限 {#time-based-expiration}

**セッションの持続時間**

[!DNL Marketo Measure] セッションは、web サイトで 30 分間アクティビティがないと終了します。例：

Haley が adobe.com を訪問すると、セッションが開始します。数分間 web サイトを探索した後、コンピューターから離れますが、web サイトは開いたままにします。30 分間の無操作状態が続くと、セッションは終了します。

現在、[!DNL Marketo Measure] は、ページナビゲーションとフォーム送信のみをアクティビティと見なします。Web ページをスクロールしたり、ページ上の要素にポインタを合わせたりすることは、アクティビティと見なされません。そのため、Haley がブログ投稿を読むために adobe.com を訪問し、読むのに 1 時間かかる場合、ページ上のコンテンツをスクロールしていても、web セッションは 30 分後に終了します。

## チャネルベースの有効期限 {#channel-based-expiration}

[!DNL Marketo Measure] は、ユーザーが別のデジタルマーケティングチャネルや外部 Web サイトから Web サイトにアクセスすると常に新しいセッションを開始します。 これには以下が含まれます。

* リファラル web サイト
* ソーシャルチャネル ([!DNL Facebook], [!DNL LinkedIn]など )
* 有料またはオーガニック検索チャネル（[!DNL Google/Bing]）

**リファレル web サイトとソーシャルチャネル**

訪問者が参照元 Web サイトまたはソーシャルチャネルから Web サイトにアクセスすると、新しいセッションが開始されます。

Haley がLinkedInにいるとして、 [!DNL Marketo Measure] 投稿すると、AdobeWeb サイトにリダイレクトされます。 次に、[!DNL Facebook] をスクロールしている際に、Haley は別の [!DNL Marketo Measure] の投稿を見つけます。この投稿をクリックしてAdobeサイトにリダイレクトされると、Sarah が次のリンクに関連する最初の Web セッションを開始します。 [!DNL LinkedIn] 関連する新しいセッションを終了する [!DNL Facebook] が開始されます。

**有料またはオーガニック検索チャネル**

新しいセッションは、ユーザーが有料検索チャネルやオーガニック検索チャネルを通じてサイトにアクセスしたときに始まります。 Haley がオーガニック検索でAdobeの Web サイトにアクセスし、すぐにGoogleの有料広告を通じて Web サイトにアクセスすると、2 つの異なるセッションが作成されます。

**Web ダイレクトトラフィック**

訪問者が web サイトの URL をアドレスバーに入力して web サイトを訪問した場合、必ずしも新しいセッションが開始されるわけではありません。

Haley の最初の web セッションがリファレルサイト、ソーシャルチャネルまたは有料／オーガニック検索チャネルからの訪問の結果として開始され、その後、web ダイレクト経由でサイトを訪問しても、新しいセッションは開始されません。

_ただし、_（Haley の最初の Web セッションが Web Direct から開始された場合）、Haley はを介して Web サイトにアクセスします。 _外部/紹介サイト_&#x200B;に設定すると、最初のセッションが終了し、外部/リファラルサイトに関連する新しいセッションが開きます。

## Google Analytics セッション {#google-analytics-sessions}

[!DNL Marketo Measure] と Google Analytics がセッションを定義する方法には、いくつかの類似点があります。セッションの定義方法の詳細については、次のGoogle Analyticsを参照してください。 [https://support.google.com/analytics/answer/2731565?hl=en](https://support.google.com/analytics/answer/2731565?hl=en){target="_blank"}
