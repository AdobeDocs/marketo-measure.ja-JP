---
unique-page-id: 18874519
description: Lightbox Formsへの [!DNL Marketo Measure]  スクリプトの追加 –  [!DNL Marketo Measure]
title: Lightbox フォームへの [!DNL Marketo Measure] スクリプトの追加
exl-id: fa9ce480-fc4f-4abd-8555-dbb74849747e
feature: Tracking
TQID: https://experienceleague.adobe.com/FGsXJ6c98YinAH4rgzfySe0wNCkHb5AWH1KcZ6whnjA
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 2%

---

# Lightbox Formsへの[!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-to-lightbox-forms}

ライトボックス内のフォームに[!DNL Marketo Measure] JavaScriptを適切に追加する方法について説明します。

ライトボックスは、訪問者が特定のアクション（ページの特定の部分をクリックしたり、ページで特定の時間を過ごしたりなど）を実行すると、コンテンツの前にフォームを開きます。 通常、[!DNL Marketo Measure] JavaScriptをランディングページの先頭に配置することを求めますが、ライトボックス内のフォームの場合は、必要な手順が1つ増えています。

ライトボックス内のフォームは基本的にiFrame内のフォームなので、スクリプトはそのiFrame内に配置されます。

まず、[!UICONTROL lightbox] フォームが存在するiFrameを見つけます。

![](assets/1.png)

次に、[!DNL Marketo Measure] JavaScriptをiFrame内に配置します。

![](assets/2.png)

最後に、JavaScriptが追加されると、次の手順に従ってフォーム送信を追跡しているかどうかを検証します。

1. [!UICONTROL lightbox] フォームを含むランディングページのURLをコピーします。
1. シークレットブラウザーを開き、URLを貼り付けます。
1. 一意の電子メールアドレスを使用してフォームを送信します。
1. 使用した一意のメールアドレスのCRMを確認して、テストが追跡されたことを確認し、タッチポイントデータが入力されていることを確認します。
