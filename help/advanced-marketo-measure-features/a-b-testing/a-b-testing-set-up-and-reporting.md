---
unique-page-id: 18874773
description: A/B テストの設定とレポート - [!DNL Marketo Measure]
title: A/B テストの設定とレポート
exl-id: 9a3f0731-5909-4fbf-a35a-9608ff561061
feature: A/B Testing
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 95%

---

# A/B テストの設定とレポート {#a-b-testing-set-up-and-reporting}

[!DNL Marketo Measure] A/B テストの統合により、[Optimizely](https://www.optimizely.com/){target="_blank"} と VWO サイト実験による収益への影響を追跡できます。この記事では、[!DNL Marketo Measure] A/B テストセクションをリード、[!UICONTROL 取引先責任]、ケース、[!UICONTROL 商談]のページレイアウトに追加する方法について説明します。また、[!DNL Marketo Measure] A/B レポートタイプの実行に関する一般的なレポート作成方法と、推奨事項についても説明します。

## 設定 {#set-up}

リード、取引先責任者、ケース、商談に関する [!DNL Marketo Measure] A/B テストセクションを追加します。[!DNL Marketo Measure] A/B テストの統合により、（Optimizely[ と [VWO](https://vwo.com/){target="_blank"} サイト実験の売上高の影響を追跡でき ](https://www.optimizely.com/){target="_blank"} す。

1. パッケージ [!DNL Marketo Measure] v3.9 以降を使用していることを確認してください。これを行うには、[!UICONTROL Salesforce]／[!UICONTROL 設定]／[!UICONTROL インストール済みパッケージ]に移動します。
1. リードページレイアウトを編集し、**[!DNL Marketo Measure]A/B テスト** 関連リストをページに追加します。

   ![](assets/1.png)

1. 「[!UICONTROL レンチ]」ボタンをクリックします。選択したフィールドのリストからストックの「ID」フィールドを削除します。「**[!UICONTROL 実験]**」、「**[!UICONTROL バリエーション]**」、「**[!UICONTROL DateReported]**」フィールドを追加します。「[!UICONTROL 並べ替え基準]」を「**[!UICONTROL 報告日]**」に変更し、ドロップダウンで「**[!UICONTROL 降順]**」を選択します。

   ![](assets/2.png)

1. [!UICONTROL ボタン]で、「**[!UICONTROL 新規]**」のチェックを外します。

   ![](assets/3.png)

1. この機能を有効にするには、[!DNL Marketo Measure] 担当者または [Marketo サポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}にお問い合わせください。

## レポート {#reporting}

お客様は、リード、取引先責任者、商談に関する A/B テストのレポートを可能にする、いくつかの [!DNL Marketo Measure] A/B レポートタイプにアクセスできます。

* [!DNL Marketo Measure] A/B テスト
* 取引先責任者に関する [!DNL Marketo Measure] A/B テスト
* リードに関する [!DNL Marketo Measure] A/B テスト
* 商談に関する [!DNL Marketo Measure] A/B テスト

![](assets/4.png)

A/B レポートタイプは、A/B テストの対象となったリード、取引先責任者、または商談に関するレポートに使用します。これらのレポートには、A/B テストの対象となった商談に結び付けられた売上高も示されます。

Optimizely/VWO は、マーケティングチャネルではなく、コンテンツのバリエーションプラットフォームであることに注意することが重要です。したがって、これらの [!DNL Marketo Measure] A/B レポートタイプの使用方法は、Buyer Touchpoint レポートとは異なります。Buyer touchpoint レポートタイプは、リードまたは取引先責任者を特定のページに導いたマーケティングチャネル（有料広告、Web ダイレクト、ソーシャル）を把握するために使用します。しかし、[!DNL Marketo Measure] A/B レポートタイプは、バリエーションがリードや商談に与えた影響をレポートする場合には使用できません。A/B テストのバリエーションはチャネルではないので、バリエーションの詳細は Buyer touchpoint には表示されません。

次に、A/B テストのレポートを作成して、明確性とインサイトを高める際に使用する推奨フィールドをいくつか示します。

* コンバージョン済みリード
* 実験
* 実験 ID
* バリエーション
* バリエーション ID
* 報告日

## [!DNL Salesforce] レポートの例 {#salesforce-example-reports}

リードに関する **[!DNL Marketo Measure]A/B テスト**

![](assets/5.png)

商談に関する **[!DNL Marketo Measure]A/B テスト**

![](assets/6.png)
