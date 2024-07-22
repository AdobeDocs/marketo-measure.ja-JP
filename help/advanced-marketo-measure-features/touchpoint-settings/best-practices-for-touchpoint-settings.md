---
description: タッチポイント設定のベストプラクティス - [!DNL Marketo Measure]
title: Touchpoint 設定のベストプラクティス
exl-id: 01e314a6-e33d-45cd-aaa3-c212afec07d1
feature: Touchpoints
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 6%

---

# Touchpoint 設定のベストプラクティス {#best-practices-for-touchpoint-settings}

## 概要 {#overview}

[!DNL Marketo Measure] アプリの [!UICONTROL  タッチポイント設定 ] セクションを使用すると、[!DNL Marketo Measure] データおよび関連システムのタッチポイントを抑制または削除するルールを設定できます。 これらのルールは、購入者のタッチポイントデータで表す必要がないデータや、トラッキングやデータ収集の妨げとならずにアトリビューションクレジットを受け取りたくないデータのセットを分離するのに役立ちます。

**タッチポイントの削除** とは、ルール条件 [!DNL Marketo Measure] 適合する CRM からすべてのタッチポイントを削除（つまり、削除）することを意味します。 データは、[!DNL Marketo Measure] ROI ダッシュボード（Discover）内でレポートできますが、CRM には表示されません。 CRM 内のデータストレージ制限に対するストレスを軽減するために一般的に使用される

**タッチポイント抑制** は、タッチポイントの削除に似ていますが、ROI ダッシュボード内でデータをレポートすることはできません。 抑制されているタッチポイントは、CRM または Discover からアクセスできません。 抑制を使用すると、CRM データと Discover データが一致するようになります。 アトリビューションクレジットを受け取るタッチポイントデータを微調整し、さらに指定するために一般的に使用されます。

[!DNL Marketo Measure] アプリでは、「[!UICONTROL  タッチポイント設定 ] セクションが 4 つの主要なセクションに分類されます。 各セクションでは、異なるデータセットが抑制または削除されます。 以下のキーを使用して、ルールが目的のタッチポイントを抑制または削除していることを確認します。

* Buyer Touchpointを CRM から削除
   * このセクションを使用すると、**Buyer Touchpoint データ** （オポチュニティではなく、個人に関連付けられたタッチポイント）を **CRM** から削除するルールを作成できます
* CRM のBuyer Touchpointを抑制
   * このセクションを使用して、**Buyer Touchpoint データ** （商談ではなく、個人に関連付けられたタッチポイント）を **CRM** と **Discover** から削除するルールを作成する場合を設定します
* Buyer Attribution Touchpoint を CRM から削除
   * このセクションを使用すると、**Buyer Attribution Touchpoint** データ（商談と売上高に関連付けられているタッチポイント）を **CRM** から削除するルールを作成できます
* CRM のBuyer Attribution Touchpointを抑制
   * このセクションは、**Buyer Attribution Touchpoint** データ（商談と売上高に関連付けられているタッチポイント）を **CRM** と **Discover** から削除するルールを作成する場合に使用します

## ベストプラクティス {#best-practice}

タッチポイント設定ルールを初めて設定する場合でも、精度を確認するためにタッチポイント設定ルールを見直す場合でも、次のベストプラクティスを念頭に置いてください。

* ルールを作成する前に、抑制または削除するデータのリストを設定します
* 設定しているルールを明確に示すフィールドを正確に特定する
* ルールに対して正しい演算子を指定したことを確認します
* 上記のキーを利用して、ルールがタッチポイント設定の正しいセクションで指定されていることを確認します
* CRM の購入者タッチポイントレポートのルールロジックをレプリケートし、目的のデータを抑制または削除していることを確認してから、ルールを実装します

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

[!UICONTROL  タッチポイント設定 ] の確認は、適切に定義されていないとデータが大幅に変更される可能性があるので、重要です。 ベストプラクティスとして、少なくとも年に 2 回タッチポイント設定を確認することをお勧めします。 これは、[!DNL Marketo Measure] アプリのタッチポイント設定セクションで設定されたルールを視覚的に簡単に確認するものです。 このレビューにより、タッチポイント設定が最新であり、それに応じて変更を加えることができると確信できます。

[!UICONTROL  タッチポイント ] 設定を確認する理由には次が含まれます…

* マーケティングチームの入れ替わり
* Web サイト構造の大幅な更新
* 役に立たなくなったタッチポイントデータの識別
   * アトリビューションクレジットを受け取るべきではないと感じるタッチポイントデータに遭遇するたびに、[!DNL touchpoint suppression] のルールは、データをできる限りクリーンで正確にする機能です。
* 抑制または削除ルールの定義に使用するフィールドへの変更

>[!MORELIKETHIS]
>
>* [ タッチポイントの削除と抑制の概要 ](/help/advanced-marketo-measure-features/touchpoint-settings/touchpoint-removal-and-touchpoint-suppression.md)
>* [ タッチポイントを削除してはいけない理由 ](/help/advanced-marketo-measure-features/touchpoint-settings/why-you-should-never-delete-touchpoints.md)
>* [ バイヤータッチポイント（BT）とバイヤー属性タッチポイント（BAT）の比較 ](/help/configuration-and-setup/getting-started-with-marketo-measure/difference-between-buyer-touchpoints-and-buyer-attribution-touchpoints.md)

