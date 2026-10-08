---
unique-page-id: 18874554
description: タッチポイントの生成とマッピング - [!DNL Marketo Measure]
title: 顧客接点の生成とマッピング
exl-id: bb4988f5-4fbc-43b7-9544-da541b8e1d32
feature: Touchpoints
TQID: 'https://experienceleague.adobe.com/otuePoQBPvb-UEJCTI1CeyA1BYQ7Jn-jZQm63si-6uA'
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: 32d2f1bc-61d0-598c-a8bf-f6fbc8920276
    internal-label: Touchpoints
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 98%
---
# 顧客接点の生成とマッピング {#touchpoint-generation-and-mapping}

[!DNL Marketo Measure] アトリビューションストーリーは、次の 2 つのプロセスに依存します。

* 顧客接点の生成：マーケティング活動と営業活動に対する人物のインタラクションを表す顧客接点を作成します。
* 顧客接点のマッピング：顧客接点を適切なチャネルおよびサブチャネルに割り当てます。

[!DNL Marketo Measure] を最大限に活用するには、[!DNL Marketo Measure] の担当者と協力して、組織のニーズに合わせて両方のプロセスをカスタマイズする必要があります。

タッチポイントの生成方法

タッチポイントの生成プロセスでは、「[!DNL Marketo Measure] では、これが発生したことをどのようにして認識するのか？」という質問に回答します。 機能セットと見込み顧客が行うことができるインタラクションのタイプに応じて、[!DNL Marketo Measure] ではインタラクションを検出し、これを表すタッチポイントを作成できる方法が最大 3 つあります。

>[!IMPORTANT]
>
>[!DNL Marketo Measure] では、セッションごとに 1 つのタッチポイントのみを生成します。 複数のフォームに入力している場合は、最初のフォーム入力のみが取り込まれます。

| **インタラクションのタイプ** | **例** | **タッチポイントの生成方法** |
|---|---|---|
| オンライン、サイト上 | フォーム入力 | [!DNL Marketo Measure] JavaScript |
| オフライン、オンライン（貴社サイト上以外） | 展示会では、コンテンツシンジケーションパートナーがコンテンツに関与したリードのリストを提供します | キャンペーンにキャンペーン同期タイプを直接設定するか、[!DNL Marketo Measure] のキャンペーンページでルールを設定することにより、CRM キャンペーンメンバーシップが [!DNL Marketo Measure] に同期されます |
| セールスアクティビティ | SDR によるアウトバウンド呼び出し | CRM アクティビティ（タスクまたはイベント）レコードは、[!DNL Marketo Measure] の[!UICONTROL アクティビティ]ページのロジックを通じて [!DNL Marketo Measure] に同期されます |

タッチポイントのマッピング方法

タッチポイントのマッピングプロセスでは、「このタッチポイントを作成すると、[!DNL Marketo Measure] では、属するチャネルとサブチャネルをどのようにして認識するのか？」という質問に回答します。 顧客接点を生成する各方法には、それぞれ独自の顧客接点マッピング方法があります。

| **インタラクションのタイプ** | **生成方法** | **マッピング方法** |
|---|---|---|
| オンライン、サイト上 | [!DNL Marketo Measure] JavaScript | [!DNL Marketo Measure] の [!DNL Online Channels] ページを通じて、UTM 値、ランディングページ、参照ページ情報を参照します |
| オフライン、オンライン（貴社サイト上以外） | CRM キャンペーンメンバーシップの同期 | [!DNL Marketo Measure] の[!UICONTROL オフラインチャネル]ページを通じて、キャンペーンタイプを参照します |
| セールスアクティビティ | CRM アクティビティの同期 | [!DNL Marketo Measure] の[!UICONTROL オンラインチャネル]ページを通じて、[!UICONTROL アクティビティ]ページで割り当てられたキャンペーン名を参照します |

>[!MORELIKETHIS]
>
>* [ [!DNL Marketo Measure]  チャネル／サブチャネルへのオンラインタッチポイントのマッピング](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md)
>* [SFDC 内からの CRM キャンペーンの同期](/help/channel-tracking-and-setup/offline-channels/legacy-processes/syncing-offline-campaigns.md)
>* [ [!DNL Marketo Measure]](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md) 内からの CRM キャンペーンの同期
>* [ [!DNL Marketo Measure]  チャネル／サブチャネルへの CRM キャンペーンのマッピング](/help/channel-tracking-and-setup/offline-channels/offline-custom-channel-setup.md)
>* [セールスアクティビティからのタッチポイントの作成](/help/advanced-marketo-measure-features/activities-attribution/salesforce-activities-attribution.md)
>* [アクティビティにに関する FAQ と、チャネル／サブチャネルへのアクティビティのタッチポイントのマッピング](/help/advanced-marketo-measure-features/activities-attribution/activities-attribution-faq.md)

