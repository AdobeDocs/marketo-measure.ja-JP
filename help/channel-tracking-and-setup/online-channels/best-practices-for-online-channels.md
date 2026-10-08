---
description: オンライン チャネルのベストプラクティス - [!DNL Marketo Measure]
title: オンラインチャネルのベストプラクティス
exl-id: 766cb01c-98b3-492d-bb35-e0a78b76333a
feature: Channels
TQID: 'https://experienceleague.adobe.com/USJRMuxX8gBPFwCYWb5ujG-158EWyVpwwy47studXK0'
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: c8f57308-7e33-4e41-a385-b55041c78939
    internal-label: Integrations
  - id: 60acc924-ea94-5885-b419-e793b9682efd
    internal-label: Channels
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 99%
---
# オンラインチャネルのベストプラクティス {#best-practices-for-online-channels}

## 概要 {#overview}

正確な [!DNL Marketo Measure] レポートを作成するには、マーケティングチャネルが正しく設定されている必要があります。 「マーケティングチャネル」フィールドには、顧客接点が属することのできるマーケティングアクティビティの最上位のグループが表示されます（有料検索、ダイレクト、ソーシャルなど）。

マーケティングチャネルの設定には、オンラインとオフラインの 2 つの側面があります。 このドキュメントでは、オンラインチャネルの設定と維持に関する [!DNL Marketo Measure] のベストプラクティスのレコメンデーションに焦点を当てます。

オンラインチャネルルールとは、[!DNL Marketo Measure] がデジタルタッチポイント、つまりサイト上の [!DNL Marketo Measure] JS を介して追跡および作成されるタッチポイントをマッピングする方法に関するガイドラインです。 これらのルールが包括的でない場合、または正しく順序付けされていない場合、顧客接点が誤ったチャネルに割り当てられ、レポートの精度が低下します。 オンラインチャネルルールが正確かつ最新であることを確認すると、デジタルデータが [!DNL Marketo Measure] レポートで正しいチャネルとサブチャネルに関連付けられることが保証されます。

## ベストプラクティス {#best-practice}

ルールを初めて設定する場合でも、ルールが正確かどうかを確認するために単にレビューする場合でも、次のベストプラクティスに留意してください。

マーケティングキャンペーンの組織と、それが [!DNL Marketo Measure] フレームワークにどのように適合するかを、じっくり考えてみてください。 オンラインチャネルとしてどのチャネルとサブチャネルを設定するかを決定し、それらのチャネルを互いに区別するキャンペーン、UTM パラメーター、参照元 web サイトが何かを特定します。

留意点：

* すべてのデジタルチャネルとサブチャネルは、少なくとも 1 つのルールで表される必要がある
  * チャネルが訪問者をサイトに誘導しない場合、それはオンラインチャネルではありません
* 1 つのチャネル／サブチャネルに対して複数のルールを設定しても問題ない
  * 複数のルールは、各顧客接点が正しくマッピングされるように「網を広く張る」イメージと考えることができます。 多くの場合、パラメーターが正しく追加されない、または完全に欠落する可能性があるので、マッピングの正確性を確保するには、チャネル／サブチャネルをキャプチャするための複数のルールを用意するとよいでしょう。
* [!DNL Marketo Measure] ロジックは、スプレッドシートの一番上の行から下に向かって降順で、タッチポイントマッピングに優先順位を付ける
  * [!DNL Marketo Measure] は各ルール（行）を読み取り、true の最初の適合を探します。 その後、タッチポイントがそのチャネル／サブチャネルにマッピングされます
  * 論理ルールに干渉するので、シートをアルファベット順で並べ替えないでください。
* 括弧付きのルールを維持し、括弧付きのルールを編集したり追加したりしない（例：[AdWords 有料検索]または [Facebook 有料検索]）
  * これらは、[!DNL Marketo Measure] 統合に関連付けられたビルトインのロジックを持つ、すぐに使用できる [!DNL Marketo Measure] ルールです。 [!DNL Marketo Measure] 統合は設計どおりに動作できるように、これらのルールをそのチャネル／サブチャネルセクションで最優先に設定します。
* ファイルがアップロードされると、7 日間はルールを変更できない
  * [!DNL Marketo Measure] では、この時間を利用してタッチポイントを処理および更新するので、アップロードする前に必ずルールを再確認すること。

## メンテナンスのベストプラクティス {#best-practice-for-maintenace}

オンラインチャネルルールは、保存および処理した後、デジタルタッチポイントをバケット化するために引き続き機能します。 ただし、特定の変更やシナリオにより、オンラインチャネルの設定を見直す必要が生じます。 [!DNL Marketo Measure] では、6 か月に 1 回、オンラインチャネルルールを見直すことをお勧めします。 これにより、[!DNL Marketo Measure] データがオンラインチャネル／サブチャネルの内部定義および UTM の使用状況と一致します。

チームがオンラインチャネルのメンテナンスを行うきっかけとなる可能性のある、その他の項目を以下に示します。

* 新しいデジタルチャネル／サブチャネルのローンチ
* UTM パラメーターの更新または変更
* チャネル組織または命名規則の変更
* マーケティングチームの入れ替わり

チームが最近上記のいずれかを経験した場合、[!DNL Marketo Measure] ではオンラインチャネルのルールを確認し、適切な変更を行うことをお勧めします。

>[!MORELIKETHIS]
>
>* [オンラインチャネルの設定](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md)
>* [UTM パラメーター](/help/channel-tracking-and-setup/online-channels/utm-parameters.md)
>* [マーケティングチャネルとサブチャネル](/help/channel-tracking-and-setup/online-channels/marketing-channels-and-subchannels.md)
>* [UTM のベストプラクティス](/help/channel-tracking-and-setup/online-channels/best-practices-for-setting-up-utm-parameters.md)
