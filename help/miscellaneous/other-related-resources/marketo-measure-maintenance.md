---
unique-page-id: 18874556
description: '"[!DNL Marketo Measure] メンテナンス — [!DNL Marketo Measure]  — 製品ドキュメント»'
title: "[!DNL Marketo Measure] メンテナンス"
exl-id: 4e1d53bb-0af8-4774-9f69-6a95516b3d11
source-git-commit: 09ffdbb0b1baeed870a3145268997e63a3707c97
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# [!DNL Marketo Measure] メンテナンス {#marketo-measure-maintenance}

[!DNL Marketo Measure] 必要なほとんどすべてを CRM から毎日取り込みますが、定期的に保持するようにスケジュールする必要のあるメンテナンスタスクがいくつかあります [!DNL Marketo Measure] ハミングし、可能な限り正確な情報を出力します。

**新しいオフラインキャンペーン用の購入者タッチポイントの同期（月 2 回）**

オンボーディング時に学習した内容 [!DNL Marketo Measure] は、CRM のキャンペーンと同期して、オフラインマーケティング活動に関する情報を取得します。 組織が新しいキャンペーンを開始したら、必要に応じて、各キャンペーンの購入者タッチポイントを有効にしてください。 チェックアウト [この記事](/help/channel-tracking-and-setup/offline-channels/syncing-offline-campaigns.md)を参照してください。

**すべてのチャネルのアップロード費用（1 回/月）**

の完全な売上高と ROI レポート機能を活用する[!DNL Marketo Measure]、 [!DNL Marketo Measure] 各マーケティングチャネルおよびサブチャネルに費やしている量。 各チャネル/サブチャネルの所有者を指定し、その担当者が新しいコスト情報を月単位でアップロードする際に、1 人のパーティに支出を報告することをお勧めします。

読んでコスト情報をアップロードする方法に関するメモリを更新 [この記事](/help/marketing-spend/spend-management/marketing-channel-costs.md).

**追跡するドメインのリストを更新します（1 回/月）**

Marketo Measureは、JavaScript がアクティブなすべてのページおよびサブドメインを追跡しますが、それは既知のドメインに対してのみ追跡します。 新しいドメインのデビュー、国際展開、またはプライマリドメインの変更を最近おこなった場合は、 [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} アカウントを適切に更新するようにしてください。

**正確性を確認するためにカスタムチャネルマッピングを確認する（1 回/月）**

オンボーディング中に、オンラインマーケティングとオフラインマーケティングの取り組みのカスタムチャネルマッピングを設定します。 マーケティング戦略とMarketo Measureの使用が進化するにつれ、すべてのタッチポイントが適切に分類されるように、そのマッピングロジックに目を向けたいと考えます。

忘れないで下さい [!DNL Marketo Measure] マッピングロジックを編集する際にデータが再処理されるので、これらのルールを 7 日に 1 回以上変更することはできません。

参照 [この記事](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md) （オンラインセットアップの場合） [この記事](/help/channel-tracking-and-setup/offline-channels/offline-custom-channel-setup.md) オフラインセットアップの場合と、お客様から厳選されたこのベストプラクティスのリストを示します。

* 現在、設定した「その他」または「NULL」チャネルに分類されているタッチポイントを確認します。 必要に応じて、マッピングロジックを更新し、それらのタッチポイントをより正確なチャネルに再分類します。
* 現在ダイレクトチャネルに分類されているタッチポイントを確認します。 電子メールマーケティングキャンペーンやその他の取り組みの一部で UTM パラメーターが欠落している場合は、トラフィックが不適切にダイレクトチャネルにグループ化されている可能性が高くなります。 参照元を取り込むには、UTM パラメーターの更新を検討してください。

**タッチポイント抑制設定の評価（1 x /四半期）**

多数のタッチポイントが表示されている場合は、( [!DNL Login] または [!DNL Unsubscribe forms]、キャリアページ、内部アプリなど ) の場合は、既存のタッチポイント抑制設定を評価できます。 1 四半期に 1 回、不要なノイズを生成しているタッチポイントのグループを特定し、抑制ロジックを適切に更新します。 [次に、役立つ記事を示します。](/help/advanced-marketo-measure-features/touchpoint-settings/touchpoint-removal-and-touchpoint-suppression.md)  ハウツーと

**正確性（1 x /四半期）を確認するためのカスタムステージマッピングの確認（該当する場合）**

任意のカスタム [!UICONTROL リード], [!UICONTROL 連絡先]または [!UICONTROL 商談] また、これらのステージがカスタムアトリビューションモデルに含まれるかどうかや、それらのステージのパイプラインのどの部分にマッピングされるかをカスタマイズしている場合もあります。 四半期に 1 回、訪問 [この記事](/help/advanced-marketo-measure-features/custom-attribution-models/custom-attribution-model-and-setup.md) をクリックして、カスタムステージマッピングのメモリを更新し、カスタムステージを正確に追跡していることを確認します。

**機械学習モデルとカスタムモデルの重み付け（1 x/四半期）の比較（該当する場合）**

のライセンスを取得している場合、 [!DNL Marketo Measure] カスタムモデルの場合は、 [!UICONTROL 設定] > [!UICONTROL 属性設定]. MLM は、アカウントからのタッチポイントデータを使用して各ステージの重要度を計算し、カスタムモデルでアトリビューションの重み付けを割り当てる方法を決定するのに役立つ場合があります。 MLM とカスタムモデルを 1 四半期に 1 回比較し、カスタムモデルに対する潜在的な変更の影響を SM と比較することをお勧めします。

詳しくは、 [!DNL Marketo Measure] 機械学習モデル、チェックアウト [この記事](/help/advanced-marketo-measure-features/custom-attribution-models/machine-learning-model-faq.md).
