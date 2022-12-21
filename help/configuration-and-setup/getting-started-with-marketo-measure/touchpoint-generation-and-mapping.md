---
unique-page-id: 18874554
description: タッチポイントの生成とマッピング — [!DNL Marketo Measure]  — 製品ドキュメント
title: タッチポイントの生成とマッピング
exl-id: bb4988f5-4fbc-43b7-9544-da541b8e1d32
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# タッチポイントの生成とマッピング {#touchpoint-generation-and-mapping}

[!DNL Marketo Measure] 属性のストーリーは、次の 2 つのプロセスによって決まります。

* タッチポイント生成：マーケティングおよび販売活動との個人のインタラクションを表すタッチポイントを作成します。
* タッチポイントマッピング（適切なチャネルとサブチャネルにタッチポイントをクレジットする）

を最大限に活用するために [!DNL Marketo Measure]を使用する場合、 [!DNL Marketo Measure] 担当者は、組織のニーズに合わせて両方のプロセスをカスタマイズします。

タッチポイント生成方法

タッチポイント生成プロセスは、「 [!DNL Marketo Measure] これが起こった事を知る事になるのか？」 機能セットと、見込み客が持つインタラクションのタイプに応じて、最大 3 つの方法があります [!DNL Marketo Measure] では、インタラクションを取得し、それを表すタッチポイントを作成できます。

| **インタラクションのタイプ** | **例** | **タッチポイント生成方法** |
|---|---|---|
| オンライン、サイト上 | フォームの入力 | [!DNL Marketo Measure] JavaScript |
| オフライン、サイト上にないオンライン | 展示会コンテンツシンジケーションパートナーは、コンテンツに関与したリードのリストを提供します | CRM キャンペーンメンバーシップがに同期されました [!DNL Marketo Measure]キャンペーンで直接キャンペーン同期タイプを設定するか、 [!DNL Marketo Measure] |
| セールスアクティビティ | SDR による発信呼び出し | CRM アクティビティ（タスクまたはイベント）レコードがに同期されました [!DNL Marketo Measure]( [!UICONTROL アクティビティ] ページ内 [!DNL Marketo Measure] |

タッチポイントマッピングメソッド

タッチポイントマッピングプロセスは、「このタッチポイントが作成されたら、どのようにしてがおこなわれるか」という問いに対する回答を提供します [!DNL Marketo Measure] そのチャネルが属するチャネルとサブチャネルを把握しようとしている場合は、 タッチポイント生成の各方法には、タッチポイントマッピングの独自の方法があります。

| **インタラクションのタイプ** | **生成方法** | **マッピング方法** |
|---|---|---|
| オンライン、サイト上 | [!DNL Marketo Measure] JavaScript | を通じて [!DNL Online Channels] ページ内 [!DNL Marketo Measure]（UTM 値、ランディングページ、参照ページ情報を参照） |
| オフライン、オンライン、サイト上にない | CRM キャンペーンメンバーシップの同期 | を通じて [!UICONTROL オフラインチャネル] ページ内 [!DNL Marketo Measure]（キャンペーンタイプを参照） |
| セールスアクティビティ | CRM アクティビティの同期 | を通じて [!UICONTROL オンラインチャネル] ページ内 [!DNL Marketo Measure]( [!UICONTROL アクティビティ] ページ |

>[!MORELIKETHIS]
>
>* [オンラインタッチポイントのマッピング先 [!DNL Marketo Measure] チャネル/サブチャネル](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md)
>* [SFDC 内から CRM キャンペーンを同期中](/help/channel-tracking-and-setup/offline-channels/syncing-offline-campaigns.md)
>* [内から CRM キャンペーンを同期中 [!DNL Marketo Measure]](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md)
>* [CRM キャンペーンのマッピング先 [!DNL Marketo Measure] チャネル/サブチャネル](/help/channel-tracking-and-setup/offline-channels/offline-custom-channel-setup.md)
>* [セールスアクティビティからのタッチポイントの作成](/help/advanced-marketo-measure-features/activities-attribution/salesforce-activities-attribution.md)
>* [アクティビティ FAQ およびアクティビティのマッピングタッチポイントをチャネル/サブチャネルにマッピングします](/help/advanced-marketo-measure-features/activities-attribution/activities-attribution-faq.md)


