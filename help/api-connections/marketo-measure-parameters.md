---
description: '[!DNL Marketo Measure] パラメーター –  [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] パラメーター'
exl-id: d66b9864-0d7e-455a-ae20-cca555f4d8c8
feature: APIs, Integration, UTM Parameters
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 64%

---


# [!DNL Marketo Measure] パラメーター {#marketo-measure-parameters}

## [!DNL Marketo Measure] パラメーターの説明 {#marketo-measure-parameters-explained}

UTM の使用からさらにinsightを得るには、[!DNL Marketo Measure] で [!DNL Google] AdWords、Bing Ads および [!DNL Facebook] Ads の広告にカスタムパラメーターを追加します。[!DNL Marketo Measure] は、これらのプラットフォームと統合して、設定プロセスのほとんどを自動化します。 自動タギングを使用する [!DNL Marketo Measure] とを選択すると、広告の URL にパラメーターが自動的に追加されます。[!DNL Marketo Measure] また、は、プラットフォームからマーケティングコストを自動的にダウンロードし、[!DNL Marketo Measure] アプリに読み込みます。

パラメーターを含まない URL の例：

`http://adobe.com/landing-page?myParam=foo`

[!DNL Marketo Measure] パラメーターを含む URL の例：

`http://adobe.com/landing-page?myParam=foo&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

## AdWords パラメーター {#adwords-parameters}

* `_bk={keyword}`
   * ユーザが検索エンジンで使用したキーワードを表します。
   * UTM 用語パラメーターに似ています。

* `_bt={creative}`
   * クリエイティブ ID または名前を表します。
   * UTM コンテンツパラメーターに似ています。

* `_bm={matchtype}`
   * キーワードの一致レベルを表します。
   * キーワード一致タイプは、広告をトリガーする検索を制御するのに役立ちます。 例えば、部分一致を使用して広範なオーディエンスに広告を表示することや、完全一致を使用して特定の顧客グループに絞り込むことができます。
   * 部分一致、あいまい一致、完全一致の 3 つの一致タイプがあります。

>[!TIP]
>一致タイプについて詳しくは、[ 関連する AdWords 記事を参照 ](https://support.google.com/adwords/answer/2497836?hl=ja){target="_blank"} してください。

* `_bn={network}`
   * 広告ネットワークのタイプ [ 表示または検索 ](https://support.google.com/adwords/answer/1752334?hl=ja){target="_blank"} を表します。
   * UTM ソースパラメーターに似ています。

* `_bg={adgroupID}`
   * 広告が属する広告グループの ID を表します

>[!NOTE]
>リダイレクト URL パラメーターはサポートしていません。

## Bing Ads パラメーター {#bing-ads-parameters}

* `_bt={adid}`
* `utm_medium=cpc`
* `utm_source=bing`
* `utm_term={keyword}`

## Facebook パラメーター {#facebook-parameters}

* `_bf ={creative}`
   * クリエイティブ ID または名前を表します
