---
description: Adobe Launchとの'[!DNL Marketo Measure]統合 –  [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] と Adobe Launch の統合'
exl-id: 316ee8a8-b2d3-42e9-9ee5-c9b1d91c2769
feature: Integration
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 8%

---

# [!DNL Marketo Measure] と Adobe Launch の統合 {#marketo-measure-integrations-with-adobe-launch}

Adobe Launch拡張機能は、web サイトで既にAdobe Launchを使用している既存の[!DNL Marketo Measure]人のユーザー向けに設計されています。 この拡張機能は、特定のイベントと条件に基づいてページ上のスクリプトを設定および動的に読み込むためのタグ管理ソリューションとして機能します。

Adobe Launchにインストールして設定すると、[!DNL Marketo Measure]拡張機能は、Adobe Launch スクリプトが存在するページにbizible.js スクリプトを読み込みます。 これにより、マーケターは、web ページを明示的に変更してbizible.js スクリプトタグを追加するのではなく、Adobe Launch設定を使用してbizible.jsを追加できます。

## Adobe Launch拡張機能の設定 {#configure-the-adobe-launch-extension}

>[!PREREQUISITES]
>
>Adobe Launchとその拡張機能について詳しくは、次のリンクを参照してください。
>
>* [[!DNL Marketo Measure] 拡張機能](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email/bizible.html#catalog){target="_blank"}
>* [Adobe Launchの概要](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/overview.html?lang=ja){target="_blank"}
>* [Adobe Launch拡張機能の概要](https://experienceleague.adobe.com/docs/experience-platform/tags/extension-dev/overview.html){target="_blank"}

1. この記事[&#128279;](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/configure-tags/create-a-property.html#go-to-the-data-collection-interface){target="_blank"}の手順に従ってプロパティを作成します。

1. 作成したプロパティをクリックします。

   ![1. 作成したプロパティをクリックします。](assets/marketo-launch-12.png)

1. 「**[!UICONTROL 拡張機能]**」をクリックします。

   ![1. 拡張機能をクリックします。](assets/marketo-launch-11.png)

1. 「**[!UICONTROL カタログ]**」タブをクリックし、「[!UICONTROL Bizible]」を検索します。

   ![1. 「カタログ」タブをクリックし、「Bizible」を検索します。](assets/marketo-launch-10.png)

1. [!UICONTROL Bizible Analytics] タイルで、**[!UICONTROL インストール]**&#x200B;をクリックします。

   ![1. Bizible Analytics タイルで、「インストール」をクリックします。](assets/marketo-launch-7.png)

1. Bizible AccountId フィールドに、web サイトのURLを入力します（例：`adobe.com`）。

   ![1. Bizible AccountId フィールドに、](assets/marketo-launch-6.png)のURLを入力します

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![1. 「保存」をクリックします。](assets/marketo-launch-8.png)

1. 「**[!UICONTROL ルール]**」をクリックし、「**[!UICONTROL 新しいルールを作成]**」を選択します。

   ![1. 「ルール」をクリックし、「新しいルールを作成」を選択します。](assets/marketo-launch-9.png)

1. 「[!UICONTROL &#x200B; イベント &#x200B;]」の下にある「**[!UICONTROL 追加]**」ボタンをクリックします。

   ![1. イベントの下の「追加」ボタンをクリックします。](assets/marketo-launch-2.png)

1. 拡張機能ドロップダウンで、**[!UICONTROL Core]**&#x200B;を選択します。 次に、「イベントタイプ」ドロップダウンで、「**[!UICONTROL ライブラリ読み込み（ページトップ）]**」を選択します。 イベントに名前を付けないと、デフォルトの名前が適用されます。 完了したら、**[!UICONTROL 変更を保持]**&#x200B;をクリックします。

   ![1. 拡張機能ドロップダウンで、「コア」を選択します。 イベント &#x200B;](assets/marketo-launch-1.png)で

1. 「アクション」の「**[!UICONTROL 追加]**」ボタンをクリックします。

   ![1. アクションの下にある「追加」ボタンをクリックします。](assets/marketo-launch-3.png)

1. 拡張機能ドロップダウンで、**[!UICONTROL Bizible Analytics]**&#x200B;を選択します。 次に、「アクションタイプ」ドロップダウンで、「**[!UICONTROL 初期化]**」を選択します。 アクションに名前を付けないと、デフォルトの名前が適用されます。 完了したら、**[!UICONTROL 変更を保持]**&#x200B;をクリックします。

   ![1. 拡張機能ドロップダウンで、「Bizible Analytics」を選択します。 次に、アクション &#x200B;](assets/marketo-launch-4.png)で

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![1. 「保存」をクリックします。](assets/marketo-launch-5.png)

