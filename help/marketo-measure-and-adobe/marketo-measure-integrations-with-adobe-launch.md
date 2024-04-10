---
description: '[!DNL Marketo Measure] Adobe Launch との統合 –  [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] Adobeローンチとの統合'
exl-id: 316ee8a8-b2d3-42e9-9ee5-c9b1d91c2769
feature: Integration
source-git-commit: 6aaf6fd26f19e9382cc559e54558e1c5d84cfd6d
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 3%

---

# [!DNL Marketo Measure] と Adobe Launch の統合 {#marketo-measure-integrations-with-adobe-launch}

Adobeローンチ拡張機能は、既存ので使用できるように設計されています [!DNL Marketo Measure] web サイトで既にAdobeローンチを使用しているユーザー。 拡張機能は、タグ管理ソリューションとして機能し、特定のイベントと条件に基づいて、ページにスクリプトを設定して動的に読み込むことができます。

Adobeの Launch にインストールして設定する場合、 [!DNL Marketo Measure] Adobeは、拡張機能 Launch スクリプトが存在するページに bizible.js スクリプトを読み込みます。 これにより、web ページを明示的に修正して bizible.js スクリプトタグを追加するのではなく、マーケターはAdobeローンチ設定を通じて bizible.js を追加することができます。

## Adobe Launch 拡張機能の設定 {#configure-the-adobe-launch-extension}

>[!PREREQUISITES]
>
>Adobeローンチとその拡張機能について詳しくは、次のリンクを参照してください。
>
>* [[!DNL Marketo Measure] 拡張機能](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email/bizible.html#catalog){target="_blank"}
>* [Adobeローンチの概要](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/overview.html){target="_blank"}
>* [AdobeLaunch 拡張機能の概要](https://experienceleague.adobe.com/docs/experience-platform/tags/extension-dev/overview.html){target="_blank"}

1. 手順に従ってプロパティを作成します [この記事の](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/configure-tags/create-a-property.html#go-to-the-data-collection-interface){target="_blank"}.

1. 作成したプロパティをクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-1.png)

1. 「**[!UICONTROL 拡張機能]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-2.png)

1. 「」をクリックします **[!UICONTROL カタログ]** タブで「」を検索[!UICONTROL Bizible].」と入力します。

   ![](assets/marketo-measure-integrations-with-adobe-launch-3.png)

1. が含まれる [!UICONTROL Bizible Analytics] タイル、クリック **[!UICONTROL インストール]**.

   ![](assets/marketo-measure-integrations-with-adobe-launch-4.png)

1. 「Bizible アカウント ID」フィールドに、web サイトの URL を入力します（例： `adobe.com`）に設定します。

   ![](assets/marketo-measure-integrations-with-adobe-launch-5.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-6.png)

1. クリック **[!UICONTROL ルール]**&#x200B;を選択してから、 **[!UICONTROL 新しいルールの作成]**.

   ![](assets/marketo-measure-integrations-with-adobe-launch-7.png)

1. 「」をクリックします **[!UICONTROL 追加]** 下のボタン [!UICONTROL イベント].

   ![](assets/marketo-measure-integrations-with-adobe-launch-8.png)

1. 「拡張機能」ドロップダウンで、次を選択します **[!UICONTROL コア]**. 次に、「イベントタイプ」ドロップダウンで、を選択します。 **[!UICONTROL ライブラリが読み込まれました（ページのトップ）]**. イベントに名前を付けない場合は、デフォルトの名前が適用されます。 クリック **[!UICONTROL 変更を保持]** 完了した場合。

   ![](assets/marketo-measure-integrations-with-adobe-launch-9.png)

1. 「」をクリックします **[!UICONTROL 追加]** ボタンはアクションの下にあります。

   ![](assets/marketo-measure-integrations-with-adobe-launch-10.png)

1. 拡張子ドロップダウンで、 **[!UICONTROL Bizible Analytics]**. 次に、「アクションタイプ」ドロップダウンで以下を選択します。 **[!UICONTROL Initialize]**. アクションに名前を付けない場合は、デフォルトの名前が適用されます。 クリック **[!UICONTROL 変更を保持]** 完了した場合。

   ![](assets/marketo-measure-integrations-with-adobe-launch-11.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-12.png)

