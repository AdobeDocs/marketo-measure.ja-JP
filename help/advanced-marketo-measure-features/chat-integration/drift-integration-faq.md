---
unique-page-id: 27656441
description: Drift 統合に関する FAQ - [!DNL Marketo Measure]
title: Drift 統合に関するよくある質問
exl-id: ae5706b1-1f6c-4201-8585-0d7c587746e1
feature: Integration
source-git-commit: 741ab20845de2f3bcde589291d7446a5b4f877d8
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 2%

---

# Drift 統合に関するよくある質問 {#drift-integration-faq}

の一部として [!DNL Marketo Measure] Drift との統合に関して、最もよくある質問を以下に示します。 以下に概要がない質問がある場合は、Adobeアカウントチーム（担当のアカウントマネージャー）にお問い合わせください。または [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.

**統合はどのように有効になっていますか？**

Drift Chat 追跡対象 [!DNL Marketo Measure] はデフォルトで有効になっています。 無効にする（デフォルトでは Drift Chats からタッチポイントを作成しない）場合は、 [!DNL Marketo Measure] JavaScript 実装。次の太字で示します。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" id="bizible-settings" data-chatEnabled="false"></script>`

を使用しているユーザー向け [!DNL Google Tag Manager] 荷を積む [!DNL Marketo Measure] スクリプトを使用して、タッチポイント対象から Drift チャットを除外する場合は、次にを追加します。 `<span>` あなたの [!DNL Marketo Measure] スクリプト：

`<span id="bizible-settings" data-chatEnabled="false"></span>`

**統合の機能**

統合で、 [!DNL Marketo Measure] エンドユーザが Drift チャットでいつメールアドレスを提供したかを追跡する。 ここから、「Web チャット」のタッチポイントタイプを持つこれらのインタラクションからタッチポイントを作成します。 この統合により、マーケターは、チャットとのやり取りを促すチャネル/サブチャネル/キャンペーンと共に、チャットのインタラクションのパフォーマンスを理解できます。

**キャンペーン同期ルールを使用して Drift を追跡した場合はどうなりますか？**

Drift チャットインタラクション用のタッチポイントを作成するためのキャンペーン同期ルールが設定されている場合は、該当するエンドユーザーを対応する CRM キャンペーンに追加しないようにしてください。 それ以外の場合は、機能ビットが有効になったら、1 つの Drift チャットインタラクション用に CRM キャンペーンタッチポイントとデジタルタッチポイントを作成します。

**CRM キャンペーンを介して Drift を追跡する場合はどうなりますか？**

Drift チャットインタラクション用のタッチポイントを作成する CRM キャンペーンがある場合は、それらの特定のキャンペーンにタッチポイント終了日を設定する必要があります（タッチポイント終了日は、ウェブチャット統合機能ビットが有効な日付です）。

**アクティビティを介して Drift を追跡する場合はどうなりますか？**

Drift チャットインタラクション用のタッチポイントを作成するアクティビティルールがある場合は、ルールに別のロジックを追加する必要があります。 タッチポイントの重複が作成されるのを防ぐために、「タスク作成日」フィールドを使用してロジックを追加します（IE CrmTask.CreatedDate は、機能ビットが有効になった日付よりも小さい）。 例については、以下のスクリーンショットを参照してください。

![](assets/activity-rule-drift.png)
