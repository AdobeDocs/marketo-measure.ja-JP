---
description: '''Adobe Launch との [!DNL Marketo Measure] 統合 –  [!DNL Marketo Measure]'''
title: '[!DNL Marketo Measure] と Adobe Launch の統合'
exl-id: 316ee8a8-b2d3-42e9-9ee5-c9b1d91c2769
feature: Integration
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 7%

---

# [!DNL Marketo Measure] と Adobe Launch の統合 {#marketo-measure-integrations-with-adobe-launch}

Adobe Launch 拡張機能は、web サイトで既にAdobe Launch を使用している既存の [!DNL Marketo Measure] ユーザー向けに設計されています。 拡張機能は、タグ管理ソリューションとして機能し、特定のイベントと条件に基づいて、ページにスクリプトを設定して動的に読み込むことができます。

Adobe Launch にインストールして設定すると、[!DNL Marketo Measure] 拡張機能はAdobe Launch スクリプトが存在するページに bizible.js スクリプトを読み込みます。 これにより、web ページを明示的に変更して bizible.js スクリプトタグを追加するのではなく、マーケターはAdobe Launch 設定を通じて bizible.js を追加することができます。

## Adobe Launch 拡張機能の設定 {#configure-the-adobe-launch-extension}

>[!PREREQUISITES]
>
>Adobe Launch とその拡張機能について詳しくは、次のリンクを参照してください。
>
>* [[!DNL Marketo Measure]  拡張機能 ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email/bizible.html#catalog){target="_blank"}
>* [Adobe Launch の概要 ](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/overview.html?lang=ja){target="_blank"}
>* [Adobe Launch 拡張機能の概要 ](https://experienceleague.adobe.com/docs/experience-platform/tags/extension-dev/overview.html){target="_blank"}

1. 手順 [ この記事 ](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/configure-tags/create-a-property.html#go-to-the-data-collection-interface){target="_blank"} に従ってプロパティを作成します。

1. 作成したプロパティをクリックします。

   ![1.作成したプロパティをクリックします。](assets/marketo-launch-12.png)

1. 「**[!UICONTROL 拡張機能]**」をクリックします。

   ![1.「拡張機能」をクリックします。](assets/marketo-launch-11.png)

1. 「**[!UICONTROL カタログ]**」タブをクリックし、「[!UICONTROL Bizible]」を検索します。

   ![1.「Catalog」タブをクリックし、「Bizible」を検索します ](assets/marketo-launch-10.png)

1. [!UICONTROL Bizible Analytics] タイルで、「**[!UICONTROL インストール]**」をクリックします。

   ![1.Bizible Analytics タイルで、「インストール」をクリックします。](assets/marketo-launch-7.png)

1. 「Bizible アカウント ID」フィールドに、web サイトの URL を入力します（例：`adobe.com`）。

   ![1.「Bizible AccountId」フィールドに、](assets/marketo-launch-6.png) の URL を入力します。

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![1.「保存」をクリックします。](assets/marketo-launch-8.png)

1. **[!UICONTROL ルール]** をクリックし、「**[!UICONTROL 新しいルールの作成]**」を選択します。

   ![1.「ルール」をクリックし、「新しいルールの作成」を選択します。](assets/marketo-launch-9.png)

1. **[!UICONTROL イベント]** の下の [!UICONTROL  追加 ] ボタンをクリックします。

   ![1.「イベント」の下の「追加」ボタンをクリックします。](assets/marketo-launch-2.png)

1. 「拡張機能」ドロップダウンで、「**[!UICONTROL コア]**」を選択します。 次に、「イベントタイプ」ドロップダウンで、「ライブラリの読み込み **[!UICONTROL ページのトップ）]**」を選択します。 イベントに名前を付けない場合は、デフォルトの名前が適用されます。 完了したら、「**[!UICONTROL 変更を保持]**」をクリックします。

   ![1.「拡張機能」ドロップダウンで、「コア」を選択します。 次に、イベントで ](assets/marketo-launch-1.png)

1. 「アクション」の下の **[!UICONTROL 追加]** ボタンをクリックします。

   ![1.「アクション」の下の「追加」ボタンをクリックします。](assets/marketo-launch-3.png)

1. 「拡張機能」ドロップダウンで、「**[!UICONTROL Bizible 分析]**」を選択します。 次に、「アクションタイプ」ドロップダウンで「**[!UICONTROL 初期化]**」を選択します。 アクションに名前を付けない場合は、デフォルトの名前が適用されます。 完了したら、「**[!UICONTROL 変更を保持]**」をクリックします。

   ![1.「拡張機能」ドロップダウンで、「Bizible Analytics」を選択します。 次に、アクションで ](assets/marketo-launch-4.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![1.「保存」をクリックします。](assets/marketo-launch-5.png)

