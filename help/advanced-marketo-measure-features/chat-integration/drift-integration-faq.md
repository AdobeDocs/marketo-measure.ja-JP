---
unique-page-id: 27656441
description: Drift 統合に関する FAQ - [!DNL Marketo Measure]  — 製品ドキュメント
title: Drift 統合に関するよくある質問
exl-id: ae5706b1-1f6c-4201-8585-0d7c587746e1
feature: Integration
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 3%

---

# Drift 統合に関するよくある質問 {#drift-integration-faq}

の一部として [!DNL Marketo Measure] Drift との統合に関して、最もよくある質問のいくつかを概説しました。 以下に概要を示さないご質問がある場合は、Adobeアカウントチーム（担当のアカウントマネージャー）にお問い合わせください。または [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.

**統合はどのように有効になっていますか？**

Drift Chat 追跡対象 [!DNL Marketo Measure] はデフォルトで有効になっています。 何らかの理由で無効にしたい場合（デフォルトでは Drift Chats からタッチポイントを作成しない場合）、 [!DNL Marketo Measure] JavaScript 実装。次の太字で示します。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" id="bizible-settings" data-chatEnabled="false"></script>`

を使用しているユーザー向け [!DNL Google Tag Manager] 荷を積む [!DNL Marketo Measure] スクリプトを使用すると、Drift チャットをタッチポイント対象から除外する場合は、次の項目を追加する必要があります `<span>` あなたの [!DNL Marketo Measure] スクリプト：

`<span id="bizible-settings" data-chatEnabled="false"></span>`

**統合の機能**

統合で、 [!DNL Marketo Measure] エンドユーザが Drift チャットでいつメールアドレスを提供したかを追跡する。 ここから、「Web チャット」のタッチポイントタイプを持つこれらのインタラクションからタッチポイントを作成します。 この統合により、マーケターは、チャットとのやり取りを促すチャネル/サブチャネル/キャンペーンと共に、チャットのインタラクションのパフォーマンスを理解できます。

**キャンペーン同期ルールを使用して Drift を追跡した場合はどうなりますか？**

Drift チャットインタラクション用のタッチポイントを作成するキャンペーン同期ルールが設定されている場合は、該当するエンドユーザーを対応する CRM キャンペーンに追加するのを確実に停止する必要があります。 それ以外の場合は、機能ビットが有効になった後、1 つの Drift チャットインタラクション用に CRM キャンペーンタッチポイントとデジタルタッチポイントを作成します。

**CRM キャンペーンを介して Drift を追跡する場合はどうなりますか？**

Drift チャットインタラクション用のタッチポイントを作成する CRM キャンペーンがある場合は、タッチポイント終了日をそれらの特定のキャンペーンに設定する必要があります（タッチポイント終了日は、Web チャット統合機能ビットが有効な日付です）。

**アクティビティを介して Drift を追跡する場合はどうなりますか？**

Drift チャットインタラクション用のタッチポイントを作成するアクティビティルールがある場合は、追加のロジックをルールに追加する必要があります。 タッチポイントの重複が作成されるのを防ぐには、「タスク作成日」フィールドを使用してロジックを追加する必要があります（IE CrmTask.CreatedDate は、機能ビットが有効になった日付よりも小さい）。 例については、以下のスクリーンショットを参照してください。

![](assets/activity-rule-drift.png)
