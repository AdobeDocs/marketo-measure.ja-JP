---
unique-page-id: 18874718
description: ' [!DNL Salesforce Campaigns] - [!DNL Marketo Measure]のキャンペーンリストビューを作成しています'
title: ' [!DNL Salesforce] キャンペーンのキャンペーンリストビューの作成'
exl-id: 8c673ea3-ac24-4b3d-b67d-76888179c07a
feature: Channels
TQID: https://experienceleague.adobe.com/MYh66JaJKdgBI7XVxfffWlX9QDg4SqLWDhpsdv1kSG4
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 444
ht-degree: 6%

---

# [!DNL Salesforce] キャンペーンのキャンペーンリストビューを作成しています {#creating-a-campaign-list-view-for-salesforce-campaigns}

顧客接点と同期させるキャンペーンのリストビューを作成する方法を説明します。

>[!NOTE]
>
>この記事では、古いプロセスについて説明します。 ユーザには、[新しく改善されたアプリ内プロセス](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md){target="_blank"}を使用することをお勧めします。

作成できるキャンペーンリストビューでは、「タイプ」フィールドと「バイヤーのタッチポイントを有効にする」フィールドを表示および管理する「移動」場所を使用して、オフラインマーケティングチャネルに通知する各[!DNL Salesforce] キャンペーンが適切に設定されていることを確認できます。

1. [!DNL Salesforce]の「キャンペーン」タブに移動し、新しいリストビューを作成します
1. ビューに「Campaigns to sync with [!DNL Marketo Measure]」という名前を付けます。
1. このリストには、[!DNL Marketo Measure]と同期するキャンペーンのみを表示するので、いくつかのフィルターが必要です。

   * **Type** [EQUALS] 「オフラインチャネルにマッピングしたすべてのキャンペーンタイプ」。 実装プランまたは[!DNL Marketo Measure]の「オフラインチャネル」タブ（[experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} -> マイアカウント ->設定 – > オフラインチャネル）を参照してください。 虫眼鏡アイコンを使用して、必要なタイプ（オフラインマーケティングチャネルにマッピングされているタイプ）を選択できます。

      * 各フィルターに対して「最大3種類」を選択します。 フィルターフィールドには、文字数の制限があります。 フィルターごとに3つのタイプから開始し、必要に応じて「タイプ」フィルターの行を追加します。

   * **作成日** [以上]が[!DNL Marketo Measure]の開始日です。 開始日は、[!DNL Marketo Measure] アプリ内のROI ダッシュボードで確認できます。 ダッシュの日付範囲で「作成日以降」を選択すると、開始日が表示されます。
   * **&#42;レコードタイプ&#42;** - リスト表示を編集するには、レコードタイプのフィルターを追加する必要があります。 編集する必要がある各キャンペーンレコードは、同じレコードタイプである必要があります。

1. 選択したフィールドを編集して、リストビューに表示します。 リストビューの完全な設定は、次の例のようになります。

   このビューでは、キャンペーンを表示し、必要に応じて「タイプ」フィールドと「バイヤタッチポイントを有効にする」フィールドを編集できます。 [!DNL Marketo Measure]と同期する新しいキャンペーンを作成すると、このビューに表示され、リスト内からそれらのキャンペーンのすべての設定を直接管理できます。

   リスト ビューからインライン編集を行うには、[!DNL Salesforce]の設定内で次の設定も満たしていることを確認する必要があります。

   * **[!UICONTROL セットアップ]** > **[!UICONTROL ユーザーインターフェイス]** > **[!UICONTROL インライン編集を有効にする]**
   * また、「拡張リストを有効にする」をオンにする（インライン編集用のボックスのすぐ下にある）
   * 必ずフィールドに対する権限を持つようにしてください

>[!MORELIKETHIS]
>
>[&#x200B; リスト表示のインライン編集に関する一般的な問題のトラブルシューティング &#x200B;](http://help.salesforce.com/articleView?id=000003911&language=en_US&type=1){target="_blank"}
