---
unique-page-id: 18874564
description: の定義 [!DNL Marketo Measure] ウェブセッション — [!DNL Marketo Measure]  — 製品ドキュメント
title: の定義 [!DNL Marketo Measure] ウェブセッション
exl-id: ddf4f19d-2024-413a-b0ae-4efd468c24de
source-git-commit: ae5b77744d523606ce6cfcf48d7e8d5049d5ccb7
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# の定義 [!DNL Marketo Measure] ウェブセッション {#definition-of-marketo-measure-web-sessions}

方法 [!DNL Marketo Measure] web セッションを定義します。

A **web セッション** は、ある一定期間における個人の Web サイトとのやり取りを指します。 セッションは、ユーザーが Web サイトにアクセスした時点で開始されます。

例えば、Haley が adobe.com を訪問したとします。 彼女がサイトを訪れると、セッションが始まります。 Haley がサイトを離れたとき、タブ/Web ブラウザーを閉じるかサイトから移動すると、セッションは終了します。

1 人のユーザーが同時に複数のセッションを開くことはできません。 Haley が開いた場合 [!DNL adobe.com] 10 個の異なるタブでは、Sarah の web サイトへの訪問に関連して作成されたセッションは 1 つだけです。

## 方法 [!DNL Marketo Measure] 新しいセッションを定義しますか？ {#how-does-marketo-measure-define-a-new-session}

セッションが終了するタイミングと新しいセッションが開始されるタイミングを決定するいくつかの点があります。 2 つの主な方法 [!DNL Marketo Measure] セッションは次のように終了します。

* **時間ベースの有効期限**
* **チャネルベースの有効期限**

## 時間ベースの有効期限 {#time-based-expiration}

**セッションはどのくらい続きますか？**

[!DNL Marketo Measure] セッションは、Web サイトで 30 分間操作が実行されなかった場合に終了します。 例：

Haley が adobe.com を訪問すると、セッションが開始されます。 数分間ウェブサイトを探索し、コンピュータから離れて行くが、ウェブサイトは開いたままにする。 無操作状態が 30 分間続くと、セッションは終了します。

現在、 [!DNL Marketo Measure] は、ページナビゲーションとフォーム送信をアクティビティと見なします。 Web ページをスクロールしたり、ページ上の要素の上にマウスポインターを置いたりしても、「アクティビティ」とは見なされません。 Haley が adobe.com を訪問してブログの投稿を読み、1 時間かかっても、ページ上のコンテンツをスクロールしていても、Web セッションは 30 分後に終了します。

## チャネルベースの有効期限 {#channel-based-expiration}

[!DNL Marketo Measure] は、ユーザーが別のデジタルマーケティングチャネルや外部 Web サイトから Web サイトにアクセスしたときにいつでも新しいセッションを開始します。 これには以下が含まれます。

* 紹介 Web サイト
* ソーシャルチャネル ([!DNL Facebook], [!DNL LinkedIn]など )
* 有料検索チャネルまたはオーガニック検索チャネル ([!DNL Google/Bing])

**紹介 Web サイトとソーシャルチャネル**

訪問者が参照元 Web サイトまたはソーシャルチャネルから Web サイトにアクセスすると、常に新しいセッションが開始されます。

Haley がLinkedInにいて、 [!DNL Marketo Measure] 投稿すると、AdobeWeb サイトにリダイレクトされます。 次に、スクロールしながら [!DNL Facebook]ヘーリーは別の [!DNL Marketo Measure] 投稿します。 この投稿をクリックしてAdobeサイトにリダイレクトされると、Sarah が次のリンクに関連する最初の Web セッションを開始します。 [!DNL LinkedIn] 関連する新しいセッションを終了する [!DNL Facebook] が開始されます。

**有料検索チャネルまたはオーガニック検索チャネル**

ユーザーが有料検索チャネルやオーガニック検索チャネルを通じてサイトにアクセスすると、常に新しいセッションが開始されます。 Haley がオーガニック検索でAdobeの Web サイトにアクセスし、すぐにGoogleの有料広告を通じて Web サイトにアクセスすると、2 つの異なるセッションが作成されます。

**ウェブダイレクトトラフィック**

訪問者が Web サイトの URL をアドレスバーに入力して Web サイトにアクセスした場合、新しいセッションが開始されることはありません。

Haley の最初の Web セッションが紹介サイト、ソーシャルチャネル、有料/オーガニック検索チャネルからの訪問の結果として開始され、Web 経由でサイトに直接アクセスした場合、新しいセッションは開始されません。

_ただし、_（Haley の最初の Web セッションが Web Direct から開始された場合）、Haley はを介して Web サイトにアクセスします。 _外部/紹介サイト_&#x200B;に設定すると、最初のセッションが終了し、外部/リファラルサイトに関連する新しいセッションが開きます。

## Google Analyticsセッション {#google-analytics-sessions}

方法には似た点があります [!DNL Marketo Measure] Google Analyticsはセッションを定義します。 セッションの定義方法の詳細については、次のGoogle Analyticsを参照してください。 [https://support.google.com/analytics/answer/2731565?hl=en](http://support.google.com/analytics/answer/2731565?hl=en){target=&quot;_blank&quot;}
