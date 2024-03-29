---
unique-page-id: 42762600
description: スナップショットダッシュボードのドキュメント — [!DNL Marketo Measure]
title: スナップショットダッシュボードドキュメント
exl-id: 4dfc92d2-ccab-4726-a869-3ae32aa89a5f
feature: Reporting
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 1%

---

# スナップショットダッシュボードドキュメント {#snapshot-dashboard-documentation}

スナップショットダッシュボードを使用すると、任意の時点での CRM の状態を表示でき、リード/連絡先ステージと商談ステージにわたるレコードの配分を表示できます。

このダッシュボードには次の 2 つのタイルがあります。

* **リード/連絡先のスナップショット：** 選択した日付の各ステージのリードまたは連絡先レコードの数。

>[!NOTE]
>
>すべての Discover ダッシュボードで、リードまたは連絡先のいずれか 1 つの担当者オブジェクトのみをレポートできます。 これは、 [!UICONTROL 設定] > [!UICONTROL レポート] > [!UICONTROL 属性設定] > [!UICONTROL デフォルトのダッシュボードオブジェクト].

* **商談のスナップショット：** 選択した日付の各ステージの商談レコード数。

このダッシュボードでは、次のフィルターをサポートしています（すべてのフィルターは両方のタイルに適用されます）。

* スナップショットの日付：スナップショットの日付を選択します。
* CRM アカウント ID/名前： CRM アカウント ID または名前でレコードをフィルターします。

>[!NOTE]
>
>候補には名前のみが表示されます。

* チャネル：チャネルでレコードをフィルターします。 レコードのタッチポイントの 1 つがチャネルに関連付けられている場合、そのレコードはチャネルに関連付けられます。
* サブチャネル：サブチャネルでレコードをフィルターします。 レコードのタッチポイントのいずれかがサブチャネルに関連付けられている場合、そのレコードはサブチャネルに関連付けられます。
* キャンペーン：キャンペーンでレコードをフィルターします。 レコードのタッチポイントがキャンペーンに関連付けられている場合、そのレコードはキャンペーンに関連付けられます。
* キャンペーンのソース：キャンペーンのソースでレコードをフィルタリングします。 以下にキャンペーンソースの例を示します。 [!DNL Adwords], [!DNL BingAds], [!DNL Facebook], [!DNL LinkedIn]など レコードのタッチポイントのいずれかがキャンペーンソースに関連付けられている場合、そのレコードはキャンペーンソースに関連付けられます。
* 広告アカウント ID/名前：広告アカウント ID または名前でレコードをフィルタリングします。 レコードのタッチポイントのいずれかが選択した広告アカウントからのキャンペーンに関連付けられている場合、そのレコードは広告アカウントに関連付けられます。

>[!NOTE]
>
>候補には名前のみが表示されます。

* セグメントフィルター：カスタムセグメントでレコードをフィルターします。 レコードのタッチポイントのいずれかがセグメントに関連付けられている場合、そのレコードはセグメントに関連付けられます。

すべてのフィルターで、「AND」論理が使用されます。

>[!NOTE]
>
>選択した日付でレコードのステージが変更されると、レコードは開始ステージと終了ステージ、およびすべてのパススルーステージに対してカウントされます。

## リード/連絡先スナップショット {#lead-contact-snapshot}

![](assets/one.png)

ステージには、FT、LC および選択したファネルステージが含まれ、オープンリード/連絡先ステージ ([!UICONTROL 設定] > [!UICONTROL CRM] > [!UICONTROL ステージマッピング]) をクリックします。

各バーからドリルダウンして、各ステージのリード/連絡先レコードを表示できます。

## 商談スナップショット {#opportunity-snapshot}

![](assets/two.png)

ステージには、FT、LC、選択されたファネルステージが含まれます（オープンリード/連絡先ステージ） ([!UICONTROL 設定] > [!UICONTROL CRM] > [!UICONTROL ステージマッピング]) をクリックします。 オープン商談ステージの OC および選択したファネルステージ ([!UICONTROL 設定] > [!UICONTROL CRM] > [!UICONTROL ステージマッピング]) をクリックします。

各バーからドリルダウンして、各ステージの商談レコードを表示できます。
