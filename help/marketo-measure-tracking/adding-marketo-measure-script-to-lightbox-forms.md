---
description: Marketo Measure ユーザー向けLightbox Forms ガイダンスへの [!DNL Marketo Measure] Scriptの追加
title: Lightbox フォームへの [!DNL Marketo Measure] スクリプトの追加
exl-id: fa9ce480-fc4f-4abd-8555-dbb74849747e
feature: Tracking
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# Lightbox Formsへの[!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-to-lightbox-forms}

ライトボックス内のフォームに[!DNL Marketo Measure] JavaScriptを適切に追加する方法について説明します。

ライトボックスは、訪問者が特定のアクション（ページの特定の部分をクリックしたり、ページで特定の時間を過ごしたりなど）を実行すると、コンテンツの前にフォームを開きます。 通常、[!DNL Marketo Measure] JavaScriptをランディングページの先頭に配置することを求めますが、ライトボックス内のフォームの場合は、必要な手順が1つ増えています。

ライトボックス内のフォームは基本的にiFrame内のフォームなので、スクリプトはそのiFrame内に配置されます。

まず、[!UICONTROL lightbox] フォームが存在するiFrameを見つけます。

![まず、Lightbox フォームが存在するiFrameを探します。](assets/adding-providers-8.png)

次に、[!DNL Marketo Measure] JavaScriptをiFrame内に配置します。

![次に、Marketo Measure JavaScriptをiFrame内に配置します。](assets/adding-providers-5.png)

最後に、JavaScriptが追加されると、次の手順に従ってフォーム送信を追跡しているかどうかを検証します。

1. [!UICONTROL lightbox] フォームを含むランディングページのURLをコピーします。
1. シークレットブラウザーを開き、URLを貼り付けます。
1. 一意の電子メールアドレスを使用してフォームを送信します。
1. 使用した一意のメールアドレスのCRMを確認して、テストが追跡されたことを確認し、タッチポイントデータが入力されていることを確認します。
