---
unique-page-id: 18874560
description: タッチポイントを削除しない理由 — [!DNL Marketo Measure]
title: タッチポイントを削除してはいけない理由
exl-id: e74c14ff-0399-4ee9-b732-6686823ff5c7
feature: Touchpoints
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 5%

---

# タッチポイントを削除してはいけない理由 {#why-you-should-never-delete-touchpoints}

オポチュニティにタッチポイントが誤ってアトリビューションクレジットを割り当てられている場合は、担当のアカウントマネージャーに連絡して、次の手順を決定してください。 このような状況では、バイヤーのタッチポイント抑制機能を使用して、SFDC および ROI ダッシュボードからタッチポイントを削除することをお勧めします。 担当のアカウントマネージャーが、これらのルールの作成に役立ちます。 これらのタッチポイントを手動で自分で削除しないでください。

The [!DNL Marketo Measure] タッチポイントが SFDC から手動で削除されたという情報は、処理システムによって登録されません。 現在のところ、データを調整するためにシステムに信号を送るトリガーはありません。 [!DNL Marketo Measure] は、別のタッチポイントを自動的にプッシュして削除されたタッチポイントに置き換えたり、タッチポイントの位置またはアトリビューションを後続のタッチポイントに再割り当てしたりすることはありません。

タッチポイントが削除されると、アトリビューションデータに穴が作成されます。 通常、これはオポチュニティのアトリビューションタッチポイントで表示されます。 次の画像では、商談の作成タッチを受け取ったと思われるタッチポイントが削除されていました。 その結果、このオポチュニティには OC タッチポイントがなく、この商談の属性割合は最大 100%になりません。

![](assets/1.png)

SFDC からタッチポイントが削除されている場合は、次の URL にアクセスしてください： [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} をクリックして、データの再インポートをリクエストします。
