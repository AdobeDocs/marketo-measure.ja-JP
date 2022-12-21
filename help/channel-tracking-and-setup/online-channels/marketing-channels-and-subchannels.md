---
unique-page-id: 18874682
description: マーケティングチャネルとサブチャネル — [!DNL Marketo Measure]  — 製品ドキュメント
title: マーケティングチャネルとサブチャネル
exl-id: fbe2a994-cf6d-439c-af96-a562216434cc
source-git-commit: 02f686645e942089df92800d8d14c76215ae558f
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 3%

---

# マーケティングチャネルとサブチャネル {#marketing-channels-and-subchannels}

## 目的 {#purpose}

チャネルとサブチャネルを定義するには [!DNL Marketo Measure]、コンテンツに対する関係、2 つの分類の違い、 [!DNL Marketo Measure] アプリを使用します。

## 概要 {#overview}

マーケティングチャネルは、レポートを簡単にするために、マーケティングアクティビティを分類（「バケット」）するのに使用されます ( 両方とも [!DNL Marketo Measure] ROI ダッシュおよび CRM 内。 [!DNL Marketo Measure] には、標準搭載のチャネル（組織の規則に合わせてカスタマイズしたり名前を変更したりできます）と、より詳細なフィルタリング用にカスタムチャネルをさらに作成する機能が付属しています。

サイトのコンテンツページの 1 人に対する訪問者を受け取ると（そのコンテンツが Web ページ、ホワイトペーパーのダウンロード、ページの URL など）、そのリードは URL にある複数の UTM パラメーターに基づいてチャネル/サブチャネルに「グループ化」されます。

* 中
* ソース
* キャンペーン
* ランディングページ
* 参照元サイト

リードを UTM パラメーターに基づいて分類する「バケット」をカスタマイズするには、チャネルルールを使用します。 チャネルルールの設定と管理について詳しくは、 [ここをクリック](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md).

設定方法 [オンラインチャネル](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md) および [オフラインチャネル](/help/channel-tracking-and-setup/offline-channels/offline-custom-channel-setup.md)そして、両者の違いも同様です。

**マーケティングチャネル**

マーケティングチャネルは最も幅広いレベルの分類で、様々なサブチャネルをカバーできます。 これらを、リードが来ているサブチャネルの「タイプ」と見なすことができます。 マーケティングチャネルの例を次に示します。 **有料検索、オーガニック検索、表示、** および **有料ソーシャル**. マーケティングチャネルは、通常、URL にある utm_medium パラメーター値に対応します。

**サブチャネル**

サブチャネルは、着信リードをグループ化する際のパズルの 2 番目の部分です。 サブチャネルは、 _which_ マーケティングチャネルの反復が使用されていました。 例えば、有料ソーシャルマーケティングチャネル内には、 **AdWords**, **BingAds**, **Facebook**&#x200B;など Subchannel は通常、URL にある utm_source パラメーター値に対応します。

## 使用例 {#use-case-example}

次の図は、次の URL を持つ Web ページに基づくマーケティングチャネル、サブチャネル、コンテンツの例を示しています。

* [http://info.bizible.com/intro-guide-b2b-marketing-attribution?utm_source=linkedin&amp;utm_medium=paidsocial](http://info.bizible.com/intro-guide-b2b-marketing-attribution?utm_source=linkedin&amp;utm_medium=paidsocial)*

この場合、ユーザーがアクセスしようとしているコンテンツは、B2B マーケティングアトリビューションの概要ガイドです。 [!DNL Marketo Measure] は、この組織で設定されたチャネルルールを使用して、このコンテンツへの URL を分析し、それらを使用して、マーケティングチャネル「有料ソーシャル」とサブチャネル「LinkedIn」にリードを「バケット」する。

![](assets/1.jpg)

その他の例…

**マーケティングチャネル（中）**

* PPC
* 有料ソーシャル
* オーガニックソーシャル
* メール
* イベントと会議
* オーガニック検索/SEO
* PR
* 紹介プログラム

**サブチャネル（タッチポイントソース）**

* Google AdWords
* BingAds
* Facebook 広告
* Adroll
* ダブルクリック
* カプテラ
* ドリップキャンペーン
* linkedIn Ads

**コンテンツ（ホワイトペーパー、ページの URL、ブログ投稿）**

* www.adobe.com/blog1
* www.adobe.com/whitepaper
* www.adobe.com/sign-up-now
