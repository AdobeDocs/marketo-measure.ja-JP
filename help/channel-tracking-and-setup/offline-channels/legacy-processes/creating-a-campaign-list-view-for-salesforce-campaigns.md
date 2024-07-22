---
unique-page-id: 18874718
description: ' [!DNL Salesforce Campaigns] - [!DNL Marketo Measure] 用のキャンペーンリスト表示の作成'
title: ' [!DNL Salesforce] キャンペーンのキャンペーンリストビューの作成'
exl-id: 8c673ea3-ac24-4b3d-b67d-76888179c07a
feature: Channels
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 5%

---

# キャンペーン用のキャンペーンリスト表示 [!DNL Salesforce] 作成 {#creating-a-campaign-list-view-for-salesforce-campaigns}

バイヤータッチポイントと同期するキャンペーンのリスト表示を作成する方法を説明します。

>[!NOTE]
>
>この記事では、古いプロセスについて説明します。ユーザには、[新しく改善されたアプリ内プロセス](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md){target="_blank"}を使用することをお勧めします。

作成可能なキャンペーンリスト表示を使用すると、「タイプ」フィールドと「購入者タッチポイントを有効にする」フィールドを表示および管理するための「ゴー [!DNL Salesforce]」場所を設定して、オフラインマーケティングチャネルに通知する各キャンペーンキャンペーンが正しく設定されていることを確認できます。

1. [!DNL Salesforce] の「キャンペーン」タブに移動し、新しいリスト表示を作成します
1. ビューに「[!DNL Marketo Measure] と同期するキャンペーン」という名前を付けます。
1. このリストには、[!DNL Marketo Measure] と同期するキャンペーンのみを表示するので、次のフィルターが必要です。

   * **Type**[EQUALS] 「オフラインチャネルにマッピングしたすべてのキャンペーンタイプ」。 実装プランまたは [!DNL Marketo Measure] の「オフラインチャネル」タブ（[experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}/「マイアカウント」/「設定」/「オフラインチャネル」）を参照します。 虫めがねアイコンを使用して、必要なタイプ（オフラインのマーケティングチャネルにマッピングされるタイプ）を選択できます。

      * 各フィルターに対して 3 種類の最大を選択します。 フィルターフィールドには、文字数の制限があります。 フィルターごとに 3 つのタイプから開始し、必要に応じて「Type」フィルターの行を追加します。

   * **作成日**[ 以上 ][!DNL Marketo Measure] の開始日。 開始日は、[!DNL Marketo Measure] アプリ内の ROI ダッシュボードで確認できます。 ダッシュの日付範囲で「作成日から」を選択するだけで、開始日が表示されます。
   * **&#42;レコードタイプ&#42;** - リスト表示で編集を行うには、レコードタイプのフィルターを追加する必要があります。 編集が必要になる各キャンペーンレコードは、同じレコードタイプである必要があります。

1. 選択したフィールドを編集して、リスト表示に表示します。 リスト表示の完全な設定は、次の例のようになります。

   このビューでは、キャンペーンを表示し、「タイプ」および「購入者タッチポイントを有効にする」フィールドを必要に応じて編集できます。 [!DNL Marketo Measure] と同期する必要がある新しいキャンペーンを作成すると、そのキャンペーンはこのビューに表示され、リスト内からキャンペーンのすべての設定を管理できます。

   リスト表示からインライン編集を行うには、[!DNL Salesforce] の設定内で次の点にも当てはまることを確認する必要があります。

   * **[!UICONTROL 設定]**/**[!UICONTROL ユーザーインターフェイス]**/**[!UICONTROL インライン編集を有効にする]**
   * また、「拡張リストを有効にする」をオンにする（インライン編集用ボックスの直下）必要があります
   * フィールドへの権限があることを確認します

>[!MORELIKETHIS]
>
>[ リスト表示のインライン編集に関する一般的な問題のトラブルシューティング ](http://help.salesforce.com/articleView?id=000003911&amp;language=en_US&amp;type=1){target="_blank"}
