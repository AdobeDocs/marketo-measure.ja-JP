---
description: '[!DNL Marketo Measure] メンテナンス - [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] メンテナンス'
exl-id: 4e1d53bb-0af8-4774-9f69-6a95516b3d11
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 95%

---


# [!DNL Marketo Measure] メンテナンス {#marketo-measure-maintenance}

[!DNL Marketo Measure] は、必要な情報のほぼすべてを CRM から毎日取得しますが、[!DNL Marketo Measure] を稼動させ、可能な限り最も正確な情報を出力し続けるために、定期的にスケジュールする必要があるメンテナンスタスクがいくつかあります。

**新しいオフラインキャンペーンの Buyer Touchpoints の同期（2 回／月）**

オンボーディング中に学んだように、[!DNL Marketo Measure] は CRM のキャンペーンと同期して、オフラインのマーケティング活動に関する情報を取得します。組織が新しいキャンペーンを開始する際は、必要に応じてキャンペーンごとに Buyer Touchpoints を有効にします。

**すべてのチャネルに対する支出のアップロード（1 回／月）**

[!DNL Marketo Measure] の収益と ROI レポート機能を最大限に活用するには、各マーケティングチャネルとサブチャネルにどれだけ費やしているかを [!DNL Marketo Measure] に伝える必要があります。各チャネル／サブチャネルの所有者を指定し、その所有者に毎月新しいコスト情報をアップロードする必要があるシングルパーティに対する支出を報告させます。

コスト情報をアップロードする方法については、[この記事](/help/marketing-spend/marketing-channel-costs.md)を参照してください。

**追跡するドメインのリストの更新（1 回／月）**

Marketo Measure は、JavaScript がアクティブになっているすべてのページとサブドメインを追跡しますが、対象となるのは既知のドメインのみです。最近新しいドメインをデバッグした場合、国際的に展開された場合、またはプライマリドメインを変更した場合は、[Marketo サポート &#x200B;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} に連絡して、アカウントを適切に更新するようにしてください。

**カスタムチャネルマッピングの精度の確認（1 回／月）**

オンボーディング中に、オンラインおよびオフラインのマーケティング活動用のカスタムチャネルマッピングを設定します。マーケティング戦略と Marketo Measure の使用が進化するにつれて、マッピングロジックに常に注目して、すべてのタッチポイントが適切に分類されていることを確認する必要があります。

[!DNL Marketo Measure] はマッピングロジックを編集する際にデータを再処理するので、これらのルールは 7 日に 1 回しか変更できません。

オンライン設定については[この記事](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md)、オフライン設定については[この記事](/help/channel-tracking-and-setup/offline-channels/offline-custom-channel-setup.md)、およびお客様から厳選したベストプラクティスのリストを参照してください。

* 現在設定している「その他」または「NULL」チャネルに分類されているタッチポイントを確認します。必要に応じて、マッピングロジックを更新して、これらのタッチポイントをより正確なチャネルに再分類します。
* 現在ダイレクトチャネルに分類されているタッチポイントを確認します。メールマーケティングキャンペーンやその他の取り組みの一部に UTM パラメーターがない場合、トラフィックが不適切にダイレクトチャネルにバケット化されている可能性が高くなります。参照元を取り込むには、UTM パラメーターの更新を検討してください。

**タッチポイント抑制設定の評価（1 回／四半期）**

アトリビューションストーリーで考慮しないタッチポイントが（[!DNL Login] や [!DNL Unsubscribe forms]、採用ページ、社内アプリなどから）多数表示されている場合、既存のタッチポイント抑制設定を評価することをお勧めします。四半期に 1 回、不要なノイズを生成しているタッチポイントのグループを特定し、抑制ロジックを適切に更新します。ハウツーを含む[役立つ記事はこちらです](/help/advanced-features/touchpoint-settings/touchpoint-removal-and-touchpoint-suppression.md)。

**カスタムステージマッピングの精度の確認（1 回／四半期）（該当する場合）**

カスタムの[!UICONTROL リード]ステージ、[!UICONTROL 取引先責任者]ステージまたは[!UICONTROL 商談]ステージを使用している場合は、これらのステージがパイプラインのどの部分にマッピングされるか、またこれらのステージがカスタムアトリビューションモデルに含まれるかどうかもカスタマイズしている可能性があります。四半期に 1 回、[この記事](/help/advanced-features/custom-attribution-models/custom-attribution-model-and-setup.md)を参照して、カスタムステージマッピングに関する記憶を更新し、カスタムステージを正確に追跡していることを確認します。

**機械学習モデルとカスタムモデルの重み付けの比較（1 回／四半期）（該当する場合）**

[!DNL Marketo Measure] カスタムモデルのライセンスを取得している場合は、[!UICONTROL 設定]／[!UICONTROL アトリビューション設定]で機械学習モデル（MLM）からデータを利用することもできます。MLM は、アカウントからのタッチポイントデータを使用して各ステージの重要性を計算し、カスタムモデルでアトリビューションの重み付けを割り当てる方法を決定するのに役立ちます。四半期に一度 MLM とカスタムモデルを比較し、カスタムモデルへの潜在的な変更の影響について SM と話し合うことをお勧めします。

[!DNL Marketo Measure] 機械学習モデルについて詳しくは、[この記事](/help/advanced-features/custom-attribution-models/machine-learning-model-faq.md)を参照してください。
