---
unique-page-id: 18874608
description: '"[!DNL Marketo Measure] パラメーター — [!DNL Marketo Measure]  — 製品ドキュメント»'
title: "[!DNL Marketo Measure] パラメーター"
exl-id: d66b9864-0d7e-455a-ae20-cca555f4d8c8
source-git-commit: 65e7f8bc198ceba2f873ded23c94601080ad0546
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 5%

---

# [!DNL Marketo Measure] パラメーター {#marketo-measure-parameters}

## [!DNL Marketo Measure] パラメータの説明 {#marketo-measure-parameters-explained}

UTM の使用からより深い洞察を得るには、 [!DNL Marketo Measure] で広告にカスタムパラメーターを追加します。 [!DNL Google] AdWords、Bing Ads および [!DNL Facebook] 広告。 [!DNL Marketo Measure] は、これらのプラットフォームと統合されており、ほとんどの設定プロセスを自動化します。 自動タグ付けの使用を選択した場合、 [!DNL Marketo Measure] は、広告の URL に自動的にパラメーターを追加します。 [!DNL Marketo Measure] また、はマーケティングコストをプラットフォームから自動的にダウンロードし、 [!DNL Marketo Measure] アプリを使用します。

パラメーターのない URL の例：

`http://adobe.com/landing-page?myParam=foo`

を含む URL の例 [!DNL Marketo Measure] パラメータ：

`http://adobe.com/landing-page?myParam=foo&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

## AdWords パラメーター {#adwords-parameters}

* `_bk={keyword}`
   * 検索エンジンで使用された人物のキーワードを表します。
   * これは、UTM 用語パラメーターに似ています。

* `_bt={creative}`
   * クリエイティブ ID または名前を表します。
   * これは、UTM コンテンツパラメーターに似ています。

* `_bm={matchtype}`
   * キーワードがどの程度近くに一致したかを表します。
   * キーワード一致タイプは、広告のトリガー検索を制御するのに役立ちます。 例えば、広告を広範なオーディエンスに対して表示する場合は部分一致を使用し、特定の顧客グループに対しては完全一致を使用します。
   * 次の 3 つの一致タイプがあります。広く、曖昧で正確な

>[!NOTE]
>
>一致タイプの詳細は、次のとおりです。 [関連する AdWords の記事を以下に示します](https://support.google.com/adwords/answer/2497836?hl=ja){target="_blank"}.

* `_bn={network}`
   * 広告ネットワークタイプを表します — [表示または検索](https://support.google.com/adwords/answer/1752334?hl=ja){target="_blank"}.
   * これは、UTM Source パラメーターに似ています。

* `_bg={adgroupID}`
   * 広告が属する広告グループの ID を表します

## Bing Ads のパラメーター {#bing-ads-parameters}

* `_bt={adid}`
* `utm_medium=cpc`
* `utm_source=bing`
* `utm_term={keyword}`

## Facebook Parameters {#facebook-parameters}

* `_bf ={creative}`
   * クリエイティブ ID または名前を表します
