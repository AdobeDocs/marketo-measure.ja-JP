---
description: Marketo Measure ユーザー向け Drift Integration FAQ ガイダンス
title: Drift 統合に関するよくある質問
exl-id: ae5706b1-1f6c-4201-8585-0d7c587746e1
feature: Integration
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# Drift 統合に関するよくある質問 {#drift-integration-faq}

ドリフトとの [!DNL Marketo Measure] 統合の一環として、最もよくある質問のいくつかを以下に示します。 以下に記載されていないご質問については、Adobe アカウントチーム（アカウントマネージャー）または [Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。

**統合はどのように有効になりますか？**

[!DNL Marketo Measure] のドリフトチャットトラッキングは、デフォルトで有効になっています。 これを無効にする（デフォルトでドリフトチャットからタッチポイントを作成しない）場合は、[!DNL Marketo Measure] JavaScript 実装に追加の属性（下図を参照）を追加します。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async="" id="bizible-settings" data-chatEnabled="false"></script>`

[!DNL Google Tag Manager] を使用して [!DNL Marketo Measure] スクリプトを読み込む場合、ドリフトチャットをタッチポイント適格から除外するには、`<span>` スクリプトの直後に次の [!DNL Marketo Measure] を追加します。

`<span id="bizible-settings" data-chatEnabled="false"></span>`

**統合の機能**

この統合により、エンドユーザーが Drift [!DNL Marketo Measure] ャットで自分のメールアドレスを提供したタイミングを追跡できるようになりました。 そこから、タッチポイントタイプの「web チャット」で、これらのインタラクションからタッチポイントを作成します。 この統合により、マーケターは、チャットインタラクションのパフォーマンスと、ユーザーがこれらのチャットを操作できるようにするチャネル/サブチャネル/キャンペーンを理解できます。

**キャンペーン同期ルールを使用してドリフトを追跡するとどうなりますか？**

ドリフトチャットインタラクションのタッチポイントを作成するためのキャンペーン同期ルールが設定されている場合は、それらの特定のエンドユーザーを対応する CRM キャンペーンに追加しないようにしてください。 そうでない場合は、機能ビットが有効になったら、1 つの Drift チャットインタラクション用に CRM キャンペーンタッチポイントとデジタルタッチポイントを作成します。

**CRM キャンペーンを使用してドリフトを追跡するとどうなりますか？**

ドリフトチャットインタラクションのタッチポイントを作成する CRM キャンペーンが存在する場合は、それらの特定のキャンペーンにタッチポイント終了日を設定する必要があります（タッチポイント終了日は、web チャット統合機能ビットが有効になっている日付である必要があります）。

**アクティビティを使用してドリフトを追跡するとどうなりますか？**

ドリフトチャットインタラクションのタッチポイントを作成するアクティビティルールが設定されている場合は、ルールにロジックを追加する必要があります。 タッチポイントの重複を防ぐために、タスク作成日フィールドを使用してロジックを追加します（つまり、CrmTask.CreatedDate が機能ビットが有効だった日付より前の日付です）。 例として、以下のスクリーンショットを参照してください。

![ ドリフトのタッチポイントを作成するアクティビティルールが設定されている場合 ](assets/chat-integration-1.png)
