---
description: タッチポイント設定のベストプラクティス — [!DNL Marketo Measure]  — 製品ドキュメント
title: タッチポイント設定のベストプラクティス
exl-id: 01e314a6-e33d-45cd-aaa3-c212afec07d1
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 3%

---

# タッチポイント設定のベストプラクティス {#best-practices-for-touchpoint-settings}

## 概要 {#overview}

タッチポイント設定セクション ( [!DNL Marketo Measure] アプリを使用すると、タッチポイントを抑制または削除するルールを設定できます [!DNL Marketo Measure] データと関連システム。 これらのルールを使用すると、購入者のタッチポイントデータに表示する必要がないデータや、トラッキングやデータ収集を妨げることなく、アトリビューションクレジットを受け取りたくないデータのセットを分離できます。

**タッチポイントの削除** 手段 [!DNL Marketo Measure] は、ルール条件に適合するタッチポイントを CRM からパージ（つまり、削除）します。 データは、 [!DNL Marketo Measure] ROI ダッシュボード (Discover) ですが、CRM には表示されません。 CRM 内のデータストレージ制限へのストレスを緩和するために一般的に使用されます

**タッチポイント抑制** は、タッチポイントの削除に似ていますが、ROI ダッシュボード内ではデータをレポートできません。 抑制されているタッチポイントは、CRM や Discover からはアクセスできません。 抑制により、CRM データと Discover データが一致するようになります。 アトリビューションクレジットを受け取るタッチポイントデータを微調整し、さらに指定するために一般的に使用されます。

を [!DNL Marketo Measure] アプリの場合、タッチポイント設定セクションは、4 つの主要セクションに分類されます。 各セクションでは、異なるデータセットを抑制または削除します。 以下のキーを使用して、ルールで目的のタッチポイントを抑制または削除していることを確認します。

* Buyer Touchpointを CRM から削除
   * このセクションは、 **購入者タッチポイントデータ** （オポチュニティではなく、個人に関連付けられたタッチポイント） **CRM**
* CRM のBuyer Touchpointを抑制
   * このセクションは、 **購入者タッチポイントデータ** （オポチュニティではなく、個人に関連付けられたタッチポイント） **CRM** および **Discover**
* Buyer Attribution Touchpoint を CRM から削除
   * このセクションは、 **購入者の属性タッチポイント** お客様の **CRM**
* CRM のBuyer Attribution Touchpointを抑制
   * このセクションは、 **購入者の属性タッチポイント** お客様の **CRM** および **Discover**

## ベストプラクティス {#best-practice}

タッチポイント設定ルールを初めて設定する場合でも、正確性を確認するためにルールをレビューする場合でも、次のベストプラクティスに留意してください。

* ルールを作成する前に、抑制または削除するデータのリストを設定します
* 設定しているルールを明確に示すフィールドを正確に特定します
* ルールに正しい演算子が指定されていることを確認します。
* 上記のキーを使用して、タッチポイント設定の正しいセクションでルールが指定されていることを確認します。
* CRM の購入者タッチポイントレポートでルールロジックをレプリケートし、目的のデータを抑制または削除していることを確認して、ルールを実装する前にテストしてください

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

タッチポイント設定を適切に定義していないと、データが大幅に変更される可能性があるので、タッチポイント設定を確認することが重要です。 ベストプラクティスとして、タッチポイント設定は少なくとも年に 2 回確認することをお勧めします。 これは、 [!DNL Marketo Measure] アプリを使用します。 このレビューでは、タッチポイント設定が最新であり、それに応じて変更を加えることができると確信できます。

タッチポイント設定を確認する理由には次が含まれます…

* マーケティングチームの売上高
* Web サイト構造の大幅なアップデート
* 役に立たなくなったタッチポイントデータの特定
   * アトリビューションクレジットを受け取るべきではないと思われるタッチポイントデータに遭遇した場合、タッチポイント抑制ルールは、できるだけクリーンで正確なデータを保証する機能です。
* 抑制または削除ルールの定義に使用されるフィールドの変更

>[!MORELIKETHIS]
>
>* [タッチポイントの削除と抑制の概要](/help/advanced-marketo-measure-features/touchpoint-settings/touchpoint-removal-and-touchpoint-suppression.md)
>* [タッチポイントを削除しない理由](/help/advanced-marketo-measure-features/touchpoint-settings/why-you-should-never-delete-touchpoints.md)
>* [購入者タッチポイント (BT) と購入者属性タッチポイント (BAT) の比較](/help/configuration-and-setup/getting-started-with-marketo-measure/difference-between-buyer-touchpoints-and-buyer-attribution-touchpoints.md)

