---
unique-page-id: 42762729
description: '"[!DNL Marketo Engage] プログラム統合 — [!DNL Marketo Measure]  — 製品ドキュメント»'
title: '"[!DNL Marketo Engage] プログラム統合»'
exl-id: c26087e3-d821-4fe7-bacd-eeaa1530a4b0
source-git-commit: 54337a0a65b79d80ebeae6531f5e92f4f48721a7
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 1%

---

# [!DNL Marketo Engage] プログラム統合 {#marketo-engage-programs-integration}

を通じて [!DNL Marketo Measure] ～との統合 [!DNL Marketo Engage] プログラム、お客様は、Marketoプログラムメンバーシップから、アトリビューショントラッキング用のタッチポイントを作成できます。 この機能を使用すると、マーケターは、メールまたはエンゲージメントプログラムから、他の方法では見られないメールまたはエンゲージメントプログラムからプログラムメンバーシップの追跡を開始できます [!DNL Marketo Measure] javascript とは、アトリビューションジャーニー内で測定される必要があります。

## 利用可能性 {#availability}

すべての層。

## 要件 {#requirements}

* 実稼動Marketoインスタンス
* 実稼動 Salesforce またはMicrosoft Dynamics インスタンス
* 任意の有料 [!DNL Marketo Measure] 購読
* Marketo担当者同期が有効 ([!DNL Marketo Measure] 設定 )
* Marketoプログラム有効 ([!DNL Marketo Measure] 設定 )

## セットアップ {#setup}

**ルール**

1. Marketoプログラムのルールの設定を開始するには、に移動します。 **[!UICONTROL マイアカウント]** > **[!UICONTROL 設定]** > **[!UICONTROL プログラム]**. 次をクリック： **+** アイコンをクリックして最初のルールの作成を開始します。

   ![](assets/one.png)

   ![](assets/two.png)

1. ルールの名前は、追跡に役立つ場合は、オプションで設定できます。 最初に、「プログラム」フィールドと「プログラムメンバーシップ」フィールドのリストからルールを定義するフィールドを選択します。 引き続き、確認する演算子と期待値を選択してルールを作成します。

   ![](assets/three.png)

1. 同じボックス内に別の文を追加して、ルール内に「and」条件を設定するか、ボックスの外側にある+アイコンをクリックして「or」文を設定します。

   ![](assets/four.png)

1. タッチポイント日付へのマッピングに使用する日付または日付/時間フィールドを選択します。 Marketoで使用可能な値のリストを表示するには、中括弧を入力します `{` 使用可能なフィールドを表示します。

   ![](assets/five.png)

   >[!NOTE]
   >
   >ルールでアクティビティの日付、またはプログラムメンバーが特定のステータスに達した日付を取り込む場合、 [!DNL Marketo Engage] アクティビティ統合を参照し、「進行状況のステータスを変更」アクティビティタイプのルールを設定します。

   ![](assets/six.png)

完了したルールは次のようになります。

## テスト {#test}

いくつかのルールを作成した後は、そのルールをテストして、文がプログラムと一致することを確認することができます。

1. テストを実行するには、 **[!UICONTROL テスト]** 」ボタンをクリックします。

   ![](assets/seven.png)

1. モーダルが表示され、Marketoのプログラム ID にを入力できます。

   ![](assets/eight.png)

   ID を入力し、 [!UICONTROL テスト] ボタンをクリックすると、各ルールが処理され、プログラムがルールに適合するかどうかが判断されます。 次の例では、Program 1002( [!DNL Marketo Measure] Ebook は、5 つのプログラムメンバーを持ち、表示されるルールのために適格です。

   ルールは、サンプルサイズが 5,000 メンバーの場合に実行されます。 プログラムに 5,000 を超えるメンバーが含まれている場合、すべてのメンバーの互換性がチェックされない可能性があります。 このツールは、単に、ルールが正しく構築されているかどうかを確認する方法の 1 つです。

   ![](assets/nine.png)

   「メンバー数」をクリックすると、プログラム内で適格なMarketo People ID のリストが表示されます。

   ![](assets/ten.png)

## チャネルマッピング {#channel-mapping}

Marketoプログラムチャネルのリストから、 [!DNL Marketo Measure] 設定内で作成したカスタムマーケティングチャネル。 これらのプログラムで生成されるタッチポイントは、ここで選択したチャネル名とサブチャネル名を継承します。

1. 最初に、 **[!UICONTROL マイアカウント]** > **[!UICONTROL 設定]** > **[!UICONTROL オフラインチャネル]**.

1. 上部には、CRM キャンペーンタイプにマッピングするオプションがあり、下部には、Marketoプログラムチャネルのオプションが表示されます。

1. まず、値にマッピングするチャネルを選択し、次にオプションでサブチャネルを選択します。 完了したら、「 **[!UICONTROL 保存]** 下に

   ![](assets/eleven.png)

## プログラムコスト {#program-costs}

Marketoプログラムのデータインポートを通じて、コストが期間原価から自動的にダウンロードされ、Marketoで報告されたコストが割り当てられた月を通じて配分されます。 例えば、2021 年 1 月に$1000 がレポートされる場合、$1000 は 31 日間に分割されます。 費用は、 [!DNL Marketo Measure Discover].

## 仕組み {#how-it-works}

**フィールドマッピング**

<table> 
 <colgroup> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <th>biz_ad_campaigns</th> 
   <th>Marketo</th> 
  </tr> 
  <tr> 
   <td>ID</td> 
   <td>ID</td> 
  </tr> 
  <tr> 
   <td>IS_DELETED</td> 
   <td>（プログラムが API 経由でまだ存在するかどうかを確認）</td> 
  </tr> 
  <tr> 
   <td><p>名前</p></td> 
   <td>名前</td> 
  </tr> 
 </tbody> 
</table>

| biz_campaign_members | Marketo |
|---|---|
| ID | &quot;MarketoProgramMembership&quot;_ProgramId_Lead Id |
| MODIFIED_DATE | updatedAt |
| CREATED_DATE | membershipDate |
| LEAD_ID | ID （リストのメンバーシップ） |
| LEAD_EMAIL | E メール（リストのメンバーシップ） |
| ステータス | progressionStatus |
| HAS_RESPONDED | reachedStatus |
| CAMPAIGN_NAME | programName |
| CAMPAIGN_ID | programId |
| CAMPAIGN_TYPE | チャネル |

## Cookie マッピング {#cookie-mapping}

結果として [!DNL Marketo Measure] Marketo、 [!DNL Marketo Measure] cookie ID もマッピングされ、 [!DNL Marketo Munchkin Id]. これにより、FT タッチと LC タッチの両方をMarketo Activity に関連付けるのではなく、匿名のファーストタッチを Web セッションに関連付けるのに役立ちます。 次のシナリオを想像してください。

次の項目のクリック数のマーク [!DNL Facebook] 広告を追加して wayneenterprises.com に移動し、でクッキーを取得します。 [!DNL Marketo Measure] ID 123 および [!DNL Marketo Munchkin Id] 456. フォームの入力は行われません。

Wayne Enterprises マーケティングチームが、特定のターゲットリードに E メールの一斉送信を送信します。そのうちの 1 つは、 `mark@email.com`.

`mark@email.com` が電子メールを受信し、をクリックスルーして wayneenterprises.com にランディングします。 これは `mark@email.com's` ～への 2 回目の訪問 `wayneenterprise.com` 同じ cookie ID を持つものの、フォームの入力が行われていない場合、 [!DNL Marketo Measure]に値を付けると、その訪問者は匿名の訪問者となります。

Wayne Enterprises マーケティングチームは、「E メールのクリック」アクティビティタイプのタッチポイントを生成するMarketoアクティビティルールを作成します。

今日の実装では、 `mark@email.com` 「E メールをクリック」アクティビティタイプの「Marketoアクティビティ」から。

この cookie マッピング機能の強化により、FT はに戻り、 [!DNL Facebook] 広告と LC が E メールに与えられます。

>[!NOTE]
>
>cookie マッピング動作では、Web 訪問から取得された LC タッチポイントが見つかる場合があります。 関連付けられたアクティビティなしでMarketoにリードが表示された可能性があります。 [!DNL Marketo Measure] そのリードをダウンロードし、関連する cookie と一致し、リードを作成したフォームアクティビティがない場合でも、最新の web セッションまでトレースしました。

## よくある質問 {#faq}

**タッチポイント日をプログラムメンバーに対して、進行日または状態変更が発生した日付に設定する方法を教えてください。**

ルールでアクティビティの日付、またはプログラムメンバーが特定のステータスに達した日付を取り込む場合、 [!DNL Marketo Engage] アクティビティ統合を参照し、「進行状況のステータスを変更」アクティビティタイプのルールを設定します。 それ以外の場合は、 [!DNL Marketo Engage] プログラム統合では、複数のステータスがある場合でも、メンバーシップの日付 (Marketoの担当者をプログラムに導いた最初の日付 ) のみが使用可能になります。

**タッチポイント日付の日付オプションの選択リストを取得できますか？**

オートコンプリートをトリガーするには、中括弧を入力して開始します `{` テキストフィールドに、使用可能なフィールドが表示されます。

**Marketoプログラムルールを作成し、CRM キャンペーンルールも設定している場合、2 回カウントされますか。**

ルールの定義によって異なりますが、可能性はあります。 類似のメンバーシップの重複を排除または検出しないため、プログラムおよびキャンペーンを対象とするルールがないように、ルールセットを評価する必要があります。 解決策の 1 つは、Marketoを信頼できる唯一の情報源にしたい場合に、キャンペーンルールをプログラムにコピーし、キャンペーンルールを削除することです。 別のオプションとして、「CreatedOn」または「CreatedDate」条件をルールに追加し、特定の日付より前のルールでキャンペーンルールと特定の日付より後のルールでプログラムルールが使用されるようにします。 多くの回避策がありますが、計画と調整が必要になります。

**Marketoプログラムメンバーシップカスタムフィールドを定義できますか？**

技術上の制限により、現時点ではプログラムメンバーシップカスタムフィールドをサポートできません。 追加のMarketo API でこれらのフィールドが利用可能になると、アドビに公開され、使用できるようになります。

**プログラムとアクティビティのどちらを使用すればよいかを知るにはどうすればよいですか？**

この [!DNL Marketo Engage] プログラム統合は、個人がプログラムのプログラムメンバーかどうかに基づいてタッチポイントを生成する簡単な方法です。 個人が特定のプログラムステータスに変わる時間に基づいてルールを定義する場合、 [!DNL Marketo Engage] アクティビティ統合は、お客様が必要とする設定となります。特に、「進行状況のステータス変更」アクティビティタイプです。
