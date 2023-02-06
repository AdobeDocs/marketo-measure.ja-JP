---
description: カスタムの売上高額を利用する際のベストプラクティス — [!DNL Marketo Measure]  — 製品ドキュメント
title: カスタムの売上高を利用する際のベストプラクティス
exl-id: 553bd75a-512a-4733-a24b-8112eb420afc
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# カスタムの売上高を利用する際のベストプラクティス {#best-practices-for-utilizing-a-custom-revenue-amount}

## 概要 {#overview}

の主な機能 [!DNL Marketo Measure] は、購入者のジャーニーを通じてマーケティングタッチポイントに売上高クレジットを割り当てる機能です。 正確な売上高アトリビューションのキーは、 [!DNL Marketo Measure] を使用すると、オポチュニティに関する正しい売上高を参照できます。これらの売上高は、様々なアトリビューションモデルを介してマーケティングタッチポイント全体に分散されます。

実装時に別途指定されない限り、 [!DNL Marketo Measure] インスタンスは、収益属性の標準商談額（SFDC デフォルト）を参照するように設定されます。 しかし、多くの [!DNL Marketo Measure] アカウントの場合、このフィールドには商談の正確な売上高は反映されません。 この場合、 [!DNL Marketo Measure] は、次の項目に対してカスタムの売上高を設定する機能を提供します。 [!DNL Marketo Measure] を使用して、Attribution タッチポイント (BAT) 全体で参照および配布します。

## ベストプラクティス {#best-practice}

カスタムの売上高を設定する場合は、次のベストプラクティスに従って、 [!DNL Marketo Measure] アトリビューションデータは正確で一貫性があります。

注意事項：

* すべての商談に対して正確で使用されている収益フィールドを選択します
   * ARR または合計契約額お勧め
* 数式フィールドを使用しない
* 通貨換算にカスタム売上高を使用している場合、 [!UICONTROL Marketo Measure Multiple Currencies] の代わりに、の機能を使用することをお勧めします。
   * この [!DNL Marketo Measure] 「複数通貨」機能は、 [!DNL Salesforce] 通貨換算間の調整を最も確実におこなうため。 これにより、標準の「金額」（SFDC デフォルト）や、 [!DNL Salesforce] コンバージョン率。
* Amount フィールドを更新する場合 [!DNL Marketo Measure] を参照するには、データローダーを使用して過去の商談を更新し、売上高データの一貫性を確保し、適切なフィールドがワークフロー経由で設定されるようにします。

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

年別の売上高額の設定を調べて、アトリビューションデータが正確で、組織の他の売上高レポートと一致していることを確認します。

カスタムの売上高を利用している場合は、次の手順に従って収益の設定を確認してください。

* を [!DNL Marketo Measure] アカウントで、[!UICONTROL 商談]「 」セクション（CRM の下）
* 次を識別： [!UICONTROL カスタム商談額] フィールド、ここで [!UICONTROL カスタム売上高 API] フィールドをリストする必要があります
* これがまだ正しいフィールドであることを確認します。
* また、 [!DNL Salesforce] 管理者が、 [!DNL Salesforce] まだ実行中です

年次レビューの他に、組織の特定の変更が売上高の設定を確認する必要性を示す場合があります。

* マーケティングチームの売上高
* 「カスタム売上高」フィールドの変更点
* 収益のレポート方法に関する組織の変更

>[!MORELIKETHIS]
>
>* [カスタムの「売上高」フィールドの使用](/help/advanced-marketo-measure-features/custom-revenue-amount/using-a-custom-revenue-amount-field.md)
>* [データ・ローダを使用したカスタム金額フィールドの更新](/help/advanced-marketo-measure-features/custom-revenue-amount/using-data-loader-to-update-marketo-measure-custom-amount-field.md)
>* [複数通貨の概要](/help/advanced-marketo-measure-features/multi-currency/overview.md)
>* [複数通貨設定](/help/advanced-marketo-measure-features/multi-currency/settings.md)

