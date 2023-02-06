---
unique-page-id: 18874797
description: 追加中 [!DNL Marketo Measure] スクリプト経由 [!DNL Google Tag Manager] - [!DNL Marketo Measure]  — 製品ドキュメント
title: 追加中 [!DNL Marketo Measure] スクリプト経由 [!DNL Google Tag Manager]
exl-id: 539efb10-35cb-4146-8eea-728c3948a11e
source-git-commit: 82cc8269bfdb26b6acf039d0ce0e06564f5e2612
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# 追加中 [!DNL Marketo Measure] スクリプト経由 [!DNL Google Tag Manager] {#adding-marketo-measure-script-via-google-tag-manager}

をインストールする際 [!DNL Marketo Measure] javascript、 [スクリプトのハードコーディング](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md){target="_blank"} を直接サイトに貼り付けます。 ただし、それが不可能な場合は、 [!DNL Google Tag Manager] (GTM) を使用して [!DNL Marketo Measure] JS. 注意： [!DNL Marketo Measure] GTM を介して読み込まれる JS は、遅延の影響を受けやすくなります。 遅延により、スクリプトの読み込み時間が遅延し、すべてのフォーム送信の約 3 ～ 5%が欠落する可能性があります。

GTM を使用してスクリプトを追加する場合は、 [!DNL Marketo Measure] スクリプトを実行順序で最も優先度が高く、 [!DNL Marketo Measure] タグを使用して、GTM の遅延による影響を減らすことができます。

>[!NOTE]
>
>これを使用してください [Googleの支援記事](https://support.google.com/tagmanager/answer/2772421?hl=ja){target="_blank"} を参照してください。

## 追加方法 [!DNL Marketo Measure] 経由での JS [!DNL Google Tag Manager] {#how-to-add-marketo-measure-js-via-google-tag-manager}

1. GTM を開き、 [!DNL Marketo Measure] スクリプトを web サイトコンテナに追加します。 必ず **[!UICONTROL カスタムHTMLタグ]**.

1. 以下を使用： [!DNL Marketo Measure] 以下のスクリプトを作成し、コンテナに組み込みます。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. クリック **[!UICONTROL 実行ルールの追加]** そのため、Googleにスニペットを読み込むように指示できます。 *すべてのページ*.

1. 左側の「コンテナドラフトの概要」セクションに移動します。 「 」ボタンをクリックして、コンテナの新しいバージョンを作成し、変更を公開します。
