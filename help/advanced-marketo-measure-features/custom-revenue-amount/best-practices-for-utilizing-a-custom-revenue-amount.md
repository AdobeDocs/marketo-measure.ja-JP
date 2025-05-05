---
description: カスタム収益額の利用に関するベストプラクティス - [!DNL Marketo Measure]
title: カスタム収益額の利用のベストプラクティス
exl-id: 553bd75a-512a-4733-a24b-8112eb420afc
feature: Custom Revenue Amount
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 7%

---

# カスタム収益額の利用のベストプラクティス {#best-practices-for-utilizing-a-custom-revenue-amount}

## 概要 {#overview}

[!DNL Marketo Measure] の主な機能は、買い手のジャーニー全体を通じてマーケティングタッチポイントに売上高クレジットを割り当てる機能です。 正確な収益アトリビューションの鍵は、[!DNL Marketo Measure] が Opportunity で正しい収益額を参照する機能です。これは、様々なアトリビューションモデルを介してマーケティングタッチポイント全体に分散されます。

実装時に特に指定しない限り、[!DNL Marketo Measure] インスタンスは、収益属性の標準的な商談額（SFDC デフォルト）を参照するように設定されます。 ただし、多くの [!DNL Marketo Measure] アカウントでは、このフィールドには商談の正確な収益額が反映されません。 このような場合、[!DNL Marketo Measure] では、アトリビューションタッチポイント（BAT）全体で参照および配布する [!DNL Marketo Measure] のカスタム収益額を設定する機能を提供します。

## ベストプラクティス {#best-practice}

カスタム収益額を設定する場合、[!DNL Marketo Measure] アトリビューションデータを正確かつ一貫性のあるものにするために、次のベストプラクティスに留意してください。

留意点：

* 正確で、すべてのオポチュニティに活用される収益フィールドを選択します。
   * 推奨される ARR または合計契約金額
* 式フィールドを使用しない
* 通貨コンバージョンにカスタム売上高を使用する場合は、代わりに [!UICONTROL Marketo Measure多通貨 &#x200B;] 機能を使用することをお勧めします。
   * 多通貨 [!DNL Marketo Measure] 機能は、通貨換算間の整合性を最もよく確保するために、[!DNL Salesforce] で確立された換算レートを参照します。 これにより、標準の「金額」（SFDC のデフォルト）や、[!DNL Salesforce] のコンバージョン率に関連するその他のカスタム金額フィールドを引き続き利用できます。
* 参照 [!DNL Marketo Measure] る「金額」フィールドを更新する場合は、データローダーを使用して過去の商談を更新し、売上高データの一貫性を確保し、ワークフローを介して適切なフィールドが入力されるようにします

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

収益額の設定を毎年レビューすることで、アトリビューションデータが正確になり、組織の残りの収益レポートと連携できるようになります。

カスタム収益金額を使用している場合は、次のように収益設定を確認します。

* [!DNL Marketo Measure] アカウントで、CRM の「[!UICONTROL &#x200B; 商談 &#x200B;]」セクションに移動します
* 「[!UICONTROL &#x200B; カスタム商談額 &#x200B;]」フィールドを特定します。ここでは、「[!UICONTROL &#x200B; カスタム収益額 API] フィールドがリストされています
* このフィールドがまだ正しいことを確認します
* また、[!DNL Salesforce] のカスタム収益額ワークフローがまだ実行中であることも [!DNL Salesforce] 管理者に確認してもらいます

年次のレビューを除いて、特定の組織変更は、収益額の設定をレビューする必要があることを示している場合があります。

* マーケティングチームの入れ替わり
* カスタム収益フィールドの変更
* 売上高のレポート方法における組織の変更

>[!MORELIKETHIS]
>
>* [ カスタムの「売上高」フィールドの使用 ](/help/advanced-marketo-measure-features/custom-revenue-amount/using-a-custom-revenue-amount-field.md)
>* [ データローダーを使用したカスタム金額フィールドの更新 ](/help/advanced-marketo-measure-features/custom-revenue-amount/using-data-loader-to-update-marketo-measure-custom-amount-field.md)
>* [ 多通貨の概要 ](/help/advanced-marketo-measure-features/multi-currency/overview.md)
>* [ 複数通貨設定 ](/help/advanced-marketo-measure-features/multi-currency/settings.md)
