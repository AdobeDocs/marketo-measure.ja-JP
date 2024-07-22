---
unique-page-id: 18874732
description: UTM パラメーターの設定のベストプラクティス - [!DNL Marketo Measure]
title: UTM パラメーターの設定のベストプラクティス
exl-id: 56019f41-b6ba-48c1-9bef-2a5f56d2d5f4
feature: UTM Parameters
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 91%

---

# UTM パラメーターの設定のベストプラクティス {#best-practices-for-setting-up-utm-parameters}

UTM パラメーターは、マーケティングデータをスライスしてデータを多角的に分析する優れた方法です。[!DNL Marketo Measure] は、すべての UTM パラメーターを使用して取り込み、Salesforce および [!DNL Marketo Measure] アプリのフィールドに値を入力します。この情報を使用すると、リード、商談、クローズ／獲得した契約の発信元を詳細に把握できます。

[Google URL ビルダー ](https://support.google.com/analytics/answer/1033867?hl=ja){target="_blank"} を使用して UTM パラメーターを設定し、それらをマーケティング活動内のリンクに追加できます。 すべての UTM リンクを簡単に追跡する方法が必要な場合は ](https://docs.google.com/spreadsheets/d/1QCIr1WUJQHE68cA4VTks2XE7nxuryaUymCEy_23-Oew/edit#gid=0){target="_blank"} この [Google スプレッドシートを使用します。

## 各パラメーターの高レベル値 {#high-level-values-for-each-parameter}

**utm_medium**：このフィールドは、「メディア」フィールドにマッピングします。高レベルのチャネルを示すには、utm_medium を使用します。

例：[!UICONTROL Social]、CPC、メール、Web、オーガニック

サブチャネルを呼び出すために、このフィールドを使用しないでください。

**utm_source**：このフィールドは、「タッチポイントソース」フィールドにマッピングします。リードの発信元となるサブチャネルを定義するには、utm_source を使用します。

例：Facebook、Twitter、LinkedIn、Drip_email、Email_blast、ニュースレター。

シンプルにしておきましょう。リターゲティング、スポンサー付きなどの広告タイプを示すために、このパラメーターを使用しないでください。utm_source = homepage、webdirect、website は追加しないでください。[!DNL Marketo Measure] により、この情報は自動的に入力されます。

**utm_campaign**：このフィールドは、広告キャンペーン名にマッピングします。広告プラットフォームに存在するキャンペーンのタイトルや、内部で参照されるキャンペーンのタイトルを示すには、utm_campaign を使用します。

これは、位置情報、広告ネットワークのタイプ（表示と検索）などを示すのに適したパラメーターでもあります。

スペースの代わりにアンダースコアを使用し、句読点の使用は避けることをお勧めします。これにより、パラメーターを読み取る際に、ブラウザーでエンコードエラーが発生する可能性が低くなります。

例：AU_Idea_for_an_App_50k

**utm_content**：これは、広告コンテンツにマッピングします。utm_content パラメーターで広告タイトルを使用します。画像広告の場合は、広告タイトルを使用し、広告の寸法を含めます。

例：[広告タイトル] 200x400px

**utm_term**：これは、キーワードテキストにマッピングします。広告の配信に関連するキーワードを示すには、このパラメーターを使用します。

広告に関連するキーワードがない場合、このパラメーターは空白のままにします。

例：iPhone アプリのアイデア

**シンプルかつ簡潔にしておきましょう。取り組み、用語、チャネルを重複させないでください。**

UTM の階層は、次のようになると想定されます。

メディア／[!UICONTROL ソース]／[!UICONTROL キャンペーン]／[!UICONTROL コンテンツ／用語]

例えば、Facebook に[!UICONTROL ディスプレイ]広告を配置する場合は、次をお勧めします。

fakewebsite.com/

?utm_medium=social

&amp;utm_source=facebook

&amp;utm_campaign=Display_campaign_ID

&amp;utm_content=content_of_campaign

この場合、用語／チャネルは重複せず、utm_term は使用されません。

ご質問がある場合は、アドビのアカウントチーム（担当のアカウントマネージャー）または [Marketo サポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}にお問い合わせください。
