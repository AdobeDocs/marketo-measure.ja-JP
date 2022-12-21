---
unique-page-id: 18874720
description: 入札管理ツールの影響 [!DNL Marketo Measure] - [!DNL Marketo Measure]  — 製品ドキュメント
title: 入札管理ツールの影響 [!DNL Marketo Measure]
exl-id: 67c00ad9-8b12-4238-8a1f-2d2f5ed04423
source-git-commit: 65e7f8bc198ceba2f873ded23c94601080ad0546
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# 入札管理ツールの影響 [!DNL Marketo Measure] {#how-bid-management-tools-affect-marketo-measure}

入札管理プラットフォームが [!DNL Marketo Measure] AdWords と BingAds を追跡する機能と、すべてを正しく追跡するために、パラメーターを使用してトラッキングテンプレートを設定する方法。

Kenshoo と Marin は、マーケターが様々な検索エンジンを使用して広告キャンペーンを追跡、管理、最適化できる優れたツールです。 次のために [!DNL Marketo Measure] これらの広告 URL に追加するパラメーターは、 [!DNL Marketo Measure] パラメーター。 広告プラットフォームを [!DNL Marketo Measure] アカウントを作成し、自動タギングを有効にします。 [!DNL Marketo Measure] タグ付けシステムを使用して、Kenshoo/Marin のタグ付けシステムと競合します。 その結果、パラメーターが変更され、誤って追加されます。 これを回避するには、 [!DNL Marketo Measure] パラメーターは Kenshoo と Marin 内で設定する必要があります。

## の場合 [!DNL Adwords] アカウント {#for-adwords-accounts}

次のようにトラッキングテンプレートを設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* 次をクリック： **[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* クリック **URL オプション**.
* 「トラッキングテンプレート」の横の **編集**.
* URL を入力します。

   * すべての広告の URL に「?」が含まれている場合 その際に、次の URL を使用します。
      * `{lpurl}&_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`
   * どの広告 URL にも「?」 その際に、次の URL を使用します。
      * `{lpurl}?_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`


## の場合 [!DNL Bing Ads] アカウント {#for-bing-ads-accounts}

次のようにトラッキングテンプレートを設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* 次をクリック： **[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* クリック **URL オプション**.
* 「トラッキングテンプレート」の横の **編集**.
* URL を入力します。

   * すべての広告の URL に「?」が含まれている場合 その際に、次の URL を使用します。
      * `{lpurl}&_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
   * どの広告 URL にも「?」 その際に、次の URL を使用します。
      * `{lpurl}?_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
