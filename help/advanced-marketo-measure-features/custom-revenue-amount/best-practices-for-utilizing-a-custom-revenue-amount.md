---
description: カスタム収益金額を利用するためのベストプラクティス -  [!DNL Marketo Measure]
title: カスタム収益額の利用のベストプラクティス
exl-id: 553bd75a-512a-4733-a24b-8112eb420afc
feature: Custom Revenue Amount
TQID: https://experienceleague.adobe.com/r0HE7od6BWa4ntQMPyrVqQWwebruGyxM3lhOOu6-RWc
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 433
ht-degree: 7%

---

# カスタム収益額の利用のベストプラクティス {#best-practices-for-utilizing-a-custom-revenue-amount}

## 概要 {#overview}

[!DNL Marketo Measure]の主な機能は、バイヤージャーニー全体を通じて、マーケティング接点に収益クレジットを割り当てる機能です。 正確な収益アトリビューションの鍵は、[!DNL Marketo Measure]が商談の正しい収益金額を参照できることです。これにより、さまざまなアトリビューションモデルを介してマーケティング接点に分配されます。

実装中に特に指定されていない限り、[!DNL Marketo Measure] インスタンスは、収益アトリビューション用の標準的な商談金額（SFDC デフォルト）を参照するように設定されます。 ただし、多くの[!DNL Marketo Measure] アカウントの場合、このフィールドには商談の正確な収益金額が反映されません。 これらの場合、[!DNL Marketo Measure]は、[!DNL Marketo Measure]がアトリビューション タッチポイント （BAT）を参照して配布するためのカスタム売上額を設定する機能を提供します。

## ベストプラクティス {#best-practice}

カスタム収益金額を設定する際には、次のベストプラクティスを念頭に置いて、[!DNL Marketo Measure] アトリビューションデータが正確かつ一貫性のあるものであることを確認してください。

留意点：

* すべての商談に対して正確で利用される収益フィールドを選択します
   * ARRまたは総契約額を推奨
* 数式フィールドを使用しない
* 通貨換算にカスタム売上金額を使用する場合は、代わりに[!UICONTROL Marketo Measure複数通貨]機能を使用することをお勧めします。
   * [!DNL Marketo Measure]複数通貨機能は、通貨換算の整合性を最も確保するために、[!DNL Salesforce]で設定されたコンバージョン率を参照します。 これにより、標準の「金額」（SFDCのデフォルト）または[!DNL Salesforce] コンバージョン率に関連するその他のカスタム金額フィールドを引き続き使用できます。
* [!DNL Marketo Measure]を参照する「金額」フィールドを更新する場合は、データローダーを使用して過去の商談を更新し、収益データが一貫しており、ワークフローを介して適切なフィールドに入力されていることを確認します

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

売上額の設定を毎年レビューすることで、アトリビューションデータが正確であり、他の組織の売上レポートと一致していることを確認できます。

カスタム収益金額を使用している場合は、次のように収益設定を確認します。

* [!DNL Marketo Measure] アカウントで、CRMの「[!UICONTROL 商談]」セクションに移動します
* [!UICONTROL  カスタム商談金額] フィールドを特定します。ここでは、[!UICONTROL  カスタム売上金額API] フィールドを表示します
* これが正しいフィールドであることを確認します
* また、[!DNL Salesforce]管理者に、[!DNL Salesforce]のカスタム収益金額ワークフローが実行中であることを確認してもらいます

毎年のレビューを除いて、特定の組織の変更は、収益金額の設定をレビューする必要性を示している可能性があります…

* マーケティングチームの入れ替わり
* カスタム収益フィールドへの変更
* 売上の報告方法における組織の変更

>[!MORELIKETHIS]
>
>* [ カスタム売上金額フィールドの使用](/help/advanced-marketo-measure-features/custom-revenue-amount/using-a-custom-revenue-amount-field.md)
>* [ データローダーを使用したカスタム金額フィールドの更新](/help/advanced-marketo-measure-features/custom-revenue-amount/using-data-loader-to-update-marketo-measure-custom-amount-field.md)
>* [複数通貨の概要](/help/advanced-marketo-measure-features/multi-currency/overview.md)
>* [複数通貨設定](/help/advanced-marketo-measure-features/multi-currency/settings.md)
