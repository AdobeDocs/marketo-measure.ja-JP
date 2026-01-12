---
description: コールトラッキングの統合 –  [!DNL Marketo Measure]
title: コールトラッキングの統合
exl-id: bc35a789-e056-4456-9038-306ed34c2a8e
feature: Tracking, Integration
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 1%

---


# コールトラッキングの統合 {#call-tracking-integration}

[!DNL CallTrackingMetrics] との統合は、web セッションと電話を結合することを目的としています。 電話は、[!DNL Marketo Measure] へのフォーム送信として扱われます。 実際のフォーム送信がなかったので、web 訪問とみなされるだけだった web セッションにクレジットを与えます。

## コールトラッキング {#call-tracking-explained}

一般的な意味での「コールトラッキング」は、[!DNL CallTrackingMetrics]、[!DNL DiaglogTech]、[!DNL Invoca]、[!DNL CallRail] などの企業の製品です。 一意の電話番号は、送信元の様々なマーケティングチャネルやキャンペーンに基づいてユーザーに表示されます。 これにより、マーケターは、これらのチャネルやキャンペーンのパフォーマンスを確認できます。

![ 様々なマーケティングチャネルおよびキャンペーンに基づいて表示された一意の電話番号を示す図 ](assets/1.png)

## 前後 {#before-and-after}

CallTrackingMetrics との統合を行わずに [!DNL Marketo Measure] が電話の呼び出しを処理する方法については、以下のフローチャートを参照してください。 発生した電話は追跡されなかったので、web セッションと見なされ、タッチポイントは作成されませんでした。 ユーザーがフォームを完了した次の訪問まで、タッチポイントは最終的に入力されませんでした。

この統合により、web セッションが実際に通話に結び付けられていることがわかります。 次のフォーム入力は最終的に PostLC タッチになり、まだジャーニーの一環として追跡されています。

![CallTrackingMetrics 統合を使用した、およびを使用した通話トラッキングを比較する前後のフローチャート ](assets/2.png)

## 仕組み {#how-it-works}

CallTrackingMetrics は、これを機能させるために、開発作業を行う必要があります。 サイトにJavaScriptを配置すると、CallTrackingMetrics は [!DNL Marketo Measure] Cookie から_biz_uid を取得できます。 この「[!DNL BizibleId]」は、CallTrackingMetrics によって保存されます。

訪問者がサイトを訪れて電話をかけると、そのデータを [!DNL Salesforce] にプッシュするのが CallTrackingMetrics の仕事です。  通常、電話番号、件名、タイプなどのデータを入力する [!DNL Salesforce Task] ールが作成され、[!DNL BizibleId] が表示されるようになりました

[!DNL BizibleId] は、[!DNL Marketo Measure] Marketing Attribution パッケージのバージョン 6.7 以降と共にインストールされるフィールドです。

次に、[!DNL BizibleId] が入力されたタスクレコードの例を示します。

![ 値が設定された BizibleId フィールドを示しているSalesforce タスクレコードの例 ](assets/3.png)

[!DNL Marketo Measure] が既知の [!DNL BizibleId] 値が入力されている Task レコードを見つけ [!DNL Marketo Measure] と、そのユーザーを同じ [!DNL BizibleId] を持つ web セッションにマッピングし、そのセッションを web 訪問ではなく通話に関連付けることができます。

## タッチポイント {#the-touchpoint}

タスク [!DNL Marketo Measure] インポート/ダウンロードできる場合、その詳細を web セッションと共に処理します。 通常は、リファラーまたは広告と結合できます。 次の例では、訪問者が有料Google広告からビジネスを見つけ、電話をかけました。

[!UICONTROL  タッチポイント ] タイプ「呼び出し」は、上記のスクリーンショットからタスクから取得されます。また、このスクリーンショットは、タスクの作成時に CallTrackingMetrics によって入力されます。

![ 結合された web セッションと通話データからの通話としてタイプを示すタッチポイントレコード ](assets/4.png)

## レポート {#reporting}

タッチポイントタイプの値 [!DNL Marketo Measure]、通常、Web 訪問、Web フォームまたは Web チャットですが、CallTrackingMetrics タッチポイントの場合、タッチポイントタイプは Phone Call です。 これにより、マーケターは、どのチャネルが最も多くの電話で引き込まれるのかを確認し、組織の収益を生み出すのに役立ちます。

![ チャネル別の呼び出し生成収益を追跡するための電話を含む、タッチポイントタイプを示すレポート ](assets/5.png)

## よくある質問 {#faq}

**タッチポイントタイプの web 訪問はなぜですか？**

タッチポイントタイプは、Task.Type フィールドから入力されます。 Task.Type フィールドが空白の場 [!DNL Marketo Measure]、タッチポイントタイプが Web 訪問として自動的に設定されます。 Task.Type フィールドに値が入力されると [!DNL Marketo Measure] その値が読み取られ、それに応じてタッチポイントタイプが入力されます。

**タッチポイントは電話から他にどのようなフィールドを入力しますか？**

タッチポイントタイプとMediumの両方に、Task.Type から取り込まれたデータが含まれています。 その他のすべてのデータポイントは、web トラッキングと Javascript データから取り込まれます。

**この電話が web セッションに結び付けられないのはなぜですか？**

まず、タスクをチェックして、[!DNL BizibleId] が入力されていることを確認します。 値がない場合、そのタッチポイントを作成することはできません。 これは CallTrackingMetrics でエスカレーションする必要があります。

値がある場合、すべての web セッションは 30 分と見なされることに注意してください。 Google広告が 12:17pm （Web サイトでのセッションの開始）でクリックされたが、1:05pm まで通話が発生しなかった場合、Web セッションと通話は結合されません。 代わりに、[!DNL Marketo Measure] は電話を追跡するための個別の [!DNL Salesforce Task] タッチポイントを作成しますが、web セッションデータは持ちません。

![ 広告クリックから電話までの間に 30 分の web セッションタイムアウトウィンドウを示す図 ](assets/6.png)

## パートナーシップ {#partnerships}

[!DNL Marketo Measure] には現在、共同マーケティングや製品トレーニングを含む「公式」統合プロセスを経た 1 つの公式コールトラッキングパートナーがあります。 この 1 つのパートナーは CallTrackingMetrics です。
