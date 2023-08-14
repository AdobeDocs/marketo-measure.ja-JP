---
unique-page-id: 18874797
description: ' [!DNL Google Tag Manager]  経由での  [!DNL Marketo Measure]  スクリプトの追加 - [!DNL Marketo Measure] - 製品ドキュメント'
title: ' [!DNL Google Tag Manager] 経由での  [!DNL Marketo Measure]  スクリプトの追加'
exl-id: 539efb10-35cb-4146-8eea-728c3948a11e
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 100%

---

# [!DNL Google Tag Manager] 経由での [!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-via-google-tag-manager}

[!DNL Marketo Measure] JavaScript をインストールする場合は、サイトに直接[スクリプトをハードコード](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md){target="_blank"}することを強くお勧めします。ただし、それが不可能な場合は、[!DNL Google Tag Manager]（GTM）を使用して [!DNL Marketo Measure] JS を読み込むこともできます。GTM 経由で読み込んだ [!DNL Marketo Measure] JS は待ち時間の影響を受けやすいことに注意してください。遅延によりスクリプトの読み込み時間に遅延が生じ、その結果、すべてのフォーム送信の約 3～5％が失われる可能性があります。

GTM 経由でスクリプトを追加する場合は、GTM の待ち時間による影響を軽減するために、[!DNL Marketo Measure] スクリプトを実行順序で最高の優先度に設定し、[!DNL Marketo Measure] タグの前に同期スクリプトがないことを確認してください。

>[!NOTE]
>
>詳しくは、この [Google によるサポート記事](https://support.google.com/tagmanager/answer/2772421?hl=ja){target="_blank"}を参照してください。

## [!DNL Google Tag Manager] 経由での [!DNL Marketo Measure] JS の追加方法 {#how-to-add-marketo-measure-js-via-google-tag-manager}

1. GTM を開き、web サイトのコンテナに [!DNL Marketo Measure] スクリプトを追加します。**[!UICONTROL カスタム HTML タグ]**&#x200B;を選択する必要があります。

1. 以下の [!DNL Marketo Measure] スクリプトを使用して、コンテナに組み込みます。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 実行ルールを追加]**」をクリックします。これにより、*すべてのページ*&#x200B;にスニペットを読み込むように Google に指示できます。

1. 左側の「コンテナドラフトの概要」セクションに移動します。ボタンをクリックしてコンテナの新しいバージョンを作成し、変更を公開します。
