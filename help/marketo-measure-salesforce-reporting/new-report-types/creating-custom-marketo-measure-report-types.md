---
unique-page-id: 18874539
description: カスタムの作成 [!DNL Marketo Measure] レポートタイプ — [!DNL Marketo Measure]
title: カスタム [!DNL Marketo Measure] レポートタイプの作成
exl-id: 1d72a04f-6a2d-4607-ad09-3b025125156a
feature: Reporting
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 5%

---

# カスタムの作成 [!DNL Marketo Measure] レポートタイプ {#creating-custom-marketo-measure-report-types}

>[!NOTE]
>
>この場合、[!DNL Marketo Measure]」と表示されるが、まだ「[!DNL Bizible]」と入力します。 アドビは現在、その更新を行っており、ブランディングの変更がまもなく CRM に反映される予定です。

カスタムの作成方法を学ぶ [!DNL Marketo Measure] [!DNL Salesforce] レポートタイプ。 作成を推奨するレポートタイプは、「購入者タッチポイント（カスタム）のリード」と「購入者タッチポイント（カスタム）」の 3 つです。 [!DNL Marketo Measure] 購入者タッチポイント（カスタム）を持つ顧客、購入者属性タッチポイント（カスタム）を持つ商談。

## 購入者タッチポイントを持つリード（カスタム） {#leads-with-buyer-touchpoints-custom}

1. に移動します。 **[!UICONTROL 設定]** > **[!UICONTROL ビルド]** > **[!UICONTROL レポートタイプ]** > **[!UICONTROL 新しいカスタムレポートタイプ]**.

   ![](assets/1.png)

1. カスタムレポートタイプを定義します。

   * [!UICONTROL レポートタイプフォーカス] > [!UICONTROL [!UICONTROL プライマリオブジェクト]]：リード
   * 識別情報 > [!UICONTROL レポートタイプラベル]：購入者タッチポイントを持つリード（カスタム）
   * [!UICONTROL カテゴリに保存]：その他のレポート
   * [!UICONTROL 導入] > [!UICONTROL デプロイメントステータス]：デプロイ済み

   ![](assets/2.png)

1. オブジェクトの関係を定義します。

   * リードオブジェクト (A) を [!DNL Marketo Measure] 人物オブジェクト (B) に続いて購入者タッチポイントオブジェクト (C) に続いて
   * 次を確認します。[!UICONTROL 各 A/B レコードには少なくとも 1 つの B/C が必要です]&quot;件のレコードが選択されています
   * [!UICONTROL 保存]

   ![](assets/3.png)

## [!DNL Marketo Measure] 購入者タッチポイントを持つ担当者（カスタム） {#marketo-measure-person-with-buyer-touchpoints-custom}

1. に移動します。 **[!UICONTROL 設定]** > **[!UICONTROL ビルド]** > **[!UICONTROL レポートタイプ]** > **[!UICONTROL 新しいカスタムレポートタイプ]**.

   ![](assets/4.png)

1. カスタムレポートタイプを定義します。

   * [!UICONTROL レポートタイプフォーカス] > [!UICONTROL プライマリオブジェクト]: [!DNL Marketo Measure] 人物
   * [!UICONTROL 識別] > [!UICONTROL レポートタイプラベル]: [!DNL Marketo Measure] 購入者タッチポイントを持つ担当者（カスタム）
   * [!UICONTROL カテゴリに保存]：その他のレポート
   * [!UICONTROL 導入] > [!UICONTROL デプロイメントステータス]：デプロイ済み

   ![](assets/5.png)

1. オブジェクトの関係を定義します。

   * 関連付け [!DNL Marketo Measure] 人物オブジェクト (A) から購入者タッチポイントオブジェクト (B) へ
   * 次を確認します。[!UICONTROL 各 A レコードには少なくとも 1 つの B が必要です]&quot;件のレコードが選択されています
   * [!UICONTROL 保存]

   ![](assets/6.png)

## 購入者属性タッチポイント（カスタム）を持つ商談 {#opportunities-with-buyer-attribution-touchpoint-custom}

1. に移動します。 **[!UICONTROL 設定]** > **[!UICONTROL ビルド]** > **[!UICONTROL レポートタイプ]** > **[!UICONTROL 新しいカスタムレポートタイプ]**.

   ![](assets/7.png)

1. カスタムレポートタイプを定義します。

   * [!UICONTROL レポートタイプフォーカス] > [!UICONTROL プライマリオブジェクト]：商談
   * [!UICONTROL 識別] > [!UICONTROL レポートタイプラベル]：購入者属性タッチポイント（カスタム）を持つ商談
   * [!UICONTROL カテゴリに保存]：その他のレポート
   * [!UICONTROL 導入] > [!UICONTROL デプロイメントステータス]：デプロイ済み

   ![](assets/8.png)

1. オブジェクトの関係を定義します。

   * 商談オブジェクト (A) を購入者属性タッチポイントオブジェクト (B) に関連付けます。
   * 次を確認します。[!UICONTROL 各 A レコードには少なくとも 1 つの B が必要です]&quot;件のレコードが選択されています
   * [!UICONTROL 保存]

   ![](assets/9.png)

## カスタムレポートタイプへのカスタムフィールドの追加 {#adding-custom-fields-to-custom-report-types}

1. レポートを作成すると、レポートタイプの概要にリダイレクトされます。 クリック **[!UICONTROL レイアウトを編集]**.

   ![](assets/10.png)

1. レポートに追加するカスタムフィールドが「フィールドレイアウトプロパティ」セクションに表示されていることを確認します。 追加する他のフィールドがある場合は、[!UICONTROL 参照を使用して関連するフィールドを追加]&quot;オプション。

   ![](assets/11.png)
