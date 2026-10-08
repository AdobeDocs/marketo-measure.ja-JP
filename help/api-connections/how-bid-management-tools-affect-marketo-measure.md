---
description: 入札管理ツールが[!DNL Marketo Measure] ガイダンスに与える影響（Marketo Measure ユーザー向け）
title: 入札管理ツールが[!DNL Marketo Measure]に与える影響
exl-id: 67c00ad9-8b12-4238-8a1f-2d2f5ed04423
feature: APIs, Integration, UTM Parameters
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: fb43f4c1-87d9-4081-8df1-6fe7e6e5cdc8
    internal-label: APIs
  - id: 7da342c5-06ee-5869-b3e8-b73d5bf75a9d
    internal-label: Integration
  - id: 3968a9c0-3e19-5a76-a1f0-f5a9a986c53a
    internal-label: UTM Parameters
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 2%
---
# 入札管理ツールが[!DNL Marketo Measure]に与える影響 {#how-bid-management-tools-affect-marketo-measure}

入札管理プラットフォームがAdWordsとBingAdsを追跡する[!DNL Marketo Measure]機能にどのような影響を与えるか、また、すべてのトラッキングを正しく行えるようにパラメーターを使用してトラッキングテンプレートを設定する方法について説明します。

KenshooとMarinは、マーケターが様々な検索エンジンで広告キャンペーンを追跡、管理、最適化できる優れたツールです。 これらの広告URLに[!DNL Marketo Measure] パラメーターを追加するには、[!DNL Marketo Measure] パラメーターを使用してトラッキングテンプレートを設定する必要があります。 広告プラットフォームを[!DNL Marketo Measure] アカウントに接続して自動タグ付けを有効にすることはできません。[!DNL Marketo Measure] タグ付けシステムは、Kenshoo/Marinのタグ付けシステムと競合します。 これにより、パラメーターが変更され、誤って追加されます。 これを回避するには、[!DNL Marketo Measure]個のパラメーターを持つトラッキングテンプレートをKenshooとMarin内で設定する必要があります。

## [!DNL Adwords] アカウント用 {#for-adwords-accounts}

トラッキングテンプレートを次のように設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* サイドナビゲーションバーの&#x200B;**[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* 「**URL オプション**」をクリックします。
* 「トラッキングテンプレート」の横にある「**編集**」をクリックします。
* URLを入力します。

  * すべての広告URLに「?」がある場合 その中で、次のURLを使用します。
    * `{lpurl}&_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`
  * 広告URLに「?」がない場合 その中で、次のURLを使用します。
    * `{lpurl}?_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`


## [!DNL Bing Ads] アカウント用 {#for-bing-ads-accounts}

トラッキングテンプレートを次のように設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* サイドナビゲーションバーの&#x200B;**[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* 「**URL オプション**」をクリックします。
* 「トラッキングテンプレート」の横にある「**編集**」をクリックします。
* URLを入力します。

  * すべての広告URLに「?」がある場合 その中で、次のURLを使用します。
    * `{lpurl}&_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
  * 広告URLに「?」がない場合 その中で、次のURLを使用します。
    * `{lpurl}?_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
