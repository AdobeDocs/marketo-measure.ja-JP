---
unique-page-id: 18874519
description: 追加中 [!DNL Marketo Measure] Lightbox Formsへのスクリプト — [!DNL Marketo Measure]  — 製品ドキュメント
title: 追加中 [!DNL Marketo Measure] スクリプトを Lightbox Formsに
exl-id: fa9ce480-fc4f-4abd-8555-dbb74849747e
source-git-commit: ae5b77744d523606ce6cfcf48d7e8d5049d5ccb7
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# 追加中 [!DNL Marketo Measure] スクリプトを Lightbox Formsに {#adding-marketo-measure-script-to-lightbox-forms}

適切に [!DNL Marketo Measure] Lightbox 内のフォームに JavaScript を追加する。

Lightbox は、訪問者が特定のアクションを実行する（例えば、ページの特定の部分をクリックする、ページ上で一定期間を過ごすなど）と、コンテンツの前にフォームを開きます。 通常は、 [!DNL Marketo Measure] JavaScript はランディングページの head に配置されていますが、Lightbox 内のフォームの場合は、追加の手順が 1 つ必要です。

Lightbox 内のフォームは基本的に iFrame 内のフォームなので、その iFrame 内にスクリプトを配置する必要があります。

まず、 [!UICONTROL ライトボックス] 生きる。

![](assets/1.png)

次に、 [!DNL Marketo Measure] iFrame 内の JavaScript。

![](assets/2.png)

最後に、JavaScript が追加されたら、次の指示に従ってフォーム送信が追跡されていることを検証することをお勧めします。

1. 次を含むランディングページの URL をコピー [!UICONTROL ライトボックス] フォーム。
1. 匿名ブラウザーを開き、URL を貼り付けます。
1. 一意の電子メールアドレスを使用してフォームを送信します。
1. 使用している一意の電子メールアドレスが CRM で確認し、テストが追跡されたことを確認します。タッチポイントデータが入力されていることを確認します。
