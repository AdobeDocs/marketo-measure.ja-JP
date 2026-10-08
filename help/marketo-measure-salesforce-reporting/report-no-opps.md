---
description: Marketo Measure ユーザー向けの「商談のない連絡先」ガイダンスのレポートタイプ
title: 商談を含まない連絡先のレポートタイプ
exl-id: 255048be-16ff-4964-85fd-cc07888a05af
feature: Reporting
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: d24e0b99-7796-5c7d-831d-d71a1d725f01
    internal-label: Reporting
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 16%
---
# 商談を含まない取引先責任者用レポートタイプ {#report-type-for-contacts-without-opportunities}

>[!NOTE]
>
>ドキュメントに「[!DNL Marketo Measure]」を指定する手順が表示される場合がありますが、CRMには「[!DNL Bizible]」が表示されます。 アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

商談に関連付けられていないバイヤータッチポイントを持つ連絡先をレポートするには、カスタムレポートタイプを作成する必要があります。

1. **[!UICONTROL 設定]** > **[!UICONTROL 作成]** > **[!UICONTROL レポートタイプ]**&#x200B;に移動します。

   ![1. レポートの種類を作成の設定に移動します。](assets/new-types-1.png)

1. **[!UICONTROL 新しいカスタムレポートタイプ]**&#x200B;を選択します。

   ![1. 新しいカスタムレポートタイプを選択します。](assets/new-types-10.jpg)

1. [!UICONTROL プライマリオブジェクト &#x200B;]を「[!UICONTROL 連絡先]」に設定します。 レポートタイプラベルに「バイヤーのタッチポイントを使用した連絡先」という名前を付けます。 レポートタイプ名には、同じ名前を使用します。 説明入力内の「購入者のタッチポイントへの連絡」をクリックします。 「[!UICONTROL その他]」内にレポートを保存し、レポートを「[!UICONTROL &#x200B; デプロイ &#x200B;]」に設定します。

   ![1. プライマリオブジェクトを「連絡先」に設定します。 レポートに名前を付ける](assets/new-types-11.png)

1. そこから、Contacts オブジェクトをBuyer Touchpoints オブジェクトにリンクします。 「各「A」レコードには、関連する「B」レコードが少なくとも1つ必要です」ボタンを選択していることを確認します。

   ![1. そこから、連絡先オブジェクトを購入者](assets/new-types-12.png)にリンクします

1. **[!UICONTROL 保存]**&#x200B;をクリックすると、完了です。
