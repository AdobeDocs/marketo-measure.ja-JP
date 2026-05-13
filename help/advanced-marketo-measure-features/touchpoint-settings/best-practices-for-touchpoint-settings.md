---
description: タッチポイント設定のベストプラクティス - [!DNL Marketo Measure]
title: Touchpoint 設定のベストプラクティス
exl-id: 01e314a6-e33d-45cd-aaa3-c212afec07d1
feature: Touchpoints
TQID: https://experienceleague.adobe.com/57Y-eSngdDje7RcPmmKobrzk2-QWrRyxN2rIVtdrOLQ
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 658
ht-degree: 6%

---

# Touchpoint 設定のベストプラクティス {#best-practices-for-touchpoint-settings}

## 概要 {#overview}

[!DNL Marketo Measure] アプリの[!UICONTROL &#x200B; タッチポイント設定] セクションでは、[!DNL Marketo Measure] データおよび関連システムからタッチポイントを除外または削除するルールを設定できます。 これらのルールは、購入者のタッチポイントデータで表現する必要がない、トラッキングやデータ収集に影響を与えることなくアトリビューションクレジットを受け取りたくない、特定のデータセットを分離するのに役立ちます。

**顧客接点の削除**&#x200B;とは、[!DNL Marketo Measure]がルール条件に適合する顧客接点をCRMから削除（つまり、削除）することを意味します。 データは、[!DNL Marketo Measure] ROI ダッシュボード （Discover）内でレポートできますが、CRMには表示されません。 CRM内のデータストレージ限界に対するストレスを軽減するために一般的に使用されます

**タッチポイント抑制**&#x200B;はタッチポイント削除に似ていますが、データはROI ダッシュボード内で報告できません。 抑制されたタッチポイントは、CRMまたは「もっと知る」ではアクセスできません。 抑制することで、CRM データとDiscover データが一致することが保証されます。 アトリビューションのクレジットを受け取るタッチポイントデータを調整し、さらに指定するために一般的に使用されます。

[!DNL Marketo Measure] アプリでは、[!UICONTROL &#x200B; タッチポイント設定] セクションが4つの重要なセクションに分けられます。 各セクションは、異なるデータセットのセットを抑制または削除します。 以下のキーを使用して、ルールが目的のタッチポイントを抑制または削除していることを確認します。

* Buyer Touchpointを CRM から削除
   * このセクションは、**CRM**&#x200B;から&#x200B;**Buyer Touchpoint data** （商談ではなく、個人に関連付けられているタッチポイント）を削除するルールを作成する場合に使用します
* CRM のBuyer Touchpointを抑制
   * このセクションは、**CRM**&#x200B;および&#x200B;**もっと知る**&#x200B;から&#x200B;**Buyer Touchpoint データ** （商談ではなく、個人に関連付けられているタッチポイント）を削除するルールを作成する場合に使用します
* Buyer Attribution Touchpoint を CRM から削除
   * このセクションは、**CRM**&#x200B;から&#x200B;**Buyer Attribution Touchpoint** データ （商談と収益に関連付けられているタッチポイント）を削除するルールを作成する場合に使用します
* CRM のBuyer Attribution Touchpointを抑制
   * このセクションは、**CRM**&#x200B;および&#x200B;**もっと知る**&#x200B;から&#x200B;**Buyer Attribution Touchpoint** データ （商談と収益に関連付けられているタッチポイント）を削除するルールを作成する場合に使用します

## ベストプラクティス {#best-practice}

タッチポイント設定ルールを初めて確立する場合でも、単に正確性をチェックするためにルールを確認する場合でも、次のベストプラクティスを念頭に置いてください。

* ルールを作成する前に、除外または削除するデータのリストを設定します
* 設定するルールを明確に示すフィールドを正確に特定します
* ルールに正しい演算子を指定していることを確認してください
* 上記のキーを使用して、タッチポイント設定の正しいセクションにルールを指定してください
* ルールを実装する前に、CRMのバイヤータッチポイントレポートでルールロジックをレプリケートして、ルールが目的のデータを抑制または削除していることを確認します

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

[!UICONTROL &#x200B; タッチポイント設定]を確認することは、適切に定義されていない場合にデータを大幅に変更できるため重要です。 ベストプラクティスとして、少なくとも年に2回、タッチポイント設定を確認することをお勧めします。 これは、[!DNL Marketo Measure] アプリの「タッチポイント設定」セクションで設定されたルールを簡単に視覚的に確認したものです。 このレビューにより、タッチポイント設定が最新であり、それに応じて変更を加えることができることを確認できます。

[!UICONTROL &#x200B; タッチポイント &#x200B;]設定を確認する理由には、次のようなものがあります。

* マーケティングチームの入れ替わり
* web サイト構造の大幅な更新
* 役に立たなくなった顧客接点データの識別
   * アトリビューションクレジットを受け取ってはいけないと思われるタッチポイントデータに遭遇するたびに、[!DNL touchpoint suppression] ルールは、データをできるだけクリーンで正確なものにする機能です。
* 抑制ルールまたは削除ルールの定義に使用されるフィールドの変更

>[!MORELIKETHIS]
>
>* [&#x200B; タッチポイントの削除と抑制の概要](/help/advanced-marketo-measure-features/touchpoint-settings/touchpoint-removal-and-touchpoint-suppression.md)
>* [&#x200B; タッチポイントを削除しない理由](/help/advanced-marketo-measure-features/touchpoint-settings/why-you-should-never-delete-touchpoints.md)
>* [購入者のタッチポイント （BT）と購入者のアトリビューションのタッチポイント （BAT） &#x200B;](/help/configuration-and-setup/getting-started-with-marketo-measure/difference-between-buyer-touchpoints-and-buyer-attribution-touchpoints.md)

