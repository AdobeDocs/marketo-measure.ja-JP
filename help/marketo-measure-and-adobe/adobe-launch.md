---
description: Adobe Launch との [!DNL Marketo Measure] 統合 –  [!DNL Marketo Measure]
title: '[!DNL Marketo Measure] と Adobe Launch の統合'
exl-id: 316ee8a8-b2d3-42e9-9ee5-c9b1d91c2769
feature: Integration
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 4%

---


# [!DNL Marketo Measure] と Adobe Launch の統合 {#marketo-measure-integrations}

Adobe Launch 拡張機能は、web サイトで既にAdobe Launch を使用している既存の [!DNL Marketo Measure] ユーザー向けに設計されています。 拡張機能は、タグ管理ソリューションとして機能し、特定のイベントと条件に基づいて、ページにスクリプトを設定して動的に読み込むことができます。

Adobe Launch にインストールして設定すると、[!DNL Marketo Measure] 拡張機能はAdobe Launch スクリプトが存在するページに bizible.js スクリプトを読み込みます。 これにより、web ページを明示的に変更して bizible.js スクリプトタグを追加するのではなく、マーケターはAdobe Launch 設定を通じて bizible.js を追加することができます。

## Adobe Launch 拡張機能の設定 {#configure-the-adobe-launch-extension}

>[!PREREQUISITES]
>Adobe Launch とその拡張機能について詳しくは、次のリンクを参照してください。
> [[!DNL Marketo Measure] 拡張機能 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email/bizible.html#catalog){target="_blank"}
> [Adobe Launch](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/overview.html?lang=ja){target="_blank"} 概要
> [Adobe Launch 拡張機能の概要 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extension-dev/overview.html){target="_blank"}

1. 手順 [&#x200B; この記事 &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/configure-tags/create-a-property.html#go-to-the-data-collection-interface){target="_blank"} に従ってプロパティを作成します。

1. 作成したプロパティをクリックします。

   ![&#x200B; 使用可能なプロパティを示したAdobe Launch プロパティ選択画面 &#x200B;](assets/marketo-measure-integrations-1.png)

1. 「**[!UICONTROL 拡張機能]**」をクリックします。

   ![Adobe Launch のプロパティ設定の「拡張機能」タブ &#x200B;](assets/marketo-measure-integrations-2.png)

1. 「**[!UICONTROL カタログ]**」タブをクリックし、「[!UICONTROL Bizible]」を検索します。

   ![Bizible 拡張機能を示した拡張機能カタログ検索 &#x200B;](assets/marketo-measure-integrations-3.png)

1. [!UICONTROL Bizible Analytics] タイルで、「**[!UICONTROL インストール]**」をクリックします。

   ![&#x200B; 「インストール」ボタン付き Bizible Analytics 拡張機能タイル &#x200B;](assets/marketo-measure-integrations-4.png)

1. 「Bizible アカウント ID」フィールドに、web サイトの URL を入力します（例：`adobe.com`）。

   ![AccountId フィールドを使用した Bizible 拡張機能の設定 &#x200B;](assets/marketo-measure-integrations-5.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![Bizible 拡張機能設定の「保存」ボタン &#x200B;](assets/marketo-measure-integrations-6.png)

1. **[!UICONTROL ルール]** をクリックし、「**[!UICONTROL 新しいルールの作成]**」を選択します。

   ![&#x200B; 「新規ルールを作成」ボタンを含む「ルール」タブ &#x200B;](assets/marketo-measure-integrations-7.png)

1. **[!UICONTROL イベント]** の下の [!UICONTROL &#x200B; 追加 &#x200B;] ボタンをクリックします。

   ![&#x200B; ルール設定の「イベント」セクションの「追加」ボタン &#x200B;](assets/marketo-measure-integrations-8.png)

1. 「拡張機能」ドロップダウンで、「**[!UICONTROL コア]**」を選択します。 次に、「イベントタイプ」ドロップダウンで、「ライブラリの読み込み **[!UICONTROL ページのトップ）]**」を選択します。 イベントに名前を付けない場合は、デフォルトの名前が適用されます。 完了したら、「**[!UICONTROL 変更を保持]**」をクリックします。

   ![&#x200B; コア拡張機能とライブラリの読み込みイベントタイプを含むイベント設定ダイアログ &#x200B;](assets/marketo-measure-integrations-9.png)

1. 「アクション」の下の **[!UICONTROL 追加]** ボタンをクリックします。

   ![&#x200B; ルール設定の「アクション」セクションの「追加」ボタン &#x200B;](assets/marketo-measure-integrations-10.png)

1. 「拡張機能」ドロップダウンで、「**[!UICONTROL Bizible 分析]**」を選択します。 次に、「アクションタイプ」ドロップダウンで「**[!UICONTROL 初期化]**」を選択します。 アクションに名前を付けない場合は、デフォルトの名前が適用されます。 完了したら、「**[!UICONTROL 変更を保持]**」をクリックします。

   ![Bizible Analytics 拡張機能と初期化アクションタイプを含むアクション設定ダイアログ &#x200B;](assets/marketo-measure-integrations-11.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![&#x200B; ルール設定の「保存」ボタン &#x200B;](assets/marketo-measure-integrations-12.png)

