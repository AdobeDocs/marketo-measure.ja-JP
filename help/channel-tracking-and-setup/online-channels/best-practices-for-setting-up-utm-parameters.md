---
unique-page-id: 18874732
description: UTM パラメーターの設定のベストプラクティス — [!DNL Marketo Measure]  — 製品ドキュメント
title: UTM パラメーターの設定のベストプラクティス
exl-id: 56019f41-b6ba-48c1-9bef-2a5f56d2d5f4
source-git-commit: 51397a02872035fef41d308c1f855bcaecc29c4e
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 5%

---

# UTM パラメーターの設定のベストプラクティス {#best-practices-for-setting-up-utm-parameters}

UTM パラメーターは、マーケティングデータをスライスしてデータを多角的に分析する優れた方法です。 [!DNL Marketo Measure] は、すべての UTM パラメーターを使用して取り込み、Salesforce のフィールドに、 [!DNL Marketo Measure] アプリを使用します。 この情報を使用して、リード、商談、クローズ/獲得した契約の発信元を詳細に把握できます。

以下を利用できます。 [Google URL Builder](https://support.google.com/analytics/answer/1033867?hl=ja){target="_blank"} to set up your UTM parameters and add them to your links within your marketing efforts. Use this [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1QCIr1WUJQHE68cA4VTks2XE7nxuryaUymCEy_23-Oew/edit#gid=0){target="_blank"} すべての UTM リンクを簡単に追跡する方法が必要な場合。

## 各パラメーターの高レベル値 {#high-level-values-for-each-parameter}

**utm_medium**:このフィールドは、「メディア」フィールドにマッピングされます。 utm_medium を使用して、高レベルのチャネルを示します。

例： [!UICONTROL Social], CPC，メール， Web，オーガニック

このフィールドを使用してサブチャネルを呼び出さないでください。

**utm_source**:このフィールドは、「タッチポイントソース」フィールドにマッピングされます。 utm_source を使用して、リードの発信元となるサブチャネルを定義します。

例： Facebook、Twitter、Linkedin、Drip_email、Email_blast、ニュースレター。

簡単にしておけ。 このパラメーターを使用して、再ターゲティング、スポンサー付きなどの広告のタイプを示さないでください。 utm_source = homepage, webdirect, web サイトは追加しないでください。 [!DNL Marketo Measure] がこの情報を自動的に入力します。

**utm_campaign**:このフィールドは、広告キャンペーン名にマッピングされます。 utm_campaign は、広告プラットフォーム内に存在するキャンペーンのタイトル、または内部的に参照されるキャンペーンのタイトルを示す場合に使用します。

また、これは、位置情報、広告ネットワークタイプ（表示 v 検索）などを示す良いパラメーターです。

スペースの代わりにアンダースコアを使用し、句読点の使用は避けることをお勧めします。 これにより、パラメーターを読み取る際に、ブラウザーでエンコードエラーが発生する可能性が低くなります。

例： AU_Idea_for_an_App_50k

**utm_content**:これは、広告コンテンツにマッピングされます。 utm_content パラメーターで広告タイトルを使用します。 画像広告の場合は、広告タイトルを使用し、広告のサイズを含めます。

例： [広告タイトル] 200x400px

**utm_term**:これは「キーワードテキスト」にマッピングされます。 このパラメーターは、広告の実行に関連するキーワードを示すために使用します。

広告に関連するキーワードがない場合、このパラメーターは空白のままにします。

例： iPhone App Ideas

**簡単で簡潔なものにします。 取り組み、キーワードおよびチャネルを重複させないでください。**

UTM の階層は次のようになると想像します。

メディア > [!UICONTROL ソース] > [!UICONTROL Campaign] > [!UICONTROL コンテンツ/用語]

例： [!UICONTROL 表示] 広告をFacebookに配置する場合は、以下をお勧めします。

fakewebsite.com/

?utm_medium=social

&amp;utm_source=facebook

&amp;utm_campaign=Display_campaign_ID

&amp;utm_content=content_of_campaign

用語/チャネルは重複せず、この場合 utm_term は使用されません。

ご質問がある場合は、Adobeアカウントチーム（担当のアカウントマネージャー）または [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.
