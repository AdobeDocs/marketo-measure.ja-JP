---
unique-page-id: 18874781
description: アトリビューションを使用した Doubleclick Campaign Manager ビューの設定 –  [!DNL Marketo Measure]
title: Doubleclick Campaign Manager ビュースルーアトリビューションの設定
exl-id: 2cc6c2cd-afb7-4052-b18b-9ad0bf16a9fa
feature: Attribution
source-git-commit: 48962b999fdd16fe96d18708ec301e64a39bc76e
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 27%

---

# Doubleclick Campaign Manager ビュースルーアトリビューションの設定 {#configuring-doubleclick-campaign-manager-view-through-attribution}

## アトリビューションによるビューの測定 {#measuring-view-through-attribution}

>[!IMPORTANT]
>
>プライバシーに関する懸念により、サードパーティ Cookie は廃止されます。Google Chrome が 2024 年第 3 四半期に発表したサードパーティ Cookie の廃止は、事実上、この形式のトラッキングの終了を意味します。その結果、アドビでは、サードパーティ Cookie に依存する Marketo Measure 機能、特に、Google／DoubleClick インプレッション Cookie を使用するクロスドメイントラッキングとビュースルーアトリビューションを廃止します。Marketo Measure のその他の機能に影響はありません。また、ファーストパーティ cookie の使用にも影響はありません。Google のスケジュールを考慮すると、上記 2 つの機能の廃止予定日は 2024年6月1日（PT）です。この日付より前に収集された関連データは、アドビのお客様が引き続き使用できます。

>[!NOTE]
>
>を使用する場合 [!DNL Marketo Measure] および [!DNL DoubleClick Campaign Manager] 統合するには、 [API 接続](/help/api-connections/utilizing-marketo-measures-api-connections/integrated-ad-platforms.md#how-to-connect-ad-platforms) そのため、広告を解決するキャンペーンとクリエイティブの詳細をダウンロードできます。

を使用して、ビューからトラッキングに至るまでより詳細なインサイトを得るには [!DNL Doubleclick Campaign Manager]を設定する必要があります。

について [!DNL Marketo Measure] アトリビューションによる表示機能については、を参照してください。 [Marketo Measure ビュースルー属性に関するよくある質問](/help/advanced-marketo-measure-features/view-through-attribution/marketo-measure-view-through-attribution-faq.md).

[!DNL Marketo Measure] は、DCM 広告タグを介したサードパーティの呼び出しであるため、ピギーバックタグと見なされます。 ピギーバックタグは、画像タグでは機能しません。iframe タグまたは JavaScript タグのみです。 DCM サポートによると、これは最近変更されておらず、常にそうでした。 標準タグは 2017 年 10 月 2 日（PT）に非推奨（廃止予定）となりましたが、の機能には影響しません [!DNL Marketo Measure] インプレッション数をトラッキングする

DCM で親子階層を使用する場合は、インプレッショントラッキングのためにすべてのレベルにタグを適用する必要があります。

## 画像タグの追加方法 {#how-to-add-the-image-tag}

広告主設定の下の Doubleclick にタグを追加し、インプレッションイベントタグを作成します。

1. 次のコードを 1 x 1 画像ピクセルとして追加します。

`https://cdn.bizibly.com/i?v=%eadv!&a=%eaid!&c=%ecid!&s=%esid!&p=%epid!&m=%m&n=%n`

1. 追加したら、次のように区切り文字がマッピングされていることを確認します。 タグを適用したら、これは自動的に行われます。

   v = %eadv! [!DNL Expand] 広告主 Id\
   a = %eaid! 広告 Id を展開\
   c = %ecid! クリエイティブ Id を展開\
   s = %esid! サイト Id を展開\
   p = %epid! プレースメント Id を展開\
   m = %m マッチ コード マクロ\
   n = %n 乱数マクロ

   ![](assets/1.png)

## よくある質問 {#faq}

**Q：画像タグは保護されていますか？**

A：はい。 JavaScript タグではなく、画像タグです。

**Q：接続されたユーザーに必要な権限は何ですか？**

A:dfatrafficking、dfareporting、userinfo.email

**Q：費用データのインポートにはどのくらいの時間がかかりますか？**

A：最大 6 時間

**Q：広告データのインポートにはどのくらいの時間がかかりますか？**

A：最大 6 時間
