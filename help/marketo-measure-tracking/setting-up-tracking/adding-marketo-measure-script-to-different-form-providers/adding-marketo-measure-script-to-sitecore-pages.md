---
unique-page-id: 18874747
description: Sitecore ページへの [!DNL Marketo Measure]  スクリプトの追加 –  [!DNL Marketo Measure]
title: Sitecore ページへの [!DNL Marketo Measure] スクリプトの追加
exl-id: 87ce1857-7532-45a7-8c39-255c6118b50a
feature: Tracking
TQID: https://experienceleague.adobe.com/sXO-rCY3NbxX0AztYt-o3f-tpJFlrncLIb7-NvEjZO0
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 3%

---

# Sitecore ページへの[!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-to-sitecore-pages}

コンテンツ管理システムは、フォーム送信を認識するために、[!DNL Marketo Measure]の標準スクリプト実装を超える追加の手順を必要とする場合があります。 以下のプロセスでは、[!DNL Marketo Measure] JavaScriptを[!DNL Sitecore] ページに追加する方法の概要を説明します。

Sitecore ページを含むサイトの場合：

1. Sitecoreにログインし、web サイトに移動します。 [!UICONTROL  ホーム ]項目および[!UICONTROL  メタデータ ] フォルダーと同じレベルにある[!UICONTROL 構成] フォルダーを探します。
1. [!UICONTROL Configuration] フォルダーの横にある&#x200B;**[!UICONTROL +]**&#x200B;をクリックします。
1. [!UICONTROL  ツール ] フォルダーの横にある&#x200B;**[!UICONTROL +]**&#x200B;をクリックします。
1. [!UICONTROL Javascript]項目を選択します。
1. 「[!UICONTROL  コンテンツ ]」タブで、「**[!UICONTROL ロックして編集]**」リンクをクリックして、編集用のアイテムのロックを解除します。
1. 「[!UICONTROL &#39;JavaScript&#39;]」セクションを検索します。 まだ展開されていない場合は、**[!UICONTROL +]**&#x200B;をクリックします。
1. 次のスクリプトを入力してください：`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js"async=""></script>`
1. 左上隅の「**[!UICONTROL 保存]**」をクリックします。
