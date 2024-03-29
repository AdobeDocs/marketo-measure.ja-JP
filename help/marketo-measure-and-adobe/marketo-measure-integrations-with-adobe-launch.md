---
description: '[!DNL Marketo Measure] AdobeLaunch との統合 — [!DNL Marketo Measure]'
title: '''[!DNL Marketo Measure] AdobeLaunch との統合`'
exl-id: 316ee8a8-b2d3-42e9-9ee5-c9b1d91c2769
feature: Integration
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 3%

---

# [!DNL Marketo Measure] と Adobe Launch の統合 {#marketo-measure-integrations-with-adobe-launch}

AdobeLaunch 拡張機能は、既存のユーザー向けに設計されています。 [!DNL Marketo Measure] の Web サイトで既にAdobeLaunch を使用しているユーザーのみを対象としています。 拡張機能は、特定のイベントや条件に基づいてページにスクリプトを設定し、動的に読み込むためのタグ管理ソリューションとして機能します。

Launch でインストールおよび設定した場合、AdobeLaunch では、 [!DNL Marketo Measure] 拡張機能は、Launch スクリプトが存在するページに bizible.jsAdobeを読み込みます。 これにより、マーケターは Web ページを明示的に変更して bizible.js スクリプトタグを追加するのに対し、AdobeLaunch 設定を通じて bizible.js を追加できます。

## AdobeLaunch 拡張機能の設定 {#configure-the-adobe-launch-extension}

>[!PREREQUISITES]
>
>Launch とその拡張機能について詳しくは、次のリンクをAdobeしてください。
>
>* [[!DNL Marketo Measure] 拡張](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email/bizible.html#catalog){target="_blank"}
>* [Adobe起動の概要](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/overview.html){target="_blank"}
>* [AdobeLaunch 拡張機能の概要](https://experienceleague.adobe.com/docs/experience-platform/tags/extension-dev/overview.html){target="_blank"}

1. 手順に従ってプロパティを作成します。 [この記事では、](https://experienceleague.adobe.com/docs/platform-learn/implement-in-websites/configure-tags/create-a-property.html#go-to-the-data-collection-interface){target="_blank"}.

1. 作成したプロパティをクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-1.png)

1. 「**[!UICONTROL 拡張機能]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-2.png)

1. 次をクリック： **[!UICONTROL カタログ]** 」タブで、「[!UICONTROL Bizible].&quot;

   ![](assets/marketo-measure-integrations-with-adobe-launch-3.png)

1. Adobe Analytics の [!UICONTROL Bizible Analytics] タイル、クリック **[!UICONTROL インストール]**.

   ![](assets/marketo-measure-integrations-with-adobe-launch-4.png)

1. 「Bizible AccountId」フィールドに、Web サイトの URL を入力します ( 例： `adobe.com`) をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-5.png)

   >[!NOTE]
   >
   >このフィールドは、Business_Prod.Business テーブルの「アカウント ID」ではありません。 指定された URL からのすべての Web アクティビティ ( 例： `adobe.com`) が [!DNL Marketo Measure] テナント。

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-6.png)

1. クリック **[!UICONTROL ルール]**&#x200B;を選択し、「 **[!UICONTROL 新規ルールの作成]**.

   ![](assets/marketo-measure-integrations-with-adobe-launch-7.png)

1. 次をクリック： **[!UICONTROL 追加]** 下のボタン [!UICONTROL イベント].

   ![](assets/marketo-measure-integrations-with-adobe-launch-8.png)

1. 拡張機能ドロップダウンで、「 」を選択します。 **[!UICONTROL コア]**. 次に、「イベントタイプ」ドロップダウンで、「 **[!UICONTROL 読み込まれたライブラリ（ページ上部）]**. イベントに名前を付けない場合、デフォルトの名前が適用されます。 クリック **[!UICONTROL 変更を保持]** 完了したら、

   ![](assets/marketo-measure-integrations-with-adobe-launch-9.png)

1. 次をクリック： **[!UICONTROL 追加]** ボタンをクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-10.png)

1. 「拡張機能」ドロップダウンで、「 」を選択します。 **[!UICONTROL Bizible Analytics]**. 次に、「アクションタイプ」ドロップダウンで、「 **[!UICONTROL 初期設定]**. アクションに名前を付けない場合、デフォルトの名前が適用されます。 クリック **[!UICONTROL 変更を保持]** 完了したら、

   ![](assets/marketo-measure-integrations-with-adobe-launch-11.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/marketo-measure-integrations-with-adobe-launch-12.png)
