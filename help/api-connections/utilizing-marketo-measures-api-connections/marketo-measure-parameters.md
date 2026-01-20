---
unique-page-id: 18874608
description: '[!DNL Marketo Measure] パラメーター –  [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] パラメーター'
exl-id: d66b9864-0d7e-455a-ae20-cca555f4d8c8
feature: APIs, Integration, UTM Parameters
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 91%

---

# [!DNL Marketo Measure] パラメーター {#marketo-measure-parameters}

## [!DNL Marketo Measure] パラメーターの説明 {#marketo-measure-parameters-explained}

UTM の使用からさらにインサイトを取得するために、[!DNL Marketo Measure] では [!DNL Google] AdWords、Bing Ads、[!DNL Facebook] Ads の広告にカスタムパラメーターを追加します。[!DNL Marketo Measure] では、これらのプラットフォームと統合して、ほとんどの設定プロセスを自動化します。自動タグ付けの使用を選択した場合、[!DNL Marketo Measure] ではそのパラメーターを広告の URL に自動的に追加します。また、[!DNL Marketo Measure] では、マーケティングコストをプラットフォームから自動的にダウンロードし、[!DNL Marketo Measure] アプリに読み込みます。

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
   * キーワード一致タイプは、広告をトリガーする検索を制御するのに役立ちます。例えば、部分一致を使用して広範なオーディエンスに広告を表示することや、完全一致を使用して特定の顧客グループに絞り込むことができます。
   * 部分一致、あいまい一致、完全一致の 3 つの一致タイプがあります。

>[!TIP]
>
>一致タイプについて詳しくは、[&#x200B; 関連する AdWords 記事を参照 &#x200B;](https://support.google.com/adwords/answer/2497836?hl=ja){target="_blank"} してください。

* `_bn={network}`
   * 広告ネットワークのタイプ [&#x200B; 表示または検索 &#x200B;](https://support.google.com/adwords/answer/1752334?hl=ja){target="_blank"} を表します。
   * UTM ソースパラメーターに似ています。

* `_bg={adgroupID}`
   * 広告が属する広告グループの ID を表します

>[!NOTE]
>
>リダイレクト URL パラメーターはサポートしていません。

## Bing Ads パラメーター {#bing-ads-parameters}

* `_bt={adid}`
* `utm_medium=cpc`
* `utm_source=bing`
* `utm_term={keyword}`

## Facebook パラメーター {#facebook-parameters}

* `_bf ={creative}`
   * クリエイティブ ID または名前を表します
