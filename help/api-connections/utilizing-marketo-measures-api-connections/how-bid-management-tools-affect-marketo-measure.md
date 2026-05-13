---
unique-page-id: 18874720
description: 入札管理ツールが [!DNL Marketo Measure] - [!DNL Marketo Measure]に与える影響
title: 入札管理ツールの [!DNL Marketo Measure] への影響
exl-id: 67c00ad9-8b12-4238-8a1f-2d2f5ed04423
feature: APIs, Integration, UTM Parameters
TQID: https://experienceleague.adobe.com/gcugeRrHUi4qetrYBpUavRyrBHVpB0qCzPo4OYMI4hw
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
feature_v2:
  - id: fb43f4c1-87d9-4081-8df1-6fe7e6e5cdc8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 265
ht-degree: 4%

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
