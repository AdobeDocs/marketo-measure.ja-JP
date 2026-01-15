---
description: 入札管理ツールがMarketo Measure ユーザーに与える影響  [!DNL Marketo Measure]  ガイダンス
title: 入札管理ツールの [!DNL Marketo Measure] への影響
exl-id: 67c00ad9-8b12-4238-8a1f-2d2f5ed04423
feature: APIs, Integration, UTM Parameters
source-git-commit: 0299ef68139df574bd1571a749baf1380a84319b
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 4%

---

# 入札管理ツールが [!DNL Marketo Measure] に与える影響 {#how-bid-management-tools-affect-marketo-measure}

入札管理プラットフォームが AdWords と BingAds を追跡する [!DNL Marketo Measure] 機能にどのように影響するか、また、すべてが正しく追跡されるようにパラメーターを使用してトラッキングテンプレートを設定する方法について説明します。

Kenshoo と Marin は、マーケターが様々な検索エンジンで広告キャンペーンを追跡、管理、最適化できる優れたツールです。 これらの広告 URL に [!DNL Marketo Measure] パラメーターを追加するには、[!DNL Marketo Measure] パラメーターを使用してトラッキングテンプレートを設定する必要があります。 広告プラットフォームを [!DNL Marketo Measure] アカウントに接続して自動タグ付けを有効にすることはできません。これにより、[!DNL Marketo Measure] タグ付けシステムが Kenshoo/Marin のタグ付けシステムと競合するからです。 その結果、パラメーターが変更され、誤って追加されます。 これを回避するには、パラメーターが [!DNL Marketo Measure] のトラッキングテンプレートを Kenshoo と Marin 内で設定する必要があります。

## [!DNL Adwords] アカウント用 {#for-adwords-accounts}

追跡テンプレートを次のように設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* サイドナビゲーションバーの **[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* **URL オプション** をクリックします。
* 「トラッキングテンプレート」の横にある **編集** をクリックします。
* 次の URL に入力します。

   * すべての広告 URL に「?」が含まれる場合 その中で、次の URL を使用します。
      * `{lpurl}&_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`
   * 広告 URL に「?」が含まれていない場合 その中で、次の URL を使用します。
      * `{lpurl}?_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`


## [!DNL Bing Ads] アカウント用 {#for-bing-ads-accounts}

追跡テンプレートを次のように設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* サイドナビゲーションバーの **[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* **URL オプション** をクリックします。
* 「トラッキングテンプレート」の横にある **編集** をクリックします。
* 次の URL に入力します。

   * すべての広告 URL に「?」が含まれる場合 その中で、次の URL を使用します。
      * `{lpurl}&_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
   * 広告 URL に「?」が含まれていない場合 その中で、次の URL を使用します。
      * `{lpurl}?_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
