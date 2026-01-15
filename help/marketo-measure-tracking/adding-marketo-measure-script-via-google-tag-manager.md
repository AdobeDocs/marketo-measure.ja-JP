---
description: Marketo Measure ユーザー向け  [!DNL Marketo Measure]  スクリプ  [!DNL Google Tag Manager]  の追加 – ガイダンス
title: ' [!DNL Google Tag Manager] 経由での  [!DNL Marketo Measure]  スクリプトの追加'
exl-id: 539efb10-35cb-4146-8eea-728c3948a11e
feature: Tracking
hidefromtoc: true
source-git-commit: 0299ef68139df574bd1571a749baf1380a84319b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 83%

---

# [!DNL Google Tag Manager] 経由での [!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-via-google-tag-manager}

[!DNL Marketo Measure] JavaScriptをインストールする場合は、サイトに直接 [&#x200B; スクリプトをハードコード &#x200B;](/help/marketo-measure-tracking/adding-marketo-measure-script.md){target="_blank"} することをお勧めします。 不可能な場合は、[!DNL Google Tag Manager]（GTM）を使用して [!DNL Marketo Measure] JS を読み込むこともできます。GTM 経由で読み込んだ [!DNL Marketo Measure] JS は待ち時間の影響を受けやすいことに注意してください。遅延によりスクリプトの読み込み時間に遅延が生じ、その結果、すべてのフォーム送信の約 3～5％が失われる可能性があります。

GTM 経由でスクリプトを追加する場合は、GTM の待ち時間による影響を軽減するために、[!DNL Marketo Measure] スクリプトを実行順序で最高の優先度に設定し、[!DNL Marketo Measure] タグの前に同期スクリプトがないことを確認してください。

>[!NOTE]
>
>詳しくは、[Googleのサポート記事 &#x200B;](https://support.google.com/tagmanager/answer/2772421?hl=ja){target="_blank"} を参照してください。

## [!DNL Google Tag Manager] 経由での [!DNL Marketo Measure] JS の追加方法 {#how-to-add-marketo-measure-js-via-google-tag-manager}

1. GTM を開き、web サイトのコンテナに [!DNL Marketo Measure] スクリプトを追加します。**[!UICONTROL カスタム HTML タグ]**&#x200B;を選択する必要があります。

1. 以下の [!DNL Marketo Measure] スクリプトを使用して、コンテナに組み込みます。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 実行ルールを追加]**」をクリックします。これにより、*すべてのページ*&#x200B;にスニペットを読み込むように Google に指示できます。

1. 左側の「コンテナドラフトの概要」セクションに移動します。ボタンをクリックしてコンテナのバージョンを作成し、変更を公開します。
