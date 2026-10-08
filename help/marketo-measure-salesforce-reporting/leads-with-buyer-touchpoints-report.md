---
description: Marketo Measureのユーザー向けレポートのガイダンスである「Buyer Touchpoints」を使用したリード
title: 「Buyer Touchpointsを使用したリード」レポート
exl-id: 0376abb0-5eed-41bb-ab4f-3c204ab437df
feature: Touchpoints, Reporting
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: 32d2f1bc-61d0-598c-a8bf-f6fbc8920276
    internal-label: Touchpoints
  - id: d24e0b99-7796-5c7d-831d-d71a1d725f01
    internal-label: Reporting
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 8%
---
# 「Buyer Touchpointsを使用したリード」レポート {#leads-with-buyer-touchpoints-report}

>[!NOTE]
>
>ドキュメントに「[!DNL Marketo Measure]」を指定する手順が表示される場合がありますが、CRMには「[!DNL Bizible]」が表示されます。 アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

すぐに使える多くのレポート機能が[!DNL Marketo Measure]に関して簡単に利用できますが、作成することをお勧めします。追加のレポートタイプがいくつかあります。 以下のレポートタイプのバイヤータッチポイントを使用して、包括的なリードを作成する方法について説明します。

1. [!DNL Salesforce]内の設定オプションに移動します。 そこから、「作成」グループを展開し、**[!UICONTROL レポートタイプ]**&#x200B;を選択します。

   ![1. Salesforceで「設定」オプションに移動します。 そこから、](assets/bizible-guide-1.png)を展開します

1. **[!UICONTROL 新しいカスタムレポートタイプ]**&#x200B;を選択します。

   ![1. 新しいカスタムレポートタイプを選択します。](assets/marketo-reports-17.jpg)

1. プライマリオブジェクトを「リード」に設定し、「レポートタイプラベル」入力の「バイヤタッチポイントを持つリード – 含める」内に設定します。 「リード」カテゴリ内にレポートを保存し、デプロイメントステータスを&#x200B;**[!UICONTROL デプロイ]**&#x200B;に変更します。 次に、**[!UICONTROL 次へ]**&#x200B;を選択します。

   ![1. プライマリオブジェクトを「リード」として、「レポートタイプ &#x200B;](assets/marketo-reports-18.jpg)」内に設定します

1. オブジェクト関係で、**[!DNL Marketo Measure]Person** オブジェクトをセカンダリオブジェクトとして選択します。 「各「A」レコードには、少なくとも1つの関連「B」レコードが必要です」という名前で、AからBへの関係を選択します。 そこから、「Buyer Touchpoint」オブジェクトを関連付け、BとCのオブジェクト間に同じリレーションシップを選択します。

   ![1. オブジェクトの関係で、Marketo Measure Persons オブジェクト &#x200B;](assets/bizible-guide-2.png)を選択します

1. レポートを作成しましょう。
