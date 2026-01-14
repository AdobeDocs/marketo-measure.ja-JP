---
description: Marketo Measure ユーザー向けのタッチポイントの生成とマッピングガイダンス
title: タッチポイントの生成とマッピング
exl-id: bb4988f5-4fbc-43b7-9544-da541b8e1d32
feature: Touchpoints
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 97%

---

# タッチポイントの生成とマッピング {#touchpoint-generation-and-mapping}

[!DNL Marketo Measure] アトリビューションストーリーは、次の 2 つのプロセスに依存します。

* タッチポイントの生成：マーケティング活動とセールスアクティビティに対する個人のインタラクションを表すタッチポイントを作成します。
* タッチポイントのマッピング：タッチポイントを適切なチャネルおよびサブチャネルに割り当てます。

[!DNL Marketo Measure] を最大限に活用するには、[!DNL Marketo Measure] の担当者と協力して、組織のニーズに合わせて両方のプロセスをカスタマイズする必要があります。

タッチポイントの生成方法

タッチポイントの生成プロセスでは、「[!DNL Marketo Measure] では、これが発生したことをどのようにして認識するのか？」という質問に回答します。機能セットと見込み顧客が行うことができるインタラクションのタイプに応じて、[!DNL Marketo Measure] ではインタラクションを検出し、これを表すタッチポイントを作成できる方法が最大 3 つあります。

>[!IMPORTANT]
>
>[!DNL Marketo Measure] では、セッションごとに 1 つのタッチポイントのみを生成します。複数のフォームに入力している場合は、最初のフォーム入力のみが取り込まれます。

| **インタラクションのタイプ** | **例** | **タッチポイントの生成方法** |
|---|---|---|
| オンライン、サイト上 | フォーム入力 | [!DNL Marketo Measure] JavaScript |
| オフライン、オンライン（貴社サイト上以外） | 展示会：コンテンツシンジケーションパートナーは、コンテンツに関与したリードのリストを提供します | キャンペーンにキャンペーン同期タイプを直接設定するか、[!DNL Marketo Measure] のキャンペーンページでルールを設定することにより、CRM キャンペーンメンバーシップが [!DNL Marketo Measure] に同期されます |
| セールスアクティビティ | SDR によるアウトバウンド呼び出し | CRM アクティビティ（タスクまたはイベント）レコードは、[!DNL Marketo Measure] の[!UICONTROL アクティビティ]ページのロジックを通じて [!DNL Marketo Measure] に同期されます |

タッチポイントのマッピング方法

タッチポイントのマッピングプロセスでは、「このタッチポイントを作成すると、[!DNL Marketo Measure] では、属するチャネルとサブチャネルをどのようにして認識するのか？」という質問に回答します。タッチポイントの生成の各方法には、独自のタッチポイントのマッピング方法があります。

| **インタラクションのタイプ** | **生成方法** | **マッピング方法** |
|---|---|---|
| オンライン、サイト上 | [!DNL Marketo Measure] JavaScript | [!DNL Marketo Measure] の [!DNL Online Channels] ページを通じて、UTM 値、ランディングページ、参照ページ情報を参照します |
| オフライン、オンライン（貴社サイト上以外） | CRM キャンペーンメンバーシップの同期 | [!DNL Marketo Measure] の[!UICONTROL オフラインチャネル]ページを通じて、キャンペーンタイプを参照します |
| セールスアクティビティ | CRM アクティビティの同期 | [!DNL Marketo Measure] の[!UICONTROL オンラインチャネル]ページを通じて、[!UICONTROL アクティビティ]ページで割り当てられたキャンペーン名を参照します |

>[!MORELIKETHIS]
>
>* [&#x200B; [!DNL Marketo Measure]  チャネル／サブチャネルへのオンラインタッチポイントのマッピング](/help/channel-tracking-and-setup/online-custom-channel-setup.md)
>* [SFDC 内からの CRM キャンペーンの同期](/help/channel-tracking-and-setup/syncing-offline-campaigns.md)
>* [&#x200B; [!DNL Marketo Measure]](/help/channel-tracking-and-setup/custom-campaign-sync.md) 内からの CRM キャンペーンの同期
>* [&#x200B; [!DNL Marketo Measure]  チャネル／サブチャネルへの CRM キャンペーンのマッピング](/help/channel-tracking-and-setup/offline-custom-channel-setup.md)
>* [セールスアクティビティからのタッチポイントの作成](/help/channel-tracking-and-setup/salesforce-activities-attribution.md)
>* [アクティビティにに関する FAQ と、チャネル／サブチャネルへのアクティビティのタッチポイントのマッピング](/help/channel-tracking-and-setup/activities-attribution-faq.md)

