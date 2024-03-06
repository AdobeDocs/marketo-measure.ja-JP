---
description: 支出管理方法 — [!DNL Marketo Measure]
title: 支出管理方法
exl-id: 36478d8d-986c-4d4f-8854-3287d6c57a9d
feature: Spend Management
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 2%

---

# 支出管理方法 {#spend-management-methods}

支出データは、ROI レポートを成功させるための鍵となります。 [!DNL Marketo Measure]. すべてのチャネルとサブチャネルにわたって正確で包括的な ROI レポートを作成するには、適切な支出データをに取り込む必要があります。 [!DNL Marketo Measure].

にデータを費やす方法は 3 つあります。 [!DNL Marketo Measure]. 各方法は、特定のデータ入力から支出データを取り込むように設計されています。

**1 API 接続済みアカウント**

接続している任意の広告アカウント [!DNL Marketo Measure] API を通じての支出は、自動的に [!DNL Marketo Measure] :ROI レポート用。 どのアカウントに接続し、そのために支出を引き出したかを確認するには、 [!DNL Marketo Measure] アプリケーションに移動して、 [!UICONTROL 接続] 」タブをクリックします。 [!UICONTROL 統合] 」セクションに入力します。 API 接続の設定について詳しくは、 [統合広告プラットフォーム](/help/api-connections/utilizing-marketo-measures-api-connections/integrated-ad-platforms.md#how-to-connect-ad-platforms).

**2 CRM キャンペーンコストの同期**

毎 [!DNL Marketo Measure] アカウントは、 [CRM キャンペーンコストを同期](/help/marketing-spend/spend-management/crm-campaign-costs.md#availability). デフォルトでは、この機能ビットは「いいえ」に設定されていますが、いつでもオンにすることができます。

![](assets/spend-management-methods-1.png)

有効にすると、この機能は、次の条件を満たす任意の CRM キャンペーン/プログラムから自動的に取り込みます。

i. [!DNL Marketo Measure] 最初に、Campaign/Program がタッチポイントを作成しているかどうかを調べます。 [キャンペーン同期ルール](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md) 作成された、または一致する [プログラム同期ルール](/help/marketo-measure-and-marketo/marketo-measure-integrations-with-marketo/marketo-engage-programs-integration.md) 作成された、または [購入者タッチポイント値の有効化](/help/channel-tracking-and-setup/offline-channels/legacy-processes/syncing-offline-campaigns.md#how-to-create-a-campaign-and-sync-buyer-touchpoints) は、「すべてのキャンペーンメンバーを含む」または「返信済みのキャンペーンメンバーを含む」です。

ii.開始日をキャンペーン/プログラムに入力する必要があります

iii.終了日をキャンペーン/プログラムに入力する必要があります

iv.実際のコスト（SFDC のキャンペーンの場合）または期間のコスト (Marketoのプログラムの場合 ) を指定する必要があります。

**3 手動コストアップロード**

このメソッドを使用すると、次のことができます。 [支出データを手動でアップロード](/help/marketing-spend/spend-management/marketing-channel-costs.md#uploading-marketing-costs) API 接続アカウントまたは CRM キャンペーンコスト同期でカバーされないチャネルとサブチャネルの場合。 次の手順を実行するには、 [!DNL Marketo Measure] 設定を使用すると、任意のチャネルの支出データを CSV ファイルを使用してアップロードできます。

お客様は、これら 3 つの方法のすべてを組み合わせて、 [!DNL Marketo Measure]. 費用をに輸入する方法は 3 つあるので [!DNL Marketo Measure]を使用する場合は、Discover にあるマーケティング費用ボードを使用して、すべての支出データを包括的に把握することを強くお勧めします。 このボードは、すべてのチャネルとその関連支出を表示できる唯一の場所です。 マーケティング支出委員会は、支出データにギャップが生じる可能性がある場所や、ROI レポートの改善方法をすばやく特定するのに役立ちます。
