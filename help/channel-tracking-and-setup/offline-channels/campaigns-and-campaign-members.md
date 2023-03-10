---
unique-page-id: 18874578
description: キャンペーンとキャンペーンメンバー — [!DNL Marketo Measure]  — 製品ドキュメント
title: キャンペーンとキャンペーンメンバー
exl-id: e4e2b154-39ac-4295-a541-7fa6112672e3
source-git-commit: 65e7f8bc198ceba2f873ded23c94601080ad0546
workflow-type: tm+mt
source-wordcount: '1172'
ht-degree: 0%

---

# キャンペーンとキャンペーンメンバー {#campaigns-and-campaign-members}

[!DNL Salesforce] キャンペーンは、マーケティングプログラムまたはアクティビティに関連付けられたリードと連絡先のリストを追跡するためのものです。 これは、一般的にウェビナー、登録、ブース訪問などです。 マーケターは、キャンペーンにタッチポイントジャーニーでクレジットを付与するかどうかを選択できます。

## タッチポイントの有効化 {#enabling-touchpoints}

この [!DNL Marketo Measure] [!DNL Salesforce] パッケージには、Campaign オブジェクト上の「購入者タッチポイントを有効にする」というラベルの付いたフィールドが含まれます。 フィールドがページレイアウトに追加されると、次のように表示されます。

![](assets/1.png)

選択リストで使用できるオプションは次のとおりです。

![](assets/2.png)

* すべてのキャンペーンメンバーを含める — キャンペーンに追加されたすべてのリードまたは連絡先に、そのキャンペーンに関連するタッチポイントが割り当てられます。
* 「応答済み」キャンペーンメンバーのみを含める — キャンペーンメンバーステータスが「応答済み」のリードまたは連絡先のみが、そのキャンペーンに関連するタッチポイントを受け取ります。
* すべてのキャンペーンメンバーを除外 — リードまたは連絡先に、そのキャンペーンに関連付けられたタッチポイントが送信されません。

次の条件を満たすには、キャンペーンメンバーのレコードに E メールアドレスが関連付けられている必要があります。 [!DNL Marketo Measure] タッチポイントを作成します。 E メールアドレスがない場合、 [!DNL Marketo Measure] は、キャンペーンメンバーにタッチポイントを割り当てません。

## キャンペーン同期日 {#campaign-sync-dates}

パッケージのインストールで、 [!DNL Marketo Measure] また、Campaign オブジェクトに次の 2 つの日付フィールドが含まれます。タッチポイントの開始日とタッチポイントの終了日です。

これらの日付は、 [!DNL Marketo Measure] キャンペーンメンバーをキャンペーンからタッチポイントジャーニーに含めるのを開始または停止するタイミング。 1 つの日付を設定するか、両方を設定するか、まったく設定しないかを指定できます。

## タッチポイントの開始日の使用例 {#use-case-for-touchpoint-start-date}

リードと連絡先の追跡に既存のキャンペーンを使用している場合でも、ユーザーが新しいシステムまたはプロセスが導入された後にのみ測定を開始したいと考えた場合に、開始日を 1 回設定することにしました [!DNL Marketo Measure] が、これらのキャンペーンメンバーの追跡を開始する必要があります。

## タッチポイント終了日の使用例 {#use-case-for-touchpoint-end-date}

を使用する前に [!DNL Marketo Measure]では、リードのデジタルインタラクション（IE フォーム送信）を追跡するマーケティングオートメーションプラットフォームを使用し、これらのリードを [!DNL Saleforce] キャンペーンでは、「タッチポイントの終了日」フィールドを利用できます。 タッチポイント終了日を開始日として設定しているのは、 [!DNL Marketo Measure] 「購入者のタッチポイント」を有効にすると、これらの各リードのデジタルインタラクションがタッチポイントとして作成されます。 タッチポイントの終了日を開始日に設定する理由は、 [!DNL Marketo Measure] は、今後、javascript を使用してこれらのデジタルインタラクションを追跡するからです。

![](assets/3.png)

## キャンペーンメンバー {#campaign-members}

キャンペーンメンバーは、の下にネストされます [!UICONTROL キャンペーン]、およびはリードまたは連絡先に関連しています。 リードまたは連絡先は 1 回のみキャンペーンに追加できます。キャンペーンの使用事例によっては、問題になる場合があります。 キャンペーンを同期すると、キャンペーンのメンバーシップがマーケティングアクティビティとして使用され、タッチポイントジャーニーに組み込まれ、フォームの入力のように処理されます。

## 購入者タッチポイントのステータス {#buyer-touchpoint-status}

有効な場合、 [!DNL Marketo Measure] は、インストールされたパッケージに含まれる 4 つの異なるフィールドにわたって、ステータス値をキャンペーンメンバーにプッシュします。タッチポイントステータス（リード）、タッチポイントステータス（連絡先）、タッチポイントステータス（商談）およびタッチポイントステータス日です。 これは、タッチポイントが関連するオブジェクトに応じて、バイヤータッチポイントまたはバイヤー属性タッチポイントとして作成されたかどうかを監査するのに役立ちます。 タッチポイントステータス日は、キャンペーンメンバーでステータスが更新された最後の日付です。

![](assets/4.png)

## 購入者タッチポイント日 {#buyer-touchpoint-date}

パッケージのインストールで、 [!DNL Marketo Measure] また、キャンペーンメンバーの「Buyer Touchpoint Date」というラベルの付いたフィールドも含まれます。 これにより、 [!DNL Marketo Measure] タッチポイントレコードのタッチポイント日にを使用します。

これは、イベントが実際に発生してから数日、数週、数ヶ月後にリストがアップロードされた場合に必要になる場合があります。 すべてのレコードを一度に更新する方法があります。以下に説明します。

![](assets/5.png)

購入者タッチポイント日を使用する必要があるかどうかを知るには、次のようにして日付が次のように決定されます。 [!DNL Marketo Measure] 次に応じて： [!UICONTROL 同期タイプ] がキャンペーン用に選択されている

この [!UICONTROL 同期タイプ] が「すべてのキャンペーンメンバーを含める」に設定されている場合、タッチポイント日付は上から下に順に設定されます。

* 購入者タッチポイント日
* キャンペーンメンバー作成日

この [!UICONTROL 同期タイプ] が「応答済みのキャンペーンメンバーのみを含める」に設定されている場合、タッチポイントの日付は上から下に順に設定されます。

* 購入者タッチポイント日
* 最初の応答日
   * 最初の応答日は、ステータスが「応答済み」に変更されるとすぐに自動的に設定され、標準です [!DNL Salesforce] 変更できないフィールド

* キャンペーンメンバー作成日

## タッチポイント日の一括更新 {#bulk-update-touchpoint-date}

一括更新タッチポイント日は、インストールされている [!DNL Marketo Measure] [!DNL Salesforce] パッケージとボタンをページレイアウトに追加する必要があります。

![](assets/6.png)

多数のキャンペーンメンバーレコードを更新する必要がある場合は、 [!UICONTROL タッチポイント日の一括更新] ボタンをクリックして一括編集を行います。

このインターフェイスで扱われない一意の使用例がある場合は、 [データローダー](https://dataloader.io/){target="_blank"} レコードをエクスポートするには、変更を加え、レコードを再度アップロードします。

まず、レコードを検索し、購入者タッチポイント日付を設定するレコードをフィルタリングします。

>[!CAUTION]
>
>動作しない検索が 1 つあります。これは、次の例で表示されます。 UI では、null の購入者タッチポイント日の検索はサポートされていません（以下の検索は機能しません）。

![](assets/7.png)

検索を使用する必要がなく、すべてのキャンペーンメンバーレコードに日付を適用するだけの場合は、[!UICONTROL すべてのレコードを含める]「 」チェックボックス（下のスクリーンショットを参照）。これにより、すべてのページのすべてのレコードがチェックされます。

カレンダーピッカーから日時を選択します。 現在の日時を選択する場合は、カレンダーピッカーの横に表示される日時をクリックします。

日時を設定したら、 **[!UICONTROL 選択したレコードを更新]** ボタンをクリックして、変更を適用します。

![](assets/8.png)

## キャンペーンコスト {#campaign-costs}

キャンペーンコストのすべてを表示 [この記事では、](/help/marketing-spend/spend-management/crm-campaign-costs.md).

## キャンペーンメンバーの削除 {#campaign-member-removal}

この方法は [!DNL Marketo Measure] は、削除されたリード、アカウント、商談のどれが API でそれらのレコードを表示し、エントリが「IsDeleted」とマークされているかを追跡するために、Salesforce 内の削除されたレコードを保持します。 残念ながら、Salesforce はキャンペーンメンバーからこれらのキャンペーンメンバーを削除する別の方法を導入し、実際には「削除済み」とは異なり「削除済み」とマークされているので、削除されたキャンペーンメンバーに関連する Salesforce にタッチポイントがまだ存在していました。

この問題を回避するには、 [!DNL Marketo Measure] 作成済み [!DNL Marketo Measure] Campaign メンバーが削除され、対応するタッチポイントが削除された場合に追跡する履歴オブジェクトおよびトリガー。 **必要になる [!DNL Marketo Measure] マーケティング分析パッケージ V6.15 以降** この機能を使用するには、をクリックします。

>[!CAUTION]
>
>このトリガーは、過去に削除されたキャンペーンメンバーを追跡しないので、先に進むだけであることに注意してください。 過去のキャンペーンメンバーのタッチポイントを多数削除する必要がある場合は、 [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.

>[!MORELIKETHIS]
>
>[[!DNL Marketo Measure] 大学：Campaign オブジェクトのフィールド](https://universityonline.marketo.com/courses/bizible-fundamentals-channel-management/#/page/5c63007334d9f0367662b758)
>
>[[!DNL Marketo Measure] 大学：オフラインチャネルのマッピング](https://universityonline.marketo.com/courses/bizible-fundamentals-channel-management/#/page/5c630eca34d9f0367662b77f)
