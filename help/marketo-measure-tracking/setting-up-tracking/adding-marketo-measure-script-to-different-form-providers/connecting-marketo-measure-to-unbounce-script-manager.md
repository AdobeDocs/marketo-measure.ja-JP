---
unique-page-id: 18874743
description: 接続中 [!DNL Marketo Measure] スクリプトマネージャをバウンス解除するには — [!DNL Marketo Measure]  — 製品ドキュメント
title: Unbounce Script Manager への [!DNL Marketo Measure] の接続
exl-id: c3212bc3-1d8f-4da5-bb2d-11ffd2fb4e98
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 11%

---

# Unbounce Script Manager への[!DNL Marketo Measure]の接続 {#connecting-marketo-measure-to-unbounce-script-manager}

[!DNL Marketo Measure] を Unbounce と直接統合すると、ランディングページのコンバージョンを [!DNL Salesforce]. 接続を確立するには、 [!DNL Marketo Measure] スクリプトをバウンス解除スクリプトマネージャに追加します。 手順は以下のとおりです。

1. にログインします。 [!DNL Unbounce] アカウント。
1. クリック **[!UICONTROL 設定]** > **[!UICONTROL スクリプトマネージャ]** > **[!UICONTROL スクリプトを追加]**.
1. ポップアップで、 [!UICONTROL カスタムスクリプト] そして、&quot;という名前を付けます。[!DNL Marketo Measure Marketing Analytics].&quot; クリック **[!UICONTROL スクリプトの詳細を追加]**.
1. ヘッドの配置を選択します。 メインのランディングページとフォームの確認ダイアログにスクリプトを含めます。 を貼り付けます。 [!DNL Marketo Measure] スクリプトをボックスに追加します。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 保存]**」をクリックします。

The [!DNL Marketo Measure] 統合は、unbounce.comドメインを使用しているドメイン ( 例：landing.mysite.com) でホストされていない限り、バウンス解除のランディングページで機能します。
