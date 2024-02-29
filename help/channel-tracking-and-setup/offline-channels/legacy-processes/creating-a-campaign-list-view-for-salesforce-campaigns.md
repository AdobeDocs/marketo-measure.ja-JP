---
unique-page-id: 18874718
description: 用のキャンペーンリストビューの作成 [!DNL Salesforce Campaigns] - [!DNL Marketo Measure]
title: ' [!DNL Salesforce] キャンペーンのキャンペーンリストビューの作成'
exl-id: 8c673ea3-ac24-4b3d-b67d-76888179c07a
feature: Channels
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 1%

---

# 用のキャンペーンリストビューの作成 [!DNL Salesforce] キャンペーン {#creating-a-campaign-list-view-for-salesforce-campaigns}

購入者タッチポイントと同期するキャンペーンのリスト表示を作成する方法を説明します。

>[!NOTE]
>
>この記事では、古いプロセスについて説明します。 ユーザーには、 [新しく改善されたアプリ内プロセス](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md){target="_blank"}.

作成可能なキャンペーンリストビューでは、「移動先」の場所で「タイプ」フィールドと「購入者のタッチポイントを有効にする」フィールドを確認および管理し、各 [!DNL Salesforce] オフラインマーケティングチャネルに通知するキャンペーンが適切に設定されていること。

1. の「キャンペーン」タブに移動 [!DNL Salesforce] 新しいリストビューを作成します。
1. ビューに「同期するキャンペーン」と名前を付けます。 [!DNL Marketo Measure].&quot;
1. 同期したいキャンペーンのみをこのリストに表示します [!DNL Marketo Measure] そのため、次の 2 つのフィルターが必要です。

   * **タイプ** [次と等しい] 「オフラインチャネルにマッピングしたすべてのキャンペーンタイプ」。 実装計画または [!DNL Marketo Measure] ([experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} -> マイアカウント/設定/オフラインチャネル )。 虫眼鏡アイコンを使用して、目的のタイプ（オフラインマーケティングチャネルにマッピングされるタイプ）を選択できます。

      * 各フィルターに対して、最大 3 種類を選択します。 フィルターフィールドに入力できる文字数は制限されています。 フィルターごとに 3 種類から始め、必要に応じて「タイプ」フィルターの行を追加します。

   * **作成日** [次よりも大きいか等しい] あなたの [!DNL Marketo Measure] 開始日。 開始日は、 [!DNL Marketo Measure] アプリ。 ダッシュの日付範囲で「作成日以降」を選択すると、開始日が表示されます。
   * **&#42;レコードタイプ&#42;**  — リストビューで編集を行うには、レコードタイプ用のフィルタを追加する必要があります。 編集が必要になる可能性のある各キャンペーンレコードは、同じレコードタイプである必要があります。

1. 選択したフィールドを編集して、リスト表示に表示します。 リスト表示の完全な設定は、次の例のようになります。

   このビューでは、キャンペーンを確認し、必要に応じて「タイプ」および「購入者タッチポイントを有効にする」フィールドを編集できます。 と同期する新しいキャンペーンを作成するとき [!DNL Marketo Measure]を使用すると、このビューが表示され、これらのキャンペーンのすべての設定をリスト内から直接管理できます。

   リスト表示からインライン編集を行うには、 [!DNL Salesforce] 設定：

   * **[!UICONTROL 設定]** > **[!UICONTROL ユーザーインターフェイス]** > **[!UICONTROL インライン編集を有効にする]**
   * また、「拡張リストを有効にする」チェックボックス（インライン編集用のボックスのすぐ下）もオンにしている必要があります。
   * フィールドに対する権限を持っていることを確認します。

>[!MORELIKETHIS]
>
>[リスト表示のインライン編集に関する一般的な問題のトラブルシューティング](http://help.salesforce.com/articleView?id=000003911&amp;language=en_US&amp;type=1){target="_blank"}
