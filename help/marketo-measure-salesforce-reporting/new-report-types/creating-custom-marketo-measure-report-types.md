---
unique-page-id: 18874539
description: カスタム  [!DNL Marketo Measure]  レポートタイプの作成 –  [!DNL Marketo Measure]
title: カスタム [!DNL Marketo Measure] レポートタイプの作成
exl-id: 1d72a04f-6a2d-4607-ad09-3b025125156a
feature: Reporting
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 5%

---

# カスタム [!DNL Marketo Measure] レポートタイプの作成 {#creating-custom-marketo-measure-report-types}

>[!NOTE]
>
>ドキュメントに「[!DNL Marketo Measure]」を指定する手順が表示される場合がありますが、CRM には「[!DNL Bizible]」が表示されます。 アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

カスタム [!DNL Marketo Measure] [!DNL Salesforce] レポートタイプを作成する方法を説明します。 購入者タッチポイントを持つリード（カスタム）、購入者タッチポイントを持つ人物（カスタム）、Buyer Attribution Touchpointを持つ商談（カスタム）の 3 つの異なるレポートタイプを作成することをお勧 [!DNL Marketo Measure] します。

## 買い手タッチポイントを使用したリード （カスタム） {#leads-with-buyer-touchpoints-custom}

1. **[!UICONTROL 設定]**/**[!UICONTROL ビルド]**/**[!UICONTROL レポートタイプ]**/**[!UICONTROL 新規カスタムレポートタイプ]** に移動します。

   ![](assets/1.png)

1. カスタムレポートタイプを定義します。

   * [!UICONTROL &#x200B; レポートタイプのフォーカス &#x200B;] > [!UICONTROL [!UICONTROL プライマリオブジェクト &#x200B;]]: リード
   * 識別/[!UICONTROL &#x200B; レポートタイプラベル &#x200B;]：購入者タッチポイントを持つリード（カスタム）
   * [!UICONTROL &#x200B; カテゴリ内に保存 &#x200B;]：その他のレポート
   * [!UICONTROL &#x200B; デプロイメント &#x200B;]/[!UICONTROL &#x200B; デプロイメントステータス &#x200B;]：デプロイ済み

   ![](assets/2.png)

1. オブジェクトの関係を定義します。

   * リードオブジェクト（A）を [!DNL Marketo Measure] ースユーザーオブジェクト（B）に関連付け、次にBuyer Touchpointオブジェクト（C）に関連付けます
   * 「[!UICONTROL &#x200B; 各 A/B レコードには少なくとも 1 つの B/C] が必要」レコードが選択されていることを確認します
   * [!UICONTROL &#x200B; 保存 &#x200B;]

   ![](assets/3.png)

## 買い手タッチポイントを持つ [!DNL Marketo Measure] Person （カスタム） {#marketo-measure-person-with-buyer-touchpoints-custom}

1. **[!UICONTROL 設定]**/**[!UICONTROL ビルド]**/**[!UICONTROL レポートタイプ]**/**[!UICONTROL 新規カスタムレポートタイプ]** に移動します。

   ![](assets/4.png)

1. カスタムレポートタイプを定義します。

   * [!UICONTROL &#x200B; レポートタイプのフォーカス &#x200B;] > [!UICONTROL プライマリオブジェクト &#x200B;]: [!DNL Marketo Measure] 人
   * [!UICONTROL ID]/[!UICONTROL &#x200B; レポートタイプラベル &#x200B;]：購入者タッチポイントを持つ [!DNL Marketo Measure] ユーザー（カスタム）
   * [!UICONTROL &#x200B; カテゴリ内に保存 &#x200B;]：その他のレポート
   * [!UICONTROL &#x200B; デプロイメント &#x200B;]/[!UICONTROL &#x200B; デプロイメントステータス &#x200B;]：デプロイ済み

   ![](assets/5.png)

1. オブジェクトの関係を定義します。

   * [!DNL Marketo Measure] Person オブジェクト（A）とBuyer Touchpoint オブジェクト（B）の関連付け
   * 「[!UICONTROL &#x200B; 各 A レコードには少なくとも 1 つの B が必要 &#x200B;]」レコードが選択されていることを確認します
   * [!UICONTROL &#x200B; 保存 &#x200B;]

   ![](assets/6.png)

## Buyer Attribution Touchpointを使用した商談（カスタム） {#opportunities-with-buyer-attribution-touchpoint-custom}

1. **[!UICONTROL 設定]**/**[!UICONTROL ビルド]**/**[!UICONTROL レポートタイプ]**/**[!UICONTROL 新規カスタムレポートタイプ]** に移動します。

   ![](assets/7.png)

1. カスタムレポートタイプを定義します。

   * [!UICONTROL &#x200B; レポートタイプのフォーカス &#x200B;] > [!UICONTROL プライマリオブジェクト &#x200B;]：商談
   * [!UICONTROL ID]/[!UICONTROL &#x200B; レポートタイプラベル &#x200B;]:Buyer Attribution Touchpointに関する商談（カスタム）
   * [!UICONTROL &#x200B; カテゴリ内に保存 &#x200B;]：その他のレポート
   * [!UICONTROL &#x200B; デプロイメント &#x200B;]/[!UICONTROL &#x200B; デプロイメントステータス &#x200B;]：デプロイ済み

   ![](assets/8.png)

1. オブジェクトの関係を定義します。

   * 商談オブジェクト（A）とBuyer Attribution Touchpointオブジェクト（B）の関連付け
   * 「[!UICONTROL &#x200B; 各 A レコードには少なくとも 1 つの B が必要 &#x200B;]」レコードが選択されていることを確認します
   * [!UICONTROL &#x200B; 保存 &#x200B;]

   ![](assets/9.png)

## カスタムレポートタイプへのカスタムフィールドの追加 {#adding-custom-fields-to-custom-report-types}

1. レポートが作成されると、レポートタイプの概要にリダイレクトされます。 **[!UICONTROL レイアウトを編集]** をクリックします。

   ![](assets/10.png)

1. レポートに追加するカスタムフィールドが「フィールドレイアウトのプロパティ」セクションに表示されていることを確認します。 追加したい他のフィールドがある場合は、「[!UICONTROL &#x200B; ルックアップ経由で関連するフィールドを追加 &#x200B;]」オプションを使用します。

   ![](assets/11.png)
