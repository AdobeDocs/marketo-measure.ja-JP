---
unique-page-id: 18874519
description: 追加中 [!DNL Marketo Measure] Lightbox Formsへのスクリプト — [!DNL Marketo Measure]
title: Lightbox フォームへの [!DNL Marketo Measure] スクリプトの追加
exl-id: fa9ce480-fc4f-4abd-8555-dbb74849747e
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# 追加中 [!DNL Marketo Measure] スクリプトを Lightbox Formsに {#adding-marketo-measure-script-to-lightbox-forms}

を適切に追加する方法を学ぶ [!DNL Marketo Measure] Lightbox 内のフォームに JavaScript を追加する。

Lightbox は、訪問者が特定のアクションを実行する（つまり、ページの特定の部分をクリックして、ページに一定時間を費やすなど）と、コンテンツの前にフォームを開きます。 通常は、 [!DNL Marketo Measure] JavaScript はランディングページの head に配置されていますが、Lightbox 内のフォームの場合は、追加の手順が 1 つ必要です。

Lightbox 内のフォームは基本的に iFrame 内のフォームなので、スクリプトはその iFrame 内に配置されます。

まず、 [!UICONTROL ライトボックス] 住む場所を形成する。

![](assets/1.png)

次に、 [!DNL Marketo Measure] iFrame 内の JavaScript。

![](assets/2.png)

最後に、JavaScript が追加されると、次の指示に従ってフォーム送信の検証が追跡されます。

1. 次を含むランディングページの URL をコピー [!UICONTROL ライトボックス] フォーム。
1. 匿名ブラウザーを開き、URL を貼り付けます。
1. 一意の電子メールアドレスを使用してフォームを送信します。
1. 使用する一意の電子メールアドレスが CRM で確認し、テストが追跡されたことを確認します。タッチポイントデータが入力されていることを確認します。
