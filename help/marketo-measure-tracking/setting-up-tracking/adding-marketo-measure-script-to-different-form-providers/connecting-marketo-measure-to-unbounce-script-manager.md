---
unique-page-id: 18874743
description: 接続中 [!DNL Marketo Measure] スクリプトマネージャをバウンス解除するには — [!DNL Marketo Measure]  — 製品ドキュメント
title: 接続中 [!DNL Marketo Measure] スクリプトマネージャをバウンス解除するには
exl-id: c3212bc3-1d8f-4da5-bb2d-11ffd2fb4e98
source-git-commit: ae5b77744d523606ce6cfcf48d7e8d5049d5ccb7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 接続中 [!DNL Marketo Measure] スクリプトマネージャをバウンス解除するには {#connecting-marketo-measure-to-unbounce-script-manager}

[!DNL Marketo Measure] を Unbounce と直接統合すると、ランディングページのコンバージョンを [!DNL Salesforce]. 接続を確立するには、 [!DNL Marketo Measure] スクリプトをバウンス解除スクリプトマネージャに追加します。 手順は以下のとおりです。

1. にログインします。 [!DNL Unbounce] アカウント
1. クリック **[!UICONTROL 設定]** > **[!UICONTROL スクリプトマネージャ]** > **[!UICONTROL スクリプトを追加]**.
1. ポップアップで、 [!UICONTROL カスタムスクリプト] そして、「[!DNL Marketo Measure Marketing Analytics].&quot; クリック **[!UICONTROL スクリプトの詳細を追加]**.
1. ヘッドの配置を選択します。 メインのランディングページとフォームの確認ダイアログにスクリプトを含めます。 貼り付け [!DNL Marketo Measure] スクリプトをボックスに追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 保存]**」をクリックします。

この [!DNL Marketo Measure] unbounce.com ドメインを使用していないドメイン（例：landing.mysite.com）でホストされている限り、統合はバウンス解除ランディングページで機能します。
