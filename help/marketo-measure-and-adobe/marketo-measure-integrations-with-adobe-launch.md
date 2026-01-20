---
description: Adobe Launch との [!DNL Marketo Measure] 統合 –  [!DNL Marketo Measure]
title: '[!DNL Marketo Measure] と Adobe Launch の統合'
exl-id: 316ee8a8-b2d3-42e9-9ee5-c9b1d91c2769
feature: Integration
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 5%

---

# [!DNL Marketo Measure] と Adobe Launch の統合 {#marketo-measure-integrations-with-adobe-launch}

Adobe Launch 拡張機能は、web サイトで既にAdobe Launch を使用している既存の [!DNL Marketo Measure] ユーザー向けに設計されています。 拡張機能は、タグ管理ソリューションとして機能し、特定のイベントと条件に基づいて、ページにスクリプトを設定して動的に読み込むことができます。

Adobe Launch にインストールして設定すると、[!DNL Marketo Measure] 拡張機能はAdobe Launch スクリプトが存在するページに bizible.js スクリプトを読み込みます。 これにより、web ページを明示的に変更して bizible.js スクリプトタグを追加するのではなく、マーケターはAdobe Launch 設定を通じて bizible.js を追加することができます。

## Adobe Launch 拡張機能の設定 {#configure-the-adobe-launch-extension}

>[!PREREQUISITES]
>
>Adobe Launch とその拡張機能について詳しくは、次のリンクを参照してください。
>
>* [[!DNL Marketo Measure]  拡張機能 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email/bizible.html?lang=ja#catalog){target="_blank"}
>* [Adobe Launch の概要 &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/overview.html?lang=ja){target="_blank"}
>* [Adobe Launch 拡張機能の概要 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extension-dev/overview.html?lang=ja){target="_blank"}

1. 手順 [&#x200B; この記事 &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/configure-tags/create-a-property.html?lang=ja#go-to-the-data-collection-interface){target="_blank"} に従ってプロパティを作成します。

1. 作成したプロパティをクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-1.png)

1. 「**[!UICONTROL 拡張機能]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-2.png)

1. 「**[!UICONTROL カタログ]**」タブをクリックし、「[!UICONTROL Bizible]」を検索します。

   ![](assets/marketo-measure-integrations-with-adobe-launch-3.png)

1. [!UICONTROL Bizible Analytics] タイルで、「**[!UICONTROL インストール]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-4.png)

1. 「Bizible アカウント ID」フィールドに、web サイトの URL を入力します（例：`adobe.com`）。

   ![](assets/marketo-measure-integrations-with-adobe-launch-5.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-6.png)

1. **[!UICONTROL ルール]** をクリックし、「**[!UICONTROL 新しいルールの作成]**」を選択します。

   ![](assets/marketo-measure-integrations-with-adobe-launch-7.png)

1. **[!UICONTROL イベント]** の下の [!UICONTROL &#x200B; 追加 &#x200B;] ボタンをクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-8.png)

1. 「拡張機能」ドロップダウンで、「**[!UICONTROL コア]**」を選択します。 次に、「イベントタイプ」ドロップダウンで、「ライブラリの読み込み **[!UICONTROL ページのトップ）]**」を選択します。 イベントに名前を付けない場合は、デフォルトの名前が適用されます。 完了したら、「**[!UICONTROL 変更を保持]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-9.png)

1. 「アクション」の下の **[!UICONTROL 追加]** ボタンをクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-10.png)

1. 「拡張機能」ドロップダウンで、「**[!UICONTROL Bizible 分析]**」を選択します。 次に、「アクションタイプ」ドロップダウンで「**[!UICONTROL 初期化]**」を選択します。 アクションに名前を付けない場合は、デフォルトの名前が適用されます。 完了したら、「**[!UICONTROL 変更を保持]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-11.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-12.png)

