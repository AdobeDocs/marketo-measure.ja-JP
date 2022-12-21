---
unique-page-id: 18874773
description: A/B テストの設定とレポート — [!DNL Marketo Measure]  — 製品ドキュメント
title: A/B テストの設定とレポート
exl-id: 9a3f0731-5909-4fbf-a35a-9608ff561061
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 3%

---

# A/B テストの設定とレポート {#a-b-testing-set-up-and-reporting}

この [!DNL Marketo Measure] A/B テストの統合により、 [Optimizely](https://optimizely.com/){target=&quot;_blank&quot;} および VWO サイト実験。 この記事では、 [!DNL Marketo Measure] リードに対する A/B テストセクション [!UICONTROL 連絡先]、大文字と小文字、 [!UICONTROL 商談] ページレイアウト。 また、実行に関する一般的なレポートの慣行と推奨事項についても説明します [!DNL Marketo Measure] A/B レポートタイプ。

## 設定 {#set-up}

を [!DNL Marketo Measure] リード、連絡先、事例、商談に関する A/B テストのセクション。 [!DNL Marketo Measure] A/B テストの統合により、 [Optimizely](https://optimizely.com/){target=&quot;_blank&quot;} および [VWO](https://vwo.com/){target=&quot;_blank&quot;} サイト実験。

1. パッケージを使用していることを確認します。 [!DNL Marketo Measure] v3.9 以降。 これをおこなうには、 [!UICONTROL Salesforce] >[!UICONTROL 設定] > [!UICONTROL インストール済みパッケージ].
1. リードページレイアウトを編集し、 **[!DNL Marketo Measure]A/B テスト** ページに関連するリスト。

   ![](assets/1.png)

1. 次をクリック： [!UICONTROL レンチ] 」ボタンをクリックします。 選択したフィールドのリストから在庫「ID」フィールドを削除します。 追加 **[!UICONTROL 実験]**, **[!UICONTROL バリエーション]**、および **[!UICONTROL DateReported]** フィールド。 &quot;[!UICONTROL 並べ替え基準]」から **[!UICONTROL 報告日]**&#x200B;を選択し、 **[!UICONTROL 降順]** 」と入力します。

   ![](assets/2.png)

1. の下 [!UICONTROL ボタン]，オフ **[!UICONTROL 新規]**.

   ![](assets/3.png)

1. お問い合わせ [!DNL Marketo Measure] rep または [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target=&quot;_blank&quot;} をクリックして、この機能を有効にします。

## レポート {#reporting}

お客様は、 [!DNL Marketo Measure] リード、連絡先、商談に関する A/B テストのレポートを可能にする A/B レポートタイプ：

* [!DNL Marketo Measure] A/BTests
* [!DNL Marketo Measure] 連絡先との A/B テスト
* [!DNL Marketo Measure] リードを持つ A/B テスト
* [!DNL Marketo Measure] 商談を伴う A/B テスト

![](assets/4.png)

A/B レポートタイプは、A/B テストにさらされたリード、連絡先、または商談に関するレポートに使用します。 また、これらのレポートは、A/B テストにさらされた商談に結び付けられた売上高を示すことができます。

Optimizely/VWO は、マーケティングチャネルではなく、コンテンツのバリエーションプラットフォームであることに注意する必要があります。 したがって、これらは [!DNL Marketo Measure] A/B レポートタイプの使用方法は、購入者タッチポイントレポートとは異なります。 購入者のタッチポイントレポートタイプは、リードまたは連絡先が特定のページに導いたマーケティングチャネル（有料広告、Web 直接、ソーシャルなど）を把握するために使用します。 しかし、 [!DNL Marketo Measure] A/B レポートタイプは、バリエーションがリードや商談に与えた影響をレポートする場合には使用できません。 さらに、A/B テストのバリエーションはチャネルではないので、バリエーションの詳細は購入者のタッチポイントには表示されません。

次に、A/B テストのレポートを作成して明確性と洞察を高める際に使用する一般的なフィールドを示します。

* 変換済みリード
* 実験
* 実験 ID
* バリエーション
* バリエーション ID
* 報告日

## [!DNL Salesforce] サンプルレポート {#salesforce-example-reports}

**[!DNL Marketo Measure]リード付き A/B テスト**

![](assets/5.png)

**[!DNL Marketo Measure]商談を含む A/B テスト**

![](assets/6.png)
