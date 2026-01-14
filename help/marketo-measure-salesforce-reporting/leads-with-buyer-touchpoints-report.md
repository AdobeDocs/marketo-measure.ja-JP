---
description: Marketo Measure ユーザー向けのバイヤータッチポイントを使用したリードのレポートガイダンス
title: 「購買担当タッチポイントのある引合」レポート
exl-id: 0376abb0-5eed-41bb-ab4f-3c204ab437df
feature: Touchpoints, Reporting
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 8%

---

# 「購買担当タッチポイントのある引合」レポート {#leads-with-buyer-touchpoints-report}

>[!NOTE]
>
>ドキュメントに「[!DNL Marketo Measure]」を指定する手順が表示される場合がありますが、CRM には「[!DNL Bizible]」が表示されます。 アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

すぐに使用できる多数のレポート機能が [!DNL Marketo Measure] 要ですが、構築を推奨するその他のレポートタイプもいくつかあります。 以下の買い手タッチポイントを使用した包括的なリードのレポートタイプについて説明します。

1. [!DNL Salesforce] 内の設定オプションに移動します。 そこから、「作成」グループ化を展開し、**[!UICONTROL レポートタイプ]** を選択します。

   ![1.Salesforce内の設定オプションに移動します。 そこから、](assets/bizible-guide-1.png) を展開します。

1. **[!UICONTROL 新規カスタムレポートタイプ]** を選択します。

   ![1.新規カスタムレポートタイプを選択。](assets/marketo-reports-17.jpg)

1. プライマリオブジェクトを「リード」に設定し、「レポートタイプのラベル」に「購入者タッチポイントを含むリード – その他」と入力します。 レポートを「リード」カテゴリ内に保存し、デプロイメントステータスを **[!UICONTROL デプロイ済み]** に変更します。 次に **[!UICONTROL 次へ]** を選択します。

   ![1.プライマリオブジェクトを「リード」として、「レポートタイプ &#x200B;](assets/marketo-reports-18.jpg) 内に設定します

1. オブジェクトの関係については、**[!DNL Marketo Measure]Person** オブジェクトをセカンダリ オブジェクトとして選択します。 A と B の関係を「各「A」レコードには、少なくとも 1 つの関連「B」レコードが必要」として選択します。 そこから、「Buyer Touchpoint」オブジェクトを関連付け、B オブジェクトと C オブジェクトの間に同じ関係を選択します。

   ![1.オブジェクトの関係については、Marketo Measure人物オブジェクトを選択し &#x200B;](assets/bizible-guide-2.png) す。

1. 保存して、レポートの作成を開始します。
