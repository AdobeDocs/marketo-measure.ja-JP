---
unique-page-id: 18874600
description: オフラインキャンペーンの同期 — [!DNL Marketo Measure]
title: オフラインキャンペーンの同期
exl-id: a6f9e217-ff6e-474d-9f14-c6f6238c9e84
feature: Channels
source-git-commit: b84909fbb34a1d8f739ebeea3400ef8816e17d32
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# オフラインキャンペーンの同期 {#syncing-offline-campaigns}

オフラインキャンペーンを正確に追跡し、それらをデジタルマーケティング活動と比較する方法を理解するのは困難な場合があります。 [!DNL Marketo Measure] では、 [!DNL Salesforce]( 場合によっては [!DNL Salesforce] キャンペーンは、イベントの数週間後まで作成されません。

>[!NOTE]
>
>この記事では、古いプロセスについて説明します。 ユーザーには、 [新しく改善されたアプリ内プロセス](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md){target="_blank"}.

## 同期前 {#before-you-sync}

以下に、効率的な同期プロセスのヒントを示します。

* オフラインキャンペーンとは、オンラインで発生しないマーケティングインタラクションを指します。 これには、イベント、ウェビナー、トレードショーなどのマーケティングチャネルが含まれます。 オフラインマーケティングキャンペーンのみを含めます。
* をインストールする前に、オンラインアクティビティを追跡したキャンペーンを含める場合。 [!DNL Marketo Measure]タッチポイントの終了日は、JavaScript がサイトにデプロイされた日付として必ず設定してください。
* これは、 [!DNL Marketo Measure] アプリをオフラインチャネルページで開き、様々なキャンペーンタイプや、タッチポイントの分類先となるマーケティングチャネルを簡単に識別できるようにします。

* 「[!UICONTROL 保存]&quot;ボタン！

## タッチポイント日の一括更新 {#bulk-update-touchpoint-date}

In [!DNL Salesforce]に設定されている場合、キャンペーンメンバーオブジェクトの「作成日」フィールドに、キャンペーンメンバーがキャンペーンに追加された日付が記録されます。 同期処理をスムーズに進めるには、Buyer Touchpoint Date Field の日付が Salesforce Campaign メンバーオブジェクトの日付と同じ日付であることを確認します。 この手順は、「[!UICONTROL タッチポイント日付の一括更新ボタン],&quot; _前_ 次を選択します。 [!UICONTROL 候補リスト] 「 Enable Buyer Touchpoints 」フィールドのオプションを使用します。

なぜこれが重要なのか？ 1 月の会議であなたの会社がブースをスポンサーした瞬間を想像してみてください。 会議では、100 人の個人が製品に対する関心を示し、メールの更新を受け取るための連絡先情報を提供しました。 3 週間後、最終的に [!DNL Salesforce] 会議の結果を追跡する。

アップロード日は、会議日より 3 週間後になります。 この違いを修正するには、 [!UICONTROL タッチポイント日の一括更新] ボタンを使用して、適切な日付を設定できます。 ボタンは下の画像に示されています。

![](assets/1-3.png)

この場合、3 週間分のアップロード日をバックフィルします。 この手順は、[!UICONTROL 購入者タッチポイントの有効化]」フィールドに値を入力します。

要約すると、 [!UICONTROL タッチポイント日の一括更新] ボタンをクリックし、タッチポイントの日付をイベントの日付に変更します。 [!DNL Marketo Measure] は、アップロード日ではなく、イベントの実際の日付のタッチポイントを生成します。

また、既存のキャンペーンのすべてのキャンペーンメンバーの日付を更新することもできます。 その際は、タッチポイントの日付が、メンバーのインタラクションの日付であることを確認してください。 「一括更新購入者タッチポイント日」をクリックし、必要に応じてキャンペーンメンバーのリストをフィルターし、「[!UICONTROL 日付を選択]「キャンペーンメンバーのリストの上にあるオプションで、イベントが発生した日付と同じ日付を追加します。

>[!CAUTION]
>
>タッチポイントの日付を必ず更新してください _前_ すべてのキャンペーンメンバーに対してタッチポイントを有効にします。

![](assets/2-3.png)

## キャンペーンの作成方法と購入者のタッチポイントの同期方法 {#how-to-create-a-campaign-and-sync-buyer-touchpoints}

でキャンペーンを作成するには、以下を実行します。 [!DNL Salesforce]をクリックし、 [!UICONTROL キャンペーン] タブで「 」を選択します。[!UICONTROL 新規]」と表示されます。 次の条件に応じて、 [!DNL Salesforce] セットアップ時に、プラス (+) アイコンをクリックして、上部のバーにキャンペーンを追加する必要がある場合があります。

![](assets/3-3.png)

このキャンペーンを作成する際に、「[!UICONTROL 購入者タッチポイントの有効化]」フィールドで選択し、選択リストから次のいずれかのオプションを選択します。

![](assets/4-3.png)

* **すべてのキャンペーンメンバーを含める**
   * このオプションは、 [!DNL Marketo Measure] タッチポイントを各キャンペーンメンバーに関連付けます。

* **「応答済み」キャンペーンメンバーを含めます。**
   * このオプションは、「応答済み」ステータスのキャンペーンメンバーにタッチポイントを適用します。

* **すべてのキャンペーンメンバーを除外します。**
   * このオプションは、タッチポイントをキャンペーン内のメンバーに関連付けず、キャンペーンが意図的に除外されたフラグとして機能します。 [!DNL Marketo Measure]. 誤ってキャンペーンを購入者タッチポイントと同期した場合は、ステータスを「すべてのキャンペーンメンバーを除外」に変更すると、タッチポイントが削除されます。

これらの選択の 1 つを選択したら、 [!DNL Marketo Measure] 該当する場合は、各キャンペーンメンバーにタッチポイントを割り当てます。 キャンペーンに追加されたリードまたは連絡先 _必須_ ～のためにレコードにメールアドレスを関連付ける [!DNL Marketo Measure] タッチポイントを作成します。 E メールアドレスがない場合、 [!DNL Marketo Measure] は、キャンペーンメンバーにタッチポイントを割り当てません。

>[!MORELIKETHIS]
>
>[[!DNL Marketo Measure] Tutorials：オフラインチャネルのマッピング](https://experienceleague.adobe.com/en/docs/marketo-measure-learn/tutorials/onboarding/marketo-measure-salesforce/mapping-offline-channels){target="_blank"}
>
>[[!DNL Marketo Measure] Tutorials:Campaign オブジェクトのフィールド](https://experienceleague.adobe.com/en/docs/marketo-measure-learn/tutorials/onboarding/marketo-measure-salesforce/campaign-object-fields){target="_blank"}
