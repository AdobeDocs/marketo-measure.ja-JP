---
unique-page-id: 18874592
description: コールトラッキングの統合 — [!DNL Marketo Measure]
title: コールトラッキングの統合
exl-id: bc35a789-e056-4456-9038-306ed34c2a8e
feature: Tracking, Integration
source-git-commit: 4787f765348da71bc149c997470ce678ba498772
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 1%

---

# コールトラッキングの統合 {#call-tracking-integration}

との統合 [!DNL CallTrackingMetrics] は、web セッションと電話の呼び出しを結合することを目的としています。 電話の呼び出しは、次に対するフォーム送信として処理されます： [!DNL Marketo Measure]. 実際のフォーム送信がないので、Web 訪問と見なされるだけの Web セッションにクレジットが与えられます。

## コールトラッキングの説明 {#call-tracking-explained}

一般的な意味での「コールトラッキング」は、 [!DNL CallTrackingMetrics], [!DNL DiaglogTech], [!DNL Invoca]または [!DNL CallRail]を参照してください。 一意の電話番号は、ユーザーが来た様々なマーケティングチャネルやキャンペーンに基づいてユーザーに表示されます。 これにより、マーケターは、これらのチャネルやキャンペーンの効果を確認できます。

![](assets/1.png)

## 前後 {#before-and-after}

以下のフローチャートを見て、 [!DNL Marketo Measure] CallTrackingMetrics との統合なしで電話を処理するために使用します。 発生した電話呼び出しはトラッキングされなかったので、Web セッションと見なされ、そのタッチポイントは作成されませんでした。 タッチポイントが最終的に入力されるのは、次の訪問でユーザーがフォームに入力してからです。

統合を使用すると、Web セッションが電話呼び出しに実際に結び付けられていたことを確認できます。 次のフォーム入力は PostLC タッチになり、ジャーニーの一環として引き続き追跡されます。

![](assets/2.png)

## 仕組み {#how-it-works}

CallTrackingMetrics を機能させるには、その目的で開発作業を行う必要があります。 CallTrackingMetrics は、サイトに配置される JavaScript を使用して、 [!DNL Marketo Measure] cookie. この「[!DNL BizibleId]」が CallTrackingMetrics によって保存されます。

訪問者がサイトに来訪して電話をかけると、そのデータをにプッシュするのは CallTrackingMetrics の役割です。 [!DNL Salesforce].  通常、 [!DNL Salesforce Task] は、電話番号、件名、タイプなどのデータを入力するために作成されます。 [!DNL BizibleId]

The [!DNL BizibleId] は、バージョン 6.7 以降の [!DNL Marketo Measure] マーケティング属性パッケージ。

以下は、 [!DNL BizibleId] が設定されている。

![](assets/3.png)

条件 [!DNL Marketo Measure] 既知の [!DNL BizibleId] 値が入力されました。 [!DNL Marketo Measure] は、同じ [!DNL BizibleId] とは、そのセッションを web 訪問ではなく電話呼び出しに関連付けます。

## タッチポイント {#the-touchpoint}

条件 [!DNL Marketo Measure] タスクをインポート/ダウンロードできるので、Web セッションと共にその詳細を処理します。 通常、リファラーまたは広告と結合できます。 次の例では、訪問者が有料Google広告を通じてビジネスを見つけ、電話をかけました。

The [!UICONTROL タッチポイント] 上のスクリーンショットから「Call」と入力すると、タスクから取り出されます。この値は、タスクの作成時に CallTrackingMetrics によっても設定されます。

![](assets/4.png)

## レポート {#reporting}

タッチポイントタイプの値 [!DNL Marketo Measure] 通常、プッシュは Web 訪問、Web フォームまたは Web チャットですが、CallTrackingMetrics タッチポイントの場合、タッチポイントのタイプは電話呼び出しです。 これにより、マーケターは、最も多くの電話に出回っているチャネルを確認し、組織の売上高を生み出すことができます。

![](assets/5.png)

## よくある質問 {#faq}

**タッチポイントタイプの Web 訪問が発生するのはなぜですか？**

タッチポイントタイプは、Task.Type フィールドから設定されます。 Task.Type フィールドが空白の場合、 [!DNL Marketo Measure] は、タッチポイントタイプを自動的に「Web 訪問」に設定します。 Task.Type フィールドに値が入力されると、 [!DNL Marketo Measure] はその値を読み取り、それに応じてタッチポイントタイプを設定します。

**タッチポイントは電話の呼び出しから他にどのようなフィールドに入力されますか？**

タッチポイントタイプとメディアの両方に、Task.Type から取り込まれたデータが含まれます。 その他すべてのデータポイントは、Web トラッキングと JavaScript データから取得されます。

**この電話が Web セッションに結び付けられていないのはなぜですか？**

まず、「タスク」をチェックして、 [!DNL BizibleId] が設定されている。 値がない場合、そのタッチポイントを作成できません。 これは、CallTrackingMetrics でエスカレーションする必要があります。

値がある場合、すべての Web セッションは 30 分と見なされるだけです。 Google Ad が午後 12:17（Web サイトのセッションの開始）にクリックされたが、電話が午後 1:05 まで発生しなかった場合、Web セッションと電話の呼び出しは結合されません。 むしろ [!DNL Marketo Measure] 別のを作成 [!DNL Salesforce Task] 電話の呼び出しを追跡するタッチポイントですが、web セッションデータは持ちません。

![](assets/6.png)

## パートナーシップ {#partnerships}

[!DNL Marketo Measure] 現在、当社との「公式」統合プロセスを経て、コマーケティングおよび製品トレーニングを含む、正式なコールトラッキングパートナーが 1 人います。 この 1 つのパートナーは CallTrackingMetrics です。
