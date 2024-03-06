---
unique-page-id: 18874781
description: アトリビューションを使用した Doubleclick Campaign Manager ビューの設定 — [!DNL Marketo Measure]
title: Doubleclick Campaign Manager ビュースルーアトリビューションの設定
exl-id: 2cc6c2cd-afb7-4052-b18b-9ad0bf16a9fa
feature: Attribution
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 4%

---

# Doubleclick Campaign Manager ビュースルーアトリビューションの設定 {#configuring-doubleclick-campaign-manager-view-through-attribution}

## 属性を通じたビューの測定 {#measuring-view-through-attribution}

>[!NOTE]
>
>を使用している場合、 [!DNL Marketo Measure] および [!DNL DoubleClick Campaign Manager] 統合、 [API 接続](/help/api-connections/utilizing-marketo-measures-api-connections/integrated-ad-platforms.md#how-to-connect-ad-platforms) 広告を解決するキャンペーンとクリエイティブの詳細をダウンロードできます。

を使用して、追跡を通じて、ビューからより詳細なインサイトを得るには [!DNL Doubleclick Campaign Manager]に値を指定する場合は、トラッキングピクセルを設定する必要があります。

詳しくは、 [!DNL Marketo Measure] ビュースルーアトリビューション機能： [Marketo Measureビュースルーアトリビューションに関する FAQ](/help/advanced-marketo-measure-features/view-through-attribution/marketo-measure-view-through-attribution-faq.md).

[!DNL Marketo Measure] は、DCM 広告タグを介したサードパーティ呼び出しなので、ピギーバックタグと見なされます。 ピギーバックタグは画像タグでは機能せず、iframe タグまたは javascript タグでのみ機能します。 DCM サポートによると、これは最近は変更されておらず、常にそのようでした。 標準タグは 2017 年 10 月 3 日に廃止されましたが、の機能には影響しません。 [!DNL Marketo Measure] インプレッション数を追跡する場合。

DCM で親と子の階層を使用する場合、インプレッション追跡のためにすべてのレベルにタグを適用する必要があります。

## イメージタグの追加方法 {#how-to-add-the-image-tag}

広告主設定の下で Doubleclick にタグを追加し、インプレッションイベントタグを作成します。

1. 次のコードを 1 x 1 画像ピクセルとして追加します。

`https://cdn.bizibly.com/i?v=%eadv!&a=%eaid!&c=%ecid!&s=%esid!&p=%epid!&m=%m&n=%n`

1. 区切り文字が追加されたら、次のようにマッピングされていることを確認します。 タグが適用されたら、これは自動的におこなわれる必要があります。

   v = %eadv! [!DNL Expand] 広告主 ID\
   a = %eaid! 広告 ID を展開\
   c = %ecid! クリエイティブ ID を展開\
   s = %esid! サイト ID を展開\
   p = %epid! 配置 ID を展開\
   m = %m マッチコードマクロ\
   n = %n 乱数マクロ

   ![](assets/1.png)

## よくある質問 {#faq}

**Q：イメージタグは安全ですか。**

A：はい。 これは JavaScript タグではなく、イメージタグです。

**Q：接続したユーザーに必要な権限は何ですか？**

A: dfaticking, dfareporting, userinfo.email

**Q：支出データのインポートにはどのくらいの時間がかかりますか。**

A：最大 6 時間

**Q：広告データのインポートにはどのくらい時間がかかりますか？**

A：最大 6 時間
