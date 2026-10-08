---
description: Marketo Measure ユーザー向けのUnbounce Script Manager ガイダンスに[!DNL Marketo Measure]を接続しています
title: '[!DNL Marketo Measure]をバウンス解除スクリプト マネージャーに接続しています'
exl-id: c3212bc3-1d8f-4da5-bb2d-11ffd2fb4e98
feature: Tracking
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: dcbeff6e-0253-5a4b-9ac2-1b67cc4a6286
    internal-label: Tracking
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 7%
---

# [!DNL Marketo Measure]をバウンス解除スクリプト マネージャーに接続しています {#connecting-marketo-measure-to-unbounce-script-manager}

[!DNL Marketo Measure]はバウンス解除と直接統合され、ランディングページのコンバージョンのデジタルマーケティングソースを[!DNL Salesforce]で直接追跡できます。 接続するには、バウンス解除スクリプトマネージャーに[!DNL Marketo Measure] スクリプトを追加するだけです。 手順は次のとおりです。

1. [!DNL Unbounce] アカウントにログインします。
1. **[!UICONTROL 設定]** > **[!UICONTROL Script Manager]** > **[!UICONTROL スクリプトを追加]**&#x200B;をクリックします。
1. ポップアップで「[!UICONTROL  カスタムスクリプト ]」を選択し、「[!DNL Marketo Measure Marketing Analytics]」という名前を付けます。 「**[!UICONTROL スクリプトの詳細を追加]**」をクリックします。
1. ヘッドの配置を選択します。 メインランディングページとフォーム確認ダイアログにスクリプトを含めます。 下の[!DNL Marketo Measure] スクリプトをボックスに貼り付けます。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 保存]**」をクリックします。

[!DNL Marketo Measure]統合は、unbounce.com ドメインを使用していないドメイン（landing.mysite.comなど）でホストされている限り、バウンス解除ランディングページで機能します。
