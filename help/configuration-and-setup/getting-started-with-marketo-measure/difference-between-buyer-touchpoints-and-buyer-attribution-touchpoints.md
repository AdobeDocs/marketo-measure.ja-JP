---
unique-page-id: 18874646
description: 購入者タッチポイントと購入者アトリビューションタッチポイントの違い — [!DNL Marketo Measure]
title: Buyer Touchpoints と Buyer Attribution Touchpoints の違い
exl-id: 19109271-7b59-44c0-b1ff-e3b0bba9f5ce
feature: Touchpoints
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 61%

---

# Buyer Touchpoints と Buyer Attribution Touchpoints の違い {#difference-between-buyer-touchpoints-and-buyer-attribution-touchpoints}

Buyer Touchpoint（BT）と Buyer Attribution Touchpoint（BAT）の定義、両者の違い、よくある質問について説明します。

Buyer Touchpoints と Buyer Attribution Touchpoints を区別する主なものは、[!DNL Salesforce] オブジェクトとの関係です。BT は、リード、連絡先および事例オブジェクトに関連しますが、商談オブジェクトには関連しません。つまり、購入者タッチポイントに関連する売上高はありません。

購入者属性タッチポイントオブジェクトは連絡先、アカウント、商談の各オブジェクトに関連していますが、リードオブジェクトには関連していません。購入者属性タッチポイントはリードに結び付けられていません。 BAT オブジェクトを使用すると、特定のマーケティングインタラクションに結び付けられた売上高を確認できます。

BT と BAT の違い：

<table> 
 <colgroup> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <td>Buyer Touchpoint（BT）</td> 
   <td>Buyer Attribution Touchpoint（BAT）</td> 
  </tr> 
  <tr> 
   <td> 
    <ul> 
     <li>リード、連絡先、事例オブジェクトに関連する</li> 
     <li>商談オブジェクトに関連しない</li> 
     <li>収益は Buyer Touchpoint には関連付けられない</li> 
    </ul></td> 
   <td> 
    <ul> 
     <li>連絡先、アカウント、商談オブジェクトに関連する</li> 
     <li>リードオブジェクトに関連しない</li> 
     <li>Buyer Attribution Touchpoint は、商談に関連付けられているので、すべての BAT には、それらに関連付けられた収益がある</li> 
    </ul></td> 
  </tr> 
 </tbody> 
</table>

## よくある質問 {#faq}

**Buyer Touchpoint は、いつ Buyer Attribution Touchpoint になりますか？**

BT は、関連した商談を含む連絡先にこの BT が関連付けられると、BAT になります。1 つの特定のマーケティングインタラクションが BT と BAT になることを理解することが重要です。

**Buyer Touchpoint は、Touchpoint の位置として商談作成（OC）を取ることはできますか？**

Buyer Touchpoint は、Touchpoint の位置として、ファーストタッチ（FT）、リード作成（LC）またはフォーム申請（中間のタッチポイント）のいずれかのみを取ることができます。BT は商談に関連していないので、BT が商談の作成またはクローズのタッチポイントポジションを持つことはできません。

**購入者タッチポイントデータはどのように使用されますか？**

通常、顧客は購入者タッチポイントデータを使用して、ファネルのトップとファネルエンゲージメントの中間を理解します。 意味 [!DNL Marketo Measure] ユーザーは、誰がフォームを送信し、誰がサイトを閲覧し、どのブログ投稿のパフォーマンスが高いか、どの AdWords 広告がコンバージョンにつながっているかなどを把握します。 Buyer Touchpoint データは、リードおよび連絡先のエンゲージメントを把握するのに最適です。

**Buyer Touchpoint は、Salesforce ではどのように見えますか？**

以下に、[!DNL Salesforce] での BT のスクリーンショットを示します。

![](assets/1.png)

**Buyer Attribution Touchpoint は、Salesforce ではどのように見えますか？**

以下に、[!DNL Salesforce] での BAT のスクリーンショットを示します。

![](assets/2.png)
