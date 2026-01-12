---
description: Lightbox Formsへ  [!DNL Marketo Measure]  スクリプトの追加 –  [!DNL Marketo Measure]
title: Lightbox フォームへの [!DNL Marketo Measure] スクリプトの追加
exl-id: fa9ce480-fc4f-4abd-8555-dbb74849747e
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# Lightbox Formsへ [!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script-to-lightbox-forms}

ライトボックス内のフォームに [!DNL Marketo Measure] JavaScriptを適切に追加する方法を説明します。

ライトボックスは、訪問者が特定のアクション（ページの特定の部分のクリックや、ページへの特定の時間の滞在など）を実行すると、コンテンツの前にフォームを開きます。 通常、[!DNL Marketo Measure] JavaScriptをランディングページの先頭に配置する必要がありますが、Lightbox 内のフォームの場合は、追加の手順が 1 つ必要です。

Lightbox 内のフォームは基本的に iFrame 内のフォームなので、スクリプトはその iFrame 内に配置されます。

まず、[!UICONTROL lightbox] フォームが格納されている iFrame を見つけます。

![&#x200B; ページソースでの Lightbox フォーム iFrame の場所 &#x200B;](assets/1.png)

次に、[!DNL Marketo Measure] JavaScriptを iFrame 内に配置します。

![Lightbox iFrame 内に配置されたMarketo Measure スクリプト &#x200B;](assets/2.png)

最後に、JavaScriptが追加されたら、次の手順に従って、フォーム送信が追跡されていることを検証します。

1. [!UICONTROL lightbox] フォームを含むランディングページの URL をコピーします。
1. 匿名ブラウザーを開き、URL を貼り付けます。
1. 一意のメールアドレスを使用してフォームを送信します。
1. CRM で使用されている一意のメールアドレスを確認して、テストが追跡されたことを確認し、タッチポイントデータが入力されていることを確認します。
