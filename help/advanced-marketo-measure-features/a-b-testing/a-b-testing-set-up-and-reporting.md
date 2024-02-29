---
unique-page-id: 18874773
description: A/B テストの設定とレポート — [!DNL Marketo Measure]
title: A/B テストの設定とレポート
exl-id: 9a3f0731-5909-4fbf-a35a-9608ff561061
feature: A/B Testing
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 5%

---

# A/B テストの設定とレポート {#a-b-testing-set-up-and-reporting}

The [!DNL Marketo Measure] A/B テストの統合により、 [Optimizely](https://www.optimizely.com/){target="_blank"} と VWO サイト実験。 この記事では、 [!DNL Marketo Measure] リードに対する A/B テストセクション [!UICONTROL 連絡先]、大文字と小文字、および [!UICONTROL 商談] ページレイアウト。 また、実行に関する一般的なレポートの慣行と推奨事項も示します。 [!DNL Marketo Measure] A/B レポートタイプ。

## 設定 {#set-up}

次を追加： [!DNL Marketo Measure] リード、連絡先、事例、商談に関する A/B テストのセクション。 [!DNL Marketo Measure] A/B テストの統合により、 [Optimizely](https://www.optimizely.com/){target="_blank"} and [VWO](https://vwo.com/){target="_blank"} サイト実験。

1. パッケージを使用していることを確認します。 [!DNL Marketo Measure] v3.9 以降。 これをおこなうには、次に進みます。 [!UICONTROL Salesforce] >[!UICONTROL 設定] > [!UICONTROL インストール済みパッケージ].
1. リードページレイアウトを編集し、 **[!DNL Marketo Measure]A/B テスト** 関連するリストをページに追加します。

   ![](assets/1.png)

1. 次をクリック： [!UICONTROL レンチ] 」ボタンをクリックします。 選択したフィールドのリストから在庫「ID」フィールドを削除します。 追加 **[!UICONTROL 実験]**, **[!UICONTROL バリエーション]**、および **[!UICONTROL DateReported]** フィールド。 &quot;の変更[!UICONTROL 並べ替え基準]」から **[!UICONTROL 報告日]**&#x200B;をクリックし、次を選択します。 **[!UICONTROL 降順]** 」と入力します。

   ![](assets/2.png)

1. の下 [!UICONTROL ボタン]，オフ **[!UICONTROL 新規]**.

   ![](assets/3.png)

1. お問い合わせ [!DNL Marketo Measure] rep または [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} をクリックして機能を有効にします。

## レポート {#reporting}

お客様は、 [!DNL Marketo Measure] リード、連絡先、商談に関する A/B テストのレポートを可能にする A/B レポートタイプ：

* [!DNL Marketo Measure] A/BTests
* [!DNL Marketo Measure] 連絡先との A/B テスト
* [!DNL Marketo Measure] リードを持つ A/B テスト
* [!DNL Marketo Measure] 商談を伴う A/B テスト

![](assets/4.png)

A/B レポートタイプは、A/B テストにさらされたリード、連絡先、または商談に関するレポートに使用します。 これらのレポートは、A/B テストにさらされた商談に結び付けられた売上高も示します。

Optimizely/VWO は、マーケティングチャネルではなく、コンテンツのバリエーションプラットフォームであることに注意する必要があります。 したがって、これらは [!DNL Marketo Measure] A/B レポートタイプの使用方法は、購入者タッチポイントレポートとは異なります。 購入者タッチポイントレポートタイプは、リードまたは連絡先が特定のページに導いたマーケティングチャネル（有料広告、Web ダイレクト、ソーシャル）を把握するために使用します。 しかし、 [!DNL Marketo Measure] A/B レポートタイプは、バリエーションがリードや商談に与えた影響をレポートする場合には使用できません。 A/B テストのバリエーションはチャネルではないので、バリエーションの詳細は購入者のタッチポイントには表示されません。

次に、A/B テストのレポートを作成して明確性と洞察を高める際に使用する推奨フィールドを示します。

* 変換済みリード
* 実験
* 実験 ID
* バリエーション
* バリエーション ID
* 報告日

## [!DNL Salesforce] レポートの例 {#salesforce-example-reports}

**[!DNL Marketo Measure]リード付き A/B テスト**

![](assets/5.png)

**[!DNL Marketo Measure]商談を含む A/B テスト**

![](assets/6.png)
