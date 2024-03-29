---
unique-page-id: 42762648
description: コホートジャーニーダッシュボードドキュメント — [!DNL Marketo Measure]
title: コホートジャーニーダッシュボードドキュメント
exl-id: b139f720-86ae-4f6d-9dfc-cc67b4186f88
feature: Reporting
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 1%

---

# コホートジャーニーダッシュボードドキュメント {#cohort-journey-dashboard-documentation}

コホートインパクトとファネルのダッシュボードを使用すると、マーケターは、選択した期間におけるコホートの開始ステージからの進行状況を表示し、コンバージョン率を測定できます。

主な違いは、コホートステージから各エンティティをカウントする方法です。

* コホートファネル：各ステージの結果は、前のステージから直接導き出されます。

   * 設定されたコホート開始時間の後にファネルの各ステージを下回ったレコードのみがカウントされます。

![](assets/cohort-journey-dashboard-documentation-1.png)

* コホートの影響：各ステージの結果は、前のステージではなく、コホートステージから導き出されます。

   * 設定されたコホート開始時間の後に発生した限り、各ステージのすべてのレコードがカウントされます。 このダッシュボードには、ファネルを通る動きだけでなく、コホートステージからのエンティティの影響を調べるので、当然、ファネルダッシュボードよりも多くのレコードが含まれます。

![](assets/cohort-journey-dashboard-documentation-2.png)

各ダッシュボードには次の 2 つのタイルがあります。

* コホート売上高：コホートジャーニータイルの「掘り出し物」ステージにあるすべての商談からの合計商談額。
* コホートジャーニー：選択した期間の、開始コホートステージから各ジャーニーステージへの進行。

>[!NOTE]
>
>すべての Discover ダッシュボードで、リードまたは連絡先のいずれか 1 つの担当者オブジェクトのみをレポートできます。 これは、 [!UICONTROL 設定] > [!UICONTROL レポート] > [!UICONTROL 属性設定] > [!UICONTROL デフォルトのダッシュボードオブジェクト].

ダッシュボードは、次のフィルターをサポートしています。

* コホートステージ：開始コホートステージを選択します。 次のすべてのステージのレコードは、コホートステージのレコードから進化します。
* コホート日付範囲：選択したコホートステージの期間を選択します。 コホートステージと共に、開始データセットを定義します。
* 期限日：次のすべての段階でレコードの進行を行う必要がある日付を選択します。 デフォルトは今日です。 これは、コホートステージ以外のすべてのステージに適用されます。
* チャネル：チャネルでレコードをフィルターします。 レコードのタッチポイントの 1 つがチャネルに関連付けられている場合、そのレコードはチャネルに関連付けられます。
* サブチャネル：サブチャネルでレコードをフィルターします。 レコードのタッチポイントのいずれかがサブチャネルに関連付けられている場合、そのレコードはサブチャネルに関連付けられます。
* キャンペーン：キャンペーンでレコードをフィルターします。 レコードのタッチポイントがキャンペーンに関連付けられている場合、そのレコードはキャンペーンに関連付けられます。
* キャンペーンのソース：キャンペーンのソースでレコードをフィルタリングします。 以下にキャンペーンソースの例を示します。 [!DNL Adwords], [!DNL BingAds], [!DNL Facebook], [!DNL LinkedIn]など レコードのタッチポイントのいずれかがキャンペーンソースに関連付けられている場合、そのレコードはキャンペーンソースに関連付けられます。
* セグメントフィルター：カスタムセグメントでレコードをフィルターします。 レコードのタッチポイントのいずれかがセグメントに関連付けられている場合、そのレコードはセグメントに関連付けられます。

すべてのフィルターで、「AND」論理が使用されます。

>[!NOTE]
>
>セグメントフィルターは LC ステージ以降にのみ適用されます。 コホートステージが不明または既知で、いずれかのセグメントフィルターの値がある場合、ダッシュボードは何の結果も返しません。

ステージには、不明、既知、LC、オープンリード/連絡先ステージ（設定/CRM/ステージマッピング）で選択されたファネルステージ、OC、オープン商談ステージ（設定/CRM/ステージマッピング）で選択されたファネルステージ、および契約（クローズ済獲得商談）が含まれます。

>[!NOTE]
>
>コホートステージ以外のステージとして定義されたジャーニーステージのレコード数には、コホートレコードに関連する、選択した期間の開始日より後から期限切れ日までに作成されたすべての新しいレコードが含まれます。 これは因果性と推測される。

各バーからドリルダウンして、各ステージのレコードを表示できます。

* 「不明」の場合は、匿名の訪問者の詳細が表示されます。
* 既知の場合は、既知の訪問者の詳細が表示されます。
* LC およびオープンリード/連絡先ステージの場合、リード/連絡先詳細が表示されます。
* OC、オープン商談ステージ、および取引の場合は、商談の詳細が表示されます。
