---
unique-page-id: 18874797
description: 追加中 [!DNL Marketo Measure] スクリプト経由 [!DNL Google Tag Manager] - [!DNL Marketo Measure]
title: ' [!DNL Google Tag Manager] 経由での  [!DNL Marketo Measure]  スクリプトの追加'
exl-id: 539efb10-35cb-4146-8eea-728c3948a11e
feature: Tracking
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 59%

---

# [!DNL Google Tag Manager] 経由での [!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-via-google-tag-manager}

[!DNL Marketo Measure] JavaScript をインストールする場合は、サイトに直接[スクリプトをハードコード](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md){target="_blank"}することを強くお勧めします。ただし、不可能な場合は、 [!DNL Google Tag Manager] (GTM) を使用して [!DNL Marketo Measure] JS. 注意： [!DNL Marketo Measure] GTM を介して読み込まれる JS は、遅延の影響を受けやすくなります。 遅延によりスクリプトの読み込み時間に遅延が生じ、その結果、すべてのフォーム送信の約 3～5％が失われる可能性があります。

GTM を使用してスクリプトを追加する場合は、 [!DNL Marketo Measure] スクリプトを実行順序で最も優先度が高く、 [!DNL Marketo Measure] タグを使用して、GTM の遅延による影響を減らすことができます。

>[!NOTE]
>
>使用方法 [Googleの支援記事](https://support.google.com/tagmanager/answer/2772421?hl=ja){target="_blank"} を参照してください。

## [!DNL Google Tag Manager] 経由での [!DNL Marketo Measure] JS の追加方法 {#how-to-add-marketo-measure-js-via-google-tag-manager}

1. GTM を開き、web サイトのコンテナに [!DNL Marketo Measure] スクリプトを追加します。**[!UICONTROL カスタム HTML タグ]**&#x200B;を選択する必要があります。

1. 以下の [!DNL Marketo Measure] スクリプトを使用して、コンテナに組み込みます。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 実行ルールを追加]**」をクリックします。これにより、*すべてのページ*&#x200B;にスニペットを読み込むように Google に指示できます。

1. 左側の「コンテナドラフトの概要」セクションに移動します。ボタンをクリックしてコンテナの新しいバージョンを作成し、変更を公開します。
