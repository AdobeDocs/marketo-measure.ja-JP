---
unique-page-id: 18874720
description: 入札管理ツールが及ぼす影響 [!DNL Marketo Measure] - [!DNL Marketo Measure]
title: 入札管理ツールの [!DNL Marketo Measure] への影響
exl-id: 67c00ad9-8b12-4238-8a1f-2d2f5ed04423
feature: APIs, Integration, UTM Parameters
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# 入札管理ツールが及ぼす影響 [!DNL Marketo Measure] {#how-bid-management-tools-affect-marketo-measure}

入札管理プラットフォームが [!DNL Marketo Measure] AdWords と BingAds を追跡する機能と、すべてを正しく追跡するために、パラメーターを使用してトラッキングテンプレートを設定する方法。

Kenshoo と Marin は、マーケターが様々な検索エンジンを使用して広告キャンペーンを追跡、管理、最適化できる優れたツールです。 次の条件を満たすため [!DNL Marketo Measure] これらの広告 URL に追加するパラメーターは、 [!DNL Marketo Measure] パラメーター。 広告プラットフォームを [!DNL Marketo Measure] アカウントを作成し、自動タギングを有効にします。 [!DNL Marketo Measure] タグ付けシステムを使用して、Kenshoo/Marin のタグ付けシステムと競合します。 その結果、パラメーターが変更され、誤って追加されます。 これを回避するには、 [!DNL Marketo Measure] パラメーターは Kenshoo と Marin 内で設定する必要があります。

## の場合 [!DNL Adwords] アカウント {#for-adwords-accounts}

次のようにトラッキングテンプレートを設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* 次をクリック： **[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* クリック **URL オプション**.
* 「トラッキングテンプレート」の横の「 **編集**.
* 次の URL を入力します。

   * すべての広告の URL に「?」が含まれている場合 その際に、次の URL を使用します。
      * `{lpurl}&_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`
   * どの広告 URL にも「?」 その際に、次の URL を使用します。
      * `{lpurl}?_bk={keyword}&_bt={creative}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`


## の場合 [!DNL Bing Ads] アカウント {#for-bing-ads-accounts}

次のようにトラッキングテンプレートを設定します。

* 「**[!UICONTROL キャンペーン]**」タブをクリックします。
* 次をクリック： **[!UICONTROL 共有ライブラリ]** リンクをクリックします。
* クリック **URL オプション**.
* 「トラッキングテンプレート」の横の「 **編集**.
* 次の URL を入力します。

   * すべての広告の URL に「?」が含まれている場合 その際に、次の URL を使用します。
      * `{lpurl}&_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
   * どの広告 URL にも「?」 その際に、次の URL を使用します。
      * `{lpurl}?_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`
