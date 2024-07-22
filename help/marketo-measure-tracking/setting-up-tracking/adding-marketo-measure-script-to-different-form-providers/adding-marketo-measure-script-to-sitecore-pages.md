---
unique-page-id: 18874747
description: Sitecore ペ  [!DNL Marketo Measure]  ジへのスクリプトの追加 –  [!DNL Marketo Measure]
title: Sitecore ページへの [!DNL Marketo Measure] スクリプトの追加
exl-id: 87ce1857-7532-45a7-8c39-255c6118b50a
feature: Tracking
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# Sitecore ページへ [!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-to-sitecore-pages}

コンテンツ管理システムでは、フォーム送信を認識するために、標準のスクリプト実装を超える追加の手順が必要 [!DNL Marketo Measure] なる場合があります。 次のプロセスでは、[!DNL Sitecore] ページに [!DNL Marketo Measure] JavaScript を追加する方法の概要を説明します。

Sitecore ページを使用しているサイトの場合：

1. Sitecore にログインし、web サイトに移動します。 [!UICONTROL  ホーム ] アイテムおよび [!UICONTROL  メタデータ ] フォルダーと同じレベルにある [!UICONTROL Configuration] フォルダーを見つけます。
1. [!UICONTROL Configuration] フォルダーの横にある **[!UICONTROL +]** をクリックします。
1. [!UICONTROL  ツール ] フォルダーの横にある **[!UICONTROL +]** をクリックします。
1. [!UICONTROL JavaScript] 項目を選択します。
1. 「[!UICONTROL  コンテンツ ]」タブで「**[!UICONTROL ロックして編集]**」リンクをクリックして、編集用に項目のロックを解除します。
1. [!UICONTROL  のJavaScriptの節を見つけ ] す。 まだ展開していない場合は、「**[!UICONTROL +]**」をクリックします。
1. スクリプト `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js"async=""></script>` を入力してください
1. 左上隅の **[!UICONTROL 保存]** をクリックします。
